---
description: Specifica se il flusso di output deve essere strutturato in modo che il flusso codificato abbia una latenza di decodifica bassa.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Proprietà AVEncCommonLowLatency (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225481"
---
# <a name="avenccommonlowlatency-property"></a><span data-ttu-id="869da-103">Proprietà AVEncCommonLowLatency</span><span class="sxs-lookup"><span data-stu-id="869da-103">AVEncCommonLowLatency property</span></span>

<span data-ttu-id="869da-104">Specifica se il flusso di output deve essere strutturato in modo che il flusso codificato abbia una latenza di decodifica bassa.</span><span class="sxs-lookup"><span data-stu-id="869da-104">Specifies whether the output stream should be structured so that the encoded stream has a low decoding latency.</span></span>

<span data-ttu-id="869da-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="869da-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="869da-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="869da-106">Data type</span></span>

<span data-ttu-id="869da-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="869da-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="869da-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="869da-108">Property GUID</span></span>

<span data-ttu-id="869da-109">**Codecapis \_ AVEncCommonLowLatency**</span><span class="sxs-lookup"><span data-stu-id="869da-109">**CODECAPI\_AVEncCommonLowLatency**</span></span>

## <a name="remarks"></a><span data-ttu-id="869da-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="869da-110">Remarks</span></span>

<span data-ttu-id="869da-111">La latenza di decodifica viene definita come la quantità di dati che il decodificatore deve memorizzare nel buffer.</span><span class="sxs-lookup"><span data-stu-id="869da-111">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="869da-112">Se ad esempio si imposta questa proprietà su **Variant \_ true** in un codificatore video MPEG, vengono limitati i tipi di strutture GOP che il codificatore può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="869da-112">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

## <a name="requirements"></a><span data-ttu-id="869da-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="869da-113">Requirements</span></span>



| <span data-ttu-id="869da-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="869da-114">Requirement</span></span> | <span data-ttu-id="869da-115">Valore</span><span class="sxs-lookup"><span data-stu-id="869da-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="869da-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="869da-116">Minimum supported client</span></span><br/> | <span data-ttu-id="869da-117">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="869da-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="869da-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="869da-118">Minimum supported server</span></span><br/> | <span data-ttu-id="869da-119">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="869da-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="869da-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="869da-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="869da-121"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="869da-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="869da-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="869da-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="869da-123">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="869da-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="869da-124">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="869da-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




