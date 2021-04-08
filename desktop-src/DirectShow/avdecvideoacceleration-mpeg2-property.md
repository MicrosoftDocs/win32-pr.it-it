---
description: Abilita o Disabilita l'accelerazione hardware per la decodifica video MPEG-2.
ms.assetid: 2e05f9e5-28a6-48f3-956d-a14eaf3bf4ba
title: Proprietà AVDecVideoAcceleration_MPEG2 (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943459ae3810e1a0dc668c1f11c4c5d2354afaf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747250"
---
# <a name="avdecvideoacceleration_mpeg2-property"></a><span data-ttu-id="a2a09-103">\_Proprietà MPEG2 AVDecVideoAcceleration</span><span class="sxs-lookup"><span data-stu-id="a2a09-103">AVDecVideoAcceleration\_MPEG2 property</span></span>

<span data-ttu-id="a2a09-104">Abilita o Disabilita l'accelerazione hardware per la decodifica video MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="a2a09-104">Enables or disables hardware acceleration for MPEG-2 video decoding.</span></span>

<span data-ttu-id="a2a09-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a2a09-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a2a09-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a2a09-106">Data type</span></span>

<span data-ttu-id="a2a09-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a2a09-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a2a09-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="a2a09-108">Property GUID</span></span>

<span data-ttu-id="a2a09-109">**Codecapis \_ AVDecVideoAcceleration \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="a2a09-109">**CODECAPI\_AVDecVideoAcceleration\_MPEG2**</span></span>

## <a name="remarks"></a><span data-ttu-id="a2a09-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2a09-110">Remarks</span></span>

<span data-ttu-id="a2a09-111">Se il valore è zero, il decodificatore non usa l'accelerazione video DirectX (DXVA) per la decodifica video MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="a2a09-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for MPEG-2 video decoding.</span></span> <span data-ttu-id="a2a09-112">Per i filtri DirectShow, impostare questa proprietà prima della connessione del PIN di output del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="a2a09-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2a09-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2a09-113">Requirements</span></span>



| <span data-ttu-id="a2a09-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2a09-114">Requirement</span></span> | <span data-ttu-id="a2a09-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a2a09-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a09-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2a09-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a2a09-117">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="a2a09-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a2a09-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2a09-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a2a09-119">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a2a09-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a2a09-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2a09-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2a09-121"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2a09-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2a09-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2a09-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2a09-123">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="a2a09-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a2a09-124">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a2a09-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




