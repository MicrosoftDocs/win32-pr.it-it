---
description: L'interfaccia IUpdateDownloader definisce le proprietà seguenti.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Proprietà di IUpdateDownloader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c16aa762bcc14dc1919ef91d162752652c327e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752082"
---
# <a name="iupdatedownloader-properties"></a>Proprietà di IUpdateDownloader

L'interfaccia [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) definisce le proprietà seguenti.



| Proprietà                                                             | Descrizione                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | Ottiene e imposta l'applicazione client corrente.                                                                                                                              |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | Ottiene e imposta un valore booleano che indica se l'agente di Windows Update (WUA) forza il download degli aggiornamenti già installati o che non possono essere installati. |
| [**Priority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | Ottiene e imposta il livello di priorità del download.                                                                                                                          |
| [**Aggiornamenti**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | Ottiene e imposta un'interfaccia che contiene una raccolta di sola lettura degli aggiornamenti specificati per il download.                                                            |



 

 

 



