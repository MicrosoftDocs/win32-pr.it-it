---
description: Uso dei controlli mixer video
ms.assetid: 475996c6-a205-4133-8882-f55beaf9f8fd
title: Uso dei controlli mixer video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a062c6f984e0eac0128bd67c72bf691c95af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049795"
---
# <a name="using-the-video-mixer-controls"></a>Uso dei controlli mixer video

Il mixer EVR offre diverse interfacce che un'applicazione può usare per controllare il modo in cui il mixer elabora il video. Queste interfacce possono essere utilizzate sia in DirectShow che in Media Foundation.



| Interfaccia                                                      | Descrizione                                                                                                                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaccia [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)   | Alfa-fonde un'immagine bitmap statica nel video.                                                                                                                                                                                          |
| Interfaccia [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) | Controlla il modo in cui EVR combina i flussi sottoflussi video.                                                                                                                                                                                                |
| Interfaccia [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)       | Controlla la regolazione del colore, i filtri immagini e altre funzionalità di elaborazione video. Questa interfaccia consente di accedere alle funzionalità implementate dal driver di grafica, pertanto le funzionalità esatte dipendono dal driver grafico dell'utente. |



 

Il modo corretto per ottenere i puntatori a queste interfacce varia a seconda che si usi la versione DirectShow di EVR o la versione Media Foundation. Per il Media Foundation EVR, dipende anche dal fatto che il EVR venga usato direttamente o tramite la [sessione multimediale](media-session.md). In genere, un'applicazione userà EVR tramite la sessione multimediale, non direttamente.

Per ottenere un puntatore a una di queste interfacce, procedere come segue:

1.  Ottenere un puntatore all'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) in EVR.

    -   Se si usa il filtro EVR DirectShow, chiamare **QueryInterface** sul filtro.

    -   Se si usa direttamente il sink di supporto EVR, chiamare **QueryInterface** sul sink multimediale.

    -   Se si usa la sessione multimediale, chiamare **QueryInterface** nella sessione multimediale.

2.  Se si usa la sessione multimediale, attendere che la sessione multimediale invii l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) con un valore di stato MF \_ TOPOSTATUS \_ Ready. Ignorare questo passaggio se non si usa la sessione multimediale.

3.  Chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere l'interfaccia del mixer. Usare il servizio di mixer video dell'identificatore del servizio \_ \_ \_ .

## <a name="alpha-blending-a-bitmap-onto-the-video"></a>Fusione alfa di una bitmap nel video

È possibile usare l'interfaccia [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) per la fusione alfa di una bitmap statica nel video durante la riproduzione. È possibile archiviare la bitmap in una superficie Direct3D, specificata come puntatore **IDirect3DSurface9** , oppure utilizzare una bitmap GDI.

Se si usa una superficie Direct3D per la bitmap, la superficie può contenere dati alfa per pixel, che verranno usati quando il mixer Alfa-fonde l'immagine. In alternativa, è possibile definire una chiave di colore, ovvero un singolo colore che sarà trasparente ovunque venga visualizzato nella bitmap. Inoltre, è possibile specificare un valore alfa che verrà applicato all'intera immagine. È anche possibile impostare un rettangolo di origine per ritagliare la bitmap e un rettangolo di destinazione per posizionare la bitmap all'interno del fotogramma video.

Per impostare la bitmap, chiamare [**IMFVideoMixerBitmap:: SetAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap). Questo metodo accetta un puntatore a una struttura [**MFVideoAlphaBitmap**](/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmap) che specifica la bitmap e i parametri di fusione alfa. Per un esempio di codice, vedere l'argomento di riferimento per il metodo **SetAlphaBitmap** .

Dopo aver impostato la bitmap, è possibile aggiornare i parametri di fusione, inclusi i recangles di origine e di destinazione, chiamando [**IMFVideoMixerBitmap:: UpdateAlphaBitmapParameters**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters). L'aggiornamento viene applicato al frame video successivo. Per eseguire l'aggiornamento, è necessario che il video sia in esecuzione. È possibile utilizzare questo metodo per eseguire animazioni semplici sulla bitmap. Se sono necessari effetti più sofisticati, provare a scrivere un mixer EVR personalizzato.

Per cancellare la bitmap, chiamare [**IMFVideoMixerBitmap:: ClearAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-clearalphabitmap).

## <a name="controlling-substreams"></a>Controllo di sottoflussi

EVR è in grado di combinare uno o più flussi video nel flusso video primario. Per controllare la combinazione di sottoflussi, utilizzare l'interfaccia [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) .

-   Chiamare [**IMFVideoMixerControl:: SetStreamOutputRect**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamoutputrect) per impostare la posizione di un sottoflusso all'interno del frame video composito.

-   Chiamare [**IMFVideoMixerControl:: SetStreamZOrder**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamzorder) per impostare l'ordine z per i flussi sottoflussi. Il EVR disegna i flussi video nell'ordine dei valori dell'ordine z, a partire da zero. Il flusso video primario è sempre primo nell'ordine z.

## <a name="video-processor-settings"></a>Impostazioni del processore video

Il mixer EVR usa l'accelerazione video DirectX (DXVA) per eseguire l'elaborazione video sui flussi di input. Le funzionalità di elaborazione esatte dipendono dal driver Graphics. Le funzionalità di elaborazione video sono descritte usando la struttura [**\_ VideoProcessorCaps di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) . Un particolare set di funzionalità viene definito *modalità di elaborazione video*, ogni modalità identificata da un GUID. Per un elenco di GUID predefiniti, vedere [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids). Il driver può definire GUID aggiuntivi specifici del fornitore, che rappresentano diverse combinazioni di funzionalità.

Per trovare le modalità supportate e le funzionalità di ogni modalità, eseguire le operazioni seguenti:

1.  Chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere un puntatore all'interfaccia [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) del mixer.

2.  Chiamare [**IMFVideoProcessor:: GetAvailableVideoProcessorModes**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes). Questo metodo restituisce una matrice di GUID che identificano le modalità di elaborazione video disponibili. L'elenco viene restituito in ordine di qualità decrescente, ovvero la modalità con la qualità più elevata visualizzata per prima nell'elenco. L'elenco può variare a seconda del formato del video.

3.  Per ogni GUID nell'elenco, chiamare [**IMFVideoProcessor:: GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) per trovare le funzionalità della modalità di elaborazione video corrispondente. Il metodo compila una struttura [**\_ VideoProcessorCaps di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) con una descrizione delle funzionalità.

4.  Per selezionare una modalità, chiamare [**IMFVideoProcessor:: SetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode). In caso contrario, EVR seleziona automaticamente una modalità di inizio del flusso. In tal caso, è possibile chiamare [**IMFVideoProcessor:: GetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessormode) per individuare la modalità selezionata.

La maggior parte dei campi nella [**struttura \_ VideoProcessorCaps di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) descrive il comportamento dei driver di basso livello e non è rilevante in un'applicazione tipica. È più probabile che i campi seguenti siano di interesse:

-   **DeviceCaps**. Questo campo indica se l'elaborazione video viene eseguita in hardware o software e se il driver di grafica è un driver DXVA 1,0 precedente.

-   **DeinterlaceTechnology**. Questo campo fornisce un'indicazione del livello di qualità di deinterlacciamento che è possibile prevedere se il video di origine è interlacciato.

-   **ProcAmpControlCaps**. Questo campo specifica i controlli di regolazione del colore disponibili. Per un elenco delle possibili regolazioni dei colori, vedere [impostazioni del Procampo](procamp-settings.md). Se il driver non è in grado di eseguire la regolazione del colore, questo campo è zero.

-   **VideoProcessorOperations**. Questo campo contiene i flag che descrivono le varie funzionalità di elaborazione video. Due flag di particolare importanza sono il \_ flag dei \_ sottoflussi VIDEOPROCESS di DXVA2 e il \_ flag dei \_ sottoflussi DXVA2 VideoProcess. È necessario che sia presente almeno uno di questi flag per EVR per combinare i flussi sottoflussi nel flusso video di riferimento. Se non è presente alcun flag, il EVR è limitato a un flusso video.

-   **NoiseFilterTechnology**. Questo campo indica quali filtri acustici sono supportati dal driver di grafica. Se il driver non supporta il filtro acustico, il valore è DXVA2 \_ NoiseFilterTech non \_ supportato.

-   **DetailFilterTechnology**. Questo campo indica quali filtri dei dettagli sono supportati dal driver di grafica. Se il driver non supporta il filtro acustico, il valore è DXVA2 \_ DetailFilterTech non \_ supportato.

## <a name="color-adjustment-and-image-filtering"></a>Regolazione del colore e filtro delle immagini

Il driver di grafica potrebbe supportare la regolazione del colore (detta anche *amplificazione dei processi* o *ProcAmp*) e il filtro delle immagini. Quando vengono eseguite dalla GPU, la regolazione del colore e il filtro delle immagini possono essere eseguiti in tempo reale senza overhead della CPU.

Per usare queste funzionalità, seguire questa procedura:

1.  Selezionare una modalità di elaborazione video come descritto nella sezione precedente.

2.  Chiamare [**IMFVideoProcessor:: GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) per trovare le funzionalità di elaborazione video, come descritto nella sezione precedente. Il metodo compila una struttura [**\_ VideoProcessorCaps DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) che descrive le funzionalità, ad esempio se il driver supporta la regolazione del colore e il filtro delle immagini.

3.  Per ogni regolazione del colore supportata dal driver, chiamare [**IMFVideoProcessor:: GetProcAmpRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocamprange) per trovare il possibile intervallo di valori per tale impostazione. Questo metodo restituisce anche il valore predefinito per l'impostazione. Chiamare [**IMFVideoProcessor:: GetProcAmpValues**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocampvalues) per trovare il valore corrente delle impostazioni. I valori non hanno unità specificate. Spetta al driver definire l'intervallo di valori.

4.  Chiamare [**IMFVideoProcessor:: SetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue) per impostare un valore di regolazione del colore.

5.  Se il driver supporta il filtro delle immagini, ogni tipo di filtro (rumore e dettagli) supporta tre impostazioni, ovvero livello, raggio e soglia, sia in crominanza che in luminanza. Vedere [impostazioni del filtro immagine DXVA](dxva-image-filter-settings.md). Per ogni impostazione, chiamare [**IMFVideoProcessor:: GetFilteringRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringrange) per ottenere l'intervallo dei valori possibili e chiamare [**IMFVideoProcessor:: GetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringvalue) per ottenere il valore corrente.

6.  Per modificare un'impostazione del filtro immagine, chiamare [**IMFVideoProcessor:: SetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Renderer video migliorato](enhanced-video-renderer.md)
</dt> </dl>

 

 



