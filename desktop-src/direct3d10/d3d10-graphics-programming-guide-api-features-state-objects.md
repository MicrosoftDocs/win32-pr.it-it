---
description: In Direct3D 10 lo stato del dispositivo è raggruppato in oggetti di stato che riducono notevolmente il costo delle modifiche dello stato.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Oggetti di stato (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a51c05e3e220e510c462265941549f91e6368a9
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335425"
---
# <a name="state-objects-direct3d-10"></a>Oggetti di stato (Direct3D 10)

In Direct3D 10 lo stato del dispositivo è raggruppato in oggetti di stato che riducono notevolmente il costo delle modifiche dello stato. Sono disponibili diversi oggetti stato e ognuno è progettato per inizializzare un set di stato per una determinata fase della pipeline. È possibile creare fino a 4096 di ogni tipo di oggetto stato.

-   [Stato del layout di input](#input-layout-state)
-   [Stato rasterizzazione](#rasterizer-state)
-   [Stato depth-stencil](#depth-stencil-state)
-   [Stato di blend](#blend-state)
-   [Stato del campionatore](#sampler-state)
-   [Considerazioni sulle prestazioni](#performance-considerations)
-   [Argomenti correlati](#related-topics)

## <a name="input-layout-state"></a>Input-Layout stato

Questo gruppo di stato (vedere [**D3D10 \_ INPUT \_ ELEMENT \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)determina il modo in cui la fase dell'assembler di [input](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) legge i dati dai buffer di input e lo assembla per l'uso da parte del vertex shader. Include lo stato, ad esempio il numero di elementi nel buffer di input e la firma dei dati di input. La fase dell'assembler di input è una nuova fase della pipeline il cui processo è quello di trasmettere le primitive dalla memoria alla pipeline.

Per creare un oggetto input-layout-state, vedere [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).

## <a name="rasterizer-state"></a>Stato rasterizzazione

Questo gruppo di stato (vedere [**D3D10 \_ RASTERIZER \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)inizializza la fase [del rasterizzatore](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md). Questo oggetto include lo stato, ad esempio le modalità di riempimento o di interruzione, l'abilitazione di un rettangolo di forbice per il ritaglio e l'impostazione di parametri multicampionamento. Questa fase rasterizza le primitive in pixel, eseguendo operazioni come il ritaglio e il mapping delle primitive al viewport.

Per creare un oggetto stato di rasterizzazione, vedere [**CreateRasterizerState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate)

## <a name="depth-stencil-state"></a>Depth-Stencil stato

Questo gruppo di stato (vedere [**D3D10 \_ DEPTH \_ STENCIL \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)inizializza la parte depth-stencil della fase [di unione dell'output.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) In particolare, questo oggetto inizializza i test di profondità e stencil.

Per creare un oggetto depth-stencil-state, vedere [**CreateDepthStencilState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate)

## <a name="blend-state"></a>Stato blend

Questo gruppo di stato (vedere [**D3D10 \_ BLEND \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)inizializza la parte di fusione della fase [di unione dell'output.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md)

Per creare un oggetto stato di blend, vedere [**CreateBlendState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate)

## <a name="sampler-state"></a>Stato del campionatore

Questo gruppo di stato (vedere [**D3D10 \_ SAMPLER \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)inizializza un oggetto campionatore. Un oggetto campionatore viene usato dalle fasi dello shader per filtrare le trame in memoria.



Differenze tra Direct3D 9 e Direct3D 10:

- In Direct3D 10 l'oggetto campionatore non è più associato a una trama specifica, ma descrive semplicemente come filtrare in base a qualsiasi risorsa collegata.



 

Per creare un oggetto sampler-state, vedere [**CreateSamplerState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate)

## <a name="performance-considerations"></a>Considerazioni sulle prestazioni

La progettazione dell'API per l'uso di oggetti di stato offre diversi vantaggi in termini di prestazioni. Questi includono la convalida dello stato al momento della creazione dell'oggetto, l'abilitazione della memorizzazione nella cache degli oggetti di stato nell'hardware e la riduzione notevolmente della quantità di stato passata durante una chiamata API di impostazione dello stato (passando un handle all'oggetto di stato anziché lo stato).

Per ottenere questi miglioramenti delle prestazioni, è necessario creare gli oggetti di stato all'avvio dell'applicazione, molto prima del ciclo di rendering. Gli oggetti di stato non sono modificabili, in altri modo, una volta creati, non è possibile modificarli. È invece necessario eliminare e ricrearli. Per far fronte a questa restrizione, è possibile creare fino a 4096 di ogni tipo di oggetti di stato. Ad esempio, è possibile creare diversi oggetti campionatore con varie combinazioni di stato del campionatore. La modifica dello stato del campionatore viene quindi eseguita chiamando l'API Set appropriata che passa un handle all'oggetto (anziché allo stato del campionatore). In questo modo si riduce notevolmente la quantità di overhead durante ogni frame di rendering per la modifica dello stato poiché il numero di chiamate e la quantità di dati vengono notevolmente ridotti.

In alternativa, è possibile scegliere di usare il sistema di effetti che gestirà automaticamente la creazione e la distruzione efficienti degli oggetti di stato per l'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
