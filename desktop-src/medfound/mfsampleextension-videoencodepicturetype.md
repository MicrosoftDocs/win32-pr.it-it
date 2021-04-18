---
description: Specifica il tipo di immagine restituito da un codificatore video.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: Attributo MFSampleExtension_VideoEncodePictureType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe0df0e4f3163e7c8c0581c5c7c2a854555eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309086"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a><span data-ttu-id="ae6a5-103">\_Attributo VideoEncodePictureType di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="ae6a5-103">MFSampleExtension\_VideoEncodePictureType attribute</span></span>

<span data-ttu-id="ae6a5-104">Specifica il tipo di immagine restituito da un codificatore video.</span><span class="sxs-lookup"><span data-stu-id="ae6a5-104">Specifies the type of picture that is output by a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="ae6a5-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ae6a5-105">Data type</span></span>

<span data-ttu-id="ae6a5-106">**eAVEncH264PictureType \_ B** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae6a5-106">**eAVEncH264PictureType\_B** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ae6a5-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="ae6a5-107">Get/set</span></span>

<span data-ttu-id="ae6a5-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ae6a5-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ae6a5-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="ae6a5-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ae6a5-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="ae6a5-110">Applies to</span></span>

[<span data-ttu-id="ae6a5-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="ae6a5-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="ae6a5-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae6a5-112">Remarks</span></span>

<span data-ttu-id="ae6a5-113">Il [**codificatore video H. 264**](h-264-video-encoder.md) imposta questo attributo sugli esempi di output generati.</span><span class="sxs-lookup"><span data-stu-id="ae6a5-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span> <span data-ttu-id="ae6a5-114">Il valore dell'attributo è un membro dell'enumerazione [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) .</span><span class="sxs-lookup"><span data-stu-id="ae6a5-114">The value of the attribute is a member of the [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae6a5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae6a5-115">Requirements</span></span>



| <span data-ttu-id="ae6a5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae6a5-116">Requirement</span></span> | <span data-ttu-id="ae6a5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ae6a5-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6a5-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae6a5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ae6a5-119">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ae6a5-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="ae6a5-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae6a5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ae6a5-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ae6a5-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="ae6a5-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae6a5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae6a5-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a5-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae6a5-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae6a5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae6a5-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ae6a5-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae6a5-126">**Codificatore video H. 264**</span><span class="sxs-lookup"><span data-stu-id="ae6a5-126">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="ae6a5-127">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="ae6a5-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae6a5-128">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="ae6a5-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




