---
description: Specifica il livello iniziale del buffer di codifica, in bit. Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: Proprietà AVEncCommonBufferInLevel (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8219ab951fb68cd5dfc04e0b5415d77fe674e763
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125253"
---
# <a name="avenccommonbufferinlevel-property"></a><span data-ttu-id="fad71-104">Proprietà AVEncCommonBufferInLevel</span><span class="sxs-lookup"><span data-stu-id="fad71-104">AVEncCommonBufferInLevel property</span></span>

<span data-ttu-id="fad71-105">Specifica il livello iniziale del buffer di codifica, in bit.</span><span class="sxs-lookup"><span data-stu-id="fad71-105">Specifies the initial level of the encoding buffer, in bits.</span></span> <span data-ttu-id="fad71-106">Questa proprietà si applica solo alle modalità di codifica della velocità in bit costante (CBR) e della velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="fad71-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="fad71-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fad71-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fad71-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fad71-108">Data type</span></span>

<span data-ttu-id="fad71-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="fad71-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fad71-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="fad71-110">Property GUID</span></span>

<span data-ttu-id="fad71-111">**Codecapis \_ AVEncCommonBufferInLevel**</span><span class="sxs-lookup"><span data-stu-id="fad71-111">**CODECAPI\_AVEncCommonBufferInLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="fad71-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fad71-112">Property value</span></span>

<span data-ttu-id="fad71-113">Questa proprietà ha un intervallo lineare di valori.</span><span class="sxs-lookup"><span data-stu-id="fad71-113">This property has a linear range of values.</span></span> <span data-ttu-id="fad71-114">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="fad71-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="fad71-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fad71-115">Remarks</span></span>

<span data-ttu-id="fad71-116">Per il video MPEG questa proprietà definisce la completezza del verificatore video buffer iniziale (VBV).</span><span class="sxs-lookup"><span data-stu-id="fad71-116">For MPEG video, this property defines the initial video buffer verifier (VBV) fullness.</span></span> <span data-ttu-id="fad71-117">Supporta la concatenazione dei flussi durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="fad71-117">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="fad71-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fad71-118">Requirements</span></span>



| <span data-ttu-id="fad71-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fad71-119">Requirement</span></span> | <span data-ttu-id="fad71-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fad71-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fad71-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fad71-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fad71-122">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="fad71-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fad71-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fad71-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fad71-124">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fad71-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fad71-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fad71-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fad71-126"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="fad71-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad71-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fad71-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad71-128">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="fad71-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fad71-129">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="fad71-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




