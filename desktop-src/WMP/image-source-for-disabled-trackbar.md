---
title: Origine immagine per TrackBar disabilitato
description: Origine immagine per TrackBar disabilitato
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Windows Media Player Mobile Skins, trackbars
- interfacce, TrackBar
- riferimento per Skin, trackbars
- TrackBar in interfacce, origine immagine
- origine immagine per Skin, trackbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298237"
---
# <a name="image-source-for-disabled-trackbar"></a><span data-ttu-id="3bd4f-108">Origine immagine per TrackBar disabilitato</span><span class="sxs-lookup"><span data-stu-id="3bd4f-108">Image Source for Disabled Trackbar</span></span>

<span data-ttu-id="3bd4f-109">È necessario definire l'origine dell'immagine che si desidera visualizzare quando un TrackBar è disabilitato, utilizzando il tipo di bitmap da cui si desidera creare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-109">You must define the source of the image you want to display when a trackbar is disabled, using the bitmap type you want to draw the image from.</span></span> <span data-ttu-id="3bd4f-110">L'immagine visualizzata si trova in genere all'interno del file con privilegi avanzati o se si sta creando un'interfaccia per Windows Media Player 10 Mobile, l'immagine si trova all'interno del file SeekThumb.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-110">The image you display will usually be inside the Super file or if you are creating a skin for Windows Media Player 10 Mobile, the image would be inside the SeekThumb file.</span></span> <span data-ttu-id="3bd4f-111">È necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="3bd4f-112">È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine che si vuole usare all'interno del tipo di bitmap da cui si sta disegnando.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="3bd4f-113">Ad esempio, per usare un'immagine dalla bitmap SeekThumb con una posizione superiore e sinistra di 50, 60 pixel, digitare:</span><span class="sxs-lookup"><span data-stu-id="3bd4f-113">For example, to use an image from the SeekThumb bitmap that has a top and left position of 50,60 pixels, type:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="3bd4f-114">È necessario definire un percorso immagine per un'immagine TrackBar disabilitata.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-114">You must define an image location for a disabled trackbar image.</span></span> <span data-ttu-id="3bd4f-115">Se non si vuole visualizzare una nuova immagine, è possibile definire l'immagine di sfondo come immagine disabilitata con un offset di 0, 0:</span><span class="sxs-lookup"><span data-stu-id="3bd4f-115">If you do not want to display a new image, you can define the Background image as your Disabled image with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="3bd4f-116">Nell'esempio precedente, 50, 60 rappresenta la posizione del pulsante che si sta utilizzando nel file SeekThumb (in questo caso, la stessa posizione del pulsante nella bitmap di sfondo).</span><span class="sxs-lookup"><span data-stu-id="3bd4f-116">In the preceding example, 50,60 represents the location of the button you are working with in the SeekThumb file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="3bd4f-117">Tuttavia, si consiglia di visualizzare un'immagine disabilitata per tutti i TrackBar per fornire all'utente un'indicazione visiva, perché i TrackBar non saranno utilizzabili in determinate condizioni.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-117">However, it is highly recommended that you display a Disabled image for all trackbars to give your user a visual indication, because trackbars will not be useable under certain conditions.</span></span> <span data-ttu-id="3bd4f-118">Ad esempio, la ricerca di TrackBar può essere disabilitata quando la playlist corrente è vuota.</span><span class="sxs-lookup"><span data-stu-id="3bd4f-118">For example, Seek trackbars may be disabled when the current playlist is empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bd4f-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3bd4f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bd4f-120">**TrackBar**</span><span class="sxs-lookup"><span data-stu-id="3bd4f-120">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 




