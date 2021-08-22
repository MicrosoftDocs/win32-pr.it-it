---
description: Acquisizione di audio tv
ms.assetid: c0c62a8e-ab16-4617-936c-b64e6e3865b4
title: Acquisizione di audio tv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d699533480bdeaaa528e362c0773e9df8100fda3dc2195a65c055ae7f7d5bb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641011"
---
# <a name="capturing-tv-audio"></a>Acquisizione di audio tv

Per acquisire audio dalla tv analogica a un file, usare il [filtro di acquisizione audio](audio-capture-filter.md). Usare Enumeratore dispositivo di sistema per creare il filtro di acquisizione audio. Nel sistema dell'utente possono essere presenti diversi dispositivi di acquisizione audio. l'utente deve selezionare il dispositivo che rappresenta la scheda audio.

Connessione pin di output di acquisizione audio al filtro mux:


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



I pin di input non devono essere connessi ad alcun elemento. Ogni pin di input rappresenta un input fisico nel dispositivo di acquisizione audio. Usare [**l'interfaccia IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) per abilitare l'input che riceve il flusso audio dal sintassi. I pin di input sono identificati dal nome, ad esempio "Line In" o "CD Audio". Sfortunatamente, i nomi possono cambiare da un dispositivo a quello successivo. Inoltre, diverse schede di siner TV usano input diversi per la scheda audio. È quindi l'utente a identificare l'input da usare.


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

[Audio analogico analogico](analog-television-audio.md)
</dt> <dt>

[Acquisizione audio](audio-capture.md)
</dt> </dl>

 

 



