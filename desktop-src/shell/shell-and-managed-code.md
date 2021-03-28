---
description: Le estensioni in-process vengono caricate in tutti i processi che li attivano.
title: Linee guida per l'implementazione di estensioni In-Process
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FE830DBF-3F18-453c-9A51-91E10559D0E8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e4dc9fd0573f3f98f0ec1110079f95f56a8c42e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968613"
---
# <a name="guidance-for-implementing-in-process-extensions"></a>Linee guida per l'implementazione di estensioni In-Process

Le estensioni in-process vengono caricate in tutti i processi che li attivano. Ad esempio, un'estensione dello spazio dei nomi della shell può essere caricata in qualsiasi processo che accede direttamente o indirettamente allo spazio dei nomi della shell. Lo spazio dei nomi shell viene usato da molte operazioni della shell, ad esempio la visualizzazione di una finestra di dialogo di file comune, l'avvio di un documento tramite l'applicazione associata o il recupero dell'icona usata per rappresentare un file. Poiché le estensioni in-process possono essere caricate in processi arbitrari, è necessario prestare attenzione che non influiscano negativamente sull'applicazione host o su altre estensioni in-process.

Un runtime di particolare nota è la *Common Language Runtime (CLR)*, nota anche come *codice gestito* o il *.NET Framework*. **Microsoft consiglia di evitare di scrivere estensioni in-process gestite in Esplora risorse o in Windows Internet Explorer e non li considera uno scenario supportato.**

In questo argomento vengono illustrati i fattori da considerare quando si determina se un runtime diverso da CLR è adatto per l'utilizzo da parte di estensioni in-process. Esempi di altri Runtime includono Java, Visual Basic, JavaScript/ECMAScript, Delphi e la libreria di runtime C/C++. In questo argomento vengono inoltre forniti alcuni motivi per cui il codice gestito non è supportato nelle estensioni in-process.

## <a name="version-conflicts"></a>Conflitti di versione

Un conflitto di versione può verificarsi tramite un runtime che non supporta il caricamento di più versioni di runtime all'interno di un singolo processo. Le versioni di CLR precedenti alla versione 4,0 rientrano in questa categoria. Se il caricamento di una versione di un Runtime impedisce il caricamento di altre versioni dello stesso runtime, questo può creare un conflitto se l'applicazione host o un'altra estensione in-process usa una versione in conflitto. Nel caso di una versione in conflitto con un'altra estensione in-process, il conflitto può essere difficile da riprodurre perché l'errore richiede le estensioni in conflitto corrette e la modalità di errore dipende dall'ordine in cui vengono caricate le estensioni in conflitto.

Si consideri un'estensione in-process scritta utilizzando una versione di CLR precedente alla versione 4,0. Ogni applicazione nel computer che utilizza una finestra di dialogo **Apri** file potrebbe potenzialmente avere il codice gestito della finestra di dialogo e la relativa dipendenza CLR di supervisore caricata nel processo dell'applicazione. L'applicazione o l'estensione che innanzitutto carica una versione precedente a 4,0 di CLR nel processo dell'applicazione limita le versioni di CLR che possono essere utilizzate successivamente da tale processo. Se un'applicazione gestita con una finestra di dialogo **aperta** si basa su una versione in conflitto di CLR, è possibile che l'estensione non venga eseguita correttamente e che sia possibile che si verifichino errori nell'applicazione. Viceversa, se l'estensione è la prima a caricare in un processo e una versione in conflitto del codice gestito tenta di avviare dopo tale operazione (ad esempio un'applicazione gestita o un'applicazione in esecuzione carica il CLR su richiesta), l'operazione ha esito negativo. Per l'utente, sembra che alcune funzionalità dell'applicazione smettano di funzionare in modo casuale o che l'applicazione si arresti in modo anomalo.

Si noti che le versioni di CLR uguali o successive alla versione 4,0 non sono generalmente suscettibili al problema di controllo delle versioni, perché sono progettate per coesistere tra loro e con la maggior parte delle versioni precedenti a 4,0 di CLR (ad eccezione della versione 1,0, che non può coesistere con altre versioni). Tuttavia, è possibile che si verifichino problemi diversi dai conflitti di versione come descritto nella parte restante di questo argomento.

## <a name="performance-issues"></a>Problemi di prestazioni

I problemi di prestazioni possono verificarsi con i runtime che impongono una riduzione significativa delle prestazioni quando vengono caricati in un processo. La riduzione delle prestazioni può compromettere l'utilizzo della memoria, l'utilizzo della CPU, il tempo trascorso o persino il consumo dello spazio degli indirizzi. CLR, JavaScript/ECMAScript e Java sono noti come runtime a elevato effetto. Poiché le estensioni in-process possono essere caricate in molti processi e spesso vengono eseguite in momenti sensibili alle prestazioni, ad esempio quando si prepara un menu per la visualizzazione dell'utente, i runtime a impatto elevato possono influire negativamente sulla velocità di risposta complessiva.

Un runtime a impatto elevato che utilizza risorse significative può causare un errore nel processo host o in un'altra estensione in-process. Ad esempio, un runtime ad alto effetto che utilizza centinaia di megabyte di spazio di indirizzi per il relativo heap può comportare che l'applicazione host non sia in grado di caricare un set di dati di grandi dimensioni. Inoltre, dal momento che le estensioni in-process possono essere caricate in più processi, l'utilizzo elevato delle risorse in una singola estensione può essere rapidamente moltiplicato per un consumo di risorse elevato nell'intero sistema.

Se un runtime rimane caricato o continua a usare le risorse anche quando l'estensione che usa tale Runtime viene scaricata, il runtime non è adatto per l'uso in un'estensione.

## <a name="issues-specific-to-the-net-framework"></a>Problemi specifici del .NET Framework

Nelle sezioni seguenti vengono illustrati esempi di problemi rilevati con l'utilizzo di codice gestito per le estensioni. Non si tratta di un elenco completo di tutti i possibili problemi che potrebbero verificarsi. I problemi illustrati di seguito sono entrambi i motivi per cui il codice gestito non è supportato nelle estensioni e i punti da considerare quando si valuta l'uso di altri Runtime.

### <a name="re-entrancy"></a>Rientro

Quando CLR blocca un thread di Apartment a thread singolo (STA), ad esempio a causa di un monitoraggio. Immettere, WaitHandle. WaitOne o l'istruzione di [**blocco**](https://msdn.microsoft.com/library/c5kehkcz(v=VS.71).aspx) con conflitti, il CLR, nella configurazione standard, immette un ciclo di messaggi annidati mentre è in attesa. Molti metodi di estensione non sono consentiti dall'elaborazione dei messaggi e questa rientranza imprevedibile e imprevista può causare un comportamento anomalo, che è difficile da riprodurre e diagnosticare.

### <a name="the-multithreaded-apartment"></a>Apartment con multithreading

CLR crea *Runtime Callable Wrapper* per gli oggetti Component Object Model (com). Questi stessi Runtime Callable Wrapper vengono eliminati in un secondo momento dal finalizzatore di CLR, che fa parte dell'Apartment a thread multipli (MTA). Per lo spostamento del proxy da STA all'MTA è necessario il marshalling, ma non tutte le interfacce utilizzate dalle estensioni possono essere sottoposte a marshalling.

### <a name="non-deterministic-object-lifetimes"></a>Durate degli oggetti non deterministici

CLR ha garanzie di durata degli oggetti più vulnerabili rispetto al codice nativo. Molte estensioni hanno requisiti di conteggio dei riferimenti su oggetti e interfacce e il modello di Garbage Collection utilizzato da CLR non è in grado di soddisfare tali requisiti.

-   Se un oggetto CLR ottiene un riferimento a un oggetto COM, il riferimento all'oggetto COM utilizzato dal Runtime Callable Wrapper non viene rilasciato fino a quando il Runtime Callable Wrapper non viene sottoposto a Garbage Collection. Il comportamento di rilascio non deterministico può essere in conflitto con alcuni contratti di interfaccia. Il metodo [**IPersistPropertyBag:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768206(v=vs.85)) , ad esempio, richiede che nessun riferimento all'elenco proprietà venga mantenuto dall'oggetto quando il metodo **Load** restituisce.
-   Se un riferimento a un oggetto CLR viene restituito al codice nativo, il Runtime Callable Wrapper cede il riferimento all'oggetto CLR [**quando viene effettuata**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) la chiamata finale del Runtime Callable Wrapper, ma l'oggetto CLR sottostante non viene finalizzato fino a quando non viene sottoposto a Garbage Collection. La finalizzazione non deterministica può essere in conflitto con alcuni contratti di interfaccia. Ad esempio, i gestori di anteprime sono necessari per rilasciare tutte le risorse immediatamente quando il conteggio dei riferimenti scende a zero.

## <a name="acceptable-uses-of-managed-code-and-other-runtimes"></a>Usi accettabili del codice gestito e di altri Runtime

È accettabile usare codice gestito e altri runtime per implementare estensioni out-of-process. Di seguito sono riportati alcuni esempi di estensioni della shell out-of-process:

-   Gestori di anteprime
-   Azioni basate su riga di comando, ad esempio quelle registrate sotto le \\  \\ sottochiavi del **comando** del verbo Shell.
-   Oggetti COM implementati in un server locale per i punti di estensione della shell che consentono l'attivazione out-of-process.

Alcune estensioni possono essere implementate come estensioni in-process o out-of-process. È possibile implementare queste estensioni come estensioni out-of-process se non soddisfano questi requisiti per le estensioni in-process. Nell'elenco seguente vengono illustrati esempi di estensioni che possono essere implementate come estensioni in-process o out-of-process:

-   [**IExecuteCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexecutecommand) associato a una voce **DelegateExecute** registrata in una  \\  \\ sottochiave del **comando** di un verbo della shell.
-   [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) associato al CLSID registrato in una  \\  \\ sottochiave **DropTarget** del verbo della shell.
-   [**IExplorerCommandState**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) associato a una voce **CommandStateHandler** registrata in una  \\ sottochiave del *verbo* della shell.

 

 
