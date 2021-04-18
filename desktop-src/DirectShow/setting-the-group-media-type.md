---
description: Impostazione del tipo di supporto di gruppo
ms.assetid: 05f0fdcb-74a4-441e-ac3c-d3d2c1dfee80
title: Impostazione del tipo di supporto di gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365bd2171100a9d4bcfc48d70dbeb94d8a6639dd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320652"
---
# <a name="setting-the-group-media-type"></a><span data-ttu-id="77c0c-103">Impostazione del tipo di supporto di gruppo</span><span class="sxs-lookup"><span data-stu-id="77c0c-103">Setting the Group Media Type</span></span>

<span data-ttu-id="77c0c-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="77c0c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="77c0c-105">Tutti i gruppi devono definire un tipo di supporto non compresso, ovvero audio o video.</span><span class="sxs-lookup"><span data-stu-id="77c0c-105">All groups must define an uncompressed media type, either audio or video.</span></span> <span data-ttu-id="77c0c-106">Il tipo di supporto non compresso è il formato che i visualizzatori visualizzano o sentono durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="77c0c-106">The uncompressed media type is the format that viewers see or hear during playback.</span></span> <span data-ttu-id="77c0c-107">In genere, l'output finale sarà in formato compresso.</span><span class="sxs-lookup"><span data-stu-id="77c0c-107">Typically, the final output will be in a compressed format.</span></span> <span data-ttu-id="77c0c-108">Per ulteriori informazioni, vedere [rendering di un progetto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="77c0c-108">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="77c0c-109">Per impostare il formato non compresso, creare una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) e riempirla con il tipo principale, il sottotipo e l'intestazione di formato appropriati.</span><span class="sxs-lookup"><span data-stu-id="77c0c-109">To set the uncompressed format, create an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and fill it with the appropriate major type, subtype, and format header.</span></span> <span data-ttu-id="77c0c-110">Per video, allocare una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) per il blocco di formato e impostare la larghezza, l'altezza e la profondità del bit.</span><span class="sxs-lookup"><span data-stu-id="77c0c-110">For video, allocate a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure for the format block, and set the width, height, and bit depth.</span></span> <span data-ttu-id="77c0c-111">Per audio, allocare una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) per il blocco di formato e impostare la frequenza di campionamento, la profondità dei bit e il numero di canali.</span><span class="sxs-lookup"><span data-stu-id="77c0c-111">For audio, allocate a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure for the format block, and set the sample rate, bit depth, and number of channels.</span></span> <span data-ttu-id="77c0c-112">Se si imposta solo il tipo principale, DES fornisce impostazioni predefinite ragionevoli per gli altri valori.</span><span class="sxs-lookup"><span data-stu-id="77c0c-112">If you set just the major type, DES provides reasonable defaults for the other values.</span></span> <span data-ttu-id="77c0c-113">In pratica, è necessario impostare i valori in modo esplicito per controllare l'output.</span><span class="sxs-lookup"><span data-stu-id="77c0c-113">In practice, you should set the values explicitly to control the output.</span></span>

<span data-ttu-id="77c0c-114">Dopo aver inizializzato la struttura del tipo di supporto, chiamare il metodo [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) per impostare il tipo di supporto per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="77c0c-114">After you initialize the media type structure, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method to set the media type for the group.</span></span>

<span data-ttu-id="77c0c-115">Nell'esempio seguente vengono specificati i video RGB a 16 bit, 320 pixel in larghezza per 240 pixel di altezza:</span><span class="sxs-lookup"><span data-stu-id="77c0c-115">The following example specifies 16-bit RGB video, 320 pixels wide by 240 pixels high:</span></span>


```C++
AM_MEDIA_TYPE mtGroup;  
mtGroup.majortype = MEDIATYPE_Video;
mtGroup.subtype = MEDIASUBTYPE_RGB555;

// Set format headers.
mtGroup.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(VIDEOINFOHEADER));
if (mtGroup.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}

VIDEOINFOHEADER *pVideoHeader = (VIDEOINFOHEADER*)mtGroup.pbFormat;
ZeroMemory(pVideoHeader, sizeof(VIDEOINFOHEADER));
pVideoHeader->bmiHeader.biBitCount = 16;
pVideoHeader->bmiHeader.biWidth = 320;
pVideoHeader->bmiHeader.biHeight = 240;
pVideoHeader->bmiHeader.biPlanes = 1;
pVideoHeader->bmiHeader.biSize = sizeof(BITMAPINFOHEADER);
pVideoHeader->bmiHeader.biSizeImage = DIBSIZE(pVideoHeader->bmiHeader);

// Set the format type and size.
mtGroup.formattype = FORMAT_VideoInfo;
mtGroup.cbFormat = sizeof(VIDEOINFOHEADER);

// Set the sample size.
mtGroup.bFixedSizeSamples = TRUE;
mtGroup.lSampleSize = DIBSIZE(pVideoHeader->bmiHeader);

// Now use this media type for the group.
pGroup->SetMediaType(&mtGroup);

// Clean up.
CoTaskMemFree(mtGroup.pbFormat);
```



<span data-ttu-id="77c0c-116">Nell'esempio seguente viene specificato un gruppo audio, impostando il tipo di supporto di gruppo su stereo a 16 bit, 44100 campioni al secondo:</span><span class="sxs-lookup"><span data-stu-id="77c0c-116">The next example specifies an audio group, by setting the group media type to 16-bit stereo, 44100 samples per second:</span></span>


```C++
AM_MEDIA_TYPE mt;  
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));

mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.formattype = FORMAT_WaveFormatEx;

// Set format block.
mt.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(WAVEFORMATEX));
if (mt.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}
mt.cbFormat = sizeof(WAVEFORMATEX);

// Fill in the WAVEFORMATEX structure.
WAVEFORMATEX *wave = (WAVEFORMATEX*) mt.pbFormat;
wave->wFormatTag = WAVE_FORMAT_PCM;
wave->nChannels = 2;  // Stereo
wave->nSamplesPerSec = 44100;
wave->wBitsPerSample = 16;
wave->nBlockAlign = wave->nChannels * wave->wBitsPerSample/8;
wave->nAvgBytesPerSec = wave->nSamplesPerSec * wave->nBlockAlign; 
wave->cbSize = 0;

hr = pGroup->SetMediaType(&mt);
CoTaskMemFree(mt.pbFormat);
```



<span data-ttu-id="77c0c-117">È anche possibile usare la classe [**CMediaType**](cmediatype.md) nelle [classi base di DirectShow](directshow-base-classes.md) per gestire i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="77c0c-117">You can also use the [**CMediaType**](cmediatype.md) class in the [DirectShow Base Classes](directshow-base-classes.md) to manage media types.</span></span> <span data-ttu-id="77c0c-118">Contiene alcuni metodi helper utili e rilascia automaticamente il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="77c0c-118">It contains some useful helper methods, and automatically releases the format block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77c0c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77c0c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77c0c-120">Informazioni sui tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="77c0c-120">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="77c0c-121">Creazione di una sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="77c0c-121">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
