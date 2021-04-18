---
description: Specifica un elenco di comandi di script e i parametri per un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto comando script nell'intestazione ASF, definito nella specifica ASF.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: Attributo MF_PD_ASF_SCRIPT (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03de86298d28183aa57cc80b451c4e46bb054de2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314545"
---
# <a name="mf_pd_asf_script-attribute"></a><span data-ttu-id="8652f-104">\_ \_ Attributo script MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="8652f-104">MF\_PD\_ASF\_SCRIPT attribute</span></span>

<span data-ttu-id="8652f-105">Specifica un elenco di comandi di script e i parametri per un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="8652f-105">Specifies a list of script commands and the parameters for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="8652f-106">Questo attributo corrisponde all'oggetto comando script nell'intestazione ASF, definito nella specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="8652f-106">This attribute corresponds to the Script Command Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="8652f-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8652f-107">Data type</span></span>

<span data-ttu-id="8652f-108">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="8652f-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="8652f-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="8652f-109">Remarks</span></span>

<span data-ttu-id="8652f-110">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="8652f-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="8652f-111">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea il descrittore di presentazione e genera questo attributo dall'intestazione dell'oggetto del comando per script.</span><span class="sxs-lookup"><span data-stu-id="8652f-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Script Command Object header.</span></span> <span data-ttu-id="8652f-112">La tabella seguente illustra il formato del BLOB:</span><span class="sxs-lookup"><span data-stu-id="8652f-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="8652f-113">Campo oggetto comando script</span><span class="sxs-lookup"><span data-stu-id="8652f-113">Script Command Object field</span></span> | <span data-ttu-id="8652f-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8652f-114">Data type</span></span>    | <span data-ttu-id="8652f-115">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8652f-115">Size</span></span>    | <span data-ttu-id="8652f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8652f-116">Description</span></span>               |
|-----------------------------|--------------|---------|---------------------------|
| <span data-ttu-id="8652f-117">Conteggio comandi</span><span class="sxs-lookup"><span data-stu-id="8652f-117">Commands Count</span></span>              | <span data-ttu-id="8652f-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="8652f-118">**DWORD**</span></span>    | <span data-ttu-id="8652f-119">4 byte</span><span class="sxs-lookup"><span data-stu-id="8652f-119">4 bytes</span></span> | <span data-ttu-id="8652f-120">Numero di comandi script</span><span class="sxs-lookup"><span data-stu-id="8652f-120">Number of script commands</span></span> |
| <span data-ttu-id="8652f-121">Tipo di comando, comandi</span><span class="sxs-lookup"><span data-stu-id="8652f-121">Command Type, Commands</span></span>      | <span data-ttu-id="8652f-122">**BYTE**\[\]</span><span class="sxs-lookup"><span data-stu-id="8652f-122">**BYTE**\[\]</span></span> | <span data-ttu-id="8652f-123">Varia</span><span class="sxs-lookup"><span data-stu-id="8652f-123">Varies</span></span>  | <span data-ttu-id="8652f-124">Matrice di comandi script</span><span class="sxs-lookup"><span data-stu-id="8652f-124">Array of script commands</span></span>  |



 

<span data-ttu-id="8652f-125">Il primo **valore DWORD** è il numero di comandi script, seguito da una matrice di comandi.</span><span class="sxs-lookup"><span data-stu-id="8652f-125">The first **DWORD** is the number of script commands, followed by an array of commands.</span></span> <span data-ttu-id="8652f-126">Ogni comando di script ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="8652f-126">Each script command has the following format:</span></span>



| <span data-ttu-id="8652f-127">Campo oggetto comando script</span><span class="sxs-lookup"><span data-stu-id="8652f-127">Script Command Object field</span></span> | <span data-ttu-id="8652f-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8652f-128">Data type</span></span>     | <span data-ttu-id="8652f-129">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8652f-129">Size</span></span>    | <span data-ttu-id="8652f-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8652f-130">Description</span></span>                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| <span data-ttu-id="8652f-131">Lunghezza del nome del comando</span><span class="sxs-lookup"><span data-stu-id="8652f-131">Command Name Length</span></span>         | <span data-ttu-id="8652f-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="8652f-132">**DWORD**</span></span>     | <span data-ttu-id="8652f-133">4 byte</span><span class="sxs-lookup"><span data-stu-id="8652f-133">4 bytes</span></span> | <span data-ttu-id="8652f-134">Dimensione della stringa di comando, in byte, incluso il carattere NULL.</span><span class="sxs-lookup"><span data-stu-id="8652f-134">Size of the command string, in bytes, including the NULL character.</span></span>      |
| <span data-ttu-id="8652f-135">Nome comando</span><span class="sxs-lookup"><span data-stu-id="8652f-135">Command Name</span></span>                | <span data-ttu-id="8652f-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="8652f-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="8652f-137">Varia</span><span class="sxs-lookup"><span data-stu-id="8652f-137">Varies</span></span>  | <span data-ttu-id="8652f-138">Stringa con terminazione null che contiene il comando script.</span><span class="sxs-lookup"><span data-stu-id="8652f-138">Null-terminated string that contains the script command.</span></span>                 |
| <span data-ttu-id="8652f-139">Lunghezza del nome del tipo di comando</span><span class="sxs-lookup"><span data-stu-id="8652f-139">Command Type Name Length</span></span>    | <span data-ttu-id="8652f-140">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="8652f-140">**DWORD**</span></span>     | <span data-ttu-id="8652f-141">4 byte</span><span class="sxs-lookup"><span data-stu-id="8652f-141">4 bytes</span></span> | <span data-ttu-id="8652f-142">Dimensione della stringa del tipo di comando, in byte, incluso il carattere NULL.</span><span class="sxs-lookup"><span data-stu-id="8652f-142">Size of the command type string, in bytes, including the NULL character.</span></span> |
| <span data-ttu-id="8652f-143">Nome tipo di comando</span><span class="sxs-lookup"><span data-stu-id="8652f-143">Command Type Name</span></span>           | <span data-ttu-id="8652f-144">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="8652f-144">**WCHAR**\[\]</span></span> | <span data-ttu-id="8652f-145">Varia</span><span class="sxs-lookup"><span data-stu-id="8652f-145">Varies</span></span>  | <span data-ttu-id="8652f-146">Stringa con terminazione null che contiene il tipo di comando.</span><span class="sxs-lookup"><span data-stu-id="8652f-146">Null-terminated string that contains the command type.</span></span>                   |
| <span data-ttu-id="8652f-147">Ora di presentazione</span><span class="sxs-lookup"><span data-stu-id="8652f-147">Presentation Time</span></span>           | <span data-ttu-id="8652f-148">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="8652f-148">**DWORD**</span></span>     | <span data-ttu-id="8652f-149">4 byte</span><span class="sxs-lookup"><span data-stu-id="8652f-149">4 bytes</span></span> | <span data-ttu-id="8652f-150">Tempo di presentazione del comando in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="8652f-150">Presentation time of the command in milliseconds.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="8652f-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8652f-151">Requirements</span></span>



| <span data-ttu-id="8652f-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="8652f-152">Requirement</span></span> | <span data-ttu-id="8652f-153">Valore</span><span class="sxs-lookup"><span data-stu-id="8652f-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8652f-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8652f-154">Minimum supported client</span></span><br/> | <span data-ttu-id="8652f-155">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8652f-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8652f-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8652f-156">Minimum supported server</span></span><br/> | <span data-ttu-id="8652f-157">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8652f-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8652f-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8652f-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="8652f-159"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="8652f-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8652f-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8652f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8652f-161">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8652f-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8652f-162">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="8652f-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="8652f-163">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="8652f-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="8652f-164">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8652f-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="8652f-165">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="8652f-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="8652f-166">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="8652f-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="8652f-167">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="8652f-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




