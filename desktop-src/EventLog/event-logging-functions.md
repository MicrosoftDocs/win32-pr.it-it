---
description: Le funzioni seguenti vengono usate con la registrazione degli eventi.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Funzioni di registrazione eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6ba5e43286a65b9d3456edc9cd80e8812bd9a32975ec63158c0717b41c6894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069591"
---
# <a name="event-logging-functions"></a>Funzioni di registrazione eventi

Le funzioni seguenti vengono usate con la registrazione degli eventi.



| Funzione                                                         | Descrizione                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | Salva il log eventi specificato in un file di backup.                                                     |
| [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | Cancella il registro eventi specificato e, facoltativamente, salva la copia corrente del log in un file di backup.  |
| [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | Chiude un handle di lettura nel log eventi specificato.                                                    |
| [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | Chiude un handle di scrittura nel log eventi specificato.                                                   |
| [**GetEventLogInformation**](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | Recupera informazioni sul log eventi specificato.                                                |
| [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | Recupera il numero di record nel log eventi specificato.                                         |
| [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | Recupera il numero di record assoluto del record meno recente nel registro eventi specificato.               |
| [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | Consente a un'applicazione di ricevere una notifica quando un evento viene scritto nel registro eventi specificato. |
| [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | Apre un handle per un log eventi di backup.                                                               |
| [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | Apre un handle per il log eventi specificato.                                                          |
| [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | Legge un numero intero di voci dal registro eventi specificato.                                       |
| [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | Recupera un handle registrato per il log eventi specificato.                                           |
| [**Reportevent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | Scrive una voce alla fine del log eventi specificato.                                              |



 

 

 



