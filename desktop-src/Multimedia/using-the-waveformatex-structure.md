---
title: Uso della struttura WAVEFORMATEX
description: Uso della struttura WAVEFORMATEX
ms.assetid: 9b668e1e-cb5f-4065-802b-23974925eacf
keywords:
- audio a forma d'onda, struttura WAVEFORMATEX
- audio ausiliario, struttura WAVEFORMATEX
- Struttura WAVEFORMATEX
- Dati audio PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3831d9760580f294573a4bc1bec3aef1d42cf345b2d714a897b22940a89a0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136055"
---
# <a name="using-the-waveformatex-structure"></a>Uso della struttura WAVEFORMATEX

Per i dati audio PCM su non più di due canali e con esempi a 8 o 16 bit, usare la struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) per specificare il formato dei dati.

L'esempio seguente illustra come configurare una struttura **WAVEFORMATEX** per 11,025 kilohertz (kHz) mono a 8 bit e per uno stereo a 16 bit a 44,1 kHz. Dopo aver impostato **WAVEFORMATEX,** l'esempio chiama la funzione IsFormatSupported per verificare che il dispositivo di output della forma d'onda PCM supporti il formato. Il codice sorgente per IsFormatSupported è illustrato in un esempio in [Determining Nonstandard Format Support](determining-nonstandard-format-support.md).


```C++
UINT wReturn; 
WAVEFORMATEX pcmWaveFormat; 
 
// Set up WAVEFORMATEX for 11 kHz 8-bit mono. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 1; 
pcmWaveFormat.nSamplesPerSec = 11025L; 
pcmWaveFormat.nAvgBytesPerSec = 11025L; 
pcmWaveFormat.nBlockAlign = 1; 
pcmWaveFormat.wBitsPerSample = 8; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono is supported.", 
       "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono NOT supported.", 
       "", MB_ICONINFORMATION); 
else 
     MessageBox(hMainWnd, "Error opening waveform device.", 
       "Error", MB_ICONEXCLAMATION); 
 
// Set up WAVEFORMATEX for 44.1 kHz 16-bit stereo. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 2; 
pcmWaveFormat.nSamplesPerSec = 44100L; 
pcmWaveFormat.nAvgBytesPerSec = 176400L; 
pcmWaveFormat.nBlockAlign = 4; 
pcmWaveFormat.wBitsPerSample = 16; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in the system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo is supported.", 
      "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo NOT supported.", 
      "", MB_ICONINFORMATION); 
else 
    MessageBox(hMainWnd, "Error opening waveform device.", 
      "Error", MB_ICONEXCLAMATION); 

```



 

 