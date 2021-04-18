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
# <a name="capturing-tv-audio"></a><span data-ttu-id="fa969-103">Acquisizione audio TV</span><span class="sxs-lookup"><span data-stu-id="fa969-103">Capturing TV Audio</span></span>

<span data-ttu-id="fa969-104">Per acquisire audio da televisione analoga a un file, usare il [Filtro acquisizione audio](audio-capture-filter.md).</span><span class="sxs-lookup"><span data-stu-id="fa969-104">To capture audio from analog television to a file, use the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="fa969-105">Usare l'enumeratore di dispositivo di sistema per creare il filtro di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="fa969-105">Use the System Device Enumerator to create the Audio Capture Filter.</span></span> <span data-ttu-id="fa969-106">Nel sistema dell'utente possono essere presenti diversi dispositivi di acquisizione audio; l'utente deve selezionare il dispositivo che rappresenta la scheda audio.</span><span class="sxs-lookup"><span data-stu-id="fa969-106">There may be several audio capture devices on the user's system; the user must select the device that represents the sound card.</span></span>

<span data-ttu-id="fa969-107">Connettere il pin di output di acquisizione audio al filtro Mux:</span><span class="sxs-lookup"><span data-stu-id="fa969-107">Connect the audio capture output pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



<span data-ttu-id="fa969-108">Non è necessario che i pin di input siano connessi ad alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="fa969-108">The input pins do not have to be connected to anything.</span></span> <span data-ttu-id="fa969-109">Ogni pin di input rappresenta un input fisico sul dispositivo di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="fa969-109">Each input pin represents a physical input on the audio capture device.</span></span> <span data-ttu-id="fa969-110">Usare l'interfaccia [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) per abilitare l'input che riceve il flusso audio dal sintonizzatore.</span><span class="sxs-lookup"><span data-stu-id="fa969-110">Use the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface to enable the input that receives the audio stream from the tuner.</span></span> <span data-ttu-id="fa969-111">I pin di input sono identificati in base al nome, ad esempio "line in" o "CD audio".</span><span class="sxs-lookup"><span data-stu-id="fa969-111">The input pins are identified by name, such as "Line In" or "CD Audio."</span></span> <span data-ttu-id="fa969-112">Sfortunatamente, i nomi possono cambiare da un dispositivo a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="fa969-112">Unfortunately, the names can change from one device to the next.</span></span> <span data-ttu-id="fa969-113">Inoltre, diverse schede del sintonizzatore TV utilizzano input diversi per la scheda audio.</span><span class="sxs-lookup"><span data-stu-id="fa969-113">Also, different TV tuner cards use different inputs to the sound card.</span></span> <span data-ttu-id="fa969-114">Pertanto, spetta all'utente identificare l'input da usare.</span><span class="sxs-lookup"><span data-stu-id="fa969-114">Therefore, it is up to the user to identify which input to use.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fa969-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa969-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa969-116">Audio TV analogico</span><span class="sxs-lookup"><span data-stu-id="fa969-116">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="fa969-117">Acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="fa969-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



