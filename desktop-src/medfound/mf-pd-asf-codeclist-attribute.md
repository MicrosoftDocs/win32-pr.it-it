---
description: Contiene informazioni sui codec e i formati utilizzati per codificare il contenuto in un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto elenco di codec nell'intestazione ASF, definito nella specifica ASF.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: Attributo MF_PD_ASF_CODECLIST (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316440"
---
# <a name="mf_pd_asf_codeclist-attribute"></a><span data-ttu-id="bf939-104">\_ \_ \_ Attributo codecs MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="bf939-104">MF\_PD\_ASF\_CODECLIST attribute</span></span>

<span data-ttu-id="bf939-105">Contiene informazioni sui codec e i formati utilizzati per codificare il contenuto in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="bf939-105">Contains information about the codecs and formats that were used to encode the content in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="bf939-106">Questo attributo corrisponde all'oggetto elenco di codec nell'intestazione ASF, definito nella specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="bf939-106">This attribute corresponds to the Codec List Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="bf939-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bf939-107">Data type</span></span>

<span data-ttu-id="bf939-108">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="bf939-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="bf939-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf939-109">Remarks</span></span>

<span data-ttu-id="bf939-110">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="bf939-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="bf939-111">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea il descrittore di presentazione e genera questo attributo dall'oggetto elenco di codec nell'intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="bf939-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Codec List Object in the ASF header.</span></span> <span data-ttu-id="bf939-112">Un'applicazione che usa l' [origine dei supporti ASF](asf-media-source.md) può ottenere questo attributo chiamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) e quindi recuperando l'attributo dal descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="bf939-112">An application that uses the [ASF Media Source](asf-media-source.md) can get this attribute by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) and then getting the attribute from the presentation descriptor.</span></span>

<span data-ttu-id="bf939-113">La tabella seguente illustra il layout del BLOB dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="bf939-113">The following table shows the layout of the attribute blob.</span></span>



| <span data-ttu-id="bf939-114">Campo oggetto elenco di codec</span><span class="sxs-lookup"><span data-stu-id="bf939-114">Codec List Object field</span></span> | <span data-ttu-id="bf939-115">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bf939-115">Data type</span></span>    | <span data-ttu-id="bf939-116">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bf939-116">Size</span></span>    | <span data-ttu-id="bf939-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf939-117">Description</span></span>                           |
|-------------------------|--------------|---------|---------------------------------------|
| <span data-ttu-id="bf939-118">Conteggio voci codec</span><span class="sxs-lookup"><span data-stu-id="bf939-118">Codec Entries Count</span></span>     | <span data-ttu-id="bf939-119">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="bf939-119">**DWORD**</span></span>    | <span data-ttu-id="bf939-120">4 byte</span><span class="sxs-lookup"><span data-stu-id="bf939-120">4 bytes</span></span> | <span data-ttu-id="bf939-121">Numero di codec</span><span class="sxs-lookup"><span data-stu-id="bf939-121">Number of codecs</span></span>                      |
| <span data-ttu-id="bf939-122">Voci di codec</span><span class="sxs-lookup"><span data-stu-id="bf939-122">Codec Entries</span></span>           | <span data-ttu-id="bf939-123">**BYTE**\[\]</span><span class="sxs-lookup"><span data-stu-id="bf939-123">**BYTE**\[\]</span></span> | <span data-ttu-id="bf939-124">Varia</span><span class="sxs-lookup"><span data-stu-id="bf939-124">Varies</span></span>  | <span data-ttu-id="bf939-125">Matrice di strutture di informazioni sui codec</span><span class="sxs-lookup"><span data-stu-id="bf939-125">Array of codec information structures</span></span> |



 

<span data-ttu-id="bf939-126">Il campo voci di codice è una matrice di strutture.</span><span class="sxs-lookup"><span data-stu-id="bf939-126">The Code Entries field is an array of structures.</span></span> <span data-ttu-id="bf939-127">La tabella seguente mostra il formato di ogni voce:</span><span class="sxs-lookup"><span data-stu-id="bf939-127">The following table shows the format of each entry:</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf939-128">Campo oggetto elenco di codec</span><span class="sxs-lookup"><span data-stu-id="bf939-128">Codec List Object field</span></span></th>
<th><span data-ttu-id="bf939-129">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bf939-129">Data type</span></span></th>
<th><span data-ttu-id="bf939-130">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bf939-130">Size</span></span></th>
<th><span data-ttu-id="bf939-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf939-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf939-132">Type</span><span class="sxs-lookup"><span data-stu-id="bf939-132">Type</span></span></td>
<td><span data-ttu-id="bf939-133"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="bf939-133"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="bf939-134">4 byte</span><span class="sxs-lookup"><span data-stu-id="bf939-134">4 bytes</span></span></td>
<td><span data-ttu-id="bf939-135">Tipo di codec.</span><span class="sxs-lookup"><span data-stu-id="bf939-135">Codec type.</span></span> <span data-ttu-id="bf939-136">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf939-136">This can be one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="bf939-137">0x0001: codec audio</span><span class="sxs-lookup"><span data-stu-id="bf939-137">0x0001: Audio codec</span></span></li>
<li><span data-ttu-id="bf939-138">0x0002: codec video</span><span class="sxs-lookup"><span data-stu-id="bf939-138">0x0002: Video codec</span></span></li>
<li><span data-ttu-id="bf939-139">0xFFFF: sconosciuto</span><span class="sxs-lookup"><span data-stu-id="bf939-139">0xFFFF: Unknown</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf939-140">Lunghezza del nome del codec</span><span class="sxs-lookup"><span data-stu-id="bf939-140">Codec Name Length</span></span></td>
<td><span data-ttu-id="bf939-141"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="bf939-141"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="bf939-142">4 byte</span><span class="sxs-lookup"><span data-stu-id="bf939-142">4 bytes</span></span></td>
<td><span data-ttu-id="bf939-143">Dimensione della stringa del nome del codec, in byte, incluso il carattere <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="bf939-143">Size of the Codec Name string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf939-144">Nome codec</span><span class="sxs-lookup"><span data-stu-id="bf939-144">Codec Name</span></span></td>
<td><span data-ttu-id="bf939-145"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="bf939-145"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="bf939-146">Varia</span><span class="sxs-lookup"><span data-stu-id="bf939-146">Varies</span></span></td>
<td><span data-ttu-id="bf939-147">Stringa Unicode con terminazione null che contiene il nome del codec, ad esempio &quot; Windows Media video 9 &quot; .</span><span class="sxs-lookup"><span data-stu-id="bf939-147">Null-terminated Unicode string that contains the name of the codec, such as &quot;Windows Media Video 9&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf939-148">Lunghezza Descrizione codec</span><span class="sxs-lookup"><span data-stu-id="bf939-148">Codec Description Length</span></span></td>
<td><span data-ttu-id="bf939-149"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="bf939-149"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="bf939-150">4 byte</span><span class="sxs-lookup"><span data-stu-id="bf939-150">4 bytes</span></span></td>
<td><span data-ttu-id="bf939-151">Dimensione della stringa di descrizione del codec, in byte, incluso il carattere <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="bf939-151">Size of the Codec Description string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf939-152">Descrizione codec</span><span class="sxs-lookup"><span data-stu-id="bf939-152">Codec Description</span></span></td>
<td><span data-ttu-id="bf939-153"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="bf939-153"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="bf939-154">Varia</span><span class="sxs-lookup"><span data-stu-id="bf939-154">Varies</span></span></td>
<td><span data-ttu-id="bf939-155">Stringa Unicode con terminazione null che contiene una descrizione del codec.</span><span class="sxs-lookup"><span data-stu-id="bf939-155">A null-terminated Unicode string that contains a description of the codec.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf939-156">Lunghezza informazioni codec</span><span class="sxs-lookup"><span data-stu-id="bf939-156">Codec Information Length</span></span></td>
<td><span data-ttu-id="bf939-157"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="bf939-157"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="bf939-158">4 byte</span><span class="sxs-lookup"><span data-stu-id="bf939-158">4 bytes</span></span></td>
<td><span data-ttu-id="bf939-159">Dimensioni in byte del campo informazioni sul codec.</span><span class="sxs-lookup"><span data-stu-id="bf939-159">Size of the Codec Information field, in bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf939-160">Informazioni sui codec</span><span class="sxs-lookup"><span data-stu-id="bf939-160">Codec Information</span></span></td>
<td><span data-ttu-id="bf939-161"><strong>Byte</strong>[]</span><span class="sxs-lookup"><span data-stu-id="bf939-161"><strong>BYTE</strong>[]</span></span></td>
<td><span data-ttu-id="bf939-162">Varia</span><span class="sxs-lookup"><span data-stu-id="bf939-162">Varies</span></span></td>
<td><span data-ttu-id="bf939-163">Dati di codec.</span><span class="sxs-lookup"><span data-stu-id="bf939-163">Codec data.</span></span> <span data-ttu-id="bf939-164">Il significato di questi dati dipende dal codec.</span><span class="sxs-lookup"><span data-stu-id="bf939-164">The meaning of this data depends on the codec.</span></span> <span data-ttu-id="bf939-165">In genere, questi dati indicano il formato.</span><span class="sxs-lookup"><span data-stu-id="bf939-165">Typically, this data indicates the format.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="bf939-166">Il layout del BLOB dell'attributo non corrisponde esattamente al layout dell'oggetto elenco di codec nell'intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="bf939-166">The layout of the attribute blob does not exactly match the layout of the Codec List Object in the ASF header.</span></span> <span data-ttu-id="bf939-167">In particolare, le lunghezze di stringa sono specificate in byte e includono le dimensioni del carattere di terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="bf939-167">In particular, string lengths are given in bytes and include the size of the **NULL** terminator.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf939-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf939-168">Requirements</span></span>



| <span data-ttu-id="bf939-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf939-169">Requirement</span></span> | <span data-ttu-id="bf939-170">Valore</span><span class="sxs-lookup"><span data-stu-id="bf939-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf939-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf939-171">Minimum supported client</span></span><br/> | <span data-ttu-id="bf939-172">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf939-172">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bf939-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf939-173">Minimum supported server</span></span><br/> | <span data-ttu-id="bf939-174">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf939-174">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bf939-175">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf939-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf939-176"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf939-176"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf939-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf939-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf939-178">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf939-178">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bf939-179">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="bf939-179">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="bf939-180">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="bf939-180">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="bf939-181">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="bf939-181">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="bf939-182">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="bf939-182">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="bf939-183">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="bf939-183">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="bf939-184">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="bf939-184">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




