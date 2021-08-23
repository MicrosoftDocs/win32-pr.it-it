---
title: Connessione a un driver di acquisizione
description: Connessione a un driver di acquisizione
ms.assetid: ce83329f-de5a-4428-bc0d-be5f3d35ff1a
keywords:
- Macro capDriverDisconnect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34e606c439143400f1ea1845db37e7faf93009350254c173c4003400c3996f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144864"
---
# <a name="connecting-to-a-capture-driver"></a>Connessione a un driver di acquisizione

L'esempio seguente connette la finestra di acquisizione con l'handle *hWndC* al driver MSVIDEO e quindi le disconnette usando la macro [**capDriverDisconnect:**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect)


```C++
fOK = SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0, 0L); 
// 
// Or, use the macro to connect to the MSVIDEO driver: 
// fOK = capDriverConnect(hWndC, 0); 
// 
// Place code to set up and capture video here. 
// 
capDriverDisconnect (hWndC); 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




