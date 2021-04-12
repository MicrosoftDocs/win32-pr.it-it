---
description: L'attributo time specifica l'ora in cui un parametro presuppone un nuovo valore, relativo all'inizio della transizione o dell'effetto.
ms.assetid: bb478215-cbd5-4fea-9d88-a1f2b002f3da
title: Time (attributo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15a84d40c5e38ed81f8c17cd2d931e3f85e389a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234205"
---
# <a name="time-attribute"></a><span data-ttu-id="1df83-103">Time (attributo)</span><span class="sxs-lookup"><span data-stu-id="1df83-103">time Attribute</span></span>

> [!Note]  
> <span data-ttu-id="1df83-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1df83-104">\[Deprecated.</span></span> <span data-ttu-id="1df83-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1df83-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1df83-106">L' `time` attributo specifica l'ora in cui un parametro presuppone un nuovo valore, relativo all'inizio della transizione o dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="1df83-106">The `time` attribute specifies the time at which a parameter assumes a new value, relative to the start of the transition or effect.</span></span>

## <a name="possible-values"></a><span data-ttu-id="1df83-107">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1df83-107">Possible Values</span></span>

<span data-ttu-id="1df83-108">Deve essere una stringa con formato *hh: mm: SS. FF* , dove *HH* = hours, *mm* = minutes, *SS* = seconds e *FF* = frazioni di secondi.</span><span class="sxs-lookup"><span data-stu-id="1df83-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="1df83-109">Esempio: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="1df83-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="1df83-110">È possibile omettere le unità iniziali.</span><span class="sxs-lookup"><span data-stu-id="1df83-110">Leading units can be omitted.</span></span> <span data-ttu-id="1df83-111">Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.</span><span class="sxs-lookup"><span data-stu-id="1df83-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1df83-112">Si applica a</span><span class="sxs-lookup"><span data-stu-id="1df83-112">Applies To</span></span>

<span data-ttu-id="1df83-113">[**at**](at-element.md), [ **lineari**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="1df83-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="1df83-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1df83-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df83-115">Attributi XTL</span><span class="sxs-lookup"><span data-stu-id="1df83-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> </dl>

 

 



