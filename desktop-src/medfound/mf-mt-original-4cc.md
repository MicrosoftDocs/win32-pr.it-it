---
description: Contiene il codec originale FOURCC per un flusso video.
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: Attributo MF_MT_ORIGINAL_4CC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968164"
---
# <a name="mf_mt_original_4cc-attribute"></a><span data-ttu-id="523f0-103">\_ \_ Attributo 4cc originale MF mt \_</span><span class="sxs-lookup"><span data-stu-id="523f0-103">MF\_MT\_ORIGINAL\_4CC attribute</span></span>

<span data-ttu-id="523f0-104">Contiene il codec originale FOURCC per un flusso video.</span><span class="sxs-lookup"><span data-stu-id="523f0-104">Contains the original codec FOURCC for a video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="523f0-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="523f0-105">Data type</span></span>

<span data-ttu-id="523f0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="523f0-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="523f0-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="523f0-107">Get/set</span></span>

<span data-ttu-id="523f0-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="523f0-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="523f0-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="523f0-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="523f0-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="523f0-110">Applies to</span></span>

[<span data-ttu-id="523f0-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="523f0-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="523f0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="523f0-112">Remarks</span></span>

<span data-ttu-id="523f0-113">A seconda del file di origine, l'origine multimediale AVI potrebbe impostare questo attributo sui tipi di supporto che offre.</span><span class="sxs-lookup"><span data-stu-id="523f0-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="523f0-114">Un file AVI contiene un'intestazione del flusso per ogni flusso del file.</span><span class="sxs-lookup"><span data-stu-id="523f0-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="523f0-115">L'origine multimediale AVI Converte l'intestazione del flusso in un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="523f0-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="523f0-116">Per i flussi video compressi, l'intestazione del flusso contiene un FOURCC che identifica il codec video.</span><span class="sxs-lookup"><span data-stu-id="523f0-116">For compressed video streams, the stream header contains a FOURCC that identifies the video codec.</span></span> <span data-ttu-id="523f0-117">Nella maggior parte dei casi, l'origine multimediale AVI Converte questo FOURCC direttamente in un GUID di sottotipo, come descritto nell'argomento [GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="523f0-117">In most cases, the AVI media source converts this FOURCC directly to a subtype GUID, as described in the topic [Video Subtype GUIDs](video-subtype-guids.md).</span></span> <span data-ttu-id="523f0-118">In alcuni casi, tuttavia, esegue il mapping del FOURCC originale a un altro FOURCC equivalente.</span><span class="sxs-lookup"><span data-stu-id="523f0-118">In some cases, however, it maps the original FOURCC to another FOURCC that is equivalent.</span></span> <span data-ttu-id="523f0-119">In tal caso, l'origine multimediale archivia il FOURCC originale nel tipo di supporto, usando l' \_ \_ attributo 4cc originale MF mt \_ .</span><span class="sxs-lookup"><span data-stu-id="523f0-119">If so, the media source stores the original FOURCC in the media type, using the MF\_MT\_ORIGINAL\_4CC attribute.</span></span>

<span data-ttu-id="523f0-120">I mapping di FOURCC vengono archiviati nel registro di sistema con la seguente chiave:</span><span class="sxs-lookup"><span data-stu-id="523f0-120">The FOURCC mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="523f0-121">**HKEY \_ Classi \_ radice** \\ **MediaFoundation** \\ **MapVideo4cc**</span><span class="sxs-lookup"><span data-stu-id="523f0-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapVideo4cc**</span></span>

<span data-ttu-id="523f0-122">Ogni voce è un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="523f0-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="523f0-123">Il nome della voce è la rappresentazione esadecimale di FOURCC, senza un prefisso "0x" e con il primo carattere visualizzato per primo nella stringa.</span><span class="sxs-lookup"><span data-stu-id="523f0-123">The name of the entry is the hexadecimal representation of the FOURCC, without an "0x" prefix, and with the first character appearing first in the string.</span></span> <span data-ttu-id="523f0-124">Il codice FOURCC ' abcd ', ad esempio, verrebbe visualizzato come "61626364".</span><span class="sxs-lookup"><span data-stu-id="523f0-124">For example, the FOURCC code 'abcd' would appear as "61626364".</span></span> <span data-ttu-id="523f0-125">Il valore della voce è il codice FOURCC equivalente.</span><span class="sxs-lookup"><span data-stu-id="523f0-125">The value of the entry is the equivalent FOURCC code.</span></span>

<span data-ttu-id="523f0-126">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="523f0-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="523f0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="523f0-127">Requirements</span></span>



| <span data-ttu-id="523f0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="523f0-128">Requirement</span></span> | <span data-ttu-id="523f0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="523f0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="523f0-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="523f0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="523f0-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="523f0-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="523f0-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="523f0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="523f0-133">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="523f0-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="523f0-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="523f0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="523f0-135"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="523f0-135"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="523f0-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="523f0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="523f0-137">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="523f0-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="523f0-138">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="523f0-138">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




