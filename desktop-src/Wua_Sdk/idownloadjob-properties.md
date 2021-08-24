---
description: L'interfaccia IDownloadJob definisce le proprietà seguenti.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Proprietà di IDownloadJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cdd4f95a14df215017f9fd628497d15c6c7410e4a82cbfb53c076b2112899b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049339"
---
# <a name="idownloadjob-properties"></a>Proprietà di IDownloadJob

[**L'interfaccia IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) definisce le proprietà seguenti.



| Proprietà                                        | Descrizione                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Asyncstate**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | Ottiene l'oggetto stato specifico del chiamante passato al metodo [**IUpdateDownloader.BeginDownload.**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload)           |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | Ottiene l'impostazione che indica se la chiamata a [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) è stata elaborata completamente. |
| [**Aggiornamenti**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | Ottiene un'interfaccia che contiene una raccolta di sola lettura degli aggiornamenti specificati in un download.                                                  |



 

 

 



