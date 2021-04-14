---
description: L'attributo swapinputs specifica se scambiare gli input di transizione. Se il valore è TRUE, gli input vengono scambiati. Il valore predefinito è FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: Attributo swapinputs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e2f02c642283e90b994bcd1bfa9e05076a7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349066"
---
# <a name="swapinputs-attribute"></a><span data-ttu-id="95578-105">Attributo swapinputs</span><span class="sxs-lookup"><span data-stu-id="95578-105">swapinputs Attribute</span></span>

> [!Note]  
> <span data-ttu-id="95578-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="95578-106">\[Deprecated.</span></span> <span data-ttu-id="95578-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="95578-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="95578-108">L' `swapinputs` attributo specifica se scambiare gli input di transizione.</span><span class="sxs-lookup"><span data-stu-id="95578-108">The `swapinputs` attribute specifies whether to swap transition inputs.</span></span> <span data-ttu-id="95578-109">Se il valore è **true**, gli input vengono scambiati.</span><span class="sxs-lookup"><span data-stu-id="95578-109">If the value is **TRUE**, the inputs are swapped.</span></span> <span data-ttu-id="95578-110">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="95578-110">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="95578-111">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="95578-111">Possible Values</span></span>

<span data-ttu-id="95578-112">I valori seguenti sono definiti come TRUE: y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="95578-112">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="95578-113">I valori seguenti sono definiti come FALSE: n, N, f, F, 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="95578-113">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="95578-114">Si applica a</span><span class="sxs-lookup"><span data-stu-id="95578-114">Applies To</span></span>

[<span data-ttu-id="95578-115">**transizione**</span><span class="sxs-lookup"><span data-stu-id="95578-115">**transition**</span></span>](transition-element.md)

## <a name="remarks"></a><span data-ttu-id="95578-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="95578-116">Remarks</span></span>

<span data-ttu-id="95578-117">Per impostazione predefinita, una transizione procede dalla composizione di tutti i livelli di priorità inferiore al livello su cui risiede la transizione.</span><span class="sxs-lookup"><span data-stu-id="95578-117">By default, a transition proceeds from the composite of all lower-priority layers to the layer on which the transition resides.</span></span> <span data-ttu-id="95578-118">Se l' `swapinputs` attributo è 1, questa direzione è invertita.</span><span class="sxs-lookup"><span data-stu-id="95578-118">If the `swapinputs` attribute is 1, this direction is reversed.</span></span> <span data-ttu-id="95578-119">Per ulteriori informazioni sul modello di sovrapposizione utilizzato da DES, vedere [il modello di sequenza temporale](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="95578-119">For more information about the layering model used by DES, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="95578-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95578-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95578-121">Attributi XTL</span><span class="sxs-lookup"><span data-stu-id="95578-121">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="95578-122">**IAMTimelineTrans::SetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="95578-122">**IAMTimelineTrans::SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



