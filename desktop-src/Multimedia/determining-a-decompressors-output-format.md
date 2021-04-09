---
title: Determinazione del formato di output di un decompressore
description: Determinazione del formato di output di un decompressore
ms.assetid: afedef5e-a506-40bd-aaad-fd85b0468ed7
keywords:
- Gestione compressione video (VCM), formato di output
- VCM (Video Compression Manager), formato di output
- ICDecompressGetFormatSize (macro)
- ICDecompressQuery (macro)
- ICDecompressGetPalette (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb4140a4118cb2a36ccd75088556c53c55fdcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117683"
---
# <a name="determining-a-decompressors-output-format"></a><span data-ttu-id="f8234-108">Determinazione del formato di output di un decompressore</span><span class="sxs-lookup"><span data-stu-id="f8234-108">Determining a Decompressor's Output Format</span></span>

<span data-ttu-id="f8234-109">Nell'esempio seguente vengono determinate le dimensioni del buffer necessarie per i dati che specificano il formato di decompressione utilizzando la macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) , viene allocato un buffer delle dimensioni appropriate utilizzando la funzione [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) e vengono recuperate le informazioni sul formato di decompressione utilizzando la macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .</span><span class="sxs-lookup"><span data-stu-id="f8234-109">The following example determines the buffer size needed for the data specifying the decompression format using the [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) macro, allocates a buffer of the appropriate size using the [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) function, and retrieves the decompression format information using the [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) macro.</span></span>


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



<span data-ttu-id="f8234-110">Nell'esempio seguente viene illustrato come un'applicazione può utilizzare la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) per determinare se un decompressore è in grado di gestire i formati di input e di output.</span><span class="sxs-lookup"><span data-stu-id="f8234-110">The following example shows how an application can use the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro to determine if a decompressor can handle the input and output formats.</span></span>


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



<span data-ttu-id="f8234-111">Nel frammento di codice seguente viene illustrato come ottenere le informazioni sulla tavolozza utilizzando la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="f8234-111">The following code fragment shows how to get the palette information using the [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) macro.</span></span>


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 