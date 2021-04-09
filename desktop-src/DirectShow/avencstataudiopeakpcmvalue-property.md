---
description: Restituisce il livello di volume più elevato presente nel contenuto audio.
ms.assetid: 1d9a6a22-bb82-45e1-80d2-88627c90340c
title: Proprietà AVEncStatAudioPeakPCMValue (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d75444631a63c946d4020fe91cdd3a980fc393
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124230"
---
# <a name="avencstataudiopeakpcmvalue-property"></a><span data-ttu-id="02016-103">Proprietà AVEncStatAudioPeakPCMValue</span><span class="sxs-lookup"><span data-stu-id="02016-103">AVEncStatAudioPeakPCMValue property</span></span>

<span data-ttu-id="02016-104">Restituisce il livello di volume più elevato presente nel contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="02016-104">Returns the highest volume level that was present in the audio content.</span></span>

<span data-ttu-id="02016-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="02016-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="02016-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="02016-106">Data type</span></span>

<span data-ttu-id="02016-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="02016-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="02016-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="02016-108">Property GUID</span></span>

<span data-ttu-id="02016-109">**Codecapis \_ AVEncStatAudioPeakPCMValue**</span><span class="sxs-lookup"><span data-stu-id="02016-109">**CODECAPI\_AVEncStatAudioPeakPCMValue**</span></span>

## <a name="remarks"></a><span data-ttu-id="02016-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="02016-110">Remarks</span></span>

<span data-ttu-id="02016-111">Questa proprietà è disponibile al termine della codifica.</span><span class="sxs-lookup"><span data-stu-id="02016-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="02016-112">Questa proprietà è valida solo per la codifica con velocità in bit variabile (VBR) basata sulla qualità</span><span class="sxs-lookup"><span data-stu-id="02016-112">This property applies only to quality-based variable bit rate (VBR) encoding</span></span>

## <a name="requirements"></a><span data-ttu-id="02016-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02016-113">Requirements</span></span>



| <span data-ttu-id="02016-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="02016-114">Requirement</span></span> | <span data-ttu-id="02016-115">Valore</span><span class="sxs-lookup"><span data-stu-id="02016-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02016-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02016-116">Minimum supported client</span></span><br/> | <span data-ttu-id="02016-117">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="02016-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="02016-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02016-118">Minimum supported server</span></span><br/> | <span data-ttu-id="02016-119">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="02016-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="02016-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02016-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="02016-121"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="02016-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02016-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02016-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02016-123">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="02016-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="02016-124">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="02016-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




