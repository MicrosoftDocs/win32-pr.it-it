---
title: Origine immagine secondaria push
description: Origine immagine secondaria push
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Windows Media Player Mobile Skin, origine immagine pulsante
- interfacce, origine immagine pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, origine immagine
- origine immagine per interfacce, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de50f72c8af34fa4f3e44507e172cae6890dc47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044789"
---
# <a name="pushed-secondary-image-source"></a><span data-ttu-id="13b5c-108">Origine immagine secondaria push</span><span class="sxs-lookup"><span data-stu-id="13b5c-108">Pushed Secondary Image Source</span></span>

<span data-ttu-id="13b5c-109">A seconda della funzione Button, potrebbe essere necessario definire il percorso dell'immagine push per lo stato secondario del pulsante.</span><span class="sxs-lookup"><span data-stu-id="13b5c-109">Depending on the button function, you may need to define the location of the pushed image for the secondary state of the button.</span></span> <span data-ttu-id="13b5c-110">Si tratta dell'immagine visualizzata dagli utenti quando eseguono il push di un pulsante della funzione come playpause la seconda volta.</span><span class="sxs-lookup"><span data-stu-id="13b5c-110">This will be the image users see when they push a PlayPause function button the second time.</span></span>

<span data-ttu-id="13b5c-111">Per definire questa immagine, è necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio.</span><span class="sxs-lookup"><span data-stu-id="13b5c-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="13b5c-112">È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine che si vuole usare all'interno del tipo di immagine da cui si sta disegnando.</span><span class="sxs-lookup"><span data-stu-id="13b5c-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the image type you are drawing from.</span></span>

<span data-ttu-id="13b5c-113">Ad esempio, per definire l'immagine push per un'origine di un'immagine secondaria, se l'immagine si trova all'interno della bitmap di cui è stato eseguito il push, digitare:</span><span class="sxs-lookup"><span data-stu-id="13b5c-113">For example, to define the Pushed image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 248,0

```



<span data-ttu-id="13b5c-114">Gli stati secondari non possono avere un'immagine disabilitata.</span><span class="sxs-lookup"><span data-stu-id="13b5c-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="13b5c-115">Si presuppone che le immagini secondarie siano della stessa larghezza e altezza dell'immagine principale.</span><span class="sxs-lookup"><span data-stu-id="13b5c-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13b5c-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13b5c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13b5c-117">**Pulsanti**</span><span class="sxs-lookup"><span data-stu-id="13b5c-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




