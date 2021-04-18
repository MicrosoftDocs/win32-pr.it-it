---
description: Modalità di selezione dell'area DVD da parte di Microsoft DVD Navigator
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Modalità di selezione dell'area DVD da parte di Microsoft DVD Navigator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303729"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a><span data-ttu-id="72cf2-103">Modalità di selezione dell'area DVD da parte di Microsoft DVD Navigator</span><span class="sxs-lookup"><span data-stu-id="72cf2-103">How Microsoft DVD Navigator Selects the DVD Region</span></span>

<span data-ttu-id="72cf2-104">Microsoft DVD Navigator usa l'algoritmo seguente per determinare la corrispondenza dell'area durante la riproduzione di dischi DVD su un PC:</span><span class="sxs-lookup"><span data-stu-id="72cf2-104">The Microsoft DVD Navigator uses the following algorithm to determine region match while playing DVD discs on a PC:</span></span>

1.  <span data-ttu-id="72cf2-105">Il navigatore DVD ottiene l'area del disco, l'area dell'unità e l'area del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="72cf2-105">The DVD Navigator gets the disc region, drive region, and decoder region.</span></span>
2.  <span data-ttu-id="72cf2-106">Se l'area del disco è "tutte le aree", il navigatore DVD riproduce il disco.</span><span class="sxs-lookup"><span data-stu-id="72cf2-106">If the disc region is "all regions," the DVD Navigator plays the disc.</span></span>
3.  <span data-ttu-id="72cf2-107">Se il disco non è contrassegnato per tutte le aree, il navigatore DVD controlla se il decodificatore ha un'area preimpostata.</span><span class="sxs-lookup"><span data-stu-id="72cf2-107">If the disc is not marked for all regions, the DVD Navigator checks whether the decoder has a preset region.</span></span>
4.  <span data-ttu-id="72cf2-108">Se il decodificatore ha un'area preimpostata e non corrisponde all'area del disco, il navigatore DVD restituisce un errore che indica che non è possibile riprodurre il disco nella configurazione DVD corrente.</span><span class="sxs-lookup"><span data-stu-id="72cf2-108">If the decoder has a preset region and it does not match the disc region, the DVD Navigator returns an error indicating that it cannot play the disc on the current DVD configuration.</span></span> <span data-ttu-id="72cf2-109">Uscita</span><span class="sxs-lookup"><span data-stu-id="72cf2-109">(Exit)</span></span>
5.  <span data-ttu-id="72cf2-110">Se l'area del decodificatore non è impostata o è uguale all'area del disco, il navigatore DVD controlla se l'area dell'unità è uguale all'area del disco.</span><span class="sxs-lookup"><span data-stu-id="72cf2-110">If the decoder region is not set, or is the same as the disc region, the DVD Navigator checks whether the drive region is the same as the disc region.</span></span>
6.  <span data-ttu-id="72cf2-111">Se l'area dell'unità corrisponde all'area del disco, il navigatore DVD riproduce il titolo.</span><span class="sxs-lookup"><span data-stu-id="72cf2-111">If the drive region matches the disc region, the DVD Navigator plays the title.</span></span>
7.  <span data-ttu-id="72cf2-112">In caso contrario, se l'area del driver non corrisponde all'area del disco, il navigatore DVD richiama il codice per modificare l'area dell'unità.</span><span class="sxs-lookup"><span data-stu-id="72cf2-112">Otherwise, if the driver region does not match the disc region, the DVD Navigator invokes the code to change the drive's region.</span></span> <span data-ttu-id="72cf2-113">Se il numero consentito di modifiche all'area è esaurito, il tentativo di modifica dell'area ha esito negativo e il titolo non può essere riprodotto nel sistema.</span><span class="sxs-lookup"><span data-stu-id="72cf2-113">If the allowed number of region changes has been exhausted, the region change attempt fails and the title cannot be played on that system.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72cf2-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72cf2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72cf2-115">Supporto delle modifiche all'area DVD in Windows</span><span class="sxs-lookup"><span data-stu-id="72cf2-115">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



