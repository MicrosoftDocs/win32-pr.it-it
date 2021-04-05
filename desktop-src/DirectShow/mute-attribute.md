---
description: L'attributo mute specifica lo stato di silenziamento dell'oggetto.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: Disattiva attributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124899"
---
# <a name="mute-attribute"></a><span data-ttu-id="41639-103">Disattiva attributo</span><span class="sxs-lookup"><span data-stu-id="41639-103">mute Attribute</span></span>

> [!Note]  
> <span data-ttu-id="41639-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="41639-104">\[Deprecated.</span></span> <span data-ttu-id="41639-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="41639-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="41639-106">L' `mute` attributo specifica lo stato di silenziamento dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="41639-106">The `mute` attribute specifies the object's mute state.</span></span> <span data-ttu-id="41639-107">Se il valore è **true**, né l'oggetto né i relativi elementi figlio vengono sottoposti a rendering.</span><span class="sxs-lookup"><span data-stu-id="41639-107">If the value is **TRUE**, neither the object nor its children are rendered.</span></span> <span data-ttu-id="41639-108">Se il valore è **false**, viene eseguito il rendering dell'oggetto e viene eseguito il rendering dei relativi elementi figlio in base al relativo stato di silenziamento.</span><span class="sxs-lookup"><span data-stu-id="41639-108">If the value is **FALSE**, the object is rendered, and its children are rendered according to their own mute state.</span></span> <span data-ttu-id="41639-109">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="41639-109">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="41639-110">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="41639-110">Possible Values</span></span>

<span data-ttu-id="41639-111">I valori seguenti sono definiti come TRUE: y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="41639-111">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="41639-112">I valori seguenti sono definiti come FALSE: n, N, f, F, 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="41639-112">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="41639-113">Si applica a</span><span class="sxs-lookup"><span data-stu-id="41639-113">Applies To</span></span>

<span data-ttu-id="41639-114">[**clip**](clip-element.md), [**composito**](composite-element.md), [**effetto**](effect-element.md), [**gruppo**](group-element.md), [**sequenza temporale**](timeline-element.md), [**transizione**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="41639-114">[**clip**](clip-element.md), [**composite**](composite-element.md), [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="41639-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41639-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41639-116">Attributi XTL</span><span class="sxs-lookup"><span data-stu-id="41639-116">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="41639-117">**IAMTimelineObj:: semutato**</span><span class="sxs-lookup"><span data-stu-id="41639-117">**IAMTimelineObj::SetMuted**</span></span>](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



