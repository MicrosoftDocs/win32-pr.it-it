---
description: Come individuare la durata di un file multimediale.
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: Come individuare la durata di un file multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8915e52e97a4532b1d174166ec2863e26d18e34a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530504"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a><span data-ttu-id="c3ae0-103">Come individuare la durata di un file multimediale</span><span class="sxs-lookup"><span data-stu-id="c3ae0-103">How to Find the Duration of a Media File</span></span>

<span data-ttu-id="c3ae0-104">Per trovare la durata di un file multimediale, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="c3ae0-104">To find the duration of a media file, perform the following steps:</span></span>

1.  <span data-ttu-id="c3ae0-105">Usare il [resolver di origine](source-resolver.md) per creare un'origine multimediale in grado di analizzare il file multimediale.</span><span class="sxs-lookup"><span data-stu-id="c3ae0-105">Use the [Source Resolver](source-resolver.md) to create a media source that can parse the media file.</span></span>
2.  <span data-ttu-id="c3ae0-106">Chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sull'origine supporto.</span><span class="sxs-lookup"><span data-stu-id="c3ae0-106">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source.</span></span> <span data-ttu-id="c3ae0-107">Questo metodo restituisce il descrittore di presentazione che descrive il contenuto del file multimediale.</span><span class="sxs-lookup"><span data-stu-id="c3ae0-107">This method returns presentation descriptor that describes the contents of the media file.</span></span>
3.  <span data-ttu-id="c3ae0-108">Eseguire una query sul descrittore di presentazione per l'attributo della [ \_ \_ durata MF PD](mf-pd-duration-attribute.md) chiamando il metodo [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) .</span><span class="sxs-lookup"><span data-stu-id="c3ae0-108">Query the presentation descriptor for the [MF\_PD\_DURATION](mf-pd-duration-attribute.md) attribute by calling the [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) method.</span></span> <span data-ttu-id="c3ae0-109">Il valore dell'attributo, se presente, è la durata del file in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="c3ae0-109">The value of the attribute, if present, is the file duration in 100-nanosecond units.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c3ae0-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3ae0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3ae0-111">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="c3ae0-111">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



