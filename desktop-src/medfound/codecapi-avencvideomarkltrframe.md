---
description: Contrassegna il frame corrente come frame LTR.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: Proprietà CODECAPI_AVEncVideoMarkLTRFrame (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524626"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a><span data-ttu-id="62c42-103">Proprietà AVEncVideoMarkLTRFrame di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="62c42-103">CODECAPI\_AVEncVideoMarkLTRFrame property</span></span>

<span data-ttu-id="62c42-104">Contrassegna il frame corrente come frame LTR.</span><span class="sxs-lookup"><span data-stu-id="62c42-104">Marks the current frame as a LTR frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="62c42-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="62c42-105">Data type</span></span>

<span data-ttu-id="62c42-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="62c42-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="62c42-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="62c42-107">Property GUID</span></span>

<span data-ttu-id="62c42-108">**Codecapis \_ AVEncVideoMarkLTRFrame**</span><span class="sxs-lookup"><span data-stu-id="62c42-108">**CODECAPI\_AVEncVideoMarkLTRFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="62c42-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="62c42-109">Remarks</span></span>

<span data-ttu-id="62c42-110">**Codificatori H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="62c42-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="62c42-111">Il valore di questo controllo corrisponde al valore della sintassi H. 264 *LongTermFramIdx* associato al frame corrente.</span><span class="sxs-lookup"><span data-stu-id="62c42-111">The value of this control is the value of H.264 syntax *LongTermFramIdx* associated with the current frame.</span></span> <span data-ttu-id="62c42-112">Se il frame corrente non è nel livello di base, ad esempio l' *\_ ID temporale* dell'elemento della sintassi non è uguale a 0, questa proprietà si applica al frame del livello di base successivo nell'ordine di codifica.</span><span class="sxs-lookup"><span data-stu-id="62c42-112">If the current frame is not in the base layer, for example syntax element *temporal\_id* is not equal to 0, this property applies to the next base layer frame in encoding order.</span></span>

<span data-ttu-id="62c42-113">Questa proprietà non deve essere chiamata se è stata eseguita una chiamata in sospeso per contrassegnare un frame LTR usando la proprietà codecapis \_ AVEncVideoMarkLTRFrame e il codificatore non ha ancora contrassegnato un frame come LTR.</span><span class="sxs-lookup"><span data-stu-id="62c42-113">This property should not be called if a pending call to mark an LTR frame has been issued using the CODECAPI\_AVEncVideoMarkLTRFrame property and the encoder has not yet marked a frame as LTR.</span></span> <span data-ttu-id="62c42-114">In altre parole, il codificatore non deve accodare le richieste AVEncVideoMarkLTRFrame di codecapis \_ .</span><span class="sxs-lookup"><span data-stu-id="62c42-114">In other words, the encoder should not queue up CODECAPI\_AVEncVideoMarkLTRFrame requests.</span></span> <span data-ttu-id="62c42-115">Se viene inviata una richiesta AVEncVideoMarkLTRFrame di codecapite \_ mentre un'altra \_ richiesta AVEncVideoMarkLTRFrame di codecapites è ancora in sospeso, la richiesta precedente deve essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="62c42-115">If a CODECAPI\_AVEncVideoMarkLTRFrame request is submitted while another CODECAPI\_AVEncVideoMarkLTRFrame request is still pending, the older request should be dropped.</span></span>

<span data-ttu-id="62c42-116">La proprietà codecapis \_ AVEncVideoMarkLTRFrame è dinamica e può essere impostata durante la sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="62c42-116">The CODECAPI\_AVEncVideoMarkLTRFrame property is dynamic and can be set during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c42-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62c42-117">Requirements</span></span>



| <span data-ttu-id="62c42-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c42-118">Requirement</span></span> | <span data-ttu-id="62c42-119">Valore</span><span class="sxs-lookup"><span data-stu-id="62c42-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62c42-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c42-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62c42-121">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="62c42-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="62c42-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c42-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62c42-123">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="62c42-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="62c42-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62c42-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c42-125"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c42-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c42-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62c42-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c42-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62c42-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




