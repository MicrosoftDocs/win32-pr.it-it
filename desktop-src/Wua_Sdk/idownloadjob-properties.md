---
description: L'interfaccia IDownloadJob definisce le proprietà seguenti.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Proprietà di IDownloadJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307656"
---
# <a name="idownloadjob-properties"></a>Proprietà di IDownloadJob

L'interfaccia [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) definisce le proprietà seguenti.



| Proprietà                                        | Descrizione                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | Ottiene l'oggetto di stato specifico del chiamante passato al metodo [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) .           |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | Ottiene l'impostazione che indica se la chiamata a [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) è stata elaborata completamente. |
| [**Aggiornamenti**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | Ottiene un'interfaccia che contiene una raccolta di sola lettura degli aggiornamenti specificati in un download.                                                  |



 

 

 



