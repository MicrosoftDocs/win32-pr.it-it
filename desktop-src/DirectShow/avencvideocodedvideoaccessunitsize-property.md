---
description: Specifica le dimensioni in byte delle unità di accesso ai video. Questa proprietà è valida solo per le modalità di controllo della velocità in bit variabile (VBR).
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: Proprietà AVEncVideoCodedVideoAccessUnitSize (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be3a6e499749d862fdcc63f28b1a9a02f476d1c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965484"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a><span data-ttu-id="ac7e1-104">Proprietà AVEncVideoCodedVideoAccessUnitSize</span><span class="sxs-lookup"><span data-stu-id="ac7e1-104">AVEncVideoCodedVideoAccessUnitSize property</span></span>

<span data-ttu-id="ac7e1-105">Specifica le dimensioni in byte delle unità di accesso ai video.</span><span class="sxs-lookup"><span data-stu-id="ac7e1-105">Specifies the size of the video access units, in bytes.</span></span> <span data-ttu-id="ac7e1-106">Questa proprietà è valida solo per le modalità di controllo della velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="ac7e1-106">This property applies only to variable bit rate (VBR) control modes.</span></span>

<span data-ttu-id="ac7e1-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ac7e1-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ac7e1-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ac7e1-108">Data type</span></span>

<span data-ttu-id="ac7e1-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="ac7e1-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ac7e1-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="ac7e1-110">Property GUID</span></span>

<span data-ttu-id="ac7e1-111">**Codecapis \_ AVEncVideoCodedVideoAccessUnitSize**</span><span class="sxs-lookup"><span data-stu-id="ac7e1-111">**CODECAPI\_AVEncVideoCodedVideoAccessUnitSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="ac7e1-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ac7e1-112">Property value</span></span>

<span data-ttu-id="ac7e1-113">Questa proprietà viene restituita come un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="ac7e1-113">This property is returned as a range of values.</span></span> <span data-ttu-id="ac7e1-114">Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="ac7e1-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac7e1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac7e1-115">Requirements</span></span>



| <span data-ttu-id="ac7e1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac7e1-116">Requirement</span></span> | <span data-ttu-id="ac7e1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ac7e1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac7e1-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac7e1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac7e1-119">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="ac7e1-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ac7e1-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac7e1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac7e1-121">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ac7e1-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ac7e1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac7e1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac7e1-123"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac7e1-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac7e1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac7e1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac7e1-125">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="ac7e1-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ac7e1-126">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="ac7e1-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




