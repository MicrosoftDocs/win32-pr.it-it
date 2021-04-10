---
description: Specifica la modalità di controllo della frequenza.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Proprietà AVEncCommonRateControlMode (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225479"
---
# <a name="avenccommonratecontrolmode-property"></a><span data-ttu-id="a85a4-103">Proprietà AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="a85a4-103">AVEncCommonRateControlMode property</span></span>

<span data-ttu-id="a85a4-104">Specifica la modalità di controllo della frequenza.</span><span class="sxs-lookup"><span data-stu-id="a85a4-104">Specifies the rate control mode.</span></span>

<span data-ttu-id="a85a4-105">Le applicazioni possono impostare questa proprietà per specificare la modalità di controllo della frequenza.</span><span class="sxs-lookup"><span data-stu-id="a85a4-105">Applications can set this property to specify the rate control mode.</span></span> <span data-ttu-id="a85a4-106">I codificatori possono inoltre restituire questa proprietà come funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a85a4-106">Encoders can also return this property as a capability.</span></span>

<span data-ttu-id="a85a4-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a85a4-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a85a4-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a85a4-108">Data type</span></span>

<span data-ttu-id="a85a4-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a85a4-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a85a4-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="a85a4-110">Property GUID</span></span>

<span data-ttu-id="a85a4-111">**Codecapis \_ AVEncCommonRateControlMode**</span><span class="sxs-lookup"><span data-stu-id="a85a4-111">**CODECAPI\_AVEncCommonRateControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="a85a4-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a85a4-112">Property value</span></span>

<span data-ttu-id="a85a4-113">Il valore di questa proprietà è un membro dell'enumerazione [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) .</span><span class="sxs-lookup"><span data-stu-id="a85a4-113">The value of this property is a member of the [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="a85a4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a85a4-114">Remarks</span></span>

<span data-ttu-id="a85a4-115">Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="a85a4-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="a85a4-116">[CODEcapi \_ AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [codecapit \_ AVENCVIDEOUSAGE](/windows/desktop/medfound/codecapi-avencvideousage)e codecapi \_ AVEncCommonRateControlMode sono proprietà del codificatore statiche.</span><span class="sxs-lookup"><span data-stu-id="a85a4-116">[CODECAPI\_AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [CODECAPI\_AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage), and CODECAPI\_AVEncCommonRateControlMode are static encoder properties.</span></span> <span data-ttu-id="a85a4-117">Una volta impostate, queste diverranno effettive solo dopo la chiamata di un tipo di supporto set sul pin di output della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="a85a4-117">Once set, these will only take effect after a set media type is called on the camera’s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a85a4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a85a4-118">Requirements</span></span>



| <span data-ttu-id="a85a4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a85a4-119">Requirement</span></span> | <span data-ttu-id="a85a4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a85a4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a85a4-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a85a4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a85a4-122">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="a85a4-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a85a4-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a85a4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a85a4-124">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a85a4-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a85a4-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a85a4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a85a4-126"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="a85a4-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a85a4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a85a4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a85a4-128">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="a85a4-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a85a4-129">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a85a4-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

