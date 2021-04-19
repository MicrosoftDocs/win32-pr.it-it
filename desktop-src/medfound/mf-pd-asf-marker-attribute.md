---
description: Specifica i marcatori in un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto marcatore nell'intestazione ASF, definito nella specifica ASF.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: Attributo MF_PD_ASF_MARKER (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318059"
---
# <a name="mf_pd_asf_marker-attribute"></a><span data-ttu-id="71604-104">\_ \_ \_ Attributo marcatore ASF MF PD</span><span class="sxs-lookup"><span data-stu-id="71604-104">MF\_PD\_ASF\_MARKER attribute</span></span>

<span data-ttu-id="71604-105">Specifica i marcatori in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="71604-105">Specifies the markers in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="71604-106">Questo attributo corrisponde all'oggetto marcatore nell'intestazione ASF, definito nella specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="71604-106">This attribute corresponds to the Marker Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="71604-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="71604-107">Data type</span></span>

<span data-ttu-id="71604-108">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="71604-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="71604-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="71604-109">Remarks</span></span>

<span data-ttu-id="71604-110">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="71604-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="71604-111">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea il descrittore di presentazione e genera questo attributo dall'oggetto marcatore.</span><span class="sxs-lookup"><span data-stu-id="71604-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Marker Object.</span></span> <span data-ttu-id="71604-112">La tabella seguente illustra il formato del BLOB:</span><span class="sxs-lookup"><span data-stu-id="71604-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="71604-113">Campo oggetto marcatore</span><span class="sxs-lookup"><span data-stu-id="71604-113">Marker Object field</span></span> | <span data-ttu-id="71604-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="71604-114">Data type</span></span>    | <span data-ttu-id="71604-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="71604-115">Size</span></span>    | <span data-ttu-id="71604-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71604-116">Description</span></span>       |
|---------------------|--------------|---------|-------------------|
| <span data-ttu-id="71604-117">Conteggio marcatori</span><span class="sxs-lookup"><span data-stu-id="71604-117">Markers Count</span></span>       | <span data-ttu-id="71604-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="71604-118">**DWORD**</span></span>    | <span data-ttu-id="71604-119">4 byte</span><span class="sxs-lookup"><span data-stu-id="71604-119">4 bytes</span></span> | <span data-ttu-id="71604-120">Numero di marcatori</span><span class="sxs-lookup"><span data-stu-id="71604-120">Number of markers</span></span> |
| <span data-ttu-id="71604-121">Indicatori</span><span class="sxs-lookup"><span data-stu-id="71604-121">Markers</span></span>             | <span data-ttu-id="71604-122">**BYTE**\[\]</span><span class="sxs-lookup"><span data-stu-id="71604-122">**BYTE**\[\]</span></span> | <span data-ttu-id="71604-123">Varia</span><span class="sxs-lookup"><span data-stu-id="71604-123">Varies</span></span>  | <span data-ttu-id="71604-124">Matrice di marcatori</span><span class="sxs-lookup"><span data-stu-id="71604-124">Array of markers</span></span>  |



 

<span data-ttu-id="71604-125">Il primo **valore DWORD** è il numero di marcatori, seguiti da una matrice di marcatori.</span><span class="sxs-lookup"><span data-stu-id="71604-125">The first **DWORD** is the number of markers, followed by an array of markers.</span></span> <span data-ttu-id="71604-126">Ogni marcatore ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="71604-126">Each marker has the following format:</span></span>



| <span data-ttu-id="71604-127">Campo oggetto marcatore</span><span class="sxs-lookup"><span data-stu-id="71604-127">Marker Object field</span></span>       | <span data-ttu-id="71604-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="71604-128">Data type</span></span>     | <span data-ttu-id="71604-129">Dimensione</span><span class="sxs-lookup"><span data-stu-id="71604-129">Size</span></span>    | <span data-ttu-id="71604-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71604-130">Description</span></span>                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="71604-131">Lunghezza Descrizione indicatore</span><span class="sxs-lookup"><span data-stu-id="71604-131">Marker Description Length</span></span> | <span data-ttu-id="71604-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="71604-132">**DWORD**</span></span>     | <span data-ttu-id="71604-133">4 byte</span><span class="sxs-lookup"><span data-stu-id="71604-133">4 bytes</span></span> | <span data-ttu-id="71604-134">Dimensione della stringa di descrizione, in byte, incluso il carattere NULL.</span><span class="sxs-lookup"><span data-stu-id="71604-134">Size of the description string, in bytes, including the NULL character.</span></span>           |
| <span data-ttu-id="71604-135">Descrizione indicatore</span><span class="sxs-lookup"><span data-stu-id="71604-135">Marker Description</span></span>        | <span data-ttu-id="71604-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="71604-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="71604-137">Varia</span><span class="sxs-lookup"><span data-stu-id="71604-137">Varies</span></span>  | <span data-ttu-id="71604-138">Stringa con terminazione null che descrive il marcatore.</span><span class="sxs-lookup"><span data-stu-id="71604-138">Null-terminated string that describes the marker.</span></span>                                 |
| <span data-ttu-id="71604-139">Ora di presentazione</span><span class="sxs-lookup"><span data-stu-id="71604-139">Presentation Time</span></span>         | <span data-ttu-id="71604-140">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="71604-140">**LONGLONG**</span></span>  | <span data-ttu-id="71604-141">8 byte</span><span class="sxs-lookup"><span data-stu-id="71604-141">8 bytes</span></span> | <span data-ttu-id="71604-142">Tempo di presentazione del marcatore, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="71604-142">Presentation time of the marker, in 100-nanosecond units.</span></span>                         |
| <span data-ttu-id="71604-143">Ora di invio</span><span class="sxs-lookup"><span data-stu-id="71604-143">Send Time</span></span>                 | <span data-ttu-id="71604-144">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="71604-144">**LONGLONG**</span></span>  | <span data-ttu-id="71604-145">8 byte</span><span class="sxs-lookup"><span data-stu-id="71604-145">8 bytes</span></span> | <span data-ttu-id="71604-146">Tempo di invio della voce del marcatore, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="71604-146">Send time of the marker entry, in milliseconds.</span></span>                                   |
| <span data-ttu-id="71604-147">Offset</span><span class="sxs-lookup"><span data-stu-id="71604-147">Offset</span></span>                    | <span data-ttu-id="71604-148">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="71604-148">**UINT64**</span></span>    | <span data-ttu-id="71604-149">8 byte</span><span class="sxs-lookup"><span data-stu-id="71604-149">8 bytes</span></span> | <span data-ttu-id="71604-150">Offset, in byte, nell'oggetto dati che specifica la posizione del mercato.</span><span class="sxs-lookup"><span data-stu-id="71604-150">Offset, in bytes, into the Data Object that specifies the position of the market.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="71604-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71604-151">Requirements</span></span>



| <span data-ttu-id="71604-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="71604-152">Requirement</span></span> | <span data-ttu-id="71604-153">Valore</span><span class="sxs-lookup"><span data-stu-id="71604-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="71604-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71604-154">Minimum supported client</span></span><br/> | <span data-ttu-id="71604-155">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71604-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="71604-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71604-156">Minimum supported server</span></span><br/> | <span data-ttu-id="71604-157">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71604-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="71604-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71604-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="71604-159"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="71604-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71604-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71604-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71604-161">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="71604-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="71604-162">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="71604-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="71604-163">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="71604-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="71604-164">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="71604-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="71604-165">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="71604-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="71604-166">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="71604-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="71604-167">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="71604-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




