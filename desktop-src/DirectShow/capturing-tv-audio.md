---
description: Acquisizione audio TV
ms.assetid: c0c62a8e-ab16-4617-936c-b64e6e3865b4
title: Acquisizione audio TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138ce631aedf12ddfb52be92d08ffb47da0cbdec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304162"
---
# <a name="capturing-tv-audio"></a>Acquisizione audio TV

Per acquisire audio da televisione analoga a un file, usare il [Filtro acquisizione audio](audio-capture-filter.md). Usare l'enumeratore di dispositivo di sistema per creare il filtro di acquisizione audio. Nel sistema dell'utente possono essere presenti diversi dispositivi di acquisizione audio; l'utente deve selezionare il dispositivo che rappresenta la scheda audio.

Connettere il pin di output di acquisizione audio al filtro Mux:


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



Non è necessario che i pin di input siano connessi ad alcun elemento. Ogni pin di input rappresenta un input fisico sul dispositivo di acquisizione audio. Usare l'interfaccia [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) per abilitare l'input che riceve il flusso audio dal sintonizzatore. I pin di input sono identificati in base al nome, ad esempio "line in" o "CD audio". Sfortunatamente, i nomi possono cambiare da un dispositivo a quello successivo. Inoltre, diverse schede del sintonizzatore TV utilizzano input diversi per la scheda audio. Pertanto, spetta all'utente identificare l'input da usare.


```C++
IEnumPins *pEnum = NULL;
hr = pAudioCap->EnumPins(&pEnum);
if (SUCCEEDED(hr))
{
    IPin *pPin = NULL;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        IAMAudioInputMixer *pMix;
        hr = pPin->QueryInterface(IID_IAMAudioInputMixer, (void**)&pMix);
        if (SUCCEEDED(hr))
        {
            // Use IPin::QueryPinInfo to get the pin name.
            pPin->Release();
            if (...) // If the user selects this pin:
            {
                pMix->put_Enable(TRUE);
                pMix->put_MixLevel(1.0);
                pMix->Release();
                break;
            }
            pMix->Release();
        }
    }
}
pEnum->Release();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Audio TV analogico](analog-television-audio.md)
</dt> <dt>

[Acquisizione audio](audio-capture.md)
</dt> </dl>

 

 



