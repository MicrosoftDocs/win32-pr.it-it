---
description: Con determinati formati di file, è possibile salvare più immagini (frame) in un singolo file.
ms.assetid: 9b61e01d-0a98-4ac3-865e-7570ed0c3cde
title: Creazione e salvataggio di un'immagine a più frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532a8fc8f8fc7e8742651f3d3853e001d493609b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131355"
---
# <a name="creating-and-saving-a-multiple-frame-image"></a>Creazione e salvataggio di un'immagine a più frame

Con determinati formati di file, è possibile salvare più immagini (frame) in un singolo file. Ad esempio, è possibile salvare più pagine in un unico file TIFF. Per salvare la prima pagina, chiamare il metodo [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) della classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Per salvare le pagine successive, chiamare il metodo [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) della classe **Image** .

> [!Note]  
> Non è possibile usare [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) per aggiungere frame a un file GIF animato.

 

La seguente applicazione console crea un file TIFF con quattro pagine. Le immagini che diventano le pagine del file TIFF provengono da quattro file su disco: Shapes.bmp, Cereal.gif, Iron.jpg e House.png. Il codice crea innanzitutto quattro oggetti [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) : multi, **pagina2** **,** **pagina3** e **pagina4**. Inizialmente, la **funzionalità multifunzione** contiene solo l'immagine di Shapes.bmp, ma alla fine contiene tutte e quattro le immagini. Man mano **che le singole** pagine vengono aggiunte all'oggetto **multiimage** , vengono aggiunte anche al file su disco multiframe. TIF.  

Si noti che il codice chiama [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (Not [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) per salvare la prima pagina. Il primo argomento passato al metodo Save è il nome del file su disco che conterrà infine diversi frame. Il secondo argomento passato al metodo Save specifica il codificatore che verrà usato per **convertire i dati** nell'oggetto [**multiimage**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) nel formato (in questo caso TIFF) richiesto dal file su disco.   Lo stesso codificatore viene usato automaticamente da **tutte le chiamate** successive al Metodo SaveAdd dell'oggetto **multiimage** .  

Il terzo argomento passato al metodo [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) è l'indirizzo di un oggetto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) . L'oggetto **EncoderParameters** include una matrice che contiene un singolo oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Il membro **GUID** di tale oggetto **EncoderParameter** è impostato su EncoderSaveFlag. Il membro del **valore** dell'oggetto **EncoderParameter** punta a un **ULONG** che contiene il valore EncoderValueMultiFrame.

Il codice salva la seconda, la terza e la quarta pagina chiamando il metodo [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) **dell'oggetto**  [**multiimage**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Il primo argomento passato al Metodo SaveAdd è l'indirizzo di un oggetto **Image** . L'immagine nell'oggetto **Image** viene **aggiunta all'oggetto**  **multiimage** ed è aggiunta anche al file su disco multiframe. TIF. Il secondo argomento passato al Metodo SaveAdd è l'indirizzo dello stesso oggetto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) utilizzato dal metodo [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) . La differenza è che **ULONG** a cui fa riferimento il membro **value** ora contiene il valore EncoderValueFrameDimensionPage.

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



 

 
