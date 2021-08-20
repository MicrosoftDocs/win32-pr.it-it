---
title: Determinazione del formato di output di un oggetto
description: Determinazione del formato di output di un oggetto
ms.assetid: 910bd77f-4c65-4ea2-bab2-96f42a2b6cf1
keywords:
- gestione compressione video(VCM), formato di output
- VCM (Gestione compressione video),formato di output
- Macro ICCompressGetFormat
- Macro ICCompressQuery
- Macro ICCompressGetSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4160942c2b5524e57a3a7d7e4eb79128abd55bf5f62ea0926c1ba60e02ce70c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989001"
---
# <a name="determining-a-compressors-output-format"></a>Determinazione del formato di output di un oggetto

L'esempio seguente usa la macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) size per determinare le dimensioni del buffer necessarie per i dati che specificano il formato di compressione, alloca un buffer delle dimensioni appropriate usando la funzione [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) e recupera le informazioni sul formato di compressione usando la macro **ICCompressGetFormat.**


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// *lpbiIn must be initialized to the input format. 
 
dwFormatSize = ICCompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICCompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



Nell'esempio seguente viene utilizzata la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) per determinare se un oggetto è in grado di gestire i formati di input e output.


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// Both *lpbiIn and *lpbiOut must be initialized to the respective
// formats.
 

if (ICCompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
 
    // Format is supported; use the compressor. 
 
}
 
 
```



L'esempio seguente usa la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) per determinare le dimensioni del buffer e alloca un buffer di tale dimensione usando [GlobalAlloc.](/windows/win32/api/winbase/nf-winbase-globalalloc)


```C++
// Find the worst-case buffer size. 
dwCompressBufferSize = ICCompressGetSize(hIC, lpbiIn, lpbiOut); 
 
// Allocate a buffer and get lpOutput to point to it. 
h = GlobalAlloc(GHND, dwCompressBufferSize); 
lpOutput = (LPVOID)GlobalLock(h);
 
 
```



 

 