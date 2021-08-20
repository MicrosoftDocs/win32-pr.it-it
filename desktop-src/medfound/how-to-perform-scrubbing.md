---
description: Come eseguire lo scrubbing
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Come eseguire lo scrubbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab86ae39567132352592883b7441e4f325cb1b021b74e5b7a67f4a2755c3c947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063358"
---
# <a name="how-to-perform-scrubbing"></a>Come eseguire lo scrubbing

Lo scrubbing viene eseguito per cercare immediatamente punti specifici all'interno di un file interagendo con una rappresentazione visiva del tempo, ad esempio una barra di scorrimento. In Media Foundation, lo scrubbing indica la ricerca in un file e il recupero di un frame aggiornato.

Per informazioni sullo scrubbing, vedere [Informazioni sul controllo della frequenza.](about-rate-control.md)

## <a name="to-perform-scrubbing"></a>Per eseguire lo scrubbing

1.  Chiamare [**MFGetService per**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) ottenere [**l'interfaccia IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) dalla [sessione multimediale.](media-session.md)
    > [!Note]  
    > Non ottenere [**l'interfaccia IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) dall'origine multimediale. Ottenere sempre l'interfaccia dalla sessione multimediale.

     

2.  Chiamare [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) per impostare la velocità di riproduzione su zero. Per altre informazioni sulla chiamata a questo metodo, vedere [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).
3.  Creare una posizione di ricerca in **un oggetto PROPVARIANT** specificando l'ora di presentazione in cui eseguire la ricerca in un **tipo MFTIME.**
4.  Chiamare [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) con la posizione di ricerca per avviare la riproduzione.
5.  Al termine dell'operazione di puli pagina, la sessione multimediale invia un [evento MESessionScsampleSampleComplete.](mesessionscrubsamplecomplete.md) Attendere questo evento prima di chiamare [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) di nuovo per un'altra operazione di pulitura.

## <a name="example"></a>Esempio

Nell'esempio di codice seguente viene illustrato come eseguire lo scrubbing.


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



Un'operazione di pulitura riuscita genera l'evento [MESessionScsampleSampleComplete](mesessionscrubsamplecomplete.md) dopo che tutti i sink di flusso sono stati aggiornati con il nuovo frame e l'operazione di pulitura viene completata correttamente. Lo scrubbing di un file video visualizza il fotogramma cercato, ma non genera un output audio.

L'applicazione può eseguire l'esecuzione passo a passo dei fotogrammi impostando la velocità di riproduzione su zero e quindi passando un **PROPVARIANT** impostato su **VT \_ EMPTY** nella chiamata a [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Controllo della frequenza](rate-control.md)
</dt> </dl>

 

 



