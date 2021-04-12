---
description: Specifica la dominanza del campo per un fotogramma video interlacciato.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: Attributo MFSampleExtension_BottomFieldFirst (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608160c92fa53e8cde6adee1831d6c3e8789bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344866"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a><span data-ttu-id="ec0e4-103">\_Attributo BottomFieldFirst di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="ec0e4-103">MFSampleExtension\_BottomFieldFirst attribute</span></span>

<span data-ttu-id="ec0e4-104">Specifica la dominanza del campo per un fotogramma video interlacciato.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-104">Specifies the field dominance for an interlaced video frame.</span></span> <span data-ttu-id="ec0e4-105">Questo attributo si applica agli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="ec0e4-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ec0e4-106">Data type</span></span>

<span data-ttu-id="ec0e4-107">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec0e4-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ec0e4-108">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="ec0e4-108">Get/set</span></span>

<span data-ttu-id="ec0e4-109">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ec0e4-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ec0e4-110">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ec0e4-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="ec0e4-111">Applies to</span></span>

[<span data-ttu-id="ec0e4-112">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="ec0e4-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="ec0e4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec0e4-113">Remarks</span></span>

<span data-ttu-id="ec0e4-114">Se il fotogramma video è interlacciato e l'esempio contiene due campi con interfoliazione, questo attributo indica il campo che viene visualizzato per primo.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-114">If the video frame is interlaced and the sample contains two interleaved fields, this attribute indicates which field is displayed first.</span></span> <span data-ttu-id="ec0e4-115">Se **true**, il campo inferiore è il primo nel tempo.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-115">If **TRUE**, the bottom field is first in time.</span></span> <span data-ttu-id="ec0e4-116">Se **false**, il campo superiore è primo.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-116">If **FALSE**, the top field is first.</span></span>

<span data-ttu-id="ec0e4-117">Se il frame è interlacciato e l'esempio contiene un solo campo, questo attributo indica il campo contenuto nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-117">If the frame is interlaced and the sample contains a single field, this attribute indicates which field the sample contains.</span></span> <span data-ttu-id="ec0e4-118">Se **true**, l'esempio contiene il campo in basso.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-118">If **TRUE**, the sample contains the bottom field.</span></span> <span data-ttu-id="ec0e4-119">Se **false**, l'esempio contiene il campo superiore.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-119">If **FALSE**, the sample contains the top field.</span></span>

<span data-ttu-id="ec0e4-120">Se il frame è progressivo, questo attributo descrive il modo in cui i campi devono essere ordinati quando l'output è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-120">If the frame is progressive, this attribute describes how the fields should be ordered when the output is interlaced.</span></span> <span data-ttu-id="ec0e4-121">Se **true**, il campo inferiore dovrebbe essere l'output per primo.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-121">If **TRUE**, the bottom field should be output first.</span></span> <span data-ttu-id="ec0e4-122">Se **false**, il campo superiore deve essere restituito per primo.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-122">If **FALSE**, the top field should be output first.</span></span>

<span data-ttu-id="ec0e4-123">Se questo attributo non è impostato, il tipo di supporto descrive la dominanza dei campi.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-123">If this attribute not set, the media type describes the field dominance.</span></span>

<span data-ttu-id="ec0e4-124">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ec0e4-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec0e4-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec0e4-125">Requirements</span></span>



| <span data-ttu-id="ec0e4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec0e4-126">Requirement</span></span> | <span data-ttu-id="ec0e4-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ec0e4-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec0e4-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec0e4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ec0e4-129">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ec0e4-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ec0e4-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec0e4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ec0e4-131">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ec0e4-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ec0e4-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec0e4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec0e4-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec0e4-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec0e4-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec0e4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec0e4-135">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ec0e4-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ec0e4-136">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="ec0e4-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="ec0e4-137">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="ec0e4-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="ec0e4-138">Interlacciamento video</span><span class="sxs-lookup"><span data-stu-id="ec0e4-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




