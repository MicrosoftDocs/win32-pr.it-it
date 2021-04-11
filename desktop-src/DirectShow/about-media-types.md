---
description: Informazioni sui tipi di supporto
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Informazioni sui tipi di supporto (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3289a37e95bf5dbd1e5c277b5799a2c7c8c90586
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351231"
---
# <a name="about-media-types-directshow"></a><span data-ttu-id="25a2b-103">Informazioni sui tipi di supporto (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="25a2b-103">About Media Types (DirectShow)</span></span>

<span data-ttu-id="25a2b-104">Poiché DirectShow è modulare, richiede un modo per descrivere il formato dei dati in ogni punto del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="25a2b-104">Because DirectShow is modular, it requires a way to describe the format of the data at each point in the filter graph.</span></span> <span data-ttu-id="25a2b-105">Ad esempio, si consideri la riproduzione AVI.</span><span class="sxs-lookup"><span data-stu-id="25a2b-105">For example, consider AVI playback.</span></span> <span data-ttu-id="25a2b-106">I dati entrano nel grafico come un flusso di blocchi RIFF.</span><span class="sxs-lookup"><span data-stu-id="25a2b-106">Data enters the graph as a stream of RIFF chunks.</span></span> <span data-ttu-id="25a2b-107">Questi vengono analizzati in flussi video e audio.</span><span class="sxs-lookup"><span data-stu-id="25a2b-107">These are parsed into video and audio streams.</span></span> <span data-ttu-id="25a2b-108">Il flusso video è costituito da fotogrammi video, probabilmente compressi.</span><span class="sxs-lookup"><span data-stu-id="25a2b-108">The video stream consists of video frames, which are probably compressed.</span></span> <span data-ttu-id="25a2b-109">Dopo la decodifica, il flusso video è una serie di bitmap non compresse.</span><span class="sxs-lookup"><span data-stu-id="25a2b-109">After decoding, the video stream is a series of uncompressed bitmaps.</span></span> <span data-ttu-id="25a2b-110">Il flusso audio passa attraverso un processo simile.</span><span class="sxs-lookup"><span data-stu-id="25a2b-110">The audio stream goes through a similar process.</span></span>

<span data-ttu-id="25a2b-111">Tipi di supporto: come DirectShow rappresenta i formati</span><span class="sxs-lookup"><span data-stu-id="25a2b-111">Media Types: How DirectShow Represents Formats</span></span>

<span data-ttu-id="25a2b-112">Il *tipo di supporto* è un modo universale ed estendibile per descrivere i formati multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="25a2b-112">The *media type* is a universal and extensible way to describe digital media formats.</span></span> <span data-ttu-id="25a2b-113">Quando due filtri si connettono, accettano un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="25a2b-113">When two filters connect, they agree on a media type.</span></span> <span data-ttu-id="25a2b-114">Il tipo di supporto identifica il tipo di dati che il filtro upstream fornirà al filtro downstream e il layout fisico dei dati.</span><span class="sxs-lookup"><span data-stu-id="25a2b-114">The media type identifies what kind of data the upstream filter will deliver to the downstream filter, and the physical layout of the data.</span></span> <span data-ttu-id="25a2b-115">Se due filtri non sono in grado di accettare un tipo di supporto, non verranno connessi.</span><span class="sxs-lookup"><span data-stu-id="25a2b-115">If two filters cannot agree on a media type, they will not connect.</span></span>

<span data-ttu-id="25a2b-116">Per alcune applicazioni, non sarà mai necessario preoccuparsi dei tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="25a2b-116">For some applications, you will never have to worry about media types.</span></span> <span data-ttu-id="25a2b-117">Nella riproduzione dei file, ad esempio, DirectShow gestisce tutti i dettagli.</span><span class="sxs-lookup"><span data-stu-id="25a2b-117">In file playback, for example, DirectShow handles all of the details.</span></span> <span data-ttu-id="25a2b-118">È possibile che altri tipi di applicazioni debbano funzionare direttamente con i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="25a2b-118">Other kinds of applications may need to work directly with media types.</span></span>

<span data-ttu-id="25a2b-119">I tipi di supporto vengono definiti utilizzando la struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="25a2b-119">Media types are defined using the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="25a2b-120">Questa struttura contiene le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="25a2b-120">This structure contains the following information:</span></span>

-   <span data-ttu-id="25a2b-121">**Tipo principale**: il tipo principale è un GUID che definisce la categoria complessiva dei dati.</span><span class="sxs-lookup"><span data-stu-id="25a2b-121">**Major type**: The major type is a GUID that defines the overall category of the data.</span></span> <span data-ttu-id="25a2b-122">I tipi principali includono video, audio, flusso di byte non analizzato, dati MIDI e così via.</span><span class="sxs-lookup"><span data-stu-id="25a2b-122">Major types include video, audio, unparsed byte stream, MIDI data, and so forth.</span></span>
-   <span data-ttu-id="25a2b-123">**Sottotipo**: il sottotipo è un altro GUID, che definisce ulteriormente il formato.</span><span class="sxs-lookup"><span data-stu-id="25a2b-123">**Subtype**: The subtype is another GUID, which further defines the format.</span></span> <span data-ttu-id="25a2b-124">Ad esempio, all'interno del tipo principale video sono presenti sottotipi per RGB-24, RGB-32, UYVY e così via.</span><span class="sxs-lookup"><span data-stu-id="25a2b-124">For example, within the video major type, there are subtypes for RGB-24, RGB-32, UYVY, and so forth.</span></span> <span data-ttu-id="25a2b-125">All'interno di audio, sono presenti audio PCM, payload MPEG-1 e altri.</span><span class="sxs-lookup"><span data-stu-id="25a2b-125">Within audio, there is PCM audio, MPEG-1 payload, and others.</span></span> <span data-ttu-id="25a2b-126">Il sottotipo fornisce più informazioni rispetto al tipo principale, ma non definisce tutti gli elementi del formato.</span><span class="sxs-lookup"><span data-stu-id="25a2b-126">The subtype provides more information than the major type, but it does not define everything about the format.</span></span> <span data-ttu-id="25a2b-127">Ad esempio, i sottotipi video non definiscono le dimensioni dell'immagine o la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="25a2b-127">For example, video subtypes do not define the image size or the frame rate.</span></span> <span data-ttu-id="25a2b-128">Questi vengono definiti dal blocco di formato, descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="25a2b-128">These are defined by the format block, described below.</span></span>
-   <span data-ttu-id="25a2b-129">**Format Block**: il blocco di formato è un blocco di dati che descrive in dettaglio il formato.</span><span class="sxs-lookup"><span data-stu-id="25a2b-129">**Format block**: The format block is a block of data that describes the format in detail.</span></span> <span data-ttu-id="25a2b-130">Il blocco di formato viene allocato separatamente dalla struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="25a2b-130">The format block is allocated separately from the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="25a2b-131">Il membro **pbFormat** della struttura **del \_ \_ tipo di supporto am** punta al blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="25a2b-131">The **pbFormat** member of the **AM\_MEDIA\_TYPE** structure points to the format block.</span></span>

    <span data-ttu-id="25a2b-132">Il membro **pbFormat** è tipizzato \*\* \* void\* _ perché il layout del blocco di formato cambia a seconda del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="25a2b-132">The **pbFormat** member is typed \**void\** _ because the layout of the format block changes depending on the media type.</span></span> <span data-ttu-id="25a2b-133">Ad esempio, l'audio PCM usa una struttura [_ *WAVEFORMATEX* \*](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="25a2b-133">For example, PCM audio uses a [_ *WAVEFORMATEX*\*](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="25a2b-134">Il video usa varie strutture, tra cui [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) e [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="25a2b-134">Video uses various structures, including [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span> <span data-ttu-id="25a2b-135">Il membro **formatType** della struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) è un GUID che specifica la struttura contenuta nel blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="25a2b-135">The **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure is a GUID that specifies which structure is contained in the format block.</span></span> <span data-ttu-id="25a2b-136">A ogni struttura di formato viene assegnato un GUID.</span><span class="sxs-lookup"><span data-stu-id="25a2b-136">Each format structure is assigned a GUID.</span></span> <span data-ttu-id="25a2b-137">Il membro **cbFormat** specifica le dimensioni del blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="25a2b-137">The **cbFormat** member specifies the size of the format block.</span></span> <span data-ttu-id="25a2b-138">Controllare sempre questi valori prima di dereferenziare il puntatore **pbFormat** .</span><span class="sxs-lookup"><span data-stu-id="25a2b-138">Always check these values before dereferencing the **pbFormat** pointer.</span></span>

<span data-ttu-id="25a2b-139">Se il blocco di formato è compilato, il tipo e il sottotipo principale contengono informazioni ridondanti.</span><span class="sxs-lookup"><span data-stu-id="25a2b-139">If the format block is filled in, then the major type and subtype contain redundant information.</span></span> <span data-ttu-id="25a2b-140">Il tipo e il sottotipo principale, tuttavia, costituiscono un modo pratico per identificare i formati senza un blocco di formato completo.</span><span class="sxs-lookup"><span data-stu-id="25a2b-140">The major type and subtype, however, provide a convenient way to identify formats without a complete format block.</span></span> <span data-ttu-id="25a2b-141">Ad esempio, è possibile specificare un formato RGB a 24 bit generico (MEDIASUBTYPE \_ RGB24), senza conoscere tutte le informazioni necessarie per la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , ad esempio le dimensioni dell'immagine e la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="25a2b-141">For example, you can specify a generic 24-bit RGB format (MEDIASUBTYPE\_RGB24), without knowing all of the information required by the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, such as image size and frame rate.</span></span>

<span data-ttu-id="25a2b-142">Ad esempio, un filtro può utilizzare il codice seguente per controllare un tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="25a2b-142">For example, a filter might use the following code to check a media type:</span></span>


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



<span data-ttu-id="25a2b-143">La struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) contiene anche alcuni campi facoltativi.</span><span class="sxs-lookup"><span data-stu-id="25a2b-143">The [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure also contains some optional fields.</span></span> <span data-ttu-id="25a2b-144">Questi possono essere usati per fornire informazioni aggiuntive, ma i filtri non sono necessari per utilizzarli:</span><span class="sxs-lookup"><span data-stu-id="25a2b-144">These can be used to provide additional information, but filters are not required to use them:</span></span>

-   <span data-ttu-id="25a2b-145">**lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="25a2b-145">**lSampleSize**.</span></span> <span data-ttu-id="25a2b-146">Se questo campo è diverso da zero, definisce la dimensione di ogni campione.</span><span class="sxs-lookup"><span data-stu-id="25a2b-146">If this field is non-zero, it defines the size of each sample.</span></span> <span data-ttu-id="25a2b-147">Se è zero, indica che la dimensione del campione può variare da campione a campione.</span><span class="sxs-lookup"><span data-stu-id="25a2b-147">If it is zero, it indicates that the sample size may change from sample to sample.</span></span>
-   <span data-ttu-id="25a2b-148">**bFixedSizeSamples**.</span><span class="sxs-lookup"><span data-stu-id="25a2b-148">**bFixedSizeSamples**.</span></span> <span data-ttu-id="25a2b-149">Se questo flag booleano è **true**, significa che il valore in **lSampleSize** è valido.</span><span class="sxs-lookup"><span data-stu-id="25a2b-149">If this Boolean flag is **TRUE**, it means the value in **lSampleSize** is valid.</span></span> <span data-ttu-id="25a2b-150">In caso contrario, è consigliabile ignorare **lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="25a2b-150">Otherwise, you should ignore **lSampleSize**.</span></span>
-   <span data-ttu-id="25a2b-151">**bTemporalCompression**.</span><span class="sxs-lookup"><span data-stu-id="25a2b-151">**bTemporalCompression**.</span></span> <span data-ttu-id="25a2b-152">Se questo flag booleano è **false**, significa che tutti i frame sono fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="25a2b-152">If this Boolean flag is **FALSE**, it means that all frames are key frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25a2b-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="25a2b-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25a2b-154">Il grafico del filtro e i relativi componenti</span><span class="sxs-lookup"><span data-stu-id="25a2b-154">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
