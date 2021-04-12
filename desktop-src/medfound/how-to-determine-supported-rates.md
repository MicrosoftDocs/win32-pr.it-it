---
description: Come determinare le tariffe supportate
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Come determinare le tariffe supportate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226458"
---
# <a name="how-to-determine-supported-rates"></a>Come determinare le tariffe supportate

Prima di modificare la velocità di riproduzione, un'applicazione deve controllare se la velocità di riproduzione è supportata dagli oggetti nella pipeline. L'interfaccia [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) fornisce metodi per ottenere la frequenza massima di avanzamento e inversione, la velocità supportata più vicina a una frequenza richiesta e la velocità più lenta. Ognuna di queste query di frequenza può specificare la direzione di riproduzione e se utilizzare l'assottigliamento. Viene eseguita una query sulla frequenza di riproduzione esatta usando l'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .

Per informazioni sulla modifica delle frequenze di riproduzione, vedere [come impostare la velocità di riproduzione nella sessione multimediale](how-to-set-the-playback-rate-on-the-media-session.md).

Per informazioni generali sulle frequenze di riproduzione, vedere [informazioni sul controllo della frequenza](about-rate-control.md).

## <a name="to-determine-the-current-playback-rate"></a>Per determinare la frequenza di riproduzione corrente

1.  Ottenere il servizio di controllo della velocità dalla sessione multimediale.

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    Passare un puntatore all'interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inizializzato nel parametro *punkObject* di [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

    L'applicazione deve eseguire una query per il servizio di controllo della velocità tramite la sessione multimediale. Internamente, la sessione multimediale esegue una query sugli oggetti nella topologia.

2.  Chiamare il metodo [**IMFRateControl:: getrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) per ottenere la frequenza di riproduzione corrente.

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    Il parametro *pfThin* di [**getrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) riceve un valore **bool** che indica se il flusso è attualmente in fase di assottigliamento. L'applicazione deve passare **null** se non si desidera eseguire una query sul supporto di assottigliamento per il flusso. Il parametro *pflRate* riceve la velocità di riproduzione corrente.

## <a name="to-determine-the-nearest-supported-rate"></a>Per determinare la frequenza supportata più vicina

1.  Ottenere il servizio di supporto della frequenza dalla sessione multimediale.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Passare un puntatore all'interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inizializzato nel parametro *punkObject* di [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Chiamare il metodo [**IMFRateSupport:: IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) per recuperare la velocità supportata più vicina a una velocità di riproduzione richiesta.

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    Nell'esempio viene eseguita una query che indica se la frequenza di riproduzione 4,0 è supportata con il diluente. Questa operazione viene indicata passando **true** nel parametro *fThin* di [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported). Se questa frequenza è supportata, *actualRate* contiene la velocità di riproduzione di 4,0 e la chiamata ha esito positivo con un valore restituito di S \_ OK. Se la frequenza di riproduzione esatta non è supportata, in *actualRate* viene ricevuta la frequenza supportata più vicina. Se la frequenza non è supportata e non è disponibile una frequenza di riproduzione più vicina, la chiamata restituisce un codice di errore appropriato.

    Questi valori possono variare a seconda dei componenti della pipeline caricati. Pertanto, è necessario eseguire di nuovo la query sui valori ogni volta che si carica un nuovo topololgy.

    Se la frequenza di riproduzione desiderata non è supportata, un'opzione consiste nell'eseguire una query su ogni oggetto della topologia singolarmente, per verificare se un particolare componente non supporta la frequenza. Potrebbe essere possibile ricompilare la topologia senza questo componente, quindi riprodurla alla velocità desiderata. Se, ad esempio, ogni componente eccetto il renderer audio supporta una determinata frequenza, è possibile ricompilare la topologia senza il ramo audio e riprodurla alla velocità desiderata senza audio.

## <a name="to-determine-the-slowest-supported-rate"></a>Per determinare la velocità più lenta supportata

1.  Ottenere il servizio di supporto della frequenza dalla sessione multimediale.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Passare un puntatore all'interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inizializzato nel parametro *punkObject* di [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Chiamare il metodo [**IMFRateSupport:: GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) per recuperare la velocità supportata più lenta.

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    Nell'esempio viene eseguita una query per la frequenza di riproduzione inversa più lenta con assottigliamento. Il tasso di limite inferiore è stato ricevuto nel parametro *slowestRate* di [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).

    Se la riproduzione inversa o l'assottigliamento non è supportato, la chiamata restituisce un codice di errore appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Controllo della frequenza](rate-control.md)
</dt> <dt>

[Ricerca, avanzamento rapido e riproduzione inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



