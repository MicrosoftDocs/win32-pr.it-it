---
description: È possibile ruotare, riflettere e inclinare un'immagine specificando punti di destinazione per gli angoli superiore sinistro, superiore destro e inferiore sinistro dell'immagine originale.
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: Rotazione, Reflection e inclinazione di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967198"
---
# <a name="rotating-reflecting-and-skewing-images"></a><span data-ttu-id="f17e1-103">Rotazione, Reflection e inclinazione di immagini</span><span class="sxs-lookup"><span data-stu-id="f17e1-103">Rotating, Reflecting, and Skewing Images</span></span>

<span data-ttu-id="f17e1-104">È possibile ruotare, riflettere e inclinare un'immagine specificando punti di destinazione per gli angoli superiore sinistro, superiore destro e inferiore sinistro dell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="f17e1-104">You can rotate, reflect, and skew an image by specifying destination points for the upper-left, upper-right, and lower-left corners of the original image.</span></span> <span data-ttu-id="f17e1-105">I tre punti di destinazione determinano una trasformazione affine che esegue il mapping dell'immagine rettangolare originale a un parallelogramma.</span><span class="sxs-lookup"><span data-stu-id="f17e1-105">The three destination points determine an affine transformation that maps the original rectangular image to a parallelogram.</span></span> <span data-ttu-id="f17e1-106">L'angolo inferiore destro dell'immagine originale viene mappato al quarto angolo del parallelogramma, che viene calcolato dai tre punti di destinazione specificati.</span><span class="sxs-lookup"><span data-stu-id="f17e1-106">(The lower-right corner of the original image is mapped to the fourth corner of the parallelogram, which is calculated from the three specified destination points.)</span></span>

<span data-ttu-id="f17e1-107">Si supponga, ad esempio, che l'immagine originale sia un rettangolo con angolo superiore sinistro in corrispondenza di (0, 0), angolo superiore destro in corrispondenza di (100, 0) e angolo inferiore sinistro in (0, 50).</span><span class="sxs-lookup"><span data-stu-id="f17e1-107">For example, suppose the original image is a rectangle with upper-left corner at (0, 0), upper-right corner at (100, 0), and lower-left corner at (0, 50).</span></span> <span data-ttu-id="f17e1-108">Si supponga ora di eseguire il mapping di questi tre punti ai punti di destinazione come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f17e1-108">Now suppose we map those three points to destination points as follows.</span></span>



| <span data-ttu-id="f17e1-109">Punto originale</span><span class="sxs-lookup"><span data-stu-id="f17e1-109">Original point</span></span>       | <span data-ttu-id="f17e1-110">Punto di destinazione</span><span class="sxs-lookup"><span data-stu-id="f17e1-110">Destination point</span></span> |
|----------------------|-------------------|
| <span data-ttu-id="f17e1-111">Superiore sinistro (0,0)</span><span class="sxs-lookup"><span data-stu-id="f17e1-111">Upper-left (0, 0)</span></span>    | <span data-ttu-id="f17e1-112">(200, 20)</span><span class="sxs-lookup"><span data-stu-id="f17e1-112">(200, 20)</span></span>         |
| <span data-ttu-id="f17e1-113">In alto a destra (100, 0)</span><span class="sxs-lookup"><span data-stu-id="f17e1-113">Upper-right (100, 0)</span></span> | <span data-ttu-id="f17e1-114">(110, 100)</span><span class="sxs-lookup"><span data-stu-id="f17e1-114">(110, 100)</span></span>        |
| <span data-ttu-id="f17e1-115">In basso a sinistra (0, 50)</span><span class="sxs-lookup"><span data-stu-id="f17e1-115">Lower-left (0, 50)</span></span>   | <span data-ttu-id="f17e1-116">(250, 30)</span><span class="sxs-lookup"><span data-stu-id="f17e1-116">(250, 30)</span></span>         |



 

<span data-ttu-id="f17e1-117">La figura seguente mostra l'immagine originale e l'immagine mappata al parallelogramma.</span><span class="sxs-lookup"><span data-stu-id="f17e1-117">The following illustration shows the original image and the image mapped to the parallelogram.</span></span> <span data-ttu-id="f17e1-118">L'immagine originale è stata inclinata, riflessa, ruotata e convertita.</span><span class="sxs-lookup"><span data-stu-id="f17e1-118">The original image has been skewed, reflected, rotated, and translated.</span></span> <span data-ttu-id="f17e1-119">L'asse x lungo il bordo superiore dell'immagine originale viene mappato alla riga che esegue fino a (200, 20) e (110, 100).</span><span class="sxs-lookup"><span data-stu-id="f17e1-119">The x-axis along the top edge of the original image is mapped to the line that runs through (200, 20) and (110, 100).</span></span> <span data-ttu-id="f17e1-120">L'asse y lungo il bordo sinistro dell'immagine originale viene mappato alla riga che esegue fino a (200, 20) e (250, 30).</span><span class="sxs-lookup"><span data-stu-id="f17e1-120">The y-axis along the left edge of the original image is mapped to the line that runs through (200, 20) and (250, 30).</span></span>

![illustrazione che mostra strisce colorate all'origine degli assi delle coordinate e le stesse strisce inclinate e in una posizione, una rotazione e una dimensione diverse](images/stripes1.png)

<span data-ttu-id="f17e1-122">Nell'esempio seguente vengono generate le immagini mostrate nella figura precedente.</span><span class="sxs-lookup"><span data-stu-id="f17e1-122">The following example produces the images shown in the preceding illustration.</span></span>


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



<span data-ttu-id="f17e1-123">Nella figura seguente viene illustrata una trasformazione simile applicata a un'immagine fotografica.</span><span class="sxs-lookup"><span data-stu-id="f17e1-123">The following illustration shows a similar transformation applied to a photographic image.</span></span>

![illustrazione che mostra la stessa foto due volte. il secondo è invertito, inclinato e ha dimensioni, rotazione e posizione diverse](images/transformedclimber.png)

<span data-ttu-id="f17e1-125">Nella figura seguente viene illustrata una trasformazione simile applicata a un metafile.</span><span class="sxs-lookup"><span data-stu-id="f17e1-125">The following illustration shows a similar transformation applied to a metafile.</span></span>

![illustrazione che mostra le forme e il testo, quindi ancora una volta invertita, asimmetrica e con posizioni, rotazione e dimensioni diverse](images/transformedmetafile.png)

 

 



