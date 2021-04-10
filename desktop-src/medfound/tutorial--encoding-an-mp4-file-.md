---
description: Questa esercitazione illustra come usare l'API transcode per codificare un file MP4, usando H. 264 per il flusso video e AAC per il flusso audio.
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: 'Esercitazione: codifica di un file MP4'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae895ef321b35f080bf946384ee32d83c2c539fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226903"
---
# <a name="tutorial-encoding-an-mp4-file"></a><span data-ttu-id="c3add-103">Esercitazione: codifica di un file MP4</span><span class="sxs-lookup"><span data-stu-id="c3add-103">Tutorial: Encoding an MP4 File</span></span>

<span data-ttu-id="c3add-104">Questa esercitazione illustra come usare l' [API transcode](transcode-api.md) per codificare un file MP4, usando H. 264 per il flusso video e AAC per il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="c3add-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode an MP4 file, using H.264 for the video stream and AAC for the audio stream.</span></span>

-   [<span data-ttu-id="c3add-105">Intestazioni e file di libreria</span><span class="sxs-lookup"><span data-stu-id="c3add-105">Headers and Library Files</span></span>](#headers-and-library-files)
-   [<span data-ttu-id="c3add-106">Definire i profili di codifica</span><span class="sxs-lookup"><span data-stu-id="c3add-106">Define the Encoding Profiles</span></span>](#define-the-encoding-profiles)
-   [<span data-ttu-id="c3add-107">Scrivere la funzione wmain</span><span class="sxs-lookup"><span data-stu-id="c3add-107">Write the wmain Function</span></span>](#write-the-wmain-function)
-   [<span data-ttu-id="c3add-108">Codificare il file</span><span class="sxs-lookup"><span data-stu-id="c3add-108">Encode the File</span></span>](#encode-the-file)
    -   [<span data-ttu-id="c3add-109">Creare l'origine multimediale</span><span class="sxs-lookup"><span data-stu-id="c3add-109">Create the Media Source</span></span>](#create-the-media-source)
    -   [<span data-ttu-id="c3add-110">Ottenere la durata di origine</span><span class="sxs-lookup"><span data-stu-id="c3add-110">Get the Source Duration</span></span>](#get-the-source-duration)
    -   [<span data-ttu-id="c3add-111">Creare il profilo di transcodifica</span><span class="sxs-lookup"><span data-stu-id="c3add-111">Create the Transcode Profile</span></span>](#create-the-transcode-profile)
    -   [<span data-ttu-id="c3add-112">Eseguire la sessione di codifica</span><span class="sxs-lookup"><span data-stu-id="c3add-112">Run the Encoding Session</span></span>](#run-the-encoding-session)
-   [<span data-ttu-id="c3add-113">Helper della sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="c3add-113">Media Session Helper</span></span>](#media-session-helper)
-   [<span data-ttu-id="c3add-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3add-114">Related topics</span></span>](#related-topics)

## <a name="headers-and-library-files"></a><span data-ttu-id="c3add-115">Intestazioni e file di libreria</span><span class="sxs-lookup"><span data-stu-id="c3add-115">Headers and Library Files</span></span>

<span data-ttu-id="c3add-116">Includere i file di intestazione seguenti.</span><span class="sxs-lookup"><span data-stu-id="c3add-116">Include the following header files.</span></span>


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



<span data-ttu-id="c3add-117">Collegare i seguenti file di libreria.</span><span class="sxs-lookup"><span data-stu-id="c3add-117">Link the following library files.</span></span>


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a><span data-ttu-id="c3add-118">Definire i profili di codifica</span><span class="sxs-lookup"><span data-stu-id="c3add-118">Define the Encoding Profiles</span></span>

<span data-ttu-id="c3add-119">Un approccio alla codifica consiste nel definire un elenco di profili di codifica di destinazione noti in anticipo.</span><span class="sxs-lookup"><span data-stu-id="c3add-119">One approach to encoding is to define a list of target encoding profiles that are known in advance.</span></span> <span data-ttu-id="c3add-120">Per questa esercitazione, viene adottato un approccio relativamente semplice e viene archiviato un elenco di formati di codifica per audio AAC e video H. 264.</span><span class="sxs-lookup"><span data-stu-id="c3add-120">For this tutorial, we take a relatively simple approach, and store a list of encoding formats for H.264 video and AAC audio.</span></span>

<span data-ttu-id="c3add-121">Per H. 264, gli attributi di formato più importanti sono il profilo H. 264, la frequenza dei fotogrammi, le dimensioni del frame e la velocità in bit codificata.</span><span class="sxs-lookup"><span data-stu-id="c3add-121">For H.264, the most important format attributes are the H.264 profile, the frame rate, the frame size, and the encoded bit rate.</span></span> <span data-ttu-id="c3add-122">La matrice seguente contiene un elenco di formati di codifica H. 264.</span><span class="sxs-lookup"><span data-stu-id="c3add-122">The following array contains a list of H.264 encoding formats.</span></span>


```C++
struct H264ProfileInfo
{
    UINT32  profile;
    MFRatio fps;
    MFRatio frame_size;
    UINT32  bitrate;
};

H264ProfileInfo h264_profiles[] = 
{
    { eAVEncH264VProfile_Base, { 15, 1 },       { 176, 144 },   128000 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 30, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 29970, 1000 }, { 320, 240 },   528560 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 720, 576 },  4000000 },
    { eAVEncH264VProfile_Main, { 25, 1 },       { 720, 576 }, 10000000 },
    { eAVEncH264VProfile_Main, { 30, 1 },       { 352, 288 }, 10000000 },
};
```



<span data-ttu-id="c3add-123">I profili H. 264 vengono specificati usando l'enumerazione [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="c3add-123">H.264 profiles are specified using the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span> <span data-ttu-id="c3add-124">È anche possibile specificare il livello H. 264, ma il [**codificatore video h. 264**](h-264-video-encoder.md) Microsoft Media Foundation può derivare il livello appropriato per un determinato flusso video, pertanto è consigliabile non eseguire l'override del livello selezionato del codificatore.</span><span class="sxs-lookup"><span data-stu-id="c3add-124">You could also specify the H.264 level, but the Microsoft Media Foundation [**H.264 Video Encoder**](h-264-video-encoder.md) can derive the proper level for a given video stream, so it is recommended not to override the encoder's selected level.</span></span> <span data-ttu-id="c3add-125">Per i contenuti interlacciati, è necessario specificare anche la modalità interlacciata (vedere [interlacciamento video](video-interlacing.md)).</span><span class="sxs-lookup"><span data-stu-id="c3add-125">For interlaced content, you would also specify the interlace mode (see [Video Interlacing](video-interlacing.md)).</span></span>

<span data-ttu-id="c3add-126">Per l'audio AAC, gli attributi di formato più importanti sono la frequenza di campionamento audio, il numero di canali, il numero di bit per campione e la velocità in bit codificata.</span><span class="sxs-lookup"><span data-stu-id="c3add-126">For AAC audio, the most important format attributes are the audio sample rate, the number of channels, the number of bits per sample, and the encoded bit rate.</span></span> <span data-ttu-id="c3add-127">Facoltativamente, è possibile impostare l'indicazione del livello di profilo audio AAC.</span><span class="sxs-lookup"><span data-stu-id="c3add-127">Optionally, you can set the AAC audio profile level indication.</span></span> <span data-ttu-id="c3add-128">Per ulteriori informazioni, vedere [**AAC Encoder**](aac-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="c3add-128">For more information, see [**AAC Encoder**](aac-encoder.md).</span></span> <span data-ttu-id="c3add-129">La matrice seguente contiene un elenco di formati di codifica AAC.</span><span class="sxs-lookup"><span data-stu-id="c3add-129">The following array contains a list of AAC encoding formats.</span></span>


```C++
struct AACProfileInfo
{
    UINT32  samplesPerSec;
    UINT32  numChannels;
    UINT32  bitsPerSample;
    UINT32  bytesPerSec;
    UINT32  aacProfile;
};

AACProfileInfo aac_profiles[] = 
{
    { 96000, 2, 16, 24000, 0x29}, 
    { 48000, 2, 16, 24000, 0x29}, 
    { 44100, 2, 16, 16000, 0x29}, 
    { 44100, 2, 16, 12000, 0x29}, 
};
```



> [!Note]  
> <span data-ttu-id="c3add-130">Le `H264ProfileInfo` `AACProfileInfo` strutture e definite qui non fanno parte dell'API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c3add-130">The `H264ProfileInfo` and `AACProfileInfo` structures defined here are not part of the Media Foundation API.</span></span>

 

## <a name="write-the-wmain-function"></a><span data-ttu-id="c3add-131">Scrivere la funzione wmain</span><span class="sxs-lookup"><span data-stu-id="c3add-131">Write the wmain Function</span></span>

<span data-ttu-id="c3add-132">Il codice seguente illustra il punto di ingresso per l'applicazione console.</span><span class="sxs-lookup"><span data-stu-id="c3add-132">The following code shows the entry point for the console application.</span></span>


```C++
int video_profile = 0;
int audio_profile = 0;

int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc < 3 || argc > 5)
    {
        std::cout << "Usage:" << std::endl;
        std::cout << "input output [ audio_profile video_profile ]" << std::endl;
        return 1;
    }

    if (argc > 3)
    {
        audio_profile = _wtoi(argv[3]);
    }
    if (argc > 4)
    {
        video_profile = _wtoi(argv[4]);
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            hr = EncodeFile(argv[1], argv[2]);
            MFShutdown();
        }
        CoUninitialize();
    }

    if (SUCCEEDED(hr))
    {
        std::cout << "Done." << std::endl;
    }
    else
    {
        std::cout << "Error: " << std::hex << hr << std::endl;
    }

    return 0;
}
```



<span data-ttu-id="c3add-133">La `wmain` funzione esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3add-133">The `wmain` function does the following:</span></span>

1.  <span data-ttu-id="c3add-134">Chiama la funzione [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com.</span><span class="sxs-lookup"><span data-stu-id="c3add-134">Calls the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library.</span></span>
2.  <span data-ttu-id="c3add-135">Chiama la funzione [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) per inizializzare Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c3add-135">Calls the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize Media Foundation.</span></span>
3.  <span data-ttu-id="c3add-136">Chiama la funzione definita dall'applicazione `EncodeFile` .</span><span class="sxs-lookup"><span data-stu-id="c3add-136">Calls the application-defined `EncodeFile` function.</span></span> <span data-ttu-id="c3add-137">Questa funzione transcodifica il file di input nel file di output e viene illustrato nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="c3add-137">This function transcodes the input file to the output file, and is shown in the next section.</span></span>
4.  <span data-ttu-id="c3add-138">Chiama la funzione [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) per arrestare Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c3add-138">Calls the [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) function to shut down Media Foundation.</span></span>
5.  <span data-ttu-id="c3add-139">Chiamare la funzione [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) per annullare l'inizializzazione della libreria com.</span><span class="sxs-lookup"><span data-stu-id="c3add-139">Call the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function to uninitialize the COM library.</span></span>

## <a name="encode-the-file"></a><span data-ttu-id="c3add-140">Codificare il file</span><span class="sxs-lookup"><span data-stu-id="c3add-140">Encode the File</span></span>

<span data-ttu-id="c3add-141">Nel codice seguente viene illustrata la `EncodeFile` funzione, che esegue la transcodifica.</span><span class="sxs-lookup"><span data-stu-id="c3add-141">The following code shows `EncodeFile` function, which performs the transcoding.</span></span> <span data-ttu-id="c3add-142">Questa funzione è costituita principalmente da chiamate ad altre funzioni definite dall'applicazione, illustrate più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="c3add-142">This function consists mostly of calls to other application-defined functions, which are shown later in this topic.</span></span>


```C++
HRESULT EncodeFile(PCWSTR pszInput, PCWSTR pszOutput)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFMediaSource *pSource = NULL;
    IMFTopology *pTopology = NULL;
    CSession *pSession = NULL;

    MFTIME duration = 0;

    HRESULT hr = CreateMediaSource(pszInput, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetSourceDuration(pSource, &duration);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateTranscodeTopology(pSource, pszOutput, pProfile, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CSession::Create(&pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->StartEncodingSession(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = RunEncodingSession(pSession, duration);

done:            
    if (pSource)
    {
        pSource->Shutdown();
    }

    SafeRelease(&pSession);
    SafeRelease(&pProfile);
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="c3add-143">La `EncodeFile` funzione esegue i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c3add-143">The `EncodeFile` function performs the following steps.</span></span>

1.  <span data-ttu-id="c3add-144">Crea un'origine multimediale per il file di input, usando l'URL o il percorso del file di input.</span><span class="sxs-lookup"><span data-stu-id="c3add-144">Creates a media source for the input file, using the URL or file path of the input file.</span></span> <span data-ttu-id="c3add-145">(Vedere [creare l'origine multimediale](#create-the-media-source)).</span><span class="sxs-lookup"><span data-stu-id="c3add-145">(See [Create the Media Source](#create-the-media-source).)</span></span>
2.  <span data-ttu-id="c3add-146">Ottiene la durata del file di input.</span><span class="sxs-lookup"><span data-stu-id="c3add-146">Gets the duration of the input file.</span></span> <span data-ttu-id="c3add-147">(Vedere [ottenere la durata dell'origine](#get-the-source-duration)).</span><span class="sxs-lookup"><span data-stu-id="c3add-147">(See [Get the Source Duration](#get-the-source-duration).)</span></span>
3.  <span data-ttu-id="c3add-148">Creare il profilo transcodifica.</span><span class="sxs-lookup"><span data-stu-id="c3add-148">Create the transcode profile.</span></span> <span data-ttu-id="c3add-149">(Vedere [creare il profilo transcodifica](#create-the-transcode-profile)).</span><span class="sxs-lookup"><span data-stu-id="c3add-149">(See [Create the Transcode Profile](#create-the-transcode-profile).)</span></span>
4.  <span data-ttu-id="c3add-150">Chiamare [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) per creare la topologia transcodifica parziale.</span><span class="sxs-lookup"><span data-stu-id="c3add-150">Call [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) to create the partial transcode topology.</span></span>
5.  <span data-ttu-id="c3add-151">Creare un oggetto helper che gestisce la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="c3add-151">Create a helper object that manages the Media Session.</span></span> <span data-ttu-id="c3add-152">(Vedere helper della sessione multimediale).</span><span class="sxs-lookup"><span data-stu-id="c3add-152">(See Media Session Helper).</span></span>
6.  <span data-ttu-id="c3add-153">Eseguire la sessione di codifica e attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="c3add-153">Run the encoding session and wait for it to complete.</span></span> <span data-ttu-id="c3add-154">(Vedere [eseguire la sessione di codifica](#run-the-encoding-session)).</span><span class="sxs-lookup"><span data-stu-id="c3add-154">(See [Run the Encoding Session](#run-the-encoding-session).)</span></span>
7.  <span data-ttu-id="c3add-155">Chiamare [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) per arrestare l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="c3add-155">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
8.  <span data-ttu-id="c3add-156">Puntatori dell'interfaccia della versione.</span><span class="sxs-lookup"><span data-stu-id="c3add-156">Release interface pointers.</span></span> <span data-ttu-id="c3add-157">Questo codice usa la funzione [SafeRelease](saferelease.md) per rilasciare i puntatori a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c3add-157">This code uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span> <span data-ttu-id="c3add-158">Un'altra opzione consiste nell'usare una classe di puntatore intelligente COM, ad esempio **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="c3add-158">Another option is to use a COM smart pointer class, such as **CComPtr**.</span></span>

### <a name="create-the-media-source"></a><span data-ttu-id="c3add-159">Creare l'origine multimediale</span><span class="sxs-lookup"><span data-stu-id="c3add-159">Create the Media Source</span></span>

<span data-ttu-id="c3add-160">L'origine del supporto è l'oggetto che legge e analizza il file di input.</span><span class="sxs-lookup"><span data-stu-id="c3add-160">The media source is the object that reads and parses the input file.</span></span> <span data-ttu-id="c3add-161">Per creare l'origine del supporto, passare l'URL del file di input al [resolver di origine](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="c3add-161">To create the media source, pass the URL of the input file to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="c3add-162">A tal fine, osservare il codice indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c3add-162">The following code shows how to do this.</span></span>


```C++
HRESULT CreateMediaSource(PCWSTR pszURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source
    hr = pResolver->CreateObjectFromURL(pszURL, MF_RESOLUTION_MEDIASOURCE, 
        NULL, &ObjectType, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pResolver);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="c3add-163">Per ulteriori informazioni, vedere [using the source resolver](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="c3add-163">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

### <a name="get-the-source-duration"></a><span data-ttu-id="c3add-164">Ottenere la durata di origine</span><span class="sxs-lookup"><span data-stu-id="c3add-164">Get the Source Duration</span></span>

<span data-ttu-id="c3add-165">Sebbene non sia obbligatorio, è utile eseguire una query sull'origine multimediale per la durata del file di input.</span><span class="sxs-lookup"><span data-stu-id="c3add-165">Although not required, it is useful to query the media source for the duration of the input file.</span></span> <span data-ttu-id="c3add-166">Questo valore può essere usato per tenere traccia dello stato di avanzamento della codifica.</span><span class="sxs-lookup"><span data-stu-id="c3add-166">This value can be used to track the encoding progress.</span></span> <span data-ttu-id="c3add-167">La durata viene archiviata nell'attributo della [**\_ \_ durata MF PD**](mf-pd-duration-attribute.md) del descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="c3add-167">The duration is stored in the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute of the presentation descriptor.</span></span> <span data-ttu-id="c3add-168">Ottenere il descrittore della presentazione chiamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="c3add-168">Get the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



### <a name="create-the-transcode-profile"></a><span data-ttu-id="c3add-169">Creare il profilo di transcodifica</span><span class="sxs-lookup"><span data-stu-id="c3add-169">Create the Transcode Profile</span></span>

<span data-ttu-id="c3add-170">Il profilo transcode descrive i parametri di codifica.</span><span class="sxs-lookup"><span data-stu-id="c3add-170">The transcode profile describes the encoding parameters.</span></span> <span data-ttu-id="c3add-171">Per ulteriori informazioni sulla creazione di un profilo transcodifica, vedere [utilizzo dell'API transcodifica](fast-transcode-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c3add-171">For more information about creating a transcode profile, see [Using the Transcode API](fast-transcode-objects.md).</span></span> <span data-ttu-id="c3add-172">Per creare il profilo, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="c3add-172">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="c3add-173">Chiamare [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) per creare il profilo vuoto.</span><span class="sxs-lookup"><span data-stu-id="c3add-173">Call [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) to create the empty profile.</span></span>
2.  <span data-ttu-id="c3add-174">Creare un tipo di supporto per il flusso audio AAC.</span><span class="sxs-lookup"><span data-stu-id="c3add-174">Create a media type for the AAC audio stream.</span></span> <span data-ttu-id="c3add-175">Aggiungerlo al profilo chiamando [**IMFTranscodeProfile:: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span><span class="sxs-lookup"><span data-stu-id="c3add-175">Add it to the profile by calling [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span>
3.  <span data-ttu-id="c3add-176">Creare un tipo di supporto per il flusso video H. 264.</span><span class="sxs-lookup"><span data-stu-id="c3add-176">Create a media type for the H.264 video stream.</span></span> <span data-ttu-id="c3add-177">Aggiungerlo al profilo chiamando [**IMFTranscodeProfile:: SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span><span class="sxs-lookup"><span data-stu-id="c3add-177">Add it to the profile by calling [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span>
4.  <span data-ttu-id="c3add-178">Chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un archivio di attributi per gli attributi a livello di contenitore.</span><span class="sxs-lookup"><span data-stu-id="c3add-178">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
5.  <span data-ttu-id="c3add-179">Impostare l'attributo [MF \_ transcode \_ CONTAINERTYPE](mf-transcode-containertype.md) .</span><span class="sxs-lookup"><span data-stu-id="c3add-179">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute.</span></span> <span data-ttu-id="c3add-180">Si tratta dell'unico attributo a livello di contenitore obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c3add-180">This is the only required container-level attribute.</span></span> <span data-ttu-id="c3add-181">Per l'output del file MP4, impostare questo attributo su **MFTranscodeContainerType \_ MPEG4**.</span><span class="sxs-lookup"><span data-stu-id="c3add-181">For MP4 file output, set this attribute to **MFTranscodeContainerType\_MPEG4**.</span></span>
6.  <span data-ttu-id="c3add-182">Chiamare [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) per impostare gli attributi a livello di contenitore.</span><span class="sxs-lookup"><span data-stu-id="c3add-182">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes.</span></span>

<span data-ttu-id="c3add-183">Nel codice seguente vengono illustrati questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="c3add-183">The following code shows these steps.</span></span>


```C++
HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFAttributes *pAudio = NULL;
    IMFAttributes *pVideo = NULL;
    IMFAttributes *pContainer = NULL;

    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Audio attributes.
    hr = CreateAACProfile(audio_profile, &pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetAudioAttributes(pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Video attributes.
    hr = CreateH264Profile(video_profile, &pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetVideoAttributes(pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_MPEG4);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr)) 
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAudio);
    SafeRelease(&pVideo);
    SafeRelease(&pContainer);
    return hr;
}
```



<span data-ttu-id="c3add-184">Per specificare gli attributi per il flusso video H. 264, creare un archivio di attributi e impostare i seguenti attributi:</span><span class="sxs-lookup"><span data-stu-id="c3add-184">To specify the attributes for the H.264 video stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="c3add-185">Attributo</span><span class="sxs-lookup"><span data-stu-id="c3add-185">Attribute</span></span>                                                       | <span data-ttu-id="c3add-186">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3add-186">Desription</span></span>                      |
|-----------------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="c3add-187">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="c3add-187">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)              | <span data-ttu-id="c3add-188">Impostare su **MFVideoFormat \_ H264**.</span><span class="sxs-lookup"><span data-stu-id="c3add-188">Set to **MFVideoFormat\_H264**.</span></span> |
| [<span data-ttu-id="c3add-189">**\_ \_ Profilo MPEG2 MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="c3add-189">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md) | <span data-ttu-id="c3add-190">Profilo H. 264.</span><span class="sxs-lookup"><span data-stu-id="c3add-190">H.264 profile.</span></span>                  |
| [<span data-ttu-id="c3add-191">**\_dimensioni del \_ frame MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="c3add-191">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)       | <span data-ttu-id="c3add-192">Dimensioni del frame.</span><span class="sxs-lookup"><span data-stu-id="c3add-192">Frame size.</span></span>                     |
| [<span data-ttu-id="c3add-193">**\_ \_ frequenza fotogrammi MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="c3add-193">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)       | <span data-ttu-id="c3add-194">Frequenza di fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="c3add-194">Frame rate.</span></span>                     |
| [<span data-ttu-id="c3add-195">**\_velocità in \_ bit media MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="c3add-195">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)     | <span data-ttu-id="c3add-196">Velocità in bit codificata.</span><span class="sxs-lookup"><span data-stu-id="c3add-196">Encoded bit rate.</span></span>               |



 

<span data-ttu-id="c3add-197">Per specificare gli attributi per il flusso audio AAC, creare un archivio di attributi e impostare i seguenti attributi:</span><span class="sxs-lookup"><span data-stu-id="c3add-197">To specify the attributes for the AAC audio stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="c3add-198">Attributo</span><span class="sxs-lookup"><span data-stu-id="c3add-198">Attribute</span></span>                                                                                      | <span data-ttu-id="c3add-199">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3add-199">Desription</span></span>                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [<span data-ttu-id="c3add-200">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="c3add-200">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="c3add-201">Imposta su **MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="c3add-201">Set to **MFAudioFormat\_AAC**</span></span>            |
| [<span data-ttu-id="c3add-202">**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="c3add-202">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="c3add-203">Frequenza di campionamento audio.</span><span class="sxs-lookup"><span data-stu-id="c3add-203">Audio sample rate.</span></span>                       |
| [<span data-ttu-id="c3add-204">**\_ \_ bit audio MF \_ mt \_ per \_ campione**</span><span class="sxs-lookup"><span data-stu-id="c3add-204">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="c3add-205">Bit per esempio audio.</span><span class="sxs-lookup"><span data-stu-id="c3add-205">Bits per audio sample.</span></span>                   |
| [<span data-ttu-id="c3add-206">**numero \_ di \_ \_ canali audio MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="c3add-206">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="c3add-207">Numero dei canali audio.</span><span class="sxs-lookup"><span data-stu-id="c3add-207">Number of audio channels.</span></span>                |
| [<span data-ttu-id="c3add-208">**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="c3add-208">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="c3add-209">Velocità in bit codificata.</span><span class="sxs-lookup"><span data-stu-id="c3add-209">Encoded bit rate.</span></span>                        |
| [<span data-ttu-id="c3add-210">**\_ \_ \_ allineamento blocchi audio MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="c3add-210">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="c3add-211">impostare su 1.</span><span class="sxs-lookup"><span data-stu-id="c3add-211">Set to 1.</span></span>                                |
| [<span data-ttu-id="c3add-212">\_ \_ \_ \_ \_ indicazione livello profilo audio MF mt \_ AAC</span><span class="sxs-lookup"><span data-stu-id="c3add-212">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="c3add-213">Indicazione del livello di profilo AAC (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="c3add-213">AAC profile level indication (optional).</span></span> |



 

<span data-ttu-id="c3add-214">Il codice seguente crea gli attributi del flusso video.</span><span class="sxs-lookup"><span data-stu-id="c3add-214">The following code creates the video stream attributes.</span></span>


```C++
HRESULT CreateH264Profile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    IMFAttributes *pAttributes = NULL;

    const H264ProfileInfo& profile = h264_profiles[index];

    HRESULT hr = MFCreateAttributes(&pAttributes, 5);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_H264);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_MPEG2_PROFILE, profile.profile);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(
            pAttributes, MF_MT_FRAME_SIZE, 
            profile.frame_size.Numerator, profile.frame_size.Numerator);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(
            pAttributes, MF_MT_FRAME_RATE, 
            profile.fps.Numerator, profile.fps.Denominator);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AVG_BITRATE, profile.bitrate);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="c3add-215">Il codice seguente crea gli attributi del flusso audio.</span><span class="sxs-lookup"><span data-stu-id="c3add-215">The following code creates the audio stream attributes.</span></span>


```C++
HRESULT CreateAACProfile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    const AACProfileInfo& profile = aac_profiles[index];

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 7);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_AAC);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_BITS_PER_SAMPLE, profile.bitsPerSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_SAMPLES_PER_SECOND, profile.samplesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_NUM_CHANNELS, profile.numChannels);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_AVG_BYTES_PER_SECOND, profile.bytesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, 1);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION, profile.aacProfile);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="c3add-216">Si noti che l'API transcode non richiede un vero tipo di supporto, sebbene usi gli attributi di tipo supporto.</span><span class="sxs-lookup"><span data-stu-id="c3add-216">Note that the transcode API does not require a true media type, although it uses media-type attributes.</span></span> <span data-ttu-id="c3add-217">In particolare, l'attributo del [**\_ \_ \_ tipo principale MF mt**](mf-mt-major-type-attribute.md) non è obbligatorio perché i metodi [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) e [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) implicano il tipo principale.</span><span class="sxs-lookup"><span data-stu-id="c3add-217">In particular, the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute it not required, because the [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) and [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) methods imply the major type.</span></span> <span data-ttu-id="c3add-218">Tuttavia, è anche possibile passare un tipo di supporto effettivo a questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c3add-218">However, it also valid to pass an actual media type to these methods.</span></span> <span data-ttu-id="c3add-219">(L'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) eredita [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)).</span><span class="sxs-lookup"><span data-stu-id="c3add-219">(The [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface inherits [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)</span></span>

### <a name="run-the-encoding-session"></a><span data-ttu-id="c3add-220">Eseguire la sessione di codifica</span><span class="sxs-lookup"><span data-stu-id="c3add-220">Run the Encoding Session</span></span>

<span data-ttu-id="c3add-221">Il codice seguente esegue la sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="c3add-221">The following code runs the encoding session.</span></span> <span data-ttu-id="c3add-222">Usa la classe helper della sessione multimediale, illustrata nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="c3add-222">It uses the Media Session helper class, which is shown in the next section.</span></span>


```C++
HRESULT RunEncodingSession(CSession *pSession, MFTIME duration)
{
    const DWORD WAIT_PERIOD = 500;
    const int   UPDATE_INCR = 5;

    HRESULT hr = S_OK;
    MFTIME pos;
    LONGLONG prev = 0;
    while (1)
    {
        hr = pSession->Wait(WAIT_PERIOD);
        if (hr == E_PENDING)
        {
            hr = pSession->GetEncodingPosition(&pos);

            LONGLONG percent = (100 * pos) / duration ;
            if (percent >= prev + UPDATE_INCR)
            {
                std::cout << percent << "% .. ";  
                prev = percent;
            }
        }
        else
        {
            std::cout << std::endl;
            break;
        }
    }
    return hr;
}
```



## <a name="media-session-helper"></a><span data-ttu-id="c3add-223">Helper della sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="c3add-223">Media Session Helper</span></span>

<span data-ttu-id="c3add-224">La [sessione multimediale](media-session.md) è descritta più dettagliatamente nella sezione [architettura Media Foundation](media-foundation-architecture.md) di questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="c3add-224">The [Media Session](media-session.md) is described more fully in the [Media Foundation Architecture](media-foundation-architecture.md) section of this documentation.</span></span> <span data-ttu-id="c3add-225">La sessione multimediale usa un modello di eventi asincrono.</span><span class="sxs-lookup"><span data-stu-id="c3add-225">The Media Session uses an asynchronous event model.</span></span> <span data-ttu-id="c3add-226">In un'applicazione GUI è necessario rispondere agli eventi di sessione senza bloccare il thread dell'interfaccia utente per attendere l'evento successivo.</span><span class="sxs-lookup"><span data-stu-id="c3add-226">In a GUI application, you should respond to session events without blocking the UI thread to wait for the next event.</span></span> <span data-ttu-id="c3add-227">L'esercitazione [come riprodurre file multimediali non protetti](how-to-play-unprotected-media-files.md) Mostra come eseguire questa operazione in un'applicazione di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c3add-227">The tutorial [How to Play Unprotected Media Files](how-to-play-unprotected-media-files.md) shows how to do this in a playback application.</span></span> <span data-ttu-id="c3add-228">Per la codifica, il principio è lo stesso, ma un minor numero di eventi è pertinente:</span><span class="sxs-lookup"><span data-stu-id="c3add-228">For encoding, the principle is the same, but fewer events are relevant:</span></span>



| <span data-ttu-id="c3add-229">Evento</span><span class="sxs-lookup"><span data-stu-id="c3add-229">Event</span></span>                                  | <span data-ttu-id="c3add-230">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3add-230">Desription</span></span>                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3add-231">MESessionEnded</span><span class="sxs-lookup"><span data-stu-id="c3add-231">MESessionEnded</span></span>](mesessionended.md)   | <span data-ttu-id="c3add-232">Generato quando la codifica è completa.</span><span class="sxs-lookup"><span data-stu-id="c3add-232">Raised when the encoding is complete.</span></span>                                                                                                                            |
| [<span data-ttu-id="c3add-233">MESessionClosed</span><span class="sxs-lookup"><span data-stu-id="c3add-233">MESessionClosed</span></span>](mesessionclosed.md) | <span data-ttu-id="c3add-234">Generato quando il metodo [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) viene completato.</span><span class="sxs-lookup"><span data-stu-id="c3add-234">Raised when the [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes.</span></span> <span data-ttu-id="c3add-235">Dopo la generazione di questo evento, è possibile arrestare la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="c3add-235">After this event is raised, it is safe to shut down the Media Session.</span></span> |



 

<span data-ttu-id="c3add-236">Per un'applicazione console, è ragionevole bloccarsi e attendere gli eventi.</span><span class="sxs-lookup"><span data-stu-id="c3add-236">For a console application, it is reasonable to block and wait for events.</span></span> <span data-ttu-id="c3add-237">A seconda del file di origine e delle impostazioni di codifica, potrebbe essere necessario un po' di tempo per completare la codifica.</span><span class="sxs-lookup"><span data-stu-id="c3add-237">Depending on the source file and the encoding settings, it might take awhile to complete the encoding.</span></span> <span data-ttu-id="c3add-238">È possibile ottenere gli aggiornamenti dello stato di avanzamento come segue:</span><span class="sxs-lookup"><span data-stu-id="c3add-238">You can get progress updates as follows:</span></span>

1.  <span data-ttu-id="c3add-239">Chiamare [**IMFMediaSession:: getclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) per ottenere il clock di presentazione.</span><span class="sxs-lookup"><span data-stu-id="c3add-239">Call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) to get the presentation clock.</span></span>
2.  <span data-ttu-id="c3add-240">Eseguire una query sul clock per l'interfaccia [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .</span><span class="sxs-lookup"><span data-stu-id="c3add-240">Query the clock for the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span>
3.  <span data-ttu-id="c3add-241">Chiamare [**IMFPresentationClock:: GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) per ottenere la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="c3add-241">Call [**IMFPresentationClock::GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) to get the current position.</span></span>
4.  <span data-ttu-id="c3add-242">La posizione viene specificata in unità di tempo.</span><span class="sxs-lookup"><span data-stu-id="c3add-242">The position is given in units of time.</span></span> <span data-ttu-id="c3add-243">Per ottenere la percentuale completata, usare il valore `(100 * position) / duration` .</span><span class="sxs-lookup"><span data-stu-id="c3add-243">To get the percentage completed, use the value `(100 * position) / duration`.</span></span>

<span data-ttu-id="c3add-244">Di seguito è illustrata la dichiarazione della `CSession` classe.</span><span class="sxs-lookup"><span data-stu-id="c3add-244">Here is the declaration of the `CSession` class.</span></span>


```C++
class CSession  : public IMFAsyncCallback 
{
public:
    static HRESULT Create(CSession **ppSession);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP Invoke(IMFAsyncResult *pResult);

    // Other methods
    HRESULT StartEncodingSession(IMFTopology *pTopology);
    HRESULT GetEncodingPosition(MFTIME *pTime);
    HRESULT Wait(DWORD dwMsec);

private:
    CSession() : m_cRef(1), m_pSession(NULL), m_pClock(NULL), m_hrStatus(S_OK), m_hWaitEvent(NULL)
    {
    }
    virtual ~CSession()
    {
        if (m_pSession)
        {
            m_pSession->Shutdown();
        }

        SafeRelease(&m_pClock);
        SafeRelease(&m_pSession);
        CloseHandle(m_hWaitEvent);
    }

    HRESULT Initialize();

private:
    IMFMediaSession      *m_pSession;
    IMFPresentationClock *m_pClock;
    HRESULT m_hrStatus;
    HANDLE  m_hWaitEvent;
    long    m_cRef;
};
```



<span data-ttu-id="c3add-245">Nel codice seguente viene illustrata l'implementazione completa della `CSession` classe.</span><span class="sxs-lookup"><span data-stu-id="c3add-245">The following code shows the complete implementation of the `CSession` class.</span></span>


```C++
HRESULT CSession::Create(CSession **ppSession)
{
    *ppSession = NULL;

    CSession *pSession = new (std::nothrow) CSession();
    if (pSession == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pSession->Initialize();
    if (FAILED(hr))
    {
        pSession->Release();
        return hr;
    }
    *ppSession = pSession;
    return S_OK;
}

STDMETHODIMP CSession::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CSession, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CSession::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CSession::Release()
{
    long cRef = InterlockedDecrement(&m_cRef);
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}

HRESULT CSession::Initialize()
{
    IMFClock *pClock = NULL;

    HRESULT hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->GetClock(&pClock);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pClock));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->BeginGetEvent(this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_hWaitEvent = CreateEvent(NULL, FALSE, FALSE, NULL);  
    if (m_hWaitEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
done:
    SafeRelease(&pClock);
    return hr;
}

// Implements IMFAsyncCallback::Invoke
STDMETHODIMP CSession::Invoke(IMFAsyncResult *pResult)
{
    IMFMediaEvent* pEvent = NULL;
    MediaEventType meType = MEUnknown;
    HRESULT hrStatus = S_OK;

    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetStatus(&hrStatus);
    if (FAILED(hr))
    {
        goto done;
    }

    if (FAILED(hrStatus))
    {
        hr = hrStatus;
        goto done;
    }

    switch (meType)
    {
    case MESessionEnded:
        hr = m_pSession->Close();
        if (FAILED(hr))
        {
            goto done;
        }
        break;

    case MESessionClosed:
        SetEvent(m_hWaitEvent);
        break;
    }

    if (meType != MESessionClosed)
    {
        hr = m_pSession->BeginGetEvent(this, NULL);
    }

done:
    if (FAILED(hr))
    {
        m_hrStatus = hr;
        m_pSession->Close();
    }

    SafeRelease(&pEvent);
    return hr;
}

HRESULT CSession::StartEncodingSession(IMFTopology *pTopology)
{
    HRESULT hr = m_pSession->SetTopology(0, pTopology);
    if (SUCCEEDED(hr))
    {
        PROPVARIANT varStart;
        PropVariantClear(&varStart);
        hr = m_pSession->Start(&GUID_NULL, &varStart);
    }
    return hr;
}

HRESULT CSession::GetEncodingPosition(MFTIME *pTime)
{
    return m_pClock->GetTime(pTime);
}

HRESULT CSession::Wait(DWORD dwMsec)
{
    HRESULT hr = S_OK;

    DWORD dwTimeoutStatus = WaitForSingleObject(m_hWaitEvent, dwMsec);
    if (dwTimeoutStatus != WAIT_OBJECT_0)
    {
        hr = E_PENDING;
    }
    else
    {
        hr = m_hrStatus;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c3add-246">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3add-246">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3add-247">**Codificatore AAC**</span><span class="sxs-lookup"><span data-stu-id="c3add-247">**AAC Encoder**</span></span>](aac-encoder.md)
</dt> <dt>

[<span data-ttu-id="c3add-248">**Codificatore video H. 264**</span><span class="sxs-lookup"><span data-stu-id="c3add-248">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="c3add-249">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="c3add-249">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="c3add-250">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="c3add-250">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="c3add-251">API transcodifica</span><span class="sxs-lookup"><span data-stu-id="c3add-251">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 
