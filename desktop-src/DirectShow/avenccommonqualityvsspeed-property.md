---
description: Specifica il compromesso tra la qualità e la velocità di codifica. Questa proprietà è valida in tutte le modalità di controllo della frequenza.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Proprietà AVEncCommonQualityVsSpeed (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8af65f816bc9be6642e2a23ee4dc05e2e4fa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125244"
---
# <a name="avenccommonqualityvsspeed-property"></a><span data-ttu-id="cbf46-104">Proprietà AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="cbf46-104">AVEncCommonQualityVsSpeed property</span></span>

<span data-ttu-id="cbf46-105">Specifica il compromesso tra la qualità e la velocità di codifica.</span><span class="sxs-lookup"><span data-stu-id="cbf46-105">Specifies the tradeoff between encoding quality and speed.</span></span> <span data-ttu-id="cbf46-106">Questa proprietà è valida in tutte le modalità di controllo della frequenza.</span><span class="sxs-lookup"><span data-stu-id="cbf46-106">This property is valid in all rate control modes.</span></span>

<span data-ttu-id="cbf46-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="cbf46-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="cbf46-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cbf46-108">Data type</span></span>

<span data-ttu-id="cbf46-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="cbf46-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="cbf46-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="cbf46-110">Property GUID</span></span>

<span data-ttu-id="cbf46-111">**Codecapis \_ AVEncCommonQualityVsSpeed**</span><span class="sxs-lookup"><span data-stu-id="cbf46-111">**CODECAPI\_AVEncCommonQualityVsSpeed**</span></span>

## <a name="property-value"></a><span data-ttu-id="cbf46-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cbf46-112">Property value</span></span>

<span data-ttu-id="cbf46-113">Il valore di questa proprietà presenta l'intervallo seguente.</span><span class="sxs-lookup"><span data-stu-id="cbf46-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="cbf46-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cbf46-114">Value</span></span> | <span data-ttu-id="cbf46-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbf46-115">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="cbf46-116">0</span><span class="sxs-lookup"><span data-stu-id="cbf46-116">0</span></span>     | <span data-ttu-id="cbf46-117">Qualità inferiore, codifica più veloce.</span><span class="sxs-lookup"><span data-stu-id="cbf46-117">Lower quality, faster encoding.</span></span>  |
| <span data-ttu-id="cbf46-118">100</span><span class="sxs-lookup"><span data-stu-id="cbf46-118">100</span></span>   | <span data-ttu-id="cbf46-119">Maggiore qualità, codifica più lenta.</span><span class="sxs-lookup"><span data-stu-id="cbf46-119">Higher quality, slower encoding.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="cbf46-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbf46-120">Requirements</span></span>



| <span data-ttu-id="cbf46-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbf46-121">Requirement</span></span> | <span data-ttu-id="cbf46-122">Valore</span><span class="sxs-lookup"><span data-stu-id="cbf46-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf46-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbf46-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cbf46-124">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="cbf46-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="cbf46-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbf46-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cbf46-126">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cbf46-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cbf46-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cbf46-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbf46-128"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbf46-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbf46-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbf46-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf46-130">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="cbf46-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="cbf46-131">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="cbf46-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




