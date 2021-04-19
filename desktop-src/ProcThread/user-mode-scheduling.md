---
description: La pianificazione in modalità utente è un meccanismo leggero che le applicazioni possono utilizzare per pianificare i propri thread.
ms.assetid: f9dd92fe-6d7a-452c-893e-e6df1757e377
title: Pianificazione User-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ceea3c4d4e40d73f48414d074bcb5b4f6e911d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313315"
---
# <a name="user-mode-scheduling"></a>Pianificazione User-Mode

La pianificazione in modalità utente è un meccanismo leggero che le applicazioni possono utilizzare per pianificare i propri thread. Un'applicazione può passare tra i thread UMS in modalità utente senza coinvolgere l' [utilità di pianificazione del sistema](scheduling.md) e riacquisire il controllo del processore se un thread UMS si blocca nel kernel. I thread UMS differiscono dalle [fibre](fibers.md) in quanto ogni thread UMS dispone di un proprio contesto di thread invece di condividere il contesto del thread di un singolo thread. La possibilità di passare da un thread all'altro in modalità utente rende il UMS più efficiente dei [pool di thread](thread-pools.md) per la gestione di un numero elevato di elementi di lavoro di breve durata che richiedono poche chiamate di sistema.

Il sistema UMS è consigliato per le applicazioni con requisiti di prestazioni elevate che richiedono l'esecuzione efficiente di molti thread contemporaneamente su sistemi multiprocessore o multicore. Per sfruttare i vantaggi di UMS, un'applicazione deve implementare un componente dell'utilità di pianificazione che gestisce i thread UMS dell'applicazione e determina quando devono essere eseguiti. Gli sviluppatori devono considerare se i requisiti relativi alle prestazioni dell'applicazione giustificano il lavoro necessario per lo sviluppo di un componente di questo tipo. Le applicazioni con requisiti di prestazioni moderati possono essere gestite meglio consentendo all'utilità di pianificazione del sistema di pianificare i thread.

UMS è disponibile per le applicazioni a 64 bit in esecuzione su versioni a 64 bit di Windows 7 e Windows Server 2008 R2 o versioni successive a 64 bit di Windows. Questa funzionalità non è disponibile nelle versioni di Windows a 32 bit.

Per informazioni dettagliate, vedere le sezioni seguenti:

-   [Utilità di pianificazione UMS](#ums-scheduler)
-   [Thread dell'utilità di pianificazione UMS](#ums-scheduler-thread)
-   [Thread di lavoro UMS, contesti di thread ed elenchi di completamento](#ums-worker-threads-thread-contexts-and-completion-lists)
-   [Funzione del punto di ingresso dell'utilità di pianificazione UMS](#ums-scheduler-entry-point-function)
-   [Esecuzione del thread UMS](#ums-thread-execution)
-   [Procedure consigliate per UMS](#ums-best-practices)

## <a name="ums-scheduler"></a>Utilità di pianificazione UMS

L'utilità di pianificazione UMS di un'applicazione è responsabile della creazione, della gestione e dell'eliminazione di thread UMS e della determinazione del thread UMS da eseguire. L'utilità di pianificazione di un'applicazione esegue le attività seguenti:

-   Crea un thread dell'utilità di pianificazione UMS per ogni processore in cui l'applicazione eseguirà i thread di lavoro di UMS.
-   Crea thread di lavoro UMS per eseguire il lavoro dell'applicazione.
-   Gestisce la coda dei thread di lavoro pronta per l'esecuzione e seleziona i thread da eseguire in base ai criteri di pianificazione dell'applicazione.
-   Crea e monitora uno o più elenchi di completamento in cui il sistema accoda i thread al termine dell'elaborazione nel kernel. Sono inclusi i thread e i thread di lavoro appena creati precedentemente bloccati in una chiamata di sistema che viene sbloccata.
-   Fornisce una funzione del punto di ingresso dell'utilità di pianificazione per gestire le notifiche dal sistema. Il sistema chiama la funzione del punto di ingresso quando viene creato un thread dell'utilità di pianificazione, quando un thread di lavoro si blocca in una chiamata di sistema o quando un thread di lavoro restituisce in modo esplicito il controllo.
-   Esegue attività di pulizia per i thread di lavoro che hanno terminato l'esecuzione.
-   Esegue un arresto ordinato dell'utilità di pianificazione quando richiesto dall'applicazione.

## <a name="ums-scheduler-thread"></a>Thread dell'utilità di pianificazione UMS

Un thread dell'utilità di pianificazione UMS è un thread normale che si è convertito in UMS chiamando la funzione [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) . L'utilità di pianificazione del sistema determina il momento in cui il thread dell'utilità di pianificazione UMS viene eseguito in base alla priorità rispetto ad altri thread pronti. Il processore in cui viene eseguito il thread dell'utilità di pianificazione è influenzato dall'affinità del thread, come per i thread non UMS.

Il chiamante di [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) specifica un elenco di completamento e una funzione del punto di ingresso [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) da associare al thread dell'utilità di pianificazione UMS. Il sistema chiama la funzione del punto di ingresso specificata al termine della conversione del thread chiamante in UMS. La funzione del punto di ingresso dell'utilità di pianificazione è responsabile della determinazione dell'azione successiva appropriata per il thread specificato. Per ulteriori informazioni, vedere la [funzione del punto di ingresso dell'utilità di pianificazione UMS](#ums-scheduler-entry-point-function) più avanti in questo argomento.

Un'applicazione potrebbe creare un thread dell'utilità di pianificazione UMS per ogni processore che verrà usato per eseguire i thread UMS. L'applicazione potrebbe anche impostare l'affinità di ogni thread dell'utilità di pianificazione UMS per un processore logico specifico, che tende a escludere i thread non correlati dall'esecuzione su tale processore, riservando in modo efficace il thread dell'utilità di pianificazione. Tenere presente che l'impostazione dell'affinità dei thread in questo modo può influire sulle prestazioni complessive del sistema, eliminando gli altri processi che potrebbero essere in esecuzione nel sistema. Per ulteriori informazioni sull'affinità di thread, vedere la pagina relativa a [più processori](multiple-processors.md).

## <a name="ums-worker-threads-thread-contexts-and-completion-lists"></a>Thread di lavoro UMS, contesti di thread ed elenchi di completamento

Un thread di lavoro UMS viene creato chiamando [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) con l' \_ attributo thread \_ \_ UMS \_ thread UMS e specificando un contesto del thread UMS e un elenco di completamento.

Un contesto del thread UMS rappresenta lo stato del thread UMS di un thread di lavoro e viene usato per identificare il thread di lavoro nelle chiamate di funzione UMS. Viene creato chiamando [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext).

Viene creato un elenco di completamento chiamando la funzione [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist) . Un elenco di completamento riceve i thread di lavoro UMS che hanno completato l'esecuzione nel kernel e sono pronti per l'esecuzione in modalità utente. Solo il sistema può accodare i thread di lavoro a un elenco di completamento. I nuovi thread di lavoro UMS vengono accodati automaticamente all'elenco di completamento specificato al momento della creazione dei thread. I thread di lavoro bloccati in precedenza vengono accodati anche all'elenco di completamento quando non sono più bloccati.

Ogni thread dell'utilità di pianificazione UMS è associato a un unico elenco di completamento. Tuttavia, lo stesso elenco di completamento può essere associato a un numero qualsiasi di thread dell'utilità di pianificazione UMS e un thread dell'utilità di pianificazione può recuperare i contesti UMS da qualsiasi elenco di completamento per il quale è presente un puntatore.

A ogni elenco di completamento è associato un evento segnalato dal sistema quando Accoda uno o più thread di lavoro a un elenco vuoto. La funzione [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent) recupera un handle per l'evento per un elenco di completamento specificato. Un'applicazione può attendere più di un evento di elenco di completamento insieme ad altri eventi che hanno senso per l'applicazione.

## <a name="ums-scheduler-entry-point-function"></a>Funzione del punto di ingresso dell'utilità di pianificazione UMS

La funzione del punto di ingresso dell'utilità di pianificazione di un'applicazione viene implementata come funzione [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) . Il sistema chiama la funzione del punto di ingresso dell'utilità di pianificazione dell'applicazione negli orari seguenti:

-   Quando un thread non UMS viene convertito in un thread dell'utilità di pianificazione UMS chiamando [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode).
-   Quando un thread di lavoro UMS chiama [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield).
-   Quando un thread di lavoro UMS si blocca in un servizio di sistema, ad esempio una chiamata di sistema o un errore di pagina.

Il parametro *reason* della funzione [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) specifica il motivo per cui è stata chiamata la funzione del punto di ingresso. Se la funzione del punto di ingresso è stata chiamata perché è stato creato un nuovo thread dell'utilità di pianificazione UMS, il parametro *SchedulerParam* contiene i dati specificati dal chiamante di [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode). Se la funzione del punto di ingresso è stata chiamata perché è stato restituito un thread di lavoro UMS, il parametro *SchedulerParam* contiene i dati specificati dal chiamante di [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield). Se la funzione del punto di ingresso è stata chiamata perché un thread di lavoro UMS è bloccato nel kernel, il parametro *SchedulerParam* è null.

La funzione del punto di ingresso dell'utilità di pianificazione è responsabile della determinazione dell'azione successiva appropriata per il thread specificato. Se, ad esempio, un thread di lavoro è bloccato, la funzione del punto di ingresso dell'utilità di pianificazione potrebbe eseguire il thread di lavoro UMS pronto disponibile successivo.

Quando viene chiamata la funzione del punto di ingresso dell'utilità di pianificazione, l'utilità di pianificazione dell'applicazione deve tentare di recuperare tutti gli elementi nell'elenco di completamento associato chiamando la funzione [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) . Questa funzione recupera un elenco di contesti di thread UMS che hanno terminato l'elaborazione nel kernel e sono pronti per l'esecuzione in modalità utente. L'utilità di pianificazione dell'applicazione non deve eseguire i thread UMS direttamente da questo elenco perché questo può causare un comportamento imprevedibile nell'applicazione. L'utilità di pianificazione deve invece recuperare tutti i contesti di thread UMS chiamando la funzione [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem) una volta per ogni contesto, inserire i contesti del thread UMS nella coda dei thread pronti dell'utilità di pianificazione e quindi eseguire i thread UMS dalla coda dei thread pronti.

Se l'utilità di pianificazione non deve attendere più eventi, deve chiamare [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) con un parametro di timeout diverso da zero, in modo che la funzione attenda l'evento dell'elenco di completamento prima di restituire. Se l'utilità di pianificazione deve attendere più eventi dell'elenco di completamento, deve chiamare **DequeueUmsCompletionListItems** con un parametro di timeout pari a zero, in modo che la funzione venga restituita immediatamente, anche se l'elenco di completamento è vuoto. In questo caso, l'utilità di pianificazione può attendere in modo esplicito gli eventi dell'elenco di completamento, ad esempio usando [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

## <a name="ums-thread-execution"></a>Esecuzione del thread UMS

Un thread di lavoro UMS appena creato viene accodato all'elenco di completamento specificato e non inizia l'esecuzione fino a quando l'utilità di pianificazione UMS dell'applicazione non la seleziona per l'esecuzione. Questo comportamento è diverso da quello dei thread non UMS, che l'utilità di pianificazione di sistema pianifica automaticamente per l'esecuzione, a meno che il chiamante non crei in modo esplicito il thread sospeso.

L'utilità di pianificazione esegue un thread di lavoro chiamando [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread) con il contesto UMS del thread di lavoro. Un thread di lavoro UMS viene eseguito fino a quando non viene restituito chiamando la funzione [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) , i blocchi o termina.

## <a name="ums-best-practices"></a>Procedure consigliate per UMS

Le applicazioni che implementano UMS devono seguire queste procedure consigliate:

-   Le strutture sottostanti per i contesti di thread UMS vengono gestite dal sistema e non devono essere modificate direttamente. Usare invece [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation) e [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation) per recuperare e impostare le informazioni su un thread di lavoro UMS.
-   Per evitare deadlock, il thread dell'utilità di pianificazione UMS non deve condividere i blocchi con i thread di lavoro UMS. Sono inclusi i blocchi creati dall'applicazione e i blocchi di sistema che vengono acquisiti indirettamente da operazioni quali l'allocazione dall'heap o il caricamento di dll. Si supponga, ad esempio, che l'utilità di pianificazione esegua un thread di lavoro UMS che carica una DLL. Il thread di lavoro acquisisce il blocco del caricatore e i blocchi. Il sistema chiama la funzione del punto di ingresso dell'utilità di pianificazione, che quindi carica una DLL. Questo causa un deadlock, perché il blocco del caricatore è già attivo e non può essere rilasciato fino a quando il primo thread non viene sbloccato. Per evitare questo problema, delegare il lavoro che potrebbe condividere blocchi con thread di lavoro UMS a un thread di lavoro UMS dedicato o a un thread non UMS.
-   UMS è più efficiente quando la maggior parte dell'elaborazione viene eseguita in modalità utente. Laddove possibile, evitare di effettuare chiamate di sistema nei thread di lavoro UMS.
-   I thread di lavoro UMS non devono presupporre che l'utilità di pianificazione del sistema venga utilizzata. Questo presupposto può avere effetti delicati; Se, ad esempio, un thread nel codice sconosciuto imposta una priorità o un'affinità del thread, l'utilità di pianificazione UMS potrebbe ancora eseguirne l'override. Il codice che presuppone che l'utilità di pianificazione del sistema venga utilizzato potrebbe non comportarsi come previsto e potrebbe interrompersi quando viene chiamato da un thread UMS.
-   Il sistema potrebbe dover bloccare il contesto del thread di un thread di lavoro UMS. Ad esempio, una chiamata di procedura asincrona (APC) in modalità kernel potrebbe modificare il contesto del thread UMS, quindi il contesto del thread deve essere bloccato. Se l'utilità di pianificazione tenta di eseguire il contesto del thread UMS mentre è bloccata, la chiamata avrà esito negativo. Questo comportamento è basato sulla progettazione e l'utilità di pianificazione deve essere progettata per ritentare l'accesso al contesto del thread UMS.

 

 
