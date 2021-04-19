---
description: Specifica il parametro di quantizzazione (QP) usato per codificare un campione video.
ms.assetid: F7C4FEFC-FEE7-4614-BC90-4F9D5D878F49
title: Attributo MFSampleExtension_VideoEncodeQP (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721f5df00ff24b307daed2ccbcbf61a04b129db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310230"
---
# <a name="mfsampleextension_videoencodeqp-attribute"></a><span data-ttu-id="ae9c5-103">\_Attributo VideoEncodeQP di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="ae9c5-103">MFSampleExtension\_VideoEncodeQP attribute</span></span>

<span data-ttu-id="ae9c5-104">Specifica il parametro di quantizzazione (QP) usato per codificare un campione video.</span><span class="sxs-lookup"><span data-stu-id="ae9c5-104">Specifies the quantization parameter (QP) that was used to encode a video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="ae9c5-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ae9c5-105">Data type</span></span>

<span data-ttu-id="ae9c5-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="ae9c5-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="ae9c5-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="ae9c5-107">Get/set</span></span>

<span data-ttu-id="ae9c5-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="ae9c5-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="ae9c5-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="ae9c5-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ae9c5-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="ae9c5-110">Applies to</span></span>

[<span data-ttu-id="ae9c5-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="ae9c5-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="ae9c5-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae9c5-112">Remarks</span></span>

<span data-ttu-id="ae9c5-113">Il [**codificatore video H. 264**](h-264-video-encoder.md) imposta questo attributo sugli esempi di output generati.</span><span class="sxs-lookup"><span data-stu-id="ae9c5-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae9c5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae9c5-114">Requirements</span></span>



| <span data-ttu-id="ae9c5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae9c5-115">Requirement</span></span> | <span data-ttu-id="ae9c5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ae9c5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9c5-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae9c5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ae9c5-118">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ae9c5-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="ae9c5-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae9c5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ae9c5-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ae9c5-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="ae9c5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae9c5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae9c5-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae9c5-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae9c5-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae9c5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae9c5-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ae9c5-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae9c5-125">**Codificatore video H. 264**</span><span class="sxs-lookup"><span data-stu-id="ae9c5-125">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="ae9c5-126">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="ae9c5-126">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae9c5-127">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="ae9c5-127">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




