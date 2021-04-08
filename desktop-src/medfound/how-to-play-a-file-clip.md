---
description: In questo argomento viene descritto come riprodurre un segmento di un file multimediale in MFPlay, impostando le ore di inizio e di fine per la riproduzione.
ms.assetid: cd761a4a-42ad-4994-b1b8-0946d29c3d8b
title: Come riprodurre una clip di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744db96c6dc384f2473f6c6d3361b24950a8881d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879934"
---
# <a name="how-to-play-a-file-clip"></a><span data-ttu-id="a54ea-103">Come riprodurre una clip di file</span><span class="sxs-lookup"><span data-stu-id="a54ea-103">How to Play a File Clip</span></span>

<span data-ttu-id="a54ea-104">\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a54ea-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a54ea-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="a54ea-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a54ea-106">\]</span><span class="sxs-lookup"><span data-stu-id="a54ea-106">\]</span></span>

<span data-ttu-id="a54ea-107">In questo argomento viene descritto come riprodurre un segmento di un file multimediale in MFPlay, impostando le ore di inizio e di fine per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a54ea-107">This topic describes how to play a segment of a media file in MFPlay, by setting the start and stop times for playback.</span></span>

<span data-ttu-id="a54ea-108">**Per riprodurre una clip di file**</span><span class="sxs-lookup"><span data-stu-id="a54ea-108">**To Play a File Clip**</span></span>

1.  <span data-ttu-id="a54ea-109">Chiamare [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) o [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) per creare un elemento multimediale per il file.</span><span class="sxs-lookup"><span data-stu-id="a54ea-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="a54ea-110">Facoltativamente, ottenere la durata totale del file, come descritto in [come ottenere la durata della riproduzione](how-to-get-the-playback-duration.md).</span><span class="sxs-lookup"><span data-stu-id="a54ea-110">Optionally, get the total duration of the file, as described in [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>
3.  <span data-ttu-id="a54ea-111">Chiamare [**IMFPMediaItem:: SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) per impostare l'ora di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="a54ea-111">Call [**IMFPMediaItem::SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) to set the start and stop times.</span></span> <span data-ttu-id="a54ea-112">L'ora di arresto non deve superare la durata del file.</span><span class="sxs-lookup"><span data-stu-id="a54ea-112">The stop time must not exceed the file duration.</span></span>
4.  <span data-ttu-id="a54ea-113">Chiamare [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) per avviare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a54ea-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to start playback.</span></span>

<span data-ttu-id="a54ea-114">Nell'esempio seguente viene utilizzata la versione di blocco di [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span><span class="sxs-lookup"><span data-stu-id="a54ea-114">The following example uses the blocking version of [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span> <span data-ttu-id="a54ea-115">Se viene usata la versione non bloccante, il codice visualizzato dopo **CreateMediaItemFromURL** deve essere inserito nel gestore per il tipo di **\_ evento MFP \_ \_ MEDIAITEM \_ creato** evento.</span><span class="sxs-lookup"><span data-stu-id="a54ea-115">If the non-blocking version is used, the code that appears after **CreateMediaItemFromURL** should be placed in the handler for the **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="a54ea-116">Per ulteriori informazioni sugli eventi in MFPlay, vedere [ricezione di eventi dal lettore](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="a54ea-116">For more information about events in MFPlay, see [Receiving Events From the Player](getting-started-with-mfplay.md).</span></span>

<span data-ttu-id="a54ea-117">Per ottenere la durata del file, in questo esempio viene chiamata la `GetPlaybackDuration` funzione illustrata nell'argomento [come ottenere la durata della riproduzione](how-to-get-the-playback-duration.md).</span><span class="sxs-lookup"><span data-stu-id="a54ea-117">To get the file duration, this example calls the `GetPlaybackDuration` function shown in the topic [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>


```C++
HRESULT PlayMediaClip(
    IMFPMediaPlayer *pPlayer,
    PCWSTR pszURL,
    LONGLONG    hnsStart,
    LONGLONG    hnsEnd
    )
{
    IMFPMediaItem *pItem = NULL;
    PROPVARIANT varStart, varEnd;

    ULONGLONG hnsDuration = 0;

    HRESULT hr = pPlayer->CreateMediaItemFromURL(pszURL, TRUE, 0, &pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetPlaybackDuration(pItem, &hnsDuration);
    if (FAILED(hr))
    {
        goto done;
    }

    if ((ULONGLONG)hnsEnd > hnsDuration)
    {
        hnsEnd = hnsDuration;
    }

    hr = InitPropVariantFromInt64(hnsStart, &varStart);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitPropVariantFromInt64(hnsEnd, &varEnd);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pItem->SetStartStopPosition(
        &MFP_POSITIONTYPE_100NS,
        &varStart,
        &MFP_POSITIONTYPE_100NS,
        &varEnd
        );
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPlayer->SetMediaItem(pItem);

done:
    SafeRelease(&pItem);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="a54ea-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a54ea-118">Requirements</span></span>

<span data-ttu-id="a54ea-119">MFPlay richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a54ea-119">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a54ea-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a54ea-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a54ea-121">Uso di MFPlay per la riproduzione audio/video</span><span class="sxs-lookup"><span data-stu-id="a54ea-121">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



