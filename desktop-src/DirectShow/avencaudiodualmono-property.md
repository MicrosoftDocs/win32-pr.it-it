---
description: "Proprietà AVEncAudioDualMono: specifica se l'audio a 2 canali è codificato come stereo o doppio mono."
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: Proprietà AVEncAudioDualMono (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58cbd901079d8f4dede1efae140791ae99c7fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096579"
---
# <a name="avencaudiodualmono-property"></a><span data-ttu-id="920c9-103">AVEncAudioDualMono - proprietà</span><span class="sxs-lookup"><span data-stu-id="920c9-103">AVEncAudioDualMono property</span></span>

<span data-ttu-id="920c9-104">Specifica se l'audio a 2 canali è codificato come stereo o doppio mono.</span><span class="sxs-lookup"><span data-stu-id="920c9-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="920c9-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="920c9-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="920c9-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="920c9-106">Data type</span></span>

<span data-ttu-id="920c9-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="920c9-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="920c9-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="920c9-108">Property GUID</span></span>

<span data-ttu-id="920c9-109">**CODECAPI \_ AVEncAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="920c9-109">**CODECAPI\_AVEncAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="920c9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="920c9-110">Property value</span></span>

<span data-ttu-id="920c9-111">Il valore di questa proprietà è un membro [**dell'enumerazione eAVEncAudioDualMono.**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)</span><span class="sxs-lookup"><span data-stu-id="920c9-111">The value of this property is a member of the [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="920c9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="920c9-112">Remarks</span></span>

<span data-ttu-id="920c9-113">Questa proprietà non si applica ai codificatori audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="920c9-113">This property does not apply to MPEG audio encoders.</span></span> <span data-ttu-id="920c9-114">Per l'audio MPEG, usare la [**proprietà AVEncMPACodingMode.**](avencmpacodingmode-property.md)</span><span class="sxs-lookup"><span data-stu-id="920c9-114">For MPEG audio, use the [**AVEncMPACodingMode**](avencmpacodingmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="920c9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="920c9-115">Requirements</span></span>



| <span data-ttu-id="920c9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="920c9-116">Requirement</span></span> | <span data-ttu-id="920c9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="920c9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="920c9-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="920c9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="920c9-119">App UWP per app desktop di Windows 2000 Professional \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="920c9-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="920c9-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="920c9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="920c9-121">App UWP per app desktop di Windows 2000 Server \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="920c9-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="920c9-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="920c9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="920c9-123"><dt>Codecapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="920c9-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="920c9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="920c9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="920c9-125">Proprietà API codec</span><span class="sxs-lookup"><span data-stu-id="920c9-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="920c9-126">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="920c9-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

