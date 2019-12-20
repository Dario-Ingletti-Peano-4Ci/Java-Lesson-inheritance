# Java-Lesson-inheritance
Ereditarieta' in Java

Il codice [MyCar.java](https://github.com/Prof-Matteo-Palitto-Peano/Java-Lesson-inheritance/blob/master/MyCar.java) vuole illustrare i concetti legati all'ereitarieta' in Java.

## Architettura del Codice
* La SUPER-CLASSE **Veicolo**
* La SOTTO-CLASSE **Auto** che eredita dalla classe **Veicolo** tutte le sue variabili e tutte i suoi metodi
* Nel **main** viene instanziato l'oggetto **myFastCar** di tipo **Auto**

## Concetti evidenziati
* Tutte le variabili e tutti i metodi della SUPER-CLASSE vengono ereditati dall SOTTO-CLASSE
* Le varibili PRIVATE della super classe NON sono accessibili direttamente dall SOTTO-CLASSE
* Le variabili non PRIVATE della SUPER-CLASSE sono accessibili alla SOTTO-CLASSE **solo** se appartengono allo stesso PACKAGE
* Le variabili PROTECTED sono accessibili direttamente dalle sotto-classi **anche** se SUPER classe appartiene ad un package differente.


# ESERCIZIO "CONTO BANCARIO"
SuperClasse **ContoBancario**
* Si vuole realizzare un classe **ContoBancario** che permetta di modellare un generico conto bancario.
* La suddetta classe deve:
  - Contenere un valore (**String**), per rappresentare il numero (alfanumerico) del conto.
  - Contenere un valore (**int**), per rappresentare il bilancio del conto corrente.
  - contenere un costruttore con un parametro che rappresenta il  numero del conto corrente. Il bilancio deve essere inizializzato con il valore 0.
  - contenere un costruttore con 2 parametri, che rappresentano rispettivamente il numero del conto corrente e il bilancio del conto.
  - permettere di conoscere il **numero** e il **bilancio** del conto corrente.
  - permettere di depositare e prelevare somme di denaro dal conto corrente --> Il prelievo puo' avvenire solo se il conto corrente presenta un bilancio sufficiente.
  
 
  
## SOTTO-CLASSE ContoEsteso



* Si vuole realizzare una classe **ContoEsteso** che permetta di modellare un conto bancario con un fido.
* La suddetta classe deve:
  - Estendere la classe **ContoBancario**
  - Contenere un valore (**int**) per rappresentare il valore del **fido**.
  - contenere un costruttore con un parametro che rappresenta il numero del conto corrente. Il **fido** viene inizializzato con il valore 1000.
  - Contienere un 2ndo contruttore con 2 parametri che rapprasentano rispettivamente il numero del conto corrente e il cilancio del conto. Il **fido** viene inizializzato con il valore 1000.
  - contenere un 3zo costruttore con 3 parametri che rappresentano rispettivamente il numero del conto corrente, il bilancio e il fido del conto.
  - permettere di conoscere il valore del **fido** 
  - permettere di creare un nuovo **fido**
  - ridefinire il metodo **preleva** della **super-classe** --> è possibile prelevare una determinata somma di denaro da un conto con **fido** solo se questo presenta un bilancio (incluso il **fido**) sufficiente .
  
  
  
  **DOPO LO SVOLGIMENTO**
  
  
   creando una classe **ContoBancario** e renderndola di tipo **abstract** possiamo far ereditare i metodi che la compongono ad un altra classe, la classe **ContoEsteso**, facendo ciò , nella sotto-classe ci saranno i costruttori della super-classe.
   un costruttore contiene un parametro mentre l'altro ne contiene due, quando nel main creeremo un'oggetto, se passeremo un parametro solo compilerà un costruttore dando a **fido** il valore di 1000 mentre se verranno passati due parametri compilerà l'altro dando a **fido** il valorte inserito dall'utente.
   Per conoscere il valore del **fido** si può inserire un **System.out.println("")** oppure un **JOptionPane...**, il primo ci stamperà il valore di **fido**, in modo semplice, l'altro creerà una pagina in cui sarà stampato il valore di **fido**.
   per definire il metodo **preleva** ereditato dalla super-classe in **ContoEsteso**, bisogna mettere un condizione, creando un cilo,
   suggerito un ciclo **for**, inserendo come parametri sufficente il **bilancio** permettendo di estrarre una quantità indefinita di valori sottraendoli da **fido** e senza far risultare negativo il valore di **fido**.
   
   
   
