---
description: È possibile riempire una forma chiusa con una trama usando la classe Image e la classe TextureBrush.
ms.assetid: 12e1e132-a93f-4438-8a1d-9036a43a8fd8
title: Riempimento di una forma con una trama dell'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f1bf6ba04311310ab1985de1d1aaccd45db43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131342"
---
# <a name="filling-a-shape-with-an-image-texture"></a><span data-ttu-id="2a3df-103">Riempimento di una forma con una trama dell'immagine</span><span class="sxs-lookup"><span data-stu-id="2a3df-103">Filling a Shape with an Image Texture</span></span>

<span data-ttu-id="2a3df-104">È possibile riempire una forma chiusa con una trama usando la classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e la classe [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .</span><span class="sxs-lookup"><span data-stu-id="2a3df-104">You can fill a closed shape with a texture by using the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) class.</span></span>

<span data-ttu-id="2a3df-105">Nell'esempio seguente viene riempita un'ellisse con un'immagine.</span><span class="sxs-lookup"><span data-stu-id="2a3df-105">The following example fills an ellipse with an image.</span></span> <span data-ttu-id="2a3df-106">Il codice costruisce un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , quindi passa l'indirizzo di tale oggetto **immagine** come argomento a un costruttore [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .</span><span class="sxs-lookup"><span data-stu-id="2a3df-106">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, and then passes the address of that **Image** object as an argument to a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) constructor.</span></span> <span data-ttu-id="2a3df-107">La terza istruzione di codice ridimensiona l'immagine e la quarta viene riempita dall'ellisse con copie ripetute dell'immagine ridimensionata:</span><span class="sxs-lookup"><span data-stu-id="2a3df-107">The third code statement scales the image, and the fourth statement fills the ellipse with repeated copies of the scaled image:</span></span>


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



<span data-ttu-id="2a3df-108">Nell'esempio di codice precedente, il metodo [**TextureBrush:: setransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) imposta la trasformazione applicata all'immagine prima che venga disegnata.</span><span class="sxs-lookup"><span data-stu-id="2a3df-108">In the preceding code example, the [**TextureBrush::SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) method sets the transformation that is applied to the image before it is drawn.</span></span> <span data-ttu-id="2a3df-109">Si supponga che l'immagine originale abbia una larghezza di 640 pixel e un'altezza di 480 pixel.</span><span class="sxs-lookup"><span data-stu-id="2a3df-109">Assume that the original image has a width of 640 pixels and a height of 480 pixels.</span></span> <span data-ttu-id="2a3df-110">La trasformazione compatta l'immagine a 75 × 75, impostando i valori di ridimensionamento orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="2a3df-110">The transform shrinks the image to 75 ×75, by setting the horizontal and vertical scaling values.</span></span>

> [!Note]  
> <span data-ttu-id="2a3df-111">Nell'esempio precedente, la dimensione dell'immagine è 75 × 75 e la dimensione dell'ellisse è 150 × 250.</span><span class="sxs-lookup"><span data-stu-id="2a3df-111">In the preceding example, the image size is 75 ×75, and the ellipse size is 150 ×250.</span></span> <span data-ttu-id="2a3df-112">Poiché l'immagine è più piccola dell'ellisse che sta riempiendo, l'ellisse viene affiancata all'immagine.</span><span class="sxs-lookup"><span data-stu-id="2a3df-112">Because the image is smaller than the ellipse it is filling, the ellipse is tiled with the image.</span></span> <span data-ttu-id="2a3df-113">L'affiancamento significa che l'immagine viene ripetuta orizzontalmente e verticalmente fino a quando non viene raggiunto il limite della forma.</span><span class="sxs-lookup"><span data-stu-id="2a3df-113">Tiling means that the image is repeated horizontally and vertically until the boundary of the shape is reached.</span></span> <span data-ttu-id="2a3df-114">Per ulteriori informazioni sull'affiancamento, vedere [affiancare una forma con un'immagine](-gdiplus-tiling-a-shape-with-an-image-use.md).</span><span class="sxs-lookup"><span data-stu-id="2a3df-114">For more information on tiling, see [Tiling a Shape with an Image](-gdiplus-tiling-a-shape-with-an-image-use.md).</span></span>

 

 

 



