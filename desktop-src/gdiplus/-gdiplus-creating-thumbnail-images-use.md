---
description: Un'immagine di anteprima è una versione ridotta di un'immagine. È possibile creare un'immagine di anteprima chiamando il metodo GetThumbnailImage di un oggetto Image.
ms.assetid: 96f95d00-6f96-4b8a-b84b-010203433d74
title: Creazione di immagini di anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ac737a49bad85ecc25eeeef1266a02cdeb408f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561189"
---
# <a name="creating-thumbnail-images"></a><span data-ttu-id="554f0-104">Creazione di immagini di anteprima</span><span class="sxs-lookup"><span data-stu-id="554f0-104">Creating Thumbnail Images</span></span>

<span data-ttu-id="554f0-105">Un'immagine di anteprima è una versione ridotta di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="554f0-105">A thumbnail image is a small version of an image.</span></span> <span data-ttu-id="554f0-106">È possibile creare un'immagine di anteprima chiamando il metodo **GetThumbnailImage** di un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="554f0-106">You can create a thumbnail image by calling the **GetThumbnailImage** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span>

<span data-ttu-id="554f0-107">Nell'esempio seguente viene costruito un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) dal file Compass.bmp.</span><span class="sxs-lookup"><span data-stu-id="554f0-107">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Compass.bmp.</span></span> <span data-ttu-id="554f0-108">L'immagine originale ha una larghezza di 640 pixel e un'altezza di 479 pixel.</span><span class="sxs-lookup"><span data-stu-id="554f0-108">The original image has a width of 640 pixels and a height of 479 pixels.</span></span> <span data-ttu-id="554f0-109">Il codice crea un'immagine di anteprima con una larghezza di 100 pixel e un'altezza di 100 pixel.</span><span class="sxs-lookup"><span data-stu-id="554f0-109">The code creates a thumbnail image that has a width of 100 pixels and a height of 100 pixels.</span></span>


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



<span data-ttu-id="554f0-110">Nella figura seguente è illustrata l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="554f0-110">The following illustration shows the thumbnail image.</span></span>

![illustrazione di un piccolo grafico che mostra una bussola](images/thumbnail1.png)

 

 



