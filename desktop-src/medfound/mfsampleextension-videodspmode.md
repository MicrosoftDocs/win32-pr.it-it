---
description: Indica se la stabilizzazione video è stata applicata a un fotogramma video.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: Attributo MFSampleExtension_VideoDSPMode (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309d4b5b68455e78ba63074b9d8ec5e4cbde4fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310231"
---
# <a name="mfsampleextension_videodspmode-attribute"></a><span data-ttu-id="30501-103">\_Attributo VideoDSPMode di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="30501-103">MFSampleExtension\_VideoDSPMode attribute</span></span>

<span data-ttu-id="30501-104">Indica se la stabilizzazione video è stata applicata a un fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="30501-104">Indicates whether video stabilization was applied to a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="30501-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="30501-105">Data type</span></span>

<span data-ttu-id="30501-106">**MFVideoDSPMode** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="30501-106">**MFVideoDSPMode** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="30501-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="30501-107">Get/set</span></span>

<span data-ttu-id="30501-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="30501-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="30501-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="30501-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="30501-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="30501-110">Applies to</span></span>

[<span data-ttu-id="30501-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="30501-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="30501-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="30501-112">Remarks</span></span>

<span data-ttu-id="30501-113">Il [**stabilizzazione video MFT**](video-stabilization-mft.md) imposta questo attributo sugli esempi di output che produce.</span><span class="sxs-lookup"><span data-stu-id="30501-113">The [**Video Stabilization MFT**](video-stabilization-mft.md) sets this attribute on the output samples that it produces.</span></span> <span data-ttu-id="30501-114">Il valore dell'attributo è un valore di enumerazione [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) .</span><span class="sxs-lookup"><span data-stu-id="30501-114">The value of the attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="30501-115">Se il valore è **la \_ stabilizzazione MFVideoDSPMode**, il MFT applica la stabilizzazione dell'immagine al frame.</span><span class="sxs-lookup"><span data-stu-id="30501-115">If the value is **MFVideoDSPMode\_Stabilization**, it means that the MFT applied image stabilization to the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="30501-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30501-116">Requirements</span></span>



| <span data-ttu-id="30501-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="30501-117">Requirement</span></span> | <span data-ttu-id="30501-118">Valore</span><span class="sxs-lookup"><span data-stu-id="30501-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30501-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30501-119">Minimum supported client</span></span><br/> | <span data-ttu-id="30501-120">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="30501-120">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="30501-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30501-121">Minimum supported server</span></span><br/> | <span data-ttu-id="30501-122">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="30501-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30501-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30501-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="30501-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="30501-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30501-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30501-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30501-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="30501-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="30501-127">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="30501-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="30501-128">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="30501-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="30501-129">**Stabilizzazione video MFT**</span><span class="sxs-lookup"><span data-stu-id="30501-129">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




