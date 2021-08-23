---
description: Formato segnale
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Formato segnale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66add7467f2f497985094c603aaea83b55967f6b2c07eba4cacde080503ef2e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583181"
---
# <a name="signal-format"></a>Formato segnale

Il formato di segnale di un videocamere DV può essere NTSC o PAL, standard o long play.

**MSDV Driver**

Per ottenere il formato del segnale di input dal driver MSDV, chiamare il metodo [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) e passare il flag ED \_ TRANSBASIC \_ INPUT \_ SIGNAL. Il metodo restituisce una costante definita, che indica il formato.

Il codice seguente controlla il formato del segnale e usa questo valore per calcolare il tempo medio per fotogramma. La variabile Mode riceve la costante signal-format.


```C++
LONG Mode, AvgTimePerFrame;
hr = MyDevCap.pTransport->GetTransportBasicParameters(
        ED_TRANSBASIC_INPUT_SIGNAL, &Mode, NULL);
if (SUCCEEDED(hr))
{
    switch (Mode)
    {
    case ED_TRANSBASIC_SIGNAL_525_60_SD: // NTSC SD
        AvgTimePerFrame = 33;  // 33 msec (29.97 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_525_60_SDL: // NTSC SDL
        AvgTimePerFrame = 33;  
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SD: // PAL SD
        AvgTimePerFrame = 40;  // 40 msec (25 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SDL: // PAL SDL
        AvgTimePerFrame = 40;  
        break;
    default: 
        // Unknown type
        AvgTimePerFrame = 33; // Default
        break;
    }
}
```



Per ottenere il formato del segnale di output, chiamare lo stesso metodo con il flag ED \_ TRANSBASIC \_ OUTPUT \_ SIGNAL.

**UVC Driver**

Per ottenere il formato del segnale di input o output dal driver UVC, chiamare [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) sul pin ed esaminare il blocco di formato video. Per i dispositivi UVC, il codice illustrato nell'esempio precedente restituisce in genere ed \_ TRANSBASIC \_ SIGNAL \_ UNKNOWN, quindi non è affidabile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di un videocamere DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



