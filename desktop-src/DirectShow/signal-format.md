---
description: Formato segnale
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Formato segnale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6983328729e0dc72d93c0e00a74e7e65a7f237
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876641"
---
# <a name="signal-format"></a>Formato segnale

Il formato del segnale di una videocamera DV può essere NTSC o PAL, standard o Long-Play.

**Driver MSDV**

Per ottenere il formato del segnale di input dal driver MSDV, chiamare il metodo [**IAMExtTransport:: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) e passare il flag del segnale di input di ed \_ \_ \_ . Il metodo restituisce una costante definita, che indica il formato.

Il codice seguente controlla il formato del segnale e usa questo valore per calcolare il tempo medio per frame. La modalità variabile riceve la costante del formato del segnale.


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



Per ottenere il formato del segnale di output, chiamare lo stesso metodo con il flag del segnale di output di ED \_ \_ \_ .

**Driver UVC**

Per ottenere il formato del segnale di input o output dal driver UVC, chiamare [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) sul pin ed esaminare il blocco del formato video. Per i dispositivi UVC, il codice illustrato nell'esempio precedente restituisce in genere ED \_ \_Segnale transbasic \_ sconosciuto, quindi non è affidabile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di una videocamera DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



