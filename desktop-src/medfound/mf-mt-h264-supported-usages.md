---
description: Specifica le modalità di utilizzo supportate per un flusso video H. 264.
ms.assetid: EEAE0B57-9731-4032-80A3-6A1AD11214EC
title: Attributo MF_MT_H264_SUPPORTED_USAGES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d1803c532e005c9fca8fca2fcd5cf211214989
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307510"
---
# <a name="mf_mt_h264_supported_usages-attribute"></a><span data-ttu-id="089ae-103">\_ \_ \_ Attributo Usage supportati MF mt H264 \_</span><span class="sxs-lookup"><span data-stu-id="089ae-103">MF\_MT\_H264\_SUPPORTED\_USAGES attribute</span></span>

<span data-ttu-id="089ae-104">Specifica le modalità di utilizzo supportate per un flusso video H. 264.</span><span class="sxs-lookup"><span data-stu-id="089ae-104">Specifies the supported usage modes for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="089ae-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="089ae-105">Data type</span></span>

<span data-ttu-id="089ae-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="089ae-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="089ae-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="089ae-107">Get/set</span></span>

<span data-ttu-id="089ae-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="089ae-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="089ae-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="089ae-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="089ae-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="089ae-110">Applies to</span></span>

[<span data-ttu-id="089ae-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="089ae-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="089ae-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="089ae-112">Remarks</span></span>

<span data-ttu-id="089ae-113">Questo attributo si applica ai tipi di supporto per i flussi H. 264 trasmessi tramite USB.</span><span class="sxs-lookup"><span data-stu-id="089ae-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="089ae-114">Il valore corrisponde al campo **bmSupportedUsages** nel descrittore del frame video UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="089ae-114">The value corresponds to the **bmSupportedUsages** field in the UVC 1.5 H.264 video frame descriptor.</span></span>

<span data-ttu-id="089ae-115">Questo attributo viene usato anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="089ae-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="089ae-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="089ae-116">Requirements</span></span>



| <span data-ttu-id="089ae-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="089ae-117">Requirement</span></span> | <span data-ttu-id="089ae-118">Valore</span><span class="sxs-lookup"><span data-stu-id="089ae-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="089ae-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="089ae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="089ae-120">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="089ae-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="089ae-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="089ae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="089ae-122">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="089ae-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="089ae-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="089ae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="089ae-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="089ae-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="089ae-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="089ae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="089ae-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="089ae-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="089ae-127">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="089ae-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




