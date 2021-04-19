---
description: Le funzioni seguenti vengono utilizzate con la registrazione degli eventi.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Funzioni di registrazione eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437899684861c5fc7ddbfe98c2499dc07bd9da8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310820"
---
# <a name="event-logging-functions"></a>Funzioni di registrazione eventi

Le funzioni seguenti vengono utilizzate con la registrazione degli eventi.



| Funzione                                                         | Descrizione                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | Salva il registro eventi specificato in un file di backup.                                                     |
| [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | Cancella il registro eventi specificato e, facoltativamente, salva la copia corrente del log in un file di backup.  |
| [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | Chiude un handle di lettura al log eventi specificato.                                                    |
| [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | Chiude un handle di scrittura nel log eventi specificato.                                                   |
| [**GetEventLogInformation**](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | Recupera le informazioni sul log eventi specificato.                                                |
| [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | Recupera il numero di record nel registro eventi specificato.                                         |
| [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | Recupera il numero di record assoluto del record meno recente nel registro eventi specificato.               |
| [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | Consente a un'applicazione di ricevere una notifica quando un evento viene scritto nel registro eventi specificato. |
| [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | Apre un handle per un log eventi di backup.                                                               |
| [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | Apre un handle per il registro eventi specificato.                                                          |
| [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | Legge un numero intero di voci dal log eventi specificato.                                       |
| [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | Recupera un handle registrato nel registro eventi specificato.                                           |
| [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | Scrive una voce alla fine del log eventi specificato.                                              |



 

 

 



