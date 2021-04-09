---
description: L'attributo mlength specifica la durata di un file di origine. Questo valore deve corrispondere alla durata effettiva oppure è possibile che si verifichino errori di rendering.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: Attributo mlength
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965448"
---
# <a name="mlength-attribute"></a><span data-ttu-id="951ae-104">Attributo mlength</span><span class="sxs-lookup"><span data-stu-id="951ae-104">mlength Attribute</span></span>

> [!Note]  
> <span data-ttu-id="951ae-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="951ae-105">\[Deprecated.</span></span> <span data-ttu-id="951ae-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="951ae-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="951ae-107">L' `mlength` attributo specifica la durata di un file di origine.</span><span class="sxs-lookup"><span data-stu-id="951ae-107">The `mlength` attribute specifies the duration of a source file.</span></span> <span data-ttu-id="951ae-108">Questo valore deve corrispondere alla durata effettiva oppure è possibile che si verifichino errori di rendering.</span><span class="sxs-lookup"><span data-stu-id="951ae-108">This value must be the actual duration, or rendering errors may occur.</span></span>

## <a name="applies-to"></a><span data-ttu-id="951ae-109">Si applica a</span><span class="sxs-lookup"><span data-stu-id="951ae-109">Applies To</span></span>

[<span data-ttu-id="951ae-110">**clip**</span><span class="sxs-lookup"><span data-stu-id="951ae-110">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="951ae-111">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="951ae-111">Possible Values</span></span>

<span data-ttu-id="951ae-112">Deve essere una stringa con formato *hh: mm: SS. FF* , dove *HH* = hours, *mm* = minutes, *SS* = seconds e *FF* = frazioni di secondi.</span><span class="sxs-lookup"><span data-stu-id="951ae-112">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="951ae-113">Esempio: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="951ae-113">Example: 1:04:30.512.</span></span> <span data-ttu-id="951ae-114">È possibile omettere le unità iniziali.</span><span class="sxs-lookup"><span data-stu-id="951ae-114">Leading units can be omitted.</span></span> <span data-ttu-id="951ae-115">Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.</span><span class="sxs-lookup"><span data-stu-id="951ae-115">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="951ae-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="951ae-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="951ae-117">Attributi XTL</span><span class="sxs-lookup"><span data-stu-id="951ae-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="951ae-118">**IAMTimelineSrc::SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="951ae-118">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



