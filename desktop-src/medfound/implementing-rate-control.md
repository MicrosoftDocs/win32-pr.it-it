---
description: In questo argomento viene descritto in che modo gli oggetti pipeline personalizzati possono supportare frequenze di riproduzione variabili, inclusa la riproduzione inversa. Per informazioni sull'uso del controllo della velocità da un'applicazione, vedere controllo della frequenza.
ms.assetid: 077678db-ca5a-423b-9430-93497113d639
title: Implementazione del controllo della frequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5fd78cbbb95316a0d4ed12a50c9d3aa8954fe8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057918"
---
# <a name="implementing-rate-control"></a>Implementazione del controllo della frequenza

In questo argomento viene descritto in che modo gli oggetti pipeline personalizzati possono supportare frequenze di riproduzione variabili, inclusa la riproduzione inversa. Per informazioni sull'uso del controllo della velocità da un'applicazione, vedere [controllo della frequenza](rate-control.md).

In questo argomento sono incluse le sezioni seguenti:

-   [Origini supporti](#media-sources)
-   [Trasformazioni Media Foundation](#media-foundation-transforms)
    -   [Riproduzione inversa](#reverse-playback)
-   [Sink di supporti](#media-sinks)
-   [Argomenti correlati](#related-topics)

Se si scrive un oggetto Microsoft Media Foundation pipeline (un'origine multimediale, una trasformazione o un sink multimediale), potrebbe essere necessario supportare frequenze di riproduzione variabili. A tale scopo, implementare le interfacce seguenti:

1.  Implementare l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
2.  Supportare il servizio di **\_ \_ controllo \_ della velocità di MF** . Vedere [interfacce del servizio](service-interfaces.md).
3.  Implementare l'interfaccia [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , che ottiene le frequenze di riproduzione supportate dall'oggetto.
4.  Implementare l'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) , che ottiene o imposta la velocità di riproduzione.

## <a name="media-sources"></a>Origini supporti

Se un'origine supporto supporta il controllo della frequenza, deve implementare sia [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) che [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). In caso contrario, la sessione multimediale segnala che la frequenza di riproduzione minima e massima è 1,0, indipendentemente dagli altri componenti presenti nella pipeline.

La velocità di riproduzione non influisce sui tempi di presentazione degli esempi, quindi l'origine multimediale non deve modificare i timestamp. Al contrario, il clock di presentazione viene eseguito a una velocità più veloce o più lenta. Per la riproduzione inversa, l'origine recapita gli esempi in ordine inverso, con indicatori temporali decrescenti.

Il parametro *fThin* del metodo [**IMFRateControl::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) SetValue indica se l'origine del supporto deve *assottigliare* il contenuto. Il diluente si applica principalmente ai flussi video. In modalità assottigliata, l'origine Elimina i frame Delta e recapita solo i fotogrammi chiave. A frequenze di riproduzione molto elevate, l'origine potrebbe ignorare alcuni fotogrammi chiave, ad esempio recapitare tutti gli altri fotogrammi chiave.

Non è necessario che l'origine elimini gli esempi audio in modalità diluita. A frequenze di riproduzione molto elevate, tuttavia, l'origine potrebbe non essere in grado di leggere i dati nough rapidamente per completare le richieste di esempio della pipeline. In tal caso, l'origine potrebbe dover eliminare alcuni dati audio. In tal caso, è consigliabile provare a recapitare gli esempi audio che sono vicini agli esempi video (presupponendo che l'origine abbia entrambi i tipi di flusso).

Quando un flusso esegue una transizione tra la modalità assottigliata e quella non diluita, invia un evento [MEStreamThinMode](mestreamthinmode.md) .

Quando l'origine del supporto completa una chiamata a [**bitrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate), invia l'evento [MESourceRateChanged](mesourceratechanged.md) .

Durante la riproduzione inversa:

-   L'origine multimediale recapita gli esempi in ordine inverso, senza modificare i timestamp.
-   I timestamp all'interno di un flusso devono diminuire in maniera progressiva.
-   L'inizio del contenuto è considerato la fine del flusso. Quando ogni flusso multimediale recapita il primo campione nel flusso (ovvero il tempo di presentazione = 0), invia l'evento [MEEndOfStream](meendofstream.md) .

## <a name="media-foundation-transforms"></a>Trasformazioni Media Foundation

In generale, una trasformazione Media Foundation (MFT) non necessita di un supporto esplicito per il controllo della frequenza, a meno che il MFT non implementi la riproduzione inversa non diluita.

Se un MFT non implementa l'interfaccia [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , la sessione multimediale presuppone quanto segue:

-   Il MFT supporta la velocità di riproduzione arbitrario per la riproduzione in diretta, sia assottigliata che non assottigliata.
-   Il MFT supporta la riproduzione inversa assottigliata, ma non supporta la riproduzione inversa non diluita.

Se una di queste condizioni non è vera, il MFT deve implementare [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) e [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).

### <a name="reverse-playback"></a>Riproduzione inversa

La sessione multimediale può essere riprodotta in ordine inverso anche se una o più trasformazioni nella pipeline non supportano in modo esplicito la riproduzione inversa.

Se un MFT non espone l'interfaccia [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) , la sessione multimediale usa il *assottigliamento* per la riproduzione inversa, come indicato di seguito:

-   La sessione multimediale invia i fotogrammi chiave alla MFT nel modo consueto, chiamando [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

-   La sessione multimediale Elimina i frame Delta e li sostituisce con gli eventi [MEStreamTick](mestreamtick.md) .

-   Tra ogni esempio, la sessione multimediale Scarica la tabella MFT per evitare gli errori causati dal fatto che i timestamp diminuiscono.

Un esempio è considerato un fotogramma chiave se l'attributo [ \_ CleanPoint di MFSampleExtension](mfsampleextension-cleanpoint-attribute.md) è impostato su **true** e viene considerato un frame Delta se questo attributo è **false** o non è impostato.

Se MFT implementa [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport), la sessione multimediale usa questa interfaccia per individuare se la MFT supporta la riproduzione inversa non assottigliata. Se il file MFT supporta la riproduzione inversa non assottigliata, la sessione multimediale recapita tutti gli esempi, in ordine inverso, senza eliminare gli esempi o scaricare la MFT.

Se una MFT supporta la riproduzione inversa non assottigliata, deve implementare l'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) . La sessione multimediale utilizzerà questa interfaccia per inviare una notifica alla MFT quando si verifica la riproduzione inversa. A questo punto, è necessario preparare il MFT per la riduzione dei timestamp e per i frame Delta in ordine inverso. In genere, un decodificatore deve memorizzare nel buffer gli esempi fino a quando non riceve un intero Group of Pictures (GOP), quindi decodifica l'intero GOP e Visualizza i frame decodificati nell'ordine corretto (inverso).

## <a name="media-sinks"></a>Sink di supporti

Se un sink multimediale è *senza frequenza*, la sessione multimediale presuppone che il sink multimediale sia in grado di gestire qualsiasi frequenza di riproduzione. Il sink multimediale non deve implementare [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). Un sink multimediale senza frequenza restituisce MEDIASINK \_ Flag senza frequenza dal metodo [**IMFMediaSink:: getcaratteristiche**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) .

In caso contrario, un sink multimediale deve implementare [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) se può gestire frequenze di riproduzione diverse da 1,0.

I sink di supporto non devono implementare [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Quando la velocità di riproduzione viene modificata, il clock di presentazione chiama il metodo [**IMFClockStateSink:: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) del sink multimediale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo della frequenza](rate-control.md)
</dt> <dt>

[Ricerca, avanzamento rapido e riproduzione inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



