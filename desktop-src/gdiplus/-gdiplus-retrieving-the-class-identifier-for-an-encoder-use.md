---
description: La funzione GetEncoderClsid nell'esempio seguente riceve il tipo MIME di un codificatore e restituisce l'identificatore di classe (CLSID) del codificatore.
ms.assetid: f78dac7c-4bc1-4614-8a26-d99d5619399a
title: Recupero dell'identificatore di classe per un codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a40c31c7ad997ed3e7525ff247019f6a41c681b9523dc523105bd5ba6c7ca6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014711"
---
# <a name="retrieving-the-class-identifier-for-an-encoder"></a>Recupero dell'identificatore di classe per un codificatore

La funzione GetEncoderClsid nell'esempio seguente riceve il tipo MIME di un codificatore e restituisce l'identificatore di classe (**CLSID**) del codificatore. I tipi MIME dei codificatori incorporati in Windows GDI+ sono i seguenti:

-   image/bmp
-   image/jpeg
-   image/gif
-   image/tiff
-   image/png

La funzione chiama [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) per ottenere una matrice [**di oggetti ImageCodecInfo.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) Se uno degli oggetti **ImageCodecInfo** nella matrice rappresenta il codificatore richiesto, la funzione restituisce l'indice **dell'oggetto ImageCodecInfo** e copia il **CLSID** nella variabile a cui punta **pClsid**. Se la funzione ha esito negativo, restituisce -1.


```
int GetEncoderClsid(const WCHAR* format, CLSID* pClsid)
{
   UINT  num = 0;          // number of image encoders
   UINT  size = 0;         // size of the image encoder array in bytes

   ImageCodecInfo* pImageCodecInfo = NULL;

   GetImageEncodersSize(&num, &size);
   if(size == 0)
      return -1;  // Failure

   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));
   if(pImageCodecInfo == NULL)
      return -1;  // Failure

   GetImageEncoders(num, size, pImageCodecInfo);

   for(UINT j = 0; j < num; ++j)
   {
      if( wcscmp(pImageCodecInfo[j].MimeType, format) == 0 )
      {
         *pClsid = pImageCodecInfo[j].Clsid;
         free(pImageCodecInfo);
         return j;  // Success
      }    
   }

   free(pImageCodecInfo);
   return -1;  // Failure
}
```



L'applicazione console seguente chiama la funzione GetEncoderClsid per determinare il **CLSID** del codificatore PNG:


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

#include "GdiplusHelperFunctions.h"

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID  encoderClsid;
   INT    result;
   WCHAR  strGuid[39];

   result = GetEncoderClsid(L"image/png", &encoderClsid);

   if(result < 0)
   {
      printf("The PNG encoder is not installed.\n");
   }
   else
   {
      StringFromGUID2(encoderClsid, strGuid, 39);
      printf("An ImageCodecInfo object representing the PNG encoder\n");
      printf("was found at position %d in the array.\n", result);
      wprintf(L"The CLSID of the PNG encoder is %s.\n", strGuid);
   }

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Quando si esegue l'applicazione console precedente, si ottiene un output simile al seguente:


```
An ImageCodecInfo object representing the PNG encoder
was found at position 4 in the array.
The CLSID of the PNG encoder is {557CF406-1A04-11D3-9A73-0000F81EF32E}.
```



 

 
