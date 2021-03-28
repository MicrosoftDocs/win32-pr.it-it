---
description: La rotazione in uno spazio di colore a quattro dimensioni è difficile da visualizzare.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Rotazione di colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea322179bd4a46021d181abedd1797d6bdda7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879173"
---
# <a name="rotating-colors"></a><span data-ttu-id="8a722-103">Rotazione di colori</span><span class="sxs-lookup"><span data-stu-id="8a722-103">Rotating Colors</span></span>

<span data-ttu-id="8a722-104">La rotazione in uno spazio di colore a quattro dimensioni è difficile da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="8a722-104">Rotation in a four-dimensional color space is difficult to visualize.</span></span> <span data-ttu-id="8a722-105">È possibile semplificare la visualizzazione della rotazione accettando che uno dei componenti del colore sia fisso.</span><span class="sxs-lookup"><span data-stu-id="8a722-105">We can make it easier to visualize rotation by agreeing to keep one of the color components fixed.</span></span> <span data-ttu-id="8a722-106">Si supponga di accettare di tenere il componente alfa fisso a 1 (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="8a722-106">Suppose we agree to keep the alpha component fixed at 1 (fully opaque).</span></span> <span data-ttu-id="8a722-107">Sarà quindi possibile visualizzare uno spazio colore tridimensionale con assi rossi, verdi e blu, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="8a722-107">Then we can visualize a three-dimensional color space with red, green, and blue axes as shown in the following illustration.</span></span>

![illustrazione di una visualizzazione prospettica di uno spazio colore tridimensionale con assi con etichetta rosso, verde e blu](images/recoloring03.png)

<span data-ttu-id="8a722-109">Un colore può essere considerato come un punto nello spazio 3D.</span><span class="sxs-lookup"><span data-stu-id="8a722-109">A color can be thought of as a point in 3-D space.</span></span> <span data-ttu-id="8a722-110">Ad esempio, il punto (1, 0, 0) nello spazio rappresenta il colore rosso e il punto (0, 1, 0) nello spazio rappresenta il colore verde.</span><span class="sxs-lookup"><span data-stu-id="8a722-110">For example, the point (1, 0, 0) in space represents the color red, and the point (0, 1, 0) in space represents the color green.</span></span>

<span data-ttu-id="8a722-111">Nella figura seguente viene illustrato il significato della rotazione del colore (1, 0, 0) tramite un angolo di 60 gradi nel piano Red-Green.</span><span class="sxs-lookup"><span data-stu-id="8a722-111">The following illustration shows what it means to rotate the color (1, 0, 0) through an angle of 60 degrees in the Red-Green plane.</span></span> <span data-ttu-id="8a722-112">La rotazione in un piano parallelo al piano di Red-Green può essere considerata come rotazione sull'asse blu.</span><span class="sxs-lookup"><span data-stu-id="8a722-112">Rotation in a plane parallel to the Red-Green plane can be thought of as rotation about the blue axis.</span></span>

![illustrazione che mostra il punto (1, 0, 0) ruotato di 60 gradi a (0,5, 0,866, 0)](images/recoloring04.png)

<span data-ttu-id="8a722-114">Nella figura seguente viene illustrato come inizializzare una matrice di colori per eseguire rotazioni su ognuno dei tre assi delle coordinate (rosso, verde, blu).</span><span class="sxs-lookup"><span data-stu-id="8a722-114">The following illustration shows how to initialize a color matrix to perform rotations about each of the three coordinate axes (red, green, blue).</span></span>

![illustrazione che mostra le matrici di colore che eseguono rotazioni su ognuno dei tre assi delle coordinate](images/recoloring05.png)

<span data-ttu-id="8a722-116">Nell'esempio seguente viene accettata un'immagine che corrisponde a un solo colore (1, 0, 0,6) e viene applicata una rotazione di 60 gradi sull'asse blu.</span><span class="sxs-lookup"><span data-stu-id="8a722-116">The following example takes an image that is all one color (1, 0, 0.6) and applies a 60-degree rotation about the blue axis.</span></span> <span data-ttu-id="8a722-117">L'angolo della rotazione viene eliminato in un piano parallelo al piano di Red-Green.</span><span class="sxs-lookup"><span data-stu-id="8a722-117">The angle of the rotation is swept out in a plane that is parallel to the Red-Green plane.</span></span>


```
Image            image(L"RotationInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
REAL             degrees = 60;
REAL             pi = acos(-1);  // the angle whose cosine is -1.
REAL             r = degrees * pi / 180;  // degrees to radians

ColorMatrix colorMatrix = {
   cos(r),  sin(r), 0.0f, 0.0f, 0.0f,
   -sin(r), cos(r), 0.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   1.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 1.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(130, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="8a722-118">Nell'illustrazione seguente viene mostrata l'immagine originale a sinistra e l'immagine ruotata a colori a destra.</span><span class="sxs-lookup"><span data-stu-id="8a722-118">The following illustration shows the original image on the left and the color-rotated image on the right.</span></span>

![illustrazione che mostra i rettangoli riempiti con l'immagine originale (violetto rosso) e l'immagine ruotata a colori (verde acqua)](images/colortrans5.png)

<span data-ttu-id="8a722-120">La rotazione dei colori eseguita nell'esempio di codice precedente può essere visualizzata come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8a722-120">The color rotation performed in the preceding code example can be visualized as follows.</span></span>

![illustrazione che mostra uno spazio colore 3D e il punto (1, 0, 0,6) ruotato di 60 gradi a (0,5, 0,866, 0,6)](images/recoloring06.png)

 

 



