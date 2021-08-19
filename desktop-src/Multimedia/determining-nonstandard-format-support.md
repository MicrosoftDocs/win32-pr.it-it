---
title: Determinazione del supporto del formato non standard
description: Determinazione del supporto del formato non standard
ms.assetid: a795aa7d-704b-4f03-9815-7a298907bd3d
keywords:
- audio waveform, supporto del formato non standard
- audio ausiliario, supporto del formato non standard
- audio waveform, supporto del formato standard
- audio ausiliario, supporto del formato standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a90d38f7419b6fbdb3de951c0aa2205ccd3dd9ff5366eb1e69eab945220db1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497281"
---
# <a name="determining-nonstandard-format-support"></a>Determinazione del supporto del formato non standard

Per verificare se un dispositivo supporta un formato specifico (standard o non standard), è possibile chiamare la funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) con il flag WAVE \_ FORMAT \_ QUERY. Nell'esempio seguente viene utilizzata questa tecnica per determinare se un dispositivo waveform-audio supporta un formato specificato.


```C++
// Determines whether the specified waveform-audio output device 
// supports a specified waveform-audio format. Returns 
// MMSYSERR_NOERROR if the format is supported, WAVEERR_BADFORMAT if 
// the format is not supported, and one of the other MMSYSERR_ error 
// codes if there are other errors encountered in opening the 
// specified waveform-audio device. 
 
MMRESULT IsFormatSupported(LPWAVEFORMATEX pwfx, UINT uDeviceID) 
{ 
    return (waveOutOpen( 
        NULL,                 // ptr can be NULL for query 
        uDeviceID,            // the device identifier 
        pwfx,                 // defines requested format 
        NULL,                 // no callback 
        NULL,                 // no instance data 
        WAVE_FORMAT_QUERY));  // query only, do not open device 
} 
```



Questa tecnica per determinare il supporto del formato non standard si applica anche ai dispositivi di input waveform-audio. L'unica differenza è che la [**funzione waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) viene usata al posto di [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) per eseguire query per il supporto del formato.

Per determinare se un particolare formato dati waveform-audio è supportato da uno dei dispositivi waveform-audio in un sistema, usare la tecnica illustrata nell'esempio precedente, ma specificare la costante WAVE MAPPER per il \_ *parametro uDeviceID.*

 

 