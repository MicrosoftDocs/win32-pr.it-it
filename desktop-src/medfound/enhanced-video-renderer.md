---
description: Il renderer video avanzato (EVR) è un componente che Visualizza i video sul monitor utenti.
ms.assetid: 1c985558-d25d-4f51-978a-58c05943dab9
title: Renderer video migliorato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0881da0827e6cc757a0ea855bcb51864dd98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342491"
---
# <a name="enhanced-video-renderer"></a>Renderer video migliorato

Il renderer video avanzato (EVR) è un componente che Visualizza il video sul monitor dell'utente. Esistono due versioni di EVR:

-   Il sink multimediale EVR, per Media Foundation applicazioni.
-   Filtro EVR per le applicazioni DirectShow.

Entrambe le versioni utilizzano gli stessi oggetti interni per eseguire il rendering del video e condividono molte delle stesse interfacce.

EVR può combinare fino a 16 flussi video. Il primo flusso di input viene chiamato *flusso di riferimento*. Il flusso di riferimento viene sempre visualizzato per primo nell'ordine z. Tutti i flussi aggiuntivi sono denominati *sottoflussi* e sono combinati sopra il flusso di riferimento. L'applicazione può modificare l'ordine z dei sottoflussi, ma nessun sottoflusso può essere prima nell'ordine z.

Il driver di grafica determina quali formati video sono supportati, ma in genere sono limitati agli elementi seguenti:

-   Flusso di riferimento: YUV progressivo o interlacciato senza alfa per pixel, ad esempio NV12 o YUY2. o RGB progressivo.
-   Sottoflussi: YUV progressivo con l'alfa per pixel, ad esempio AYUV o AI44.

I formati dei sottoflussi disponibili possono dipendere dal formato del flusso di riferimento. Per altre informazioni, vedere [negoziazione del tipo di supporto EVR](evr-media-type-negotiation.md).

Internamente, EVR usa un oggetto denominato *mixer* per comporre i frame dai flussi di input su una superficie per il rendering. Il mixer esegue anche il deinterlacciamento e la correzione del colore. L'output del mixer è il fotogramma video composito finale. Un secondo oggetto denominato *Presenter* esegue il rendering del fotogramma video sullo schermo. Il presentatore pianifica quando viene eseguito il rendering dei frame e gestisce il dispositivo Direct3D. Un'applicazione può fornire un'implementazione personalizzata del mixer o del Presenter.

La frequenza dei fotogrammi di output è bloccata nel flusso di riferimento. Ogni volta che i sottoflussi ricevono nuovi frame, il mixer li utilizza. Quando il flusso di riferimento riceve un nuovo frame, il mixer compone il frame con i frame dei sottoflussi. Se il flusso di riferimento è interlacciato, un frame di riferimento completo potrebbe richiedere più di un campione multimediale. Un sottoflusso può ricevere più di un frame mentre il mixer è in attesa di un frame di riferimento. In tal caso, il mixer Elimina semplicemente il frame del sottoflusso precedente.

Poiché il Presenter crea il dispositivo Direct3D, è anche responsabile della condivisione del dispositivo con altri oggetti pipeline che devono accedere ai servizi di accelerazione video DirectX (DXVA). In particolare, il mixer EVR usa i servizi di elaborazione video di DXVA per eseguire la deinterlacciamento e combinare il video. Per la decodifica video accelerata, i decodificatori software possono utilizzare DXVA per l'esterno a EVR. Il presentatore condivide il dispositivo Direct3D per mezzo del [Gestione dispositivi Direct3D](direct3d-device-manager.md). Il diagramma seguente illustra l'architettura interna del EVR. Il decodificatore software, ombreggiato in grigio, non fa parte del EVR.

![diagramma dell'architettura che mostra i EVR.](images/5d4a1fd9-25ff-4cc5-a486-0d22f34bbfd7.gif)

## <a name="evr-interfaces"></a>Interfacce EVR

EVR supporta le interfacce seguenti. Alcune di queste interfacce sono implementate dal mixer o dal presentatore. Per ogni interfaccia, l'argomento di riferimento descrive come ottenere un puntatore all'interfaccia.

| Interfaccia                                                    | Descrizione                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)                 | Imposta il numero di pin di input nel filtro EVR (solo DirectShow).                                |
| [**IEVRFilterConfigEx**](/windows/desktop/api/evr/nn-evr-ievrfilterconfigex)             | Configura il filtro EVR (solo DirectShow).                                                      |
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin)     | Consente a un plug-in EVR di eseguire il rendering di video protetti.                                                 |
| [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)                 | Consente a EVR Presenter di richiedere un frame specifico dal mixer.                             |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                 | Consente al gestore della qualità di modificare la qualità del video EVR.                                      |
| [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) | Consente a un mixer o un Presenter personalizzato di ottenere i puntatori di interfaccia dal EVR.                       |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                 | Restituisce l'identificatore del dispositivo di un mixer o un presentatore di EVR.                                       |
| [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)     | Controlla il modo in cui EVR Visualizza il video.                                                              |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)           | Alfa-fonde un'immagine bitmap statica con il video.                                                |
| [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)         | Controlla il modo in cui il renderer video avanzato (EVR) combina i sottoflussi video.                            |
| [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2)       | Controlla le preferenze per la deinterlacciamento dei video.                                                     |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)     | Esegue il mapping di una posizione in un flusso video di input alla posizione corrispondente in un flusso video di output. |
| [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)               | Esposto dal presentatore di EVR.                                                                     |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)               | Controlla l'elaborazione video, inclusi la regolazione, i filtri acustici e i filtri dettagli.               |
| [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)                 | Imposta un mixer o un presentatore in EVR.                                                             |
| [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)   | Alloca gli esempi video.                                                                          |



 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                    | Descrizione                                                                           |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Uso del filtro EVR DirectShow](using-the-directshow-evr-filter.md)   | Come usare EVR in un'applicazione DirectShow.                                       |
| [Uso del sink di supporto EVR](using-the-evr-media-sink.md)                 | Come usare EVR in un'applicazione Media Foundation.                                 |
| [Uso dei controlli schermo video](using-the-video-display-controls.md) | Come controllare il modo in cui EVR Visualizza il video all'interno della finestra dell'applicazione. |
| [Uso dei controlli mixer video](using-the-video-mixer-controls.md)     | Come controllare il modo in cui funziona il mixer EVR.                               |
| [Negoziazione del tipo di supporto EVR](evr-media-type-negotiation.md)             | Viene descritto il modo in cui EVR determina i formati video che può accettare come input.          |
| [Mixer personalizzati](custom-mixers.md)                                       | Come scrivere un mixer personalizzato per la EVR.                                              |
| [Come scrivere un presentatore EVR](how-to-write-an-evr-presenter.md)       | Come scrivere un presentatore personalizzato per EVR.                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> </dl>

 

 



