---
description: Indica il numero di buffer non compressi richiesti dal sink multimediale EVR (Enhanced video renderer) per la deinterlacciamento.
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: Attributo MF_SA_REQUIRED_SAMPLE_COUNT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe7d47370cd4877a0f9722d443bc6bb3f7bdeb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314029"
---
# <a name="mf_sa_required_sample_count-attribute"></a><span data-ttu-id="84d4a-103">\_ \_ \_ Attributo count di esempio \_ obbligatorio MF SA</span><span class="sxs-lookup"><span data-stu-id="84d4a-103">MF\_SA\_REQUIRED\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="84d4a-104">Indica il numero di buffer non compressi richiesti dal sink multimediale EVR (Enhanced video renderer) per la deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="84d4a-104">Indicates the number of uncompressed buffers that the enhanced video renderer (EVR) media sink requires for deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="84d4a-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="84d4a-105">Data type</span></span>

<span data-ttu-id="84d4a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="84d4a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="84d4a-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="84d4a-107">Remarks</span></span>

<span data-ttu-id="84d4a-108">Si tratta di un attributo a livello di flusso.</span><span class="sxs-lookup"><span data-stu-id="84d4a-108">This is a stream-level attribute.</span></span> <span data-ttu-id="84d4a-109">Per ottenere l'attributo da EVR, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="84d4a-109">To get the attribute from the EVR, do the following:</span></span>

1.  <span data-ttu-id="84d4a-110">Chiamare [**IMFMediaSink:: GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) per ottenere il sink del flusso.</span><span class="sxs-lookup"><span data-stu-id="84d4a-110">Call [**IMFMediaSink::GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) to get the stream sink.</span></span>
2.  <span data-ttu-id="84d4a-111">Eseguire una query sul sink di flusso per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="84d4a-111">Query the stream sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>
3.  <span data-ttu-id="84d4a-112">Chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="84d4a-112">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="84d4a-113">Internamente, il mixer fornisce questo attributo a EVR.</span><span class="sxs-lookup"><span data-stu-id="84d4a-113">Internally, the mixer provides this attribute to the EVR.</span></span> <span data-ttu-id="84d4a-114">Per ottenere l'attributo dal mixer, chiamare [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span><span class="sxs-lookup"><span data-stu-id="84d4a-114">To get the attribute from the mixer, call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span></span>

<span data-ttu-id="84d4a-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="84d4a-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="84d4a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84d4a-116">Requirements</span></span>



| <span data-ttu-id="84d4a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="84d4a-117">Requirement</span></span> | <span data-ttu-id="84d4a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="84d4a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="84d4a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84d4a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="84d4a-120">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="84d4a-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="84d4a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84d4a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="84d4a-122">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="84d4a-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="84d4a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84d4a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="84d4a-124"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="84d4a-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84d4a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84d4a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84d4a-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84d4a-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="84d4a-127">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="84d4a-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="84d4a-128">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="84d4a-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="84d4a-129">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84d4a-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




