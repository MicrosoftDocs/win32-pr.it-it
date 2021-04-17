---
description: Anteprima dell'audio TV
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Anteprima dell'audio TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cc63583c946d47ed744eacd51f0939ec852d53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481484"
---
# <a name="previewing-tv-audio"></a><span data-ttu-id="4be0e-103">Anteprima dell'audio TV</span><span class="sxs-lookup"><span data-stu-id="4be0e-103">Previewing TV Audio</span></span>

<span data-ttu-id="4be0e-104">Per visualizzare l'anteprima audio della TV, instradare il pin del decodificatore audio sul filtro della barra traversa al pin del sintonizzatore audio.</span><span class="sxs-lookup"><span data-stu-id="4be0e-104">To preview TV audio, route the Audio Decoder pin on the crossbar filter to the Audio Tuner pin.</span></span> <span data-ttu-id="4be0e-105">Per disattivare l'audio, instradare il pin del decodificatore audio a-1, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="4be0e-105">To mute the audio, route the Audio Decoder pin to -1, as shown in the following diagram.</span></span> <span data-ttu-id="4be0e-106">(I filtri traversa sono descritti in [utilizzo delle barre](working-with-crossbars.md).)</span><span class="sxs-lookup"><span data-stu-id="4be0e-106">(Crossbar filters are described in [Working with Crossbars](working-with-crossbars.md).)</span></span>

![routing del pin del decodificatore audio](images/vidcap07.png)

<span data-ttu-id="4be0e-108">L'approccio di base è il seguente:</span><span class="sxs-lookup"><span data-stu-id="4be0e-108">The basic approach is as follows:</span></span>

1.  <span data-ttu-id="4be0e-109">Usare il metodo [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) per individuare il filtro traversa.</span><span class="sxs-lookup"><span data-stu-id="4be0e-109">Use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the crossbar filter.</span></span>
2.  <span data-ttu-id="4be0e-110">Usare il metodo [**IAMCrossbar:: Get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) per enumerare i pin di input e di output del filtro traversa.</span><span class="sxs-lookup"><span data-stu-id="4be0e-110">Use the [**IAMCrossbar::get\_CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) method to enumerate the crossbar filter's input and output pins.</span></span> <span data-ttu-id="4be0e-111">Cercare un pin di output del decodificatore audio e un pin di input del sintonizzatore audio.</span><span class="sxs-lookup"><span data-stu-id="4be0e-111">Search for an audio decoder output pin and an audio tuner input pin.</span></span>
3.  <span data-ttu-id="4be0e-112">Se si trovano i pin corretti, chiamare [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) per indirizzare i pin.</span><span class="sxs-lookup"><span data-stu-id="4be0e-112">If you find the correct pins, call [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) to route the pins.</span></span> <span data-ttu-id="4be0e-113">In caso contrario, controllare upstream per un'altra traversa e ripetere il processo.</span><span class="sxs-lookup"><span data-stu-id="4be0e-113">If not, look upstream for another crossbar and repeat the process.</span></span>
4.  <span data-ttu-id="4be0e-114">Per disattivare l'audio, indirizzare il pin del decodificatore audio a-1.</span><span class="sxs-lookup"><span data-stu-id="4be0e-114">To mute the audio, route the audio decoder pin to -1.</span></span>

<span data-ttu-id="4be0e-115">La maggior parte dei sintonizzatori TV usa un solo filtro traversa, ma alcuni usano due filtri traversa.</span><span class="sxs-lookup"><span data-stu-id="4be0e-115">Most TV tuners use a single crossbar filter, but some use two crossbar filters.</span></span> <span data-ttu-id="4be0e-116">Pertanto, potrebbe essere necessario cercare una seconda traversa se il primo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4be0e-116">Therefore, you might have to search for a second crossbar if the first one fails.</span></span>

> [!Note]  
> <span data-ttu-id="4be0e-117">Contrariamente a quanto ci si potrebbe aspettare, per visualizzare in anteprima l'audio non è necessario alcun filtro di acquisizione audio o renderer audio, perché esiste una connessione fisica tra la scheda Tuner e la scheda audio.</span><span class="sxs-lookup"><span data-stu-id="4be0e-117">Contrary to what you might expect, no audio capture filter or audio renderer is required to preview the audio, because there is a physical connection between the tuner card and the sound card.</span></span>

 

<span data-ttu-id="4be0e-118">Il codice seguente illustra questi passaggi in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="4be0e-118">The following code shows these steps in more detail.</span></span> <span data-ttu-id="4be0e-119">Per prima cosa, ecco una funzione helper che esegue la ricerca di un filtro barra di traversa per un tipo di PIN specificato:</span><span class="sxs-lookup"><span data-stu-id="4be0e-119">First, here is a helper function that searches a crossbar filter for a specified pin type:</span></span>


```C++
HRESULT FindCrossbarPin(
    IAMCrossbar *pXBar,                 // Pointer to the crossbar.
    PhysicalConnectorType PhysicalType, // Pin type to match.
    PIN_DIRECTION Dir,                  // Pin direction.
    long *pIndex)       // Receives the index of the pin, if found.
{
    BOOL bInput = (Dir == PINDIR_INPUT ? TRUE : FALSE);

    // Find out how many pins the crossbar has.
    long cOut, cIn;
    HRESULT hr = pXBar->get_PinCounts(&cOut, &cIn);
    if (FAILED(hr)) return hr;
    // Enumerate pins and look for a matching pin.
    long count = (bInput ? cIn : cOut);
    for (long i = 0; i < count; i++)
    {
        long iRelated = 0;
        long ThisPhysicalType = 0;
        hr = pXBar->get_CrossbarPinInfo(bInput, i, &iRelated,
            &ThisPhysicalType);
        if (SUCCEEDED(hr) && ThisPhysicalType == PhysicalType)
        {
            // Found a match, return the index.
            *pIndex = i;
            return S_OK;
        }
    }
    // Did not find a matching pin.
    return E_FAIL;
}
```



<span data-ttu-id="4be0e-120">La funzione successiva tenta di attivare o disattivare l'audio, a seconda del valore del parametro *bActivate* .</span><span class="sxs-lookup"><span data-stu-id="4be0e-120">The next function attempts to activate or mute the audio, depending on the value of the *bActivate* parameter.</span></span> <span data-ttu-id="4be0e-121">Esegue la ricerca dei pin richiesti nel filtro della barra di traversa specificato.</span><span class="sxs-lookup"><span data-stu-id="4be0e-121">It searches the specified crossbar filter for the required pins.</span></span> <span data-ttu-id="4be0e-122">Se non riesce a trovarle, restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="4be0e-122">If it cannot find them, it returns an error code.</span></span>


```C++
HRESULT ConnectAudio(IAMCrossbar *pXBar, BOOL bActivate)
{
    // Look for the Audio Decoder output pin.
    long i = 0;
    HRESULT hr = FindCrossbarPin(pXBar, PhysConn_Audio_AudioDecoder,
        PINDIR_OUTPUT, &i);
    if (SUCCEEDED(hr))
    {
        if (bActivate)  // Activate the audio. 
        {
            // Look for the Audio Tuner input pin.
            long j = 0;
            hr = FindCrossbarPin(pXBar, PhysConn_Audio_Tuner, 
                PINDIR_INPUT, &j);
            if (SUCCEEDED(hr))
            {
                return pXBar->Route(i, j);
            }
        }
        else  // Mute the audio
        {
            return pXBar->Route(i, -1);
        }
    }
    return E_FAIL;
}
```



<span data-ttu-id="4be0e-123">La funzione Next Cerca nel grafico del filtro un filtro traversa.</span><span class="sxs-lookup"><span data-stu-id="4be0e-123">The next function searches the filter graph for a crossbar filter.</span></span> <span data-ttu-id="4be0e-124">Se ne trova uno, tenta di attivare o disattivare l'audio (usando la funzione precedente).</span><span class="sxs-lookup"><span data-stu-id="4be0e-124">If it finds one, it attempts to activate or mute the audio (using the previous function).</span></span> <span data-ttu-id="4be0e-125">Se l'operazione ha esito negativo, il metodo esegue la ricerca a Monte per una seconda traversa e riprova.</span><span class="sxs-lookup"><span data-stu-id="4be0e-125">If that operation fails, the method searches upstream for a second crossbar and tries again.</span></span> <span data-ttu-id="4be0e-126">Per un approccio più generalizzato alla gestione di più filtri traversa in un grafico, vedere la classe CCrossbar nell'applicazione di esempio AmCap.</span><span class="sxs-lookup"><span data-stu-id="4be0e-126">For a more generalized approach to managing multiple crossbar filters in a graph, see the CCrossbar class in the AmCap sample application.</span></span>


```C++
HRESULT ActivateAudio(ICaptureGraphBuilder2 *pBuild, IBaseFilter *pSrc,
  BOOL bActivate)
{
    // Search upstream for a crossbar.
    IAMCrossbar *pXBar1 = NULL;
    HRESULT hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
    if (SUCCEEDED(hr)) 
    {
        hr = ConnectAudio(pXBar1, bActivate);
        if (FAILED(hr))
        {
            // Look for another crossbar.
            IBaseFilter *pF = NULL;
            hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pF);
            if (SUCCEEDED(hr)) 
            {
                // Search upstream for another one.
                IAMCrossbar *pXBar2 = NULL;
                hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pF,
                    IID_IAMCrossbar, (void**)&pXBar2);
                pF->Release();
                if (SUCCEEDED(hr))
                {
                    hr = ConnectAudio(pXBar2, bActivate);
                    pXBar2->Release();
                }
            }
        }
        pXBar1->Release();
    }
    return hr;
}
```



<span data-ttu-id="4be0e-127">Il codice seguente illustra come chiamare queste funzioni:</span><span class="sxs-lookup"><span data-stu-id="4be0e-127">The following code shows how to call these functions:</span></span>


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



<span data-ttu-id="4be0e-128">Si noti che queste funzioni di esempio ripetono molte delle stesse chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="4be0e-128">Note that these example functions repeat many of the same function calls.</span></span> <span data-ttu-id="4be0e-129">Ad esempio, enumerano i pin della traversa ogni volta.</span><span class="sxs-lookup"><span data-stu-id="4be0e-129">For example, they enumerate the crossbar pins each time.</span></span> <span data-ttu-id="4be0e-130">In un'applicazione reale, è possibile memorizzare nella cache alcune di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="4be0e-130">In a real application, you might cache some of this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4be0e-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4be0e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4be0e-132">Audio TV analogico</span><span class="sxs-lookup"><span data-stu-id="4be0e-132">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="4be0e-133">Uso di maniglie</span><span class="sxs-lookup"><span data-stu-id="4be0e-133">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



