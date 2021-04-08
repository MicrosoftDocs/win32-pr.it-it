---
description: Restituisce il numero medio di bit al secondo dell'audio codificato.
ms.assetid: c90c9247-825f-4602-bb16-809969703a98
title: Proprietà AVEncStatAudioAverageBPS (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76bcf1ca7b3ee74ae406ebd71f85988a4d13313
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049040"
---
# <a name="avencstataudioaveragebps-property"></a><span data-ttu-id="a1749-103">Proprietà AVEncStatAudioAverageBPS</span><span class="sxs-lookup"><span data-stu-id="a1749-103">AVEncStatAudioAverageBPS property</span></span>

<span data-ttu-id="a1749-104">Restituisce il numero medio di bit al secondo dell'audio codificato.</span><span class="sxs-lookup"><span data-stu-id="a1749-104">Returns the average bits per second of the encoded audio.</span></span>

<span data-ttu-id="a1749-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a1749-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a1749-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a1749-106">Data type</span></span>

<span data-ttu-id="a1749-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a1749-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a1749-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="a1749-108">Property GUID</span></span>

<span data-ttu-id="a1749-109">**Codecapis \_ AVEncStatAudioAverageBPS**</span><span class="sxs-lookup"><span data-stu-id="a1749-109">**CODECAPI\_AVEncStatAudioAverageBPS**</span></span>

## <a name="remarks"></a><span data-ttu-id="a1749-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1749-110">Remarks</span></span>

<span data-ttu-id="a1749-111">Questa proprietà è disponibile al termine della codifica.</span><span class="sxs-lookup"><span data-stu-id="a1749-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="a1749-112">Questa proprietà è valida solo per la codifica con velocità in bit variabile (VBR) basata sulla qualità</span><span class="sxs-lookup"><span data-stu-id="a1749-112">This property applies only to quality-based variable bit rate (VBR) encoding</span></span>

## <a name="requirements"></a><span data-ttu-id="a1749-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1749-113">Requirements</span></span>



| <span data-ttu-id="a1749-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1749-114">Requirement</span></span> | <span data-ttu-id="a1749-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a1749-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1749-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1749-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a1749-117">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="a1749-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a1749-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1749-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a1749-119">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a1749-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a1749-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1749-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1749-121"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1749-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1749-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1749-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1749-123">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="a1749-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a1749-124">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a1749-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




