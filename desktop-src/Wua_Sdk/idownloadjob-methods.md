---
description: L'interfaccia IDownloadJob definisce i metodi seguenti.
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: Metodi IDownloadJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f68acd6d7fef37c4ce9309c559a1de1b4d516dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526701"
---
# <a name="idownloadjob-methods"></a>Metodi IDownloadJob

L'interfaccia [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) definisce i metodi seguenti.



| Metodo                                            | Descrizione                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Pulizia**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | Attende il completamento di un'operazione asincrona e rilascia tutti i callback.                                        |
| [**GetProgress**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | Restituisce un'interfaccia [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) che descrive lo stato di avanzamento corrente di un download. |
| [**RequestAbort**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | Esegue una richiesta per terminare un download asincrono.                                                                       |



 

 

 



