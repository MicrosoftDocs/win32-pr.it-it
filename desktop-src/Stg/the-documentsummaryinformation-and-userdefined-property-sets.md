---
title: Set di proprietà DocumentSummaryInformation e UserDefined
description: Un set di proprietà DocumentSummaryInformation e UserDefined è un'estensione del set di proprietà informazioni di riepilogo. Entrambi i set di proprietà possono esistere simultaneamente.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- Set di Proprietà UserDefined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515721"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a><span data-ttu-id="dd719-106">Set di proprietà DocumentSummaryInformation e UserDefined</span><span class="sxs-lookup"><span data-stu-id="dd719-106">The DocumentSummaryInformation and UserDefined Property Sets</span></span>

<span data-ttu-id="dd719-107">Un set di proprietà **DocumentSummaryInformation** e **UserDefined** è un'estensione [del set di proprietà informazioni di riepilogo](the-summary-information-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="dd719-107">A **DocumentSummaryInformation** and **UserDefined** property set is an extension to [the Summary Information property set](the-summary-information-property-set.md).</span></span> <span data-ttu-id="dd719-108">Entrambi i set di proprietà possono esistere simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="dd719-108">Both property sets can exist simultaneously.</span></span>

<span data-ttu-id="dd719-109">Il nome del flusso che contiene il set di proprietà **DocumentSummaryInformation** è **" \\ 005DocumentSummaryInformation"**.</span><span class="sxs-lookup"><span data-stu-id="dd719-109">The name of the stream that contains the **DocumentSummaryInformation** property set is **"\\005DocumentSummaryInformation"**.</span></span> <span data-ttu-id="dd719-110">L'identificatore di formato (FMTID) per il set di proprietà **DocumentSummaryInformation** è **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span><span class="sxs-lookup"><span data-stu-id="dd719-110">The format identifier (FMTID) for the **DocumentSummaryInformation** property set is **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="dd719-111">La dichiarazione per questo valore è disponibile nei file di intestazione specificati come **fmtid \_ DocSummaryInformation**.</span><span class="sxs-lookup"><span data-stu-id="dd719-111">The declaration for this value is available in the provided header files as **FMTID\_DocSummaryInformation**.</span></span> <span data-ttu-id="dd719-112">Per ulteriori informazioni, vedere [nomi in IStorage](names-in-istorage.md), [il set di proprietà informazioni di riepilogo](the-summary-information-property-set.md), [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [identificatori di formato](format-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="dd719-112">For more information, see [Names in IStorage](names-in-istorage.md), [The Summary Information Property Set](the-summary-information-property-set.md), [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [Format Identifiers](format-identifiers.md).</span></span>

<span data-ttu-id="dd719-113">Questo flusso include anche una sezione separata per le proprietà personalizzate definite dall'utente, come nei set di proprietà **DocumentSummaryInformation** e **UserDefined** .</span><span class="sxs-lookup"><span data-stu-id="dd719-113">This stream also has a separate section for the custom-user-defined properties as in the **DocumentSummaryInformation** and **UserDefined** property sets.</span></span> <span data-ttu-id="dd719-114">Questa sezione viene visualizzata nell'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) come set di proprietà separato, con il fmtid seguente (disponibile come **fmtid \_ UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span><span class="sxs-lookup"><span data-stu-id="dd719-114">This section appears in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface as a separate property set, with the following FMTID (available as **FMTID\_UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="dd719-115">Questi due set di proprietà sono gli unici per i quali un singolo flusso può ospitare più set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd719-115">These two property sets are the only ones for which a single stream can hold multiple property sets.</span></span> <span data-ttu-id="dd719-116">Il fatto che questi due set di proprietà si trovino in un singolo flusso influiscono sul comportamento dell'interfaccia **IPropertySetStorage** .</span><span class="sxs-lookup"><span data-stu-id="dd719-116">The fact that these two property sets are in a single stream affects the behavior of the **IPropertySetStorage** interface.</span></span> <span data-ttu-id="dd719-117">Per ulteriori informazioni, vedere [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span><span class="sxs-lookup"><span data-stu-id="dd719-117">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span></span>

<span data-ttu-id="dd719-118">Nella tabella seguente sono elencate le proprietà aggiunte al set di proprietà **DocumentSummaryInformation** e **UserDefined** .</span><span class="sxs-lookup"><span data-stu-id="dd719-118">The following table lists the added properties to the **DocumentSummaryInformation** and **UserDefined** property set.</span></span> <span data-ttu-id="dd719-119">Come nel set di proprietà **SummaryInformation** , i nomi non vengono in genere archiviati nel set di proprietà, ma vengono dedotti dall'identificatore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd719-119">As in the **SummaryInformation** property set, the names are not typically stored in the property set, but are inferred from the property identifier.</span></span>



| <span data-ttu-id="dd719-120">Nome proprietà</span><span class="sxs-lookup"><span data-stu-id="dd719-120">Property name</span></span>      | <span data-ttu-id="dd719-121">Identificatore proprietà</span><span class="sxs-lookup"><span data-stu-id="dd719-121">Property identifier</span></span>     | <span data-ttu-id="dd719-122">Valore dell'identificatore di proprietà</span><span class="sxs-lookup"><span data-stu-id="dd719-122">Property identifier value</span></span> | <span data-ttu-id="dd719-123">Tipo VARIANT</span><span class="sxs-lookup"><span data-stu-id="dd719-123">VARIANT type</span></span>                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| <span data-ttu-id="dd719-124">Category</span><span class="sxs-lookup"><span data-stu-id="dd719-124">Category</span></span>           | <span data-ttu-id="dd719-125">**\_categoria PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-125">**PIDDSI\_CATEGORY**</span></span>    | <span data-ttu-id="dd719-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="dd719-126">0x00000002</span></span>                | <span data-ttu-id="dd719-127">**\_LPSTR VT**</span><span class="sxs-lookup"><span data-stu-id="dd719-127">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="dd719-128">DestinazionePresentazione</span><span class="sxs-lookup"><span data-stu-id="dd719-128">PresentationTarget</span></span> | <span data-ttu-id="dd719-129">**\_PRESFORMAT PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-129">**PIDDSI\_PRESFORMAT**</span></span>  | <span data-ttu-id="dd719-130">0x00000003</span><span class="sxs-lookup"><span data-stu-id="dd719-130">0x00000003</span></span>                | <span data-ttu-id="dd719-131">**\_LPSTR VT**</span><span class="sxs-lookup"><span data-stu-id="dd719-131">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="dd719-132">Byte</span><span class="sxs-lookup"><span data-stu-id="dd719-132">Bytes</span></span>              | <span data-ttu-id="dd719-133">**PIDDSI ( \_ GetByteCount)**</span><span class="sxs-lookup"><span data-stu-id="dd719-133">**PIDDSI\_BYTECOUNT**</span></span>   | <span data-ttu-id="dd719-134">0x00000004</span><span class="sxs-lookup"><span data-stu-id="dd719-134">0x00000004</span></span>                | <span data-ttu-id="dd719-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="dd719-135">**VT\_I4**</span></span>                        |
| <span data-ttu-id="dd719-136">Linee</span><span class="sxs-lookup"><span data-stu-id="dd719-136">Lines</span></span>              | <span data-ttu-id="dd719-137">**\_LINECOUNT PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-137">**PIDDSI\_LINECOUNT**</span></span>   | <span data-ttu-id="dd719-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="dd719-138">0x00000005</span></span>                | <span data-ttu-id="dd719-139">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="dd719-139">**VT\_I4**</span></span>                        |
| <span data-ttu-id="dd719-140">Paragrafi</span><span class="sxs-lookup"><span data-stu-id="dd719-140">Paragraphs</span></span>         | <span data-ttu-id="dd719-141">**\_PARCOUNT PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-141">**PIDDSI\_PARCOUNT**</span></span>    | <span data-ttu-id="dd719-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="dd719-142">0x00000006</span></span>                | <span data-ttu-id="dd719-143">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="dd719-143">**VT\_I4**</span></span>                        |
| <span data-ttu-id="dd719-144">Diapositive</span><span class="sxs-lookup"><span data-stu-id="dd719-144">Slides</span></span>             | <span data-ttu-id="dd719-145">**\_SLIDECOUNT PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-145">**PIDDSI\_SLIDECOUNT**</span></span>  | <span data-ttu-id="dd719-146">0x00000007</span><span class="sxs-lookup"><span data-stu-id="dd719-146">0x00000007</span></span>                | <span data-ttu-id="dd719-147">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="dd719-147">**VT\_I4**</span></span>                        |
| <span data-ttu-id="dd719-148">Note</span><span class="sxs-lookup"><span data-stu-id="dd719-148">Notes</span></span>              | <span data-ttu-id="dd719-149">**\_NOTECOUNT PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-149">**PIDDSI\_NOTECOUNT**</span></span>   | <span data-ttu-id="dd719-150">0x00000008</span><span class="sxs-lookup"><span data-stu-id="dd719-150">0x00000008</span></span>                | <span data-ttu-id="dd719-151">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="dd719-151">**VT\_I4**</span></span>                        |
| <span data-ttu-id="dd719-152">HiddenSlides</span><span class="sxs-lookup"><span data-stu-id="dd719-152">HiddenSlides</span></span>       | <span data-ttu-id="dd719-153">**\_HIDDENCOUNT PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-153">**PIDDSI\_HIDDENCOUNT**</span></span> | <span data-ttu-id="dd719-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="dd719-154">0x00000009</span></span>                | <span data-ttu-id="dd719-155">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="dd719-155">**VT\_I4**</span></span>                        |
| <span data-ttu-id="dd719-156">MMClips</span><span class="sxs-lookup"><span data-stu-id="dd719-156">MMClips</span></span>            | <span data-ttu-id="dd719-157">**\_MMCLIPCOUNT PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-157">**PIDDSI\_MMCLIPCOUNT**</span></span> | <span data-ttu-id="dd719-158">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="dd719-158">0x0000000A</span></span>                | <span data-ttu-id="dd719-159">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="dd719-159">**VT\_I4**</span></span>                        |
| <span data-ttu-id="dd719-160">ScaleCrop</span><span class="sxs-lookup"><span data-stu-id="dd719-160">ScaleCrop</span></span>          | <span data-ttu-id="dd719-161">**\_scalabilità PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-161">**PIDDSI\_SCALE**</span></span>       | <span data-ttu-id="dd719-162">0x0000000B</span><span class="sxs-lookup"><span data-stu-id="dd719-162">0x0000000B</span></span>                | <span data-ttu-id="dd719-163">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="dd719-163">**VT\_BOOL**</span></span>                      |
| <span data-ttu-id="dd719-164">HeadingPairs</span><span class="sxs-lookup"><span data-stu-id="dd719-164">HeadingPairs</span></span>       | <span data-ttu-id="dd719-165">**\_HEADINGPAIR PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-165">**PIDDSI\_HEADINGPAIR**</span></span> | <span data-ttu-id="dd719-166">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="dd719-166">0x0000000C</span></span>                | <span data-ttu-id="dd719-167">**VT \_** \| **\_ vettore VT** Variant</span><span class="sxs-lookup"><span data-stu-id="dd719-167">**VT\_VARIANT** \| **VT\_VECTOR**</span></span> |
| <span data-ttu-id="dd719-168">TitlesofParts</span><span class="sxs-lookup"><span data-stu-id="dd719-168">TitlesofParts</span></span>      | <span data-ttu-id="dd719-169">**\_DOCPARTS PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-169">**PIDDSI\_DOCPARTS**</span></span>    | <span data-ttu-id="dd719-170">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="dd719-170">0x0000000D</span></span>                | <span data-ttu-id="dd719-171">**VT \_** \| **\_ LPSTR Vector VT**</span><span class="sxs-lookup"><span data-stu-id="dd719-171">**VT\_VECTOR** \| **VT\_LPSTR**</span></span>   |
| <span data-ttu-id="dd719-172">Manager</span><span class="sxs-lookup"><span data-stu-id="dd719-172">Manager</span></span>            | <span data-ttu-id="dd719-173">**\_gestione PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-173">**PIDDSI\_MANAGER**</span></span>     | <span data-ttu-id="dd719-174">0x0000000E</span><span class="sxs-lookup"><span data-stu-id="dd719-174">0x0000000E</span></span>                | <span data-ttu-id="dd719-175">**\_LPSTR VT**</span><span class="sxs-lookup"><span data-stu-id="dd719-175">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="dd719-176">Company</span><span class="sxs-lookup"><span data-stu-id="dd719-176">Company</span></span>            | <span data-ttu-id="dd719-177">**\_società PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-177">**PIDDSI\_COMPANY**</span></span>     | <span data-ttu-id="dd719-178">0x0000000F</span><span class="sxs-lookup"><span data-stu-id="dd719-178">0x0000000F</span></span>                | <span data-ttu-id="dd719-179">**\_LPSTR VT**</span><span class="sxs-lookup"><span data-stu-id="dd719-179">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="dd719-180">LinksUpToDate</span><span class="sxs-lookup"><span data-stu-id="dd719-180">LinksUpToDate</span></span>      | <span data-ttu-id="dd719-181">**\_LINKSDIRTY PIDDSI**</span><span class="sxs-lookup"><span data-stu-id="dd719-181">**PIDDSI\_LINKSDIRTY**</span></span>  | <span data-ttu-id="dd719-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dd719-182">0x00000010</span></span>                | <span data-ttu-id="dd719-183">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="dd719-183">**VT\_BOOL**</span></span>                      |



 

<span data-ttu-id="dd719-184">Queste proprietà hanno i seguenti usi:</span><span class="sxs-lookup"><span data-stu-id="dd719-184">These properties have the following uses:</span></span>

<dl> <dt>

<span data-ttu-id="dd719-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria</span><span class="sxs-lookup"><span data-stu-id="dd719-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="dd719-186">Stringa di testo digitata dall'utente che indica a quale categoria appartiene il file (promemoria, proposta e così via).</span><span class="sxs-lookup"><span data-stu-id="dd719-186">A text string typed by the user that indicates what category the file belongs to (memo, proposal, and so on).</span></span> <span data-ttu-id="dd719-187">È utile per trovare file dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="dd719-187">It is useful for finding files of same type.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>DestinazionePresentazione</span><span class="sxs-lookup"><span data-stu-id="dd719-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget</span></span>
</dt> <dd>

<span data-ttu-id="dd719-189">Formato di destinazione per la presentazione (35mm, stampante, video e così via).</span><span class="sxs-lookup"><span data-stu-id="dd719-189">Target format for presentation (35mm, printer, video, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="dd719-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Byte</span><span class="sxs-lookup"><span data-stu-id="dd719-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes</span></span>
</dt> <dd>

<span data-ttu-id="dd719-191">Numero di byte.</span><span class="sxs-lookup"><span data-stu-id="dd719-191">Number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Linee</span><span class="sxs-lookup"><span data-stu-id="dd719-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Lines</span></span>
</dt> <dd>

<span data-ttu-id="dd719-193">Numero di righe.</span><span class="sxs-lookup"><span data-stu-id="dd719-193">Number of lines.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Paragrafi</span><span class="sxs-lookup"><span data-stu-id="dd719-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Paragraphs</span></span>
</dt> <dd>

<span data-ttu-id="dd719-195">Numero di paragrafi.</span><span class="sxs-lookup"><span data-stu-id="dd719-195">Number of paragraphs.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Diapositive</span><span class="sxs-lookup"><span data-stu-id="dd719-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Slides</span></span>
</dt> <dd>

<span data-ttu-id="dd719-197">Numero di diapositive.</span><span class="sxs-lookup"><span data-stu-id="dd719-197">Number of slides.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Note</span><span class="sxs-lookup"><span data-stu-id="dd719-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Notes</span></span>
</dt> <dd>

<span data-ttu-id="dd719-199">Numero di pagine che contengono note.</span><span class="sxs-lookup"><span data-stu-id="dd719-199">Number of pages that contain notes.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides</span><span class="sxs-lookup"><span data-stu-id="dd719-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides</span></span>
</dt> <dd>

<span data-ttu-id="dd719-201">Numero di diapositive nascoste.</span><span class="sxs-lookup"><span data-stu-id="dd719-201">Number of slides that are hidden.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips</span><span class="sxs-lookup"><span data-stu-id="dd719-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips</span></span>
</dt> <dd>

<span data-ttu-id="dd719-203">Numero di clip audio o video.</span><span class="sxs-lookup"><span data-stu-id="dd719-203">Number of sound or video clips.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop</span><span class="sxs-lookup"><span data-stu-id="dd719-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop</span></span>
</dt> <dd>

<span data-ttu-id="dd719-205">Impostare su true (-1) quando si vuole ridimensionare l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="dd719-205">Set to True (-1) when scaling of the thumbnail is desired.</span></span> <span data-ttu-id="dd719-206">Se non è impostato, si desidera il ritaglio.</span><span class="sxs-lookup"><span data-stu-id="dd719-206">If not set, cropping is desired.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs</span><span class="sxs-lookup"><span data-stu-id="dd719-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs</span></span>
</dt> <dd>

<span data-ttu-id="dd719-208">Proprietà utilizzata internamente che indica il raggruppamento di diverse parti del documento e il numero di elementi in ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="dd719-208">Internally used property indicating the grouping of different document parts and the number of items in each group.</span></span> <span data-ttu-id="dd719-209">I titoli delle parti del documento vengono archiviati nella proprietà **TitlesofParts** .</span><span class="sxs-lookup"><span data-stu-id="dd719-209">The titles of the document parts are stored in the **TitlesofParts** property.</span></span> <span data-ttu-id="dd719-210">La proprietà **HeadingPairs** viene archiviata come vettore di varianti, in coppie ripetute di valori VT **\_ LPSTR** (o **VT \_ LPWSTR**) e **VT \_ I4** .</span><span class="sxs-lookup"><span data-stu-id="dd719-210">The **HeadingPairs** property is stored as a vector of variants, in repeating pairs of **VT\_LPSTR** (or **VT\_LPWSTR**) and **VT\_I4** values.</span></span> <span data-ttu-id="dd719-211">Il valore **VT \_ LPSTR** rappresenta un nome di intestazione e il valore **VT \_ I4** indica il numero di parti del documento sotto tale intestazione.</span><span class="sxs-lookup"><span data-stu-id="dd719-211">The **VT\_LPSTR** value represents a heading name, and the **VT\_I4** value indicates the count of document parts under that heading.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts</span><span class="sxs-lookup"><span data-stu-id="dd719-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts</span></span>
</dt> <dd>

<span data-ttu-id="dd719-213">Nomi delle parti del documento.</span><span class="sxs-lookup"><span data-stu-id="dd719-213">Names of document parts.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager</span><span class="sxs-lookup"><span data-stu-id="dd719-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager</span></span>
</dt> <dd>

<span data-ttu-id="dd719-215">Responsabile del progetto.</span><span class="sxs-lookup"><span data-stu-id="dd719-215">Manager of the project.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Azienda</span><span class="sxs-lookup"><span data-stu-id="dd719-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="dd719-217">Nome della società.</span><span class="sxs-lookup"><span data-stu-id="dd719-217">Company name.</span></span>

</dd> <dt>

<span data-ttu-id="dd719-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate</span><span class="sxs-lookup"><span data-stu-id="dd719-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate</span></span>
</dt> <dd>

<span data-ttu-id="dd719-219">Valore booleano che indica se i collegamenti personalizzati sono ostacolati da un rumore eccessivo, per tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="dd719-219">Boolean value to indicate whether the custom links are hampered by excessive noise, for all applications.</span></span>

> [!Note]  
> <span data-ttu-id="dd719-220">Come descritto in 12,3.</span><span class="sxs-lookup"><span data-stu-id="dd719-220">As described in 12.3.</span></span> <span data-ttu-id="dd719-221">Formato serializzato per i set di proprietà della specifica di progettazione OLE 2,0, gli elementi Vector nelle proprietà **HeadingPairs** e **TitlesofParts** devono essere allineati nei limiti di 32 bit all'interno del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd719-221">Serialized Format for Property Sets of the OLE 2.0 Design Specification, vector elements in the **HeadingPairs** and **TitlesofParts** properties should be aligned on 32 bit boundaries within the property set.</span></span> <span data-ttu-id="dd719-222">Tuttavia, nei set di proprietà **DocumentSummaryInformation** e **UserDefined** , quando la tabella codici della proprietà impostata non è Unicode, questi elementi devono essere compressi.</span><span class="sxs-lookup"><span data-stu-id="dd719-222">However, in the **DocumentSummaryInformation** and **UserDefined** property sets, when the code page of the property set is not Unicode, these elements must be packed.</span></span>

 

</dd> </dl>

<span data-ttu-id="dd719-223">Il set di proprietà **UserDefined** può essere utilizzato per contenere qualsiasi proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd719-223">The **UserDefined** property set can be used to hold any properties.</span></span> <span data-ttu-id="dd719-224">Viene in genere usato per archiviare le proprietà denominate create da un utente.</span><span class="sxs-lookup"><span data-stu-id="dd719-224">Typically, it is used to store named properties created by a user.</span></span>

 

 




