---
title: Gestione dello stato della pipeline grafica in Direct3D 12
description: Questo argomento descrive come viene impostato lo stato della pipeline grafica in Direct3D 12.
ms.assetid: AAF97BD2-D532-469D-9242-CC94C06727C3
keywords:
- stato della pipeline
- oggetto di stato della pipeline
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7564b5863d3efebdf8a335e2c46945aeebea93e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548905"
---
# <a name="managing-graphics-pipeline-state-in-direct3d-12"></a>Gestione dello stato della pipeline grafica in Direct3D 12

Questo argomento descrive come viene impostato lo stato della pipeline grafica in Direct3D 12.

## <a name="pipeline-state-overview"></a>Panoramica dello stato della pipeline

Quando la geometria viene inviata all'unità di elaborazione grafica (GPU) da disegnare, esiste una vasta gamma di impostazioni hardware che determinano la modalità di interpretazione e rendering dei dati di input. Insieme, queste impostazioni sono denominate lo stato della pipeline grafica e includono impostazioni comuni come lo stato di rasterizzazione, lo stato di Blend e lo stato depth stencil, nonché il tipo di topologia primitiva della geometria inviata e gli shader che verranno utilizzati per il rendering. In Microsoft Direct3D 12 la maggior parte dello stato della pipeline grafica viene impostata tramite oggetti di stato della pipeline (PSO). Un'app può creare un numero illimitato di questi oggetti, rappresentati dall'interfaccia [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) , in genere in fase di inizializzazione. Quindi, in fase di rendering, gli elenchi di comandi possono cambiare rapidamente più impostazioni dello stato della pipeline chiamando [**ID3D12GraphicsCommandList:: SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate) in un elenco di comandi diretto o in un bundle per impostare il PSO attivo.

In Direct3D 11 lo stato della pipeline grafica è stato aggregato in oggetti di stato di grandi dimensioni, ad esempio [**ID3D11BlendState**](/windows/win32/api/d3d11/nn-d3d11-id3d11blendstate) , che possono essere creati e impostati in fase di rendering nel contesto immediato con metodi come [**sul ID3D11DeviceContext:: OMSetBlendState**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-omsetblendstate). L'idea alla base di questo problema era che la GPU poteva ottenere efficienza impostando impostazioni correlate, come le impostazioni dello stato di Blend, tutte contemporaneamente. Tuttavia, con l'hardware grafico odierno, esistono dipendenze tra le diverse unità hardware. Ad esempio, lo stato di Blend hardware potrebbe avere dipendenze dallo stato raster e dallo stato Blend. PSO in Direct3D 12 sono stati progettati per consentire alla GPU di pre-elaborare tutte le impostazioni dipendenti in ogni stato della pipeline, in genere durante l'inizializzazione, per eseguire il cambio tra gli stati in fase di rendering nel modo più efficiente possibile.

Si noti che, mentre la maggior parte delle impostazioni dello stato della pipeline sono impostate usando PSO, esistono alcune impostazioni di stato che vengono impostate separatamente usando le API fornite da [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist). Queste impostazioni e le API associate sono descritte in dettaglio di seguito. Inoltre, esistono differenze nel modo in cui lo stato della pipeline grafica viene ereditato da e reso permanente dagli elenchi di comandi diretti e dai bundle. Questo argomento fornisce informazioni dettagliate su entrambe le versioni seguenti.

## <a name="graphics-pipeline-states-set-with-pipeline-state-objects"></a>Stati della pipeline grafica impostati con oggetti stato della pipeline

Il modo più semplice per visualizzare tutti i diversi Stati della pipeline che possono essere impostati usando un oggetto stato della pipeline consiste nell'esaminare l'argomento di riferimento per la [**\_ \_ \_ \_ Descrizione dello stato della pipeline grafica D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) che si passa a [**ID3D12Device:: CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) quando si inizializza l'oggetto. Un breve riepilogo degli Stati che è possibile impostare include:

-   Bytecode per tutti gli shader inclusi, vertex, pixel, Domain, Hull e geometry shader.
-   Formato del vertice di input.
-   Tipo di topologia primitivo. Si noti che il tipo di topologia primitiva di input-assembler (punto, linea, triangolo, patch) viene impostato all'interno dell'oggetto PSO usando l'enumerazione [**\_ primitiva del \_ \_ tipo di topologia D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) . Il adiacenza e l'ordinamento primitivi (elenco a linee, striscia di riga, striscia di riga con dati adiacenza e così via) vengono impostati dall'interno di un elenco di comandi usando il metodo [**ID3D12GraphicsCommandList:: IASetPrimitiveTopology**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology) .
-   Stato di Blend, stato di rasterizzazione, depth stencil stato.
-   Il depth stencil e i formati della destinazione di rendering, nonché il numero di destinazioni di rendering.
-   Parametri di campionamento multiplo.
-   Buffer di output del flusso.
-   Firma radice. Per altre informazioni, vedere [firme radice](root-signatures.md).

## <a name="graphics-pipeline-states-set-outside-of-the-pipeline-state-object"></a>Stati della pipeline grafica impostati all'esterno dell'oggetto stato della pipeline

La maggior parte degli Stati della pipeline grafica viene impostata usando PSO. Tuttavia, esiste un set di parametri di stato della pipeline impostati chiamando i metodi dell'interfaccia [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) dall'interno di un elenco di comandi. La tabella seguente illustra gli stati impostati in questo modo e i metodi corrispondenti.

|State|Metodo|
|-|-|
|Associazioni di risorse|[**IASetIndexBuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)<br/>[**IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)<br/>[**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)<br/>[**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)<br/>[**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)<br/>Tutti i metodi **SetGraphicsRoot...**<br/>Tutti i metodi **SetComputeRoot...**<br/>
|Riquadri|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports">**RSSetViewports**</a>|
|Rettangoli Scissor|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects">**RSSetScissorRects**</a>|
|Fattore di fusione|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetblendfactor">**OMSetBlendFactor**</a>|
|Valore di riferimento depth stencil|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref">**OMSetStencilRef**</a>|
|Ordine della topologia primitiva di input-assembler e tipo adiacenza|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology">**IASetPrimitiveTopology**</a>|

## <a name="graphics-pipeline-state-inheritance"></a>Ereditarietà dello stato della pipeline grafica

Poiché gli elenchi di comandi diretti sono generalmente destinati a un uso alla volta e i bundle sono destinati a essere usati più volte simultaneamente, esistono regole diverse sul modo in cui ereditano lo stato della pipeline grafica impostato da elenchi di comandi o bundle precedenti.

Per gli Stati della pipeline grafica impostati con PSO, nessuno di questi stati viene ereditato da elenchi di comandi diretti o bundle. Lo stato iniziale della pipeline grafica per gli elenchi di comandi diretti e i bundle viene impostato al momento della creazione con il parametro [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) su [**ID3D12Device:: CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist). Se nella chiamata non viene specificato alcun oggetto PSO, viene utilizzato uno stato iniziale predefinito. È possibile modificare l'oggetto PSO corrente all'interno di un elenco di comandi chiamando [**ID3D12GraphicsCommandList:: SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Gli elenchi di comandi diretti non ereditano inoltre lo stato impostato con i metodi dell'elenco di comandi, ad esempio [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports). Per informazioni dettagliate sui valori iniziali predefiniti per gli Stati non PSO, vedere [**ID3D12GraphicsCommandList:: ClearState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate).

I bundle ereditano tutti gli Stati della pipeline grafica che non sono impostati con PSO, ad eccezione del tipo di topologia primitivo. La topologia primitiva è sempre impostata su [**D3D12 \_ tipo di topologia primitivo non \_ \_ \_ definito**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) quando viene avviata l'esecuzione di un bundle. Qualsiasi stato impostato all'interno di un bundle (il PSO stesso, lo stato non basato su PSO e le associazioni di risorse) influiscono sullo stato dell'elenco di comandi diretti padre. Ad esempio, se un [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports) viene chiamato dall'interno di un bundle, i viewport specificati continueranno a essere impostati nell'elenco dei comandi diretti padre per le chiamate successive alla chiamata [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) che imposta i viewport.

Le associazioni di risorse impostate in un elenco di comandi o in un bundle vengono mantenute. Le associazioni di risorse modificate in un elenco di comandi diretto verranno comunque impostate nell'esecuzione del bundle figlio successiva. Le associazioni di risorse e modificate dall'interno di un bundle verranno comunque impostate per le chiamate successive all'interno dell'elenco dei comandi diretti padre.

Per ulteriori informazioni sulle associazioni, vedere la sezione relativa alla **semantica del bundle** di [utilizzo di una firma radice](using-a-root-signature.md).

## <a name="related-topics"></a>Argomenti correlati

* [Invio di lavoro in Direct3D 12](command-queues-and-command-lists.md)