---
title: Generazione di informazioni linguistiche
description: Generazione di informazioni linguistiche
ms.assetid: 903561f0-89dc-4297-8ea0-3fa150f2e6dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23fb99a5139e287e07e353791ce776b8a04dd8d2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104551041"
---
# <a name="generating-linguistic-information"></a>Generazione di informazioni linguistiche

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Dopo aver registrato un nuovo file audio o aver caricato un file audio esistente, è possibile generare informazioni fonetiche e di Word break inserendo il testo che corrisponde al file audio nella casella **rappresentazione testo** . Scegliere quindi il comando **genera informazioni linguistiche** dal menu **modifica** o dalla barra degli strumenti. Nell'editor di suoni viene visualizzato un messaggio di stato e viene avviata l'elaborazione del file audio. Al termine della generazione di informazioni linguistiche, viene visualizzato un mapping delle etichette di Word e fonema per il file audio in caselle nella casella **rappresentazione audio** . Si noti che il comando **genera informazioni linguistiche** rimane disabilitato fino a quando non si immette una rappresentazione testuale per il file audio.

![Screenshot che mostra i riquadri "rappresentazione testuale" e "rappresentazione audio" nello strumento di modifica audio delle informazioni linguistiche di Microsoft.](images/f3listlabel.gif)

Se l'editor non produce un set di etichette di parole o Foneme accettabile, scegliere di nuovo il comando **genera informazioni linguistiche** . Se l'editor non genera alcuna informazione linguistica, controllare la rappresentazione testuale per assicurarsi che tutte le parole siano ordinate e digitate correttamente e che non siano presenti spazi inutili per la punteggiatura. Quindi scegliere di nuovo il comando **genera informazioni linguistiche** . È possibile modificare la rappresentazione testo selezionando testo nella casella di testo **rappresentazione testo** e usando i comandi **taglia**, **copia** e **Incolla** del menu **modifica** . Se non si è certi delle parole incluse nel file audio, è possibile riprodurre il file audio scegliendo **Riproduci** dal menu **modifica** o dalla barra degli strumenti dell'editor. Se l'editor non è ancora in grado di produrre etichette linguistiche, provare a registrare nuovamente il file audio. Una registrazione di scarsa qualità, soprattutto con un rumore di fondo eccessivo, può ridurre la probabilità di generare ragionevoli informazioni linguistiche.

È anche possibile creare manualmente le proprie informazioni linguistiche selezionando una parte della rappresentazione audio e scegliendo **Inserisci fonema** o **Inserisci parola** dal menu **modifica** . Questi comandi sono disponibili anche se si fa clic con il pulsante destro del mouse all'interno della selezione.

Per vedere come possono essere usate le informazioni linguistiche per l'animazione dei caratteri di sincronizzazione del labbro con Microsoft Agent, scegliere il pulsante **Riproduci** sulla barra degli strumenti e l'editor riprodurrà il file audio, animando un'immagine della bocca di esempio in base alle informazioni sull'etichetta generata.

È possibile modificare la visualizzazione dell'etichetta fonema per visualizzare le assegnazioni IPA (alfabeto fonetico internazionale) scegliendo il comando di **visualizzazione dell'etichetta fonema** dal menu **modifica** , quindi il comando IPA. Viene visualizzato il valore byte per il fonema. Per tornare ai nomi descrittivi, scegliere di nuovo il comando **Visualizza etichetta fonema** , quindi scegliere **nome**.

### <a name="playing-a-sound-file"></a>Riproduzione di un file audio

È possibile riprodurre i file audio standard di Windows o i file audio con funzionalità avanzate linguisticamente selezionando il comando **Play** dal menu **audio** o la barra degli strumenti dell'editor. I comandi **Sospendi** e **Interrompi** consentono di sospendere o arrestare la riproduzione del file audio. Quando si riproduce il file, l'immagine di esempio mouth viene animata per mostrare come le informazioni di sincronizzazione labiale possono essere utilizzate da un carattere di Microsoft Agent.

È anche possibile riprodurre una parte selezionata di un file audio trascinando una selezione nella **rappresentazione audio** o facendo clic su un'etichetta di parola o fonema, quindi scegliere **Riproduci**. È possibile estendere una selezione esistente tenendo premuto MAIUSC e facendo clic oppure premendo MAIUSC e trascinando il nuovo percorso nella **rappresentazione audio**.

### <a name="editing-linguistic-information"></a>Modifica di informazioni linguistiche

È possibile modificare le informazioni linguistiche di un file in diversi modi. È ad esempio possibile modificare il limite di una parola o di un fonema spostando il puntatore sul bordo della casella che definisce l'intervallo dell'etichetta. Quando il puntatore passa al puntatore di spostamento limite, trascinare verso sinistra o verso destra. L'Editor regola automaticamente anche il limite di parole o fonemi adiacenti.

![Screenshot che mostra le modifiche alle informazioni linguistiche di un file.](images/f4listadj.gif)

La regolazione del limite di un'etichetta fonema modifica la tempistica di un fonema quando l'audio viene riprodotto. Per i caratteri sviluppati per l'uso con Microsoft Agent, la modifica del limite dell'etichetta fonema può modificare l'intervallo o la durata di un'immagine della bocca mappata a tale fonema. Se si modifica il limite di un'etichetta di Word, la tempistica dell'aspetto della parola viene modificata nel fumetto di parola del carattere.

È anche possibile sostituire un'assegnazione fonema selezionando l'etichetta fonema e scegliendo **Sostituisci fonemi** dal menu **modifica** oppure facendo clic con il pulsante destro del mouse sull'etichetta fonema e scegliendo **Sostituisci fonemi** dal menu a comparsa. Nell'editor viene visualizzata la finestra di dialogo **Sostituisci fonemi** e viene evidenziata l'assegnazione fonema corrente dell'etichetta. È possibile scegliere un fonema sostitutivo selezionando uno nell'elenco **IPA** o scegliendo un'altra voce nell'elenco **nome** . Se è disponibile più di una traduzione IPA per quel nome, scegliere un elemento nell'elenco **IPA** . Per immettere una designazione IPA per un fonema che non è possibile includere direttamente nel linguaggio, digitare il valore esadecimale o più valori esadecimali concatenati con un carattere più (+). Dopo aver selezionato le informazioni sul fonema di sostituzione, scegliere **OK** e l'Editor sostituisce l'etichetta fonema selezionata.

![Screenshot che mostra la finestra di dialogo ' Sostituisci fonemi ', con ' <SIL>' selezionato come etichetta descrittiva.](images/f5listphone.gif)

Analogamente, è possibile sostituire un'etichetta di Word facendo clic sulla casella dell'etichetta e scegliendo **Sostituisci parola** oppure facendo clic con il pulsante destro del mouse sulla casella dell'etichetta e scegliendo **Sostituisci parola** dal menu a comparsa. Nell'editor viene visualizzata la finestra di dialogo **Sostituisci Word** . Immettere la parola sostitutiva e scegliere **OK**.

![Screenshot che mostra la finestra di dialogo ' Sostituisci Word ' con ' Sound ' immesso nella casella di testo ' Word Text '.](images/f6listrep.gif)

Per i caratteri sviluppati per l'uso con Microsoft Agent, la sostituzione di un'etichetta fonema può modificare l'immagine della bocca visualizzata quando il file audio viene riprodotto. La sostituzione di una parola sostituisce il testo visualizzato nell'aerostato di parola del carattere quando viene chiamato il metodo [**Speak**](speak-method.md) .

È anche possibile inserire una nuova etichetta o parola fonema selezionando la **rappresentazione audio** e scegliendo **Inserisci fonema** o **Inserisci parola** dal menu **modifica** oppure facendo clic con il pulsante destro del mouse all'interno della selezione e scegliendo i comandi dal menu a comparsa. Questi comandi consentono di visualizzare finestre di dialogo simili alle finestre di dialogo **Sostituisci fonemi** e **Sostituisci Word** , con la differenza che l'editor inserisce la nuova parola o il fonema anziché sostituire le informazioni esistenti.

Infine, è possibile eliminare un fonema o una parola selezionando la relativa etichetta e scegliendo **Elimina fonema** o **Elimina parola**. In questo modo le informazioni linguistiche vengono rimosse dal file.

 

 




