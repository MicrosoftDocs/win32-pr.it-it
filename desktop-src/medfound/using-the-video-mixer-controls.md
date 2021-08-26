---
description: Uso dei controlli Mixer video
ms.assetid: 475996c6-a205-4133-8882-f55beaf9f8fd
title: Uso dei controlli Mixer video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72506a69cb1e3a8584a92cc7052541ffc210cd307073dece61f3a9d76a4c35d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887147"
---
# <a name="using-the-video-mixer-controls"></a>Uso dei controlli Mixer video

Il mixer EVR offre diverse interfacce che un'applicazione può usare per controllare il modo in cui il mixer elabora il video. Queste interfacce possono essere usate in DirectShow o Media Foundation.



| Interfaccia                                                      | Descrizione                                                                                                                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaccia IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)   | Alpha combina un'immagine bitmap statica nel video.                                                                                                                                                                                          |
| [**Interfaccia IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) | Controlla la modalità di combinazione dei sottostream video da parte dell'EVR.                                                                                                                                                                                                |
| [**Interfaccia IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)       | Controlla la regolazione del colore, i filtri immagine e altre funzionalità di elaborazione video. Questa interfaccia fornisce l'accesso alle funzionalità implementate dal driver di grafica, quindi le funzionalità esatte dipendono dal driver di grafica dell'utente. |



 

Il modo corretto per ottenere puntatori a queste interfacce dipende dal fatto che si utilizzi la versione DirectShow di EVR o Media Foundation versione. Per il Media Foundation EVR, dipende anche dal fatto che l'EVR sia in uso direttamente o tramite [la sessione multimediale](media-session.md). In genere un'applicazione userà l'EVR tramite la sessione multimediale, non direttamente.

Per ottenere un puntatore a una di queste interfacce, eseguire le operazioni seguenti:

1.  Ottenere un puntatore [**all'interfaccia IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) nell'EVR.

    -   Se si usa il filtro DirectShow EVR, chiamare **QueryInterface** sul filtro.

    -   Se si usa direttamente il sink multimediale EVR, chiamare **QueryInterface** sul sink multimediale.

    -   Se si usa la sessione multimediale, chiamare **QueryInterface** nella sessione multimediale.

2.  Se si usa la sessione multimediale, attendere che la sessione multimediale invii l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) con il valore di stato MF \_ TOPOSTATUS \_ READY. Ignorare questo passaggio se non si usa la sessione multimediale.

3.  Chiamare [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere l'interfaccia del mixer. Usare l'identificatore di servizio MR \_ VIDEO \_ MIXER \_ SERVICE.

## <a name="alpha-blending-a-bitmap-onto-the-video"></a>Alpha Blending a Bitmap onto the Video

È possibile usare [**l'interfaccia IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) per unire una bitmap statica al video durante la riproduzione. È possibile archiviare la bitmap in una superficie Direct3D, specificata come puntatore **IDirect3DSurface9,** oppure usare una bitmap GDI.

Se si usa una superficie Direct3D per la bitmap, la superficie può contenere dati alfa per pixel, che verranno usati quando il mixer esegue la fusione alfa dell'immagine. In alternativa, è possibile definire una chiave di colore, ovvero un singolo colore che sarà trasparente ovunque venga visualizzata nella bitmap. È anche possibile specificare un valore alfa che verrà applicato all'intera immagine. È anche possibile impostare un rettangolo di origine per ritagliare la bitmap e un rettangolo di destinazione per posizionare la bitmap all'interno del fotogramma video.

Per impostare la bitmap, chiamare [**IMFVideoMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap). Questo metodo accetta un puntatore a una struttura [**MFVideoAlphaBitmap**](/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmap) che specifica la bitmap e i parametri di fusione alfa. Per codice di esempio, vedere l'argomento di riferimento per il **metodo SetAlphaBitmap.**

Dopo aver impostato la bitmap, è possibile aggiornare i parametri di fusione, incluse le ricangole di origine e di destinazione, chiamando [**IMFVideoMixerBitmap::UpdateAlphaBitmapParameters**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters). L'aggiornamento ha effetto sul fotogramma video successivo. Per eseguire l'aggiornamento, è necessario che il video sia in riproduzione. È possibile usare questo metodo per eseguire animazioni semplici sulla bitmap. Se sono necessari effetti più sofisticati, è consigliabile scrivere un mixer EVR personalizzato.

Per cancellare la bitmap, chiamare [**IMFVideoMixerBitmap::ClearAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-clearalphabitmap).

## <a name="controlling-substreams"></a>Controllo dei sottostream

L'EVR può combinare uno o più sottostream video nel flusso video primario. Per controllare la combinazione di sottostream, usare [**l'interfaccia IMFVideoMixerControl.**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)

-   Chiamare [**IMFVideoMixerControl::SetStreamOutputRect**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamoutputrect) per impostare la posizione di un flusso secondario all'interno del fotogramma video composito.

-   Chiamare [**IMFVideoMixerControl::SetStreamZOrder**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamzorder) per impostare l'ordine z per i sottostream. L'EVR disegna i flussi video nell'ordine dei relativi valori nell'ordine z, a partire da zero. Il flusso video primario è sempre primo nell'ordine z.

## <a name="video-processor-settings"></a>Processore video Impostazioni

Il mixer EVR usa DirectX Video Acceleration (DXVA) per eseguire l'elaborazione video sui flussi di input. Le funzionalità di elaborazione esatte dipendono dal driver di grafica. Le funzionalità di elaborazione video vengono descritte usando la [**struttura \_ VideoProcessorCaps DXVA2.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) Un particolare set di funzionalità è detto modalità *di elaborazione video,* ogni modalità identificata da un GUID. Per un elenco di GUID predefiniti, vedere [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids). Il driver può definire GUID aggiuntivi specifici del fornitore, che rappresentano diverse combinazioni di funzionalità.

Per trovare le modalità supportate e le funzionalità di ogni modalità, eseguire le operazioni seguenti:

1.  Chiamare [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere un [**puntatore all'interfaccia IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) del mixer.

2.  Chiamare [**IMFVideoProcessor::GetAvailableVideoProcessorModes**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes). Questo metodo restituisce una matrice di GUID, che identificano le modalità del processore video disponibili. L'elenco viene restituito in ordine di qualità decrescente, la modalità con la qualità più alta visualizzata per prima nell'elenco. L'elenco può cambiare a seconda del formato del video.

3.  Per ogni GUID nell'elenco, chiamare [**IMFVideoProcessor::GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) per trovare le funzionalità della modalità processore video corrispondente. Il metodo riempie una [**struttura \_ VideoProcessorCaps DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) con una descrizione delle funzionalità.

4.  Per selezionare una modalità, chiamare [**IMFVideoProcessor::SetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode). In caso contrario, l'EVR seleziona automaticamente una modalità all'avvio dello streaming. In tal caso, è possibile chiamare [**IMFVideoProcessor::GetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessormode) per trovare la modalità selezionata.

La maggior parte dei campi nella struttura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) descrive il comportamento dei driver di basso livello e non è di interesse per un'applicazione tipica. È più probabile che i campi seguenti siano di interesse:

-   **DeviceCaps**. Questo campo indica se l'elaborazione video viene eseguita nell'hardware o nel software e se il driver di grafica è un driver DXVA 1.0 meno recente.

-   **DeinterlaceTechnology**. Questo campo fornisce alcune indicazioni sul livello di qualità deinterlacing previsto se il video di origine è interlacciato.

-   **ProcAmpControlCaps**. Questo campo specifica i controlli di regolazione del colore disponibili. Per un elenco delle possibili regolazioni del colore, vedere [ProcAmp Impostazioni](procamp-settings.md). Se il driver non può eseguire la regolazione del colore, questo campo è zero.

-   **VideoProcessorOperations**. Questo campo contiene flag che descrivono varie funzionalità di elaborazione video. Due flag di particolare importanza sono il flag DXVA2 \_ VideoProcess \_ SubStreams e il flag DXVA2 \_ VideoProcess \_ SubStreams. Almeno uno di questi flag deve essere presente perché l'EVR mescoli i flussi secondari nel flusso video di riferimento. Se non è presente alcun flag, l'EVR è limitato a un flusso video.

-   **NoiseFilterTechnology**. Questo campo indica quali filtri disturbo sono supportati dal driver di grafica. Se il driver non supporta il filtro del rumore, il valore è DXVA2 \_ NoiseFilterTech \_ Non supportato.

-   **DetailFilterTechnology**. Questo campo indica i filtri di dettaglio supportati dal driver di grafica. Se il driver non supporta il filtro del rumore, il valore è DXVA2 \_ DetailFilterTech \_ Non supportato.

## <a name="color-adjustment-and-image-filtering"></a>Regolazione del colore e filtro delle immagini

Il driver di grafica potrebbe supportare la regolazione del colore (chiamata anche *amplificazione* del processo o semplicemente *ProcAmp)* e il filtro delle immagini. Se eseguita dalla GPU, la regolazione del colore e il filtro delle immagini possono essere eseguiti in tempo reale senza sovraccarico della CPU.

Per usare queste funzionalità, seguire questa procedura:

1.  Selezionare una modalità di elaborazione video come descritto nella sezione precedente.

2.  Chiamare [**IMFVideoProcessor::GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) per trovare le funzionalità di elaborazione video come descritto nella sezione precedente. Il metodo riempie una struttura [**\_ VideoProcessorCaps DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) che descrive le funzionalità, incluso se il driver supporta la regolazione del colore e il filtro delle immagini.

3.  Per ogni regolazione del colore supportata dal driver, chiamare [**IMFVideoProcessor::GetProcAmpRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocamprange) per trovare l'intervallo di valori possibile per tale impostazione. Questo metodo restituisce anche il valore predefinito per l'impostazione. Chiamare [**IMFVideoProcessor::GetProcAmpValues**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocampvalues) per trovare il valore corrente delle impostazioni. I valori non hanno unità specificate. È il driver a definire l'intervallo di valori.

4.  Chiamare [**IMFVideoProcessor::SetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue) per impostare un valore di regolazione del colore.

5.  Se il driver supporta il filtro delle immagini, ogni tipo di filtro (disturbo e dettaglio) supporta tre impostazioni, ovvero livello, raggio e soglia, sia in chroma che in luma. Vedere Filtro [immagini DXVA Impostazioni](dxva-image-filter-settings.md). Per ogni impostazione, chiamare [**IMFVideoProcessor::GetFilteringRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringrange) per ottenere l'intervallo di valori possibili e chiamare [**IMFVideoProcessor::GetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringvalue) per ottenere il valore corrente.

6.  Per modificare l'impostazione di un filtro immagine, chiamare [**IMFVideoProcessor::SetFilteringValue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Renderer video avanzato](enhanced-video-renderer.md)
</dt> </dl>

 

 



