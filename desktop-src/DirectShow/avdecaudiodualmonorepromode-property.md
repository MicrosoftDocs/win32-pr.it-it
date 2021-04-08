---
description: Specifica il modo in cui il decodificatore riproduce audio mono doppio.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: Proprietà AVDecAudioDualMonoReproMode (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ebe7e003b2dc4b6eebc30901525ffb918a9a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747082"
---
# <a name="avdecaudiodualmonorepromode-property"></a><span data-ttu-id="8dc52-103">Proprietà AVDecAudioDualMonoReproMode</span><span class="sxs-lookup"><span data-stu-id="8dc52-103">AVDecAudioDualMonoReproMode property</span></span>

<span data-ttu-id="8dc52-104">Specifica il modo in cui il decodificatore riproduce audio mono doppio.</span><span class="sxs-lookup"><span data-stu-id="8dc52-104">Specifies how the decoder reproduces dual mono audio.</span></span>

<span data-ttu-id="8dc52-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8dc52-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="8dc52-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8dc52-106">Data type</span></span>

<span data-ttu-id="8dc52-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="8dc52-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8dc52-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="8dc52-108">Property GUID</span></span>

<span data-ttu-id="8dc52-109">**Codecapis \_ AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="8dc52-109">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="8dc52-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8dc52-110">Property value</span></span>

<span data-ttu-id="8dc52-111">Il valore di questa proprietà è un membro dell'enumerazione [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) .</span><span class="sxs-lookup"><span data-stu-id="8dc52-111">The value of this property is a member of the [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dc52-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8dc52-112">Remarks</span></span>

<span data-ttu-id="8dc52-113">Questa proprietà si applica solo quando il flusso di bit di input del decodificatore contiene audio mono doppio.</span><span class="sxs-lookup"><span data-stu-id="8dc52-113">This properties applies only when the decoder's input bit stream contains dual mono audio.</span></span> <span data-ttu-id="8dc52-114">Per verificare questa condizione, ottenere il valore della proprietà [AVDecAudioDualMono](avdecaudiodualmono-property.md) .</span><span class="sxs-lookup"><span data-stu-id="8dc52-114">To test this condition, get the value of the [AVDecAudioDualMono](avdecaudiodualmono-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dc52-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8dc52-115">Requirements</span></span>



| <span data-ttu-id="8dc52-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dc52-116">Requirement</span></span> | <span data-ttu-id="8dc52-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8dc52-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc52-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8dc52-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8dc52-119">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="8dc52-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8dc52-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8dc52-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8dc52-121">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8dc52-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8dc52-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8dc52-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dc52-123"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dc52-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dc52-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8dc52-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dc52-125">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="8dc52-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8dc52-126">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="8dc52-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




