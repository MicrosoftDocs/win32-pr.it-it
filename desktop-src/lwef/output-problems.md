---
title: Problemi di output
description: Problemi di output
ms.assetid: 45423b7e-f648-408c-9cff-f7cf1affc42a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d909052feb2463637a8eab6343353f0af617c06
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104336489"
---
# <a name="output-problems"></a>Problemi di output

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

### <a name="the-character-leaves-images-or-trails-behind-when-it-moves"></a>Il carattere lascia le immagini o le tracce dietro quando si sposta.

Quando si aggiunge un'animazione a un carattere di Agent, è necessario che le finestre dell'applicazione dietro il carattere vengano aggiornate in modo tempestivo. Quando il carattere si sposta sullo schermo, è normale che talvolta vengano visualizzate alcune immagini residue che scompaiono rapidamente (a seconda della velocità del PC e delle applicazioni in esecuzione). In caso contrario, è possibile che si verifichi quanto segue:

-   Il sistema non soddisfa i requisiti minimi di sistema per Agent.
-   La finestra dell'applicazione dietro il carattere non elabora gli aggiornamenti in modo tempestivo. Provare a trascinare il carattere sul desktop o in una finestra della cartella oppure arrestare alcune applicazioni. Se si riscontra un miglioramento significativo, il problema potrebbe essere inevitabile.
-   È possibile che non sia installata la versione ufficiale di Microsoft Internet Explorer 4,0 (o versione successiva). Le prime versioni non definitive di Internet Explorer 4,0 non gestiscono correttamente l'aggiornamento dello schermo. Ciò comporterebbe la visualizzazione di immagini residue del carattere rimanenti sullo schermo. Per risolvere il problema, installare la versione ufficiale più recente di Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ).
-   Potrebbe essersi verificato un problema con i driver dello schermo o l'hardware del sistema. Assicurarsi di disporre dei driver più recenti per l'hardware grafico. Se il problema persiste, potrebbe essere necessario contattare il fornitore del computer.

### <a name="the-character-doesnt-produce-any-audio-output-when-it-speaks"></a>Il carattere non produce alcun output audio quando parla.

Questo sintomo potrebbe avere diverse cause. Per isolare il problema, provare a eseguire le operazioni seguenti:

-   Verificare che gli altoparlanti siano collegati e che la scheda audio sia compatibile con Windows. È consigliabile testarli con un'altra applicazione audio per verificare che l'output audio funzioni correttamente.
-   Verificare che l'applicazione o la pagina Web abilitata per l'agente supporti l'input vocale. Non tutte le pagine di esempio supportano l'input vocale. Tenere premuto il tasto ascolto (in genere si tratta del tasto BLOC SCORR, a meno che non sia stato modificato). Verrà visualizzata una finestra popup sotto il carattere. Il testo nella mancia indica lo stato di ascolto del carattere. Se non viene visualizzata alcuna mancia, l'applicazione o la pagina Web non supporta l'input vocale oppure non è installato un motore di riconoscimento vocale compatibile. Se il suggerimento viene visualizzato e indica che il carattere è in ascolto, pronunciare uno dei comandi vocali del carattere. Se non si conoscono i comandi vocali disponibili: rilasciare il tasto ascolto e fare clic con il pulsante destro del mouse sul carattere, quindi scegliere Apri finestra comandi vocali dal menu a comparsa. Se il comando non viene visualizzato, il supporto vocale non è disponibile per l'applicazione o la pagina Web in uso. Se viene visualizzato, tenere nuovamente premuto il tasto ascolto. Se il suggerimento di ascolto viene visualizzato sotto il carattere e indica che il carattere è in ascolto, pronunciare uno dei comandi elencati nella finestra. Se il carattere non risponde, andare al passaggio successivo.
-   Verificare che nessun'altra applicazione stia attualmente usando il dispositivo di output audio.
-   Verificare che il carattere utilizzato sia stato configurato per l'output parlato. Potrebbe essere necessario contattare il sito Web o il fornitore dell'applicazione.
-   Verificare che le impostazioni dell'agente Microsoft siano abilitate per l'output parlato
-   Se il carattere usa un motore di sintesi vocale per produrre l'output parlato, verificare di avere installato un motore TTS compatibile. Ad esempio, quando viene installato come componente aggiuntivo di Internet Explorer 4,0, vengono installati solo i componenti di base di Microsoft Agent. I componenti di base non includono un motore di sintesi vocale. Senza questo motore TTS (un motore compatibile con Microsoft Speech API), i caratteri di esempio di Microsoft Agent non produrranno output parlato.
-   Verificare che l'uso di MIDI da parte dell'agente Microsoft non blocchi il canale audio. vedere l'argomento successivo. le applicazioni che eseguono MIDI non hanno output audio quando Microsoft Agent è in esecuzione.

### <a name="applications-that-play-midi-have-no-audio-output-when-microsoft-agent-is-running"></a>Le applicazioni che svolgono MIDI non hanno output audio quando Microsoft Agent è in esecuzione.

Microsoft Agent USA MIDI per riprodurre un tono quando si preme il tasto ascolto. Se si ritiene che questa operazione interferisca con altre applicazioni che svolgono MIDI o interferiscono con l'input vocale, è possibile disattivare il tono di riproduzione quando è possibile pronunciare l'opzione nelle proprietà dell'agente Microsoft.

### <a name="i-get-the-following-message-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Viene ricevuto il messaggio seguente: non è possibile effettuare una chiamata in uscita perché l'applicazione invia una chiamata sincrona di input.

Questo messaggio può verificarsi nelle circostanze seguenti:

Quando viene chiusa una pagina Web che include Microsoft Agent (facendo clic con il pulsante destro del mouse sulla voce della barra delle applicazioni della pagina e scegliendo Chiudi dal menu a comparsa), è possibile che si verifichi questo problema. Ciò è dovuto a un problema di temporizzazione tra l'agente e il browser quando si arrestano nello stesso momento. L'errore è innocuo. Fare clic su OK per chiudere il messaggio.

Cosa si è verificato se la pagina Web abilitata per l'agente (o applicazione) ha tentato di richiedere un motore di sintesi vocale (TTS) specifico. Speechapi.dll non è stato installato.

### <a name="the-speech-engines-dont-seem-to-work-with-microsoft-agent-in-windows-xp"></a>I motori di riconoscimento vocale non sembrano funzionare con Microsoft Agent in Windows XP?

Microsoft Agent USA SAPI 4,0 per fornire servizi di riconoscimento vocale. Windows XP viene tuttavia fornito con SAPI 5,0, che non fornisce il supporto per la compatibilità con le versioni precedenti. Fortunatamente, SAPI 4,0 e SAPI 5,0 possono coesistere nello stesso computer Windows XP.

Per far funzionare i motori di sintesi vocale con Microsoft Agent in Windows XP, installare prima di tutto i [file binari di runtime di SAPI 4,0](https://activex.microsoft.com/activex/controls/sapi/spchapi.exe), quindi installare i motori vocali specifici.

### <a name="the-speech-engines-used-to-work-with-microsoft-agent-until-i-upgraded-to-windows-xp-what-happened"></a>I motori di riconoscimento vocale utilizzati per lavorare con Microsoft Agent fino a quando non è stato eseguito l'aggiornamento a Windows XP. Che cosa è successo?

Vedere la domanda e la risposta precedenti. È possibile che il processo di aggiornamento di Windows XP abbia rimosso il supporto di SAPI 4,0 già esistente nel computer. È sufficiente reinstallare il runtime di SAPI 4,0 e i motori di riconoscimento vocale SAPI 4,0 dopo l'aggiornamento a Windows XP.

### <a name="i-installed-the-tts3000-text-to-speech-engines-onto-my-computer-that-runs-windows-xp-or-windows-2000-and-correctly-edited-my-programming-accordingly-for-their-use-the-microsoft-agent-characters-speak-audibly-using-these-tts3000-text-to-speech-engines-when-i-or-other-local-administrators-are-logged-in-but-not-when-other-users-without-administrator-privileges-are-logged-into-this-computer-on-windows-98-and-windows-me-these-tts3000-text-to-speech-engines-work-correctly-for-both-sets-of-users-how-can-i-fix-this"></a>Ho installato i motori di sintesi vocale TTS3000 nel mio computer che esegue Windows XP (o Windows 2000) e modificato correttamente la programmazione di conseguenza per l'uso. I caratteri degli agenti Microsoft parlano in modo impercettibile usando questi motori di sintesi vocale TTS3000 quando l'utente o altri amministratori locali sono connessi, ma non quando vengono registrati altri utenti *senza privilegi di amministratore* nel computer. In Windows 98 e Windows me questi motori di sintesi vocale TTS3000 funzionano correttamente per entrambi i set di utenti. Come si risolve questo problema?

È necessario configurare le autorizzazioni di sicurezza per alcune delle chiavi del registro di sistema dei motori di sintesi vocale TTS3000 per abilitarne l'uso da parte degli account utente senza privilegi di amministratore. Questa operazione può essere eseguita con l'editor del registro di sistema del sistema operativo.

### <a name="i-followed-the-procedure-described-as-a-solution-to-the-problem-stated-in-the-previous-question-this-worked-fine-so-that-the-microsoft-agent-characters-could-speak-audibly-using-these-tts3000-text-to-speech-engines-when-users-without-administrator-privileges-were-logged-into-the-windows-xp-or-windows-2000-computer-now-months-later-these-same-tts3000-text-to-speech-engines-have-stopped-working-again-what-happened"></a>Ho seguito la procedura descritta come una soluzione al problema indicato nella domanda precedente. Questa operazione è stata eseguita correttamente, in modo che i caratteri degli agenti Microsoft potessero parlare in modo udibile usando questi motori di sintesi vocale TTS3000 quando gli utenti *senza privilegi di amministratore* sono stati registrati nel computer Windows XP (o Windows 2000). Ora, i mesi successivi, questi stessi motori di sintesi vocale TTS3000 hanno smesso di funzionare. Che cosa è successo?

Quando è stata seguita la procedura descritta per la domanda precedente, sono stati forniti gli account utente non amministratore con autorizzazioni di controllo completo per le chiavi del registro di sistema necessarie. È possibile che uno di questi utenti sia in grado di modificare i valori in modo noto o inconsapevole, modificare di nuovo le autorizzazioni o persino eliminare completamente la chiave del registro di sistema.

Verificare che le chiavi del registro di sistema e le relative autorizzazioni siano state modificate, eliminate o modificate in altro modo. Se necessario, modificare nuovamente queste chiavi del registro di sistema e le relative autorizzazioni oppure reinstallare il testo in TTS3000.

 

 




