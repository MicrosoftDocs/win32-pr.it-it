---
description: Interfacce utilizzate con le quote disco.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Interfacce di quota disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485621"
---
# <a name="disk-quota-interfaces"></a>Interfacce di quota disco

Con le quote disco vengono utilizzate le interfacce seguenti.



| Interfaccia                                          | Descrizione                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | Controlla le funzionalità di quota del disco di un singolo volume di file system NTFS.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | Riceve le notifiche degli eventi relative alla quota.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | Rappresenta una singola voce della quota utente nel file di informazioni sulla quota del volume.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | Aggiunge più oggetti utente della quota a un contenitore che viene quindi inviato per l'aggiornamento in una singola chiamata.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | Enumera le voci della quota utente nel volume.<br/>                                                        |



 

 

