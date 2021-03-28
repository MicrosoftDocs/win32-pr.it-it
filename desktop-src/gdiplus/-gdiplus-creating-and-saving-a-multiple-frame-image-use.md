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
# <a name="creating-and-saving-a-multiple-frame-image"></a><span data-ttu-id="19374-103">Creazione e salvataggio di un'immagine a più frame</span><span class="sxs-lookup"><span data-stu-id="19374-103">Creating and Saving a Multiple-Frame Image</span></span>

<span data-ttu-id="19374-104">Con determinati formati di file, è possibile salvare più immagini (frame) in un singolo file.</span><span class="sxs-lookup"><span data-stu-id="19374-104">With certain file formats, you can save multiple images (frames) to a single file.</span></span> <span data-ttu-id="19374-105">Ad esempio, è possibile salvare più pagine in un unico file TIFF.</span><span class="sxs-lookup"><span data-stu-id="19374-105">For example, you can save several pages to a single TIFF file.</span></span> <span data-ttu-id="19374-106">Per salvare la prima pagina, chiamare il metodo [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) della classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="19374-106">To save the first page, call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="19374-107">Per salvare le pagine successive, chiamare il metodo [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) della classe **Image** .</span><span class="sxs-lookup"><span data-stu-id="19374-107">To save subsequent pages, call the [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method of the **Image** class.</span></span>

> [!Note]  
> <span data-ttu-id="19374-108">Non è possibile usare [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) per aggiungere frame a un file GIF animato.</span><span class="sxs-lookup"><span data-stu-id="19374-108">You cannot use [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) to add frames to an animated gif file.</span></span>

 

<span data-ttu-id="19374-109">La seguente applicazione console crea un file TIFF con quattro pagine.</span><span class="sxs-lookup"><span data-stu-id="19374-109">The following console application creates a TIFF file with four pages.</span></span> <span data-ttu-id="19374-110">Le immagini che diventano le pagine del file TIFF provengono da quattro file su disco: Shapes.bmp, Cereal.gif, Iron.jpg e House.png.</span><span class="sxs-lookup"><span data-stu-id="19374-110">The images that become the pages of the TIFF file come from four disk files: Shapes.bmp, Cereal.gif, Iron.jpg, and House.png.</span></span> <span data-ttu-id="19374-111">Il codice crea innanzitutto quattro oggetti [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) : multi, **pagina2** **,** **pagina3** e **pagina4**.</span><span class="sxs-lookup"><span data-stu-id="19374-111">The code first constructs four [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects: **multi**, **page2**, **page3**, and **page4**.</span></span> <span data-ttu-id="19374-112">Inizialmente, la **funzionalità multifunzione** contiene solo l'immagine di Shapes.bmp, ma alla fine contiene tutte e quattro le immagini.</span><span class="sxs-lookup"><span data-stu-id="19374-112">At first, **multi** contains only the image from Shapes.bmp, but eventually it contains all four images.</span></span> <span data-ttu-id="19374-113">Man mano **che le singole** pagine vengono aggiunte all'oggetto **multiimage** , vengono aggiunte anche al file su disco multiframe. TIF.  </span><span class="sxs-lookup"><span data-stu-id="19374-113">As the individual pages are added to the **multi**  **Image** object, they are also added to the disk file Multiframe.tif.</span></span>

<span data-ttu-id="19374-114">Si noti che il codice chiama [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (Not [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) per salvare la prima pagina.</span><span class="sxs-lookup"><span data-stu-id="19374-114">Note that the code calls [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (not [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) to save the first page.</span></span> <span data-ttu-id="19374-115">Il primo argomento passato al metodo Save è il nome del file su disco che conterrà infine diversi frame.</span><span class="sxs-lookup"><span data-stu-id="19374-115">The first argument passed to the Save method is the name of the disk file that will eventually contain several frames.</span></span> <span data-ttu-id="19374-116">Il secondo argomento passato al metodo Save specifica il codificatore che verrà usato per **convertire i dati** nell'oggetto [**multiimage**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) nel formato (in questo caso TIFF) richiesto dal file su disco.  </span><span class="sxs-lookup"><span data-stu-id="19374-116">The second argument passed to the Save method specifies the encoder that will be used to convert the data in the **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object to the format (in this case TIFF) required by the disk file.</span></span> <span data-ttu-id="19374-117">Lo stesso codificatore viene usato automaticamente da **tutte le chiamate** successive al Metodo SaveAdd dell'oggetto **multiimage** .  </span><span class="sxs-lookup"><span data-stu-id="19374-117">That same encoder is used automatically by all subsequent calls to the SaveAdd method of the **multi**  **Image** object.</span></span>

<span data-ttu-id="19374-118">Il terzo argomento passato al metodo [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) è l'indirizzo di un oggetto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) .</span><span class="sxs-lookup"><span data-stu-id="19374-118">The third argument passed to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method is the address of an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object.</span></span> <span data-ttu-id="19374-119">L'oggetto **EncoderParameters** include una matrice che contiene un singolo oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="19374-119">The **EncoderParameters** object has an array that contains a single [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="19374-120">Il membro **GUID** di tale oggetto **EncoderParameter** è impostato su EncoderSaveFlag.</span><span class="sxs-lookup"><span data-stu-id="19374-120">The **Guid** member of that **EncoderParameter** object is set to EncoderSaveFlag.</span></span> <span data-ttu-id="19374-121">Il membro del **valore** dell'oggetto **EncoderParameter** punta a un **ULONG** che contiene il valore EncoderValueMultiFrame.</span><span class="sxs-lookup"><span data-stu-id="19374-121">The **Value** member of the **EncoderParameter** object points to a **ULONG** that contains the value EncoderValueMultiFrame.</span></span>

<span data-ttu-id="19374-122">Il codice salva la seconda, la terza e la quarta pagina chiamando il metodo [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) **dell'oggetto**  [**multiimage**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="19374-122">The code saves the second, third, and fourth pages by calling the [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method of the **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="19374-123">Il primo argomento passato al Metodo SaveAdd è l'indirizzo di un oggetto **Image** .</span><span class="sxs-lookup"><span data-stu-id="19374-123">The first argument passed to the SaveAdd method is the address of an **Image** object.</span></span> <span data-ttu-id="19374-124">L'immagine nell'oggetto **Image** viene **aggiunta all'oggetto**  **multiimage** ed è aggiunta anche al file su disco multiframe. TIF.</span><span class="sxs-lookup"><span data-stu-id="19374-124">The image in that **Image** object is added to the **multi**  **Image** object and is also added to the Multiframe.tif disk file.</span></span> <span data-ttu-id="19374-125">Il secondo argomento passato al Metodo SaveAdd è l'indirizzo dello stesso oggetto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) utilizzato dal metodo [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) .</span><span class="sxs-lookup"><span data-stu-id="19374-125">The second argument passed to the SaveAdd method is the address of the same [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object that was used by the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method.</span></span> <span data-ttu-id="19374-126">La differenza è che **ULONG** a cui fa riferimento il membro **value** ora contiene il valore EncoderValueFrameDimensionPage.</span><span class="sxs-lookup"><span data-stu-id="19374-126">The difference is that the **ULONG** pointed to by the **Value** member now contains the value EncoderValueFrameDimensionPage.</span></span>

<span data-ttu-id="19374-127">La funzione Main si basa sulla funzione helper GetEncoderClsid, che viene mostrata durante il [recupero dell'identificatore di classe per un codificatore](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="19374-127">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
