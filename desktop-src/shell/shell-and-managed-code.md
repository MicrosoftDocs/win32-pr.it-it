---
description: Le estensioni in-process vengono caricate in tutti i processi che le attivano.
title: Linee guida per l'implementazione In-Process estensioni
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FE830DBF-3F18-453c-9A51-91E10559D0E8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 15ccbee300cbfe1b08bc0509472ac3afcaa9ea3db54f6f1e38131cc08d2e8381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858176"
---
# <a name="guidance-for-implementing-in-process-extensions"></a>Linee guida per l'implementazione In-Process estensioni

Le estensioni in-process vengono caricate in tutti i processi che le attivano. Ad esempio, un'estensione dello spazio dei nomi Shell può essere caricata in qualsiasi processo che accede allo spazio dei nomi Shell direttamente o indirettamente. Lo spazio dei nomi Shell viene usato da molte operazioni shell, ad esempio la visualizzazione di una finestra di dialogo file comune, l'avvio di un documento tramite l'applicazione associata o l'ottenimento dell'icona usata per rappresentare un file. Poiché le estensioni in-process possono essere caricate in processi arbitrari, è necessario fare attenzione a non influire negativamente sull'applicazione host o su altre estensioni in-process.

Un runtime di particolare nota è Common Language Runtime  *(CLR),* noto anche come codice gestito *o*.NET Framework . **Microsoft sconsiglia di scrivere estensioni in-process gestite Windows Explorer o Windows Internet Explorer e non le considera uno scenario supportato.**

Questo argomento illustra i fattori da considerare quando si determina se un runtime diverso da CLR è adatto per l'uso da parte delle estensioni in-process. Esempi di altri runtime includono Java, Visual Basic, JavaScript/ECMAScript, Delphi e la libreria di runtime C/C++. Questo argomento illustra anche alcuni motivi per cui il codice gestito non è supportato nelle estensioni in-process.

## <a name="version-conflicts"></a>Conflitti di versione

Un conflitto di versione può verificarsi tramite un runtime che non supporta il caricamento di più versioni di runtime all'interno di un singolo processo. Le versioni di CLR precedenti alla versione 4.0 rientrano in questa categoria. Se il caricamento di una versione di un runtime preclude il caricamento di altre versioni dello stesso runtime, questo può creare un conflitto se l'applicazione host o un'altra estensione in-process usa una versione in conflitto. In caso di conflitto di versione con un'altra estensione in-process, il conflitto può essere difficile da riprodurre perché l'errore richiede le estensioni in conflitto e la modalità di errore dipende dall'ordine in cui vengono caricate le estensioni in conflitto.

Si consideri un'estensione in-process scritta usando una versione di CLR precedente alla versione 4.0. Ogni applicazione nel computer che usa una finestra di dialogo Apri **file** potrebbe potenzialmente caricare nel processo dell'applicazione il codice gestito della finestra di dialogo e la relativa dipendenza CLR che lo contiene. L'applicazione o l'estensione che prima carica una versione precedente alla 4.0 di CLR nel processo dell'applicazione limita le versioni di CLR che possono essere usate successivamente da tale processo. Se un'applicazione  gestita con una finestra di dialogo Apri si basa su una versione in conflitto di CLR, l'estensione potrebbe non essere eseguita correttamente e potrebbe causare errori nell'applicazione. Al contrario, se l'estensione è la prima a caricare in un processo e una versione in conflitto del codice gestito tenta di avviarsi dopo tale operazione (ad esempio, un'applicazione gestita o un'applicazione in esecuzione carica CLR su richiesta), l'operazione non riesce. Per l'utente, sembra che alcune funzionalità dell'applicazione smettano in modo casuale di funzionare o che l'applicazione si arresti in modo anomalo.

Si noti che le versioni di CLR uguali o successive alla versione 4.0 non sono in genere soggette al problema di controllo delle versioni perché sono progettate per coesistere tra loro e con la maggior parte delle versioni precedenti alla 4.0 di CLR (ad eccezione della versione 1.0, che non può coesistere con altre versioni). Tuttavia, possono verificarsi problemi diversi da conflitti di versione, come illustrato nella parte restante di questo argomento.

## <a name="performance-issues"></a>Problemi di prestazioni

I problemi di prestazioni possono verificarsi con i runtime che impongono una riduzione significativa delle prestazioni quando vengono caricati in un processo. La perdita di prestazioni può essere sotto forma di utilizzo della memoria, utilizzo della CPU, tempo trascorso o persino utilizzo dello spazio degli indirizzi. CLR, JavaScript/ECMAScript e Java sono noti come runtime ad alto impatto. Poiché le estensioni in-process possono essere caricate in molti processi e vengono spesso eseguite in momenti sensibili alle prestazioni (ad esempio quando si prepara un menu per visualizzare l'utente), i runtime ad alto impatto possono influire negativamente sulla velocità di risposta complessiva.

Un runtime ad alto impatto che utilizza risorse significative può causare un errore nel processo host o in un'altra estensione in-process. Ad esempio, un runtime ad alto impatto che utilizza centinaia di megabyte di spazio indirizzi per il relativo heap può causare l'impossibilità dell'applicazione host di caricare un set di dati di grandi dimensioni. Inoltre, poiché le estensioni in-process possono essere caricate in più processi, l'utilizzo elevato delle risorse in una singola estensione può moltiplicarsi rapidamente in un consumo elevato di risorse nell'intero sistema.

Se un runtime rimane caricato o continua a utilizzare le risorse anche quando l'estensione che usa tale runtime è stata scaricata, tale runtime non è adatto per l'uso in un'estensione.

## <a name="issues-specific-to-the-net-framework"></a>Problemi specifici dell'.NET Framework

Le sezioni seguenti illustrano esempi di problemi riscontrati con l'uso di codice gestito per le estensioni. Non sono un elenco completo di tutti i possibili problemi che potrebbero verificarsi. I problemi illustrati di seguito sono entrambi motivi per cui il codice gestito non è supportato nelle estensioni e punti da considerare quando si valuta l'uso di altri runtime.

### <a name="re-entrancy"></a>Re-entrancy

Quando CLR blocca un thread apartment a thread singolo (STA), ad esempio a causa di un'istruzione Monitor.Enter, WaitHandle.WaitOne o di blocco contestato, CLR, nella configurazione standard, entra in un ciclo di messaggi annidato durante l'attesa. [](https://msdn.microsoft.com/library/c5kehkcz(v=VS.71).aspx) A molti metodi di estensione non è consentito elaborare messaggi e questa reentrancy imprevedibile e imprevista può comportare un comportamento anomalo difficile da riprodurre e diagnosticare.

### <a name="the-multithreaded-apartment"></a>Apartment multithreading

CLR crea *runtime callable wrapper per* Component Object Model (COM). Questi stessi runtime callable wrapper vengono distrutti in un secondo momento dal finalizzatore CLR, che fa parte dell'apartment multithreading (MTA). Lo spostamento del proxy da STA all'MTA richiede il marshalling, ma non tutte le interfacce usate dalle estensioni possono essere marshalling.

### <a name="non-deterministic-object-lifetimes"></a>Durate degli oggetti non deterministici

CLR ha garanzie di durata degli oggetti più deboli rispetto al codice nativo. Molte estensioni hanno requisiti di conteggio dei riferimenti per oggetti e interfacce e il modello di Garbage Collection utilizzato da CLR non può soddisfare questi requisiti.

-   Se un oggetto CLR ottiene un riferimento a un oggetto COM, il riferimento all'oggetto COM mantenuto dal Runtime Callable Wrapper non viene rilasciato fino a quando runtime Callable Wrapper non viene sottoposto a Garbage Collection. Il comportamento di rilascio non deterministico può essere in conflitto con alcuni contratti di interfaccia. Ad esempio, il [**metodo IPersistPropertyBag::Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768206(v=vs.85)) richiede che nessun riferimento al contenitore di proprietà sia mantenuto dall'oggetto quando il **metodo Load** viene restituito.
-   Se un riferimento a un oggetto CLR viene restituito al codice nativo, runtime Callable Wrapper rinuncia al riferimento all'oggetto CLR quando viene effettuata la chiamata finale di Runtime Callable Wrapper a [**Release,**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ma l'oggetto CLR sottostante non viene finalizzato fino a quando non viene sottoposto a Garbage Collection. La finalizzazione non deterministica può essere in conflitto con alcuni contratti di interfaccia. Ad esempio, i gestori di anteprime sono necessari per rilasciare tutte le risorse immediatamente quando il conteggio dei riferimenti scende a zero.

## <a name="acceptable-uses-of-managed-code-and-other-runtimes"></a>Usi accettabili del codice gestito e di altri runtime

È accettabile usare codice gestito e altri runtime per implementare estensioni out-of-process. Di seguito sono riportati alcuni esempi di estensioni della shell out-of-process:

-   Gestori di anteprima
-   Azioni basate sulla riga di comando, ad esempio quelle registrate nelle **sottochiavi** dei \\ *comandi dei verbi* \\  della shell.
-   Oggetti COM implementati in un server locale, per i punti di estensione shell che consentono l'attivazione out-of-process.

Alcune estensioni possono essere implementate come estensioni in-process o out-of-process. È possibile implementare queste estensioni come estensioni out-of-process se non soddisfano questi requisiti per le estensioni in-process. L'elenco seguente mostra esempi di estensioni che possono essere implementate come estensioni in-process o out-of-process:

-   [**IExecuteCommand associato**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexecutecommand) a una **voce DelegateExecute** registrata in una **sottochiave** del comando \\ *del* \\ **verbo** della shell.
-   [**IDropTarget associato**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) al CLSID registrato in una **sottochiave** \\ DropTarget del *verbo* della \\  shell.
-   [**IExplorerCommandState associato**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) a una **voce CommandStateHandler registrata** in una **sottochiave del** \\ *verbo della* shell.

 

 
