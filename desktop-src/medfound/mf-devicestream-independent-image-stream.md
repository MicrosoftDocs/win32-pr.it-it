---
description: Specifica se il flusso di immagini in un'origine di acquisizione video è indipendente dal flusso video.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: Attributo MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174e62a1bdd178ad2d8dce7fab5bf9ce3104d834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309570"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a><span data-ttu-id="3f51b-103">\_Attributo del \_ \_ flusso immagine indipendente MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="3f51b-103">MF\_DEVICESTREAM\_INDEPENDENT\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="3f51b-104">Specifica se il flusso di immagini in un'origine di acquisizione video è indipendente dal flusso video.</span><span class="sxs-lookup"><span data-stu-id="3f51b-104">Specifies whether the image stream on a video capture source is independent of the video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="3f51b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3f51b-105">Data type</span></span>

<span data-ttu-id="3f51b-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f51b-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3f51b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f51b-107">Remarks</span></span>

<span data-ttu-id="3f51b-108">Alcune fotocamere USB espongono un flusso che produce ancora immagini.</span><span class="sxs-lookup"><span data-stu-id="3f51b-108">Some USB video cameras expose a stream that produces still images.</span></span> <span data-ttu-id="3f51b-109">In alcune fotocamere, il flusso dell'immagine restituisce semplicemente il frame successivo dal flusso video.</span><span class="sxs-lookup"><span data-stu-id="3f51b-109">In some cameras, the image stream simply returns the next frame from the video stream.</span></span> <span data-ttu-id="3f51b-110">In altre fotocamere, il flusso di immagini funziona indipendentemente dal flusso video.</span><span class="sxs-lookup"><span data-stu-id="3f51b-110">In other cameras, the image stream functions independently of the video stream.</span></span> <span data-ttu-id="3f51b-111">Se la fotocamera ha un flusso di immagini indipendente, l'origine multimediale per il dispositivo di acquisizione imposta questo attributo su **true** nel flusso di immagini.</span><span class="sxs-lookup"><span data-stu-id="3f51b-111">If the camera has an independent image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="3f51b-112">Per ottenere questo attributo, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="3f51b-112">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="3f51b-113">Eseguire una query sull'origine multimediale per l'interfaccia [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="3f51b-113">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="3f51b-114">Chiamare [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per il flusso.</span><span class="sxs-lookup"><span data-stu-id="3f51b-114">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="3f51b-115">Chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="3f51b-115">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

<span data-ttu-id="3f51b-116">Questo attributo si applica solo quando l'attributo del [ \_ \_ \_ flusso dell'immagine MF DEVICESTREAM](mf-devicestream-image-stream.md) è **true**.</span><span class="sxs-lookup"><span data-stu-id="3f51b-116">This attribute applies only when the [MF\_DEVICESTREAM\_IMAGE\_STREAM](mf-devicestream-image-stream.md) attribute is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f51b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f51b-117">Requirements</span></span>



| <span data-ttu-id="3f51b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f51b-118">Requirement</span></span> | <span data-ttu-id="3f51b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3f51b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3f51b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f51b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3f51b-121">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3f51b-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3f51b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f51b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3f51b-123">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3f51b-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3f51b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f51b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f51b-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f51b-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f51b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f51b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f51b-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f51b-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




