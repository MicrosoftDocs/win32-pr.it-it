---
description: Filtro Mux AVI
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Filtro Mux AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3755a4d5f63e824ae08eb736a5999dcac3d7ab32
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876965"
---
# <a name="avi-mux-filter"></a><span data-ttu-id="310eb-103">Filtro Mux AVI</span><span class="sxs-lookup"><span data-stu-id="310eb-103">AVI Mux Filter</span></span>

<span data-ttu-id="310eb-104">Il filtro Mux AVI accetta più flussi di input e li invia in formato AVI.</span><span class="sxs-lookup"><span data-stu-id="310eb-104">The AVI Mux filter accepts multiple input streams and interleaves them into AVI format.</span></span> <span data-ttu-id="310eb-105">Il filtro usa i pin di input separati per ogni flusso di input e un pin di output per il flusso AVI.</span><span class="sxs-lookup"><span data-stu-id="310eb-105">The filter uses separate input pins for each input stream, and one output pin for the AVI stream.</span></span>

<span data-ttu-id="310eb-106">Le applicazioni di creazione/acquisizione video possono usare questo filtro per salvare i file su disco in formato AVI.</span><span class="sxs-lookup"><span data-stu-id="310eb-106">Video capture or authoring applications can use this filter to save files to disk in AVI format.</span></span> <span data-ttu-id="310eb-107">Il filtro è in genere connesso al filtro del [writer di file](file-writer-filter.md) , ma può connettersi a qualsiasi filtro il cui pin di input supporta le interfacce IStream e [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="310eb-107">The filter is typically connected to the [File Writer](file-writer-filter.md) filter, but it can connect to any filter whose input pin supports the IStream and [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="310eb-108">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="310eb-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="310eb-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="310eb-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="310eb-110">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="310eb-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="310eb-111">Qualsiasi tipo principale che corrisponde a un FOURCC di tipo obsoleto o MEDIATYPE_AUXLine21Data.</span><span class="sxs-lookup"><span data-stu-id="310eb-111">Any major type that corresponds to an old-style FOURCC, or MEDIATYPE_AUXLine21Data.</span></span> <span data-ttu-id="310eb-112">Per ulteriori informazioni, vedere la <a href="fourccmap.md"><strong>classe FOURCCMap</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="310eb-112">(For more information, see <a href="fourccmap.md"><strong>FOURCCMap Class</strong></a>.)</span></span>
<ul>
<li><span data-ttu-id="310eb-113">Se il tipo principale è MEDIATYPE_Audio, il formato deve essere FORMAT_WaveFormatEx.</span><span class="sxs-lookup"><span data-stu-id="310eb-113">If the major type is MEDIATYPE_Audio, the format must be FORMAT_WaveFormatEx.</span></span></li>
<li><span data-ttu-id="310eb-114">Se il tipo principale è MEDIATYPE_Video, il formato deve essere FORMAT_VideoInfo o FORMAT_DvInfo.</span><span class="sxs-lookup"><span data-stu-id="310eb-114">If the major type is MEDIATYPE_Video, the format must be FORMAT_VideoInfo or FORMAT_DvInfo.</span></span></li>
<li><span data-ttu-id="310eb-115">Se il tipo principale è MEDIATYPE_Interleaved, il formato deve essere FORMAT_DvInfo.</span><span class="sxs-lookup"><span data-stu-id="310eb-115">If the major type is MEDIATYPE_Interleaved, the format must be FORMAT_DvInfo.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="310eb-116">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="310eb-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="310eb-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="310eb-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="310eb-118">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="310eb-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="310eb-119">MEDIATYPE_Stream, MEDIASUBTYPE_Avi</span><span class="sxs-lookup"><span data-stu-id="310eb-119">MEDIATYPE_Stream, MEDIASUBTYPE_Avi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="310eb-120">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="310eb-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="310eb-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="310eb-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="310eb-122">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="310eb-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="310eb-123">CLSID_AviDest</span><span class="sxs-lookup"><span data-stu-id="310eb-123">CLSID_AviDest</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="310eb-124">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="310eb-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="310eb-125">CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</span><span class="sxs-lookup"><span data-stu-id="310eb-125">CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="310eb-126">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="310eb-126">Executable</span></span></td>
<td><span data-ttu-id="310eb-127">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="310eb-127">qcap.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="310eb-128"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="310eb-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="310eb-129">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="310eb-129">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="310eb-130"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="310eb-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="310eb-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="310eb-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a><span data-ttu-id="310eb-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="310eb-132">Remarks</span></span>

<span data-ttu-id="310eb-133">Le osservazioni seguenti descrivono i vari aspetti della funzionalità del filtro Mux di AVI.</span><span class="sxs-lookup"><span data-stu-id="310eb-133">The following remarks describe various aspects of the AVI Mux filter's functionality.</span></span>

<span data-ttu-id="310eb-134">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="310eb-134">Pins</span></span>

<span data-ttu-id="310eb-135">Quando viene creato il filtro Mux AVI, è presente un pin di input.</span><span class="sxs-lookup"><span data-stu-id="310eb-135">When the AVI Mux filter is created, it has one input pin.</span></span> <span data-ttu-id="310eb-136">Quando ogni pin di input è connesso, il filtro crea un nuovo PIN di input.</span><span class="sxs-lookup"><span data-stu-id="310eb-136">As each input pin is connected, the filter creates a new input pin.</span></span>

<span data-ttu-id="310eb-137">Proprietà del flusso</span><span class="sxs-lookup"><span data-stu-id="310eb-137">Stream Properties</span></span>

<span data-ttu-id="310eb-138">I pin di input supportano l'interfaccia IPropertyBag per l'impostazione delle proprietà nei singoli flussi.</span><span class="sxs-lookup"><span data-stu-id="310eb-138">The input pins support the IPropertyBag interface for setting properties on individual streams.</span></span> <span data-ttu-id="310eb-139">Attualmente, viene definita la proprietà seguente:</span><span class="sxs-lookup"><span data-stu-id="310eb-139">Currently, the following property is defined:</span></span>



| <span data-ttu-id="310eb-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="310eb-140">Property</span></span> | <span data-ttu-id="310eb-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="310eb-141">Description</span></span>                                                           |
|----------|-----------------------------------------------------------------------|
| <span data-ttu-id="310eb-142">name</span><span class="sxs-lookup"><span data-stu-id="310eb-142">name</span></span>     | <span data-ttu-id="310eb-143">Nome del flusso.</span><span class="sxs-lookup"><span data-stu-id="310eb-143">The name of the stream.</span></span> <span data-ttu-id="310eb-144">Questa proprietà viene scritta come `'strn'` blocco.</span><span class="sxs-lookup"><span data-stu-id="310eb-144">This property is written as a `'strn'` chunk.</span></span> |



 

<span data-ttu-id="310eb-145">Se il filtro è in esecuzione o in pausa, il metodo IPropertyBag:: Write restituisce \_ \_ lo stato VFW E non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="310eb-145">If the filter is running or paused, the IPropertyBag::Write method returns VFW\_E\_WRONG\_STATE.</span></span>

<span data-ttu-id="310eb-146">Frequenza fotogrammi</span><span class="sxs-lookup"><span data-stu-id="310eb-146">Frame Rates</span></span>

<span data-ttu-id="310eb-147">Se il filtro upstream non specifica una frequenza dei fotogrammi nel membro **AvgTimePerFrame** della struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , il mux AVI usa i timestamp sul primo fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="310eb-147">If the upstream filter does not specify a frame rate in the **AvgTimePerFrame** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, the AVI Mux uses the time stamps on the first video frame.</span></span> <span data-ttu-id="310eb-148">Il formato di file AVI non supporta le frequenze dei fotogrammi variabili.</span><span class="sxs-lookup"><span data-stu-id="310eb-148">The AVI file format does not support variable frame rates.</span></span>

<span data-ttu-id="310eb-149">Frame eliminati</span><span class="sxs-lookup"><span data-stu-id="310eb-149">Dropped Frames</span></span>

<span data-ttu-id="310eb-150">Il filtro Mux AVI calcola i frame eliminati in base ai tempi di supporto di ogni campione, se disponibili, oppure ai timestamp del campione.</span><span class="sxs-lookup"><span data-stu-id="310eb-150">The AVI Mux filter calculates dropped frames based on each sample's media times, if available, or else the sample's time stamps.</span></span> <span data-ttu-id="310eb-151">Scrive una voce di indice di lunghezza zero per ogni frame eliminato.</span><span class="sxs-lookup"><span data-stu-id="310eb-151">It writes a zero-length index entry for every dropped frame.</span></span>

<span data-ttu-id="310eb-152">IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="310eb-152">IMediaSeeking</span></span>

<span data-ttu-id="310eb-153">Il filtro Mux AVI implementa l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="310eb-153">The AVI Mux filter implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface as follows:</span></span>

-   <span data-ttu-id="310eb-154">Il metodo [**getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) restituisce lo stato di avanzamento corrente del multiplexing.</span><span class="sxs-lookup"><span data-stu-id="310eb-154">The [**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the current progress of the multiplexing.</span></span> <span data-ttu-id="310eb-155">Se si esegue la transcodifica di un file (più lento rispetto al tempo reale), questo valore è più preciso del valore restituito da Filter Graph Manager.</span><span class="sxs-lookup"><span data-stu-id="310eb-155">If you are transcoding a file (slower than real time), this value is more accurate than the value returned by the Filter Graph Manager.</span></span> <span data-ttu-id="310eb-156">Per ulteriori informazioni, vedere la sezione Osservazioni della pagina di riferimento di GetCurrentPosition.</span><span class="sxs-lookup"><span data-stu-id="310eb-156">For more information, see the Remarks section of the GetCurrentPosition reference page.</span></span>
-   <span data-ttu-id="310eb-157">Il metodo [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) esegue una query su ogni filtro upstream e restituisce la durata del flusso più lungo.</span><span class="sxs-lookup"><span data-stu-id="310eb-157">The [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method queries each upstream filter and returns the duration of the longest stream.</span></span> <span data-ttu-id="310eb-158">Se uno di questi filtri ha esito negativo sulla chiamata GetDuration (o non supporta IMediaSeeking), il mux AVI restituisce un codice di errore e compila il parametro *pDuration* con la durata più lunga trovata.</span><span class="sxs-lookup"><span data-stu-id="310eb-158">If any of these filters fails the GetDuration call (or does not support IMediaSeeking), the AVI Mux returns a failure code and fills in the *pDuration* parameter with the longest duration found.</span></span> <span data-ttu-id="310eb-159">Tuttavia, il valore di *pDuration* in questo caso non è necessariamente la lunghezza del flusso di input più lungo.</span><span class="sxs-lookup"><span data-stu-id="310eb-159">However, the value of *pDuration* in this case is not necessarily the length of the longest input stream.</span></span>
-   <span data-ttu-id="310eb-160">AVI Mux non implementa i metodi GetStopPosition, GetPositions, GetAvailable, getrate o GetPreroll; né implementa alcun \* metodo set per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="310eb-160">The AVI Mux does not implement the GetStopPosition, GetPositions, GetAvailable, GetRate, or GetPreroll methods; nor does it implement any Set\* methods for seeking.</span></span>

<span data-ttu-id="310eb-161">Estensioni del formato di file AVI 2,0</span><span class="sxs-lookup"><span data-stu-id="310eb-161">AVI 2.0 File Format Extensions</span></span>

<span data-ttu-id="310eb-162">DirectShow supporta attualmente le estensioni del formato di file AVI 2,0 seguenti:</span><span class="sxs-lookup"><span data-stu-id="310eb-162">DirectShow currently supports the following AVI 2.0 file format extensions:</span></span>

-   <span data-ttu-id="310eb-163">Aumento delle dimensioni del file AVI (maggiore di 1 GB)</span><span class="sxs-lookup"><span data-stu-id="310eb-163">Increased AVI file size (greater than 1 GB)</span></span>
-   <span data-ttu-id="310eb-164">Indicizzazione gerarchica</span><span class="sxs-lookup"><span data-stu-id="310eb-164">Hierarchical indexing</span></span>

<span data-ttu-id="310eb-165">Per ulteriori informazioni, vedere la versione 1,02 delle "estensioni di formato file AVI OpenDML" pubblicate dal sottocomitato formato file OpenDML AVI M-JPEG.</span><span class="sxs-lookup"><span data-stu-id="310eb-165">For more information, see version 1.02 of the "OpenDML AVI File Format Extensions" published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="310eb-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="310eb-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="310eb-167">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="310eb-167">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



