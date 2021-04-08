---
description: Abilita o Disabilita l'accelerazione hardware per la decodifica video H. 264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: Proprietà AVDecVideoAcceleration_H264 (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876909"
---
# <a name="avdecvideoacceleration_h264-property"></a><span data-ttu-id="9a44e-103">\_Proprietà H264 AVDecVideoAcceleration</span><span class="sxs-lookup"><span data-stu-id="9a44e-103">AVDecVideoAcceleration\_H264 property</span></span>

<span data-ttu-id="9a44e-104">Abilita o Disabilita l'accelerazione hardware per la decodifica video H. 264.</span><span class="sxs-lookup"><span data-stu-id="9a44e-104">Enables or disables hardware acceleration for H.264 video decoding.</span></span>

<span data-ttu-id="9a44e-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9a44e-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="9a44e-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9a44e-106">Data type</span></span>

<span data-ttu-id="9a44e-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="9a44e-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="9a44e-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="9a44e-108">Property GUID</span></span>

<span data-ttu-id="9a44e-109">**Codecapis \_ AVDecVideoAcceleration \_ H264**</span><span class="sxs-lookup"><span data-stu-id="9a44e-109">**CODECAPI\_AVDecVideoAcceleration\_H264**</span></span>

## <a name="remarks"></a><span data-ttu-id="9a44e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a44e-110">Remarks</span></span>

<span data-ttu-id="9a44e-111">Se il valore è zero, il decodificatore non usa l'accelerazione video DirectX (DXVA) per la decodifica video H. 264.</span><span class="sxs-lookup"><span data-stu-id="9a44e-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for H.264 video decoding.</span></span> <span data-ttu-id="9a44e-112">Per i filtri DirectShow, impostare questa proprietà prima della connessione del PIN di output del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="9a44e-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a44e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a44e-113">Requirements</span></span>



| <span data-ttu-id="9a44e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a44e-114">Requirement</span></span> | <span data-ttu-id="9a44e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9a44e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a44e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a44e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9a44e-117">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="9a44e-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9a44e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a44e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9a44e-119">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9a44e-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9a44e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a44e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a44e-121"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a44e-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a44e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a44e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a44e-123">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="9a44e-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="9a44e-124">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="9a44e-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




