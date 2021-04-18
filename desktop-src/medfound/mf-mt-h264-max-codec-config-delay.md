---
description: Numero massimo di frame che il codificatore H. 264 impiega per rispondere a un comando.
ms.assetid: C856B2B0-4A06-436D-B589-B01DA86DB53D
title: Attributo MF_MT_H264_MAX_CODEC_CONFIG_DELAY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a835d5b5a37be0c722f313aaf4fe8ed8aa55f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310826"
---
# <a name="mf_mt_h264_max_codec_config_delay-attribute"></a><span data-ttu-id="2331b-103">\_ \_ \_ \_ \_ Attributo ritardo di configurazione codec \_ MF mt H264 max</span><span class="sxs-lookup"><span data-stu-id="2331b-103">MF\_MT\_H264\_MAX\_CODEC\_CONFIG\_DELAY attribute</span></span>

<span data-ttu-id="2331b-104">Numero massimo di frame che il codificatore H. 264 impiega per rispondere a un comando.</span><span class="sxs-lookup"><span data-stu-id="2331b-104">The maximum number of frames the H.264 encoder takes to respond to a command.</span></span>

## <a name="data-type"></a><span data-ttu-id="2331b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2331b-105">Data type</span></span>

<span data-ttu-id="2331b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2331b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="2331b-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="2331b-107">Get/set</span></span>

<span data-ttu-id="2331b-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="2331b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="2331b-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="2331b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="2331b-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="2331b-110">Applies to</span></span>

[<span data-ttu-id="2331b-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2331b-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="2331b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2331b-112">Remarks</span></span>

<span data-ttu-id="2331b-113">Questo attributo si applica ai tipi di supporto per i flussi H. 264 trasmessi tramite USB.</span><span class="sxs-lookup"><span data-stu-id="2331b-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="2331b-114">Il valore corrisponde al campo **bMaxCodecConfigDelay** nel descrittore di formato video UVC 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="2331b-114">The value corresponds to the **bMaxCodecConfigDelay** field in the UVC 1.2 H.264 video format descriptor.</span></span>

<span data-ttu-id="2331b-115">Questo attributo viene usato anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="2331b-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2331b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2331b-116">Requirements</span></span>



| <span data-ttu-id="2331b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2331b-117">Requirement</span></span> | <span data-ttu-id="2331b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2331b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2331b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2331b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2331b-120">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2331b-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="2331b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2331b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2331b-122">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="2331b-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2331b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2331b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2331b-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2331b-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2331b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2331b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2331b-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2331b-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2331b-127">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="2331b-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




