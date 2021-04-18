---
description: In questo argomento viene descritto quando e come usare un remux MFT e un sink MP4 H. 264/AVC.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Quando e come usare H. 264/AVC remux MFT e MP4 sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c582fa16eae56c4fec8809caa4bd501469e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310842"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="81013-103">Quando e come usare H. 264/AVC remux MFT e MP4 sink</span><span class="sxs-lookup"><span data-stu-id="81013-103">When and How to Use H.264/AVC Remux MFT and MP4 Sink</span></span>

<span data-ttu-id="81013-104">In questo argomento viene descritto quando e come usare un remux MFT e un sink MP4 H. 264/AVC.</span><span class="sxs-lookup"><span data-stu-id="81013-104">This topic describes when and how to use a H.264/AVC Remux MFT and MP4 Sink.</span></span>

## <a name="when-to-use-h264avc-remux-mft"></a><span data-ttu-id="81013-105">Quando usare H. 264/AVC remux MFT</span><span class="sxs-lookup"><span data-stu-id="81013-105">When to use H.264/AVC Remux MFT</span></span>

<span data-ttu-id="81013-106">Il formato di file MPEG-4 richiede che ogni esempio compresso contenga un'immagine principale con unità NAL nell'ordine corretto.</span><span class="sxs-lookup"><span data-stu-id="81013-106">MPEG-4 file format requires that each compressed sample contains one primary picture with NAL units in the correct order.</span></span> <span data-ttu-id="81013-107">(Fare riferimento alla definizione dell'immagine principale e dell'ordine di unità NAL obbligatorie nella sezione 7.4.1.2.3, **ordine di unità NAL e immagini codificate e associazione alle unità di accesso**, della specifica AVC H. 264). Richiede anche che ogni campione compresso sia associato a un timestamp di presentazione, alla decodifica del timestamp e alla durata del campione.</span><span class="sxs-lookup"><span data-stu-id="81013-107">(Please refer to the definition of primary picture and mandatory NAL units order in section 7.4.1.2.3, **Order of NAL units and coded pictures and association to access units**, of the H.264 AVC specification.) It also requires each compressed sample is associated with a presentation time stamp, decoding time stamp, and sample duration.</span></span>

<span data-ttu-id="81013-108">In molti scenari in cui le applicazioni devono registrare video H. 264/AVC in un contenitore di file MPEG-4, l'esempio compresso potrebbe non soddisfare i requisiti precedenti.</span><span class="sxs-lookup"><span data-stu-id="81013-108">In many scenarios when applications need to record H.264/AVC video in a MPEG-4 file container, the compressed sample may not satisfy the above requirements.</span></span> <span data-ttu-id="81013-109">Un esempio compresso, ad esempio, potrebbe non contenere un'immagine principale completa o potrebbe non essere associato a un timestamp di presentazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="81013-109">For example, one compressed sample might not contain a complete primary picture or might not have a correct presentation time stamp associated with it.</span></span> <span data-ttu-id="81013-110">Alcuni esempi di applicazioni sono:</span><span class="sxs-lookup"><span data-stu-id="81013-110">A few application examples are:</span></span>

-   <span data-ttu-id="81013-111">Scrivere il video elementare di streaming H. 264/AVC nel contenitore di file MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="81013-111">Write H.264/AVC streaming elementary video into MPEG-4 file container.</span></span>
-   <span data-ttu-id="81013-112">Registrare il video elementare H. 264/AVC della fotocamera nel contenitore di file MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="81013-112">Record camera captured H.264/AVC elementary video in MPEG-4 file container.</span></span>
-   <span data-ttu-id="81013-113">Registrare la conferenza video H. 264/AVC nel contenitore di file MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="81013-113">Record H.264/AVC video conference in MPEG-4 file container.</span></span>
-   <span data-ttu-id="81013-114">Concatenare due video H. 264/AVC in MPEG-2 TS o MP4 e scrivere nel contenitore di file MPEG-4 con timestamp corretti.</span><span class="sxs-lookup"><span data-stu-id="81013-114">Concatenate two H.264/AVC video in MPEG-2 TS or MP4 and write into MPEG-4 file container with correct time stamps.</span></span>
-   <span data-ttu-id="81013-115">Video remux H. 264/AVC dal formato di file AVCHD, MPEG-2 TS/PS al formato di file MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="81013-115">Remux H.264/AVC video from AVCHD, MPEG-2 TS/PS file format to MPEG-4 file format.</span></span>
-   <span data-ttu-id="81013-116">Tagliare il file video H. 264/AVC senza transcodifica.</span><span class="sxs-lookup"><span data-stu-id="81013-116">Trim H.264/AVC video file without transcoding.</span></span>

<span data-ttu-id="81013-117">In questa situazione, l'applicazione deve usare una remux MFT H. 264/AVC per convertire gli esempi compressi che non contengono un'immagine principale completa prima che vengano scritti nel contenitore di file MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="81013-117">In this situation, the application needs to use a H.264/AVC remux MFT to convert the compressed samples not containing a complete primary picture before they are written into the MPEG-4 file container.</span></span>

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="81013-118">Come usare H. 264/AVC remux MFT e MP4 sink</span><span class="sxs-lookup"><span data-stu-id="81013-118">How to use H.264/AVC Remux MFT and MP4 sink</span></span>

<span data-ttu-id="81013-119">Impostare il tipo di supporto di output di origine su **MFVideoFormat \_ H264 \_ es**, che indica che ogni campione potrebbe non contenere un'immagine principale completa.</span><span class="sxs-lookup"><span data-stu-id="81013-119">Set the source output media type to **MFVideoFormat\_H264\_ES**, which indicates each sample might not contain a complete primary picture.</span></span> <span data-ttu-id="81013-120">Impostare il tipo di supporto di input MP4 sink su **MFVideoFormat \_ H264**.</span><span class="sxs-lookup"><span data-stu-id="81013-120">Set the input media type of MP4 sink to **MFVideoFormat\_H264**.</span></span> <span data-ttu-id="81013-121">Il tipo di supporto di input di H. 264/AVC remux MFT è quindi **MFVideoFormat \_ H264 \_ es** e il tipo di supporto di output di h. 264/AVC remux MFT è **MFVideoFormat \_ H264**, che verrà inserito automaticamente nel resolver della topologia.</span><span class="sxs-lookup"><span data-stu-id="81013-121">So, the input media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264\_ES** and the output media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264**, which will be automatically inserted into the topology resolver.</span></span>

<span data-ttu-id="81013-122">La durata del campione viene ignorata dal remux H. 264/AVC, perché la durata del campione per un campione che non contiene un'immagine primaria completa non ha un significato chiaro.</span><span class="sxs-lookup"><span data-stu-id="81013-122">Sample duration is ignored by the H.264/AVC remux, because the sample duration for a sample not containing a complete primary picture does not have clear meaning.</span></span> <span data-ttu-id="81013-123">La durata del campione viene invece calcolata dalla frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="81013-123">Instead, the sample duration is calculated from the frame rate.</span></span> <span data-ttu-id="81013-124">La frequenza dei fotogrammi viene calcolata dal parametro Sequence.</span><span class="sxs-lookup"><span data-stu-id="81013-124">The frame rate is calculated from the sequence parameter.</span></span> <span data-ttu-id="81013-125">Se le informazioni non sono presenti nel parametro Sequence, la frequenza dei fotogrammi viene calcolata in base ai parametri nel tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="81013-125">If the information does not exist in the sequence parameter, the frame rate is calculated from the parameters in the input media type.</span></span> <span data-ttu-id="81013-126">Se non sono disponibili informazioni sulla frequenza dei fotogrammi, viene utilizzata la frequenza dei fotogrammi predefinita 29,97 fps.</span><span class="sxs-lookup"><span data-stu-id="81013-126">If frame rate information is not available, the default frame rate of 29.97 fps is used.</span></span>

<span data-ttu-id="81013-127">H. 264/AVC remux MFT esegue l'interpolazione lineare dei timestamp di decodifica (DTS) per ogni immagine compressa in base alla frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="81013-127">H.264/AVC remux MFT linearly interpolates the decoding time stamps (DTS) for each compressed picture according to the frame rate.</span></span> <span data-ttu-id="81013-128">H. 264/AVC remux MFT rispetta i timestamp di presentazione dell'input (PTS) negli esempi di input e li passa all'output se esistono.</span><span class="sxs-lookup"><span data-stu-id="81013-128">H.264/AVC remux MFT honors the input presentation time stamps (PTS) in input samples and passes them to the output if they exist.</span></span> <span data-ttu-id="81013-129">Esegue l'interpolazione PTS in base alla frequenza dei fotogrammi, ai punti precedenti e all'ordine di output dell'immagine tramite il processo di ingrandimento del buffering delle immagini decodificato (DBP), come specificato nel processo di ingrandimento **4.5.3** della specifica H. 264 AVC.</span><span class="sxs-lookup"><span data-stu-id="81013-129">It performs PTS interpolation according to frame rate, the previous PTS, and the picture output order through Decoded Picture Buffering (DBP) bumping process as specified in **Annex C.4.5.3 Bumping process** of the H.264 AVC specification.</span></span> <span data-ttu-id="81013-130">Ogni esempio di output di H. 264/AVC remux MFT deve avere PTS, DTS e la durata del campione.</span><span class="sxs-lookup"><span data-stu-id="81013-130">Each output sample from the H.264/AVC remux MFT shall have PTS, DTS, and sample duration.</span></span> <span data-ttu-id="81013-131">H. 264/AVC remux MFT identifica anche le immagini IDR nel bitstream e le imposta come punto di pulizia con l'attributo MF di [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="81013-131">H.264/AVC remux MFT also identifies the IDR pictures in the bitstream and sets them as clean point with the MF attribute of [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md).</span></span>

<span data-ttu-id="81013-132">Attualmente il remux MFT di H. 264/AVC può gestire un massimo di 64 di frame riordinato.</span><span class="sxs-lookup"><span data-stu-id="81013-132">Currently the H.264/AVC remux MFT can handle a maximum of 64 reordered frame.</span></span> <span data-ttu-id="81013-133">Se il numero di fotogrammi riordinati supera 64 con un frame di riferimento a lungo termine, l'remux MFT di H. 264/AVC eseguirà l'interpolazione di un PTS errato per quel frame e l'output del frame in un momento errato.</span><span class="sxs-lookup"><span data-stu-id="81013-133">If the number of reordered frame exceeds 64 with a long term reference frame present, the H.264/AVC remux MFT will interpolate a wrong PTS for that frame and output that frame at a wrong time.</span></span>

<span data-ttu-id="81013-134">Per creare un'istanza di un remux MFT H. 264/AVC, impostare i tipi di supporti di input e di output corretti nella MFT remux H. 264/AVC, impostare il tipo di supporto di input per il sink MP4 e risolvere la topologia.</span><span class="sxs-lookup"><span data-stu-id="81013-134">To instantiate a H.264/AVC remux MFT, set the correct input and output media types on the H.264/AVC remux MFT, set the input media type for the MP4 sink, and resolve the topology.</span></span>

<span data-ttu-id="81013-135">Il codice di esempio seguente illustra come inizializzare le remux MFT e MP4 del sink H. 264/AVC.</span><span class="sxs-lookup"><span data-stu-id="81013-135">The following sample code show how to initialize the H.264/AVC remux MFT and MP4 sink.</span></span>

<span data-ttu-id="81013-136">Per la remux MFT H. 264/AVC,</span><span class="sxs-lookup"><span data-stu-id="81013-136">For H.264/AVC remux MFT,</span></span>


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



<span data-ttu-id="81013-137">Non è richiesta alcuna configurazione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="81013-137">No further configuration is necessary.</span></span>

<span data-ttu-id="81013-138">Per il sink MP4,</span><span class="sxs-lookup"><span data-stu-id="81013-138">For MP4 sink,</span></span>


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a><span data-ttu-id="81013-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81013-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81013-140">Formati multimediali supportati in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="81013-140">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



