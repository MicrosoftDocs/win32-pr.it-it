---
description: L'attributo Start specifica l'ora di inizio di un oggetto, relativa all'oggetto padre.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: Attributo Start
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b377d0d83c86b981400a784904cf0423f0cca20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316329"
---
# <a name="start-attribute"></a><span data-ttu-id="5677f-103">Attributo Start</span><span class="sxs-lookup"><span data-stu-id="5677f-103">start Attribute</span></span>

> [!Note]  
> <span data-ttu-id="5677f-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5677f-104">\[Deprecated.</span></span> <span data-ttu-id="5677f-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5677f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5677f-106">L' `start` attributo specifica l'ora di inizio di un oggetto, relativa all'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="5677f-106">The `start` attribute specifies the start time of an object, relative to the parent object.</span></span>

## <a name="possible-values"></a><span data-ttu-id="5677f-107">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="5677f-107">Possible Values</span></span>

<span data-ttu-id="5677f-108">Deve essere una stringa con formato *hh: mm: SS. FF* , dove *HH* = hours, *mm* = minutes, *SS* = seconds e *FF* = frazioni di secondi.</span><span class="sxs-lookup"><span data-stu-id="5677f-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="5677f-109">Esempio: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="5677f-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="5677f-110">È possibile omettere le unità iniziali.</span><span class="sxs-lookup"><span data-stu-id="5677f-110">Leading units can be omitted.</span></span> <span data-ttu-id="5677f-111">Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.</span><span class="sxs-lookup"><span data-stu-id="5677f-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5677f-112">Si applica a</span><span class="sxs-lookup"><span data-stu-id="5677f-112">Applies To</span></span>

<span data-ttu-id="5677f-113">[**clip**](clip-element.md), [**effetto**](effect-element.md), [**transizione**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="5677f-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="5677f-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5677f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5677f-115">Attributi XTL</span><span class="sxs-lookup"><span data-stu-id="5677f-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="5677f-116">**IAMTimelineObj::SetStartStop**</span><span class="sxs-lookup"><span data-stu-id="5677f-116">**IAMTimelineObj::SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



