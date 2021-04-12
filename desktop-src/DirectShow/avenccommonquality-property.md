---
description: Specifica il livello di qualità per la codifica.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Proprietà AVEncCommonQuality (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e69d797f2e26e830158c969c8fcf4ec0b242a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482509"
---
# <a name="avenccommonquality-property"></a><span data-ttu-id="047f8-103">Proprietà AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="047f8-103">AVEncCommonQuality property</span></span>

<span data-ttu-id="047f8-104">Specifica il livello di qualità per la codifica.</span><span class="sxs-lookup"><span data-stu-id="047f8-104">Specifies the quality level for encoding.</span></span>

<span data-ttu-id="047f8-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="047f8-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="047f8-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="047f8-106">Data type</span></span>

<span data-ttu-id="047f8-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="047f8-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="047f8-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="047f8-108">Property GUID</span></span>

<span data-ttu-id="047f8-109">**Codecapis \_ AVEncCommonQuality**</span><span class="sxs-lookup"><span data-stu-id="047f8-109">**CODECAPI\_AVEncCommonQuality**</span></span>

## <a name="property-value"></a><span data-ttu-id="047f8-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="047f8-110">Property value</span></span>

<span data-ttu-id="047f8-111">Il valore di questa proprietà presenta l'intervallo seguente.</span><span class="sxs-lookup"><span data-stu-id="047f8-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="047f8-112">Valore</span><span class="sxs-lookup"><span data-stu-id="047f8-112">Value</span></span> | <span data-ttu-id="047f8-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="047f8-113">Description</span></span>                           |
|-------|---------------------------------------|
| <span data-ttu-id="047f8-114">0</span><span class="sxs-lookup"><span data-stu-id="047f8-114">0</span></span>     | <span data-ttu-id="047f8-115">Qualità minima, dimensioni di output inferiori.</span><span class="sxs-lookup"><span data-stu-id="047f8-115">Minimum quality, smaller output size.</span></span> |
| <span data-ttu-id="047f8-116">100</span><span class="sxs-lookup"><span data-stu-id="047f8-116">100</span></span>   | <span data-ttu-id="047f8-117">Qualità massima, dimensioni di output maggiori.</span><span class="sxs-lookup"><span data-stu-id="047f8-117">Maximum quality, larger output size.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="047f8-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="047f8-118">Remarks</span></span>

<span data-ttu-id="047f8-119">Questa proprietà controlla il livello di qualità quando il codificatore non usa una velocità in bit vincolata.</span><span class="sxs-lookup"><span data-stu-id="047f8-119">This property controls the quality level when the encoder is not using a constrained bit rate.</span></span> <span data-ttu-id="047f8-120">La proprietà [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) determina se la velocità in bit è vincolata.</span><span class="sxs-lookup"><span data-stu-id="047f8-120">The [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) property determines whether the bit rate is constrained.</span></span>

## <a name="requirements"></a><span data-ttu-id="047f8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="047f8-121">Requirements</span></span>



| <span data-ttu-id="047f8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="047f8-122">Requirement</span></span> | <span data-ttu-id="047f8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="047f8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="047f8-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="047f8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="047f8-125">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="047f8-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="047f8-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="047f8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="047f8-127">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="047f8-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="047f8-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="047f8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="047f8-129"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="047f8-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="047f8-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="047f8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="047f8-131">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="047f8-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="047f8-132">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="047f8-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




