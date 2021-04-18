---
description: Abilita o Disabilita l'accelerazione hardware per la decodifica video VC-1.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: Proprietà AVDecVideoAcceleration_VC1 (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fcdbe265f5a65212a2846b724f570b024ea0ab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304251"
---
# <a name="avdecvideoacceleration_vc1-property"></a><span data-ttu-id="2a967-103">\_Proprietà VC1 di AVDecVideoAcceleration</span><span class="sxs-lookup"><span data-stu-id="2a967-103">AVDecVideoAcceleration\_VC1 property</span></span>

<span data-ttu-id="2a967-104">Abilita o Disabilita l'accelerazione hardware per la decodifica video VC-1.</span><span class="sxs-lookup"><span data-stu-id="2a967-104">Enables or disables hardware acceleration for VC-1 video decoding.</span></span>

<span data-ttu-id="2a967-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2a967-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="2a967-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2a967-106">Data type</span></span>

<span data-ttu-id="2a967-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="2a967-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2a967-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="2a967-108">Property GUID</span></span>

<span data-ttu-id="2a967-109">**Codecapis \_ AVDecVideoAcceleration \_ VC1**</span><span class="sxs-lookup"><span data-stu-id="2a967-109">**CODECAPI\_AVDecVideoAcceleration\_VC1**</span></span>

## <a name="remarks"></a><span data-ttu-id="2a967-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a967-110">Remarks</span></span>

<span data-ttu-id="2a967-111">Se il valore è zero, il decodificatore non usa l'accelerazione video DirectX (DXVA) per la decodifica video VC-1.</span><span class="sxs-lookup"><span data-stu-id="2a967-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for VC-1 video decoding.</span></span> <span data-ttu-id="2a967-112">Per i filtri DirectShow, impostare questa proprietà prima della connessione del PIN di output del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="2a967-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a967-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a967-113">Requirements</span></span>



| <span data-ttu-id="2a967-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a967-114">Requirement</span></span> | <span data-ttu-id="2a967-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2a967-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a967-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a967-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2a967-117">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="2a967-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2a967-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a967-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2a967-119">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a967-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2a967-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a967-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a967-121"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a967-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a967-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a967-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a967-123">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="2a967-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2a967-124">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="2a967-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




