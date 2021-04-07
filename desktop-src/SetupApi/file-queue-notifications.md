---
description: Le notifiche seguenti vengono utilizzate con le code di file. Per ulteriori informazioni sul formato e sull'utilizzo delle notifiche, vedere notifiche.
ms.assetid: 4a171b4a-8623-4be3-81ee-99081fe23034
title: Notifiche della coda di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b674dee015c4c9408ff5dc853d5d3b2412e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057868"
---
# <a name="file-queue-notifications"></a>Notifiche della coda di file

Le notifiche seguenti vengono utilizzate con le code di file. Per ulteriori informazioni sul formato e sull'utilizzo delle notifiche, vedere [notifiche](notifications.md).



| Notifica                                                      | Descrizione                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**\_COPYERROR SPFILENOTIFY**](spfilenotify-copyerror.md)         | Si è verificato un errore durante un'operazione di copia del file.                                                  |
| [**\_DELETEERROR SPFILENOTIFY**](spfilenotify-deleteerror.md)     | Si è verificato un errore durante un'operazione di eliminazione del file.                                                 |
| [**\_ENDCOPY SPFILENOTIFY**](spfilenotify-endcopy.md)             | Operazione di copia file terminata.                                                                 |
| [**\_ENDDELETE SPFILENOTIFY**](spfilenotify-enddelete.md)         | Operazione di eliminazione file terminata.                                                                |
| [**\_ENDQUEUE SPFILENOTIFY**](spfilenotify-endqueue.md)           | Commit della coda completato.                                                                  |
| [**\_ENDRENAME SPFILENOTIFY**](spfilenotify-endrename.md)         | Operazione di ridenominazione file terminata.                                                                  |
| [**\_ENDSUBQUEUE SPFILENOTIFY**](spfilenotify-endsubqueue.md)     | Una coda secondaria (copia, Rinomina o Elimina) è terminata.                                               |
| [**\_FILEOPDELAYED SPFILENOTIFY**](spfilenotify-fileopdelayed.md) | Il file è in uso e l'operazione corrente è stata posticipata fino al riavvio del sistema.       |
| [**\_LANGMISMATCH SPFILENOTIFY**](spfilenotify-langmismatch.md)   | La lingua dell'operazione corrente non corrisponde alla lingua di sistema.                           |
| [**\_NEEDMEDIA SPFILENOTIFY**](spfilenotify-needmedia.md)         | È necessario un nuovo supporto di origine.                                                                         |
| [**\_QUEUESCAN SPFILENOTIFY**](spfilenotify-queuescan.md)         | Un nodo nella coda di file è stato analizzato. (Solo [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) ) |
| [**\_RENAMEERROR SPFILENOTIFY**](spfilenotify-renameerror.md)     | Si è verificato un errore durante un'operazione di ridenominazione dei file.                                                 |
| [**\_STARTCOPY SPFILENOTIFY**](spfilenotify-startcopy.md)         | Un'operazione di copia file è stata avviata.                                                                  |
| [**\_STARTDELETE SPFILENOTIFY**](spfilenotify-startdelete.md)     | È stata avviata un'operazione di eliminazione di file.                                                                |
| [**\_STARTQUEUE SPFILENOTIFY**](spfilenotify-startqueue.md)       | Il commit della coda è stato avviato.                                                                    |
| [**\_STARTRENAME SPFILENOTIFY**](spfilenotify-startrename.md)     | È stata avviata un'operazione di ridenominazione del file.                                                                |
| [**\_STARTSUBQUEUE SPFILENOTIFY**](spfilenotify-startsubqueue.md) | È stata avviata una coda secondaria (copia, Rinomina o Elimina).                                             |
| [**\_TARGETEXISTS SPFILENOTIFY**](spfilenotify-targetexists.md)   | Una copia del file specificato esiste già nella destinazione.                                          |
| [**\_TARGETNEWER SPFILENOTIFY**](spfilenotify-targetnewer.md)     | Nella destinazione è presente una versione più recente del file specificato.                                         |



 

 

 



