---
title: Origine normale dell'immagine secondaria
description: Origine normale dell'immagine secondaria
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Windows Media Player Mobile Skin, origine immagine pulsante
- interfacce, origine immagine pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, origine immagine
- origine immagine per interfacce, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff828f6d0f0c8348453cb00fef04ab31718693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298702"
---
# <a name="normal-secondary-image-source"></a><span data-ttu-id="64ca7-108">Origine normale dell'immagine secondaria</span><span class="sxs-lookup"><span data-stu-id="64ca7-108">Normal Secondary Image Source</span></span>

<span data-ttu-id="64ca7-109">A seconda della funzione Button, potrebbe essere necessario definire il percorso dell'immagine normale per lo stato secondario del pulsante.</span><span class="sxs-lookup"><span data-stu-id="64ca7-109">Depending on the button function, you may need to define the location of the normal image for the secondary state of the button.</span></span> <span data-ttu-id="64ca7-110">Si tratta dell'immagine visualizzata dagli utenti quando eseguono il push di un pulsante della funzione come playpause la prima volta.</span><span class="sxs-lookup"><span data-stu-id="64ca7-110">This will be the image users see when they push a PlayPause function button the first time.</span></span>

<span data-ttu-id="64ca7-111">Per definire questa immagine, è necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio.</span><span class="sxs-lookup"><span data-stu-id="64ca7-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="64ca7-112">È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine che si vuole usare all'interno del tipo di bitmap da cui si sta disegnando.</span><span class="sxs-lookup"><span data-stu-id="64ca7-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="64ca7-113">Ad esempio, per definire l'immagine normale per un'origine di un'immagine secondaria, se l'immagine si trova all'interno della bitmap di cui è stato eseguito il push, digitare:</span><span class="sxs-lookup"><span data-stu-id="64ca7-113">For example, to define the normal image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 210,0

```



<span data-ttu-id="64ca7-114">Gli stati secondari non possono avere un'immagine disabilitata.</span><span class="sxs-lookup"><span data-stu-id="64ca7-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="64ca7-115">Si presuppone che le immagini secondarie siano della stessa larghezza e altezza dell'immagine principale.</span><span class="sxs-lookup"><span data-stu-id="64ca7-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64ca7-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64ca7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64ca7-117">**Pulsanti**</span><span class="sxs-lookup"><span data-stu-id="64ca7-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




