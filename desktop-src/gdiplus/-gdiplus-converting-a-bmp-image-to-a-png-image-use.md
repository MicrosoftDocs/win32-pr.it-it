---
description: Per salvare un'immagine in un file su disco, chiamare il metodo Save della classe Image.
ms.assetid: a95fa3ea-2013-45d5-bdec-61eddcefc2fa
title: Conversione di un'immagine BMP in un'immagine PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a68acc269e1fecf5e8a42a2da54a5d0d5ce89ee156d83894078392e5d5f1605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467151"
---
# <a name="converting-a-bmp-image-to-a-png-image"></a>Conversione di un'immagine BMP in un'immagine PNG

Per salvare un'immagine in un file su disco, chiamare [il metodo Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) della classe [**Image.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) L'applicazione console seguente carica un'immagine BMP da un file su disco, converte l'immagine nel formato PNG e salva l'immagine convertita in un nuovo file su disco. La funzione main si basa sulla funzione helper GetEncoderClsid, illustrata in Recupero dell'identificatore di classe [per un codificatore.](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID   encoderClsid;
   Status  stat;
   Image*   image = new Image(L"Bird.bmp");

   // Get the CLSID of the PNG encoder.
   GetEncoderClsid(L"image/png", &encoderClsid);

   stat = image->Save(L"Bird.png", &encoderClsid, NULL);

   if(stat == Ok)
      printf("Bird.png was saved successfully\n");
   else
      printf("Failure: stat = %d\n", stat); 

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 



