---
description: Contiene la casella di descrizione dell'esempio per un file MP4 o 3GP.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: Attributo MF_MT_MPEG4_SAMPLE_DESCRIPTION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4620ae0b50a2c6f2dae7663aab0c49f13bc5a162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884189"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a><span data-ttu-id="b28c2-103">\_Attributo della \_ \_ Descrizione dell'esempio MF mt MPEG4 \_</span><span class="sxs-lookup"><span data-stu-id="b28c2-103">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute</span></span>

<span data-ttu-id="b28c2-104">Contiene la casella di descrizione dell'esempio per un file MP4 o 3GP.</span><span class="sxs-lookup"><span data-stu-id="b28c2-104">Contains the sample description box for an MP4 or 3GP file.</span></span>

## <a name="data-type"></a><span data-ttu-id="b28c2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b28c2-105">Data type</span></span>

<span data-ttu-id="b28c2-106">**BYTE\[\]**</span><span class="sxs-lookup"><span data-stu-id="b28c2-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="b28c2-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="b28c2-107">Get/set</span></span>

<span data-ttu-id="b28c2-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="b28c2-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="b28c2-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="b28c2-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b28c2-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="b28c2-110">Applies to</span></span>

[<span data-ttu-id="b28c2-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b28c2-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="b28c2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b28c2-112">Remarks</span></span>

<span data-ttu-id="b28c2-113">Nella casella Descrizione esempio viene descritta la codifica utilizzata per un flusso nel file.</span><span class="sxs-lookup"><span data-stu-id="b28c2-113">The sample description box describes the encoding used for a stream in the file.</span></span>

<span data-ttu-id="b28c2-114">L'origine file MPEG-4 imposta questo attributo sul tipo di supporto per ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="b28c2-114">The MPEG-4 file source sets this attribute on the media type for each stream.</span></span> <span data-ttu-id="b28c2-115">Il valore dell'attributo è costituito dai dati non elaborati nella casella Descrizione esempio.</span><span class="sxs-lookup"><span data-stu-id="b28c2-115">The value of the attribute is the raw data in the sample description box.</span></span> <span data-ttu-id="b28c2-116">Se l'origine file MPEG-4 è in grado di analizzare la descrizione dell'esempio, aggiunge anche i dettagli del formato al tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="b28c2-116">If the MPEG-4 file source can parse the sample description, it also adds the format details to the media type.</span></span> <span data-ttu-id="b28c2-117">In caso contrario, l'applicazione o il decodificatore deve analizzare la descrizione dell'esempio dall' \_ attributo MF mt \_ MPEG4 \_ Sample \_ Description.</span><span class="sxs-lookup"><span data-stu-id="b28c2-117">Otherwise, the application or the decoder must parse the sample description from the MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute.</span></span>

<span data-ttu-id="b28c2-118">Quando si imposta questo attributo sul sink MPEG-4 tramite il metodo [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , i dati per l'attributo MF \_ mt \_ MPEG4 \_ Sample \_ Description non devono essere modificati dopo che uno o più campioni sono stati inviati al sink sull'interfaccia [**IMFStreamSink::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) del flusso corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b28c2-118">When setting this attribute on MPEG-4 sink through [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) method, the data for the attribute MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION should not change after one or more samples have been sent to the sink on the corresponding stream's [**IMFStreamSink::ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) interface.</span></span>

<span data-ttu-id="b28c2-119">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b28c2-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b28c2-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b28c2-120">Requirements</span></span>



| <span data-ttu-id="b28c2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b28c2-121">Requirement</span></span> | <span data-ttu-id="b28c2-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b28c2-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b28c2-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b28c2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b28c2-124">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b28c2-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b28c2-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b28c2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b28c2-126">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b28c2-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b28c2-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b28c2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b28c2-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b28c2-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b28c2-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b28c2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b28c2-130">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b28c2-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b28c2-131">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="b28c2-131">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




