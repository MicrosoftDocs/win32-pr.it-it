---
description: Interfacce utilizzate in Gestione disco.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Interfacce di gestione disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233160"
---
# <a name="disk-management-interfaces"></a>Interfacce di gestione disco

Le interfacce seguenti vengono utilizzate in Gestione disco.

## <a name="in-this-section"></a>Contenuto della sezione



| Interfaccia                                                     | Descrizione                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | Controlla le funzionalità di quota del disco di un singolo volume di file system NTFS.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | Riceve le notifiche degli eventi relative alla quota.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | Rappresenta una singola voce della quota utente nel file di informazioni sulla quota del volume.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | Aggiunge più oggetti utente della quota a un contenitore che viene quindi inviato per l'aggiornamento in una singola chiamata.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | Enumera le voci della quota utente nel volume.<br/>                                                        |



 

 

