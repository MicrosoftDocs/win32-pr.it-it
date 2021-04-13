---
description: Negoziazione del tipo di supporto EVR
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: Negoziazione del tipo di supporto EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1f87a24db866c9e80b211b0385c12dcd6b594
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351456"
---
# <a name="evr-media-type-negotiation"></a>Negoziazione del tipo di supporto EVR

In questo argomento viene descritto il modo in cui il renderer video avanzato (EVR) convalida i tipi di supporto.

-   Per il filtro EVR DirectShow, la negoziazione dei tipi si verifica quando i pin del filtro sono connessi.

-   Per il sink di supporto EVR, i tipi di supporto vengono impostati tramite l'interfaccia [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) nei sink di flusso. In genere, il caricatore della topologia negozia i tipi di supporto, anche se l'applicazione può anche impostare direttamente i tipi di supporto.

EVR non segnala i tipi di supporto preferiti. Il client deve testare i tipi di supporti fino a quando non trova un tipo accettabile. Il tipo di supporto per il flusso di riferimento deve essere impostato prima di poter impostare i tipi in uno qualsiasi dei sottoflussi.

Per il flusso di riferimento, il mixer EVR ottiene un elenco di formati di destinazione di rendering DXVA (DirectX Video Acceleration) compatibili. EVR Presenter utilizza questo elenco per selezionare il formato per la catena di scambio Direct3D. Se non è possibile trovare un formato di destinazione di rendering compatibile, EVR rifiuterà il tipo di supporto.

Per i sottoflussi, il mixer EVR esegue una query per determinare se il dispositivo DXVA supporta tale formato in combinazione con il formato di destinazione di rendering selezionato per il flusso di riferimento. Di conseguenza, i formati dei sottoflussi disponibili possono variare a seconda del flusso di riferimento.

Ecco il processo in modo più dettagliato. Questi dettagli non sono importanti per la maggior parte delle applicazioni, ma possono essere utili se si sta scrivendo un mixer o un Presenter personalizzato.

Per il flusso di riferimento, la negoziazione si verifica nel modo seguente:

1.  EVR chiama [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) sul mixer.

2.  Il mixer converte il tipo di supporto in una descrizione di DXVA 2,0, usando la struttura [**\_ VideoDesc di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) .

3.  Il mixer chiama [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) per ottenere un elenco di GUID del processore video.

4.  Per ogni GUID del processore video, il mixer chiama [**IDirectXVideoProcessorService:: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) per ottenere i formati di destinazione di rendering supportati.

5.  EVR chiama [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) sul Presenter con il messaggio MFVP \_ INVALIDATEMEDIATYPE message \_ . Questo messaggio fa in modo che il relatore selezioni un nuovo formato.

6.  Il Presenter chiama [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere un elenco dei formati di output disponibili dal mixer. Il mixer genera questo elenco dai formati ottenuti nel passaggio 4.

7.  Il Presenter seleziona un formato e chiama [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) sul mixer.

Per i sottoflussi, il processo è più semplice:

1.  EVR chiama [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) sul mixer.

2.  Il mixer chiama [**IDirectXVideoProcessorService:: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) per ottenere un elenco dei formati sottoflussi disponibili.

3.  Se il formato proposto è contenuto nell'elenco, EVR accetta il tipo di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Renderer video migliorato](enhanced-video-renderer.md)
</dt> </dl>

 

 



