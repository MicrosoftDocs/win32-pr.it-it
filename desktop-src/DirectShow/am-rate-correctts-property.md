---
description: Il navigatore DVD usa questa proprietà per informare il decodificatore che lo strumento di navigazione sta impostando i timestamp corretti sugli esempi che recapita al decodificatore.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: Proprietà AM_RATE_CorrectTS (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa410b079d3de63de364662c7d5465c82814d24a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330336"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="92077-103">\_Proprietà rate \_ corrects</span><span class="sxs-lookup"><span data-stu-id="92077-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="92077-104">Il navigatore DVD usa questa proprietà per informare il decodificatore che lo strumento di navigazione sta impostando i timestamp corretti sugli esempi che recapita al decodificatore.</span><span class="sxs-lookup"><span data-stu-id="92077-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="92077-105">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="92077-105">Property Set GUID</span></span> | <span data-ttu-id="92077-106">\_TSRateChange KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="92077-106">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="92077-107">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="92077-107">Property ID</span></span>       | <span data-ttu-id="92077-108">\_Correttivi della velocità am \_</span><span class="sxs-lookup"><span data-stu-id="92077-108">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="92077-109">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="92077-109">Data Type</span></span>         | <span data-ttu-id="92077-110">**LONG**</span><span class="sxs-lookup"><span data-stu-id="92077-110">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="92077-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="92077-111">Remarks</span></span>

<span data-ttu-id="92077-112">Le versioni precedenti di DVD Navigator non impostano i timestamp corretti quando la velocità di riproduzione è diversa da 1,0.</span><span class="sxs-lookup"><span data-stu-id="92077-112">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="92077-113">Molti decodificatori aggirano questo problema ignorando gli indicatori temporali durante il rewind o l'avanzamento rapido e stimando i tempi di presentazione corretti.</span><span class="sxs-lookup"><span data-stu-id="92077-113">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="92077-114">Questi problemi sono stati corretti nella versione corrente del navigatore DVD.</span><span class="sxs-lookup"><span data-stu-id="92077-114">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="92077-115">Per la compatibilità con le versioni precedenti dei decodificatori esistenti, il navigatore DVD indica che i timestamp sono corretti impostando la \_ Proprietà am rate \_ corrects nel decodificatore con il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="92077-115">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="92077-116">Quando questa proprietà è impostata, il decodificatore deve utilizzare i timestamp effettivi anziché stimare i tempi di presentazione.</span><span class="sxs-lookup"><span data-stu-id="92077-116">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="92077-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92077-117">Requirements</span></span>



| <span data-ttu-id="92077-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="92077-118">Requirement</span></span> | <span data-ttu-id="92077-119">Valore</span><span class="sxs-lookup"><span data-stu-id="92077-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92077-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92077-120">Header</span></span><br/> | <dl> <span data-ttu-id="92077-121"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="92077-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92077-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92077-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92077-123">**Set di proprietà di modifica della frequenza**</span><span class="sxs-lookup"><span data-stu-id="92077-123">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




