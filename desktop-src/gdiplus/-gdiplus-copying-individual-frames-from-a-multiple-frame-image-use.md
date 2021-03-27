---
title: Copiare singoli frame da un'immagine a più fotogrammi
description: Nell'esempio seguente vengono recuperati i singoli frame da un file TIFF a più frame.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6bdb5668bcebb9babcbcb7d07839694750aec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227086"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a><span data-ttu-id="d76b3-103">Copiare singoli frame da un'immagine a più fotogrammi</span><span class="sxs-lookup"><span data-stu-id="d76b3-103">Copy individual frames from a multiple-frame image</span></span>

<span data-ttu-id="d76b3-104">Nell'esempio seguente vengono recuperati i singoli frame da un file TIFF a più frame.</span><span class="sxs-lookup"><span data-stu-id="d76b3-104">The following example retrieves the individual frames from a multiple-frame TIFF file.</span></span> <span data-ttu-id="d76b3-105">Quando il file TIFF è stato creato, i singoli frame sono stati aggiunti alla dimensione della pagina (vedere [creazione e salvataggio di un'immagine di Multiple-Frame](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span><span class="sxs-lookup"><span data-stu-id="d76b3-105">When the TIFF file was created, the individual frames were added to the Page dimension (see [Creating and Saving a Multiple-Frame Image](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span></span> <span data-ttu-id="d76b3-106">Il codice visualizza ognuna delle quattro pagine e salva ogni pagina in un file di disco PNG separato.</span><span class="sxs-lookup"><span data-stu-id="d76b3-106">The code displays each of the four pages and saves each page to a separate PNG disk file.</span></span>

<span data-ttu-id="d76b3-107">Il codice costruisce un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file TIFF a più frame.</span><span class="sxs-lookup"><span data-stu-id="d76b3-107">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the multiple-frame TIFF file.</span></span> <span data-ttu-id="d76b3-108">Per recuperare i singoli frame (pagine), il codice chiama il metodo [**Image:: SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) di tale oggetto **Image** .</span><span class="sxs-lookup"><span data-stu-id="d76b3-108">To retrieve the individual frames (pages), the code calls the [**Image::SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) method of that **Image** object.</span></span> <span data-ttu-id="d76b3-109">Il primo argomento passato al metodo **Image:: SelectActiveFrame** è l'indirizzo di un GUID che specifica la dimensione in cui i frame sono stati aggiunti in precedenza al file TIFF a più frame.</span><span class="sxs-lookup"><span data-stu-id="d76b3-109">The first argument passed to the **Image::SelectActiveFrame** method is the address of a GUID that specifies the dimension in which the frames were previously added to the multiple-frame TIFF file.</span></span> <span data-ttu-id="d76b3-110">Il GUID FrameDimensionPage è definito in Gdiplusimaging. h.</span><span class="sxs-lookup"><span data-stu-id="d76b3-110">The GUID FrameDimensionPage is defined in Gdiplusimaging.h.</span></span> <span data-ttu-id="d76b3-111">Altri GUID definiti in tale file di intestazione sono FrameDimensionTime e FrameDimensionResolution.</span><span class="sxs-lookup"><span data-stu-id="d76b3-111">Other GUIDs defined in that header file are FrameDimensionTime and FrameDimensionResolution.</span></span> <span data-ttu-id="d76b3-112">Il secondo argomento passato al metodo **Image:: SelectActiveFrame** è l'indice in base zero della pagina desiderata.</span><span class="sxs-lookup"><span data-stu-id="d76b3-112">The second argument passed to the **Image::SelectActiveFrame** method is the zero-based index of the desired page.</span></span>

<span data-ttu-id="d76b3-113">Il codice si basa sulla funzione helper GetEncoderClsid, che viene illustrata nel [recupero dell'identificatore di classe per un codificatore](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="d76b3-113">The code relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
GUID   pageGuid = FrameDimensionPage;
CLSID  encoderClsid;
Image  multi(L"Multiframe.tif");

// Get the CLSID of the PNG encoder.
GetEncoderClsid(L"image/png", &encoderClsid);

// Display and save the first page (index 0).
multi.SelectActiveFrame(&pageGuid, 0);
graphics.DrawImage(&multi, 10, 10);
multi.Save(L"Page0.png", &encoderClsid, NULL);

// Display and save the second page.
multi.SelectActiveFrame(&pageGuid, 1);
graphics.DrawImage(&multi, 200, 10);
multi.Save(L"Page1.png", &encoderClsid, NULL);

// Display and save the third page.
multi.SelectActiveFrame(&pageGuid, 2);
graphics.DrawImage(&multi, 10, 150);
multi.Save(L"Page2.png", &encoderClsid, NULL);

// Display and save the fourth page.
multi.SelectActiveFrame(&pageGuid, 3);
graphics.DrawImage(&multi, 200, 150);
multi.Save(L"Page3.png", &encoderClsid, NULL);
```



<span data-ttu-id="d76b3-114">Nella figura seguente sono illustrate le singole pagine visualizzate dal codice precedente.</span><span class="sxs-lookup"><span data-stu-id="d76b3-114">The following illustration shows the individual pages as displayed by the preceding code.</span></span>

![illustrazione che mostra una forma geometrica, una foto a colori, una foto monocromatica e una forma geometrica diversa](images/multiframe1.png)

 

 



