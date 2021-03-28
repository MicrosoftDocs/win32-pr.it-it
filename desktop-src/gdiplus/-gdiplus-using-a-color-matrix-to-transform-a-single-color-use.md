---
description: Windows GDI+ fornisce le classi di immagini e bitmap per l'archiviazione e la manipolazione delle immagini.
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: Uso di una matrice di colori per trasformare un singolo colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db56d0a64c36c08a5415d76e3fb184158d473268
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557846"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a><span data-ttu-id="0d952-103">Uso di una matrice di colori per trasformare un singolo colore</span><span class="sxs-lookup"><span data-stu-id="0d952-103">Using a Color Matrix to Transform a Single Color</span></span>

<span data-ttu-id="0d952-104">Windows GDI+ fornisce le classi di [**Immagini**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) e [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) per l'archiviazione e la manipolazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="0d952-104">Windows GDI+ provides the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) classes for storing and manipulating images.</span></span> <span data-ttu-id="0d952-105">Gli oggetti **Image** e **bitmap** memorizzano il colore di ogni pixel come numero a 32 bit: 8 bit per colore rosso, verde, blu e alfa.</span><span class="sxs-lookup"><span data-stu-id="0d952-105">**Image** and **Bitmap** objects store the color of each pixel as a 32-bit number: 8 bits each for red, green, blue, and alpha.</span></span> <span data-ttu-id="0d952-106">Ognuno dei quattro componenti è un numero compreso tra 0 e 255, 0 che rappresenta nessuna intensità e 255 che rappresenta l'intensità completa.</span><span class="sxs-lookup"><span data-stu-id="0d952-106">Each of the four components is a number from 0 through 255, with 0 representing no intensity and 255 representing full intensity.</span></span> <span data-ttu-id="0d952-107">Il componente alfa specifica la trasparenza del colore: 0 è completamente trasparente e 255 è completamente opaco.</span><span class="sxs-lookup"><span data-stu-id="0d952-107">The alpha component specifies the transparency of the color: 0 is fully transparent, and 255 is fully opaque.</span></span>

<span data-ttu-id="0d952-108">Un vettore di colore è una tupla con 4 elementi del form (rosso, verde, blu, alfa).</span><span class="sxs-lookup"><span data-stu-id="0d952-108">A color vector is a 4-tuple of the form (red, green, blue, alpha).</span></span> <span data-ttu-id="0d952-109">Ad esempio, il vettore di colore (0, 255, 0, 255) rappresenta un colore opaco che non ha rosso o blu, ma ha un verde a intensità piena.</span><span class="sxs-lookup"><span data-stu-id="0d952-109">For example, the color vector (0, 255, 0, 255) represents an opaque color that has no red or blue, but has green at full intensity.</span></span>

<span data-ttu-id="0d952-110">Un'altra convenzione per la rappresentazione dei colori usa il numero 1 per l'intensità massima e il numero 0 per l'intensità minima.</span><span class="sxs-lookup"><span data-stu-id="0d952-110">Another convention for representing colors uses the number 1 for maximum intensity and the number 0 for minimum intensity.</span></span> <span data-ttu-id="0d952-111">Usando tale convenzione, il colore descritto nel paragrafo precedente verrebbe rappresentato dal vettore (0, 1, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="0d952-111">Using that convention, the color described in the preceding paragraph would be represented by the vector (0, 1, 0, 1).</span></span> <span data-ttu-id="0d952-112">GDI+ utilizza la convenzione di 1 come intensità completa durante le trasformazioni dei colori.</span><span class="sxs-lookup"><span data-stu-id="0d952-112">GDI+ uses the convention of 1 as full intensity when it performs color transformations.</span></span>

<span data-ttu-id="0d952-113">È possibile applicare trasformazioni lineari (rotazione, ridimensionamento e così via) ai vettori colori moltiplicando per una matrice 4 × 4.</span><span class="sxs-lookup"><span data-stu-id="0d952-113">You can apply linear transformations (rotation, scaling, and the like) to color vectors by multiplying by a 4 ×4 matrix.</span></span> <span data-ttu-id="0d952-114">Tuttavia, non è possibile utilizzare una matrice 4 × 4 per eseguire una conversione (non lineare).</span><span class="sxs-lookup"><span data-stu-id="0d952-114">However, you cannot use a 4 ×4 matrix to perform a translation (nonlinear).</span></span> <span data-ttu-id="0d952-115">Se si aggiunge una quinta coordinata fittizia, ad esempio il numero 1, a ogni vettore di colore, è possibile utilizzare una matrice di 5 × 5 per applicare qualsiasi combinazione di trasformazioni e traduzioni lineari.</span><span class="sxs-lookup"><span data-stu-id="0d952-115">If you add a dummy fifth coordinate (for example, the number 1) to each of the color vectors, you can use a 5 ×5 matrix to apply any combination of linear transformations and translations.</span></span> <span data-ttu-id="0d952-116">Una trasformazione costituita da una trasformazione lineare seguita da una traduzione è detta trasformazione affine.</span><span class="sxs-lookup"><span data-stu-id="0d952-116">A transformation consisting of a linear transformation followed by a translation is called an affine transformation.</span></span> <span data-ttu-id="0d952-117">Una matrice di 5 × 5 che rappresenta una trasformazione affine è detta matrice omogenea per una trasformazione con 4 spazi.</span><span class="sxs-lookup"><span data-stu-id="0d952-117">A 5 ×5 matrix that represents an affine transformation is called a homogeneous matrix for a 4-space transformation.</span></span> <span data-ttu-id="0d952-118">L'elemento nella quinta riga e nella quinta colonna di una matrice omogenea 5 × 5 deve essere 1 e tutte le altre voci della quinta colonna devono essere pari a 0.</span><span class="sxs-lookup"><span data-stu-id="0d952-118">The element in the fifth row and fifth column of a 5 ×5 homogeneous matrix must be 1, and all of the other entries in the fifth column must be 0.</span></span>

<span data-ttu-id="0d952-119">Si supponga, ad esempio, di voler iniziare con il colore (0,2, 0,0, 0,4, 1,0) e applicare le trasformazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d952-119">For example, suppose you want to start with the color (0.2, 0.0, 0.4, 1.0) and apply the following transformations:</span></span>

1.  <span data-ttu-id="0d952-120">Raddoppiare il componente rosso</span><span class="sxs-lookup"><span data-stu-id="0d952-120">Double the red component</span></span>
2.  <span data-ttu-id="0d952-121">Aggiungere 0,2 ai componenti rosso, verde e blu</span><span class="sxs-lookup"><span data-stu-id="0d952-121">Add 0.2 to the red, green, and blue components</span></span>

<span data-ttu-id="0d952-122">La moltiplicazione di matrici seguente eseguirà la coppia di trasformazioni nell'ordine elencato.</span><span class="sxs-lookup"><span data-stu-id="0d952-122">The following matrix multiplication will perform the pair of transformations in the order listed.</span></span>

![illustrazione che mostra una matrice 5x1 di numeri moltiplicata per una matrice 5x5 per creare una nuova matrice 5x1](images/recoloring01.png)

<span data-ttu-id="0d952-124">Gli elementi di una matrice di colori sono indicizzati (in base zero) per riga e quindi colonna.</span><span class="sxs-lookup"><span data-stu-id="0d952-124">The elements of a color matrix are indexed (zero-based) by row and then column.</span></span> <span data-ttu-id="0d952-125">Ad esempio, la voce della quinta riga e della terza colonna della matrice M è indicata da M \[ 4 \] \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="0d952-125">For example, the entry in the fifth row and third column of matrix M is denoted by M\[4\]\[2\].</span></span>

<span data-ttu-id="0d952-126">La matrice di identità 5 × 5 (mostrata nella figura seguente) presenta 1S sulla diagonale e sugli zeri in qualsiasi altra posizione.</span><span class="sxs-lookup"><span data-stu-id="0d952-126">The 5 ×5 identity matrix (shown in the following illustration) has 1s on the diagonal and 0s everywhere else.</span></span> <span data-ttu-id="0d952-127">Se si moltiplica un vettore di colore per la matrice di identità, il vettore di colore non cambia.</span><span class="sxs-lookup"><span data-stu-id="0d952-127">If you multiply a color vector by the identity matrix, the color vector does not change.</span></span> <span data-ttu-id="0d952-128">Un modo pratico per formare la matrice di una trasformazione colore consiste nell'iniziare con la matrice di identità e apportare una piccola modifica che produce la trasformazione desiderata.</span><span class="sxs-lookup"><span data-stu-id="0d952-128">A convenient way to form the matrix of a color transformation is to start with the identity matrix and make a small change that produces the desired transformation.</span></span>

![illustrazione che mostra una matrice di identità 5x5; 1S in alto a sinistra e in basso a destra diagonale e 0 in qualsiasi altra posizione](images/recoloring02.png)

<span data-ttu-id="0d952-130">Per una descrizione più dettagliata delle matrici e delle trasformazioni, vedere [sistemi di coordinate e trasformazioni](-gdiplus-coordinate-systems-and-transformations-about.md).</span><span class="sxs-lookup"><span data-stu-id="0d952-130">For a more detailed discussion of matrices and transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="0d952-131">Nell'esempio seguente viene accettata un'immagine che corrisponde a un solo colore (0,2, 0,0, 0,4, 1,0) e viene applicata la trasformazione descritta nei paragrafi precedenti.</span><span class="sxs-lookup"><span data-stu-id="0d952-131">The following example takes an image that is all one color (0.2, 0.0, 0.4, 1.0) and applies the transformation described in the preceding paragraphs.</span></span>


```
Image            image(L"InputColor.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   2.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.2f, 0.2f, 0.2f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10);

graphics.DrawImage(
   &image, 
   Rect(120, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="0d952-132">Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine trasformata a destra.</span><span class="sxs-lookup"><span data-stu-id="0d952-132">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![<span data-ttu-id="0d952-133">illustrazione che mostra un rettangolo riempito da un colore a tinta unita scuro e quindi uno riempito con un colore a tinta unita più chiaro</span><span class="sxs-lookup"><span data-stu-id="0d952-133">illustration showing a rectangle filled by a dark solid color and then one filled by a lighter solid color</span></span> ](images/colortrans1.png)

<span data-ttu-id="0d952-134">Il codice nell'esempio precedente usa i passaggi seguenti per eseguire la ricolorazione:</span><span class="sxs-lookup"><span data-stu-id="0d952-134">The code in the preceding example uses the following steps to perform the recoloring:</span></span>

1.  <span data-ttu-id="0d952-135">Inizializzare una struttura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .</span><span class="sxs-lookup"><span data-stu-id="0d952-135">Initialize a [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>
2.  <span data-ttu-id="0d952-136">Creare un oggetto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) e passare l'indirizzo della struttura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) al metodo [**ImageAttributes:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) dell'oggetto **ImageAttributes** .</span><span class="sxs-lookup"><span data-stu-id="0d952-136">Create an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object and pass the address of the [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure to the [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) method of the **ImageAttributes** object.</span></span>
3.  <span data-ttu-id="0d952-137">Passare l'indirizzo dell'oggetto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) al metodo [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) di un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="0d952-137">Pass the address of the [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

 

 



