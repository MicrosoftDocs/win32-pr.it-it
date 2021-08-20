---
description: Come determinare le tariffe supportate
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Come determinare le tariffe supportate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aadbf0f9a0ce9608b58019d64ddb18a2227bbeb2941540086a6f998e40ebc3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878943"
---
# <a name="how-to-determine-supported-rates"></a>Come determinare le tariffe supportate

Prima di modificare la velocità di riproduzione, un'applicazione deve controllare se la velocità di riproduzione è supportata dagli oggetti nella pipeline. [**L'interfaccia IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) fornisce metodi per ottenere la velocità massima in avanti e inversa, la frequenza supportata più vicina a una frequenza richiesta e la velocità più lenta. Ognuna di queste query di frequenza può specificare la direzione di riproduzione e se usare il thinning. La velocità di riproduzione esatta viene eseguita tramite [**l'interfaccia IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)

Per informazioni sulla modifica delle frequenze di riproduzione, vedere [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).

Per informazioni generali sulle frequenze di riproduzione, vedere [Informazioni sul controllo della frequenza.](about-rate-control.md)

## <a name="to-determine-the-current-playback-rate"></a>Per determinare la frequenza di riproduzione corrente

1.  Ottenere il servizio di controllo della frequenza dalla sessione multimediale.

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    Passare un puntatore a [**interfaccia IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inizializzato nel *parametroobject di* [**MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)

    L'applicazione deve eseguire una query per il servizio di controllo della frequenza tramite la sessione multimediale. Internamente, la sessione multimediale esegue una query sugli oggetti nella topologia.

2.  Chiamare il [**metodo IMFRateControl::GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) per ottenere la frequenza di riproduzione corrente.

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    Il *parametro pfThin* di [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) riceve un valore **BOOL** che indica se il flusso è attualmente in fase di thinning. L'applicazione deve passare **NULL** se non desidera eseguire query sul supporto di thinning per il flusso. Il *parametro pflRate* riceve la frequenza di riproduzione corrente.

## <a name="to-determine-the-nearest-supported-rate"></a>Per determinare la tariffa supportata più vicina

1.  Ottenere il servizio di supporto tariffa dalla sessione multimediale.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Passare un puntatore a [**interfaccia IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inizializzato nel *parametroobject di* [**MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)

2.  Chiamare il [**metodo IMFRateSupport::IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) per recuperare la frequenza supportata più vicina a una velocità di riproduzione richiesta.

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    L'esempio esegue una query per determinare se una velocità di riproduzione di 4.0 è supportata con il thinning. Ciò è indicato passando **TRUE** nel *parametro fThin* di [**IsRateSupported.**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) Se questa frequenza è supportata, *actualRate* contiene la velocità di riproduzione di 4,0 e la chiamata ha esito positivo con un valore restituito S \_ OK. Se la velocità di riproduzione esatta non è supportata, viene ricevuta la frequenza supportata più vicina in *actualRate.* Se la frequenza non è supportata e non è disponibile alcuna velocità di riproduzione più vicina, la chiamata restituisce un codice di errore appropriato.

    Questi valori possono cambiare a seconda dei componenti della pipeline caricati. Pertanto, è necessario eseguire nuovamente una query dei valori ogni volta che si carica una nuova topololgy.

    Se la velocità di riproduzione desiderata non è supportata, è possibile eseguire una query su ogni oggetto della topologia singolarmente per verificare se un determinato componente non supporta la frequenza. Potrebbe essere possibile ricompilare la topologia senza questo componente e quindi riprodurre alla velocità desiderata. Ad esempio, se ogni componente ad eccezione del renderer audio supporta una determinata frequenza, è possibile ricompilare la topologia senza il ramo audio e riprodurre alla velocità desiderata senza audio.

## <a name="to-determine-the-slowest-supported-rate"></a>Per determinare la frequenza supportata più lenta

1.  Ottenere il servizio di supporto tariffa dalla sessione multimediale.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Passare un puntatore a [**interfaccia IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inizializzato nel *parametroobject di* [**MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)

2.  Chiamare il [**metodo IMFRateSupport::GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) per recuperare la frequenza supportata più lenta.

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    L'esempio esegue una query per la velocità di riproduzione inversa più lenta con thinning. La frequenza del limite inferiore viene ricevuta *nel parametro slowestRate* [**di GetSlowestRate.**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)

    Se la riproduzione inversa o il thinning non è supportato, la chiamata restituisce un codice di errore appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Controllo della frequenza](rate-control.md)
</dt> <dt>

[Ricerca, avanzamento rapido e riproduzione inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



