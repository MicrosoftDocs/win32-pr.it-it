---
title: Origine dell'immagine terziaria push
description: Origine dell'immagine terziaria push
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Windows Media Player Mobile Skin, origine immagine pulsante
- interfacce, origine immagine pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, origine immagine
- origine immagine per interfacce, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a37f79ab3c5fbf02eed1f0a02219a517b12ce1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955495"
---
# <a name="pushed-tertiary-image-source"></a><span data-ttu-id="cf552-108">Origine dell'immagine terziaria push</span><span class="sxs-lookup"><span data-stu-id="cf552-108">Pushed Tertiary Image Source</span></span>

<span data-ttu-id="cf552-109">Per la funzione del pulsante PlayPauseStop è necessario definire il percorso dell'immagine push per lo stato terziario del pulsante.</span><span class="sxs-lookup"><span data-stu-id="cf552-109">The PlayPauseStop button function requires that you define the location of the pushed image for the tertiary state of the button.</span></span> <span data-ttu-id="cf552-110">Si tratta dell'immagine visualizzata dagli utenti quando eseguono il push del pulsante PlayPauseStop durante lo streaming di una trasmissione live.</span><span class="sxs-lookup"><span data-stu-id="cf552-110">This will be the image users see when they push the PlayPauseStop button while streaming a live broadcast.</span></span>

<span data-ttu-id="cf552-111">Per definire questa immagine, è necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio.</span><span class="sxs-lookup"><span data-stu-id="cf552-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="cf552-112">È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine che si vuole usare all'interno del tipo di bitmap da cui si sta disegnando.</span><span class="sxs-lookup"><span data-stu-id="cf552-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="cf552-113">Ad esempio, per definire l'immagine push per un'origine di un'immagine terziaria, se l'immagine si trova all'interno della bitmap di cui è stato eseguito il push, digitare:</span><span class="sxs-lookup"><span data-stu-id="cf552-113">For example, to define the pushed image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 324,0

```



<span data-ttu-id="cf552-114">Gli Stati terziari non possono avere un'immagine disabilitata.</span><span class="sxs-lookup"><span data-stu-id="cf552-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="cf552-115">Si presuppone che le immagini terziarie siano della stessa larghezza e altezza delle immagini primarie e secondarie.</span><span class="sxs-lookup"><span data-stu-id="cf552-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf552-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cf552-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf552-117">**Pulsanti**</span><span class="sxs-lookup"><span data-stu-id="cf552-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




