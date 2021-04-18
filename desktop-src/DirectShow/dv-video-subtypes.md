---
description: Per il video DV sono definiti diversi sottotipi. Ogni ha un codice FOURCC e un valore GUID corrispondente. Non tutti questi formati sono supportati. Per ulteriori informazioni, vedere la sezione Osservazioni.
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: Sottotipi video DV (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330828"
---
# <a name="dv-video-subtypes"></a><span data-ttu-id="f9f0e-105">Sottotipi video DV</span><span class="sxs-lookup"><span data-stu-id="f9f0e-105">DV Video Subtypes</span></span>

<span data-ttu-id="f9f0e-106">Per il video DV sono definiti diversi sottotipi.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-106">A number of subtypes are defined for DV video.</span></span> <span data-ttu-id="f9f0e-107">Ogni ha un codice FOURCC e un valore GUID corrispondente.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-107">Each has a FOURCC code and a corresponding GUID value.</span></span> <span data-ttu-id="f9f0e-108">Non tutti questi formati sono supportati. Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-108">Not all of these formats are supported; see the Remarks section for more information.</span></span>

## <a name="consumer-formats"></a><span data-ttu-id="f9f0e-109">Formati utente</span><span class="sxs-lookup"><span data-stu-id="f9f0e-109">Consumer Formats</span></span>



| <span data-ttu-id="f9f0e-110">FOURCC</span><span class="sxs-lookup"><span data-stu-id="f9f0e-110">FOURCC</span></span> | <span data-ttu-id="f9f0e-111">GUID</span><span class="sxs-lookup"><span data-stu-id="f9f0e-111">GUID</span></span>               | <span data-ttu-id="f9f0e-112">Velocità dati</span><span class="sxs-lookup"><span data-stu-id="f9f0e-112">Data Rate</span></span> | <span data-ttu-id="f9f0e-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9f0e-113">Description</span></span>                  |
|--------|--------------------|-----------|------------------------------|
| <span data-ttu-id="f9f0e-114">'dvsl'</span><span class="sxs-lookup"><span data-stu-id="f9f0e-114">'dvsl'</span></span> | <span data-ttu-id="f9f0e-115">\_DVSL MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="f9f0e-115">MEDIASUBTYPE\_dvsl</span></span> | <span data-ttu-id="f9f0e-116">12,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="f9f0e-116">12.5 Mbps</span></span> | <span data-ttu-id="f9f0e-117">SD-DVCR (525-60 o 625-50)</span><span class="sxs-lookup"><span data-stu-id="f9f0e-117">SD-DVCR (525-60 or 625-50)</span></span>   |
| <span data-ttu-id="f9f0e-118">DVSD</span><span class="sxs-lookup"><span data-stu-id="f9f0e-118">'dvsd'</span></span> | <span data-ttu-id="f9f0e-119">\_DVSD MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="f9f0e-119">MEDIASUBTYPE\_dvsd</span></span> | <span data-ttu-id="f9f0e-120">25 Mbps</span><span class="sxs-lookup"><span data-stu-id="f9f0e-120">25 Mbps</span></span>   | <span data-ttu-id="f9f0e-121">SDL-DVCR (525-60 o 625-50)</span><span class="sxs-lookup"><span data-stu-id="f9f0e-121">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="f9f0e-122">'dvhd'</span><span class="sxs-lookup"><span data-stu-id="f9f0e-122">'dvhd'</span></span> | <span data-ttu-id="f9f0e-123">\_DVHD MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="f9f0e-123">MEDIASUBTYPE\_dvhd</span></span> | <span data-ttu-id="f9f0e-124">50 Mbps</span><span class="sxs-lookup"><span data-stu-id="f9f0e-124">50 Mbps</span></span>   | <span data-ttu-id="f9f0e-125">HD-DVCR (1125-60 o 1250-50)</span><span class="sxs-lookup"><span data-stu-id="f9f0e-125">HD-DVCR (1125-60 or 1250-50)</span></span> |



 

<span data-ttu-id="f9f0e-126">Per ulteriori informazioni su questi formati, vedere IEC-61834.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-126">Refer to IEC-61834 for more information about these formats.</span></span>

## <a name="professional-formats"></a><span data-ttu-id="f9f0e-127">Formati professionali</span><span class="sxs-lookup"><span data-stu-id="f9f0e-127">Professional Formats</span></span>



| <span data-ttu-id="f9f0e-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="f9f0e-128">FOURCC</span></span> | <span data-ttu-id="f9f0e-129">GUID</span><span class="sxs-lookup"><span data-stu-id="f9f0e-129">GUID</span></span>               | <span data-ttu-id="f9f0e-130">Velocità dati</span><span class="sxs-lookup"><span data-stu-id="f9f0e-130">Data Rate</span></span> | <span data-ttu-id="f9f0e-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9f0e-131">Description</span></span>                                 |
|--------|--------------------|-----------|---------------------------------------------|
| <span data-ttu-id="f9f0e-132">DV25</span><span class="sxs-lookup"><span data-stu-id="f9f0e-132">'dv25'</span></span> | <span data-ttu-id="f9f0e-133">\_DV25 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="f9f0e-133">MEDIASUBTYPE\_dv25</span></span> | <span data-ttu-id="f9f0e-134">25 Mbps</span><span class="sxs-lookup"><span data-stu-id="f9f0e-134">25 Mbps</span></span>   | <span data-ttu-id="f9f0e-135">DVCPRO 25 (525-60 o 625-50).</span><span class="sxs-lookup"><span data-stu-id="f9f0e-135">DVCPRO 25 (525-60 or 625-50).</span></span>               |
| <span data-ttu-id="f9f0e-136">DV50</span><span class="sxs-lookup"><span data-stu-id="f9f0e-136">'dv50'</span></span> | <span data-ttu-id="f9f0e-137">\_DV50 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="f9f0e-137">MEDIASUBTYPE\_dv50</span></span> | <span data-ttu-id="f9f0e-138">50 Mbps</span><span class="sxs-lookup"><span data-stu-id="f9f0e-138">50 Mbps</span></span>   | <span data-ttu-id="f9f0e-139">DVCPRO 50 (525-60 o 625-50)</span><span class="sxs-lookup"><span data-stu-id="f9f0e-139">DVCPRO 50 (525-60 or 625-50)</span></span>                |
| <span data-ttu-id="f9f0e-140">'dvh1'</span><span class="sxs-lookup"><span data-stu-id="f9f0e-140">'dvh1'</span></span> | <span data-ttu-id="f9f0e-141">\_DVH1 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="f9f0e-141">MEDIASUBTYPE\_dvh1</span></span> | <span data-ttu-id="f9f0e-142">100 Mbps</span><span class="sxs-lookup"><span data-stu-id="f9f0e-142">100 Mbps</span></span>  | <span data-ttu-id="f9f0e-143">DVCPRO 100 (1080/60i, 1080/50i o 720/60P)</span><span class="sxs-lookup"><span data-stu-id="f9f0e-143">DVCPRO 100 (1080/60i, 1080/50i, or 720/60P)</span></span> |



 

<span data-ttu-id="f9f0e-144">Per ulteriori informazioni su dvh1, vedere SMPTE 314M per ulteriori informazioni su DV25 e DV50 e SMPTE 370M.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-144">Refer to SMPTE 314M for more information about dv25 and dv50, and SMPTE 370M for more information about dvh1.</span></span>

## <a name="miscellaneous"></a><span data-ttu-id="f9f0e-145">Varie</span><span class="sxs-lookup"><span data-stu-id="f9f0e-145">Miscellaneous</span></span>

<span data-ttu-id="f9f0e-146">Nel file di intestazione UUIDs. h sono definiti due sottotipi DV aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-146">Two additional DV subtypes are defined in the header file Uuids.h.</span></span> <span data-ttu-id="f9f0e-147">Questi corrispondono ai codici FOURCC prodotti da determinati codec DV; non corrispondono ad alcun standard DV definito.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-147">These correspond to FOURCC codes that are produced by certain DV codecs; they do not correspond to any defined DV standards.</span></span> <span data-ttu-id="f9f0e-148">Questi sottotipi sono obsoleti e non devono essere usati.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-148">These subtypes are obsolete and should not be used.</span></span>



| <span data-ttu-id="f9f0e-149">FOURCC</span><span class="sxs-lookup"><span data-stu-id="f9f0e-149">FOURCC</span></span> | <span data-ttu-id="f9f0e-150">GUID</span><span class="sxs-lookup"><span data-stu-id="f9f0e-150">GUID</span></span>               |
|--------|--------------------|
| <span data-ttu-id="f9f0e-151">DVCS</span><span class="sxs-lookup"><span data-stu-id="f9f0e-151">'DVCS'</span></span> | <span data-ttu-id="f9f0e-152">\_DVCS MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="f9f0e-152">MEDIASUBTYPE\_DVCS</span></span> |
| <span data-ttu-id="f9f0e-153">DVSD</span><span class="sxs-lookup"><span data-stu-id="f9f0e-153">'DVSD'</span></span> | <span data-ttu-id="f9f0e-154">\_DVSD MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="f9f0e-154">MEDIASUBTYPE\_DVSD</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f9f0e-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9f0e-155">Remarks</span></span>

<span data-ttu-id="f9f0e-156">La tabella seguente mostra le frequenze dati supportate, in megabit al secondo (Mbps), per i driver MSDV e UVC.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-156">The following table shows the supported data rates, in megabits per second (Mbps), for the MSDV and UVC drivers.</span></span>



| <span data-ttu-id="f9f0e-157">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f9f0e-157">Operating System</span></span>                                                                 | <span data-ttu-id="f9f0e-158">Driver MSDV (IEEE 1394)</span><span class="sxs-lookup"><span data-stu-id="f9f0e-158">MSDV (IEEE 1394) Driver</span></span> | <span data-ttu-id="f9f0e-159">Driver UVC</span><span class="sxs-lookup"><span data-stu-id="f9f0e-159">UVC Driver</span></span>    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| <span data-ttu-id="f9f0e-160">Windows XP Service Pack 1 o versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="f9f0e-160">Windows XP Service Pack 1 or earlier</span></span>                                             | <span data-ttu-id="f9f0e-161">12,5, 25</span><span class="sxs-lookup"><span data-stu-id="f9f0e-161">12.5, 25</span></span>                | <span data-ttu-id="f9f0e-162">Non disponibile</span><span class="sxs-lookup"><span data-stu-id="f9f0e-162">Not available</span></span> |
| <span data-ttu-id="f9f0e-163">Windows XP Service Pack 2 o versione successiva, Windows Server 2003 Service Pack 1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-163">Windows XP Service Pack 2 or later, Windows Server 2003 Service Pack 1 or later.</span></span> | <span data-ttu-id="f9f0e-164">12,5, 25, 50, 100</span><span class="sxs-lookup"><span data-stu-id="f9f0e-164">12.5, 25, 50, 100</span></span>       | <span data-ttu-id="f9f0e-165">12,5, 25</span><span class="sxs-lookup"><span data-stu-id="f9f0e-165">12.5, 25</span></span>      |



 

<span data-ttu-id="f9f0e-166">Per i flussi a 25 Mbps, il comportamento del driver MSDV è stato modificato in Windows Vista prima di Windows Vista, il driver MSDV imposta sempre il tipo di supporto su MEDIASUBTYPE \_ DVSD per i flussi a 25 Mbps, indipendentemente dal fatto che l'origine sia SDL-DVCR o DVCPRO 25.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-166">For 25-Mbps streams, the behavior of the MSDV driver has changed in Windows Vista Prior to Windows Vista, the MSDV driver always set the media type to MEDIASUBTYPE\_dvsd for 25-Mbps streams, regardless of whether the source was SDL-DVCR or DVCPRO 25.</span></span> <span data-ttu-id="f9f0e-167">Il tipo di supporto ' DV25' non è stato usato.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-167">The 'dv25' media type was not used.</span></span> <span data-ttu-id="f9f0e-168">A partire da Windows Vista, il driver MSDV ora distingue tra questi due formati.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-168">Starting with Windows Vista, the MSDV driver now distinguishes between these two formats.</span></span> <span data-ttu-id="f9f0e-169">Per SDL-DVCR, continua a usare il sottotipo ' DVSD '.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-169">For SDL-DVCR, it continues to use the 'dvsd' subtype.</span></span> <span data-ttu-id="f9f0e-170">Per DVCPRO 25 USA ora il sottotipo ' DV25'.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-170">For DVCPRO 25, it now uses the 'dv25' subtype.</span></span>

<span data-ttu-id="f9f0e-171">I filtri di [decodificatore](dv-video-decoder-filter.md) DirectShow [DV](dv-splitter-filter.md) e DV video supportano solo i formati SDL-DVCR.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-171">The DirectShow [DV Splitter](dv-splitter-filter.md) and [DV Video Decoder](dv-video-decoder-filter.md) filters support SDL-DVCR formats only.</span></span> <span data-ttu-id="f9f0e-172">I dati possono essere PAL o NTSC.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-172">The data can be PAL or NTSC.</span></span> <span data-ttu-id="f9f0e-173">È possibile che siano disponibili filtri o codec di terze parti in grado di analizzare altri formati DV, purché la velocità dati sia supportata dal driver MSDV o UVC.</span><span class="sxs-lookup"><span data-stu-id="f9f0e-173">Third-party filters or codecs may be available that can parse other DV formats, as long as the data rate is supported by the MSDV or UVC driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9f0e-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9f0e-174">Requirements</span></span>



| <span data-ttu-id="f9f0e-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9f0e-175">Requirement</span></span> | <span data-ttu-id="f9f0e-176">Valore</span><span class="sxs-lookup"><span data-stu-id="f9f0e-176">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f0e-177">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9f0e-177">Header</span></span><br/> | <dl> <span data-ttu-id="f9f0e-178"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9f0e-178"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9f0e-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9f0e-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f0e-180">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f9f0e-180">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="f9f0e-181">Driver MSDV</span><span class="sxs-lookup"><span data-stu-id="f9f0e-181">MSDV Driver</span></span>](msdv-driver.md)
</dt> <dt>

[<span data-ttu-id="f9f0e-182">Sottotipi video</span><span class="sxs-lookup"><span data-stu-id="f9f0e-182">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




