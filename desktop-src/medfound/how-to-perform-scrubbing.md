---
description: Come eseguire lo scrubbing
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Come eseguire lo scrubbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dad1f06cb6abe6a570fd85407028450651e32a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527685"
---
# <a name="how-to-perform-scrubbing"></a>Come eseguire lo scrubbing

Viene eseguita la ripulitura per cercare istantaneamente punti specifici all'interno di un file interagendo con una rappresentazione visiva del tempo, ad esempio una barra di scorrimento. In Media Foundation, lo scrubbing significa cercare su un file e ottenere un frame aggiornato.

Per informazioni sullo scrubbing, vedere [informazioni sul controllo della frequenza](about-rate-control.md).

## <a name="to-perform-scrubbing"></a>Per eseguire lo scrubbing

1.  Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) dalla [sessione multimediale](media-session.md).
    > [!Note]  
    > Non ottenere l'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) dall'origine multimediale. Ottenere sempre l'interfaccia dalla sessione multimediale.

     

2.  Chiamare [**IMFRateControl:: serate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) per impostare la velocità di riproduzione su zero. Per ulteriori informazioni sulla chiamata a questo metodo, vedere [come impostare la velocità di riproduzione nella sessione multimediale](how-to-set-the-playback-rate-on-the-media-session.md).
3.  Creare una posizione di ricerca in un **PROPVARIANT** specificando il tempo di presentazione da cercare in un tipo **MFTIME** .
4.  Chiamare [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) con la posizione Seek per avviare la riproduzione.
5.  Quando l'operazione di scrub è completa, la sessione multimediale Invia un evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) . Attendere questo evento prima di chiamare di nuovo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) per un'altra operazione di pulitura.

## <a name="example"></a>Esempio

Nell'esempio di codice riportato di seguito viene illustrato come eseguire lo scrubbing.


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



Un'operazione di pulitura completata genera l'evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) dopo che tutti i sink di flusso vengono aggiornati con il nuovo frame e l'operazione di pulitura viene completata correttamente. Quando si pulisce un file video, viene visualizzato il frame cercato, ma non viene generato un output audio.

L'applicazione può eseguire lo stepping del frame impostando la velocità di riproduzione su zero e quindi passando un **PROPVARIANT** impostato su **VT \_ empty** nella chiamata a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Controllo della frequenza](rate-control.md)
</dt> </dl>

 

 



