## Panoramica teorica

1. **Smoothing (riduzione del rumore)**
   L’immagine viene filtrata con un filtro Gaussiano per ridurre il rumore e rendere più stabili i bordi.

2. **Calcolo del gradiente**
   Si calcolano le derivate parziali lungo le direzioni X e Y. Dal gradiente risultano:

   * **Magnitudine** del gradiente, che indica l’intensità del bordo.
   * **Direzione** del gradiente, che indica l’orientamento del bordo.

3. **Quantizzazione degli angoli**
   La direzione del gradiente viene approssimata a uno dei 4 angoli principali (0°, 45°, 90°, 135°) per semplificare il passo successivo.

4. **Non-Maximum Suppression (NMS)**
   Permette di “assottigliare” i bordi mantenendo solo i pixel che rappresentano massimi locali lungo la direzione del gradiente.

5. **Double Thresholding**
   I pixel vengono classificati in:

   * **Forti bordi** (superiore alla soglia alta)
   * **Deboli bordi** (tra soglia bassa e alta)
   * **Non bordi** (sotto soglia bassa)

6. **Edge Tracking by Hysteresis**
   I bordi deboli collegati a bordi forti vengono mantenuti, mentre gli altri vengono scartati. Questo passaggio è opzionale nel notebook ma può essere aggiunto per completezza.

 
 ## Autore
**Sebastiano Urzì**
