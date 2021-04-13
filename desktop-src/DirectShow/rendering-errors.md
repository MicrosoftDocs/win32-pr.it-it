---
description: Errori di rendering
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Errori di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482236"
---
# <a name="rendering-errors"></a><span data-ttu-id="0a4c7-103">Errori di rendering</span><span class="sxs-lookup"><span data-stu-id="0a4c7-103">Rendering Errors</span></span>

> [!Note]  
> <span data-ttu-id="0a4c7-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-104">\[Deprecated.</span></span> <span data-ttu-id="0a4c7-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a4c7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0a4c7-106">Microsoft® DirectShow® editing Services (DES) definisce diversi codici di errore utilizzati per registrare gli errori di rendering.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-106">Microsoft® DirectShow® Editing Services (DES) defines various error codes used to log rendering errors.</span></span> <span data-ttu-id="0a4c7-107">Se il rendering di un progetto non viene eseguito correttamente, il motore di rendering chiama il metodo [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) .</span><span class="sxs-lookup"><span data-stu-id="0a4c7-107">If a project does not render correctly, the render engine calls the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="0a4c7-108">Nella tabella seguente sono riepilogati i parametri assegnati a **LogError**:</span><span class="sxs-lookup"><span data-stu-id="0a4c7-108">The following table summarizes the parameters given to **LogError**:</span></span>

-   <span data-ttu-id="0a4c7-109">Il codice di errore è contenuto nel parametro *ErrorCode* .</span><span class="sxs-lookup"><span data-stu-id="0a4c7-109">The error code is contained in the *ErrorCode* parameter.</span></span>
-   <span data-ttu-id="0a4c7-110">La descrizione è contenuta nel parametro ErrorString.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-110">The description is contained in the ErrorString parameter.</span></span>
-   <span data-ttu-id="0a4c7-111">La descrizione è contenuta nel parametro *ErrorString* .</span><span class="sxs-lookup"><span data-stu-id="0a4c7-111">The description is contained in the *ErrorString* parameter.</span></span>
-   <span data-ttu-id="0a4c7-112">Se sono presenti informazioni aggiuntive, il tipo **Variant** è contenuto nel membro **VT** della **variante** a cui punta *pExtraInfo*.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-112">If there is extra information, the **VARIANT** type is contained in the **vt** member of the **VARIANT** pointed to by *pExtraInfo*.</span></span>

> [!Note]  
> <span data-ttu-id="0a4c7-113">I codici di errore descritti qui non sono valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a4c7-113">The error codes described here are not **HRESULT** values.</span></span> <span data-ttu-id="0a4c7-114">Per un elenco di valori restituiti **HRESULT** specifici per des, vedere [codici di errore e di esito positivo](error-and-success-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0a4c7-114">For a list of **HRESULT** return values specific to DES, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a4c7-115">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="0a4c7-115">Error code</span></span></th>
<th><span data-ttu-id="0a4c7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a4c7-116">Description</span></span></th>
<th><span data-ttu-id="0a4c7-117">Informazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="0a4c7-117">Extra information</span></span></th>
<th><span data-ttu-id="0a4c7-118">Tipo variant</span><span class="sxs-lookup"><span data-stu-id="0a4c7-118">Variant type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a4c7-119">DEX_IDS_BAD_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="0a4c7-119">DEX_IDS_BAD_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="0a4c7-120">Il nome file non esiste oppure DirectShow non riconosce l'estensione di file.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-120">File name doesn't exist, or DirectShow doesn't recognize the file extension.</span></span></td>
<td><span data-ttu-id="0a4c7-121">Nome file</span><span class="sxs-lookup"><span data-stu-id="0a4c7-121">File name</span></span></td>
<td><span data-ttu-id="0a4c7-122"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-122"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a4c7-123">DEX_IDS_BAD_SOURCE_NAME2</span><span class="sxs-lookup"><span data-stu-id="0a4c7-123">DEX_IDS_BAD_SOURCE_NAME2</span></span></td>
<td><span data-ttu-id="0a4c7-124">Il tipo di file non corrisponde all'estensione di file oppure il file è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-124">File type does not match the file extension or the file is corrupt.</span></span></td>
<td><span data-ttu-id="0a4c7-125">Nome file</span><span class="sxs-lookup"><span data-stu-id="0a4c7-125">File name</span></span></td>
<td><span data-ttu-id="0a4c7-126"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-126"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a4c7-127">DEX_IDS_MISSING_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="0a4c7-127">DEX_IDS_MISSING_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="0a4c7-128">Il nome file è obbligatorio, ma non è stato specificato.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-128">File name was required, but wasn't given.</span></span></td>
<td><span data-ttu-id="0a4c7-129">nessuno</span><span class="sxs-lookup"><span data-stu-id="0a4c7-129">None</span></span></td>
<td><span data-ttu-id="0a4c7-130">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0a4c7-130">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a4c7-131">DEX_IDS_UNKNOWN_SOURCE</span><span class="sxs-lookup"><span data-stu-id="0a4c7-131">DEX_IDS_UNKNOWN_SOURCE</span></span></td>
<td><span data-ttu-id="0a4c7-132">Impossibile analizzare l'origine dati fornita da questa origine.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-132">Cannot parse data source provided by this source.</span></span></td>
<td><span data-ttu-id="0a4c7-133">nessuno</span><span class="sxs-lookup"><span data-stu-id="0a4c7-133">None</span></span></td>
<td><span data-ttu-id="0a4c7-134">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0a4c7-134">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a4c7-135">DEX_IDS_INSTALL_PROBLEM</span><span class="sxs-lookup"><span data-stu-id="0a4c7-135">DEX_IDS_INSTALL_PROBLEM</span></span></td>
<td><span data-ttu-id="0a4c7-136">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-136">Unexpected error.</span></span> <span data-ttu-id="0a4c7-137">Componente DirectShow non installato correttamente.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-137">Some DirectShow component is not installed properly.</span></span></td>
<td><span data-ttu-id="0a4c7-138">nessuno</span><span class="sxs-lookup"><span data-stu-id="0a4c7-138">None</span></span></td>
<td><span data-ttu-id="0a4c7-139">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0a4c7-139">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a4c7-140">DEX_IDS_NO_SOURCE_NAMES</span><span class="sxs-lookup"><span data-stu-id="0a4c7-140">DEX_IDS_NO_SOURCE_NAMES</span></span></td>
<td><span data-ttu-id="0a4c7-141">Il filtro di origine non accetta nomi di file.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-141">Source filter does not accept file names.</span></span></td>
<td><span data-ttu-id="0a4c7-142">nessuno</span><span class="sxs-lookup"><span data-stu-id="0a4c7-142">None</span></span></td>
<td><span data-ttu-id="0a4c7-143">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0a4c7-143">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a4c7-144">DEX_IDS_BAD_MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="0a4c7-144">DEX_IDS_BAD_MEDIATYPE</span></span></td>
<td><span data-ttu-id="0a4c7-145">Il tipo di supporto del gruppo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-145">Group's media type is not supported.</span></span></td>
<td><span data-ttu-id="0a4c7-146">Numero gruppo</span><span class="sxs-lookup"><span data-stu-id="0a4c7-146">Group number</span></span></td>
<td><span data-ttu-id="0a4c7-147"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-147"><strong>int</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a4c7-148">DEX_IDS_STREAM_NUMBER</span><span class="sxs-lookup"><span data-stu-id="0a4c7-148">DEX_IDS_STREAM_NUMBER</span></span></td>
<td><span data-ttu-id="0a4c7-149">Il numero di flusso per questa origine non è valido.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-149">Invalid stream number for this source.</span></span></td>
<td><span data-ttu-id="0a4c7-150">Numero di flusso</span><span class="sxs-lookup"><span data-stu-id="0a4c7-150">Stream number</span></span></td>
<td><span data-ttu-id="0a4c7-151"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-151"><strong>int</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a4c7-152">DEX_IDS_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="0a4c7-152">DEX_IDS_OUTOFMEMORY</span></span></td>
<td><span data-ttu-id="0a4c7-153">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-153">Out of memory.</span></span></td>
<td><span data-ttu-id="0a4c7-154">nessuno</span><span class="sxs-lookup"><span data-stu-id="0a4c7-154">None</span></span></td>
<td><span data-ttu-id="0a4c7-155">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0a4c7-155">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a4c7-156">DEX_IDS_DIBSEQ_NOTALLSAME</span><span class="sxs-lookup"><span data-stu-id="0a4c7-156">DEX_IDS_DIBSEQ_NOTALLSAME</span></span></td>
<td><span data-ttu-id="0a4c7-157">Una bitmap nella sequenza non è dello stesso tipo degli altri.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-157">One bitmap in the sequence was not the same type as the others.</span></span></td>
<td><span data-ttu-id="0a4c7-158">Nome bitmap</span><span class="sxs-lookup"><span data-stu-id="0a4c7-158">Bitmap name</span></span></td>
<td><span data-ttu-id="0a4c7-159"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-159"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a4c7-160">DEX_IDS_CLIPTOOSHORT</span><span class="sxs-lookup"><span data-stu-id="0a4c7-160">DEX_IDS_CLIPTOOSHORT</span></span></td>
<td><span data-ttu-id="0a4c7-161">I tempi di supporto della clip non sono validi o la sequenza di bitmap (DIB) indipendente dal dispositivo è troppo corta.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-161">Clip's media times are invalid, or the device-independent bitmap (DIB) sequence is too short.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0a4c7-162">Se si verificano altri errori di rendering, questo errore può verificarsi anche se i tempi dei supporti sono validi.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-162">If other rendering errors occur, this error might occur even though the media times are valid.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="0a4c7-163">nessuno</span><span class="sxs-lookup"><span data-stu-id="0a4c7-163">None</span></span></td>
<td><span data-ttu-id="0a4c7-164">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0a4c7-164">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a4c7-165">DEX_IDS_INVALID_DXT</span><span class="sxs-lookup"><span data-stu-id="0a4c7-165">DEX_IDS_INVALID_DXT</span></span></td>
<td><span data-ttu-id="0a4c7-166">Identificatore di classe (CLSID) dell'effetto o della transizione non valido.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-166">Class identifier (CLSID) of the effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="0a4c7-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="0a4c7-167">CLSID</span></span></td>
<td><span data-ttu-id="0a4c7-168"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-168"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a4c7-169">DEX_IDS_INVALID_DEFAULT_DXT</span><span class="sxs-lookup"><span data-stu-id="0a4c7-169">DEX_IDS_INVALID_DEFAULT_DXT</span></span></td>
<td><span data-ttu-id="0a4c7-170">Il CLSID dell'effetto o della transizione predefinita non è valido.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-170">The CLSID of the default effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="0a4c7-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="0a4c7-171">CLSID</span></span></td>
<td><span data-ttu-id="0a4c7-172"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-172"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a4c7-173">DEX_IDS_NO_3D</span><span class="sxs-lookup"><span data-stu-id="0a4c7-173">DEX_IDS_NO_3D</span></span></td>
<td><span data-ttu-id="0a4c7-174">La versione di DirectX non supporta le transizioni tridimensionali.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-174">Your version of DirectX does not support three-dimensional transitions.</span></span></td>
<td><span data-ttu-id="0a4c7-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="0a4c7-175">CLSID</span></span></td>
<td><span data-ttu-id="0a4c7-176"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-176"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a4c7-177">DEX_IDS_BROKEN_DXT</span><span class="sxs-lookup"><span data-stu-id="0a4c7-177">DEX_IDS_BROKEN_DXT</span></span></td>
<td><span data-ttu-id="0a4c7-178">Questo effetto non è il tipo corretto o è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-178">This effect is not the right kind, or is broken.</span></span></td>
<td><span data-ttu-id="0a4c7-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="0a4c7-179">CLSID</span></span></td>
<td><span data-ttu-id="0a4c7-180"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-180"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a4c7-181">DEX_IDS_NO_SUCH_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="0a4c7-181">DEX_IDS_NO_SUCH_PROPERTY</span></span></td>
<td><span data-ttu-id="0a4c7-182">Questa proprietà non esiste nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-182">No such property exists on the object.</span></span></td>
<td><span data-ttu-id="0a4c7-183">Nome proprietà</span><span class="sxs-lookup"><span data-stu-id="0a4c7-183">Property name</span></span></td>
<td><span data-ttu-id="0a4c7-184"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-184"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a4c7-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span><span class="sxs-lookup"><span data-stu-id="0a4c7-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span></span></td>
<td><span data-ttu-id="0a4c7-186">Valore non valido per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-186">Illegal value for this property.</span></span></td>
<td><span data-ttu-id="0a4c7-187">Valore specificato</span><span class="sxs-lookup"><span data-stu-id="0a4c7-187">Value specified</span></span></td>
<td><span data-ttu-id="0a4c7-188"><strong>VARIANTE</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-188"><strong>VARIANT</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a4c7-189">DEX_IDS_INVALID_XML</span><span class="sxs-lookup"><span data-stu-id="0a4c7-189">DEX_IDS_INVALID_XML</span></span></td>
<td><span data-ttu-id="0a4c7-190">Errore di sintassi nel file XML.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-190">Syntax error in XML file.</span></span></td>
<td><span data-ttu-id="0a4c7-191">Numero di riga</span><span class="sxs-lookup"><span data-stu-id="0a4c7-191">Line number</span></span></td>
<td><span data-ttu-id="0a4c7-192">VT_I4 (Integer a 4 byte)</span><span class="sxs-lookup"><span data-stu-id="0a4c7-192">VT_I4 (4-byte integer)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a4c7-193">DEX_IDS_CANT_FIND_FILTER</span><span class="sxs-lookup"><span data-stu-id="0a4c7-193">DEX_IDS_CANT_FIND_FILTER</span></span></td>
<td><span data-ttu-id="0a4c7-194">Impossibile trovare il filtro specificato in XML per categoria e istanza.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-194">Cannot find filter specified in XML by category and instance.</span></span></td>
<td><span data-ttu-id="0a4c7-195">Nome descrittivo (istanza)</span><span class="sxs-lookup"><span data-stu-id="0a4c7-195">Friendly name (instance)</span></span></td>
<td><span data-ttu-id="0a4c7-196"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-196"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a4c7-197">DEX_IDS_DISK_WRITE_ERROR</span><span class="sxs-lookup"><span data-stu-id="0a4c7-197">DEX_IDS_DISK_WRITE_ERROR</span></span></td>
<td><span data-ttu-id="0a4c7-198">Errore durante la scrittura del file XML su disco.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-198">Error writing XML file to disk.</span></span></td>
<td><span data-ttu-id="0a4c7-199">nessuno</span><span class="sxs-lookup"><span data-stu-id="0a4c7-199">None</span></span></td>
<td><span data-ttu-id="0a4c7-200">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0a4c7-200">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a4c7-201">DEX_IDS_INVALID_AUDIO_FX</span><span class="sxs-lookup"><span data-stu-id="0a4c7-201">DEX_IDS_INVALID_AUDIO_FX</span></span></td>
<td><span data-ttu-id="0a4c7-202">CLSID non è un filtro effetto audio DirectShow valido.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-202">CLSID not a valid DirectShow audio effect filter.</span></span></td>
<td><span data-ttu-id="0a4c7-203">CLSID</span><span class="sxs-lookup"><span data-stu-id="0a4c7-203">CLSID</span></span></td>
<td><span data-ttu-id="0a4c7-204"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="0a4c7-204"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a4c7-205">DEX_IDS_CANT_FIND_COMPRESSOR</span><span class="sxs-lookup"><span data-stu-id="0a4c7-205">DEX_IDS_CANT_FIND_COMPRESSOR</span></span></td>
<td><span data-ttu-id="0a4c7-206">Non è possibile trovare un compressore per produrre il formato di compressione specificato.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-206">Cannot find a compressor to produce the specified compression format.</span></span></td>
<td><span data-ttu-id="0a4c7-207">nessuno</span><span class="sxs-lookup"><span data-stu-id="0a4c7-207">None</span></span></td>
<td><span data-ttu-id="0a4c7-208">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0a4c7-208">Not applicable</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0a4c7-209">Gli errori seguenti non dovrebbero mai verificarsi.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-209">The following errors should never occur.</span></span> <span data-ttu-id="0a4c7-210">Se si verifica uno di questi errori, inviare un report sui bug a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-210">If you encounter one of these errors, please send a bug report to Microsoft.</span></span>



| <span data-ttu-id="0a4c7-211">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="0a4c7-211">Error code</span></span>                 | <span data-ttu-id="0a4c7-212">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a4c7-212">Description</span></span>                                 |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="0a4c7-213">\_ \_ Analisi sequenza temporale ID Dex \_</span><span class="sxs-lookup"><span data-stu-id="0a4c7-213">DEX\_IDS\_TIMELINE\_PARSE</span></span>  | <span data-ttu-id="0a4c7-214">Errore imprevisto durante l'analisi della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-214">Unexpected error parsing the timeline.</span></span>      |
| <span data-ttu-id="0a4c7-215">\_ \_ errore grafico ID \_ Dex</span><span class="sxs-lookup"><span data-stu-id="0a4c7-215">DEX\_IDS\_GRAPH\_ERROR</span></span>     | <span data-ttu-id="0a4c7-216">Errore imprevisto durante la creazione del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-216">Unexpected error building the filter graph.</span></span> |
| <span data-ttu-id="0a4c7-217">\_errore di \_ griglia \_ ID Dex</span><span class="sxs-lookup"><span data-stu-id="0a4c7-217">DEX\_IDS\_GRID\_ERROR</span></span>      | <span data-ttu-id="0a4c7-218">Errore imprevisto della griglia interna.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-218">Unexpected error with the internal grid.</span></span>    |
| <span data-ttu-id="0a4c7-219">\_errore dell' \_ interfaccia \_ ID Dex</span><span class="sxs-lookup"><span data-stu-id="0a4c7-219">DEX\_IDS\_INTERFACE\_ERROR</span></span> | <span data-ttu-id="0a4c7-220">Errore imprevisto durante il recupero di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0a4c7-220">Unexpected error getting an interface.</span></span>      |



 

 

 




