---
description: Specifica se un flusso in un'origine di acquisizione video è un flusso di immagini fisse.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: Attributo MF_DEVICESTREAM_IMAGE_STREAM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382ce587574d6ec46509a460dfb964e23dd416d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752447"
---
# <a name="mf_devicestream_image_stream-attribute"></a><span data-ttu-id="74e39-103">\_ \_ Attributo flusso di immagine MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="74e39-103">MF\_DEVICESTREAM\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="74e39-104">Specifica se un flusso in un'origine di acquisizione video è un flusso di immagini fisse.</span><span class="sxs-lookup"><span data-stu-id="74e39-104">Specifies whether a stream on a video capture source is a still-image stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="74e39-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="74e39-105">Data type</span></span>

<span data-ttu-id="74e39-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74e39-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="74e39-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="74e39-107">Remarks</span></span>

<span data-ttu-id="74e39-108">Alcune fotocamere video espongono un flusso di immagini ancora che produce immagini ad alta risoluzione.</span><span class="sxs-lookup"><span data-stu-id="74e39-108">Some video cameras expose a still-image stream that produces high-resolution images.</span></span> <span data-ttu-id="74e39-109">Il flusso di immagini potrebbe produrre immagini non compresse o immagini JPEG.</span><span class="sxs-lookup"><span data-stu-id="74e39-109">The image stream might produce uncompressed images or JPEG images.</span></span> <span data-ttu-id="74e39-110">Se la fotocamera ha un flusso di immagini, l'origine multimediale per il dispositivo di acquisizione imposta questo attributo su **true** nel flusso di immagini.</span><span class="sxs-lookup"><span data-stu-id="74e39-110">If the camera has an image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="74e39-111">Per ottenere questo attributo, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="74e39-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="74e39-112">Eseguire una query sull'origine multimediale per l'interfaccia [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="74e39-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="74e39-113">Chiamare [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per il flusso.</span><span class="sxs-lookup"><span data-stu-id="74e39-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="74e39-114">Chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="74e39-114">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="74e39-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74e39-115">Requirements</span></span>



| <span data-ttu-id="74e39-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="74e39-116">Requirement</span></span> | <span data-ttu-id="74e39-117">Valore</span><span class="sxs-lookup"><span data-stu-id="74e39-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="74e39-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74e39-118">Minimum supported client</span></span><br/> | <span data-ttu-id="74e39-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="74e39-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="74e39-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74e39-120">Minimum supported server</span></span><br/> | <span data-ttu-id="74e39-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="74e39-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="74e39-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74e39-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="74e39-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="74e39-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74e39-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74e39-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e39-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="74e39-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




