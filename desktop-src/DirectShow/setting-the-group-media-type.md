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
# <a name="setting-the-group-media-type"></a>Impostazione del tipo di supporto di gruppo

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Tutti i gruppi devono definire un tipo di supporto non compresso, ovvero audio o video. Il tipo di supporto non compresso è il formato che i visualizzatori visualizzano o sentono durante la riproduzione. In genere, l'output finale sarà in formato compresso. Per ulteriori informazioni, vedere [rendering di un progetto](rendering-a-project.md).

Per impostare il formato non compresso, creare una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) e riempirla con il tipo principale, il sottotipo e l'intestazione di formato appropriati. Per video, allocare una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) per il blocco di formato e impostare la larghezza, l'altezza e la profondità del bit. Per audio, allocare una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) per il blocco di formato e impostare la frequenza di campionamento, la profondità dei bit e il numero di canali. Se si imposta solo il tipo principale, DES fornisce impostazioni predefinite ragionevoli per gli altri valori. In pratica, è necessario impostare i valori in modo esplicito per controllare l'output.

Dopo aver inizializzato la struttura del tipo di supporto, chiamare il metodo [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) per impostare il tipo di supporto per il gruppo.

Nell'esempio seguente vengono specificati i video RGB a 16 bit, 320 pixel in larghezza per 240 pixel di altezza:


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



Nell'esempio seguente viene specificato un gruppo audio, impostando il tipo di supporto di gruppo su stereo a 16 bit, 44100 campioni al secondo:


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



È anche possibile usare la classe [**CMediaType**](cmediatype.md) nelle [classi base di DirectShow](directshow-base-classes.md) per gestire i tipi di supporto. Contiene alcuni metodi helper utili e rilascia automaticamente il blocco di formato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui tipi di supporto](about-media-types.md)
</dt> <dt>

[Creazione di una sequenza temporale](constructing-a-timeline.md)
</dt> </dl>

 

 
