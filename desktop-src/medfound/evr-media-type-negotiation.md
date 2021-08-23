---
description: Negoziazione del tipo di supporto EVR
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: Negoziazione del tipo di supporto EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6255a32f876a48d0c6193c0a9b470d20ee178ee0ae6fe4c0504b110a353075b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974490"
---
# <a name="evr-media-type-negotiation"></a>Negoziazione del tipo di supporto EVR

Questo argomento descrive come il renderer video avanzato (EVR) convalida i tipi di supporti.

-   Per il DirectShow EVR, la negoziazione del tipo si verifica quando i pin del filtro sono connessi.

-   Per il sink multimediale EVR, i tipi di supporti vengono impostati tramite [**l'interfaccia IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) nei sink di flusso. In genere il caricatore della topologia negozia i tipi di supporti, anche se l'applicazione può impostare direttamente i tipi di supporti.

L'EVR non segnala alcun tipo di supporto preferito. Il client deve testare i tipi di supporti finché non trova un tipo accettabile. Il tipo di supporto per il flusso di riferimento deve essere impostato prima che i tipi possano essere impostati in uno dei flussi secondari.

Per il flusso di riferimento, il mixer EVR ottiene un elenco di formati di destinazione di rendering DirectX Video Acceleration (DXVA) compatibili. Il presentatore EVR usa questo elenco per selezionare il formato per la catena di scambio Direct3D. Se non viene trovato alcun formato di destinazione di rendering compatibile, l'EVR rifiuta il tipo di supporto.

Per i flussi secondari, il mixer EVR esegue una query se il dispositivo DXVA supporta tale formato di flusso secondario in combinazione con il formato di destinazione di rendering selezionato per il flusso di riferimento. Di conseguenza, i formati di flusso secondari disponibili potrebbero cambiare a seconda del flusso di riferimento.

Di seguito è descritto il processo in modo più dettagliato. Questi dettagli non sono importanti per la maggior parte delle applicazioni, ma possono essere utili se si scrive un mixer o un presentatore personalizzato.

Per il flusso di riferimento, la negoziazione avviene nel modo seguente:

1.  L'EVR chiama [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) nel mixer.

2.  Il mixer converte il tipo di supporto in una descrizione DXVA 2.0, usando la [**struttura \_ VideoDesc DXVA2.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc)

3.  Il mixer chiama [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) per ottenere un elenco di GUID del processore video.

4.  Per ogni GUID del processore video, il mixer chiama [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) per ottenere i formati di destinazione di rendering supportati.

5.  L'EVR chiama [**IMFVideoPresenter::P rocessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) nel presentatore con il messaggio MFVP \_ MESSAGE \_ INVALIDATEMEDIATYPE. Questo messaggio determina la selezione di un nuovo formato da parte del presentatore.

6.  Il presentatore chiama [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere un elenco dei formati di output disponibili dal mixer. Il mixer genera questo elenco dai formati ottenuti nel passaggio 4.

7.  Il presentatore seleziona un formato e chiama [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) nel mixer.

Per i sottostream, il processo è più semplice:

1.  L'EVR chiama [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) nel mixer.

2.  Il mixer chiama [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) per ottenere un elenco dei formati di flusso secondari disponibili.

3.  Se il formato proposto è contenuto in questo elenco, l'EVR accetta il tipo di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Renderer video avanzato](enhanced-video-renderer.md)
</dt> </dl>

 

 



