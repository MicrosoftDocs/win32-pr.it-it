---
title: Installazione di commediatori e decompressori
description: Installazione di commediatori e decompressori
ms.assetid: 8bcca000-c4c7-47e7-a4c0-5d0d1750176f
keywords:
- Gestione compressione video (VCM), installazione di compressatori
- VCM (Video Compression Manager), installazione dei commediatori
- ICInstall (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8c3421b3d7f59e7f6b16150fcd0d641deaef17
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329276"
---
# <a name="installing-compressors-and-decompressors"></a><span data-ttu-id="aba49-106">Installazione di commediatori e decompressori</span><span class="sxs-lookup"><span data-stu-id="aba49-106">Installing Compressors and Decompressors</span></span>

<span data-ttu-id="aba49-107">Nell'esempio seguente viene illustrato come un'applicazione può installare una funzione come compressore o decompressore usando la funzione [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) .</span><span class="sxs-lookup"><span data-stu-id="aba49-107">The following example shows how an application can install a function as a compressor or decompressor using the [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) function.</span></span>


```C++
// This function looks like a DriverProc entry point. 

LRESULT MyCodecFunction(DWORD dwID, HDRVR hDriver, 
    UINT uiMessage, LPARAM lParam1, LPARAM lParam2); 
 
// This function installs the MyCodecFunction as a compressor. 

result = ICInstall ( ICTYPE_VIDEO, mmioFOURCC('s','a','m','p'), 
    (LPARAM)(FARPROC)&MyCodecFunction, NULL, ICINSTALL_FUNCTION); 
 
```



 

 




