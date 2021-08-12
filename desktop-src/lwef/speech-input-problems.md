---
title: Problemi di input vocale
description: Problemi di input vocale
ms.assetid: b42664a2-9615-4e15-97a6-115e9556096b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d135ac8a098f52066854c6003c22caa7290efbd01c8038bda116cd843b21a2e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246230"
---
# <a name="speech-input-problems"></a>Problemi di input vocale

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

### <a name="the-character-does-not-respond-to-my-spoken-input"></a>Il carattere non risponde all'input parlato.

Questo sintomo può essere causato da una serie di problemi. Per isolare il problema, provare a eseguire le operazioni seguenti:

-   Verificare che il microfono sia collegato correttamente. È buona idea testarla con un'altra applicazione di input audio per assicurarsi che funzioni correttamente.
-   Verificare che sia installato un motore di riconoscimento vocale compatibile. In Windows 95, Windows 98 e Windows NT 4.0, aprire il Pannello di controllo. Se si trova l'oggetto Voce, aprirlo e elencare i motori di riconoscimento vocale disponibili e installati nel sistema.
-   Verificare che la scheda audio sia compatibile con Microsoft Windows 95, Windows 98 o Windows NT.

    Il modo migliore per eseguire questa operazione è eseguire l'applicazione Sound Recorder fornita con Windows. In genere è disponibile nella menu Start. Fare clic sul pulsante Start, fare clic su Programmi, accessori, multimedialie quindi fare clic su Registratore di suoni. Quando viene visualizzata la finestra Registratore di suoni, fare clic sul **pulsante Registra** e parlare con il microfono. La riga nella finestra deve essere animata in risposta all'input vocale.

    Se l'applicazione Sound Recorder non funziona nel sistema, contattare il reparto di supporto tecnico del produttore della scheda audio per assistenza. La scheda audio potrebbe non essere compatibile con Windows o potrebbe esserci un problema con i driver software per la scheda audio.

-   Verificare che l'input audio per l'input vocale sia impostato correttamente.
    1.  Aprire l'oggetto input voce nel Pannello di controllo. Se l'oggetto Voce non è presente, installarne uno.
    2.  Selezionare il motore di input vocale installato.
    3.  Scegliere il pulsante Impostazioni guidata microfono. Se questo pulsante viene visualizzato disabilitato, un motore di riconoscimento vocale compatibile non è installato o il motore di riconoscimento vocale installato potrebbe non supportare la regolazione automatica.
-   Verificare che l'applicazione o la pagina Web abilitata per Agent supporti l'input vocale. Non tutte le pagine (o le applicazioni) supportano l'input vocale. Tenere premuto il tasto Ascolto. In genere si tratta del tasto BLOC SCORR, a meno che non sia stato modificato. Sotto il carattere dovrebbe essere visualizzata una finestra popup. Il testo nella mancia dirà lo stato di ascolto del carattere. Se non viene visualizzato alcun suggerimento, l'applicazione o la pagina Web non supporta l'input vocale oppure non è installato un motore di riconoscimento vocale compatibile. Se la mancia viene visualizzata e indica che il carattere è in ascolto, pronunciare uno dei comandi vocali del carattere. Se non si conoscono i comandi vocali disponibili, rilasciare il tasto Ascolto e fare clic con il pulsante destro del mouse sul carattere. Scegliere quindi Apri finestra comandi vocali dal menu a comparsa. Se il comando non viene visualizzato, il supporto vocale non è disponibile per l'applicazione o la pagina Web in uso. Se viene visualizzato, premere di nuovo e tenere premuto il tasto Ascolto. Se il suggerimento ascolto viene visualizzato sotto il carattere e indica che il carattere è in ascolto, pronunciare uno dei comandi elencati nella finestra. Se il carattere non risponde, andare al passaggio successivo.
-   Verificare che nessun'altra applicazione utilizzi attualmente il dispositivo di output audio.
-   Verificare che l'uso di MIDI da parte di Microsoft Agent non blocchi il canale audio (vedere Applicazioni che eseguono [MIDI](output-problems.md)senza output audio quando Microsoft Agent è in esecuzione " nella sezione Problemi di output).
-   Se sono stati eseguiti i passaggi precedenti ma si verificano ancora problemi con l'input vocale, verificare che la scheda audio e il software del driver siano compatibili con il motore di riconoscimento vocale in uso. Rivolgersi al supporto tecnico per la scheda audio e il produttore del motore di riconoscimento vocale.

### <a name="the-midi-tone-seems-to-disrupts-speech-input"></a>Il tono MIDI sembra interrompere l'input vocale.

Ridurre il volume MIDI seguendo questa procedura.

1.  Aprire la finestra Controllo volume facendo clic con il pulsante destro del mouse sull'icona del parlante nella barra delle applicazioni o aprendo l'oggetto Multimediale nel Pannello di controllo. Fare clic sul pulsante Volume nella sezione Riproduzione della pagina Audio.
2.  Ridurre il volume MIDI spostando il dispositivo di scorrimento verso il basso.

### <a name="the-character-does-not-respond-to-voice-input-but-i-can-hear-my-voice-through-my-speakers-when-i-talk-into-my-microphone"></a>Il carattere non risponde all'input vocale, ma è possibile ascoltare la voce tramite gli altoparlanti quando si parla al microfono.

La scheda audio non è configurata correttamente per l'uso con Microsoft Agent. Scegliere la procedura guidata Impostazioni microfono nella finestra delle proprietà dell'oggetto Voce nel Pannello di controllo. Per informazioni su come accedere a questo[pulsante,](#the-character-does-not-respond-to-my-spoken-input)vedere la procedura per "Il carattere non risponde all'input parlato".

 

 




