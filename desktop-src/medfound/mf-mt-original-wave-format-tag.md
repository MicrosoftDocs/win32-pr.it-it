---
description: Contiene il tag di formato WAVE originale per un flusso audio.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: Attributo MF_MT_ORIGINAL_WAVE_FORMAT_TAG (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba89171f9ae2bf3ab99df05bd3ae64b7d52be6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319174"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a><span data-ttu-id="b2842-103">\_ \_ \_ \_ Attributo tag formato Wave originale MF mt \_</span><span class="sxs-lookup"><span data-stu-id="b2842-103">MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute</span></span>

<span data-ttu-id="b2842-104">Contiene il tag di formato WAVE originale per un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="b2842-104">Contains the original WAVE format tag for an audio stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="b2842-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b2842-105">Data type</span></span>

<span data-ttu-id="b2842-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b2842-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b2842-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="b2842-107">Get/set</span></span>

<span data-ttu-id="b2842-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b2842-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b2842-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="b2842-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b2842-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="b2842-110">Applies to</span></span>

[<span data-ttu-id="b2842-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b2842-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="b2842-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2842-112">Remarks</span></span>

<span data-ttu-id="b2842-113">A seconda del file di origine, l'origine multimediale AVI potrebbe impostare questo attributo sui tipi di supporto che offre.</span><span class="sxs-lookup"><span data-stu-id="b2842-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="b2842-114">Un file AVI contiene un'intestazione del flusso per ogni flusso del file.</span><span class="sxs-lookup"><span data-stu-id="b2842-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="b2842-115">L'origine multimediale AVI Converte l'intestazione del flusso in un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="b2842-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="b2842-116">Per i flussi audio, l'intestazione del flusso contiene un tag di formato che identifica il formato audio.</span><span class="sxs-lookup"><span data-stu-id="b2842-116">For audio streams, the stream header contains a format tag that identifies the audio format.</span></span> <span data-ttu-id="b2842-117">Il tag di formato è contenuto nel membro **wFormatTag** della struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) . Nella maggior parte dei casi, l'origine multimediale AVI Converte il tag di formato direttamente in un GUID di sottotipo, come descritto nell'argomento [**GUID del sottotipo audio**](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="b2842-117">(The format tag is contained in the **wFormatTag** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.) In most cases, the AVI media source converts the format tag directly to a subtype GUID, as described in the topic [**Audio Subtype GUIDs**](audio-subtype-guids.md).</span></span> <span data-ttu-id="b2842-118">In alcuni casi, tuttavia, il tag di formato originale viene mappato a un altro tag di formato equivalente a.</span><span class="sxs-lookup"><span data-stu-id="b2842-118">In some cases, however, it maps the original format tag to another format tag that is equivalent.</span></span> <span data-ttu-id="b2842-119">In tal caso, l'origine multimediale archivia il tag di formato originale nel tipo di supporto, usando \_ l' \_ attributo di tag di formato Original Wave di MF mt \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b2842-119">If so, the media source stores the original format tag in the media type, using the MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute.</span></span>

<span data-ttu-id="b2842-120">I mapping del formato vengono archiviati nel registro di sistema con la seguente chiave:</span><span class="sxs-lookup"><span data-stu-id="b2842-120">The format mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="b2842-121">**HKEY \_ Classi \_ radice** \\ **MediaFoundation** \\ **MapAudioFormatTag**</span><span class="sxs-lookup"><span data-stu-id="b2842-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapAudioFormatTag**</span></span>

<span data-ttu-id="b2842-122">Ogni voce è un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b2842-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="b2842-123">Il nome della voce è la rappresentazione decimale del tag di formato.</span><span class="sxs-lookup"><span data-stu-id="b2842-123">The name of the entry is the decimal representation of the format tag.</span></span> <span data-ttu-id="b2842-124">Il valore della voce è il tag di formato equivalente.</span><span class="sxs-lookup"><span data-stu-id="b2842-124">The value of the entry is the equivalent format tag.</span></span>

<span data-ttu-id="b2842-125">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b2842-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2842-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2842-126">Requirements</span></span>



| <span data-ttu-id="b2842-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2842-127">Requirement</span></span> | <span data-ttu-id="b2842-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b2842-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2842-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2842-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b2842-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b2842-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b2842-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2842-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b2842-132">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2842-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b2842-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2842-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2842-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2842-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2842-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2842-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2842-136">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b2842-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b2842-137">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="b2842-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
