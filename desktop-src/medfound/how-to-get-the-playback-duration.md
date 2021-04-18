---
description: Questo argomento descrive come ottenere la durata di riproduzione di un file multimediale usando MFPlay.
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: Come ottenere la durata della riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21dd98a916109c8fb3d0ad3311643b1ffdc0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308764"
---
# <a name="how-to-get-the-playback-duration"></a><span data-ttu-id="85366-103">Come ottenere la durata della riproduzione</span><span class="sxs-lookup"><span data-stu-id="85366-103">How to Get the Playback Duration</span></span>

<span data-ttu-id="85366-104">\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="85366-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="85366-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="85366-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="85366-106">\]</span><span class="sxs-lookup"><span data-stu-id="85366-106">\]</span></span>

<span data-ttu-id="85366-107">Questo argomento descrive come ottenere la durata di riproduzione di un file multimediale usando MFPlay.</span><span class="sxs-lookup"><span data-stu-id="85366-107">This topic describes how to get the playback duration of a media file using MFPlay.</span></span>

<span data-ttu-id="85366-108">**Per ottenere la durata della riproduzione**</span><span class="sxs-lookup"><span data-stu-id="85366-108">**To Get the Playback Duration**</span></span>

1.  <span data-ttu-id="85366-109">Chiamare [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) o [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) per creare un elemento multimediale per il file.</span><span class="sxs-lookup"><span data-stu-id="85366-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="85366-110">Chiamare [**IMFPMediaItem:: GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration).</span><span class="sxs-lookup"><span data-stu-id="85366-110">Call [**IMFPMediaItem::GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration).</span></span> <span data-ttu-id="85366-111">Specificare **MFP \_ POSITIONTYPE \_ 100 ns** per il primo parametro.</span><span class="sxs-lookup"><span data-stu-id="85366-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter.</span></span> <span data-ttu-id="85366-112">La durata viene restituita come **PROPVARIANT** che contiene un **valore \_ Integer grande** .</span><span class="sxs-lookup"><span data-stu-id="85366-112">The duration is returned as a **PROPVARIANT** that contains a **LARGE\_INTEGER** value.</span></span> <span data-ttu-id="85366-113">La durata è indicata in unità da 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="85366-113">The duration is given in 100-nanosecond units.</span></span>

<span data-ttu-id="85366-114">Nell'esempio seguente viene illustrato il passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="85366-114">The following example shows step 2:</span></span>


```C++
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="85366-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85366-115">Requirements</span></span>

<span data-ttu-id="85366-116">MFPlay richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="85366-116">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85366-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85366-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85366-118">Uso di MFPlay per la riproduzione audio/video</span><span class="sxs-lookup"><span data-stu-id="85366-118">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



