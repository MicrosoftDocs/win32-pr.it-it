---
description: Specifica il livello di combinazione, in decibel (dB), in un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.
ms.assetid: fcb16d02-af4f-4626-99ee-2831172e5280
title: Proprietà AVEncDDProductionMixLevel (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8a1726db6ab4841b4603a61bcfe39504742db42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304226"
---
# <a name="avencddproductionmixlevel-property"></a><span data-ttu-id="2e7f6-104">Proprietà AVEncDDProductionMixLevel</span><span class="sxs-lookup"><span data-stu-id="2e7f6-104">AVEncDDProductionMixLevel property</span></span>

<span data-ttu-id="2e7f6-105">Specifica il livello di combinazione, in decibel (dB), in un flusso audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="2e7f6-105">Specifies the mixing level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="2e7f6-106">Questa proprietà si applica ai codificatori audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="2e7f6-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="2e7f6-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2e7f6-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="2e7f6-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2e7f6-108">Data type</span></span>

<span data-ttu-id="2e7f6-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="2e7f6-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2e7f6-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="2e7f6-110">Property GUID</span></span>

<span data-ttu-id="2e7f6-111">**Codecapis \_ AVEncDDProductionMixLevel**</span><span class="sxs-lookup"><span data-stu-id="2e7f6-111">**CODECAPI\_AVEncDDProductionMixLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="2e7f6-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2e7f6-112">Property value</span></span>

<span data-ttu-id="2e7f6-113">Questa proprietà ha un intervallo lineare di valori.</span><span class="sxs-lookup"><span data-stu-id="2e7f6-113">This property has a linear range of values.</span></span> <span data-ttu-id="2e7f6-114">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="2e7f6-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e7f6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e7f6-115">Remarks</span></span>

<span data-ttu-id="2e7f6-116">Se si imposta questa proprietà, impostare la proprietà [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="2e7f6-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e7f6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e7f6-117">Requirements</span></span>



| <span data-ttu-id="2e7f6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e7f6-118">Requirement</span></span> | <span data-ttu-id="2e7f6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2e7f6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e7f6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e7f6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e7f6-121">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="2e7f6-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2e7f6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e7f6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e7f6-123">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2e7f6-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2e7f6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e7f6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e7f6-125"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e7f6-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e7f6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e7f6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e7f6-127">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="2e7f6-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2e7f6-128">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="2e7f6-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




