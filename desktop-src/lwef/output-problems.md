---
title: Problemi di output
description: Problemi di output
ms.assetid: 45423b7e-f648-408c-9cff-f7cf1affc42a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f19afb705e1d71b3b47bc44c35a51cb83029932287c582b0481ff6a5b078049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961051"
---
# <a name="output-problems"></a>Problemi di output

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

### <a name="the-character-leaves-images-or-trails-behind-when-it-moves"></a>Il carattere lascia le immagini o le tracce dietro quando si sposta.

Quando un carattere agent viene animato, è necessario che le finestre dell'applicazione dietro il carattere si aggiorneranno in modo regolare. Quando il carattere si sposta sullo schermo, a volte è normale vedere alcune immagini residue che scompaiono rapidamente (a seconda della velocità del PC e delle applicazioni in esecuzione). In caso contrario, la causa potrebbe essere la seguente:

-   Il sistema non soddisfa i requisiti minimi di sistema per Agent.
-   La finestra dell'applicazione dietro il carattere non elabora gli aggiornamenti in modo orario. Provare a trascinare il carattere sul desktop o su una finestra della cartella o arrestare alcune applicazioni. Se viene visualizzato un miglioramento notevole, il problema potrebbe essere inevitabile.
-   È possibile che non sia installata la versione ufficiale di Microsoft Internet Explorer 4.0 (o versione successiva). Le versioni non definitiva iniziali di Internet Explorer 4.0 non gestiva correttamente l'aggiornamento dello schermo. Ciò si trasporterebbe in immagini residue del carattere rimanente sullo schermo. Per risolvere il problema, installare la versione ufficiale più recente del Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ).
-   È possibile che si sia verificato un problema con i driver dello schermo o l'hardware del sistema. Assicurarsi di avere i driver più recenti per l'hardware grafico. Se il problema persiste, è possibile contattare il fornitore del PC.

### <a name="the-character-doesnt-produce-any-audio-output-when-it-speaks"></a>Il carattere non produce alcun output audio quando parla.

Questo sintomo può avere diverse cause. Per isolare il problema, provare a eseguire le operazioni seguenti:

-   Verificare che gli altoparlanti siano collegati e che la scheda audio sia compatibile con Windows. È buona idea testarle con un'altra applicazione audio per verificare che l'output audio funzioni correttamente.
-   Verificare che l'applicazione o la pagina Web abilitata per Agent supporti l'input vocale. Non tutte le pagine di esempio supportano l'input vocale. Tenere premuto il tasto Ascolto (in genere si tratta del tasto BLOC SCORR a meno che non sia stato modificato). Sotto il carattere dovrebbe essere visualizzata una finestra popup. Il testo nella mancia dirà lo stato di ascolto del carattere. Se non viene visualizzato alcun suggerimento, l'applicazione o la pagina Web non supporta l'input vocale o non è installato un motore di riconoscimento vocale compatibile. Se la mancia viene visualizzata e indica che il carattere è in ascolto, pronunciare uno dei comandi vocali del carattere. Se non si conoscono i comandi vocali disponibili: rilasciare il tasto Ascolto e fare clic con il pulsante destro del mouse sul carattere, quindi scegliere Apri finestra comandi vocali dal menu a comparsa. Se il comando non viene visualizzato, il supporto vocale non è disponibile per l'applicazione o la pagina Web in uso. Se viene visualizzato, premere di nuovo e tenere premuto il tasto Ascolto. Se il suggerimento ascolto viene visualizzato sotto il carattere e indica che il carattere è in ascolto, pronunciare uno dei comandi elencati nella finestra. Se il carattere non risponde, andare al passaggio successivo.
-   Verificare che nessun'altra applicazione utilizzi attualmente il dispositivo di output audio.
-   Verificare che il carattere in uso sia stato configurato per l'output parlato. Potrebbe essere necessario rivolgersi al sito Web o al fornitore dell'applicazione.
-   Verificare che le impostazioni di Microsoft Agent siano abilitate per l'output vocale
-   Se il carattere usa un motore di sintesi vocale (TTS) per produrre l'output parlato, verificare di aver installato un motore TTS compatibile. Ad esempio, quando viene installato come Internet Explorer componente aggiuntivo 4.0, vengono installati solo i componenti principali di Microsoft Agent. I componenti principali non includono un motore di sintesi vocale. Senza questo motore TTS (un motore compatibile con Microsoft Speech API), i caratteri di esempio di Microsoft Agent non produrranno output parlato.
-   Verificare che l'uso di MIDI da parte di Microsoft Agent non blocchi il canale audio (vedere l'argomento successivo, Applicazioni che eseguono MIDI non hanno output audio quando Microsoft Agent è in esecuzione).

### <a name="applications-that-play-midi-have-no-audio-output-when-microsoft-agent-is-running"></a>Le applicazioni che eseguono MIDI non hanno output audio quando Microsoft Agent è in esecuzione.

Microsoft Agent usa MIDI per riprodurre un tono quando si preme il tasto Ascolto. Se si trova che ciò interferisce con altre applicazioni che esercitono MIDI o interferisce con l'input vocale, è possibile disattivare l'opzione Riproduci tono quando si può parlare nelle proprietà di Microsoft Agent.

### <a name="i-get-the-following-message-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Viene visualizzato il messaggio seguente: Non è possibile eseguire una chiamata in uscita perché l'applicazione sta inviando una chiamata sincrona di input.

Questo messaggio può verificarsi nelle circostanze seguenti:

Quando una pagina Web che include Microsoft Agent viene chiusa (facendo clic con il pulsante destro del mouse sulla voce della barra delle applicazioni della pagina e scegliendo Chiudi dal menu a comparsa), questa operazione potrebbe verificarsi. Ciò è dovuto a un problema di temporizzazione tra Agent e il browser quando vengono arrestati contemporaneamente. L'errore è innocuo. Fare clic su OK per ignorare il messaggio.

Ciò che si è verificato è che la pagina Web (o l'applicazione) abilitata per Agent ha tentato di richiedere un motore di sintesi vocale (TTS) specifico. Speechapi.dll non è stato installato.

### <a name="the-speech-engines-dont-seem-to-work-with-microsoft-agent-in-windows-xp"></a>I motori di riconoscimento vocale non sembrano funzionare con Microsoft Agent in Windows XP?

Microsoft Agent usa SAPI 4.0 per fornire servizi voce. Windows XP viene ora fornito con SAPI 5.0, che non fornisce il supporto per la compatibilità con le versioni precedenti per il predecessore. Fortunatamente, SAPI 4.0 e SAPI 5.0 possono coesistere insieme nello stesso computer Windows XP.

Per far funzionare i motori di riconoscimento vocale con Microsoft Agent in Windows XP, installare prima i file binari di [runtime SAPI 4.0](https://activex.microsoft.com/activex/controls/sapi/spchapi.exe)e quindi installare i motori di riconoscimento vocale specifici.

### <a name="the-speech-engines-used-to-work-with-microsoft-agent-until-i-upgraded-to-windows-xp-what-happened"></a>I motori di riconoscimento vocale usati per lavorare con Microsoft Agent fino a quando non è stato eseguito l'aggiornamento a Windows XP. Che cosa è successo?

Vedere la domanda e la risposta precedenti. Il processo di aggiornamento Windows XP potrebbe aver rimosso il supporto SAPI 4.0 già esistente nel computer. È sufficiente installare nuovamente il runtime SAPI 4.0 e i motori di riconoscimento vocale SAPI 4.0 dopo l'aggiornamento a Windows XP.

### <a name="i-installed-the-tts3000-text-to-speech-engines-onto-my-computer-that-runs-windows-xp-or-windows-2000-and-correctly-edited-my-programming-accordingly-for-their-use-the-microsoft-agent-characters-speak-audibly-using-these-tts3000-text-to-speech-engines-when-i-or-other-local-administrators-are-logged-in-but-not-when-other-users-without-administrator-privileges-are-logged-into-this-computer-on-windows-98-and-windows-me-these-tts3000-text-to-speech-engines-work-correctly-for-both-sets-of-users-how-can-i-fix-this"></a>Ho installato i motori di sintesi vocale TTS3000 nel computer che esegue Windows XP (o Windows 2000) e ho modificato correttamente la programmazione per il loro uso. I caratteri di Microsoft Agent parlano in modo udibile usando questi motori di sintesi vocale TTS3000 quando io o altri amministratori locali sono connessi, ma non quando altri utenti senza privilegi di amministratore sono connessi al computer.  In Windows 98 e Windows, questi motori di sintesi vocale TTS3000 funzionano correttamente per entrambi i set di utenti. Come si risolve questo problema?

È necessario configurare le autorizzazioni di sicurezza per alcune delle chiavi del Registro di sistema dei motori di sintesi vocale TTS3000 per abilitarne l'uso da parte degli account utente senza privilegi di amministratore. Questa operazione può essere eseguita con l'editor del Registro di sistema del sistema operativo.

### <a name="i-followed-the-procedure-described-as-a-solution-to-the-problem-stated-in-the-previous-question-this-worked-fine-so-that-the-microsoft-agent-characters-could-speak-audibly-using-these-tts3000-text-to-speech-engines-when-users-without-administrator-privileges-were-logged-into-the-windows-xp-or-windows-2000-computer-now-months-later-these-same-tts3000-text-to-speech-engines-have-stopped-working-again-what-happened"></a>Ho seguito la procedura descritta come soluzione al problema indicato nella domanda precedente. Questa operazione funzionava correttamente in modo che i caratteri di Microsoft Agent fossero in grado  di parlare in modo udibile usando questi motori di sintesi vocale TTS3000 quando gli utenti senza privilegi di amministratore erano connessi al computer Windows XP (o Windows 2000). Ora, mesi dopo, questi stessi motori di sintesi vocale TTS3000 hanno smesso di funzionare di nuovo. Che cosa è successo?

Quando è stata seguita la procedura descritta per la domanda precedente, questo ha fornito agli account utente non amministratori le autorizzazioni di controllo completo per le chiavi del Registro di sistema necessarie. È possibile che uno di questi utenti abbia modificato consapevolmente o inconsapevolmente i valori, modificato nuovamente le autorizzazioni o addirittura eliminato completamente la chiave del Registro di sistema.

Controllare se queste chiavi del Registro di sistema e le relative autorizzazioni sono state modificate, eliminate o modificate in altro modo. Se necessario, modificare nuovamente queste chiavi del Registro di sistema e le relative autorizzazioni oppure installare nuovamente la sintesi vocale TTS3000.

 

 




