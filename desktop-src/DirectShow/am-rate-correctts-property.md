---
description: Lo strumento di navigazione DVD usa questa proprietà per informare il decodificatore che lo Strumento di navigazione sta impostando i timestamp corretti nei campioni che recapita al decodificatore.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: AM_RATE_CorrectTS proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c65b613f892708dc210af2ca2a05efb74785fb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910299"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="10635-103">Am \_ RATE \_ CorrectTS - proprietà</span><span class="sxs-lookup"><span data-stu-id="10635-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="10635-104">Lo strumento di navigazione DVD usa questa proprietà per informare il decodificatore che lo Strumento di navigazione sta impostando i timestamp corretti nei campioni che recapita al decodificatore.</span><span class="sxs-lookup"><span data-stu-id="10635-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



| <span data-ttu-id="10635-105">Label</span><span class="sxs-lookup"><span data-stu-id="10635-105">Label</span></span> | <span data-ttu-id="10635-106">Valore</span><span class="sxs-lookup"><span data-stu-id="10635-106">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="10635-107">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="10635-107">Property Set GUID</span></span> | <span data-ttu-id="10635-108">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="10635-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="10635-109">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="10635-109">Property ID</span></span>       | <span data-ttu-id="10635-110">AM \_ RATE \_ CorrectTS</span><span class="sxs-lookup"><span data-stu-id="10635-110">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="10635-111">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="10635-111">Data Type</span></span>         | <span data-ttu-id="10635-112">**LONG**</span><span class="sxs-lookup"><span data-stu-id="10635-112">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="10635-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="10635-113">Remarks</span></span>

<span data-ttu-id="10635-114">Le versioni precedenti dello strumento di spostamento DVD non impostano i timestamp corretti quando la velocità di riproduzione è diversa da 1.0.</span><span class="sxs-lookup"><span data-stu-id="10635-114">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="10635-115">Molti decodificatori rilascino questo problema ignorando i timestamp durante il riavvolgimento o l'avanzamento rapido e stimando i tempi di presentazione corretti.</span><span class="sxs-lookup"><span data-stu-id="10635-115">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="10635-116">Questi problemi sono stati corretti nella versione corrente dello Strumento di navigazione DVD.</span><span class="sxs-lookup"><span data-stu-id="10635-116">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="10635-117">Per garantire la compatibilità con le versioni precedenti dei decodificatori esistenti, lo strumento di spostamento DVD indica che i timestamp sono corretti impostando la proprietà AM RATE CorrectTS sul decodificatore con il \_ \_ valore **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="10635-117">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="10635-118">Quando questa proprietà è impostata, il decodificatore deve usare i timestamp effettivi anziché stimare l'ora di presentazione.</span><span class="sxs-lookup"><span data-stu-id="10635-118">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="10635-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10635-119">Requirements</span></span>



| <span data-ttu-id="10635-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="10635-120">Requirement</span></span> | <span data-ttu-id="10635-121">Valore</span><span class="sxs-lookup"><span data-stu-id="10635-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10635-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10635-122">Header</span></span><br/> | <dl> <span data-ttu-id="10635-123"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="10635-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10635-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10635-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10635-125">**Rate Change Property Set**</span><span class="sxs-lookup"><span data-stu-id="10635-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




