---
description: L'attributo PreviewMode specifica la modalità di anteprima per il gruppo. Se il valore è TRUE, i frame potrebbero essere eliminati durante l'anteprima. In caso contrario, non viene eliminato alcun frame durante l'anteprima. Il valore predefinito è TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: Attributo PreviewMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3b589b279a11b8ec329641ea2522a6a46dfa0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401199"
---
# <a name="previewmode-attribute"></a><span data-ttu-id="e0eee-106">Attributo PreviewMode</span><span class="sxs-lookup"><span data-stu-id="e0eee-106">previewmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="e0eee-107">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e0eee-107">\[Deprecated.</span></span> <span data-ttu-id="e0eee-108">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e0eee-108">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e0eee-109">L' `previewmode` attributo specifica la modalità di anteprima per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="e0eee-109">The `previewmode` attribute specifies the preview mode for the group.</span></span> <span data-ttu-id="e0eee-110">Se il valore è **true**, i frame potrebbero essere eliminati durante l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="e0eee-110">If the value is **TRUE**, frames might be dropped during preview.</span></span> <span data-ttu-id="e0eee-111">In caso contrario, non viene eliminato alcun frame durante l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="e0eee-111">Otherwise, no frames are dropped during preview.</span></span> <span data-ttu-id="e0eee-112">Il valore predefinito è **true**.</span><span class="sxs-lookup"><span data-stu-id="e0eee-112">The default value is **TRUE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="e0eee-113">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="e0eee-113">Possible Values</span></span>

<span data-ttu-id="e0eee-114">I valori seguenti sono definiti come TRUE: y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="e0eee-114">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="e0eee-115">I valori seguenti sono definiti come FALSE: n, N, f, F, 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e0eee-115">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e0eee-116">Si applica a</span><span class="sxs-lookup"><span data-stu-id="e0eee-116">Applies To</span></span>

[<span data-ttu-id="e0eee-117">**gruppo**</span><span class="sxs-lookup"><span data-stu-id="e0eee-117">**group**</span></span>](group-element.md)

## <a name="remarks"></a><span data-ttu-id="e0eee-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0eee-118">Remarks</span></span>

<span data-ttu-id="e0eee-119">Con l'impostazione predefinita, i frame vengono rilasciati durante l'anteprima degli effetti o delle transizioni lente, per sincronizzare il video con l'audio.</span><span class="sxs-lookup"><span data-stu-id="e0eee-119">Under the default setting, frames are dropped while previewing slow effects or transitions, to keep the video synchronized with the audio.</span></span> <span data-ttu-id="e0eee-120">Il video potrebbe sembrare frammentato come risultato.</span><span class="sxs-lookup"><span data-stu-id="e0eee-120">The video might look choppy as a result.</span></span> <span data-ttu-id="e0eee-121">Se si imposta questo attributo su **false** , viene eseguito il rendering di ogni fotogramma durante l'anteprima, causando probabilmente la mancata sincronizzazione del video con l'audio.</span><span class="sxs-lookup"><span data-stu-id="e0eee-121">Setting this attribute to **FALSE** forces every frame to render during preview, possibly resulting in the video becoming out of sync with the audio.</span></span> <span data-ttu-id="e0eee-122">I frame non vengono mai eliminati durante la scrittura in un file.</span><span class="sxs-lookup"><span data-stu-id="e0eee-122">Frames are never dropped when writing to a file.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0eee-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0eee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0eee-124">Attributi XTL</span><span class="sxs-lookup"><span data-stu-id="e0eee-124">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="e0eee-125">**IAMTimelineGroup:: SetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="e0eee-125">**IAMTimelineGroup::SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



