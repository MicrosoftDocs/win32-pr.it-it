---
description: L'interfaccia IUpdateDownloader definisce le proprietà seguenti.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Proprietà di IUpdateDownloader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf66fbdad678ef6a78d0fa049ecb59c34be2ca9d08c873e24e82c35c9d1eb1c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738290"
---
# <a name="iupdatedownloader-properties"></a>Proprietà di IUpdateDownloader

[**L'interfaccia IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) definisce le proprietà seguenti.



| Proprietà                                                             | Descrizione                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | Ottiene e imposta l'applicazione client corrente.                                                                                                                              |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | Ottiene e imposta un valore booleano che indica se l'agente di aggiornamento di Windows (WUA) forza il download degli aggiornamenti già installati o che non possono essere installati. |
| [**Priority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | Ottiene e imposta il livello di priorità del download.                                                                                                                          |
| [**Aggiornamenti**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | Ottiene e imposta un'interfaccia che contiene una raccolta di sola lettura degli aggiornamenti specificati per il download.                                                            |



 

 

 



