---
description: Specifica il taglio di alto livello quando il decodificatore esegue il controllo dinamico degli intervalli su un flusso audio Dolby AC-3.
ms.assetid: 8771a5f9-878b-43fd-8eaa-0bfc276194aa
title: Proprietà AVDecDDDynamicRangeScaleHigh (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521cd631d92db73f23c7018adeda9bd321d23c1a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482277"
---
# <a name="avdecdddynamicrangescalehigh-property"></a><span data-ttu-id="31157-103">Proprietà AVDecDDDynamicRangeScaleHigh</span><span class="sxs-lookup"><span data-stu-id="31157-103">AVDecDDDynamicRangeScaleHigh property</span></span>

<span data-ttu-id="31157-104">Specifica il taglio di alto livello quando il decodificatore esegue il controllo dinamico degli intervalli su un flusso audio Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="31157-104">Specifies the high-level cut when the decoder performs dynamic range control on a Dolby AC-3 audio stream.</span></span>

<span data-ttu-id="31157-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="31157-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="31157-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="31157-106">Data type</span></span>

<span data-ttu-id="31157-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="31157-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="31157-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="31157-108">Property GUID</span></span>

<span data-ttu-id="31157-109">**Codecapis \_ AVDecDDDynamicRangeScaleHigh**</span><span class="sxs-lookup"><span data-stu-id="31157-109">**CODECAPI\_AVDecDDDynamicRangeScaleHigh**</span></span>

## <a name="property-value"></a><span data-ttu-id="31157-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="31157-110">Property value</span></span>

<span data-ttu-id="31157-111">Il valore di questa proprietà presenta l'intervallo seguente.</span><span class="sxs-lookup"><span data-stu-id="31157-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="31157-112">Valore</span><span class="sxs-lookup"><span data-stu-id="31157-112">Value</span></span> | <span data-ttu-id="31157-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31157-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="31157-114">0</span><span class="sxs-lookup"><span data-stu-id="31157-114">0</span></span>     | <span data-ttu-id="31157-115">Nessuna compressione dell'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="31157-115">No dynamic range compression.</span></span> <span data-ttu-id="31157-116">Mantenere l'intervallo dinamico completo.</span><span class="sxs-lookup"><span data-stu-id="31157-116">Preserve the full dynamic range.</span></span> |
| <span data-ttu-id="31157-117">100</span><span class="sxs-lookup"><span data-stu-id="31157-117">100</span></span>   | <span data-ttu-id="31157-118">Applicare la compressione dell'intervallo dinamico completo.</span><span class="sxs-lookup"><span data-stu-id="31157-118">Apply full dynamic range compression.</span></span>                          |



 

## <a name="remarks"></a><span data-ttu-id="31157-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="31157-119">Remarks</span></span>

<span data-ttu-id="31157-120">Questa proprietà si applica solo quando il valore della proprietà [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) è eAVDecDDOperationalMode \_ line.</span><span class="sxs-lookup"><span data-stu-id="31157-120">This property applies only when the value of the [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) property is eAVDecDDOperationalMode\_LINE.</span></span>

## <a name="requirements"></a><span data-ttu-id="31157-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31157-121">Requirements</span></span>



| <span data-ttu-id="31157-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="31157-122">Requirement</span></span> | <span data-ttu-id="31157-123">Valore</span><span class="sxs-lookup"><span data-stu-id="31157-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31157-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31157-124">Minimum supported client</span></span><br/> | <span data-ttu-id="31157-125">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="31157-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="31157-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31157-126">Minimum supported server</span></span><br/> | <span data-ttu-id="31157-127">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="31157-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="31157-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31157-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="31157-129"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="31157-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31157-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31157-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31157-131">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="31157-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="31157-132">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="31157-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




