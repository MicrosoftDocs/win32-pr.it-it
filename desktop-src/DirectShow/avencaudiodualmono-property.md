---
description: Specifica se l'audio a 2 canali è codificato come stereo o doppia mono.
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Proprietà AVEncAudioDualMono (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a5b684638133a1449fc849348cdfd8627533fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304279"
---
# <a name="avencaudiodualmono-property"></a><span data-ttu-id="1f9d7-103">Proprietà AVEncAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="1f9d7-103">AVEncAudioDualMono property</span></span>

<span data-ttu-id="1f9d7-104">Specifica se l'audio a 2 canali è codificato come stereo o doppia mono.</span><span class="sxs-lookup"><span data-stu-id="1f9d7-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="1f9d7-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1f9d7-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="1f9d7-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1f9d7-106">Data type</span></span>

<span data-ttu-id="1f9d7-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="1f9d7-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="1f9d7-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="1f9d7-108">Property GUID</span></span>

<span data-ttu-id="1f9d7-109">**Codecapis \_ AVEncAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="1f9d7-109">**CODECAPI\_AVEncAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="1f9d7-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1f9d7-110">Property value</span></span>

<span data-ttu-id="1f9d7-111">Il valore di questa proprietà è un membro dell'enumerazione [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) .</span><span class="sxs-lookup"><span data-stu-id="1f9d7-111">The value of this property is a member of the [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f9d7-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f9d7-112">Remarks</span></span>

<span data-ttu-id="1f9d7-113">Questa proprietà non è applicabile ai codificatori audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="1f9d7-113">This property does not apply to MPEG audio encoders.</span></span> <span data-ttu-id="1f9d7-114">Per l'audio MPEG, usare la proprietà [**AVEncMPACodingMode**](avencmpacodingmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="1f9d7-114">For MPEG audio, use the [**AVEncMPACodingMode**](avencmpacodingmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f9d7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f9d7-115">Requirements</span></span>



| <span data-ttu-id="1f9d7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f9d7-116">Requirement</span></span> | <span data-ttu-id="1f9d7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1f9d7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9d7-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f9d7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1f9d7-119">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="1f9d7-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1f9d7-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f9d7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1f9d7-121">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1f9d7-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="1f9d7-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f9d7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f9d7-123"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f9d7-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f9d7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f9d7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9d7-125">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="1f9d7-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="1f9d7-126">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="1f9d7-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

