---
description: Questo argomento descrive come usare gli effetti audio/video con MFPlay.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Come aggiungere effetti audio o video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d2b02453ce4561ead7fee0d272a07e694e8388
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310847"
---
# <a name="how-to-add-audio-or-video-effects"></a><span data-ttu-id="246c3-103">Come aggiungere effetti audio o video</span><span class="sxs-lookup"><span data-stu-id="246c3-103">How to Add Audio or Video Effects</span></span>

<span data-ttu-id="246c3-104">\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="246c3-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="246c3-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="246c3-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="246c3-106">\]</span><span class="sxs-lookup"><span data-stu-id="246c3-106">\]</span></span>

<span data-ttu-id="246c3-107">Questo argomento descrive come usare gli effetti audio/video con MFPlay.</span><span class="sxs-lookup"><span data-stu-id="246c3-107">This topic describes how to use audio/video effects with MFPlay.</span></span>

<span data-ttu-id="246c3-108">Per usare un effetto con MFPlay, è necessario implementare l'effetto come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="246c3-108">To use an effect with MFPlay, the effect must be implemented as a Media Foundation transform (MFT).</span></span> <span data-ttu-id="246c3-109">Per ulteriori informazioni, vedere [trasformazioni Media Foundation](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="246c3-109">For more information, see [Media Foundation Transforms](media-foundation-transforms.md).</span></span>

<span data-ttu-id="246c3-110">**Per aggiungere un effetto audio o video**</span><span class="sxs-lookup"><span data-stu-id="246c3-110">**To Add an Audio or Video Effect**</span></span>

1.  <span data-ttu-id="246c3-111">Creare un'istanza del MFT che implementi l'effetto.</span><span class="sxs-lookup"><span data-stu-id="246c3-111">Create an instance of the MFT that implements the effect.</span></span>
2.  <span data-ttu-id="246c3-112">Chiamare [**IMFPMediaPlayer:: InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).</span><span class="sxs-lookup"><span data-stu-id="246c3-112">Call [**IMFPMediaPlayer::InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).</span></span>

<span data-ttu-id="246c3-113">Chiamare [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) prima di aprire il file multimediale per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="246c3-113">Call [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) before you open the media file for playback.</span></span> <span data-ttu-id="246c3-114">MFPlay determina automaticamente se l'effetto è un effetto video o un effetto audio.</span><span class="sxs-lookup"><span data-stu-id="246c3-114">MFPlay automatically determines whether the effect is a video effect or audio effect.</span></span>

<span data-ttu-id="246c3-115">Il metodo [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) accetta anche un parametro booleano che specifica se l'effetto è facoltativo o obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="246c3-115">The [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) method also takes a Boolean parameter that specifies whether the effect is optional or required.</span></span> <span data-ttu-id="246c3-116">Se MFPlay non è in grado di aggiungere un effetto obbligatorio, ad esempio perché il formato del flusso è incompatibile, si verifica un errore di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="246c3-116">If MFPlay cannot add a required effect (for example, because the stream format is incompatible), a playback error occurs.</span></span> <span data-ttu-id="246c3-117">Nella maggior parte dei casi, è preferibile impostare un effetto come facoltativo.</span><span class="sxs-lookup"><span data-stu-id="246c3-117">In most cases, it is better to set an effect as optional.</span></span>

<span data-ttu-id="246c3-118">MFPlay continua a usare l'effetto per tutta la riproduzione successiva.</span><span class="sxs-lookup"><span data-stu-id="246c3-118">MFPlay continues to use the effect for all subsequent playback.</span></span> <span data-ttu-id="246c3-119">Per rimuovere l'effetto, chiamare [**IMFPMediaPlayer:: RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) o [**IMFPMediaPlayer:: RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).</span><span class="sxs-lookup"><span data-stu-id="246c3-119">To remove the effect, call [**IMFPMediaPlayer::RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) or [**IMFPMediaPlayer::RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).</span></span>


```C++
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="246c3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="246c3-120">Requirements</span></span>

<span data-ttu-id="246c3-121">MFPlay richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="246c3-121">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="246c3-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="246c3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="246c3-123">Uso di MFPlay per la riproduzione audio/video</span><span class="sxs-lookup"><span data-stu-id="246c3-123">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



