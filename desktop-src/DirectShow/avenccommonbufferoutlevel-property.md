---
description: Specifica il livello finale del buffer di codifica, in bit, alla fine del processo di codifica. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).
ms.assetid: d5bcdf54-061a-436b-8b1a-61ef7d7c90bf
title: Proprietà AVEncCommonBufferOutLevel (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d99cdea909a1fd1c3777aac4868a570161c3fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304247"
---
# <a name="avenccommonbufferoutlevel-property"></a><span data-ttu-id="62579-104">Proprietà AVEncCommonBufferOutLevel</span><span class="sxs-lookup"><span data-stu-id="62579-104">AVEncCommonBufferOutLevel property</span></span>

<span data-ttu-id="62579-105">Specifica il livello finale del buffer di codifica, in bit, alla fine del processo di codifica.</span><span class="sxs-lookup"><span data-stu-id="62579-105">Specifies the final level of the encoding buffer, in bits, at the end of the encoding process.</span></span> <span data-ttu-id="62579-106">Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="62579-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="62579-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="62579-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="62579-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="62579-108">Data type</span></span>

<span data-ttu-id="62579-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="62579-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="62579-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="62579-110">Property GUID</span></span>

<span data-ttu-id="62579-111">**Codecapis \_ AVEncCommonBufferOutLevel**</span><span class="sxs-lookup"><span data-stu-id="62579-111">**CODECAPI\_AVEncCommonBufferOutLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="62579-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="62579-112">Property value</span></span>

<span data-ttu-id="62579-113">Questa proprietà ha un intervallo lineare di valori.</span><span class="sxs-lookup"><span data-stu-id="62579-113">This property has a linear range of values.</span></span> <span data-ttu-id="62579-114">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="62579-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="62579-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="62579-115">Remarks</span></span>

<span data-ttu-id="62579-116">La proprietà è disponibile solo se la durata della codifica è definita in anticipo, usando la proprietà [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) o la proprietà [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="62579-116">The property is available only if the encoding duration is defined in advance, using the [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) property or [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) property.</span></span>

<span data-ttu-id="62579-117">Per il video MPEG questa proprietà definisce la completezza del VBV (video buffer Verifier) al termine del processo di codifica.</span><span class="sxs-lookup"><span data-stu-id="62579-117">For MPEG video, this property defines the video buffer verifier (VBV) fullness at the end of the encoding process.</span></span> <span data-ttu-id="62579-118">Supporta la concatenazione dei flussi durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="62579-118">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="62579-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62579-119">Requirements</span></span>



| <span data-ttu-id="62579-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="62579-120">Requirement</span></span> | <span data-ttu-id="62579-121">Valore</span><span class="sxs-lookup"><span data-stu-id="62579-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62579-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62579-122">Minimum supported client</span></span><br/> | <span data-ttu-id="62579-123">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="62579-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="62579-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62579-124">Minimum supported server</span></span><br/> | <span data-ttu-id="62579-125">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="62579-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="62579-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62579-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="62579-127"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="62579-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62579-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62579-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62579-129">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="62579-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="62579-130">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="62579-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




