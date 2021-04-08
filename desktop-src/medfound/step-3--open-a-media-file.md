---
description: Questo argomento è il passaggio 3 dell'esercitazione come riprodurre file multimediali con Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 'Passaggio 3: aprire un file multimediale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b50f036b84806f96e4349f77a3f06e02e08764
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104058454"
---
# <a name="step-3-open-a-media-file"></a><span data-ttu-id="2084d-103">Passaggio 3: aprire un file multimediale</span><span class="sxs-lookup"><span data-stu-id="2084d-103">Step 3: Open a Media File</span></span>

<span data-ttu-id="2084d-104">Questo argomento è il passaggio 3 dell'esercitazione [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="2084d-104">This topic is step 3 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="2084d-105">Il codice completo è illustrato nell'esempio relativo alla [riproduzione della sessione multimediale](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="2084d-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="2084d-106">Il `CPlayer::OpenURL` metodo apre un file multimediale da un URL.</span><span class="sxs-lookup"><span data-stu-id="2084d-106">The `CPlayer::OpenURL` method opens a media file from a URL.</span></span>


```C++
//  Open a URL for playback.
HRESULT CPlayer::OpenURL(const WCHAR *sURL)
{
    // 1. Create a new media session.
    // 2. Create the media source.
    // 3. Create the topology.
    // 4. Queue the topology [asynchronous]
    // 5. Start playback [asynchronous - does not happen in this method.]

    IMFTopology *pTopology = NULL;
    IMFPresentationDescriptor* pSourcePD = NULL;

    // Create the media session.
    HRESULT hr = CreateSession();
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the media source.
    hr = CreateMediaSource(sURL, &m_pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the presentation descriptor for the media source.
    hr = m_pSource->CreatePresentationDescriptor(&pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pSourcePD, m_hwndVideo, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

    // If SetTopology succeeds, the media session will queue an 
    // MESessionTopologySet event.

done:
    if (FAILED(hr))
    {
        m_state = Closed;
    }

    SafeRelease(&pSourcePD);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="2084d-107">Questo metodo esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2084d-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="2084d-108">Chiama **CPlayer:: CreateSession** per creare una nuova istanza della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="2084d-108">Calls **CPlayer::CreateSession** to create a new instance of the Media Session.</span></span> <span data-ttu-id="2084d-109">Vedere [passaggio 4: creare la sessione multimediale](step-4--create-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="2084d-109">See [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span>
2.  <span data-ttu-id="2084d-110">Crea un'origine multimediale dall'URL.</span><span class="sxs-lookup"><span data-stu-id="2084d-110">Creates a media source from the URL.</span></span> <span data-ttu-id="2084d-111">Il codice completo per questo passaggio è illustrato nell'argomento [utilizzo del](using-the-source-resolver.md)sistema di risoluzione di origine.</span><span class="sxs-lookup"><span data-stu-id="2084d-111">The complete code for this step is shown in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>
3.  <span data-ttu-id="2084d-112">Chiama [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) per ottenere il descrittore di presentazione dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="2084d-112">Calls [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span> <span data-ttu-id="2084d-113">Il descrittore della presentazione descrive tutti i flussi nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="2084d-113">The presentation descriptor describes each streams in the source file.</span></span>
4.  <span data-ttu-id="2084d-114">Crea la topologia di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="2084d-114">Creates the playback topology.</span></span> <span data-ttu-id="2084d-115">Il codice per questo passaggio è illustrato nell'argomento [creazione di topologie di riproduzione](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="2084d-115">Code for this step is shown in the topic [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="2084d-116">Chiama [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) per impostare la topologia nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="2084d-116">Calls [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>

<span data-ttu-id="2084d-117">Il metodo di [**topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="2084d-117">The [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="2084d-118">Al termine, viene chiamato il metodo [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) dell'oggetto CPlayer. vedere [passaggio 5: gestire gli eventi della sessione multimediale](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="2084d-118">When it completes, the CPlayer object's [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called; see [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>

<span data-ttu-id="2084d-119">[Passaggio 4: creare la sessione multimediale](step-4--create-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="2084d-119">Next: [Step 4: Create the Media Session](step-4--create-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="2084d-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2084d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2084d-121">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="2084d-121">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="2084d-122">Come riprodurre file multimediali con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2084d-122">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



