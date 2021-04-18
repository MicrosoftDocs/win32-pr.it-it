---
description: Questo argomento descrive come usare MFPlay per visualizzare l'anteprima del video da una videocamera video.
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: Anteprima video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d458568a18f598e5aa4ee7e8fb21059e503362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308977"
---
# <a name="video-preview"></a><span data-ttu-id="784d4-103">Anteprima video</span><span class="sxs-lookup"><span data-stu-id="784d4-103">Video Preview</span></span>

<span data-ttu-id="784d4-104">\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="784d4-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="784d4-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="784d4-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="784d4-106">\]</span><span class="sxs-lookup"><span data-stu-id="784d4-106">\]</span></span>

<span data-ttu-id="784d4-107">Questo argomento descrive come usare MFPlay per visualizzare l'anteprima del video da una videocamera video.</span><span class="sxs-lookup"><span data-stu-id="784d4-107">This topic describes how to use MFPlay to preview video from a video camera.</span></span>

<span data-ttu-id="784d4-108">MFPlay fornisce il modo più semplice per Microsoft Media Foundation di visualizzare in anteprima i video da un dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="784d4-108">MFPlay provides the simplest way in Microsoft Media Foundation to preview video from a capture device.</span></span> <span data-ttu-id="784d4-109">È consigliabile utilizzare MFPlay se si verificano tutte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="784d4-109">You should use MFPlay if the following conditions are all true:</span></span>

-   <span data-ttu-id="784d4-110">Non è necessario acquisire il video in un file.</span><span class="sxs-lookup"><span data-stu-id="784d4-110">You do not need to capture the video to a file.</span></span>
-   <span data-ttu-id="784d4-111">Non è necessario un controllo con granularità fine sulla modalità di rendering del video.</span><span class="sxs-lookup"><span data-stu-id="784d4-111">You do not need fine-grained control over how the video is rendered.</span></span> <span data-ttu-id="784d4-112">Non è ad esempio necessario controllare la creazione del dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="784d4-112">(For example, you do not need to control the creation of the Direct3D device.)</span></span>
-   <span data-ttu-id="784d4-113">Non è necessario elaborare i dati video dalla fotocamera prima del rendering.</span><span class="sxs-lookup"><span data-stu-id="784d4-113">You do not need to process the video data from the camera prior to rendering.</span></span>

<span data-ttu-id="784d4-114">In caso contrario, il [lettore di origine](source-reader.md) potrebbe essere un'opzione migliore.</span><span class="sxs-lookup"><span data-stu-id="784d4-114">Otherwise, the [Source Reader](source-reader.md) may be a better option.</span></span>

<span data-ttu-id="784d4-115">Per usare MFPlay con un dispositivo di acquisizione video, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="784d4-115">To use MFPlay with a video capture device, perform the following steps:</span></span>

1.  <span data-ttu-id="784d4-116">Creare un'origine multimediale per il dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="784d4-116">Create a media source for the capture device.</span></span> <span data-ttu-id="784d4-117">Vedere [enumerazione dei dispositivi di acquisizione video](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="784d4-117">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="784d4-118">Chiamare [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) per creare un'istanza dell'oggetto Player.</span><span class="sxs-lookup"><span data-stu-id="784d4-118">Call [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create an instance of the player object.</span></span>
3.  <span data-ttu-id="784d4-119">Chiamare il metodo [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) .</span><span class="sxs-lookup"><span data-stu-id="784d4-119">Call the [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) method.</span></span> <span data-ttu-id="784d4-120">Passare un puntatore all'interfaccia IMFMediaSource dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="784d4-120">Pass in a pointer to the IMFMediaSource interface of the media source.</span></span> <span data-ttu-id="784d4-121">Il metodo riceve un puntatore all'interfaccia [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) .</span><span class="sxs-lookup"><span data-stu-id="784d4-121">The method receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface.</span></span>
4.  <span data-ttu-id="784d4-122">Chiamare [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span><span class="sxs-lookup"><span data-stu-id="784d4-122">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span></span>
5.  <span data-ttu-id="784d4-123">Chiamare [**IMFPMediaPlayer::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) per iniziare l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="784d4-123">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to begin previewing.</span></span>

<span data-ttu-id="784d4-124">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="784d4-124">The following code shows these steps:</span></span>


```C++
    IMFPMediaItem *pItem = NULL;

    if (SUCCEEDED(hr))
    {
        hr = MFPCreateMediaPlayer(
            NULL,       // URL.
            FALSE,      // Do not start playback yet.
            0,          // Option flags.
            NULL,       // Callback interface.
            hwnd,
            &g_pPlayer
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromObject(
            g_pSource,
            TRUE,       // Blocking call.
            0,          // User data.
            &pItem
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->Play();
    }

    SafeRelease(&pItem);
```



<span data-ttu-id="784d4-125">In una tipica applicazione, si fornirebbe un puntatore a un'interfaccia di callback nella funzione [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) e si userà l'interfaccia di callback per ottenere gli eventi dal lettore.</span><span class="sxs-lookup"><span data-stu-id="784d4-125">In a typical application, you would provide a pointer to a callback interface in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function, and use the callback interface to get events from the player.</span></span> <span data-ttu-id="784d4-126">Per semplicità, il codice illustrato di seguito Ignora questa procedura.</span><span class="sxs-lookup"><span data-stu-id="784d4-126">For simplicity, the code shown here skips these steps.</span></span> <span data-ttu-id="784d4-127">Per ulteriori informazioni, vedere [Introduzione con MFPlay](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="784d4-127">For more information, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

### <a name="shutting-down"></a><span data-ttu-id="784d4-128">Chiusura in corso</span><span class="sxs-lookup"><span data-stu-id="784d4-128">Shutting Down</span></span>

<span data-ttu-id="784d4-129">Prima di uscire dall'applicazione, arrestare l'origine del supporto e l'oggetto Player come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="784d4-129">Before the application exits, shut down the media source and the player object as follows:</span></span>

1.  <span data-ttu-id="784d4-130">Chiamare [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sull'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="784d4-130">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>
2.  <span data-ttu-id="784d4-131">Chiamare [**IMFPMediaPlayer:: Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) sull'oggetto Player.</span><span class="sxs-lookup"><span data-stu-id="784d4-131">Call [**IMFPMediaPlayer::Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) on the player object.</span></span>


```C++
    if (g_pSource)
    {
        g_pSource->Shutdown();
        g_pSource->Release();
        g_pSource = NULL;
    }

    if (g_pPlayer)
    {
        g_pPlayer->Shutdown();
        g_pPlayer->Release();
        g_pPlayer = NULL;
    }
```



## <a name="requirements"></a><span data-ttu-id="784d4-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="784d4-132">Requirements</span></span>

<span data-ttu-id="784d4-133">MFPlay richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="784d4-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="784d4-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="784d4-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="784d4-135">MFPlay</span><span class="sxs-lookup"><span data-stu-id="784d4-135">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="784d4-136">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="784d4-136">Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 



