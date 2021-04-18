---
description: Specifica i tipi di frame di sincronizzazione supportati per un flusso video H. 264.
ms.assetid: A2E548F1-A5FA-4110-AD07-46BE9D7DC4A5
title: Attributo MF_MT_H264_SUPPORTED_SYNC_FRAME_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c328cbdef60750f2df7e9af403d8748c37d53b28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307511"
---
# <a name="mf_mt_h264_supported_sync_frame_types-attribute"></a><span data-ttu-id="3dec9-103">\_ \_ \_ \_ \_ Attributo tipi di frame di sincronizzazione supportati da MF mt H264 \_</span><span class="sxs-lookup"><span data-stu-id="3dec9-103">MF\_MT\_H264\_SUPPORTED\_SYNC\_FRAME\_TYPES attribute</span></span>

<span data-ttu-id="3dec9-104">Specifica i tipi di frame di sincronizzazione supportati per un flusso video H. 264.</span><span class="sxs-lookup"><span data-stu-id="3dec9-104">Specifies the types of synchronization frame that are supported for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="3dec9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3dec9-105">Data type</span></span>

<span data-ttu-id="3dec9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3dec9-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="3dec9-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="3dec9-107">Get/set</span></span>

<span data-ttu-id="3dec9-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="3dec9-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3dec9-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="3dec9-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3dec9-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="3dec9-110">Applies to</span></span>

[<span data-ttu-id="3dec9-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3dec9-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="3dec9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3dec9-112">Remarks</span></span>

<span data-ttu-id="3dec9-113">Questo attributo si applica ai tipi di supporto per i flussi H. 264 trasmessi tramite USB.</span><span class="sxs-lookup"><span data-stu-id="3dec9-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="3dec9-114">Il valore corrisponde al campo **bmSupportedSyncFrameTypes** nel descrittore di formato video UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="3dec9-114">The value corresponds to the **bmSupportedSyncFrameTypes** field in the UVC 1.5 H.264 video format descriptor.</span></span>

<span data-ttu-id="3dec9-115">Questo attributo viene usato anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="3dec9-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3dec9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3dec9-116">Requirements</span></span>



| <span data-ttu-id="3dec9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dec9-117">Requirement</span></span> | <span data-ttu-id="3dec9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3dec9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3dec9-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3dec9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3dec9-120">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3dec9-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="3dec9-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3dec9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3dec9-122">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="3dec9-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3dec9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3dec9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dec9-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dec9-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dec9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3dec9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dec9-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3dec9-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3dec9-127">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="3dec9-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




