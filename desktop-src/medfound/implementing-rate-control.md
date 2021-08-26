---
description: Questo argomento descrive in che modo gli oggetti pipeline personalizzati possono supportare frequenze di riproduzione variabili, inclusa la riproduzione inversa. Per informazioni sull'uso del controllo della frequenza da un'applicazione, vedere Controllo della frequenza.
ms.assetid: 077678db-ca5a-423b-9430-93497113d639
title: Implementazione del controllo della frequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3ff90e7b1748efd4cfcff41244164d1d6a997b6208d3e46afa0cdae9aa6bba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114271"
---
# <a name="implementing-rate-control"></a>Implementazione del controllo della frequenza

Questo argomento descrive in che modo gli oggetti pipeline personalizzati possono supportare frequenze di riproduzione variabili, inclusa la riproduzione inversa. Per informazioni sull'uso del controllo della frequenza da un'applicazione, vedere [Controllo della frequenza.](rate-control.md)

In questo argomento sono incluse le sezioni seguenti:

-   [Origini multimediali](#media-sources)
-   [Media Foundation trasformazioni](#media-foundation-transforms)
    -   [Riproduzione inversa](#reverse-playback)
-   [Sink multimediali](#media-sinks)
-   [Argomenti correlati](#related-topics)

Se si scrive un oggetto Microsoft Media Foundation pipeline (un'origine multimediale, una trasformazione o un sink multimediale), potrebbe essere necessario supportare frequenze di riproduzione variabili. A tale scopo, implementare le interfacce seguenti:

1.  Implementare [**l'interfaccia IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
2.  Supportare **il servizio MF RATE CONTROL \_ \_ \_ SERVICE.** Vedere [Interfacce di servizio.](service-interfaces.md)
3.  Implementare [**l'interfaccia IMFRateSupport,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) che ottiene le frequenze di riproduzione supportate dall'oggetto .
4.  Implementare [**l'interfaccia IMFRateControl,**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) che ottiene o imposta la velocità di riproduzione.

## <a name="media-sources"></a>Origini multimediali

Se un'origine multimediale supporta il controllo della frequenza, deve implementare sia [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) che [**IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) In caso contrario, la sessione multimediale segnala che la velocità di riproduzione minima e massima è 1,0, indipendentemente dagli altri componenti presenti nella pipeline.

La velocità di riproduzione non influisce sui tempi di presentazione dei campioni, quindi l'origine multimediale non deve modificare i timestamp. Al contrario, l'orologio di presentazione viene eseguito a una velocità più veloce o più lenta. Per la riproduzione inversa, l'origine fornisce i campioni in ordine inverso, con timestamp decrescenti.

Il *parametro fThin* del metodo [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) indica se l'origine multimediale deve *eseguire il thin* contenuto. Il thinning si applica principalmente ai flussi video. In modalità thin, l'origine elimina i fotogrammi differenziali e fornisce solo fotogrammi chiave. A velocità di riproduzione molto elevate, l'origine potrebbe ignorare alcuni fotogrammi chiave(ad esempio, distribuire tutti gli altri fotogrammi chiave).

L'origine non deve rilasciare campioni audio in modalità thinned. A velocità di riproduzione molto elevate, tuttavia, l'origine potrebbe non essere in grado di leggere i dati rapidamente per riempire le richieste di esempio della pipeline. In tal caso, l'origine potrebbe dover eliminare alcuni dati audio. In tal caso, deve tentare di distribuire campioni audio vicini nel tempo agli esempi video (presupponendo che l'origine abbia entrambi i tipi di flusso).

Quando un flusso passa dalla modalità thin alla modalità non thin, invia un [evento MEStreamThinMode.](mestreamthinmode.md)

Quando l'origine multimediale completa una chiamata a [**SetRate,**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)invia [l'evento MESourceRateChanged.](mesourceratechanged.md)

Durante la riproduzione inversa:

-   L'origine multimediale recapita i campioni in ordine inverso, senza modificare i timestamp.
-   I timestamp all'interno di un flusso devono diminuire in modo monotona.
-   L'inizio del contenuto è considerato la fine del flusso. Dopo che ogni flusso multimediale ha recapitato il primo esempio nel flusso ,ovvero l'ora di presentazione = 0, invia [l'evento MEEndOfStream.](meendofstream.md)

## <a name="media-foundation-transforms"></a>Media Foundation trasformazioni

In generale, una trasformazione Media Foundation (MFT) non richiede il supporto esplicito per il controllo della frequenza, a meno che il MFT non implementi la riproduzione inversa senza thinning.

Se un MFT non implementa [**l'interfaccia IMFRateSupport,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) la sessione multimediale presuppone quanto segue:

-   MFT supporta le frequenze di riproduzione arbitary per la riproduzione in avanti, sia thinned che non thinned.
-   MFT supporta la riproduzione inversa con thinning, ma non la riproduzione inversa senza thinning.

Se una di queste condizioni non è vera, il MFT deve implementare [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) [**e IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).

### <a name="reverse-playback"></a>Riproduzione inversa

La sessione multimediale può essere riprodotta in ordine inverso anche se una o più trasformazioni nella pipeline non supportano in modo esplicito la riproduzione inversa.

Se un MFT non espone [**l'interfaccia IMFRateSupport,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) la sessione multimediale usa il *thinning* per la riproduzione inversa, come indicato di seguito:

-   La sessione multimediale invia fotogrammi chiave al MFT nel modo consueto, chiamando [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

-   La sessione multimediale elimina i fotogrammi differenziali e li sostituisce [con eventi MEStreamTick.](mestreamtick.md)

-   Tra un campione e l'altro, la sessione multimediale scarica il file MFT per evitare eventuali errori causati dal fatto che i timestamp diminuiscono.

Un esempio viene considerato un fotogramma chiave se l'attributo [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) è impostato su **TRUE** e viene considerato un frame differenziale se questo attributo è **FALSE** o non è impostato.

Se MFT implementa [**IMFRateSupport,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)la sessione multimediale usa questa interfaccia per determinare se MFT supporta la riproduzione inversa non con thinning. Se MFT supporta la riproduzione inversa senza thinning, la sessione multimediale fornisce tutti i campioni, in ordine inverso, senza eliminare i campioni o scaricare il MFT.

Se un dispositivo MFT supporta la riproduzione inversa senza thinning, deve implementare [**l'interfaccia IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) La sessione multimediale userà questa interfaccia per inviare una notifica a MFT quando si verifica la riproduzione inversa. A questo punto, il MFT deve essere preparato per la diminuzione dei timestamp e per l'arrivo di fotogrammi differenziali in ordine inverso. Un decodificatore dovrà in genere bufferare i campioni fino a quando non riceve un intero gruppo di immagini (GOP), quindi decodificare l'intero GOP e visualizzare i fotogrammi decodificati nell'ordine corretto (inverso).

## <a name="media-sinks"></a>Sink multimediali

Se un sink multimediale è *senza frequenza,* la sessione multimediale presuppone che il sink multimediale sia in grado di gestire qualsiasi frequenza di riproduzione. Non è necessario che il sink multimediale [**implementi IMFRateSupport.**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) Un sink multimediale senza frequenza restituisce MEDIASINK \_ Flag RATELESS del [**metodo IMFMediaSink::GetCharacteristics.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)

In caso contrario, un sink multimediale deve [**implementare IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) se è in grado di gestire velocità di riproduzione diverse da 1.0.

I sink multimediali non devono implementare [**IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) Quando la velocità di riproduzione cambia, il clock di presentazione chiama il metodo [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) del sink multimediale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo della frequenza](rate-control.md)
</dt> <dt>

[Ricerca, avanzamento rapido e riproduzione inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



