---
title: Generazione di informazioni linguistiche
description: Generazione di informazioni linguistiche
ms.assetid: 903561f0-89dc-4297-8ea0-3fa150f2e6dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a068153863236b7096b67a976bbcf0654af9c75df87d2f527027830a4df33eb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479309"
---
# <a name="generating-linguistic-information"></a>Generazione di informazioni linguistiche

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Dopo aver registrato un nuovo file audio o caricato un file audio esistente, è possibile generare informazioni fonetiche  e di word break immettendo il testo corrispondente al file audio nella casella Rappresentazione testo. Scegliere quindi il **comando Genera informazioni linguistiche** dal menu **Modifica o** dalla barra degli strumenti. L'editor audio visualizza un messaggio di stato e avvia l'elaborazione del file audio. Al termine della generazione delle informazioni linguistiche, viene visualizzato un mapping di etichette di parole e fonemi per il file audio nelle caselle della **casella Rappresentazione** audio. Si noti che il **comando Genera informazioni linguistiche** rimane disabilitato fino a quando non si immette una rappresentazione di testo per il file audio.

![Screenshot che mostra i riquadri "Rappresentazione testo" e "Rappresentazione audio" in Microsoft Linguistic Information Sound Editing Tool.](images/f3listlabel.gif)

Se l'editor non produce un set accettabile di etichette di parole o fonemi, scegliere di **nuovo il comando Genera informazioni linguistiche.** Se l'editor non genera informazioni linguistiche, controllare la rappresentazione testuale per assicurarsi che tutte le parole siano ordinate e digitate correttamente e che non siano presenti spazi non necessari intorno alla punteggiatura. Scegliere quindi di **nuovo il comando Generate Linguistic Info (Genera informazioni** linguistiche). È possibile modificare la rappresentazione  di testo selezionando il testo nella casella di testo Rappresentazione testo e usando i comandi **Taglia,** Copia e **Incolla** del menu **Modifica.** Se non si è incerti delle parole incluse nel  file audio, è possibile riprodurre il file audio scegliendo Riproduci dal **menu** Modifica o dalla barra degli strumenti dell'editor. Se l'editor non riesce ancora a produrre etichette linguistiche, provare a registrare di nuovo il file audio. È probabile che una registrazione di scarsa qualità, soprattutto con un rumore di fondo eccessivo, riduca la probabilità di generare informazioni linguistiche ragionevoli.

È anche possibile creare manualmente informazioni linguistiche personali selezionando parte della rappresentazione audio e scegliendo **Inserisci** fonema o **Inserisci parola** **dal** menu Modifica. Questi comandi sono disponibili anche se si fa clic con il pulsante destro del mouse all'interno della selezione.

Per vedere come è possibile usare le informazioni linguistiche per la  sincronizzazione dei caratteri con Microsoft Agent, scegliere il pulsante Play (Riproduci) sulla barra degli strumenti e l'editor riprodurrà il file audio, animando un'immagine di riproduzione di esempio in base alle informazioni sull'etichetta generata.

È possibile modificare la visualizzazione dell'etichetta del fonema per visualizzare le assegnazioni IPA (International Phonetic Alphabet) scegliendo il comando **Visualizzazione** etichetta fonema dal **menu** Modifica e quindi il comando IPA. Verrà visualizzato il valore in byte per il fonema. Per tornare ai nomi descrittivi, scegliere di nuovo il comando Phoneme Label Display (Visualizzazione etichetta **Phoneme),** quindi scegliere **Name (Nome).**

### <a name="playing-a-sound-file"></a>Riproduzione di un file audio

È possibile riprodurre file audio Windows standard o file audio  linguisticamente migliorati scegliendo il comando Riproduci dal menu **Audio** o dalla barra degli strumenti dell'editor. I **comandi Sospendi** e Arresta consentono di sospendere o arrestare la riproduzione del file audio.  Durante la riproduzione del file, l'immagine di esempio della sincronizzazione viene animata per mostrare come le informazioni di sincronizzazione possono essere usate da un carattere di Microsoft Agent.

È anche possibile riprodurre una parte selezionata di un file audio trascinando una selezione nella rappresentazione **audio** o facendo clic su un'etichetta di parola o fonema, quindi **scegliendo Riproduci.** È possibile estendere una selezione esistente premendo MAIUSC e facendo clic oppure premendo MAIUSC e trascinando nella nuova posizione nella **rappresentazione audio.**

### <a name="editing-linguistic-information"></a>Modifica delle informazioni linguistiche

È possibile modificare le informazioni linguistiche di un file in diversi modi. Ad esempio, è possibile modificare il limite di un'etichetta di parola o fonema spostando il puntatore sul bordo della casella che definisce l'intervallo dell'etichetta. Quando il puntatore passa al puntatore di spostamento del limite, trascinare verso sinistra o verso destra. L'editor regola automaticamente anche il confine di parola o fonema adiacente.

![Screenshot che mostra le modifiche alle informazioni linguistiche di un file.](images/f4listadj.gif)

La modifica del limite di un'etichetta fonema modifica la tempistica di un fonema durante la riproduzione dell'audio. Per i caratteri sviluppati per l'uso con Microsoft Agent, la modifica del limite dell'etichetta del fonema può modificare l'intervallo o la durata di un'immagine di stima mappata a tale fonema. La modifica del limite di un'etichetta di parola modifica la tempistica dell'aspetto della parola nel fumetto delle parole del carattere.

È anche possibile sostituire un'assegnazione di fonema selezionando l'etichetta fonema e scegliendo Sostituisci **fonema** dal **menu** Modifica oppure facendo clic con il pulsante destro del mouse sull'etichetta del fonema e scegliendo Sostituisci **fonema** dal menu a comparsa. L'editor visualizza la **finestra di dialogo Sostituisci** fonema ed evidenzia l'assegnazione corrente del fonema dell'etichetta. È possibile scegliere un fonema sostitutivo selezionandolo **nell'elenco IPA** o scegliendo un'altra voce nell'elenco Nome.  Se per tale nome sono disponibili più traduzioni IPA, scegliere un elemento **nell'elenco IPA.** Per immettere una designazione IPA per un fonema che non può essere incluso direttamente nella lingua, digitare il valore esadecimale o più valori esadecimali, concatenati con un segno più (+). Dopo aver selezionato le informazioni sul fonema sostitutivo, scegliere **OK** e l'editor sostituisce l'etichetta fonema selezionata.

![Screenshot che mostra la finestra di dialogo "Sostituisci fonema", con l'opzione "<SIL>" selezionata come etichetta descrittiva.](images/f5listphone.gif)

Analogamente, è possibile sostituire un'etichetta di parola facendo clic sulla casella dell'etichetta e scegliendo Sostituisci **parola** oppure facendo clic con il pulsante destro del mouse sulla casella dell'etichetta e scegliendo Sostituisci **parola** dal menu a comparsa. Nell'editor viene visualizzata la **finestra di dialogo Sostituisci** parola . Immettere la parola sostitutiva e scegliere **OK.**

![Screenshot che mostra la finestra di dialogo "Sostituisci parola" con "suono" immesso nella casella di testo "Testo word".](images/f6listrep.gif)

Per i caratteri sviluppati per l'uso con Microsoft Agent, la sostituzione di un'etichetta di fonema può modificare l'immagine del suono visualizzata durante la riproduzione del file audio. La sostituzione di una parola sostituisce il testo visualizzato nel fumetto delle parole del carattere quando [**viene**](speak-method.md) chiamato il metodo Speak.

È anche possibile inserire una nuova etichetta o parola fonema  effettuando  una selezione nella rappresentazione **audio** e scegliendo Inserisci fonema o Inserisci parola dal **menu** Modifica oppure facendo clic con il pulsante destro del mouse all'interno della selezione e scegliendo i comandi dal menu a comparsa. Questi comandi consentono di visualizzare  finestre di dialogo simili alle finestre di dialogo Sostituisci fonema e Sostituisci **parola,** ad eccezione del fatto che l'editor inserisce la nuova parola o fonema anziché sostituire le informazioni esistenti.

Infine, è possibile eliminare un fonema o una parola selezionandone l'etichetta e scegliendo **Delete Phoneme (Elimina fonema)** **o Delete Word (Elimina parola).** In questo modo le informazioni linguistiche vengono rimosse dal file.

 

 




