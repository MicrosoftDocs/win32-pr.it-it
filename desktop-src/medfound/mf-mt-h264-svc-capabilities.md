---
description: Specifica le funzionalità di SVC di un flusso video H. 264.
ms.assetid: B727D9D2-6126-41F8-A27A-743640FE3AE4
title: Attributo MF_MT_H264_SVC_CAPABILITIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35a39b5f1727af8399d9d0c56c93d2d9d1486c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751935"
---
# <a name="mf_mt_h264_svc_capabilities-attribute"></a><span data-ttu-id="6172d-103">Attributo delle funzionalità di MF \_ mt \_ H264 \_ SVC \_</span><span class="sxs-lookup"><span data-stu-id="6172d-103">MF\_MT\_H264\_SVC\_CAPABILITIES attribute</span></span>

<span data-ttu-id="6172d-104">Specifica le funzionalità di SVC di un flusso video H. 264.</span><span class="sxs-lookup"><span data-stu-id="6172d-104">Specifies the SVC capabilities of an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="6172d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6172d-105">Data type</span></span>

<span data-ttu-id="6172d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6172d-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6172d-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="6172d-107">Get/set</span></span>

<span data-ttu-id="6172d-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="6172d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6172d-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="6172d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="6172d-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="6172d-110">Applies to</span></span>

[<span data-ttu-id="6172d-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6172d-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="6172d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6172d-112">Remarks</span></span>

<span data-ttu-id="6172d-113">Questo attributo si applica ai tipi di supporto per i flussi H. 264 trasmessi tramite USB.</span><span class="sxs-lookup"><span data-stu-id="6172d-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="6172d-114">Il valore corrisponde al campo **bmSVCCapabilities** nel descrittore del frame video UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="6172d-114">The value corresponds to the **bmSVCCapabilities** field in the UVC 1.5 H.264 video frame descriptor.</span></span>

<span data-ttu-id="6172d-115">Questo attributo viene usato anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="6172d-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6172d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6172d-116">Requirements</span></span>



| <span data-ttu-id="6172d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6172d-117">Requirement</span></span> | <span data-ttu-id="6172d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6172d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6172d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6172d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6172d-120">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6172d-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="6172d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6172d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6172d-122">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="6172d-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6172d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6172d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6172d-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6172d-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6172d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6172d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6172d-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6172d-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6172d-127">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="6172d-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




