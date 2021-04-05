---
description: Le notifiche seguenti vengono utilizzate con le funzioni SetupInstallFile, SetupInstallFileEx e SetupInstallFromInfSection. Per ulteriori informazioni sul formato e sull'utilizzo delle notifiche, vedere notifiche.
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: Notifiche file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f58863d48c1af809c0cbbcdc2d625214a6e90a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967611"
---
# <a name="inf-file-notifications"></a>Notifiche file INF

Le notifiche seguenti vengono utilizzate con le funzioni [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)e [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) . Per ulteriori informazioni sul formato e sull'utilizzo delle notifiche, vedere [notifiche](notifications.md).



| Notifica                                                      | Descrizione                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_FILEOPDELAYED SPFILENOTIFY**](spfilenotify-fileopdelayed.md) | Il file è in uso e l'operazione corrente viene posticipata fino al riavvio del sistema. |
| [**\_LANGMISMATCH SPFILENOTIFY**](spfilenotify-langmismatch.md)   | La lingua del file corrente non corrisponde alla lingua del sistema.                   |
| [**\_TARGETEXISTS SPFILENOTIFY**](spfilenotify-targetexists.md)   | Una copia del file specificato esiste già nella destinazione.                             |
| [**\_TARGETNEWER SPFILENOTIFY**](spfilenotify-targetnewer.md)     | Nella destinazione è presente una versione più recente del file specificato.                            |



 

> [!Note]  
> Poiché [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) crea ed Esegui il commit di una coda di file interna, USA anche le [notifiche della coda di file](file-queue-notifications.md).

 

 

 



