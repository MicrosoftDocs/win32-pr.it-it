---
description: La pianificazione in modalità utente è un meccanismo leggero che le applicazioni possono usare per pianificare i propri thread.
ms.assetid: f9dd92fe-6d7a-452c-893e-e6df1757e377
title: User-Mode pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a13b30685dbcbfc4d3d502e02bdbfdc10d15ea1f804cc6a8391073c44ce447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074241"
---
# <a name="user-mode-scheduling"></a>User-Mode pianificazione

La pianificazione in modalità utente è un meccanismo leggero che le applicazioni possono usare per pianificare i propri thread. Un'applicazione può passare da un thread [](scheduling.md) UMS all'altro in modalità utente senza coinvolgere l'utilità di pianificazione del sistema e ottenere nuovamente il controllo del processore se un thread UMS si blocca nel kernel. I thread UMS si differenziano dai [fiber](fibers.md) in modo che ogni thread UMS abbia un proprio contesto di thread anziché condividere il contesto di thread di un singolo thread. La possibilità di passare da un thread all'altro in modalità utente rende UMS più efficiente rispetto ai pool di [thread](thread-pools.md) per la gestione di un numero elevato di elementi di lavoro di breve durata che richiedono poche chiamate di sistema.

UmS è consigliato per le applicazioni con requisiti di prestazioni elevate che devono eseguire in modo efficiente molti thread contemporaneamente in sistemi multiprocessore o multicore. Per sfruttare i vantaggi di UMS, un'applicazione deve implementare un componente dell'utilità di pianificazione che gestisce i thread UMS dell'applicazione e determina quando devono essere eseguiti. Gli sviluppatori devono valutare se i requisiti di prestazioni dell'applicazione giustificano il lavoro necessario per lo sviluppo di un componente di questo tipo. Le applicazioni con requisiti di prestazioni moderati potrebbero essere gestite meglio consentendo all'utilità di pianificazione di sistema di pianificare i thread.

UMS è disponibile per le applicazioni a 64 bit in esecuzione in versioni a 64 bit di Windows 7 e Windows Server 2008 R2 o versioni successive a 64 bit di Windows. Questa funzionalità non è disponibile nelle versioni a 32 bit di Windows.

Per informazioni dettagliate, vedere le sezioni seguenti:

-   [Utilità di pianificazione UMS](#ums-scheduler)
-   [Thread dell'utilità di pianificazione UMS](#ums-scheduler-thread)
-   [Thread di lavoro UMS, contesti di thread ed elenchi di completamento](#ums-worker-threads-thread-contexts-and-completion-lists)
-   [Funzione del punto di ingresso dell'utilità di pianificazione UMS](#ums-scheduler-entry-point-function)
-   [Esecuzione di thread UMS](#ums-thread-execution)
-   [Procedure consigliate per UMS](#ums-best-practices)

## <a name="ums-scheduler"></a>Utilità di pianificazione UMS

L'utilità di pianificazione UMS di un'applicazione è responsabile della creazione, della gestione e dell'eliminazione dei thread UMS e della determinazione del thread UMS da eseguire. L'utilità di pianificazione di un'applicazione esegue le attività seguenti:

-   Crea un thread dell'utilità di pianificazione UMS per ogni processore in cui l'applicazione eseguirà i thread di lavoro UMS.
-   Crea thread di lavoro UMS per eseguire il lavoro dell'applicazione.
-   Mantiene la propria coda di thread di lavoro pronti per l'esecuzione e seleziona i thread da eseguire in base ai criteri di pianificazione dell'applicazione.
-   Crea e monitora uno o più elenchi di completamento in cui il sistema accoda i thread al termine dell'elaborazione nel kernel. Sono inclusi i thread di lavoro appena creati e i thread bloccati in precedenza in una chiamata di sistema che diventano sbloccati.
-   Fornisce una funzione del punto di ingresso dell'utilità di pianificazione per gestire le notifiche dal sistema. Il sistema chiama la funzione del punto di ingresso quando viene creato un thread dell'utilità di pianificazione, quando un thread di lavoro si blocca in una chiamata di sistema o quando un thread di lavoro cede il controllo in modo esplicito.
-   Esegue attività di pulizia per i thread di lavoro che hanno terminato l'esecuzione.
-   Esegue un arresto ordinato dell'utilità di pianificazione quando richiesto dall'applicazione.

## <a name="ums-scheduler-thread"></a>Thread dell'utilità di pianificazione UMS

Un thread dell'utilità di pianificazione UMS è un thread comune che si è convertito in UMS chiamando la [**funzione EnterUmsSchedulingMode.**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) L'utilità di pianificazione di sistema determina quando il thread dell'utilità di pianificazione UMS viene eseguito in base alla priorità rispetto ad altri thread pronti. Il processore su cui viene eseguito il thread dell'utilità di pianificazione è influenzato dall'affinità del thread, come per i thread non UMS.

Il chiamante di [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) specifica un elenco di completamento e una funzione del punto di ingresso [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) da associare al thread dell'utilità di pianificazione UMS. Il sistema chiama la funzione del punto di ingresso specificato al termine della conversione del thread chiamante in UMS. La funzione del punto di ingresso dell'utilità di pianificazione è responsabile della determinazione dell'azione successiva appropriata per il thread specificato. Per altre informazioni, vedere [Funzione del punto di ingresso dell'utilità](#ums-scheduler-entry-point-function) di pianificazione UMS più avanti in questo argomento.

Un'applicazione potrebbe creare un thread dell'utilità di pianificazione UMS per ogni processore che verrà usato per eseguire i thread UMS. L'applicazione potrebbe anche impostare l'affinità di ogni thread dell'utilità di pianificazione UMS per un processore logico specifico, che tende a escludere thread non correlati dall'esecuzione su tale processore, riservando in modo efficace tale thread dell'utilità di pianificazione. Tenere presente che l'impostazione dell'affinità dei thread in questo modo può influire sulle prestazioni complessive del sistema, affamando gli altri processi che potrebbero essere in esecuzione nel sistema. Per altre informazioni sull'affinità dei thread, vedere [Più processori.](multiple-processors.md)

## <a name="ums-worker-threads-thread-contexts-and-completion-lists"></a>Thread di lavoro UMS, contesti di thread ed elenchi di completamento

Un thread di lavoro UMS viene creato chiamando [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) con l'attributo PROC THREAD ATTRIBUTE UMS THREAD e specificando un contesto di thread UMS e un elenco \_ \_ di \_ \_ completamento.

Un contesto di thread UMS rappresenta lo stato del thread UMS di un thread di lavoro e viene usato per identificare il thread di lavoro nelle chiamate di funzione UMS. Viene creato chiamando [**CreateUmsThreadContext.**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)

Un elenco di completamento viene creato chiamando [**la funzione CreateUmsCompletionList.**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist) Un elenco di completamento riceve i thread di lavoro UMS che hanno completato l'esecuzione nel kernel e sono pronti per l'esecuzione in modalità utente. Solo il sistema può accodare i thread di lavoro a un elenco di completamento. I nuovi thread di lavoro UMS vengono accodati automaticamente all'elenco di completamento specificato al momento della creazione dei thread. Anche i thread di lavoro bloccati in precedenza vengono accodati all'elenco di completamento quando non sono più bloccati.

Ogni thread dell'utilità di pianificazione UMS è associato a un singolo elenco di completamento. Tuttavia, lo stesso elenco di completamento può essere associato a un numero qualsiasi di thread dell'utilità di pianificazione UMS e un thread dell'utilità di pianificazione può recuperare i contesti UMS da qualsiasi elenco di completamento per cui dispone di un puntatore .

A ogni elenco di completamento è associato un evento segnalato dal sistema quando accoda uno o più thread di lavoro a un elenco vuoto. La [**funzione GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent) recupera un handle per l'evento per un elenco di completamento specificato. Un'applicazione può attendere più di un evento dell'elenco di completamento insieme ad altri eventi che hanno senso per l'applicazione.

## <a name="ums-scheduler-entry-point-function"></a>Funzione del punto di ingresso dell'utilità di pianificazione UMS

La funzione del punto di ingresso dell'utilità di pianificazione di un'applicazione viene implementata [*come funzione UmsSchedulerProc.*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) Il sistema chiama la funzione del punto di ingresso dell'utilità di pianificazione dell'applicazione nei momenti seguenti:

-   Quando un thread non UMS viene convertito in un thread dell'utilità di pianificazione UMS chiamando [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode).
-   Quando un thread di lavoro UMS chiama [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield).
-   Quando un thread di lavoro UMS si blocca in un servizio di sistema, ad esempio una chiamata di sistema o un errore di pagina.

Il *parametro Reason* della funzione [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) specifica il motivo per cui è stata chiamata la funzione del punto di ingresso. Se la funzione del punto di ingresso è stata chiamata perché è stato creato un nuovo thread dell'utilità di pianificazione UMS, il parametro *SchedulerParam* contiene i dati specificati dal chiamante di [**EnterUmsSchedulingMode.**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) Se la funzione del punto di ingresso è stata chiamata perché è stato restituito un thread di lavoro UMS, il parametro *SchedulerParam* contiene i dati specificati dal chiamante di [**UmsThreadYield.**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) Se la funzione del punto di ingresso è stata chiamata perché un thread di lavoro UMS è bloccato nel kernel, il *parametro SchedulerParam* è NULL.

La funzione del punto di ingresso dell'utilità di pianificazione è responsabile della determinazione dell'azione successiva appropriata per il thread specificato. Ad esempio, se un thread di lavoro è bloccato, la funzione del punto di ingresso dell'utilità di pianificazione potrebbe eseguire il successivo thread di lavoro UMS pronto disponibile.

Quando viene chiamata la funzione del punto di ingresso dell'utilità di pianificazione, l'utilità di pianificazione dell'applicazione deve tentare di recuperare tutti gli elementi nell'elenco di completamento associato chiamando la [**funzione DequeueUmsCompletionListItems.**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) Questa funzione recupera un elenco di contesti di thread UMS che hanno terminato l'elaborazione nel kernel e sono pronti per l'esecuzione in modalità utente. L'utilità di pianificazione dell'applicazione non deve eseguire thread UMS direttamente da questo elenco perché ciò può causare un comportamento imprevedibile nell'applicazione. Al contrario, l'utilità di pianificazione deve recuperare tutti i contesti di thread UMS chiamando la funzione [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem) una volta per ogni contesto, inserire i contesti dei thread UMS nella coda dei thread pronti dell'utilità di pianificazione e quindi eseguire solo i thread UMS dalla coda di thread pronta.

Se l'utilità di pianificazione non deve attendere più eventi, deve chiamare [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) con un parametro di timeout diverso da zero, in modo che la funzione attenda l'evento dell'elenco di completamento prima della restituzione. Se l'utilità di pianificazione deve attendere più eventi dell'elenco di completamento, deve chiamare **DequeueUmsCompletionListItems** con un parametro di timeout pari a zero in modo che la funzione restituisca immediatamente un risultato, anche se l'elenco di completamento è vuoto. In questo caso, l'utilità di pianificazione può attendere in modo esplicito gli eventi dell'elenco di completamento, ad esempio usando [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

## <a name="ums-thread-execution"></a>Esecuzione di thread UMS

Un thread di lavoro UMS appena creato viene accodato all'elenco di completamento specificato e non inizia l'esecuzione fino a quando l'utilità di pianificazione UMS dell'applicazione non lo seleziona per l'esecuzione. Questo comportamento è diverso dai thread non UMS, che l'utilità di pianificazione del sistema pianifica automaticamente per l'esecuzione, a meno che il chiamante non crei in modo esplicito il thread sospeso.

L'utilità di pianificazione esegue un thread di lavoro chiamando [**ExecuteUmsThread con**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread) il contesto UMS del thread di lavoro. Un thread di lavoro UMS viene eseguito fino a quando non cede chiamando la funzione [**UmsThreadYield,**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) i blocchi o le terminazioni.

## <a name="ums-best-practices"></a>Procedure consigliate per UMS

Le applicazioni che implementano UMS devono seguire queste procedure consigliate:

-   Le strutture sottostanti per i contesti di thread UMS sono gestite dal sistema e non devono essere modificate direttamente. Usare invece [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation) e [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation) per recuperare e impostare informazioni su un thread di lavoro UMS.
-   Per evitare deadlock, il thread dell'utilità di pianificazione UMS non deve condividere blocchi con i thread di lavoro UMS. Sono inclusi sia i blocchi creati dall'applicazione che i blocchi di sistema acquisiti indirettamente da operazioni quali l'allocazione dall'heap o il caricamento di DLL. Si supponga, ad esempio, che l'utilità di pianificazione esempli un thread di lavoro UMS che carica una DLL. Il thread di lavoro acquisisce il blocco e i blocchi del caricatore. Il sistema chiama la funzione del punto di ingresso dell'utilità di pianificazione, che carica quindi una DLL. Ciò causa un deadlock, perché il blocco del caricatore è già attivo e non può essere rilasciato fino a quando il primo thread non si sblocca. Per evitare questo problema, delegare il lavoro che potrebbe condividere blocchi con thread di lavoro UMS a un thread di lavoro UMS dedicato o a un thread non UMS.
-   UMS è più efficiente quando la maggior parte dell'elaborazione viene eseguita in modalità utente. Quando possibile, evitare di effettuare chiamate di sistema nei thread di lavoro UMS.
-   I thread di lavoro UMS non devono presupporre che venga usata l'utilità di pianificazione di sistema. Questo presupposto può avere effetti lievi. Ad esempio, se un thread nel codice sconosciuto imposta la priorità o l'affinità di un thread, l'utilità di pianificazione UMS potrebbe comunque eseguirne l'override. Il codice che presuppone che venga usata l'utilità di pianificazione di sistema potrebbe non comportarsi come previsto e potrebbe interrompersi quando viene chiamato da un thread UMS.
-   Il sistema potrebbe dover bloccare il contesto del thread di un thread di lavoro UMS. Ad esempio, una chiamata di procedura asincrona in modalità kernel potrebbe modificare il contesto del thread UMS, quindi il contesto del thread deve essere bloccato. Se l'utilità di pianificazione tenta di eseguire il contesto del thread UMS mentre è bloccato, la chiamata avrà esito negativo. Questo comportamento è previsto e l'utilità di pianificazione deve essere progettata per ritentare l'accesso al contesto del thread UMS.

 

 
