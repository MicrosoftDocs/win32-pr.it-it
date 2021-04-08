---
title: Domande frequenti sulla programmazione di script
description: Domande frequenti sulla programmazione di script
ms.assetid: 84078c5b-7b04-48fa-9d0a-d95393c323eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dec468eb5147968ca0db774f081212a78cf40d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043970"
---
# <a name="programming-scripting-faq"></a>Domande frequenti sulla programmazione di script

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

### <a name="when-i-use-microsoft-visual-basic-or-other-development-tools-for-scripting-microsoft-agent-i-do-not-see-all-the-properties-and-events-used-in-your-samples-how-do-i-access-them"></a>Quando si utilizza Microsoft Visual Basic (o altri strumenti di sviluppo) per lo scripting di Microsoft Agent, non vengono visualizzate tutte le proprietà e gli eventi utilizzati negli esempi. Ricerca per categorie accedervi?

La maggior parte degli eventi, dei metodi e delle proprietà supportati dal controllo Microsoft Agent viene esposta solo in fase di esecuzione. Per ulteriori informazioni, consultare [la programmazione del controllo Microsoft Agent](programming-the-microsoft-agent-control.md) .

### <a name="the-map-tag-or-some-other-tag-doesnt-seem-to-work"></a>Il tag della mappa (o un altro tag) non sembra funzionare.

Alcuni tag includono stringhe tra virgolette. Per alcuni linguaggi di programmazione, ad esempio Microsoft Visual Basic e Visual Basic Scripting Edition, potrebbe essere necessario utilizzare due virgolette per definire il parametro del tag o concatenare un carattere di virgolette doppie come parte della stringa. Il secondo è illustrato in questo Visual Basic esempio:

Agente1. Characters ("Genie"). Pronunciare "This is \\ map =" + Chr (34) + "testo parlato" \_ + Chr (34) + "=" + Chr (34) + "Balloon Text" + Chr (34) + " \\ ."

Per la programmazione C, C++ e Java, precede le barre rovesciate e le virgolette doppie con una barra rovesciata. Ad esempio:

BSTR bszSpeak = SysAllocString (L "This is \\ \\ Map = \\ " parlato Text \\ "= \\ " Balloon Text \\ " \\ \\ ");

pCharacter->Speak (bszSpeak,......);

> [!Note]  
> Microsoft Agent non supporta tutti i tag specificati nel Speech API Microsoft. Inoltre, il supporto per alcuni parametri può dipendere dal motore di sintesi vocale installato. Per ulteriori informazioni, vedere [tag di output di sintesi vocale di Microsoft Agent](microsoft-agent-speech-output-tags.md).

 

### <a name="i-dont-seem-to-get-requeststart-and-requestcomplete-events-in-my-script-or-program"></a>Non mi sembra che vengano generati eventi RequestStart e RequestComplete nello script (o programma).

Questa situazione può essere causata da uno dei problemi seguenti:

-   Il linguaggio di programmazione non supporta completamente i controlli ActiveX. Controllare la documentazione per verificare che supporti l'interfaccia ActiveX e gli eventi per gli oggetti ActiveX.
-   In una pagina Web con script non è stato possibile installare o caricare un altro controllo. Verificare che tutti gli altri controlli siano installati e caricati correttamente senza Microsoft Agent.
-   In una pagina Web con script con frame, il `<OBJECT>` tag per il controllo Microsoft Agent è presente in una pagina e gli eventi generati in un'altra pagina. Gli eventi vengono inviati solo alla pagina che ospita il controllo.

### <a name="i-am-using-the-microsoft-agent-control-with-other-activex-controls-on-my-webpage-and-i-dont-seem-to-get-any-events"></a>Sto usando il controllo di Microsoft Agent con altri controlli ActiveX nella mia pagina Web e non mi sembra di ricevere alcun evento.

Verificare se gli altri controlli sono installati correttamente. Se un altro controllo ActiveX non riesce a registrarsi correttamente, il controllo di Microsoft Agent può ricevere i relativi eventi.

### <a name="what-programming-languages-can-i-use-to-program-the-microsoft-agent-control"></a>Quali linguaggi di programmazione è possibile utilizzare per programmare il controllo di Microsoft Agent?

Microsoft Agent deve essere supportato da qualsiasi linguaggio che supporti l'interfaccia ActiveX. Sono inclusi esempi di codice per Visual Basic, VBScript, JScript, C/C++ e Java.

### <a name="can-i-access-the-parameters-returned-from-microsoft-agent-using-jscript"></a>È possibile accedere ai parametri restituiti da Microsoft Agent utilizzando JScript?

Sì, ma attualmente l'unico modo per eseguire questa operazione è usare la `<SCRIPT LANGUAGE="JScript" FOR="*object*" EVENT="event()">` sintassi. Sebbene questa sintassi sia supportata per Microsoft Internet Explorer, altri browser non lo supportano, quindi è consigliabile evitare di utilizzare JScript per questa parte dello script della pagina.

### <a name="can-microsoft-agent-be-used-with-speech-recognition-or-speech-synthesis-text-to-speech-or-tts-engines-other-than-those-supplied-by-microsoft"></a>È possibile utilizzare Microsoft Agent con i motori di riconoscimento vocale o sintesi vocale (sintesi vocale) diversi da quelli forniti da Microsoft?

Sì, purché il motore supporti le interfacce Microsoft Speech API (SAPI) 4,0 richieste da Microsoft Agent. Rivolgersi al fornitore del motore. Per informazioni dettagliate sulle interfacce SAPI richieste da Microsoft Agent, vedere [requisiti del supporto del motore vocale](speech-engine-support-requirements.md).

### <a name="my-page-includes-html-object-tags-for-microsoft-agent-the-lernout--hauspie-truvoice-tts-engine-and-the-microsoft-command-and-control-speech-recognition-engine-but-not-all-the-components-install"></a>La pagina include i tag degli oggetti HTML per Microsoft Agent, il motore di Lernout & Hauspie Speech TruVoice TTS e il motore di riconoscimento vocale di Microsoft Command and Control, ma non tutti i componenti vengono installati.

In genere, è possibile correggere il problema aggiornando la pagina. Come procedura generale, è preferibile specificare prima di tutto il tag di controllo dell'agente Microsoft `<OBJECT>` , quindi il motore di Lernout & Hauspie Speech TruVoice, quindi il motore di riconoscimento vocale di comando e controllo.

### <a name="after-calling-the-moveto-method-my-character-seems-to-freeze-even-though-i-have-return-animations-assigned-to-moving-state-animations"></a>Dopo aver chiamato il metodo MoveTo, il mio carattere sembra bloccarsi anche se sono state restituite animazioni assegnate alle animazioni dello stato di trasferimento.

Quando si riproduce un'animazione, i servizi animazione continuano a visualizzare l'ultimo frame fino a quando non viene chiamata un'altra animazione. Pertanto, è necessario riprodurre un'altra animazione dopo aver chiamato [**MoveTo**](moveto-method.md). Se è stata definita un'animazione **return** per l'animazione dello stato di **trasferimento** , il server lo riprodurrà per primo.

### <a name="when-i-query-the-characters-pitch-property-it-returns-a-value-of--1"></a>Quando si esegue una query sulla proprietà pitch del carattere, viene restituito un valore pari a-1.

Questo errore si verifica se il carattere è stato compilato utilizzando una proprietà pitch predefinita del motore di riconoscimento vocale; ovvero, il pitch non è stato modificato quando il carattere è stato compilato.

### <a name="when-my-code-attempts-to-set-the-tts-mode-id-for-a-text-to-speech-engine-i-get-the-following-error-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Quando il codice tenta di impostare l'ID della modalità TTS per un motore di sintesi vocale, viene verificato l'errore seguente: Impossibile effettuare una chiamata in uscita perché l'applicazione invia una chiamata sincrona di input.

Per impostare la proprietà TTSModeID, è necessario che Speech.dll sia installato. Si tratta in genere di una parte del codice di installazione del motore di riconoscimento vocale. È anche possibile installare questa installazione installando il pannello di controllo dell'oggetto vocale, disponibile dalla pagina dei download di Microsoft Agent.

### <a name="when-i-retry-loading-a-character-that-failed-to-load-the-call-fails-with-a-character-already-loaded-error"></a>Quando si ritenta il caricamento di un carattere che non è stato possibile caricare, la chiamata ha esito negativo con un errore di tipo "carattere già caricato".

Il controllo Microsoft Agent non Scarica un oggetto character (rilascia il riferimento) quando il caricamento del file di caratteri associato non riesce. Se si desidera riprovare a caricare il carattere, è necessario chiamare in modo esplicito [**unload**](unload-method.md) prima di chiamare [**Load**](load-method.md) la seconda volta. Se si tenta di eseguire questa operazione da uno script di pagina Web, è anche necessario precedere la chiamata di **scaricamento** con un'istruzione On Error Resume Next oppure anche la chiamata **unload** avrà esito negativo. Si noti che in JScript non è presente l'istruzione On Error Resume Next.

Potrebbe tuttavia non essere necessario includere il codice per ritentare immediatamente il caricamento di un carattere quando il caricamento del file non riesce. Microsoft Internet Explorer e il componente server Microsoft Agent tentano automaticamente di ritentare diverse volte, quindi le probabilità che il tentativo provochi un caricamento corretto sono remote. Una strategia migliore consiste nell'attendere (impostare un timer) pochi secondi prima di riprovare.

### <a name="how-can-i-install-microsoft-agent-as-part-of-my-application-or-from-my-web-server"></a>Come è possibile installare Microsoft Agent come parte dell'applicazione o del server Web?

È possibile installare Agent dal sito Web Microsoft includendo il relativo *CLSID in un tag Object HTML*. Tuttavia, se si desidera includere e installare Agent dal programma di installazione dell'applicazione o dal proprio server, è necessario scaricare il file CAB di installazione automatica di Microsoft Agent, scaricarlo dalla pagina di download. Durante il download, scegliere l'opzione Salva anziché Esegui del browser. Ogni volta che viene eseguito, il file verrà installato automaticamente nel computer di destinazione. È pertanto possibile specificare il file nello script di installazione.

Non tentare di installare Microsoft Agent copiando le diverse. Dll e tentativi di registrazione. Il tentativo di installare Agent in qualsiasi altro modo, quindi, l'esecuzione del file CAB di installazione automatica non è supportato.

Il sistema di destinazione deve includere anche le versioni recenti di MSVCRT.DLL (runtime di VC + +), REGSVR32.EXE (strumento di registrazione incluso in Microsoft VC + +) e COM. Il modo migliore per verificare che siano installate le versioni corrette consiste nel richiedere che sia installato Microsoft Internet Explorer 3,02 o versione successiva. Tuttavia, è anche possibile concedere in licenza questi requisiti di Runtime. (Per la versione più recente di COM, accedere all'aggiornamento DCOM dal sito Web Microsoft).

Microsoft Agent 2,0 non verrà installato in Microsoft Windows 2000 perché questa versione del sistema operativo include già Agent.

### <a name="can-i-use-the-visual-basic-setup-wizard-to-install-microsoft-agent"></a>È possibile utilizzare l'installazione guidata di Visual Basic per installare Microsoft Agent?

Sebbene sia possibile creare un programma di installazione personalizzato utilizzando il codice Visual Basic (VB), non è possibile utilizzare l'installazione guidata Visual Basic a tale scopo. Per installare Agent da VB, è possibile usare il comando shell, specificando il file CAB di installazione automatica di Microsoft Agent.

### <a name="how-do-i-install-microsoft-agent-on-windows-2000"></a>Ricerca per categorie installare Microsoft Agent in Windows 2000?

Microsoft Agent 2,0 non viene installato in Windows 2000 perché è già incluso nell'ambito del sistema operativo.

### <a name="agentsvr-crashes-when-speak-is-called-with-a-wav-file"></a>AgentSvr si arresta in modo anomalo quando Speak viene chiamato con un file WAV.

Questo può verificarsi quando il carattere USA TTS per l'output parlato, quindi cambia per usare un file WAV. Il testo non è stato specificato nel primo parametro del metodo Speak.

Per evitare l'arresto anomalo del sistema, includere uno spazio nel primo parametro del metodo Speak, anche se non è presente alcun output di testo.

### <a name="even-though-i-have-already-installed-the-agent-language-component-dll-for-a-particular-language-i-still-got-an-error-that-the-component-is-missing-when-i-set-the-characters-language-to-that-language"></a>Anche se è già stato installato il componente della lingua dell'agente (DLL) per una lingua specifica, viene comunque ricevuto un errore che indica che il componente è mancante quando si imposta la lingua del carattere su tale lingua.

Questo problema si verifica in genere quando si dispone di applicazioni agente, ad esempio Microsoft Office 2000 aperti quando si installa il componente del linguaggio Agent. Chiudere tutte le applicazioni e riprovare. Se il problema persiste, riavviare il computer e dovrebbe essere possibile impostare ora l'ID della lingua.

### <a name="when-i-use-the-ampersand--symbol-the-text-around-the-symbol-in-the-characters-word-balloons-is-truncated"></a>Quando si usa il simbolo e commerciale "&", il testo intorno al simbolo nei fumetti di parole del carattere viene troncato.

Si tratta di un problema noto. Per aggirare questo problema, è possibile usare il tag map. Per visualizzare, ad esempio, "A & B" nell'aerostato di parola del carattere, usare "A \\ map =" e "=" && " \\ B" nell'istruzione Speak.

### <a name="my-application-allows-users-to-change-the-default-character-and-when-they-do-the-program-crashes"></a>L'applicazione consente agli utenti di modificare il carattere predefinito e, in caso affermativo, il programma si arresta in modo anomalo.

Le cause possono essere due:

Se si modifica l'ID modalità TTS del carattere predefinito e quindi si consente all'utente di modificare il carattere predefinito tramite ShowDefaultCharacterProperties, AgentSvr si arresterà in modo anomalo.

Questo problema è stato risolto nei sistemi operativi Windows 2000 e Windows XP. Per evitare l'arresto anomalo di altre piattaforme, è consigliabile non consentire all'utente di modificare il carattere predefinito dopo aver modificato l'ID della modalità TTS del carattere predefinito oppure non usare il carattere predefinito nell'applicazione o nella pagina Web.

Se l'applicazione non usa i caratteri dell'agente forniti da Microsoft, assicurarsi che il carattere personalizzato usi una tavolozza con una tavolozza completa di 256 colori. Per ulteriori informazioni, vedere il documento progettazione di caratteri per Microsoft Agent.

### <a name="my-page-loads-the-agent-character-from-multiple-frames-with-ie-5-i-get-the-microsoft-agent-failed-to-load-error"></a>La pagina carica il carattere agente da più frame. Con IE 5, non è stato possibile caricare l'errore di Microsoft Agent.

Si tratta di un problema noto relativo a Internet Explorer 5. Si è verificata una modifica nel modo in cui il browser gestisce un determinato evento, causando l'avvio dell'esecuzione dello script HTML prima dell'avvio di AgentSvr. Per fare in modo che la pagina funzioni con tutte le versioni del browser, è necessario aggiungere questa riga allo script:

AgentControl. Connected = true

che crea in modo esplicito una connessione a AgentSvr. Si noti che è necessario eseguire questa operazione solo se la pagina carica Agent da più frame.

### <a name="when-my-application-tries-to-install-microsoft-agent-on-windows-2000-or-windows-xp-i-get-the-error-that-agent-is-not-compatible-with-windows-2000-or-windows-xp"></a>Quando l'applicazione tenta di installare Microsoft Agent in Windows 2000 (o Windows XP), si verifica un errore che indica che Agent non è compatibile con Windows 2000 (o Windows XP).

Una versione precedente del file CAB del componente core dell'agente MSAGENT.exe, se eseguita in Windows 2000 (e Windows XP), bloccherà l'installazione e visualizzerà un messaggio di errore non accurato che Agent non è compatibile con la versione del sistema operativo in esecuzione. Infatti, i componenti principali di Microsoft Agent 2,0 sono inclusi come parte di Windows 2000 (e Windows XP) e sono già installati per impostazione predefinita tramite il programma di installazione di Windows.

In questa versione, il controllo viene rimosso e il file di installazione non visualizzerà il messaggio di errore precedente in Windows 2000 (o Windows XP). Si noti che questa è l'unica modifica apportata al file di installazione e che non sono state apportate modifiche al codice per i componenti core dell'agente. Di conseguenza, non si è interessati da questo aggiornamento se è già installato l'agente 2,0 o se il sito Web usa un tag oggetto per attivare i download automatici dei componenti di base dell'agente da Microsoft Object Store.

Se si include il file di installazione dei componenti di base dell'agente con l'applicazione o se si pubblica il file di installazione nel server, è possibile scaricare questo aggiornamento. A tale scopo, fare clic qui e selezionare l'opzione "Salva il programma su disco". Per queste circostanze è necessario disporre di una licenza di distribuzione agente valida e corrente.

In alternativa, è possibile aggirare questo problema usando l'opzione invisibile all'utente quando si installa la versione precedente del file di installazione MSAGENT.exe. Il comando della shell è:

**MSAGENT.exe/q: a**

Lo stesso vale per i componenti della lingua dell'agente rilasciati in origine il 1998 ottobre. Si è verificato un controllo che impedisce che i componenti arabo, francese, tedesco, ebraico, italiano, giapponese, coreano, cinese semplificato, spagnolo e cinese tradizionale vengano installati in Windows 2000 (e Windows XP). Le versioni più recenti di questi file di installazione, insieme alle 19 lingue aggiuntive aggiunte nel 2000 marzo, non contengono questo controllo e si installano correttamente in Windows 2000 (e Windows XP).

### <a name="my-customized-character-exhibits-some-unexpected-behavior-with-its-transparency-color-on-windows-2000-and-windows-xp"></a>Il carattere personalizzato presenta un comportamento imprevisto con il colore di trasparenza in Windows 2000 (e Windows XP).

Si tratta di un problema noto per i caratteri creati con una tavolozza di colori minori di 256. I problemi con questi caratteri includono il colore della trasparenza visualizzato sullo sfondo, il testo del fumetto trasparente, il bordo trasparente del fumetto o lo sfondo trasparente del fumetto. Si noti che tali caratteri potrebbero causare l'arresto anomalo delle applicazioni quando vengono caricati nella finestra di dialogo Selezione caratteri agente o nella raccolta Microsoft Office Assistant. I caratteri personalizzati devono usare una tavolozza completa con 256 colori. È possibile usare la tavolozza di esempio fornita per i caratteri dell'assistente di Office come punto di partenza con una tavolozza dei colori 256 completa.

### <a name="the-character-does-not-use-the-british-english-tts-engine-even-though-i-have-set-its-language-id-to-british-english-h0809"></a>Il carattere non usa il motore TTS britannico (Inglese) anche se l'ID lingua è stato impostato su inglese britannico &h0809.

Assicurarsi prima di tutto che siano installati tutti i componenti necessari, ovvero i componenti di base dell'agente, i file binari di runtime SAPI e un motore di lingua inglese britannico conforme a SAPI4 come il motore di TTS3000 britannico, disponibile per il download nella pagina dei download degli agenti. Se il carattere non usa ancora il motore TTS inglese britannico, è probabile che sia installato anche un motore TTS inglese (Stati Uniti). Poiché sia la lingua inglese britannica che quella americana condividono la stessa lingua principale (Inglese) e l'inglese americano è l'impostazione predefinita, Agent sceglierà il primo motore TTS inglese americano disponibile come restituito da SAPI. Per usare un motore di sintesi vocale in inglese britannico, usare invece la proprietà TTSModeID del carattere. Ad esempio, il TTSModeID per la voce TTS3000 britannica inglese è {227A0E41-A92A-11d1-B17B-0020AFED142E}. In Microsoft Visual Basic è possibile usare questo motore impostando il TTSModeID di Merlin come indicato di seguito:

AgentControl. Characters ("Merlin"). TTSModeID = {227A0E41-A92A-11d1-B17B-0020AFED142E}

### <a name="when-the-characters-volume-is-set-to-zero-using-the-speech-tag-vol0-it-either-has-no-effects-or-crashes-the-agentsvr"></a>Quando il volume del carattere è impostato su zero usando il tag di riconoscimento vocale \\ Vol = 0 \\ , non ha alcun effetto o si arresta in modo anomalo agentsvr.

Si tratta di un problema noto. Nei sistemi operativi Windows 95, Windows 98 e Windows me il volume del carattere non cambia ma rimarrà al livello impostato in precedenza. Nelle piattaforme Windows NT 4,0, Windows 2000 e Windows XP questa operazione causerà l'arresto anomalo di AgentSvr, anche quando non è installato un motore TTS. Poiché l'intervallo del volume del carattere, da 0 (silenzioso) a 65535 (volume massimo), è elevato e la differenza tra i livelli successivi è difficilmente distinguibile, la soluzione alternativa consiste nell'impostare il volume su 1 anziché su 0 quando si desidera che la voce del carattere risulti impercettibile.

### <a name="my-customized-characters-return-animation-does-not-play-correctly-after-the-movedown-moveleft-moveright-andor-moveup-animations"></a>L'animazione di ritorno del carattere personalizzato non viene riprodotta correttamente dopo le animazioni MoveDown, MoveLeft, MoveRight e/o MoveUp.

Assicurarsi che venga assegnata una semplice animazione di pronuncia allo stato di pronuncia. Ad esempio, è possibile usare un singolo frame costituito dalla posizione neutra del carattere con sovrapposizioni della bocca.

 

 




