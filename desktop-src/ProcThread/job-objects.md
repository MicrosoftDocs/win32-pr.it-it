---
description: Un oggetto processo consente di gestire gruppi di processi come unità. Gli oggetti processo sono oggetti namable, a protezione diretta e condivisibili che controllano gli attributi dei processi ad essi associati.
ms.assetid: 59296384-5e78-44dd-8019-f1df6668928b
title: Oggetti processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e6d9758faf2b66f047ca60dbba91601b202b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345471"
---
# <a name="job-objects"></a>Oggetti processo

Un *oggetto processo* consente la gestione di gruppi di processi come unità. Gli oggetti processo sono oggetti namable, a protezione diretta e condivisibili che controllano gli attributi dei processi ad essi associati. Le operazioni eseguite su un oggetto processo interessano tutti i processi associati all'oggetto processo. Tra gli esempi sono inclusi i limiti di applicazione, ad esempio working set dimensioni e la priorità del processo o la terminazione di tutti i processi associati a un processo.

-   [Creazione di processi](#creating-jobs)
-   [Gestione dei processi nei processi](#managing-processes-in-jobs)
-   [Limiti e notifiche dei processi](#job-limits-and-notifications)
-   [Contabilità risorse per i processi](#resource-accounting-for-jobs)
-   [Gestione degli oggetti processo](#managing-job-objects)
-   [Gestione di un albero di processi che utilizza oggetti processo](#managing-a-process-tree-that-uses-job-objects)

## <a name="creating-jobs"></a>Creazione di processi

Per creare un oggetto processo, usare la funzione [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) . Quando il processo viene creato, al processo non è associato alcun processo.

Per associare un processo a un processo, usare la funzione [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) . Dopo che un processo è stato associato a un processo, l'associazione non può essere interruppe. Un processo può essere associato a più processi in una gerarchia di processi annidati. Per ulteriori informazioni, vedere [processi annidati](nested-jobs.md).

**Windows 7, Windows server 2008 R2, Windows XP con SP3, Windows server 2008, Windows Vista e Windows server 2003:** Un processo può essere associato a un solo processo. I processi non possono essere annidati. La possibilità di annidare i processi è stata aggiunta in Windows 8 e Windows Server 2012.

È possibile specificare un descrittore di sicurezza per un oggetto processo quando si chiama la funzione [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) . Per ulteriori informazioni, vedere [sicurezza dell'oggetto processo e diritti di accesso](job-object-security-and-access-rights.md).

## <a name="managing-processes-in-jobs"></a>Gestione dei processi nei processi

Dopo che un processo è stato associato a un processo, per impostazione predefinita tutti i processi figlio creati mediante [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) sono associati anche al processo. I processi figlio creati utilizzando [**il \_ processo Win32. Create**](../cimwin32prov/create-method-in-class-win32-process.md) non sono associati al processo. Questo comportamento predefinito può essere modificato impostando il limite dell'oggetto del processo di limite esteso OK \_ \_ o il limite dell' \_ \_ \_ oggetto processo \_ \_ \_ \_ per il processo.

-   Se il processo ha il limite dell'oggetto del processo limite esteso \_ \_ \_ \_ OK e il processo padre è stato creato con il \_ flag di creazione della fuga \_ dal processo, i \_ processi figlio del processo padre non sono associati al processo.
-   Se il processo ha l'oggetto limite esteso \_ \_ , il limite \_ di fuga invisibile al processo è \_ \_ OK, i processi figlio di qualsiasi processo padre associato al processo non sono associati al processo. Non è necessario che i processi padre vengano creati con il flag crea \_ fuga \_ dal \_ processo.

Se il processo è annidato, le impostazioni separati dei processi padre nella gerarchia influiscono sul fatto che i processi figlio siano associati a un altro processo nella gerarchia. Per ulteriori informazioni, vedere [processi annidati](nested-jobs.md).

Per determinare se un processo è in esecuzione in un processo, usare la funzione [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob) .

Per terminare tutti i processi attualmente associati a un oggetto processo, usare la funzione [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) .

## <a name="job-limits-and-notifications"></a>Limiti e notifiche dei processi

Un processo può applicare limiti come la dimensione working set, la priorità di processo e il limite di tempo di fine processo per ogni processo associato al processo. Se un processo associato a un processo tenta di aumentare le dimensioni working set o la priorità di processo rispetto al limite stabilito dal processo, le chiamate di funzione hanno esito positivo, ma vengono ignorate automaticamente. Un processo può anche impostare limiti che attivano una notifica quando vengono superati, ma consentono di continuare l'esecuzione del processo.

Per impostare i limiti per un processo, usare la funzione [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) . Per un elenco dei limiti possibili che è possibile impostare per un processo, vedere gli argomenti seguenti:

-   [**\_ \_ informazioni sul limite di JOBOBJECT Basic \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**\_ \_ restrizioni dell'interfaccia utente di base di JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**\_ \_ \_ informazioni sul controllo della frequenza CPU JOBOBJECT \_**](/windows/desktop/api/Winnt/ns-winnt-jobobject_cpu_rate_control_information)
-   [**\_ \_ informazioni sul limite esteso JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**\_ \_ informazioni sul limite di notifica JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_notification_limit_information)

I limiti di sicurezza devono essere impostati singolarmente per ogni processo associato a un oggetto processo. Per altre informazioni, vedere [sicurezza dei processi e diritti di accesso](process-security-and-access-rights.md).

**Windows XP con SP3 e Windows Server 2003:** La funzione [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) può essere utilizzata per impostare limitazioni di sicurezza per tutti i processi associati a un oggetto processo. A partire da Windows Vista, è necessario impostare i limiti di sicurezza singolarmente per ogni processo associato a un oggetto processo.

Se il processo è annidato, i processi padre nella gerarchia influiscono sul limite applicato per il processo. Per ulteriori informazioni, vedere [processi annidati](nested-jobs.md).

Se il processo dispone di una porta di completamento I/O associata, può ricevere notifiche quando vengono superati determinati limiti di processo. Quando viene superato un limite o se si verificano altri eventi, il sistema invia messaggi alla porta di completamento. Per associare una porta di completamento a un processo, usare la funzione [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con la classe di informazioni dell'oggetto processo **JobObjectAssociateCompletionPortInformation** e un puntatore a una struttura di [**porte di \_ \_ completamento \_ di associazione JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port) . È consigliabile eseguire questa operazione quando il processo è inattivo, in modo da ridurre la possibilità di ricevere notifiche mancanti per i processi i cui Stati cambiano durante l'associazione della porta di completamento.

Tutti i messaggi vengono inviati direttamente dal processo come se il processo avesse chiamato la funzione [**PostQueuedCompletionStatus ha provocato**](/windows/win32/api/ioapiset/nf-ioapiset-postqueuedcompletionstatus) . Un thread deve monitorare la porta di completamento utilizzando la funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) per prelevare i messaggi. Si noti che, con l'eccezione dei limiti impostati con la classe di informazioni **JobObjectNotificationLimitInformation** , il recapito dei messaggi alla porta di completamento non è garantito. l'esito negativo di un messaggio in arrivo non significa necessariamente che l'evento non si è verificato. Viene garantita la ricezione delle notifiche per i limiti impostati con **JobObjectNotificationLimitInformation** alla porta di completamento. Per un elenco dei messaggi possibili, vedere [**la \_ \_ \_ porta di completamento associata JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-jobs"></a>Contabilità risorse per i processi

L'oggetto processo registra le informazioni di contabilità di base per tutti i processi associati, inclusi quelli che sono stati terminati. Per recuperare queste informazioni di contabilità, utilizzare la funzione [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) . Per un elenco delle informazioni di contabilità gestite per un processo, vedere gli argomenti seguenti:

-   [**\_informazioni di \_ contabilità di base di JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**informazioni su JOBOBJECT \_ Basic \_ e \_ io \_ Accounting \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)

Se l'oggetto processo è annidato, le informazioni di contabilità per ogni processo figlio vengono aggregate nel processo padre. Per ulteriori informazioni, vedere [processi annidati](nested-jobs.md).

## <a name="managing-job-objects"></a>Gestione degli oggetti processo

Lo stato di un oggetto processo viene impostato su segnalato quando tutti i relativi processi vengono interrotti perché è stato superato il limite di tempo di fine del processo specificato. Usare [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) o [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) per monitorare l'oggetto processo per questo evento.

Per ottenere un handle per un oggetto processo esistente, utilizzare la funzione [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) e specificare il nome assegnato all'oggetto al momento della creazione. È possibile aprire solo oggetti processo denominati.

Per chiudere un handle di oggetto processo, usare la funzione [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) . Il processo viene eliminato definitivamente quando l'ultimo handle è stato chiuso e tutti i processi associati sono stati terminati. Tuttavia, se per il processo è stato \_ specificato il limite per l'oggetto processo \_ \_ e il \_ flag di chiusura del processo è stato \_ \_ specificato, la chiusura dell'ultimo handle dell'oggetto processo termina tutti i processi associati e quindi Elimina l'oggetto processo stesso. Se per un processo annidato è \_ stato \_ specificato il limite \_ di chiusura dell'oggetto processo nel flag di chiusura del \_ \_ processo, la \_ chiusura dell'ultimo handle dell'oggetto processo termina tutti i processi associati al processo e ai relativi processi figlio nella gerarchia.

## <a name="managing-a-process-tree-that-uses-job-objects"></a>Gestione di un albero di processi che utilizza oggetti processo

A partire da Windows 8 e Windows Server 2012, un'applicazione può utilizzare [processi annidati](nested-jobs.md) per gestire un albero del processo che utilizza più di un oggetto processo. Tuttavia, un'applicazione che deve essere eseguita in Windows 7, Windows Server 2008 R2 o versioni precedenti di Windows che non supportano i processi annidati deve gestire l'albero del processo in altri modi.

Se uno strumento deve gestire un albero del processo che utilizza oggetti processo e non è possibile utilizzare i processi annidati, sia lo strumento che i membri dell'albero del processo devono cooperare. Usare una delle seguenti opzioni:

-   Usare il limite dell'oggetto processo per il limite \_ \_ \_ \_ \_ OK. Se lo strumento utilizza questo limite, non sarà in grado di monitorare un intero albero dei processi. Lo strumento consente di monitorare solo i processi che aggiunge al processo. Se questi processi creano processi figlio, non sono associati al processo. In questa opzione, i processi figlio possono essere associati ad altri oggetti processo.
-   Usare il limite \_ di \_ \_ fughe \_ OK per l'oggetto processo. Se lo strumento utilizza questo limite, può monitorare l'intero albero del processo, ad eccezione dei processi che qualsiasi membro dell'albero interrompe in modo esplicito l'albero. Un membro dell'albero può creare un processo figlio in un nuovo oggetto processo chiamando la funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) con il flag di creazione della \_ fuga \_ dal \_ processo, quindi chiamando la funzione [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) . In caso contrario, il membro deve gestire i casi in cui **AssignProcessToJobObject** ha esito negativo.

    Il \_ flag crea fuga \_ dal processo non \_ produce alcun effetto se l'albero non viene monitorato dallo strumento. Pertanto, si tratta dell'opzione preferita, ma è necessario conoscere in anticipo i processi monitorati.

-   Evitare le fughe di qualsiasi tipo impostando il limite dell'oggetto del processo dispari \_ \_ \_ \_ OK o l'oggetto processo limite di assenza invisibile al limite \_ \_ \_ \_ \_ OK. In questa opzione, lo strumento è in grado di monitorare l'intero albero dei processi. Tuttavia, se un processo figlio tenta di associarsi a se stesso o a un altro processo figlio con un processo chiamando [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject), la chiamata avrà esito negativo. Se il processo è stato progettato per essere associato a un processo specifico, questo errore potrebbe impedire il corretto funzionamento del processo.

 

 
