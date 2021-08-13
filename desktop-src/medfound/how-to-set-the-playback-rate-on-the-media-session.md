---
description: Come impostare la velocità di riproduzione nella sessione multimediale
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Come impostare la velocità di riproduzione nella sessione multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696932d0da0147ba87e49cbc22d7ad53a525bc52c9bc2b3518c0f3e956a650aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465991"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a>Come impostare la velocità di riproduzione nella sessione multimediale

Per implementare funzionalità di riproduzione, ad esempio avanzamento rapido e riavvolgimento rapido, le applicazioni potrebbero dover modificare la velocità di riproduzione per un flusso multimediale. Media Foundation fornisce il servizio di controllo della frequenza che le applicazioni devono usare per impostare la velocità di riproduzione in modo dinamico.

Prima di impostare la velocità di riproduzione, un'applicazione deve verificare se la frequenza è supportata dall'origine multimediale. Per informazioni sull'esecuzione di query per le tariffe supportate, vedere [Come determinare le tariffe supportate.](how-to-determine-supported-rates.md)

Per informazioni sulle frequenze di riproduzione, vedere [About Rate Control](about-rate-control.md).

## <a name="to-set-the-playback-rate"></a>Per impostare la velocità di riproduzione

1.  Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'oggetto di controllo della frequenza dalla sessione multimediale.

    Le applicazioni che [**chiamano MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) devono garantire quanto segue:

    -   Il *parametro punkObject* contiene un puntatore a interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inizializzato.
    -   L'oggetto di controllo della frequenza ricevuto nel *parametro ppvObject* viene rilasciato per evitare perdite di memoria.

2.  Chiamare il [**metodo IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) per impostare la velocità di riproduzione. Dopo il completamento asincrono di **SetRate,** l'applicazione riceve [l'evento MESessionRateChanged.](mesessionratechanged.md)

## <a name="example"></a>Esempio

Il codice seguente illustra come impostare la velocità di riproduzione chiamando il [**metodo SetRate.**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate)


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



L'applicazione deve essere arrestata o sospesa prima di poter eseguire una transizione da un tasso negativo o zero a un tasso positivo. Per informazioni su questi stati, vedere [Come controllare gli stati di presentazione.](how-to-control-presentation-states.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Controllo della frequenza](rate-control.md)
</dt> <dt>

[Ricerca, avanzamento rapido e riproduzione inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



