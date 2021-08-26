---
description: Le funzioni OpenEventLog, OpenBackupEventLog, RegisterEventSource, DeregisterEventSource e CloseEventLog aprono e chiudono gli handle del registro eventi.
ms.assetid: e42a66c2-2f1e-46f8-99c7-4701075c8ec3
title: Operazioni di registrazione eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221218bdfa4fc5e4fc6a905353cde33357c4088119031062c074c75d4b8136dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901421"
---
# <a name="event-logging-operations"></a>Operazioni di registrazione eventi

Le [**funzioni OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga), [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga), [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea), [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)e [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog) aprono e chiudono gli handle del registro eventi.

Nella tabella seguente vengono illustrate le operazioni che è possibile eseguire in un log eventi aperto e la funzione corrispondente per ogni operazione.



| Operazione | Funzione                                                                                                                     |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| Backup    | [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                                                                                     |
| Cancella     | [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                                                                                       |
| Monitoraggio   | [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)                                                                         |
| Query     | [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord), [ **GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) |
| Read      | [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                                                                                         |
| Scrittura     | [**Reportevent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                                                                                           |



 

Le [**funzioni OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) [**e ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) accettano un nome di server facoltativo come parametro in modo che le operazioni possano essere eseguite nel server remoto. Usare [**OpenEventLog per**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) leggere o eseguire operazioni amministrative (backup, cancellazione, monitoraggio e query) nel log e [**Usare RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) per la scrittura nel log.

Ogni chiamata a una funzione di registrazione degli eventi è un'operazione atomica. Quando si legge dal registro eventi, vengono restituiti solo record di eventi interi. Quando si scrive nel registro eventi, ogni record di evento viene scritto in sequenza come record completo nel log. Nell'elenco seguente viene descritto il modo in cui il servizio di registrazione eventi gestisce condizioni speciali:

-   Il servizio di registrazione eventi riceve un'operazione di lettura e un'operazione di scrittura contemporaneamente: se la posizione di lettura si trova alla fine del file, l'operazione di lettura ha esito negativo con lo stato "fine del file" (se l'operazione di scrittura non è stata completata) o restituisce il nuovo record (se l'operazione di scrittura è stata completata).
-   Il servizio di registrazione eventi completa un'operazione di cancellazione prima di ricevere un'operazione di lettura: l'operazione di lettura non riesce con stato "fine del file".
-   Il servizio di registrazione eventi completa un'operazione di cancellazione prima di ricevere un'operazione di scrittura: l'operazione di cancellazione tronca il log, quindi l'operazione di scrittura aggiunge il nuovo record all'inizio del log.

 

 



