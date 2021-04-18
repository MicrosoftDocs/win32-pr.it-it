---
description: Recupero del codice temporale dal dispositivo
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Recupero del codice temporale dal dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787cf328214c1a266b7f129e4e517716b1d04f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303764"
---
# <a name="getting-timecode-from-the-device"></a>Recupero del codice temporale dal dispositivo

Mentre un nastro DV viene riprodotto o è in modalità di sospensione dei record, è possibile recuperare il timecode SMPTE o il numero di traccia assoluto. A tale scopo, chiamare il metodo [**IAMTimecodeReader:: gettimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) . Questo metodo accetta un puntatore a una struttura di [**\_ esempio del timecode**](/windows/win32/api/strmif/ns-strmif-timecode_sample) , che descrive il timecode. Prima di chiamare il metodo, inizializzare il membro **dwFlags** della struttura. Usare il valore \_ DEVCAP \_ timecode \_ Read per recuperare il timecode oppure il valore ed \_ DEVCAP \_ ATN \_ Read per recuperare il numero di traccia assoluto.

Il membro **timecode** della struttura **di \_ esempio timecode** è una struttura del timecode. Quando il metodo restituisce un risultato, il membro **dwFrames** della struttura del timecode contiene il timecode o il numero di traccia. Per il timecode, le ore, i minuti, i secondi e i frame vengono compressi in un valore DWORD come valori decimali codificati binari (BCD), con il formato *hhmmssff*. Utilizzare le maschere di maschera per estrarre i singoli valori.

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

[Controllo di una videocamera DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
