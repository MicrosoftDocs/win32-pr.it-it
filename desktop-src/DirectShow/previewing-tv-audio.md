---
description: Anteprima dell'audio TV
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Anteprima dell'audio TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6b67e33ffd6f051363e8851afbc31b9f38bed17790687db615b679f6a80a63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748316"
---
# <a name="previewing-tv-audio"></a>Anteprima dell'audio TV

Per visualizzare l'anteprima dell'audio TV, instradare il pin del decodificatore audio sul filtro barra incrociata al pin del siner audio. Per disattivare l'audio, instradare il pin del decodificatore audio a -1, come illustrato nel diagramma seguente. I filtri barra incrociata sono descritti in [Uso delle barre incrociate.](working-with-crossbars.md)

![routing del pin del decodificatore audio](images/vidcap07.png)

L'approccio di base è il seguente:

1.  Usare il [**metodo ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) per individuare il filtro della barra incrociata.
2.  Usare il [**metodo IAMCrossbar::get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) per enumerare i pin di input e output del filtro barra incrociata. Cercare un pin di output del decodificatore audio e un pin di input del siner audio.
3.  Se si trovano i pin corretti, chiamare [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) per instradare i pin. In caso contrario, cercare a monte un'altra barra incrociata e ripetere il processo.
4.  Per disattivare l'audio, instradare il pin del decodificatore audio a -1.

La maggior parte dei sintonizzatori TV usa un singolo filtro barra incrociata, ma alcuni usano due filtri barra incrociata. Pertanto, potrebbe essere necessario cercare una seconda barra incrociata se la prima non riesce.

> [!Note]  
> Diversamente da quanto ci si potrebbe aspettare, non è necessario alcun filtro di acquisizione audio o renderer audio per visualizzare in anteprima l'audio, perché esiste una connessione fisica tra la scheda siner e la scheda audio.

 

Il codice seguente illustra questi passaggi in modo più dettagliato. Prima di tutto, ecco una funzione helper che cerca un filtro barra incrociata per un tipo di pin specificato:


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



La funzione successiva tenta di attivare o disattivare l'audio, a seconda del valore del *parametro bActivate.* Cerca i segnaposti necessari nel filtro della barra incrociata specificato. Se non riesce a trovarli, restituisce un codice di errore.


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



La funzione successiva cerca un filtro barra incrociata nel grafico dei filtri. Se ne trova uno, tenta di attivare o disattivare l'audio (usando la funzione precedente). Se l'operazione non riesce, il metodo cerca a monte una seconda barra incrociata e riprova. Per un approccio più generalizzato alla gestione di più filtri barra incrociata in un grafico, vedere la classe CCrossbar nell'applicazione di esempio AmCap.


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



Il codice seguente illustra come chiamare queste funzioni:


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



Si noti che queste funzioni di esempio ripetono molte delle stesse chiamate di funzione. Ad esempio, enumerano i segnaposto della barra incrociata ogni volta. In un'applicazione reale è possibile memorizzare nella cache alcune di queste informazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Audio televisivo analogico](analog-television-audio.md)
</dt> <dt>

[Uso delle barre incrociate](working-with-crossbars.md)
</dt> </dl>

 

 



