---
title: Trasformazione di un'immagine JPEG senza perdita di dati
description: Quando si comprime un'immagine JPEG, alcune informazioni nell'immagine vengono perse.
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ea7011f25a97a228c44bdb87ba09ca8b284ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977543"
---
# <a name="lossless-transform-of-a-jpeg-image"></a>Trasformazione di un'immagine JPEG senza perdita di dati

Quando si comprime un'immagine JPEG, alcune informazioni nell'immagine vengono perse. Se si apre un file JPEG, si modifica l'immagine e lo si salva in un altro file JPEG, la qualità diminuisce. Se si ripete il processo più volte, si noterà un calo sostanziale della qualità dell'immagine.

Poiché il formato JPEG è uno dei formati di immagine più diffusi sul Web e, poiché spesso si desidera modificare le immagini JPEG, GDI+ fornisce le trasformazioni seguenti che possono essere eseguite sulle immagini JPEG senza perdita di informazioni:

-   Ruota di 90 gradi
-   Ruota di 180 gradi
-   Ruota di 270 gradi
-   Capovolgi orizzontalmente
-   Capovolgi verticalmente

È possibile applicare una delle trasformazioni mostrate nell'elenco precedente quando si chiama il metodo [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) di un oggetto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Se vengono soddisfatte le condizioni seguenti, la trasformazione proseguirà senza perdita di informazioni:

-   Il file usato per costruire l'oggetto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) è un file JPEG.
-   La larghezza e l'altezza dell'immagine sono entrambi multipli di 16.

Se la larghezza e l'altezza dell'immagine non sono entrambi multipli di 16, GDI+ ne eseguirà la migliore per mantenere la qualità dell'immagine quando si applica una delle trasformazioni di rotazione o capovolgimento visualizzate nell'elenco precedente.

Per trasformare un'immagine JPEG, inizializzare un oggetto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) e passare l'indirizzo dell'oggetto al metodo [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) della classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Inizializzare l'oggetto **EncoderParameters** in modo che disponga di una matrice costituita da un oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Inizializzare un oggetto **EncoderParameter** in modo che il membro **value** punti a una variabile **ULONG** che include uno degli elementi seguenti dell'enumerazione [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :

-   EncoderValueTransformRotate90,
-   EncoderValueTransformRotate180,
-   EncoderValueTransformRotate270,
-   EncoderValueTransformFlipHorizontal,
-   EncoderValueTransformFlipVertical

Impostare il membro **GUID** dell'oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) su EncoderTransformation.

La seguente applicazione console crea un oggetto [**immagine**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) da un file JPEG e quindi Salva l'immagine in un nuovo file. Durante il processo di salvataggio, l'immagine viene ruotata di 90 gradi. Se la larghezza e l'altezza dell'immagine sono entrambi multipli di 16, il processo di rotazione e salvataggio dell'immagine non comporta la perdita di informazioni.

La funzione Main si basa sulla funzione helper GetEncoderClsid, che viene mostrata durante il [recupero dell'identificatore di classe per un codificatore](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


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

   CLSID             encoderClsid;
   EncoderParameters encoderParameters;
   ULONG             transformation;
   UINT              width;
   UINT              height;
   Status            stat;

   // Get a JPEG image from the disk.
   Image* image = new Image(L"Shapes.jpg");

   // Determine whether the width and height of the image 
   // are multiples of 16.
   width = image->GetWidth();
   height = image->GetHeight();

   printf("The width of the image is %u", width);
   if(width / 16.0 - width / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   printf("The height of the image is %u", height);
   if(height / 16.0 - height / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // Before we call Image::Save, we must initialize an
   // EncoderParameters object. The EncoderParameters object
   // has an array of EncoderParameter objects. In this
   // case, there is only one EncoderParameter object in the array.
   // The one EncoderParameter object has an array of values.
   // In this case, there is only one value (of type ULONG)
   // in the array. We will set that value to EncoderValueTransformRotate90.

   encoderParameters.Count = 1;
   encoderParameters.Parameter[0].Guid = EncoderTransformation;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;

   // Rotate and save the image.
   transformation = EncoderValueTransformRotate90;
   encoderParameters.Parameter[0].Value = &transformation;
   stat = image->Save(L"ShapesR90.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"ShapesR90.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"ShapesR90.jpg");

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
