---
description: Windows GDI+ la funzione GetImageDecoders per determinare quali decodificatori di immagini sono disponibili nel computer.
ms.assetid: 793e23de-d959-4feb-8bf6-647a455c85ae
title: Elenco dei decodificatori installati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54548971ff4f4346d32884ff7abc687b901044022ab886f7191d5700b9db98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977391"
---
# <a name="listing-installed-decoders"></a>Elenco dei decodificatori installati

Windows GDI+ fornisce la [**funzione GetImageDecoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders) per determinare quali decodificatori di immagini sono disponibili nel computer. **GetImageDecoders restituisce** una matrice di [**oggetti ImageCodecInfo.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) Prima di chiamare **GetImageDecoders,** è necessario allocare un buffer sufficientemente grande per ricevere tale matrice. È possibile chiamare [**GetImageDecodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize) per determinare le dimensioni del buffer richiesto.

L'applicazione console seguente elenca i decodificatori di immagini disponibili:


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  num;        // number of image decoders
   UINT  size;       // size, in bytes, of the image decoder array

   ImageCodecInfo* pImageCodecInfo;

   // How many decoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageDecodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageDecoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageDecoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfo, is a pointer to that buffer. 
   GetImageDecoders(num, size, pImageCodecInfo);

   // Display the graphics file format (MimeType)
   // for each ImageCodecInfo object.
   for(UINT j = 0; j < num; ++j)
   { 
      wprintf(L"%s\n", pImageCodecInfo[j].MimeType);   
   }

   free(pImageCodecInfo);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Quando si esegue l'applicazione console precedente, l'output sarà simile al seguente:


```
image/bmp
image/jpeg
image/gif
image/x-emf
image/x-wmf
image/tiff
image/png
image/x-icon
```



 

 
