---
title: Determinazione del formato di output di un decompressore
description: Determinazione del formato di output di un decompressore
ms.assetid: afedef5e-a506-40bd-aaad-fd85b0468ed7
keywords:
- gestione compressione video(VCM), formato di output
- VCM (Gestione compressione video),formato di output
- Macro ICDecompressGetFormatSize
- Macro ICDecompressQuery
- Macro ICDecompressGetPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc17db0d7aa015c955825840fb70d12714be3c0a44a69bf5abc59290ebc633c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497421"
---
# <a name="determining-a-decompressors-output-format"></a>Determinazione del formato di output di un decompressore

L'esempio seguente determina le dimensioni del buffer necessarie per i dati che specificano il formato di decompressione usando la macro [**ICDecompressGetFormatSize,**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) alloca un buffer delle dimensioni appropriate usando la funzione [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) e recupera le informazioni sul formato di decompressione usando la macro [**ICDecompressGetFormat.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat)


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



L'esempio seguente illustra come un'applicazione può usare la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) per determinare se un decompressore può gestire i formati di input e output.


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



Il frammento di codice seguente illustra come ottenere le informazioni sulla tavolozza usando la macro [**ICDecompressGetPalette.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette)


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 