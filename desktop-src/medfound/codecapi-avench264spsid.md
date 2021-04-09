---
description: Imposta l'identificatore SPS (Sequence Parameter Set) nell'unità SPS Network Abstraction Layer (NAL) del flusso di bit H. 264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: Proprietà CODECAPI_AVEncH264SPSID (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127982"
---
# <a name="codecapi_avench264spsid-property"></a><span data-ttu-id="d471d-103">Proprietà AVEncH264SPSID di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="d471d-103">CODECAPI\_AVEncH264SPSID property</span></span>

<span data-ttu-id="d471d-104">Imposta l'identificatore SPS (Sequence Parameter Set) nell'unità SPS Network Abstraction Layer (NAL) del flusso di bit H. 264.</span><span class="sxs-lookup"><span data-stu-id="d471d-104">Sets the sequence parameter set (SPS) identifier in the SPS network abstraction layer (NAL) unit of the H.264 bit stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="d471d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d471d-105">Data type</span></span>

<span data-ttu-id="d471d-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="d471d-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d471d-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="d471d-107">Property GUID</span></span>

<span data-ttu-id="d471d-108">**Codecapis \_ AVEncH264SPSID**</span><span class="sxs-lookup"><span data-stu-id="d471d-108">**CODECAPI\_AVEncH264SPSID**</span></span>

## <a name="property-value"></a><span data-ttu-id="d471d-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d471d-109">Property value</span></span>

<span data-ttu-id="d471d-110">Specifica il valore dell' **\_ \_ \_ ID set di parametri Seq** nell'unità NAL SPS.</span><span class="sxs-lookup"><span data-stu-id="d471d-110">Specifies the value of **seq\_parameter\_set\_id** in the SPS NAL unit.</span></span> <span data-ttu-id="d471d-111">L'elemento della sintassi dell' **\_ \_ \_ ID set di parametri Seq** identifica il set di parametri di sequenza.</span><span class="sxs-lookup"><span data-stu-id="d471d-111">The **seq\_parameter\_set\_id** syntax element identifies the sequence parameter set.</span></span> <span data-ttu-id="d471d-112">Il flusso di bit risultante può essere concatenato con altri flussi di bit, per produrre un flusso di bit più lungo che contiene più set di parametri di sequenza con identificatori SPS diversi.</span><span class="sxs-lookup"><span data-stu-id="d471d-112">The resulting bit stream can be concatenated with other bit streams, to produce a longer bit stream that contains multiple sequence parameter sets with different SPS identifiers.</span></span>

<span data-ttu-id="d471d-113">L'intervallo valido è 0 31, come specificato nella specifica H. 264/AVC.</span><span class="sxs-lookup"><span data-stu-id="d471d-113">The valid range is 0 31, as specified in the H.264/AVC specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="d471d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d471d-114">Requirements</span></span>



| <span data-ttu-id="d471d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d471d-115">Requirement</span></span> | <span data-ttu-id="d471d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d471d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d471d-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d471d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d471d-118">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d471d-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="d471d-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d471d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d471d-120">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="d471d-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d471d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d471d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d471d-122"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="d471d-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d471d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d471d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d471d-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d471d-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d471d-125">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d471d-125">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

