---
title: Problemi di input vocale
description: Problemi di input vocale
ms.assetid: b42664a2-9615-4e15-97a6-115e9556096b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7b29a85c79996eb0c01260c8e2b738fcd926f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955365"
---
# <a name="speech-input-problems"></a>Problemi di input vocale

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

### <a name="the-character-does-not-respond-to-my-spoken-input"></a>Il carattere non risponde all'input parlato.

Questo sintomo può essere causato da una serie di problemi. Per isolare il problema, provare a eseguire le operazioni seguenti:

-   Verificare che il microfono sia collegato correttamente. È consigliabile testarla con un'altra applicazione di input audio per verificare che funzioni correttamente.
-   Verificare che sia installato un motore di riconoscimento vocale compatibile. In Windows 95, Windows 98 e Windows NT 4,0 aprire il pannello di controllo. Se l'oggetto vocale viene trovato, aprirlo ed elencare i motori di riconoscimento vocale disponibili e installati nel sistema.
-   Verificare che la scheda audio sia compatibile con Microsoft Windows 95, Windows 98 o Windows NT.

    Il modo migliore per eseguire questa operazione consiste nell'eseguire l'applicazione di registrazione suoni fornita con Windows. Può essere in genere visualizzato nel menu Start. Fare clic sul pulsante Start, scegliere programmi, accessori, fare clic su Multimedia, quindi fare clic su registratore di suoni. Quando viene visualizzata la finestra registratore audio, fare clic sul pulsante **registra** e comunicare con il microfono. La riga nella finestra deve essere animata in risposta all'input vocale.

    Se l'applicazione registrazione suoni non funziona nel sistema, contattare il reparto tecnico del produttore della scheda audio per assistenza. La scheda audio potrebbe non essere compatibile con Windows o potrebbe essersi verificato un problema con i driver software per la scheda audio.

-   Verificare che l'input audio per l'input vocale sia impostato correttamente.
    1.  Aprire l'oggetto input vocale nel pannello di controllo. Se l'oggetto riconoscimento vocale non è presente, installarne uno.
    2.  Selezionare il motore di input vocale installato.
    3.  Scegliere il pulsante Impostazioni microfono della procedura guidata. Se questo pulsante viene visualizzato disabilitato, non è installato un motore vocale compatibile o il motore vocale installato potrebbe non supportare la regolazione automatica.
-   Verificare che l'applicazione o la pagina Web abilitata per l'agente supporti l'input vocale. Non tutte le pagine (o applicazioni) supportano l'input vocale. Premere e tenere premuto il tasto ascolto. In genere si tratta del tasto BLOC SCORR, a meno che non sia stato modificato. Verrà visualizzata una finestra popup sotto il carattere. Il testo nella mancia indica lo stato di ascolto del carattere. Se non viene visualizzata alcuna mancia, l'applicazione o la pagina Web non supporta l'input vocale oppure non è installato un motore di riconoscimento vocale compatibile. Se il suggerimento viene visualizzato e indica che il carattere è in ascolto, pronunciare uno dei comandi vocali del carattere. Se non si conoscono i comandi vocali disponibili, rilasciare il tasto ascolto e fare clic con il pulsante destro del mouse sul carattere. Quindi, scegliere Apri finestra comandi vocali dal menu a comparsa. Se il comando non viene visualizzato, il supporto vocale non è disponibile per l'applicazione o la pagina Web in uso. Se viene visualizzato, tenere nuovamente premuto il tasto ascolto. Se il suggerimento di ascolto viene visualizzato sotto il carattere e indica che il carattere è in ascolto, pronunciare uno dei comandi elencati nella finestra. Se il carattere non risponde, andare al passaggio successivo.
-   Verificare che nessun'altra applicazione stia attualmente usando il dispositivo di output audio.
-   Verificare che l'uso di MIDI da parte dell'agente Microsoft non blocchi il canale audio (vedere le [applicazioni che svolgono MIDI non hanno output audio quando Microsoft Agent è in esecuzione](output-problems.md)nella sezione problemi di output).
-   Se è stata seguita la procedura descritta in precedenza, ma sono ancora presenti problemi con l'input vocale, verificare che il software della scheda audio e del driver siano compatibili con il motore di riconoscimento vocale in uso. Rivolgersi al supporto tecnico per la scheda audio e il produttore del motore di riconoscimento vocale.

### <a name="the-midi-tone-seems-to-disrupts-speech-input"></a>Il tono MIDI sembra compromettere l'input vocale.

Ridurre il volume MIDI attenendosi alla procedura seguente.

1.  Aprire la finestra controllo volume facendo clic con il pulsante destro del mouse sull'icona dell'altoparlante sulla barra delle applicazioni o aprendo l'oggetto Multimedia nel pannello di controllo. Fare clic sul pulsante volume nella sezione playback della pagina audio.
2.  Ridurre il volume MIDI spostando il dispositivo di scorrimento verso il basso.

### <a name="the-character-does-not-respond-to-voice-input-but-i-can-hear-my-voice-through-my-speakers-when-i-talk-into-my-microphone"></a>Il carattere non risponde all'input vocale, ma è possibile sentire la mia voce attraverso i miei speaker quando si parla nel mio microfono.

La scheda audio non è configurata correttamente per l'uso con Microsoft Agent. Scegliere la procedura guidata impostazioni microfono nella finestra delle proprietà dell'oggetto riconoscimento vocale nel pannello di controllo. Per informazioni su come accedere a questo pulsante, vedere i passaggi per "[il carattere non risponde all'input vocale](#the-character-does-not-respond-to-my-spoken-input)".

 

 




