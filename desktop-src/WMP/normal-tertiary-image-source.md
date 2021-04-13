---
title: Origine normale dell'immagine terziaria
description: Origine normale dell'immagine terziaria
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Windows Media Player Mobile Skin, origine immagine pulsante
- interfacce, origine immagine pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, origine immagine
- origine immagine per interfacce, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396570"
---
# <a name="normal-tertiary-image-source"></a><span data-ttu-id="9bf8e-108">Origine normale dell'immagine terziaria</span><span class="sxs-lookup"><span data-stu-id="9bf8e-108">Normal Tertiary Image Source</span></span>

<span data-ttu-id="9bf8e-109">Per la funzione del pulsante PlayPauseStop è necessario definire il percorso dell'immagine normale per lo stato terziario del pulsante.</span><span class="sxs-lookup"><span data-stu-id="9bf8e-109">The PlayPauseStop button function requires that you define the location of the normal image for the tertiary state of the button.</span></span> <span data-ttu-id="9bf8e-110">Si tratta dell'immagine visualizzata dagli utenti dopo aver premuto il pulsante PlayPauseStop per avviare lo streaming di una trasmissione live.</span><span class="sxs-lookup"><span data-stu-id="9bf8e-110">This will be the image users see after they have pushed the PlayPauseStop button to begin streaming a live broadcast.</span></span>

<span data-ttu-id="9bf8e-111">Per definire questa immagine, è necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio.</span><span class="sxs-lookup"><span data-stu-id="9bf8e-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="9bf8e-112">È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine che si vuole usare all'interno del tipo di bitmap da cui si sta disegnando.</span><span class="sxs-lookup"><span data-stu-id="9bf8e-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="9bf8e-113">Ad esempio, per definire l'immagine normale per un'origine di un'immagine terziaria, se l'immagine si trova all'interno della bitmap di cui è stato eseguito il push, digitare:</span><span class="sxs-lookup"><span data-stu-id="9bf8e-113">For example, to define the normal image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 286,0

```



<span data-ttu-id="9bf8e-114">Gli Stati terziari non possono avere un'immagine disabilitata.</span><span class="sxs-lookup"><span data-stu-id="9bf8e-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="9bf8e-115">Si presuppone che le immagini terziarie siano della stessa larghezza e altezza delle immagini primarie e secondarie.</span><span class="sxs-lookup"><span data-stu-id="9bf8e-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bf8e-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bf8e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bf8e-117">**Pulsanti**</span><span class="sxs-lookup"><span data-stu-id="9bf8e-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




