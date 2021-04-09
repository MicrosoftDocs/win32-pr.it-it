---
title: Transizioni di immagini video
description: Transizioni di immagini video
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Media Format SDK, transizioni di immagini video
- ASF (Advanced Systems Format), transizioni di immagini video
- ASF (Advanced Systems Format), transizioni di immagini video
- transizioni di immagini video
- Codec Windows Media Video 9 image V2
- codecs, Windows Media Video 9 image V2 codec
- flussi video, codec Windows Media Video 9 image V2
- flussi video, transizioni di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfd02628a78196a73750c2c0ff6b9e9c3d6729c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044522"
---
# <a name="video-image-transitions"></a><span data-ttu-id="f80c5-111">Transizioni di immagini video</span><span class="sxs-lookup"><span data-stu-id="f80c5-111">Video Image Transitions</span></span>

<span data-ttu-id="f80c5-112">Il codec Windows Media Video 9 image V2 aggiunge un'animazione a una serie di immagini, ottenendo così un flusso video.</span><span class="sxs-lookup"><span data-stu-id="f80c5-112">The Windows Media Video 9 Image v2 codec animates a series of images, resulting in a video stream.</span></span> <span data-ttu-id="f80c5-113">Il codec può manipolare due immagini contemporaneamente, fondendole insieme e creando una transizione da una all'altra in base alla configurazione fornita.</span><span class="sxs-lookup"><span data-stu-id="f80c5-113">The codec can manipulate two images at once, blending them together and creating a transition from one to the other according to the configuration you supply.</span></span> <span data-ttu-id="f80c5-114">Questa sezione descrive le transizioni supportate e i parametri necessari.</span><span class="sxs-lookup"><span data-stu-id="f80c5-114">This section describes the supported transitions and the parameters they require.</span></span>

<span data-ttu-id="f80c5-115">Le transizioni sono elencate nella tabella seguente in base agli identificatori globali.</span><span class="sxs-lookup"><span data-stu-id="f80c5-115">The transitions are listed in the following table by their global identifiers.</span></span>



| <span data-ttu-id="f80c5-116">Identificatore di transizione</span><span class="sxs-lookup"><span data-stu-id="f80c5-116">Transition identifier</span></span>                                                                           | <span data-ttu-id="f80c5-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f80c5-117">Description</span></span>                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f80c5-118">**WMT \_ VIDEOIMAGE \_ Transition \_ Papillon \_**</span><span class="sxs-lookup"><span data-stu-id="f80c5-118">**WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE**</span></span>](wmt-videoimage-transition-bow-tie.md)              | <span data-ttu-id="f80c5-119">La nuova immagine viene rivelata in un set di triangoli sui lati opposti del frame.</span><span class="sxs-lookup"><span data-stu-id="f80c5-119">New image is revealed in a set of triangles on opposite sides of the frame.</span></span>                                                                  |
| [<span data-ttu-id="f80c5-120">**\_cerchio di \_ transizione \_ VIDEOIMAGE di WMT**</span><span class="sxs-lookup"><span data-stu-id="f80c5-120">**WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE**</span></span>](wmt-videoimage-transition-circle.md)                 | <span data-ttu-id="f80c5-121">La nuova immagine viene rivelata in un cerchio.</span><span class="sxs-lookup"><span data-stu-id="f80c5-121">New image is revealed in a circle.</span></span>                                                                                                           |
| [<span data-ttu-id="f80c5-122">**\_ \_ \_ dissolvenza incrociata transizione VIDEOIMAGE WMT \_**</span><span class="sxs-lookup"><span data-stu-id="f80c5-122">**WMT\_VIDEOIMAGE\_TRANSITION\_CROSS\_FADE**</span></span>](wmt-videoimage-transition-cross-fade.md)        | <span data-ttu-id="f80c5-123">Nessuna transizione speciale, i coefficienti di Blend delle due immagini determinano la dissolvenza incrociata (dissolvenza).</span><span class="sxs-lookup"><span data-stu-id="f80c5-123">No special transition, the blend coefficients of the two images determine the cross-fade (dissolve).</span></span>                                         |
| [<span data-ttu-id="f80c5-124">**\_ \_ diagonale transizione VIDEOIMAGE WMT \_**</span><span class="sxs-lookup"><span data-stu-id="f80c5-124">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL**</span></span>](wmt-videoimage-transition-diagonal.md)             | <span data-ttu-id="f80c5-125">Viene rilevata una nuova immagine lungo una linea diagonale che ha origine in un angolo del frame.</span><span class="sxs-lookup"><span data-stu-id="f80c5-125">New image is revealed along a diagonal line originating in one corner of the frame.</span></span>                                                          |
| [<span data-ttu-id="f80c5-126">**WMT \_ VIDEOIMAGE \_ Transition \_ Diamond**</span><span class="sxs-lookup"><span data-stu-id="f80c5-126">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAMOND**</span></span>](wmt-videoimage-transition-diamond.md)               | <span data-ttu-id="f80c5-127">La nuova immagine viene rivelata in un rombo.</span><span class="sxs-lookup"><span data-stu-id="f80c5-127">New image is revealed in a diamond.</span></span>                                                                                                          |
| [<span data-ttu-id="f80c5-128">**\_ \_ dissolvenza WMT VIDEOIMAGE transizione \_ \_ a \_ colore**</span><span class="sxs-lookup"><span data-stu-id="f80c5-128">**WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR**</span></span>](wmt-videoimage-transition-fade-to-color.md) | <span data-ttu-id="f80c5-129">Viene risolto dall'immagine in un frame di colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="f80c5-129">Dissolves from the image to a frame of solid color.</span></span>                                                                                          |
| [<span data-ttu-id="f80c5-130">**WMT \_ VIDEOIMAGE \_ - \_ riempimento della transizione \_**</span><span class="sxs-lookup"><span data-stu-id="f80c5-130">**WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V**</span></span>](wmt-videoimage-transition-filled-v.md)            | <span data-ttu-id="f80c5-131">La nuova immagine viene rivelata in un triangolo originato da un lato del frame.</span><span class="sxs-lookup"><span data-stu-id="f80c5-131">New image is revealed in a triangle originating from one side of the frame.</span></span>                                                                  |
| [<span data-ttu-id="f80c5-132">**WMT \_ VIDEOIMAGE \_ transizione \_ Flip**</span><span class="sxs-lookup"><span data-stu-id="f80c5-132">**WMT\_VIDEOIMAGE\_TRANSITION\_FLIP**</span></span>](wmt-videoimage-transition-flip.md)                     | <span data-ttu-id="f80c5-133">L'immagine precedente viene ruotata su un asse y attraverso il centro del frame.</span><span class="sxs-lookup"><span data-stu-id="f80c5-133">Old image is rotated on a y-axis through the center of the frame.</span></span> <span data-ttu-id="f80c5-134">La nuova immagine viene rivelata come parte posteriore dell'immagine precedente.</span><span class="sxs-lookup"><span data-stu-id="f80c5-134">The new image is revealed as the back of the old image.</span></span>                    |
| [<span data-ttu-id="f80c5-135">**\_Insert WMT VIDEOIMAGE \_ Transition \_**</span><span class="sxs-lookup"><span data-stu-id="f80c5-135">**WMT\_VIDEOIMAGE\_TRANSITION\_INSET**</span></span>](wmt-videoimage-transition-inset.md)                   | <span data-ttu-id="f80c5-136">La nuova immagine viene rivelata da un rettangolo originato da un angolo del frame.</span><span class="sxs-lookup"><span data-stu-id="f80c5-136">New image is revealed by a rectangle originating from one corner of the frame.</span></span>                                                               |
| [<span data-ttu-id="f80c5-137">**\_ \_ Iris transizione VIDEOIMAGE \_ WMT**</span><span class="sxs-lookup"><span data-stu-id="f80c5-137">**WMT\_VIDEOIMAGE\_TRANSITION\_IRIS**</span></span>](wmt-videoimage-transition-iris.md)                     | <span data-ttu-id="f80c5-138">Viene rilevata una nuova immagine lungo un asse x e un asse y.</span><span class="sxs-lookup"><span data-stu-id="f80c5-138">New image is revealed along an x-axis and a y-axis.</span></span>                                                                                          |
| [<span data-ttu-id="f80c5-139">**\_ \_ \_ Roll pagina transizione VIDEOIMAGE \_ di WMT**</span><span class="sxs-lookup"><span data-stu-id="f80c5-139">**WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL**</span></span>](wmt-videoimage-transition-page-roll.md)          | <span data-ttu-id="f80c5-140">L'immagine precedente viene trasformata in un effetto di capovolgimento della pagina, mostrando la nuova immagine sotto.</span><span class="sxs-lookup"><span data-stu-id="f80c5-140">Old image is transformed in a page-flipping effect, revealing the new image underneath.</span></span>                                                      |
| [<span data-ttu-id="f80c5-141">**\_rettangolo di \_ transizione \_ VIDEOIMAGE di WMT**</span><span class="sxs-lookup"><span data-stu-id="f80c5-141">**WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE**</span></span>](wmt-videoimage-transition-rectangle.md)           | <span data-ttu-id="f80c5-142">La nuova immagine viene rivelata da un rettangolo all'interno del frame.</span><span class="sxs-lookup"><span data-stu-id="f80c5-142">New image is revealed by a rectangle within the frame.</span></span>                                                                                       |
| [<span data-ttu-id="f80c5-143">**WMT \_ VIDEOIMAGE \_ transizione \_**</span><span class="sxs-lookup"><span data-stu-id="f80c5-143">**WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL**</span></span>](wmt-videoimage-transition-reveal.md)                 | <span data-ttu-id="f80c5-144">La nuova immagine viene rivelata lungo una linea retta originata da un lato del frame.</span><span class="sxs-lookup"><span data-stu-id="f80c5-144">New image is revealed along a straight line originating from one side of the frame.</span></span>                                                          |
| [<span data-ttu-id="f80c5-145">**\_diapositiva di \_ transizione \_ VIDEOIMAGE di WMT**</span><span class="sxs-lookup"><span data-stu-id="f80c5-145">**WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE**</span></span>](wmt-videoimage-transition-slide.md)                   | <span data-ttu-id="f80c5-146">L'immagine precedente viene spostata all'esterno del frame, mostrando la nuova immagine sotto.</span><span class="sxs-lookup"><span data-stu-id="f80c5-146">Old image slides out of the frame, revealing the new image underneath.</span></span>                                                                       |
| [<span data-ttu-id="f80c5-147">**\_ \_ divisione transizione VIDEOIMAGE di WMT \_**</span><span class="sxs-lookup"><span data-stu-id="f80c5-147">**WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT**</span></span>](wmt-videoimage-transition-split.md)                   | <span data-ttu-id="f80c5-148">La nuova immagine viene rivelata da una suddivisione orizzontale o verticale nell'immagine precedente.</span><span class="sxs-lookup"><span data-stu-id="f80c5-148">New image is revealed by a horizontal or vertical split in the old image.</span></span> <span data-ttu-id="f80c5-149">La divisione viene visualizzata lungo una linea retta che inizia all'interno del frame.</span><span class="sxs-lookup"><span data-stu-id="f80c5-149">The split appears along a straight line starting inside the frame.</span></span> |
| [<span data-ttu-id="f80c5-150">**\_stella della \_ transizione \_ VIDEOIMAGE di WMT**</span><span class="sxs-lookup"><span data-stu-id="f80c5-150">**WMT\_VIDEOIMAGE\_TRANSITION\_STAR**</span></span>](wmt-videoimage-transition-star.md)                     | <span data-ttu-id="f80c5-151">La nuova immagine viene rivelata da una stella a cinque punte all'interno del frame.</span><span class="sxs-lookup"><span data-stu-id="f80c5-151">New image is revealed by a five-pointed star inside the frame.</span></span>                                                                               |
| [<span data-ttu-id="f80c5-152">**\_ \_ rotellina di transizione VIDEOIMAGE di WMT \_**</span><span class="sxs-lookup"><span data-stu-id="f80c5-152">**WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL**</span></span>](wmt-videoimage-transition-wheel.md)                   | <span data-ttu-id="f80c5-153">La nuova immagine viene rivelata da quattro spoke rotanti con un punto di perno comune.</span><span class="sxs-lookup"><span data-stu-id="f80c5-153">New image is revealed by four rotating spokes with a common pivot point.</span></span>                                                                     |



 

<span data-ttu-id="f80c5-154">Ogni transizione è descritta in modo completo in un argomento.</span><span class="sxs-lookup"><span data-stu-id="f80c5-154">Each transition is fully described in its own topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f80c5-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f80c5-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f80c5-156">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="f80c5-156">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="f80c5-157">**WMT \_ VIDEOIMAGE \_ SAMPLE2**</span><span class="sxs-lookup"><span data-stu-id="f80c5-157">**WMT\_VIDEOIMAGE\_SAMPLE2**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




