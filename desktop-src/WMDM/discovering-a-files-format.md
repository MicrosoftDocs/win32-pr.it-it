---
title: Individuazione del formato di un file
description: Individuazione del formato di un file
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows Media Gestione dispositivi, formati di file
- Gestione dispositivi, formati di file
- Guida per programmatori, formati di file
- applicazioni desktop, formati di file
- creazione di applicazioni Windows Media Gestione dispositivi, formati di file
- scrittura di file in dispositivi, formati di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b06c963b01e3b681fd078d8685e1c788c73352e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709703"
---
# <a name="discovering-a-files-format"></a><span data-ttu-id="d7122-109">Individuazione del formato di un file</span><span class="sxs-lookup"><span data-stu-id="d7122-109">Discovering a File's Format</span></span>

<span data-ttu-id="d7122-110">Prima di inviare un file al dispositivo, un'applicazione deve determinare se il dispositivo supporta tale formato di file.</span><span class="sxs-lookup"><span data-stu-id="d7122-110">Before sending a file to the device, an application should determine whether the device supports that file format.</span></span>

<span data-ttu-id="d7122-111">L'individuazione del formato di un file può essere complessa.</span><span class="sxs-lookup"><span data-stu-id="d7122-111">Discovering the format of a file can be complex.</span></span> <span data-ttu-id="d7122-112">Il modo più semplice consiste nel creare un elenco di estensioni di file di cui è stato eseguito il mapping a \_ valori di enumerazione WMDM FORMATCODE specifici.</span><span class="sxs-lookup"><span data-stu-id="d7122-112">The simplest way is to create a list of file extensions mapped to specific WMDM\_FORMATCODE enumeration values.</span></span> <span data-ttu-id="d7122-113">Tuttavia, esistono alcuni problemi con questo sistema: uno è che un singolo formato può avere più estensioni, ad esempio jpg, JPE e JPEG per le immagini JPEG.</span><span class="sxs-lookup"><span data-stu-id="d7122-113">However, there are a few problems with this system: one is that a single format can have multiple extensions (such as .jpg, .jpe, and .jpeg for JPEG images).</span></span> <span data-ttu-id="d7122-114">Inoltre, la stessa estensione di file può essere utilizzata da programmi diversi per formati diversi.</span><span class="sxs-lookup"><span data-stu-id="d7122-114">Also, the same file extension can be used by different programs for different formats.</span></span>

<span data-ttu-id="d7122-115">Per superare le limitazioni di un mapping rigoroso, è preferibile che in un'applicazione venga verificata la corrispondenza tra il formato e l'estensione.</span><span class="sxs-lookup"><span data-stu-id="d7122-115">To overcome the limitations of a strict mapping, it is best for an application to verify that the format matches the extension.</span></span> <span data-ttu-id="d7122-116">DirectShow SDK fornisce strumenti che consentono a un'applicazione di individuare un set limitato di dettagli sulla maggior parte dei tipi di file multimediali.</span><span class="sxs-lookup"><span data-stu-id="d7122-116">The DirectShow SDK provides tools that enable an application to discover a limited set of details about most media file types.</span></span> <span data-ttu-id="d7122-117">Windows Media Format SDK espone un numero elevato di dettagli, ma solo i file ASF.</span><span class="sxs-lookup"><span data-stu-id="d7122-117">The Windows Media Format SDK exposes a large number of details, but only about ASF files.</span></span> <span data-ttu-id="d7122-118">Poiché tutti i tipi di file devono avere il codice di formato verificato se possibile, è quindi consigliabile usare DirectShow per individuare o verificare il codice del formato di base e usare Windows Media Format SDK per individuare eventuali metadati aggiuntivi che si desiderano sui file ASF.</span><span class="sxs-lookup"><span data-stu-id="d7122-118">Because all file types should have their format code verified if possible, it is therefore best to use DirectShow to discover or verify the basic format code, and use the Windows Media Format SDK to discover any additional metadata desired about ASF files.</span></span> <span data-ttu-id="d7122-119">È inoltre possibile utilizzare DirectShow per individuare i metadati di base per i file non ASF.</span><span class="sxs-lookup"><span data-stu-id="d7122-119">DirectShow can also be used to discover basic metadata for non-ASF files.</span></span>

<span data-ttu-id="d7122-120">Di seguito è riportato un modo per individuare un formato di file usando il mapping delle estensioni e DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d7122-120">The following is one way to discover a file format using extension mapping and DirectShow.</span></span>

<span data-ttu-id="d7122-121">Per prima cosa, confrontare l'estensione del nome file con un elenco di estensioni note.</span><span class="sxs-lookup"><span data-stu-id="d7122-121">First, compare the file name extension to a list of known extensions.</span></span> <span data-ttu-id="d7122-122">Assicurarsi di eseguire il confronto senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d7122-122">Be sure to make your comparison case-insensitive.</span></span> <span data-ttu-id="d7122-123">Se l'estensione non è mappata, impostare il formato su WMDM \_ FORMATCODE \_ undefined.</span><span class="sxs-lookup"><span data-stu-id="d7122-123">If the extension is not mapped, set the format to WMDM\_FORMATCODE\_UNDEFINED.</span></span>

-   <span data-ttu-id="d7122-124">Se il codice di formato non è stato trovato (oppure si vuole verificare che un file sia un file multimediale), è possibile eseguire i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7122-124">If the format code was not found (or you want to verify that a file is a media file), you can perform the following steps:</span></span>
    1.  <span data-ttu-id="d7122-125">Creare un oggetto di rilevamento multimediale DirectShow usando **CoCreateInstance**(CLSID \_ mediadet) e recuperare l'interfaccia **IMediaDet** .</span><span class="sxs-lookup"><span data-stu-id="d7122-125">Create a DirectShow Media Detector object using **CoCreateInstance**(CLSID\_MediaDet), and retrieving the **IMediaDet** interface.</span></span>
    2.  <span data-ttu-id="d7122-126">Aprire il file chiamando **IMediaDet::p UT \_ filename**.</span><span class="sxs-lookup"><span data-stu-id="d7122-126">Open the file by calling **IMediaDet::put\_Filename**.</span></span> <span data-ttu-id="d7122-127">La chiamata avrà esito negativo se il file è protetto.</span><span class="sxs-lookup"><span data-stu-id="d7122-127">This call will fail if the file is protected.</span></span>
    3.  <span data-ttu-id="d7122-128">Ottenere il tipo di supporto del flusso predefinito chiamando **IMediaDet:: Get \_ StreamMediaType**, che restituisce un **tipo di \_ supporto \_ am**.</span><span class="sxs-lookup"><span data-stu-id="d7122-128">Get the media type of the default stream by calling **IMediaDet::get\_StreamMediaType**, which returns an **AM\_MEDIA\_TYPE**.</span></span>
    4.  <span data-ttu-id="d7122-129">Ottenere il numero di flussi chiamando **IMediaDet:: Get \_ OutputStreams**.</span><span class="sxs-lookup"><span data-stu-id="d7122-129">Get the number of streams by calling **IMediaDet::get\_OutputStreams**.</span></span>
        -   <span data-ttu-id="d7122-130">Se è presente un solo flusso ed è audio, il tipo di file è WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO</span><span class="sxs-lookup"><span data-stu-id="d7122-130">If there is only one stream and it is audio, the file type is WMDM\_FORMATCODE\_UNDEFINEDAUDIO</span></span>
        -   <span data-ttu-id="d7122-131">Se è presente un solo flusso ed è video, il tipo di file è WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO</span><span class="sxs-lookup"><span data-stu-id="d7122-131">If there is only one stream and it is video, the file type is WMDM\_FORMATCODE\_UNDEFINEDVIDEO</span></span>
        -   <span data-ttu-id="d7122-132">Se è presente un solo flusso ed è video e la velocità in bit è zero, il tipo di file è WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT.</span><span class="sxs-lookup"><span data-stu-id="d7122-132">If there is only one stream and it is video and the bit rate is zero, the file type is WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT.</span></span>

<span data-ttu-id="d7122-133">È anche possibile provare a abbinare codec audio o video dai membri **VIDEOINFOHEADER** o **WAVEFORMATEX** recuperati da **get \_ StreamMediaType**.</span><span class="sxs-lookup"><span data-stu-id="d7122-133">You could also try matching audio or video codecs from the **VIDEOINFOHEADER** or **WAVEFORMATEX** members retrieved from **get\_StreamMediaType**.</span></span>

<span data-ttu-id="d7122-134">La seguente funzione C++ illustra la corrispondenza dell'estensione di file e USA DirectShow per provare ad analizzare i file sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="d7122-134">The following C++ function demonstrates file extension matching and using DirectShow to try to analyze unknown files.</span></span>


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
WMDM_FORMATCODE CWMDMController::myGetWMDM_FORMATCODE(LPCWSTR pFileName)
{
    HRESULT hr = S_OK;

    // Declare the variable to hold the WMDM format code.
    WMDM_FORMATCODE fmt = WMDM_FORMATCODE_UNDEFINED;
    
    // Get the file extension.
    wstring ext = pFileName;
    ext = ext.substr(ext.find_last_of(L".") + 1);

    // This is not an exhaustive list. 
    // It is also case-sensitive.
    if (ext == L"js" || ext == L"vb")
        fmt = WMDM_FORMATCODE_SCRIPT;
    else if (ext == L".exe")
        fmt = WMDM_FORMATCODE_EXECUTABLE;
    else if (ext == L"txt")
        fmt = WMDM_FORMATCODE_TEXT;
    else if (ext == L"html" || ext == L"htm" || ext == L"shtm")
        fmt = WMDM_FORMATCODE_HTML;
    else if (ext == L"aiff")
        fmt = WMDM_FORMATCODE_AIFF;
    else if (ext == L"wav")
        fmt = WMDM_FORMATCODE_WAVE;
    else if (ext == L"mp3")
        fmt = WMDM_FORMATCODE_MP3;
    else if (ext == L"mpg" || ext == L"mpeg" || ext == L"mp2")
        fmt = WMDM_FORMATCODE_MPEG;
    else if (ext == L"bmp")
        fmt = WMDM_FORMATCODE_IMAGE_BMP;
    else if (ext == L"avi")
        fmt = WMDM_FORMATCODE_AVI;
    else if (ext == L"asf")
        fmt = WMDM_FORMATCODE_ASF;
    else if (ext == L"tif")
        fmt = WMDM_FORMATCODE_IMAGE_TIFF;
    else if (ext == L"gif")
        fmt = WMDM_FORMATCODE_IMAGE_GIF;
    else if (ext == L"pct")
        fmt = WMDM_FORMATCODE_IMAGE_PICT;
    else if (ext == L"png")
        fmt = WMDM_FORMATCODE_IMAGE_PNG;
    else if (ext == L"wma")
        fmt = WMDM_FORMATCODE_WMA;
    else if (ext == L"wpl")
        fmt = WMDM_FORMATCODE_WPLPLAYLIST;
    else if (ext == L"asx")
        fmt = WMDM_FORMATCODE_ASXPLAYLIST;
    else if (ext == L"m3u")
        fmt = WMDM_FORMATCODE_M3UPLAYLIST;
    else if (ext == L"wmv")
        fmt = WMDM_FORMATCODE_WMV;
    else if (ext == L"jpg" || ext == L"jpeg" || ext == L"jpe")
        fmt = WMDM_FORMATCODE_IMAGE_EXIF;
    else if (ext == L"jp2")
        fmt = WMDM_FORMATCODE_IMAGE_JP2;
    else if (ext == L"jpx" || ext == L"jpf")
        fmt = WMDM_FORMATCODE_IMAGE_JPX;

    // If we couldn't get the type from the extension, perhaps DirectShow 
    // can determine the type. You could also modify this to verify that 
    // the major media type matches the file extension (for example, that 
    // a .gif file has a video image stream with a bit rate of zero).
    if (fmt == WMDM_FORMATCODE_UNDEFINED)
    {
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (hr == S_OK && pIMediaDet != NULL)
        {
            hr = pIMediaDet->put_Filename(BSTR(pFileName));
            if (FAILED(hr)) return WMDM_FORMATCODE_UNDEFINED;

            AM_MEDIA_TYPE mediaType;
            if (hr == S_OK)
            {
                hr = pIMediaDet->get_StreamMediaType(&mediaType);
                CHECK_HR(hr, 
                  "get_StreamMediaType succeeded in myGetWMDM_FORMATCODE.", 
                  "get_StreamMediaType failed in myGetWMDM_FORMATCODE.");
            }

            if (hr == S_OK)
            {
                LONG numStreams = 0;
                hr = pIMediaDet->get_OutputStreams(&numStreams);

                // If there is at least one video stream, the file is video. 
                // If there are only audio streams, it is audio.
                // Loop through all streams or until first video stream is found.
                for (int i = 0; i < numStreams; i++)
                {
                    // Choices are either VIDEOINFOHEADER or WAVEFORMATEX. 
                    // VIDEOINFOHEADER2 is not supported.
                    if (IsEqualGUID(mediaType.formattype, 
                        FORMAT_VideoInfo))
                    {
                        VIDEOINFOHEADER* data = 
                            (VIDEOINFOHEADER*) mediaType.pbFormat;

                        // If only one stream and there was no matching 
                        // extension, it is undefined video. If no 
                        // bit rate, it's a still image.
                        if (data->dwBitRate == 0) fmt = 
                            WMDM_FORMATCODE_WINDOWSIMAGEFORMAT;
                        else fmt = WMDM_FORMATCODE_UNDEFINEDVIDEO;
                        break; // Found video--any additional streams are soundtracks.
                    }
                    if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
                    {
                        // If only one stream and there was no matching 
                        // extension, it is undefined audio. 
                        if (fmt == WMDM_FORMATCODE_UNDEFINED)
                        {
                            fmt = WMDM_FORMATCODE_UNDEFINEDAUDIO;
                        }
                        WAVEFORMATEX* data = 
                            (WAVEFORMATEX*) mediaType.pbFormat;
                    }
                } // Loop through streams.
            }     // Got a stream media type.
        }         // Created a media detector object.
    }
    return fmt;
}
```



## <a name="related-topics"></a><span data-ttu-id="d7122-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7122-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7122-136">**Scrittura di file nel dispositivo**</span><span class="sxs-lookup"><span data-stu-id="d7122-136">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




