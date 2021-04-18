---
description: Contiene un elenco di lingue RFC 1766 utilizzate nella presentazione corrente.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: Attributo MF_PD_ASF_LANGLIST_LEGACYORDER (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24abc714a7605800faa8ad66f8c0b888fba6f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315017"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a><span data-ttu-id="333e2-103">\_ \_ \_ Attributo LEGACYORDER di MF PD \_ ASF</span><span class="sxs-lookup"><span data-stu-id="333e2-103">MF\_PD\_ASF\_LANGLIST\_LEGACYORDER attribute</span></span>

<span data-ttu-id="333e2-104">Contiene un elenco di lingue RFC 1766 utilizzate nella presentazione corrente.</span><span class="sxs-lookup"><span data-stu-id="333e2-104">Contains a list of RFC 1766 languages used in the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="333e2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="333e2-105">Data type</span></span>

<span data-ttu-id="333e2-106">**BYTE \[\]**</span><span class="sxs-lookup"><span data-stu-id="333e2-106">**BYTE \[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="333e2-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="333e2-107">Get/set</span></span>

<span data-ttu-id="333e2-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="333e2-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="333e2-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="333e2-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="333e2-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="333e2-110">Applies to</span></span>

[<span data-ttu-id="333e2-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="333e2-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="333e2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="333e2-112">Remarks</span></span>

<span data-ttu-id="333e2-113">Questo attributo si applica ai descrittori di presentazione generati dall' [oggetto ContentInfo ASF](asf-contentinfo-object.md) mediante una chiamata a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="333e2-113">This attribute applies to presentation descriptors that were generated from the [ASF ContentInfo Object](asf-contentinfo-object.md) by a call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="333e2-114">Il formato della matrice di byte è il seguente:</span><span class="sxs-lookup"><span data-stu-id="333e2-114">The format of the byte array is as follows:</span></span>



| <span data-ttu-id="333e2-115">Campo oggetto elenco lingue</span><span class="sxs-lookup"><span data-stu-id="333e2-115">Language List Object field</span></span> | <span data-ttu-id="333e2-116">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="333e2-116">Data type</span></span>    | <span data-ttu-id="333e2-117">Dimensione</span><span class="sxs-lookup"><span data-stu-id="333e2-117">Size</span></span>    | <span data-ttu-id="333e2-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="333e2-118">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="333e2-119">Conteggio record ID lingua</span><span class="sxs-lookup"><span data-stu-id="333e2-119">Language ID Records Count</span></span>  | <span data-ttu-id="333e2-120">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="333e2-120">**DWORD**</span></span>    | <span data-ttu-id="333e2-121">4 byte</span><span class="sxs-lookup"><span data-stu-id="333e2-121">4 bytes</span></span> | <span data-ttu-id="333e2-122">Numero di lingue</span><span class="sxs-lookup"><span data-stu-id="333e2-122">Number of languages</span></span>                    |
| <span data-ttu-id="333e2-123">Record ID lingua</span><span class="sxs-lookup"><span data-stu-id="333e2-123">Language ID Records</span></span>        | <span data-ttu-id="333e2-124">**BYTE**\[\]</span><span class="sxs-lookup"><span data-stu-id="333e2-124">**BYTE**\[\]</span></span> | <span data-ttu-id="333e2-125">Varia</span><span class="sxs-lookup"><span data-stu-id="333e2-125">Varies</span></span>  | <span data-ttu-id="333e2-126">Matrice di stringhe di linguaggio (vedere di seguito).</span><span class="sxs-lookup"><span data-stu-id="333e2-126">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="333e2-127">Il primo **valore DWORD** è il numero di lingue, seguito da una matrice di stringhe dell'identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="333e2-127">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="333e2-128">Ogni stringa ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="333e2-128">Each string has the following format:</span></span>



| <span data-ttu-id="333e2-129">Campo oggetto elenco lingue</span><span class="sxs-lookup"><span data-stu-id="333e2-129">Language List Object field</span></span> | <span data-ttu-id="333e2-130">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="333e2-130">Data type</span></span>     | <span data-ttu-id="333e2-131">Dimensione</span><span class="sxs-lookup"><span data-stu-id="333e2-131">Size</span></span>    | <span data-ttu-id="333e2-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="333e2-132">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="333e2-133">Lunghezza ID lingua</span><span class="sxs-lookup"><span data-stu-id="333e2-133">Language ID Length</span></span>         | <span data-ttu-id="333e2-134">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="333e2-134">**DWORD**</span></span>     | <span data-ttu-id="333e2-135">4 byte</span><span class="sxs-lookup"><span data-stu-id="333e2-135">4 bytes</span></span> | <span data-ttu-id="333e2-136">Lunghezza della stringa in byte, incluse le dimensioni del carattere **null** finale.</span><span class="sxs-lookup"><span data-stu-id="333e2-136">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="333e2-137">ID lingua</span><span class="sxs-lookup"><span data-stu-id="333e2-137">Language ID</span></span>                | <span data-ttu-id="333e2-138">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="333e2-138">**WCHAR**\[\]</span></span> | <span data-ttu-id="333e2-139">Varia</span><span class="sxs-lookup"><span data-stu-id="333e2-139">Varies</span></span>  | <span data-ttu-id="333e2-140">Stringa con terminazione null che contiene il nome della lingua RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="333e2-140">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="333e2-141">Ogni stringa è un tag di lingua conforme a RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="333e2-141">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="333e2-142">Utilizzare questo attributo solo per compatibilità con le versioni precedenti con l'ordine di enumerazione dell'interfaccia [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="333e2-142">Use this attribute only for backward compatibility with the enumeration order of the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface in the Windows Media Format SDK.</span></span> <span data-ttu-id="333e2-143">Le stringhe della lingua sono archiviate in un ordine diverso nell'attributo [**lang di MF \_ PD \_ ASF \_**](mf-pd-asf-langlist-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="333e2-143">The language strings are stored in a different order in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="333e2-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="333e2-144">Requirements</span></span>



| <span data-ttu-id="333e2-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="333e2-145">Requirement</span></span> | <span data-ttu-id="333e2-146">Valore</span><span class="sxs-lookup"><span data-stu-id="333e2-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="333e2-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="333e2-147">Minimum supported client</span></span><br/> | <span data-ttu-id="333e2-148">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="333e2-148">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="333e2-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="333e2-149">Minimum supported server</span></span><br/> | <span data-ttu-id="333e2-150">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="333e2-150">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="333e2-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="333e2-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="333e2-152"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="333e2-152"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="333e2-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="333e2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="333e2-154">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="333e2-154">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="333e2-155">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="333e2-155">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
