---
description: Recupero del codice temporale dal dispositivo
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Recupero del codice temporale dal dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265769300c0134ec9f3b3635ada3e595205e8452ced262d4062f9fb6cdaaadc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564731"
---
# <a name="getting-timecode-from-the-device"></a>Recupero del codice temporale dal dispositivo

Mentre un nastro DV è in riproduzione o è in modalità di sospensione record, è possibile recuperare il codice temporale SMPTE o il numero di traccia assoluto. A tale scopo, chiamare il [**metodo IAMTimecodeReader::GetTimecode.**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) Questo metodo accetta un puntatore a una [**struttura TIMECODE \_ SAMPLE,**](/windows/win32/api/strmif/ns-strmif-timecode_sample) che descrive il codice temporale. Prima di chiamare il metodo , inizializzare **il membro dwFlags** della struttura . Usare il valore ED DEVCAP TIMECODE READ per recuperare il codice temporale o il valore \_ \_ ED \_ \_ DEVCAP \_ ATN READ per recuperare il numero \_ di traccia assoluto.

Il **membro timecode** della struttura **TIMECODE \_ SAMPLE** è una struttura TIMECODE. Quando il metodo viene restituito, il **membro dwFrames** della struttura TIMECODE contiene il codice temporale o il numero di traccia. Per il codice temporale, le ore, i minuti, i secondi e i fotogrammi vengono imballati in un valore DWORD come valori BCD (Binary Coded Decimal), con il formato *hhmmssff*. Usare le maschera di bit per estrarre i singoli valori.

Nell'esempio seguente vengono recuperati il codice temporale e il numero di traccia.


```C++
if (MyDevCap.bHasTimecode)
{
    TIMECODE_SAMPLE TimecodeSample;
    TimecodeSample.timecode.dwFrames = 0;
    char szBuf[32];

    TimecodeSample.dwFlags = ED_DEVCAP_TIMECODE_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample),  SUCCEEDED(hr)) 
    {
        DWORD dwTime = TimecodeSample.timecode.dwFrames; // Packed BCD value.
        int hour  = ((dwTime & 0x0F000000) >> 24) + 
                    (10 * ((dwTime & 0xF0000000) >> 28));
        int min   = ((dwTime & 0x0F0000) >> 16) + 
                    (10 * ((dwTime & 0xF00000) >> 20));
        int sec   = ((dwTime & 0x0F00) >> 8) + 
                    (10 * ((dwTime & 0xF000) >> 12));
        int frame = (dwTime & 0x0F) + 
                    (10 * ((dwTime & 0xF0) >> 4));
    }

    TimecodeSample.dwFlags = ED_DEVCAP_ATN_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample), SUCCEEDED(hr)) 
    {
        DWORD dwTrackNumber = TimecodeSample.timecode.dwFrames;
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di un camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
