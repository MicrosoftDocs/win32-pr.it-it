---
title: Determinazione del formato di output di un compressore
description: Determinazione del formato di output di un compressore
ms.assetid: 910bd77f-4c65-4ea2-bab2-96f42a2b6cf1
keywords:
- Gestione compressione video (VCM), formato di output
- VCM (Video Compression Manager), formato di output
- ICCompressGetFormat (macro)
- ICCompressQuery (macro)
- ICCompressGetSize (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4356870598dc08ad84c4073be5ffa3c2ddbd5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117742"
---
# <a name="determining-a-compressors-output-format"></a><span data-ttu-id="df008-108">Determinazione del formato di output di un compressore</span><span class="sxs-lookup"><span data-stu-id="df008-108">Determining a Compressor's Output Format</span></span>

<span data-ttu-id="df008-109">Nell'esempio seguente viene utilizzata la macro di dimensioni [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) per determinare le dimensioni del buffer necessarie per i dati che specificano il formato di compressione, alloca un buffer delle dimensioni appropriate utilizzando la funzione [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) e recupera le informazioni sul formato di compressione utilizzando la macro **ICCompressGetFormat** .</span><span class="sxs-lookup"><span data-stu-id="df008-109">The following example uses the [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) size macro to determine the buffer size needed for the data specifying the compression format, allocates a buffer of the appropriate size using the [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) function, and retrieves the compression format information using the **ICCompressGetFormat** macro.</span></span>


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// *lpbiIn must be initialized to the input format. 
 
dwFormatSize = ICCompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICCompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



<span data-ttu-id="df008-110">Nell'esempio seguente viene usata la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) per determinare se un compressore può gestire i formati di input e di output.</span><span class="sxs-lookup"><span data-stu-id="df008-110">The following example uses the [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) macro to determine whether a compressor can handle the input and output formats.</span></span>


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// Both *lpbiIn and *lpbiOut must be initialized to the respective
// formats.
 

if (ICCompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
 
    // Format is supported; use the compressor. 
 
}
 
 
```



<span data-ttu-id="df008-111">Nell'esempio seguente viene utilizzata la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) per determinare le dimensioni del buffer e viene allocato un buffer di tale dimensione utilizzando [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc).</span><span class="sxs-lookup"><span data-stu-id="df008-111">The following example uses the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro to determine the buffer size, and it allocates a buffer of that size using [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc).</span></span>


```C++
// Find the worst-case buffer size. 
dwCompressBufferSize = ICCompressGetSize(hIC, lpbiIn, lpbiOut); 
 
// Allocate a buffer and get lpOutput to point to it. 
h = GlobalAlloc(GHND, dwCompressBufferSize); 
lpOutput = (LPVOID)GlobalLock(h);
 
 
```



 

 