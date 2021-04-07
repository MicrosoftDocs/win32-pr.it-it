---
description: Specifica l'incremento di basso livello quando il decodificatore esegue il controllo dinamico degli intervalli su un flusso audio Dolby AC-3.
ms.assetid: d723c825-f2f1-4ba0-a667-8285009764fd
title: Proprietà AVDecDDDynamicRangeScaleLow (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b68b1d4376d9ba15859be943ded23458fe16d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049046"
---
# <a name="avdecdddynamicrangescalelow-property"></a><span data-ttu-id="e08f0-103">Proprietà AVDecDDDynamicRangeScaleLow</span><span class="sxs-lookup"><span data-stu-id="e08f0-103">AVDecDDDynamicRangeScaleLow property</span></span>

<span data-ttu-id="e08f0-104">Specifica l'incremento di basso livello quando il decodificatore esegue il controllo dinamico degli intervalli su un flusso audio Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="e08f0-104">Specifies the low-level boost when the decoder performs dynamic range control on a Dolby AC-3 audio stream.</span></span>

<span data-ttu-id="e08f0-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e08f0-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="e08f0-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e08f0-106">Data type</span></span>

<span data-ttu-id="e08f0-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="e08f0-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e08f0-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="e08f0-108">Property GUID</span></span>

<span data-ttu-id="e08f0-109">**Codecapis \_ AVDecDDDynamicRangeScaleLow**</span><span class="sxs-lookup"><span data-stu-id="e08f0-109">**CODECAPI\_AVDecDDDynamicRangeScaleLow**</span></span>

## <a name="property-value"></a><span data-ttu-id="e08f0-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e08f0-110">Property value</span></span>

<span data-ttu-id="e08f0-111">Il valore di questa proprietà presenta l'intervallo seguente.</span><span class="sxs-lookup"><span data-stu-id="e08f0-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="e08f0-112">Valore</span><span class="sxs-lookup"><span data-stu-id="e08f0-112">Value</span></span> | <span data-ttu-id="e08f0-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e08f0-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="e08f0-114">0</span><span class="sxs-lookup"><span data-stu-id="e08f0-114">0</span></span>     | <span data-ttu-id="e08f0-115">Nessuna compressione dell'intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="e08f0-115">No dynamic range compression.</span></span> <span data-ttu-id="e08f0-116">Mantenere l'intervallo dinamico completo.</span><span class="sxs-lookup"><span data-stu-id="e08f0-116">Preserve the full dynamic range.</span></span> |
| <span data-ttu-id="e08f0-117">100</span><span class="sxs-lookup"><span data-stu-id="e08f0-117">100</span></span>   | <span data-ttu-id="e08f0-118">Applicare la compressione dell'intervallo dinamico completo.</span><span class="sxs-lookup"><span data-stu-id="e08f0-118">Apply full dynamic range compression.</span></span>                          |



 

## <a name="remarks"></a><span data-ttu-id="e08f0-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e08f0-119">Remarks</span></span>

<span data-ttu-id="e08f0-120">Questa proprietà si applica solo quando il valore della proprietà [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) è eAVDecDDOperationalMode \_ line.</span><span class="sxs-lookup"><span data-stu-id="e08f0-120">This property applies only when the value of the [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) property is eAVDecDDOperationalMode\_LINE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e08f0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e08f0-121">Requirements</span></span>



| <span data-ttu-id="e08f0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e08f0-122">Requirement</span></span> | <span data-ttu-id="e08f0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e08f0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e08f0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e08f0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e08f0-125">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="e08f0-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e08f0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e08f0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e08f0-127">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e08f0-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e08f0-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e08f0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e08f0-129"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="e08f0-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e08f0-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e08f0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e08f0-131">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="e08f0-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="e08f0-132">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="e08f0-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




