---
title: Informazioni sul plug-in DSP video di esempio
description: Informazioni sul plug-in DSP video di esempio
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- Plug-in di Windows Media Player, esempi
- plug-in, esempi
- plug-in di elaborazione dei segnali digitali, esempi
- Plug-in DSP, esempi
- Plug-in di Windows Media Player, video DSP
- plug-in, video DSP
- plug-in per l'elaborazione di segnali digitali, esempi video
- Plug-in DSP, esempi video
- esempi, plug-in DSP
- plug-in di video DSP, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede2eda82c834cefad0e31009805f24941cd4a6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297825"
---
# <a name="about-the-sample-video-dsp-plug-in"></a><span data-ttu-id="3d8ec-113">Informazioni sul plug-in DSP video di esempio</span><span class="sxs-lookup"><span data-stu-id="3d8ec-113">About the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="3d8ec-114">Il plug-in video DSP di esempio fornisce una semplice implementazione di elaborazione che consente di ridimensionare la saturazione dei colori del video in base a un fattore fornito dall'utente nella pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-114">The sample video DSP plug-in provides a simple processing implementation that scales the color saturation of the video by a factor provided by the user in the property page.</span></span> <span data-ttu-id="3d8ec-115">Il plug-in accetta valori compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="3d8ec-116">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-116">The default value is 1.</span></span> <span data-ttu-id="3d8ec-117">Il valore 1 non ha alcun effetto sull'immagine video; altri fattori di scala desaturano il colore dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-117">A value of 1 has no effect upon the video image; other scale factors desaturate the image color.</span></span> <span data-ttu-id="3d8ec-118">Ad esempio, un valore di 0,5 comporterà una saturazione di colore del 50%.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-118">For instance, a value of .5 would result in 50 percent color saturation.</span></span> <span data-ttu-id="3d8ec-119">Il valore zero restituisce il video in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-119">A value of zero results in grayscale video.</span></span>

<span data-ttu-id="3d8ec-120">Il plug-in video DSP di esempio funziona con i formati video seguenti:</span><span class="sxs-lookup"><span data-stu-id="3d8ec-120">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="3d8ec-121">NV12</span><span class="sxs-lookup"><span data-stu-id="3d8ec-121">NV12</span></span>
-   <span data-ttu-id="3d8ec-122">YV12</span><span class="sxs-lookup"><span data-stu-id="3d8ec-122">YV12</span></span>
-   <span data-ttu-id="3d8ec-123">YUY2</span><span class="sxs-lookup"><span data-stu-id="3d8ec-123">YUY2</span></span>
-   <span data-ttu-id="3d8ec-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="3d8ec-124">UYVY</span></span>
-   <span data-ttu-id="3d8ec-125">RGB32</span><span class="sxs-lookup"><span data-stu-id="3d8ec-125">RGB32</span></span>
-   <span data-ttu-id="3d8ec-126">RGB24</span><span class="sxs-lookup"><span data-stu-id="3d8ec-126">RGB24</span></span>
-   <span data-ttu-id="3d8ec-127">RGB555</span><span class="sxs-lookup"><span data-stu-id="3d8ec-127">RGB555</span></span>
-   <span data-ttu-id="3d8ec-128">RGB565</span><span class="sxs-lookup"><span data-stu-id="3d8ec-128">RGB565</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d8ec-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3d8ec-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d8ec-130">**Creazione di un plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="3d8ec-130">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




