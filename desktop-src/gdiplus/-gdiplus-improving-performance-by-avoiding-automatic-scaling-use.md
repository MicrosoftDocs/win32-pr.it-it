---
description: Se si passa solo l'angolo superiore sinistro di un'immagine al metodo DrawImage, Windows GDI+ potrebbe ridimensionare l'immagine, riducendo le prestazioni.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Miglioramento delle prestazioni evitando il ridimensionamento automatico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b505043bf8a303a58c6fc5936a31d794052c78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979007"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a><span data-ttu-id="e4a69-103">Miglioramento delle prestazioni evitando il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="e4a69-103">Improving Performance by Avoiding Automatic Scaling</span></span>

<span data-ttu-id="e4a69-104">Se si passa solo l'angolo superiore sinistro di un'immagine al metodo **DrawImage** , Windows GDI+ potrebbe ridimensionare l'immagine, riducendo le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e4a69-104">If you pass only the upper-left corner of an image to the **DrawImage** method, Windows GDI+ might scale the image, which would decrease performance.</span></span>

<span data-ttu-id="e4a69-105">La chiamata seguente al metodo **DrawImage** specifica un angolo superiore sinistro di (50, 30) ma non specifica un rettangolo di destinazione:</span><span class="sxs-lookup"><span data-stu-id="e4a69-105">The following call to the **DrawImage** method specifies an upper-left corner of (50, 30) but does not specify a destination rectangle:</span></span>


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



<span data-ttu-id="e4a69-106">Sebbene si tratta della versione più semplice del metodo **DrawImage** in termini di numero di argomenti obbligatori, non è necessariamente il più efficiente.</span><span class="sxs-lookup"><span data-stu-id="e4a69-106">Although this is the easiest version of the **DrawImage** method in terms of the number of required arguments, it is not necessarily the most efficient.</span></span> <span data-ttu-id="e4a69-107">Se il numero di punti per pollice sul dispositivo di visualizzazione corrente è diverso dal numero di punti per pollice sul dispositivo in cui è stata creata l'immagine, GDI+ ridimensiona l'immagine in modo che le dimensioni fisiche sul dispositivo di visualizzazione corrente siano il più vicino possibile alle dimensioni fisiche del dispositivo in cui è stato creato.</span><span class="sxs-lookup"><span data-stu-id="e4a69-107">If the number of dots per inch on the current display device is different than the number of dots per inch on the device where the image was created, GDI+ scales the image so that its physical size on the current display device is as close as possible to its physical size on the device where it was created.</span></span>

<span data-ttu-id="e4a69-108">Se si desidera impedire tale scalabilità, passare la larghezza e l'altezza di un rettangolo di destinazione al metodo **DrawImage** .</span><span class="sxs-lookup"><span data-stu-id="e4a69-108">If you want to prevent such scaling, pass the width and height of a destination rectangle to the **DrawImage** method.</span></span> <span data-ttu-id="e4a69-109">Nell'esempio seguente viene disegnata due volte la stessa immagine.</span><span class="sxs-lookup"><span data-stu-id="e4a69-109">The following example draws the same image twice.</span></span> <span data-ttu-id="e4a69-110">Nel primo caso, la larghezza e l'altezza del rettangolo di destinazione non sono specificate e l'immagine viene ridimensionata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e4a69-110">In the first case, the width and height of the destination rectangle are not specified, and the image is automatically scaled.</span></span> <span data-ttu-id="e4a69-111">Nel secondo caso, la larghezza e l'altezza (misurate in pixel) del rettangolo di destinazione vengono specificate come la larghezza e l'altezza dell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="e4a69-111">In the second case, the width and height (measured in pixels) of the destination rectangle are specified to be the same as the width and height of the original image.</span></span>


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



<span data-ttu-id="e4a69-112">La figura seguente mostra il rendering dell'immagine due volte.</span><span class="sxs-lookup"><span data-stu-id="e4a69-112">The following illustration shows the image rendered twice.</span></span>

![Screenshot di una finestra che contiene due versioni di un'immagine a scale diverse](images/scaledtexture1.png)

 

 



