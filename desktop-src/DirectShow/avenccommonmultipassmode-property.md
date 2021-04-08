---
description: Specifica il numero di passaggi di codifica supportati dal codificatore.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Proprietà AVEncCommonMultipassMode (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876897"
---
# <a name="avenccommonmultipassmode-property"></a><span data-ttu-id="629e2-103">Proprietà AVEncCommonMultipassMode</span><span class="sxs-lookup"><span data-stu-id="629e2-103">AVEncCommonMultipassMode property</span></span>

<span data-ttu-id="629e2-104">Specifica il numero di passaggi di codifica supportati dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="629e2-104">Specifies the number of encoding passes that the encoder supports.</span></span>

<span data-ttu-id="629e2-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="629e2-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="629e2-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="629e2-106">Data type</span></span>

<span data-ttu-id="629e2-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="629e2-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="629e2-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="629e2-108">Property GUID</span></span>

<span data-ttu-id="629e2-109">**Codecapis \_ AVEncCommonMultipassMode**</span><span class="sxs-lookup"><span data-stu-id="629e2-109">**CODECAPI\_AVEncCommonMultipassMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="629e2-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="629e2-110">Property value</span></span>

<span data-ttu-id="629e2-111">Questa proprietà viene restituita come un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="629e2-111">This property is returned as a range of values.</span></span> <span data-ttu-id="629e2-112">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="629e2-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="629e2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="629e2-113">Remarks</span></span>

<span data-ttu-id="629e2-114">La latenza di decodifica viene definita come la quantità di dati che il decodificatore deve memorizzare nel buffer.</span><span class="sxs-lookup"><span data-stu-id="629e2-114">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="629e2-115">Se ad esempio si imposta questa proprietà su **Variant \_ true** in un codificatore video MPEG, vengono limitati i tipi di strutture GOP che il codificatore può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="629e2-115">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

<span data-ttu-id="629e2-116">Per impostare il passaggio di codifica corrente, impostare la proprietà [**AVEncCommonPassStart**](avenccommonpassstart-property.md) .</span><span class="sxs-lookup"><span data-stu-id="629e2-116">To set the current encoding pass, set the [**AVEncCommonPassStart**](avenccommonpassstart-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="629e2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="629e2-117">Requirements</span></span>



| <span data-ttu-id="629e2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="629e2-118">Requirement</span></span> | <span data-ttu-id="629e2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="629e2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="629e2-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="629e2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="629e2-121">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="629e2-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="629e2-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="629e2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="629e2-123">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="629e2-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="629e2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="629e2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="629e2-125"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="629e2-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="629e2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="629e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="629e2-127">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="629e2-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="629e2-128">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="629e2-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




