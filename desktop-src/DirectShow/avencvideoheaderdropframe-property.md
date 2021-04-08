---
description: Specifica il valore del flag drop-frame nell'intestazione Group of Pictures (GOP).
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: Proprietà AVEncVideoHeaderDropFrame (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876966"
---
# <a name="avencvideoheaderdropframe-property"></a><span data-ttu-id="aae88-103">Proprietà AVEncVideoHeaderDropFrame</span><span class="sxs-lookup"><span data-stu-id="aae88-103">AVEncVideoHeaderDropFrame property</span></span>

<span data-ttu-id="aae88-104">Specifica il valore del flag drop-frame nell'intestazione Group of Pictures (GOP).</span><span class="sxs-lookup"><span data-stu-id="aae88-104">Specifies the value of drop-frame flag in the group of pictures (GOP) header.</span></span>

<span data-ttu-id="aae88-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="aae88-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="aae88-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="aae88-106">Data type</span></span>

<span data-ttu-id="aae88-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="aae88-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="aae88-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="aae88-108">Property GUID</span></span>

<span data-ttu-id="aae88-109">**Codecapis \_ AVEncVideoHeaderDropFrame**</span><span class="sxs-lookup"><span data-stu-id="aae88-109">**CODECAPI\_AVEncVideoHeaderDropFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="aae88-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="aae88-110">Property value</span></span>

<span data-ttu-id="aae88-111">Il valore di questa proprietà può essere 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="aae88-111">The value of this property can be 0 or 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="aae88-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="aae88-112">Remarks</span></span>

<span data-ttu-id="aae88-113">La modalità drop frame viene usata nel video NTSC per correggere la discrepanza tra il video, ovvero 29,97 fotogrammi al secondo e la visualizzazione del codice temporale, ovvero 30 fotogrammi al secondo.</span><span class="sxs-lookup"><span data-stu-id="aae88-113">Drop-frame mode is used in NTSC video to correct the discrepancy between the video, which is 29.97 frames per second, and the time code display, which is 30 frames per second.</span></span> <span data-ttu-id="aae88-114">In modalità di rilascio frame, i numeri di frame 00 e 01 vengono ignorati all'inizio di ogni minuto, ad eccezione dei minuti che sono persino multipli di dieci (00, 10, 20 e così via).</span><span class="sxs-lookup"><span data-stu-id="aae88-114">In drop-frame mode, frame numbers 00 and 01 are skipped at the start of each minute, except for minutes that are even multiples of ten (00, 10, 20, and so forth).</span></span> <span data-ttu-id="aae88-115">Vengono eliminati solo i numeri di frame nel codice temporale; non vengono eliminati frame effettivi.</span><span class="sxs-lookup"><span data-stu-id="aae88-115">Only the frame numbers in the time code are dropped; no actual frames are dropped.</span></span>

## <a name="requirements"></a><span data-ttu-id="aae88-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aae88-116">Requirements</span></span>



| <span data-ttu-id="aae88-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="aae88-117">Requirement</span></span> | <span data-ttu-id="aae88-118">Valore</span><span class="sxs-lookup"><span data-stu-id="aae88-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aae88-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aae88-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aae88-120">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="aae88-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="aae88-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aae88-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aae88-122">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aae88-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="aae88-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aae88-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aae88-124"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae88-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae88-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aae88-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae88-126">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="aae88-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="aae88-127">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="aae88-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




