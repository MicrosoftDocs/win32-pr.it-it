---
description: L'attributo cutpoint specifica quando una transizione passa da un'origine all'altra, se viene eseguito il rendering della transizione come taglia. Il valore è relativo all'inizio della transizione.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: Attributo cutpoint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd516bd67577906a0a06d8da692ffbd7563ce32f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124596"
---
# <a name="cutpoint-attribute"></a><span data-ttu-id="82f1f-104">Attributo cutpoint</span><span class="sxs-lookup"><span data-stu-id="82f1f-104">cutpoint Attribute</span></span>

> [!Note]  
> <span data-ttu-id="82f1f-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="82f1f-105">\[Deprecated.</span></span> <span data-ttu-id="82f1f-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="82f1f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="82f1f-107">L' `cutpoint` attributo specifica quando una transizione passa da un'origine all'altra, se viene eseguito il rendering della transizione come taglia.</span><span class="sxs-lookup"><span data-stu-id="82f1f-107">The `cutpoint` attribute specifies when a transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="82f1f-108">Il valore è relativo all'inizio della transizione.</span><span class="sxs-lookup"><span data-stu-id="82f1f-108">The value is relative to the start of the transition.</span></span>

## <a name="possible-values"></a><span data-ttu-id="82f1f-109">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="82f1f-109">Possible Values</span></span>

<span data-ttu-id="82f1f-110">Deve essere una stringa con formato *hh: mm: SS. FF* , dove *HH* = hours, *mm* = minutes, *SS* = seconds e *FF* = frazioni di secondi.</span><span class="sxs-lookup"><span data-stu-id="82f1f-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="82f1f-111">Esempio: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="82f1f-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="82f1f-112">È possibile omettere le unità iniziali.</span><span class="sxs-lookup"><span data-stu-id="82f1f-112">Leading units can be omitted.</span></span> <span data-ttu-id="82f1f-113">Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.</span><span class="sxs-lookup"><span data-stu-id="82f1f-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="82f1f-114">Si applica a</span><span class="sxs-lookup"><span data-stu-id="82f1f-114">Applies To</span></span>

[<span data-ttu-id="82f1f-115">**transizione**</span><span class="sxs-lookup"><span data-stu-id="82f1f-115">**transition**</span></span>](transition-element.md)

## <a name="see-also"></a><span data-ttu-id="82f1f-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82f1f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f1f-117">Attributi XTL</span><span class="sxs-lookup"><span data-stu-id="82f1f-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="82f1f-118">**IAMTimelineTrans::SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="82f1f-118">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



