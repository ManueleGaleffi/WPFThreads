# WPFThreads
4i, ITTS O.Belluzzi L.da Vinci, 2022/2023

<img src="images/immagine1.PNG" width=500>
<img src="images/immagine2.PNG" width=300> 
<img src="images/immagine3.PNG" width=300>

I thread non possono usare uno le risorse dell’altro.
Prima di eseguire una nuova azione si blocca a causa del Thread.Sleep.
Uno Lavora su lblCounter1 e l’altro lavora su lblCounter2.

Il lock garantisce l’atomicità delle cose.
<img src="images/immagine4.PNG" width=100>

Una volta fermato nessuno aggiorna più la prima label.

<img src="images/immagine5.PNG" width=300>
<img src="images/immagine6.PNG" width=300>

Il semaforo è un intero che non può essere negativo e ha due comandi:
-signal, decrementa il contatore
-wait, è una procedura bloccante 

Il semaforo non può essere utilizzato all’interno di un event handler per questo dobbiamo crearli un altro thread.

<img src="images/immagine7.PNG" width=300>
<img src="images/immagine8.PNG" width=300>

Possiamo anche meglio scriverlo rendendolo meglio leggibile così:

<img src="images/immagine9.PNG" width=300>

Con il metodo “dispatcher.Invoke” facciamo collaborare i due thread facendo in modo che non si blocchino.
Invoke ha un parametro di tipo lambda expression che si utilizza con =>

Per fare in modo che nessuno clicchi il pulsante durante l'esecuzione utilizziamo

<img src="images/immagine10.PNG" width=300>

che blocca momentaneamente il pulsante. 
E per farlo ripartire lo settiamo a true
