---
description: L'interfaccia IInstallationJob definisce i metodi seguenti.
ms.assetid: 4990ef7c-b6cd-46fc-9e7d-8d1d78edc9f2
title: Metodi IInstallationJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0c1a5850f3d71ad1a6a51046fe890ea9bc7426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129651"
---
# <a name="iinstallationjob-methods"></a>Metodi IInstallationJob

L'interfaccia [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) definisce i metodi seguenti.



| Metodo                                                | Descrizione                                                                                                                                           |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pulizia**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)           | Attende il completamento di un'operazione asincrona, quindi rilascia tutti i callback.                                                              |
| [**GetProgress**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-getprogress)   | Restituisce un'interfaccia [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) che descrive lo stato di avanzamento corrente di un'installazione o di una disinstallazione. |
| [**RequestAbort**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-requestabort) | Esegue una richiesta per annullare l'installazione o la disinstallazione.                                                                                         |



 

 

 



