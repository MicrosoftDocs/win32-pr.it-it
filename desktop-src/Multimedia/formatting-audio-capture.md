---
title: Formattazione dell'acquisizione audio
description: Formattazione dell'acquisizione audio
ms.assetid: 3bbe34a6-8fd6-4780-b5af-fcf3d34ef701
keywords:
- Macro capSetAudioFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36acf1f98bcb6ea5d6786264406c28da78e909e3e57c5d796eac080139229f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496381"
---
# <a name="formatting-audio-capture"></a>Formattazione dell'acquisizione audio

L'esempio seguente usa [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) per impostare il formato audio su PCM a 8 bit a 11 kHz, stereo.


```C++
WAVEFORMATEX wfex;

wfex.wFormatTag = WAVE_FORMAT_PCM;
wfex.nChannels = 2;                // Use stereo
wfex.nSamplesPerSec = 11025;
wfex.nAvgBytesPerSec = 22050;
wfex.nBlockAlign = 2;
wfex.wBitsPerSample = 8;
wfex.cbSize = 0;

capSetAudioFormat(hWndC, &wfex, sizeof(WAVEFORMATEX)); 
 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




