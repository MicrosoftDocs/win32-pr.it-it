---
description: In Direct3D 10 lo stato del dispositivo è raggruppato in oggetti di stato che consentono di ridurre notevolmente il costo delle modifiche di stato.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Oggetti stato (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a06e8603361a83049440774cfd2e12b4148b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304603"
---
# <a name="state-objects-direct3d-10"></a>Oggetti stato (Direct3D 10)

In Direct3D 10 lo stato del dispositivo è raggruppato in oggetti di stato che consentono di ridurre notevolmente il costo delle modifiche di stato. Sono disponibili diversi oggetti di stato e ognuno è progettato per inizializzare un set di stato per una determinata fase della pipeline. È possibile creare fino a 4096 di ogni tipo di oggetto di stato.

-   [Input-stato layout](#input-layout-state)
-   [Stato rasterizzazione](#rasterizer-state)
-   [Stato stencil profondità](#depth-stencil-state)
-   [Stato di Blend](#blend-state)
-   [Stato campionatore](#sampler-state)
-   [Considerazioni sulle prestazioni](#performance-considerations)
-   [Argomenti correlati](#related-topics)

## <a name="input-layout-state"></a>Stato Input-Layout

Questo gruppo di stato (vedere [**\_ elemento input \_ D3D10 \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) determina il modo in cui la [fase input-assembler](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) legge i dati dai buffer di input e li assembla per l'uso da parte del vertex shader. Questo include lo stato, ad esempio il numero di elementi nel buffer di input e la firma dei dati di input. La fase input-assembler è una nuova fase della pipeline il cui compito è quello di trasmettere le primitive dalla memoria alla pipeline.

Per creare un oggetto di stato del layout di input, vedere [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).

## <a name="rasterizer-state"></a>Stato rasterizzazione

Questo gruppo di stato (vedere [**D3D10 \_ rasterizzator \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) Inizializza la [fase di rasterizzazione](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md). Questo oggetto include lo stato, ad esempio le modalità riempimento o selezione, l'abilitazione di un rettangolo a forbice per il ritaglio e l'impostazione di parametri multisample. In questa fase le primitive vengono rasterizzate in pixel, eseguendo operazioni come il ritaglio e il mapping delle primitive al viewport.

Per creare un oggetto di stato di rasterizzazione, vedere [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).

## <a name="depth-stencil-state"></a>Stato Depth-Stencil

Questo gruppo di stato (vedere [**D3D10 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) Inizializza la parte depth-stencil della [fase di Unione dell'output](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md). In particolare, questo oggetto Inizializza la profondità e il test di stencil.

Per creare un oggetto depth-stencil-state, vedere [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).

## <a name="blend-state"></a>Stato di Blend

Questo gruppo di stato (vedere [**D3D10 \_ Blend \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) Inizializza la parte di combinazione della [fase di Unione dell'output](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).

Per creare un oggetto di stato Blend, vedere [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).

## <a name="sampler-state"></a>Stato campionatore

Questo gruppo di stato (vedere [**D3D10 \_ Sampler \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) Inizializza un oggetto Sampler. Un oggetto Sampler viene usato dalle fasi dello shader per filtrare le trame in memoria.



|                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10:<br/> In Direct3D 10, l'oggetto Sampler non è più associato a una trama specifica, ma descrive semplicemente come applicare il filtro in base a qualsiasi risorsa collegata. |



 

Per creare un oggetto stato del campionatore, vedere [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).

## <a name="performance-considerations"></a>Considerazioni sulle prestazioni

La progettazione dell'API per l'utilizzo di oggetti stato crea diversi vantaggi in merito alle prestazioni. Sono inclusi lo stato di convalida al momento della creazione dell'oggetto, l'abilitazione della memorizzazione nella cache degli oggetti stato nell'hardware e la riduzione sostanziale della quantità di stato passato durante una chiamata API di impostazione dello stato (passando un handle all'oggetto stato anziché allo stato).

Per ottenere questi miglioramenti delle prestazioni, è necessario creare gli oggetti di stato all'avvio dell'applicazione, ben prima del ciclo di rendering. Gli oggetti di stato non sono modificabili, ovvero, una volta creati, non è possibile modificarli. È invece necessario eliminarli e ricrearli. Per ovviare a questa restrizione, è possibile creare fino a 4096 di ogni tipo di oggetti stato. Ad esempio, è possibile creare diversi oggetti sampler con diverse combinazioni di stato del campionatore. La modifica dello stato del campionatore viene quindi eseguita chiamando l'API set appropriata che passa un handle all'oggetto (anziché lo stato del campionatore). Questo riduce significativamente la quantità di overhead durante ogni frame di rendering per la modifica dello stato, in quanto il numero di chiamate e la quantità di dati vengono notevolmente ridotti.

In alternativa, è possibile scegliere di utilizzare il sistema di effetti che gestirà automaticamente la creazione e l'eliminazione efficienti degli oggetti stato per l'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
