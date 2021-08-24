---
description: Interfacce usate nella gestione del disco.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Interfacce di gestione del disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a7314de976b1a5228a8b537da5d09be3df66936ed57915d86d78b0a84c4361e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823211"
---
# <a name="disk-management-interfaces"></a>Interfacce di gestione del disco

Nella gestione del disco vengono usate le interfacce seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Interfaccia                                                     | Descrizione                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | Controlla le funzionalità di quota disco di un singolo volume file system NTFS.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | Riceve le notifiche degli eventi correlati alla quota.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | Rappresenta una singola voce di quota utente nel file di informazioni sulla quota del volume.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | Aggiunge più oggetti utente di quota a un contenitore che viene quindi inviato per l'aggiornamento in una singola chiamata.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | Enumera le voci di quota utente nel volume.<br/>                                                        |



 

 

