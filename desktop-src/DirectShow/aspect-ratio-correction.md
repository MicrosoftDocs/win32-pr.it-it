---
description: Correzione proporzioni
ms.assetid: 0ed6010b-9168-44b1-be49-0c9d5d77ce3f
title: Correzione proporzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2460f7ecce1513394d941eafe8bdf8a7a80e9727
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304209"
---
# <a name="aspect-ratio-correction"></a><span data-ttu-id="2739c-103">Correzione proporzioni</span><span class="sxs-lookup"><span data-stu-id="2739c-103">Aspect Ratio Correction</span></span>

<span data-ttu-id="2739c-104">Questo argomento si applica a Windows XP Service Pack 2 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2739c-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="2739c-105">In modalità di combinazione, il VMR ridimensiona il video con le proporzioni corrette.</span><span class="sxs-lookup"><span data-stu-id="2739c-105">In mixing mode, the VMR sizes the video to the correct aspect ratio.</span></span> <span data-ttu-id="2739c-106">(Eccezione: vedere [combinazione non quadrata](non-square-mixing.md)). Questa operazione può richiedere l'allungamento del video se le proporzioni preferite non corrispondono alle proporzioni fisiche dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2739c-106">(Exception: See [Non-Square Mixing](non-square-mixing.md).) This may require stretching the video if the preferred aspect ratio is not the same as the image's physical aspect ratio.</span></span> <span data-ttu-id="2739c-107">Il formato video digitale (DV), ad esempio, è 720 x 480 pixel (3:2), ma deve essere visualizzato con un rapporto di 4:3.</span><span class="sxs-lookup"><span data-stu-id="2739c-107">For example, digital video (DV) format is 720 x 480 pixels (3:2) but should be displayed at a 4:3 aspect ratio.</span></span>

<span data-ttu-id="2739c-108">VMR supporta due comportamenti diversi per la correzione di proporzioni:</span><span class="sxs-lookup"><span data-stu-id="2739c-108">The VMR supports two different behaviors for aspect ratio correction:</span></span>

-   <span data-ttu-id="2739c-109">Regolare la dimensione orizzontale o verticale, in modo che l'immagine venga sempre allungata, mai compattata.</span><span class="sxs-lookup"><span data-stu-id="2739c-109">Adjust either the horizontal or vertical size, so that the image is always stretched, never shrunk.</span></span> <span data-ttu-id="2739c-110">Questo è il comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="2739c-110">This is now the default behavior.</span></span>
-   <span data-ttu-id="2739c-111">Regolare le dimensioni orizzontali, ovvero l'estensione o la compattazione del video.</span><span class="sxs-lookup"><span data-stu-id="2739c-111">Adjust the horizontal size, either stretching or shrinking the video.</span></span>

<span data-ttu-id="2739c-112">Poiché il secondo comportamento (solo regolazione orizzontale) può comportare la compattazione del video, l'immagine di output potrebbe avere una risoluzione minore.</span><span class="sxs-lookup"><span data-stu-id="2739c-112">Because the second behavior (horizontal adjustment only) may entail shrinking the video, the output image may have less resolution.</span></span> <span data-ttu-id="2739c-113">Per questo motivo, è preferibile il primo comportamento.</span><span class="sxs-lookup"><span data-stu-id="2739c-113">For this reason, the first behavior is preferred.</span></span> <span data-ttu-id="2739c-114">Ad esempio, nel caso di 720 x 480 video alle proporzioni 4:3, il comportamento predefinito produce un'immagine 720 x 550, mentre la regolazione orizzontale produce un'immagine 640 x 480 più piccola.</span><span class="sxs-lookup"><span data-stu-id="2739c-114">For example, in the case of 720 x 480 video at 4:3 aspect ratio, the default behavior produces a 720 x 550 image, while horizontal adjustment produces a smaller 640 x 480 image.</span></span>

<span data-ttu-id="2739c-115">**VMR-7**: per impostare la preferenza di correzione delle proporzioni, chiamare [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect).</span><span class="sxs-lookup"><span data-stu-id="2739c-115">**VMR-7**: To set the aspect ratio correction preference, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect).</span></span> <span data-ttu-id="2739c-116">Impostare il \_ flag MixerPref ARAdjustXorY per il comportamento predefinito oppure deselezionare questo flag solo per la regolazione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="2739c-116">Set the MixerPref\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

<span data-ttu-id="2739c-117">**VMR-9**: per impostare la preferenza di correzione delle proporzioni, chiamare [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs).</span><span class="sxs-lookup"><span data-stu-id="2739c-117">**VMR-9**: To set the aspect ratio correction preference, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs).</span></span> <span data-ttu-id="2739c-118">Impostare il \_ flag MixerPref9 ARAdjustXorY per il comportamento predefinito oppure deselezionare questo flag solo per la regolazione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="2739c-118">Set the MixerPref9\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2739c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2739c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2739c-120">Uso della modalità di combinazione VMR</span><span class="sxs-lookup"><span data-stu-id="2739c-120">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



