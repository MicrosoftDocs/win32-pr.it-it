---
description: Informazioni sui tipi di file multimediali in DirectShow. Il tipo di supporto è un modo universale ed estendibile per descrivere i formati multimediali digitali.
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Informazioni sui tipi di supporti (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b1489543b33f5eeb2c288add48148b37f31915
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010894"
---
# <a name="about-media-types-directshow"></a><span data-ttu-id="aa29a-104">Informazioni sui tipi di supporti (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="aa29a-104">About Media Types (DirectShow)</span></span>

<span data-ttu-id="aa29a-105">Poiché DirectShow è modulare, richiede un modo per descrivere il formato dei dati in ogni punto del grafico filtro.</span><span class="sxs-lookup"><span data-stu-id="aa29a-105">Because DirectShow is modular, it requires a way to describe the format of the data at each point in the filter graph.</span></span> <span data-ttu-id="aa29a-106">Si consideri ad esempio la riproduzione AVI.</span><span class="sxs-lookup"><span data-stu-id="aa29a-106">For example, consider AVI playback.</span></span> <span data-ttu-id="aa29a-107">I dati entrano nel grafico come flusso di blocchi RIFF.</span><span class="sxs-lookup"><span data-stu-id="aa29a-107">Data enters the graph as a stream of RIFF chunks.</span></span> <span data-ttu-id="aa29a-108">Questi vengono analizzati in flussi video e audio.</span><span class="sxs-lookup"><span data-stu-id="aa29a-108">These are parsed into video and audio streams.</span></span> <span data-ttu-id="aa29a-109">Il flusso video è costituito da fotogrammi video, che sono probabilmente compressi.</span><span class="sxs-lookup"><span data-stu-id="aa29a-109">The video stream consists of video frames, which are probably compressed.</span></span> <span data-ttu-id="aa29a-110">Dopo la decodifica, il flusso video è una serie di bitmap non compresse.</span><span class="sxs-lookup"><span data-stu-id="aa29a-110">After decoding, the video stream is a series of uncompressed bitmaps.</span></span> <span data-ttu-id="aa29a-111">Il flusso audio passa attraverso un processo simile.</span><span class="sxs-lookup"><span data-stu-id="aa29a-111">The audio stream goes through a similar process.</span></span>

<span data-ttu-id="aa29a-112">Tipi di supporti: descrizione dei formati di DirectShow</span><span class="sxs-lookup"><span data-stu-id="aa29a-112">Media Types: How DirectShow Represents Formats</span></span>

<span data-ttu-id="aa29a-113">Il *tipo di supporto* è un modo universale ed estendibile per descrivere i formati multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="aa29a-113">The *media type* is a universal and extensible way to describe digital media formats.</span></span> <span data-ttu-id="aa29a-114">Quando due filtri si connettono, concordano su un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="aa29a-114">When two filters connect, they agree on a media type.</span></span> <span data-ttu-id="aa29a-115">Il tipo di supporto identifica il tipo di dati che verrà recapitato dal filtro upstream al filtro downstream e il layout fisico dei dati.</span><span class="sxs-lookup"><span data-stu-id="aa29a-115">The media type identifies what kind of data the upstream filter will deliver to the downstream filter, and the physical layout of the data.</span></span> <span data-ttu-id="aa29a-116">Se due filtri non sono d'accordo su un tipo di supporto, non si connetteranno.</span><span class="sxs-lookup"><span data-stu-id="aa29a-116">If two filters cannot agree on a media type, they will not connect.</span></span>

<span data-ttu-id="aa29a-117">Per alcune applicazioni, non sarà mai necessario preoccuparsi dei tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="aa29a-117">For some applications, you will never have to worry about media types.</span></span> <span data-ttu-id="aa29a-118">Nella riproduzione di file, ad esempio, DirectShow gestisce tutti i dettagli.</span><span class="sxs-lookup"><span data-stu-id="aa29a-118">In file playback, for example, DirectShow handles all of the details.</span></span> <span data-ttu-id="aa29a-119">Altri tipi di applicazioni potrebbero dover lavorare direttamente con i tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="aa29a-119">Other kinds of applications may need to work directly with media types.</span></span>

<span data-ttu-id="aa29a-120">I tipi di supporti vengono definiti usando la [**struttura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)</span><span class="sxs-lookup"><span data-stu-id="aa29a-120">Media types are defined using the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="aa29a-121">Questa struttura contiene le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa29a-121">This structure contains the following information:</span></span>

-   <span data-ttu-id="aa29a-122">**Tipo principale:** il tipo principale è un GUID che definisce la categoria complessiva dei dati.</span><span class="sxs-lookup"><span data-stu-id="aa29a-122">**Major type**: The major type is a GUID that defines the overall category of the data.</span></span> <span data-ttu-id="aa29a-123">I tipi principali includono video, audio, flusso di byte non analizzato, dati MIDI e così via.</span><span class="sxs-lookup"><span data-stu-id="aa29a-123">Major types include video, audio, unparsed byte stream, MIDI data, and so forth.</span></span>
-   <span data-ttu-id="aa29a-124">**Sottotipo:** il sottotipo è un altro GUID, che definisce ulteriormente il formato.</span><span class="sxs-lookup"><span data-stu-id="aa29a-124">**Subtype**: The subtype is another GUID, which further defines the format.</span></span> <span data-ttu-id="aa29a-125">Ad esempio, all'interno del tipo principale video, sono presenti sottotipi per RGB-24, RGB-32, UYVY e così via.</span><span class="sxs-lookup"><span data-stu-id="aa29a-125">For example, within the video major type, there are subtypes for RGB-24, RGB-32, UYVY, and so forth.</span></span> <span data-ttu-id="aa29a-126">All'interno dell'audio sono presenti audio PCM, payload MPEG-1 e altri.</span><span class="sxs-lookup"><span data-stu-id="aa29a-126">Within audio, there is PCM audio, MPEG-1 payload, and others.</span></span> <span data-ttu-id="aa29a-127">Il sottotipo fornisce più informazioni rispetto al tipo principale, ma non definisce tutti gli elementi relativi al formato.</span><span class="sxs-lookup"><span data-stu-id="aa29a-127">The subtype provides more information than the major type, but it does not define everything about the format.</span></span> <span data-ttu-id="aa29a-128">Ad esempio, i sottotipi video non definiscono le dimensioni dell'immagine o la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="aa29a-128">For example, video subtypes do not define the image size or the frame rate.</span></span> <span data-ttu-id="aa29a-129">Questi sono definiti dal blocco di formato, descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="aa29a-129">These are defined by the format block, described below.</span></span>
-   <span data-ttu-id="aa29a-130">**Blocco di** formato: il blocco di formato è un blocco di dati che descrive il formato in dettaglio.</span><span class="sxs-lookup"><span data-stu-id="aa29a-130">**Format block**: The format block is a block of data that describes the format in detail.</span></span> <span data-ttu-id="aa29a-131">Il blocco di formato viene allocato separatamente dalla [**struttura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)</span><span class="sxs-lookup"><span data-stu-id="aa29a-131">The format block is allocated separately from the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="aa29a-132">Il **membro pbFormat** della struttura **AM MEDIA \_ \_ TYPE** punta al blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="aa29a-132">The **pbFormat** member of the **AM\_MEDIA\_TYPE** structure points to the format block.</span></span>

    <span data-ttu-id="aa29a-133">Il **membro pbFormat** è tipidato \**\* void* _ perché il layout del blocco di formato cambia a seconda del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="aa29a-133">The **pbFormat** member is typed \**void\** _ because the layout of the format block changes depending on the media type.</span></span> <span data-ttu-id="aa29a-134">Ad esempio, l'audio PCM usa [una struttura _ *WAVEFORMATEX.* \*](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aa29a-134">For example, PCM audio uses a [_ *WAVEFORMATEX*\*](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="aa29a-135">Il video usa varie strutture, tra cui [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) e [**VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span><span class="sxs-lookup"><span data-stu-id="aa29a-135">Video uses various structures, including [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span> <span data-ttu-id="aa29a-136">Il **membro formattype** della struttura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) è un GUID che specifica la struttura contenuta nel blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="aa29a-136">The **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure is a GUID that specifies which structure is contained in the format block.</span></span> <span data-ttu-id="aa29a-137">A ogni struttura di formato viene assegnato un GUID.</span><span class="sxs-lookup"><span data-stu-id="aa29a-137">Each format structure is assigned a GUID.</span></span> <span data-ttu-id="aa29a-138">Il **membro cbFormat** specifica le dimensioni del blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="aa29a-138">The **cbFormat** member specifies the size of the format block.</span></span> <span data-ttu-id="aa29a-139">Controllare sempre questi valori prima di dereferenziare il **puntatore pbFormat.**</span><span class="sxs-lookup"><span data-stu-id="aa29a-139">Always check these values before dereferencing the **pbFormat** pointer.</span></span>

<span data-ttu-id="aa29a-140">Se il blocco di formato viene compilato, il tipo principale e il sottotipo contengono informazioni ridondanti.</span><span class="sxs-lookup"><span data-stu-id="aa29a-140">If the format block is filled in, then the major type and subtype contain redundant information.</span></span> <span data-ttu-id="aa29a-141">Il tipo principale e il sottotipo, tuttavia, forniscono un modo pratico per identificare i formati senza un blocco di formato completo.</span><span class="sxs-lookup"><span data-stu-id="aa29a-141">The major type and subtype, however, provide a convenient way to identify formats without a complete format block.</span></span> <span data-ttu-id="aa29a-142">Ad esempio, è possibile specificare un formato RGB a 24 bit generico (MEDIASUBTYPE RGB24), senza conoscere tutte le informazioni richieste dalla struttura \_ [**VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ad esempio le dimensioni dell'immagine e la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="aa29a-142">For example, you can specify a generic 24-bit RGB format (MEDIASUBTYPE\_RGB24), without knowing all of the information required by the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, such as image size and frame rate.</span></span>

<span data-ttu-id="aa29a-143">Ad esempio, un filtro potrebbe usare il codice seguente per controllare un tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="aa29a-143">For example, a filter might use the following code to check a media type:</span></span>


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



<span data-ttu-id="aa29a-144">La [**struttura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) contiene anche alcuni campi facoltativi.</span><span class="sxs-lookup"><span data-stu-id="aa29a-144">The [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure also contains some optional fields.</span></span> <span data-ttu-id="aa29a-145">Questi possono essere usati per fornire informazioni aggiuntive, ma i filtri non sono necessari per usarli:</span><span class="sxs-lookup"><span data-stu-id="aa29a-145">These can be used to provide additional information, but filters are not required to use them:</span></span>

-   <span data-ttu-id="aa29a-146">**lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="aa29a-146">**lSampleSize**.</span></span> <span data-ttu-id="aa29a-147">Se questo campo è diverso da zero, definisce le dimensioni di ogni campione.</span><span class="sxs-lookup"><span data-stu-id="aa29a-147">If this field is non-zero, it defines the size of each sample.</span></span> <span data-ttu-id="aa29a-148">Se è zero, indica che le dimensioni del campione possono cambiare da campione a campione.</span><span class="sxs-lookup"><span data-stu-id="aa29a-148">If it is zero, it indicates that the sample size may change from sample to sample.</span></span>
-   <span data-ttu-id="aa29a-149">**bFixedSizeSamples**.</span><span class="sxs-lookup"><span data-stu-id="aa29a-149">**bFixedSizeSamples**.</span></span> <span data-ttu-id="aa29a-150">Se questo flag booleano **è TRUE,** significa che il valore in **lSampleSize** è valido.</span><span class="sxs-lookup"><span data-stu-id="aa29a-150">If this Boolean flag is **TRUE**, it means the value in **lSampleSize** is valid.</span></span> <span data-ttu-id="aa29a-151">In caso contrario, ignorare **lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="aa29a-151">Otherwise, you should ignore **lSampleSize**.</span></span>
-   <span data-ttu-id="aa29a-152">**bRalCompression**.</span><span class="sxs-lookup"><span data-stu-id="aa29a-152">**bTemporalCompression**.</span></span> <span data-ttu-id="aa29a-153">Se questo flag booleano **è FALSE,** significa che tutti i fotogrammi sono fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="aa29a-153">If this Boolean flag is **FALSE**, it means that all frames are key frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa29a-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa29a-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa29a-155">Grafico dei filtri e relativi componenti</span><span class="sxs-lookup"><span data-stu-id="aa29a-155">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
