---
description: Così come i riquadri possono essere posizionati uno accanto all'altro per coprire un pavimento, le immagini rettangolari possono essere posizionate l'una accanto all'altra per riempire (affiancare) una forma.
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: Affiancamento di una forma con un'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c0b6e2ce39f5bf5c43b0352b8997202aa7e856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129062"
---
# <a name="tiling-a-shape-with-an-image"></a><span data-ttu-id="7c616-103">Affiancamento di una forma con un'immagine</span><span class="sxs-lookup"><span data-stu-id="7c616-103">Tiling a Shape with an Image</span></span>

<span data-ttu-id="7c616-104">Così come i riquadri possono essere posizionati uno accanto all'altro per coprire un pavimento, le immagini rettangolari possono essere posizionate l'una accanto all'altra per riempire (affiancare) una forma.</span><span class="sxs-lookup"><span data-stu-id="7c616-104">Just as tiles can be placed next to each other to cover a floor, rectangular images can be placed next to each other to fill (tile) a shape.</span></span> <span data-ttu-id="7c616-105">Per affiancare l'interno di una forma, utilizzare un pennello di trama.</span><span class="sxs-lookup"><span data-stu-id="7c616-105">To tile the interior of a shape, use a texture brush.</span></span> <span data-ttu-id="7c616-106">Quando si crea un oggetto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) , uno degli argomenti passati al costruttore è l'indirizzo di un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="7c616-106">When you construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, one of the arguments you pass to the constructor is the address of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="7c616-107">Quando si usa il pennello trama per disegnare l'interno di una forma, la forma viene riempita con copie ripetute dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7c616-107">When you use the texture brush to paint the interior of a shape, the shape is filled with repeated copies of this image.</span></span>

<span data-ttu-id="7c616-108">La proprietà modalità a capo dell'oggetto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) determina il modo in cui l'immagine è orientata mentre viene ripetuta in una griglia rettangolare.</span><span class="sxs-lookup"><span data-stu-id="7c616-108">The wrap mode property of the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object determines how the image is oriented as it is repeated in a rectangular grid.</span></span> <span data-ttu-id="7c616-109">È possibile fare in modo che tutti i riquadri nella griglia abbiano lo stesso orientamento oppure è possibile far passare l'immagine da una posizione della griglia a quella successiva.</span><span class="sxs-lookup"><span data-stu-id="7c616-109">You can make all the tiles in the grid have the same orientation, or you can make the image flip from one grid position to the next.</span></span> <span data-ttu-id="7c616-110">Il capovolgimento può essere orizzontale, verticale o entrambi.</span><span class="sxs-lookup"><span data-stu-id="7c616-110">The flipping can be horizontal, vertical, or both.</span></span> <span data-ttu-id="7c616-111">Gli esempi seguenti illustrano l'affiancamento con tipi diversi di capovolgimento.</span><span class="sxs-lookup"><span data-stu-id="7c616-111">The following examples demonstrate tiling with different types of flipping.</span></span>

## <a name="tiling-an-image"></a><span data-ttu-id="7c616-112">Affiancamento di un'immagine</span><span class="sxs-lookup"><span data-stu-id="7c616-112">Tiling an Image</span></span>

<span data-ttu-id="7c616-113">Questo esempio usa l'immagine 75 × 75 seguente per affiancare un rettangolo 200 × 200:</span><span class="sxs-lookup"><span data-stu-id="7c616-113">This example uses the following 75 ×75 image to tile a 200 ×200 rectangle:</span></span>

![illustrazione utilizzata come base di altre illustrazioni in questo argomento: una casa e un albero sullo sfondo e centrato in un rettangolo](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="7c616-115">Nella figura seguente viene illustrato il modo in cui il rettangolo viene affiancato all'immagine.</span><span class="sxs-lookup"><span data-stu-id="7c616-115">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="7c616-116">Si noti che tutti i riquadri hanno lo stesso orientamento; Nessun capovolgimento.</span><span class="sxs-lookup"><span data-stu-id="7c616-116">Note that all tiles have the same orientation; there is no flipping.</span></span>

![illustrazione che mostra l'immagine di base ripetuta orizzontalmente e verticalmente in un rettangolo di grandi dimensioni](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a><span data-ttu-id="7c616-118">Capovolgimento orizzontale di un'immagine durante l'affiancamento</span><span class="sxs-lookup"><span data-stu-id="7c616-118">Flipping an Image Horizontally While Tiling</span></span>

<span data-ttu-id="7c616-119">Questo esempio usa un'immagine 75 × 75 per riempire un rettangolo 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="7c616-119">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="7c616-120">La modalità a capo automatico è impostata per capovolgere orizzontalmente l'immagine.</span><span class="sxs-lookup"><span data-stu-id="7c616-120">The wrap mode is set to flip the image horizontally.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="7c616-121">Nella figura seguente viene illustrato il modo in cui il rettangolo viene affiancato all'immagine.</span><span class="sxs-lookup"><span data-stu-id="7c616-121">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="7c616-122">Si noti che quando si passa da un riquadro all'altro in una determinata riga, l'immagine viene capovolta orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="7c616-122">Note that as you move from one tile to the next in a given row, the image is flipped horizontally.</span></span>

![illustrazione che mostra l'immagine di base ripetuta orizzontalmente, ma le istanze con numerazione uniforme vengono invertite orizzontalmente](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a><span data-ttu-id="7c616-124">Capovolgimento verticale di un'immagine durante l'affiancamento</span><span class="sxs-lookup"><span data-stu-id="7c616-124">Flipping an Image Vertically While Tiling</span></span>

<span data-ttu-id="7c616-125">Questo esempio usa un'immagine 75 × 75 per riempire un rettangolo 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="7c616-125">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="7c616-126">La modalità Wrap è impostata per capovolgere l'immagine verticalmente.</span><span class="sxs-lookup"><span data-stu-id="7c616-126">The wrap mode is set to flip the image vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="7c616-127">Nella figura seguente viene illustrato il modo in cui il rettangolo viene affiancato all'immagine.</span><span class="sxs-lookup"><span data-stu-id="7c616-127">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="7c616-128">Si noti che quando si passa da un riquadro all'altro in una colonna specificata, l'immagine viene capovolta verticalmente.</span><span class="sxs-lookup"><span data-stu-id="7c616-128">Note that as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![illustrazione che mostra l'immagine di base ripetuta orizzontalmente e verticalmente, ma le righe con numerazione uniforme vengono invertite verticalmente](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a><span data-ttu-id="7c616-130">Capovolgimento orizzontale e verticale di un'immagine durante l'affiancamento</span><span class="sxs-lookup"><span data-stu-id="7c616-130">Flipping an Image Horizontally and Vertically While Tiling</span></span>

<span data-ttu-id="7c616-131">Questo esempio usa un'immagine 75 × 75 per affiancare un rettangolo 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="7c616-131">This example uses a 75 ×75 image to tile a 200 ×200 rectangle.</span></span> <span data-ttu-id="7c616-132">La modalità a capo è impostata per capovolgere l'immagine sia orizzontalmente che verticalmente.</span><span class="sxs-lookup"><span data-stu-id="7c616-132">The wrap mode is set to flip the image both horizontally and vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="7c616-133">Nella figura seguente viene illustrato il modo in cui il rettangolo viene affiancato dall'immagine.</span><span class="sxs-lookup"><span data-stu-id="7c616-133">The following illustration shows how the rectangle is tiled by the image.</span></span> <span data-ttu-id="7c616-134">Si noti che quando si passa da un riquadro all'altro in una determinata riga, l'immagine viene capovolta orizzontalmente e quando si passa da un riquadro all'altro in una colonna specificata, l'immagine viene capovolta verticalmente.</span><span class="sxs-lookup"><span data-stu-id="7c616-134">Note that as you move from one tile to the next in a given row, the image is flipped horizontally, and as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![illustrazione che mostra le istanze alternate dell'immagine di base in ogni riga viene capovolta orizzontalmente e le righe alternate vengono capovolte verticalmente.](images/tile5.png)

 

 



