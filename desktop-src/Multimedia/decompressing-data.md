---
title: Decompressione dei dati
description: Decompressione dei dati
ms.assetid: 1faf0238-7bef-4363-9bbc-44737600c946
keywords:
- Gestione compressione video (VCM), decompressione dei dati
- VCM (Gestione compressione video), decompressione dei dati
- ICDecompressBegin (macro)
- ICDecompress (funzione)
- ICDecompressEnd (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b44ea375bb1f2b5c41a361ca7f31387439b610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710804"
---
# <a name="decompressing-data"></a><span data-ttu-id="ce1c1-108">Decompressione dei dati</span><span class="sxs-lookup"><span data-stu-id="ce1c1-108">Decompressing Data</span></span>

<span data-ttu-id="ce1c1-109">Nell'esempio seguente viene illustrato come un'applicazione può inizializzare un decompressore utilizzando la macro [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) , decomprimere una sequenza di frame utilizzando la funzione [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) e terminare la decompressione utilizzando la macro [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .</span><span class="sxs-lookup"><span data-stu-id="ce1c1-109">The following example shows how an application can initialize a decompressor using the [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) macro, decompress a frame sequence using the [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) function, and terminate decompression using the [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) macro.</span></span>


```C++
LPBITMAPINFOHEADER lbpiIn, lpbiOut; 
LPVOID             lpIn, lpOut; 
LONG               lNumFrames, lFrameNum; 
 
// Assume lpbiIn and lpbiOut are initialized to the input and output 
// format and lpIn and lpOut are pointing to the buffers. 
if (ICDecompressBegin(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    for (lFrameNum = 0; lFrameNum < lNumFrames, lFrameNum++)
    { 
        if (ICDecompress(hIC, 0, lpbiIn, lpIn, lpbiOut, 
            lpOut) == ICERR_OK) 
        { 
            // Frame decompressed OK so we can process it as required. 
        } 
        else 
        { 
            // Handle the decompression error that occurred. 
        } 
    } 
    ICDecompressEnd(hIC); 
} 
else 
{ 
    // Handle the error identifying an unsupported format. 
} 
 
```



 

 




