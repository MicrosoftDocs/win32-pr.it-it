---
description: L'attributo mstop specifica l'ora di arresto di una clip rispetto al file multimediale originale.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: Attributo mstop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a63f52a1b912392165293e008074cf64a03b9751
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123468"
---
# <a name="mstop-attribute"></a><span data-ttu-id="c7922-103">Attributo mstop</span><span class="sxs-lookup"><span data-stu-id="c7922-103">mstop Attribute</span></span>

> [!Note]  
> <span data-ttu-id="c7922-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c7922-104">\[Deprecated.</span></span> <span data-ttu-id="c7922-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c7922-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c7922-106">L' `mstop` attributo specifica l'ora di arresto di una clip rispetto al file multimediale originale.</span><span class="sxs-lookup"><span data-stu-id="c7922-106">The `mstop` attribute specifies the stop time of a clip, relative to the original media file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c7922-107">Si applica a</span><span class="sxs-lookup"><span data-stu-id="c7922-107">Applies To</span></span>

[<span data-ttu-id="c7922-108">**clip**</span><span class="sxs-lookup"><span data-stu-id="c7922-108">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="c7922-109">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="c7922-109">Possible Values</span></span>

<span data-ttu-id="c7922-110">Deve essere una stringa con formato *hh: mm: SS. FF* , dove *HH* = hours, *mm* = minutes, *SS* = seconds e *FF* = frazioni di secondi.</span><span class="sxs-lookup"><span data-stu-id="c7922-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="c7922-111">Esempio: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="c7922-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="c7922-112">È possibile omettere le unità iniziali.</span><span class="sxs-lookup"><span data-stu-id="c7922-112">Leading units can be omitted.</span></span> <span data-ttu-id="c7922-113">Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.</span><span class="sxs-lookup"><span data-stu-id="c7922-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7922-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7922-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7922-115">Attributi XTL</span><span class="sxs-lookup"><span data-stu-id="c7922-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="c7922-116">**IAMTimelineSrc::SetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="c7922-116">**IAMTimelineSrc::SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



