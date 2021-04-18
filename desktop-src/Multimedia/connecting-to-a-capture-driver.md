---
title: Connessione a un driver di acquisizione
description: Connessione a un driver di acquisizione
ms.assetid: ce83329f-de5a-4428-bc0d-be5f3d35ff1a
keywords:
- capDriverDisconnect (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2161279f5b8b8dc528ee548d0a6a8ad6e9b397f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298135"
---
# <a name="connecting-to-a-capture-driver"></a><span data-ttu-id="d9760-104">Connessione a un driver di acquisizione</span><span class="sxs-lookup"><span data-stu-id="d9760-104">Connecting to a Capture Driver</span></span>

<span data-ttu-id="d9760-105">Nell'esempio seguente viene connessa la finestra di acquisizione con l'handle *hWndC* al driver msvideo e quindi le si disconnette utilizzando la macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) :</span><span class="sxs-lookup"><span data-stu-id="d9760-105">The following example connects the capture window with the handle *hWndC* to the MSVIDEO driver and then disconnects them using the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d9760-106">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9760-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9760-107">Uso di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d9760-107">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




