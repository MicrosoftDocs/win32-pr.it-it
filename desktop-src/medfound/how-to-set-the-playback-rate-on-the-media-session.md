---
description: Come impostare la velocità di riproduzione nella sessione multimediale
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Come impostare la velocità di riproduzione nella sessione multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761369"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a>Come impostare la velocità di riproduzione nella sessione multimediale

Per implementare la funzionalità di riproduzione, ad esempio l'avanzamento rapido e il rewind, è possibile che le applicazioni debbano modificare la velocità di riproduzione per un flusso multimediale. Media Foundation fornisce il servizio di controllo della velocità che le applicazioni devono utilizzare per impostare dinamicamente la velocità di riproduzione.

Prima di impostare la velocità di riproduzione, un'applicazione deve controllare se la frequenza è supportata dall'origine multimediale. Per informazioni sulle frequenze supportate, vedere [come determinare le tariffe supportate](how-to-determine-supported-rates.md).

Per informazioni sulle frequenze di riproduzione, vedere [informazioni sul controllo della frequenza](about-rate-control.md).

## <a name="to-set-the-playback-rate"></a>Per impostare la velocità di riproduzione

1.  Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'oggetto di controllo della velocità dalla sessione multimediale.

    Le applicazioni che chiamano [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) devono garantire quanto segue:

    -   Il parametro *punkObject* contiene un puntatore a interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inizializzato.
    -   L'oggetto frequenza di controllo ricevuto nel parametro *ppvObject* viene rilasciato per evitare perdite di memoria.

2.  Chiamare il metodo [**IMFRateControl::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) SetValue per impostare la velocità di riproduzione. Al termine dell'esecuzione della **velocità** in modo asincrono, l'applicazione riceve l'evento [MESessionRateChanged](mesessionratechanged.md) .

## <a name="example"></a>Esempio

Il codice seguente illustra come impostare la velocità di riproduzione chiamando il metodo [**serate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) .


```C++
///////////////////////////////////////////////////////////////////////
//  Name: SetPlaybackRate
//  Description: 
//      Gets the rate control service from Media Session.
//      Sets the playback rate to the specified rate.
//  Parameter:
//      pMediaSession: [in] Media session object to query.
//      rateRequested: [in] Playback rate to set.
//      bThin: [in] Indicates whether to use thinning.
///////////////////////////////////////////////////////////////////////

HRESULT SetPlaybackRate(
          IMFMediaSession *pMediaSession, 
          float rateRequested, 
          BOOL bThin)
{
    HRESULT hr = S_OK;
    IMFRateControl *pRateControl = NULL;

    // Get the rate control object from the Media Session.
    hr = MFGetService( 
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE, 
           IID_IMFRateControl, 
           (void**) &pRateControl ); 

    // Set the playback rate.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( bThin, rateRequested); 
    }

    // Clean up.
    SAFE_RELEASE(pRateControl );

    return hr;
}
```



L'applicazione deve essere arrestata o sospesa prima di poter eseguire una transizione da una velocità negativa o zero a una velocità positiva. Per informazioni su questi Stati, vedere [come controllare gli Stati di presentazione](how-to-control-presentation-states.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Controllo della frequenza](rate-control.md)
</dt> <dt>

[Ricerca, avanzamento rapido e riproduzione inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



