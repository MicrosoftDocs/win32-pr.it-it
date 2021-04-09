---
description: Specifica il numero di endpoint di streaming e il numero di flussi supportati per un codificatore H. 264 UVC.
ms.assetid: 343EC59E-30E5-4F37-8B05-60EF51717835
title: Attributo MF_MT_H264_SIMULCAST_SUPPORT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879490c6984186cf45971d2b122f0c2217b0f164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879394"
---
# <a name="mf_mt_h264_simulcast_support-attribute"></a><span data-ttu-id="b1665-103">Attributo di supporto di MF \_ mt \_ H264 \_ SIMULCAST \_</span><span class="sxs-lookup"><span data-stu-id="b1665-103">MF\_MT\_H264\_SIMULCAST\_SUPPORT attribute</span></span>

<span data-ttu-id="b1665-104">Specifica il numero di endpoint di streaming e il numero di flussi supportati per un codificatore H. 264 UVC.</span><span class="sxs-lookup"><span data-stu-id="b1665-104">Specifies the number of streaming endpoints and the number of supported streams for a UVC H.264 encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="b1665-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b1665-105">Data type</span></span>

<span data-ttu-id="b1665-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b1665-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b1665-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="b1665-107">Get/set</span></span>

<span data-ttu-id="b1665-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b1665-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b1665-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="b1665-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b1665-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="b1665-110">Applies to</span></span>

[<span data-ttu-id="b1665-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b1665-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="b1665-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1665-112">Remarks</span></span>

<span data-ttu-id="b1665-113">Questo attributo si applica ai tipi di supporto per i flussi H. 264 trasmessi tramite USB.</span><span class="sxs-lookup"><span data-stu-id="b1665-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="b1665-114">Il valore corrisponde al campo **bSimulcastSupport** nel descrittore di formato video UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="b1665-114">The value corresponds to the **bSimulcastSupport** field in the UVC 1.5 H.264 video format descriptor.</span></span>

<span data-ttu-id="b1665-115">Questo attributo viene usato anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="b1665-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1665-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1665-116">Requirements</span></span>



| <span data-ttu-id="b1665-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1665-117">Requirement</span></span> | <span data-ttu-id="b1665-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b1665-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1665-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1665-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b1665-120">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b1665-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b1665-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1665-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b1665-122">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="b1665-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b1665-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1665-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1665-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1665-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1665-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1665-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1665-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b1665-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b1665-127">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="b1665-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




