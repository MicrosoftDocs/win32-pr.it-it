---
description: Con determinati formati di file, è possibile salvare più immagini (frame) in un singolo file.
ms.assetid: 9b61e01d-0a98-4ac3-865e-7570ed0c3cde
title: Creazione e salvataggio di un'immagine a più frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd99bc2d5f21c143b66ccc201f9a96a93f3437516a6fd1cdd03e521a00ceb59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115121"
---
# <a name="creating-and-saving-a-multiple-frame-image"></a>Creazione e salvataggio di un'immagine a più frame

Con determinati formati di file, è possibile salvare più immagini (frame) in un singolo file. Ad esempio, è possibile salvare diverse pagine in un singolo file TIFF. Per salvare la prima pagina, chiamare il [metodo Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) della [**classe**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Image. Per salvare le pagine successive, chiamare il [metodo SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) della **classe Image.**

> [!Note]  
> Non è possibile usare [SalvaAggiungi](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) per aggiungere fotogrammi a un file gif animato.

 

L'applicazione console seguente crea un file TIFF con quattro pagine. Le immagini che diventano le pagine del file TIFF provengono da quattro file su disco: Shapes.bmp, Cereal.gif, Iron.jpg e House.png. Il codice costruisce innanzitutto quattro [**oggetti Image:**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) **multi**, **page2**, **page3** e **page4**. All'inizio, **multi** contiene solo l'immagine Shapes.bmp, ma alla fine contiene tutte e quattro le immagini. Quando le singole pagine vengono aggiunte all'oggetto **Multi**  **Image,** vengono aggiunte anche al file su disco Multiframe.tif.

Si noti che il codice chiama [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (non [SaveAdd)](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))per salvare la prima pagina. Il primo argomento passato al metodo Save è il nome del file su disco che conterrà alla fine diversi frame. Il secondo argomento passato al metodo Save specifica il codificatore che verrà usato per convertire i dati nell'oggetto **Multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) nel formato (in questo caso TIFF) richiesto dal file su disco. Lo stesso codificatore viene usato automaticamente da tutte le chiamate successive al metodo SaveAdd **dell'oggetto Multi****Image.**  

Il terzo argomento passato al [metodo Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) è l'indirizzo di un [**oggetto EncoderParameters.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) **L'oggetto EncoderParameters** ha una matrice che contiene un singolo [**oggetto EncoderParameter.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) Il **membro Guid** dell'oggetto **EncoderParameter** è impostato su EncoderSaveFlag. Il **membro Value** dell'oggetto **EncoderParameter** punta a un **ULONG** che contiene il valore EncoderValueMultiFrame.

Il codice salva la seconda, la terza e la quarta pagina chiamando il [metodo SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) dell'oggetto **Multi**[**Image.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)   Il primo argomento passato al metodo SaveAdd è l'indirizzo di un **oggetto** Image. L'immagine in **tale oggetto Image** viene aggiunta all'oggetto Multi **Image** e viene aggiunta anche al file di disco Multiframe.tif.   Il secondo argomento passato al metodo SaveAdd è l'indirizzo dello stesso oggetto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) usato dal [metodo Save.](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) La differenza è che **L'ULONG** a cui punta il membro **Value** contiene ora il valore EncoderValueFrameDimensionPage.

La funzione main si basa sulla funzione helper GetEncoderClsid, illustrata in Recupero dell'identificatore di classe [per un codificatore.](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)


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

   EncoderParameters encoderParameters;
   ULONG             parameterValue;
   Status            stat;

   // An EncoderParameters object has an array of
   // EncoderParameter objects. In this case, there is only
   // one EncoderParameter object in the array.
   encoderParameters.Count = 1;

   // Initialize the one EncoderParameter object.
   encoderParameters.Parameter[0].Guid = EncoderSaveFlag;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;
   encoderParameters.Parameter[0].Value = &parameterValue;

   // Get the CLSID of the TIFF encoder.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/tiff", &encoderClsid);

   // Create four image objects.
   Image* multi = new Image(L"Shapes.bmp");
   Image* page2 = new Image(L"Cereal.gif");
   Image* page3 = new Image(L"Iron.jpg");
   Image* page4 = new Image(L"House.png");

   // Save the first page (frame).
   parameterValue = EncoderValueMultiFrame;
   stat = multi->Save(L"MultiFrame.tif", &encoderClsid, &encoderParameters);
   if(stat == Ok)
      printf("Page 1 saved successfully.\n");

   // Save the second page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page2, &encoderParameters);
   if(stat == Ok)
      printf("Page 2 saved successfully.\n");

   // Save the third page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page3, &encoderParameters);
   if(stat == Ok)
      printf("Page 3 saved successfully.\n");

   // Save the fourth page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page4, &encoderParameters);
   if(stat == Ok)
      printf("Page 4 saved successfully.\n");

   // Close the multiframe file.
   parameterValue = EncoderValueFlush;
   stat = multi->SaveAdd(&encoderParameters);
   if(stat == Ok)
      printf("File closed successfully.\n");

   delete multi;
   delete page2;
   delete page3;
   delete page4;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
