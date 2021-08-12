---
title: Visualizzazioni ordinate dal rasterizzatore
description: Le viste ordinate dal rasterizzatore consentono al codice pixel shader di contrassegnare le associazioni di visualizzazione di accesso non ordinate con una dichiarazione che modifica i normali requisiti per l'ordine dei risultati della pipeline grafica per gli UAV.
ms.assetid: D308BF3E-8CBE-4DF0-B020-4D202E858D99
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214098f70608d5f20d24edb1312593c6215abea12efecfc6eea97148e8855cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300982"
---
# <a name="rasterizer-ordered-views"></a>Visualizzazioni ordinate dal rasterizzatore

Le visualizzazioni ordinate dal rasterizzatore consentono al codice pixel shader di contrassegnare le associazioni di visualizzazione di accesso non ordinate con una dichiarazione che modifica i normali requisiti per l'ordine dei risultati della pipeline grafica per gli UAV. Ciò consente il funzionamento degli algoritmi OIT (Order-Independent Transparency), che offrono risultati di rendering molto migliori quando più oggetti trasparenti sono in linea tra loro in una vista.

-   [Panoramica](#overview)
-   [Dettagli dell'implementazione](#implementation-details)
-   [Riepilogo dell'API](#api-summary)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Le pipeline di grafica standard possono avere problemi a comporre correttamente più trame contenenti trasparenza. Per ottenere l'effetto desiderato, gli oggetti come recinti, fumi, incendi, piante e vetri colorati usano la trasparenza. I problemi si verificano quando più trame che contengono trasparenza sono in linea tra loro (fuma davanti a un recinto davanti a un edificio in vetro contenente piante di piante, ad esempio). Le viste ordinate dal rasterizzatore consentono agli algoritmi OIT sottostanti di usare le funzionalità dell'hardware per tentare di risolvere correttamente l'ordine di trasparenza. La trasparenza viene gestita dal pixel shader.

Le viste ordinate dal rasterizzatore consentono al codice pixel shader di contrassegnare le associazioni UAV con una dichiarazione che modifica i normali requisiti per l'ordine dei risultati della pipeline grafica per gli UAV.

I ROV garantiscono l'ordine degli accessi UAV per qualsiasi coppia di pixel shader chiamate. In questo caso la "sovrapposizione" significa che le chiamate vengono generate dalle stesse chiamate di disegno e condividono la stessa coordinata pixel in modalità di esecuzione a frequenza pixel e la stessa coordinata pixel e campione in modalità frequenza di campionamento.

L'ordine in cui vengono eseguiti gli accessi ROV sovrapposti pixel shader chiamate è identico all'ordine in cui viene inviata la geometria. Ciò significa che, per le chiamate pixel shader sovrapposte, le scritture ROV eseguite da una chiamata pixel shader devono essere disponibili per essere lette da una chiamata successiva e non devono influire sulle operazioni di lettura da una chiamata precedente. Le operazioni di lettura ROV eseguite da una chiamata pixel shader devono riflettere le scritture eseguite da una chiamata precedente e non devono riflettere le scritture da una chiamata successiva. Questo è importante per gli UAV perché vengono omessi in modo esplicito dalle garanzie di invarianza di output normalmente impostate dall'ordine fisso dei risultati della pipeline grafica.

## <a name="implementation-details"></a>Dettagli dell'implementazione

Le viste ordinate dal rasterizzatore vengono dichiarate con i nuovi oggetti HLSL (High Level Shader Language) seguenti e sono disponibili solo per l'pixel shader:

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

Usare questi oggetti nello stesso modo degli altri oggetti UAV (ad esempio `RWBuffer` e così via).

## <a name="api-summary"></a>Riepilogo dell'API

I ROV sono un costrutto solo HLSL che applica una semantica del comportamento diversa agli UAV. Anche tutte le API rilevanti per gli UAV sono rilevanti per i ROV. Si noti che il metodo, le strutture e la classe helper seguenti fanno riferimento al rasterizzatore:

-   [**D3D12 \_ RASTERIZER \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) struttura che contiene la descrizione del rasterizzatore.
-   [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) struttura contenente un valore booleano, che indica il supporto.
-   [**CheckFeatureSupport:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) metodo per accedere alle funzionalità supportate.
-   [**CD3DX12 \_ RASTERIZER \_ DESC:**](cd3dx12-rasterizer-desc.md) classe helper per la creazione di descrizioni del rasterizzatore.
-   [**D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) struttura che contiene lo stato della pipeline.

## <a name="related-topics"></a>Argomenti correlati

* [Rasterizzazione conservativa](conservative-rasterization.md)
* [Rendering](rendering.md)
* [Associazione di risorse in HLSL](resource-binding-in-hlsl.md)
* [Modello shader 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)