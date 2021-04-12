---
title: Preparazione per l'estrazione dei dati
description: Preparazione per l'estrazione dei dati
ms.assetid: 98adcee4-06c0-4684-bd9e-e030e3f9a59d
keywords:
- Gestione compressione video (VCM), disegno
- VCM (Video Compression Manager), disegno
- ICDrawBegin (macro)
- ICDrawEnd (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de20d23c0ded51d1933918c16da3f8827b77f796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221358"
---
# <a name="preparing-to-draw-data"></a><span data-ttu-id="b5ac4-107">Preparazione per l'estrazione dei dati</span><span class="sxs-lookup"><span data-stu-id="b5ac4-107">Preparing to Draw Data</span></span>

<span data-ttu-id="b5ac4-108">Nell'esempio seguente viene illustrata la sequenza di inizializzazione che indica al decompressore di estrarre a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="b5ac4-108">The following example shows the initialization sequence that instructs the decompressor to draw full-screen.</span></span> <span data-ttu-id="b5ac4-109">Usa le macro [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) e [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .</span><span class="sxs-lookup"><span data-stu-id="b5ac4-109">It uses the [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) and [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) macros.</span></span>


```C++
// Assume lpbiIn has the input format, dwRate has the data rate. 

if (ICDrawBegin(hIC, ICDRAW_QUERY | ICDRAW_FULLSCREEN, NULL, NULL, 
    NULL, 0, 0, 0, 0, lpbiIn, 0, 0, 0, 0, dwRate, 
    dwScale) == ICERR_OK) 
{ 
    // Decompressor supports this drawing so set up to draw. 
    ICDrawBegin(hIC, ICDRAW_FULLSCREEN, hPal, NULL, NULL, 0, 0, 0, 
        0, lpbiIn, 0, 0, lbpi->biWidth, lpbi->biHeight, dwRate, 
        dwScale); 
    . 
    . // Start decompressing and drawing frames. 
    . 
 
    // Drawing done. Terminate procedure. 
    ICDrawEnd(hIC); 
} 
else 
{ 
    
    // Use another renderer to draw data on the screen; 
    // ICDraw does not support the format. 
} 
 
```



 

 




