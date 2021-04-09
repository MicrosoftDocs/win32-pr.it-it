---
description: Specifica la precisione dei coefficienti del controller di dominio, in bit. Questa proprietà si applica ai codificatori video MPEG.
ms.assetid: 2b4d11c1-767c-4466-8291-7959d841ae65
title: Proprietà AVEncMPVIntraDCPrecision (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d4bdd3c08f49586eb2663829271ae4166d917e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876689"
---
# <a name="avencmpvintradcprecision-property"></a><span data-ttu-id="57cc4-104">Proprietà AVEncMPVIntraDCPrecision</span><span class="sxs-lookup"><span data-stu-id="57cc4-104">AVEncMPVIntraDCPrecision property</span></span>

<span data-ttu-id="57cc4-105">Specifica la precisione dei coefficienti del controller di dominio, in bit.</span><span class="sxs-lookup"><span data-stu-id="57cc4-105">Specifies the precision of the DC coefficients, in bits.</span></span> <span data-ttu-id="57cc4-106">Questa proprietà si applica ai codificatori video MPEG.</span><span class="sxs-lookup"><span data-stu-id="57cc4-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="57cc4-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cc4-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="57cc4-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="57cc4-108">Data type</span></span>

<span data-ttu-id="57cc4-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="57cc4-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="57cc4-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="57cc4-110">Property GUID</span></span>

<span data-ttu-id="57cc4-111">**Codecapis \_ AVEncMPVIntraDCPrecision**</span><span class="sxs-lookup"><span data-stu-id="57cc4-111">**CODECAPI\_AVEncMPVIntraDCPrecision**</span></span>

## <a name="property-value"></a><span data-ttu-id="57cc4-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="57cc4-112">Property value</span></span>

<span data-ttu-id="57cc4-113">Questa proprietà ha un intervallo lineare di valori.</span><span class="sxs-lookup"><span data-stu-id="57cc4-113">This property has a linear range of values.</span></span> <span data-ttu-id="57cc4-114">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="57cc4-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="57cc4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="57cc4-115">Remarks</span></span>

<span data-ttu-id="57cc4-116">L'intervallo consueto per questa proprietà è da 8 a 11 bit.</span><span class="sxs-lookup"><span data-stu-id="57cc4-116">The usual range for this property is 8 to 11 bits.</span></span> <span data-ttu-id="57cc4-117">Se il valore è zero, il codificatore seleziona la precisione.</span><span class="sxs-lookup"><span data-stu-id="57cc4-117">If the value is zero, the encoder selects the precision.</span></span>

## <a name="requirements"></a><span data-ttu-id="57cc4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57cc4-118">Requirements</span></span>



| <span data-ttu-id="57cc4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="57cc4-119">Requirement</span></span> | <span data-ttu-id="57cc4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="57cc4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57cc4-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57cc4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="57cc4-122">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="57cc4-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="57cc4-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57cc4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="57cc4-124">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="57cc4-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="57cc4-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57cc4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="57cc4-126"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="57cc4-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57cc4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57cc4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57cc4-128">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="57cc4-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="57cc4-129">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="57cc4-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




