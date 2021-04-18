---
description: Questo argomento descrive come riprodurre una sequenza di file audio/video usando MFPlay.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Come riprodurre una sequenza di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dc4d1523be4cc6cc09416096af260c9eae736c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310845"
---
# <a name="how-to-play-a-sequence-of-files"></a><span data-ttu-id="80d2a-103">Come riprodurre una sequenza di file</span><span class="sxs-lookup"><span data-stu-id="80d2a-103">How to Play a Sequence of Files</span></span>

<span data-ttu-id="80d2a-104">\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="80d2a-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="80d2a-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="80d2a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="80d2a-106">\]</span><span class="sxs-lookup"><span data-stu-id="80d2a-106">\]</span></span>

<span data-ttu-id="80d2a-107">Questo argomento descrive come riprodurre una sequenza di file audio/video usando MFPlay.</span><span class="sxs-lookup"><span data-stu-id="80d2a-107">This topic describes how to play a sequence of audio/video files using MFPlay.</span></span>


<span data-ttu-id="80d2a-108">Nell'argomento [Introduzione con MFPlay](getting-started-with-mfplay.md) viene illustrato come riprodurre un singolo file multimediale.</span><span class="sxs-lookup"><span data-stu-id="80d2a-108">The topic [Getting Started with MFPlay](getting-started-with-mfplay.md) shows how to play a single media file.</span></span> <span data-ttu-id="80d2a-109">È anche possibile usare MFPlay per riprodurre una sequenza di file.</span><span class="sxs-lookup"><span data-stu-id="80d2a-109">You can also use MFPlay to play a sequence of files.</span></span>

### <a name="synchronous-blocking-method"></a><span data-ttu-id="80d2a-110">Metodo sincrono (blocco)</span><span class="sxs-lookup"><span data-stu-id="80d2a-110">Synchronous (Blocking) Method</span></span>

1.  <span data-ttu-id="80d2a-111">Chiamare il metodo [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) .</span><span class="sxs-lookup"><span data-stu-id="80d2a-111">Call the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method.</span></span> <span data-ttu-id="80d2a-112">Il metodo crea un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="80d2a-112">The method creates a media item.</span></span>
2.  <span data-ttu-id="80d2a-113">Chiamare [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) per accodare l'elemento multimediale per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="80d2a-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to queue the media item for playback.</span></span>
3.  <span data-ttu-id="80d2a-114">Chiamare [**IMFPMediaPlayer::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) per avviare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="80d2a-114">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback.</span></span>

<span data-ttu-id="80d2a-115">Il codice riportato di seguito illustra i diversi passaggi.</span><span class="sxs-lookup"><span data-stu-id="80d2a-115">These steps are shown in the following code.</span></span>


```C++
HRESULT OpenMediaFile(IMFPMediaPlayer *pPlayer, PCWSTR pwszURL)
{
    HRESULT hr = S_OK;
    
    IMFPMediaItem *pItem = NULL;

    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        TRUE,  // Blocking call
        0,     // User data.
        &pItem
        );

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pPlayer->Play();
    }

    if (pItem)
    {
        pItem->Release();
    }
    return hr;
}
```



<span data-ttu-id="80d2a-116">Il metodo [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) accetta i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="80d2a-116">The [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method takes the following parameters:</span></span>

-   <span data-ttu-id="80d2a-117">Il primo parametro è l'URL del file.</span><span class="sxs-lookup"><span data-stu-id="80d2a-117">The first parameter is the URL of the file.</span></span>
-   <span data-ttu-id="80d2a-118">Il secondo parametro specifica se il metodo si blocca.</span><span class="sxs-lookup"><span data-stu-id="80d2a-118">The second parameter specifies whether the method blocks.</span></span> <span data-ttu-id="80d2a-119">Se si specifica il valore **true**, come mostrato di seguito, il metodo si blocca fino a quando non viene creato l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="80d2a-119">Specifying the value **TRUE**, as shown here, causes the method to block until the media item is created.</span></span>
-   <span data-ttu-id="80d2a-120">Il terzo parametro associa un valore **\_ ptr DWORD** arbitrario all'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="80d2a-120">The third parameter associates an arbitrary **DWORD\_PTR** value with the media item.</span></span> <span data-ttu-id="80d2a-121">È possibile ottenere questo valore in un secondo momento chiamando [**IMFPMediaItem:: GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).</span><span class="sxs-lookup"><span data-stu-id="80d2a-121">You can get this value later by calling [**IMFPMediaItem::GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).</span></span>
-   <span data-ttu-id="80d2a-122">Il quarto parametro riceve un puntatore all'interfaccia [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="80d2a-122">The fourth parameter receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface of the media item.</span></span>

### <a name="asynchronous-non-blocking-method"></a><span data-ttu-id="80d2a-123">Metodo asincrono (non di blocco)</span><span class="sxs-lookup"><span data-stu-id="80d2a-123">Asynchronous (Non-Blocking) Method</span></span>

<span data-ttu-id="80d2a-124">Evitare l'opzione di blocco se si chiama [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) dal thread dell'interfaccia utente, perché può richiedere una quantità di tempo considerevole per il completamento.</span><span class="sxs-lookup"><span data-stu-id="80d2a-124">Avoid the blocking option if you call [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) from your UI thread, because it can take a noticeable amount of time to complete.</span></span> <span data-ttu-id="80d2a-125">Il metodo in genere apre un file o una connessione di rete e legge dati sufficienti per analizzare le intestazioni dei file, che possono richiedere tempo.</span><span class="sxs-lookup"><span data-stu-id="80d2a-125">The method typically opens a file or network connection and reads enough data to parse the file headers, all of which can take time.</span></span> <span data-ttu-id="80d2a-126">Di conseguenza, è in genere preferibile impostare il secondo parametro su **false**.</span><span class="sxs-lookup"><span data-stu-id="80d2a-126">Therefore, it is generally better to set the second parameter to **FALSE**.</span></span> <span data-ttu-id="80d2a-127">Questa opzione fa sì che il metodo venga eseguito in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="80d2a-127">This option causes the method to perform asynchronously.</span></span> <span data-ttu-id="80d2a-128">Quando si usa l'opzione asincrona, l'ultimo parametro deve essere **null**:</span><span class="sxs-lookup"><span data-stu-id="80d2a-128">When the asynchronous option is used, the last parameter must be **NULL**:</span></span>


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



<span data-ttu-id="80d2a-129">Quando viene creato l'elemento multimediale, l'applicazione riceve un evento di **\_ tipo di evento MFP \_ \_ MEDIAITEM \_ creato** .</span><span class="sxs-lookup"><span data-stu-id="80d2a-129">When the media item is created, your application receives an **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="80d2a-130">La struttura dei dati per questo evento contiene un puntatore all'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="80d2a-130">The data structure for this event contains a pointer to the media item.</span></span> <span data-ttu-id="80d2a-131">Passare questo puntatore al metodo [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) per accodare l'elemento per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="80d2a-131">Pass this pointer to the [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method to queue the item for playback.</span></span>


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    HRESULT hr = S_OK;
    if (FAILED(pEvent->header.hrEvent))
    {
        // Handle error. (Not shown.)
    }
    else
    {
        hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
    }
}
```



## <a name="requirements"></a><span data-ttu-id="80d2a-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80d2a-132">Requirements</span></span>

<span data-ttu-id="80d2a-133">MFPlay richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="80d2a-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80d2a-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80d2a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80d2a-135">Uso di MFPlay per la riproduzione audio/video</span><span class="sxs-lookup"><span data-stu-id="80d2a-135">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



