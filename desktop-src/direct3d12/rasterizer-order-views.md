---
title: Rasterizzazione-viste ordinate
description: Il rasterizzatore-viste ordinate (ROV) consente pixel shader codice di contrassegnare le associazioni di visualizzazione di accesso non ordinate con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV.
ms.assetid: D308BF3E-8CBE-4DF0-B020-4D202E858D99
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19988d3f3eec39e8fc298a2fc13031ecc29e3e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548868"
---
# <a name="rasterizer-ordered-views"></a>Rasterizzazione-viste ordinate

Le visualizzazioni ordinate del rasterizzatore (ROV) consentono al codice pixel shader di contrassegnare le associazioni di visualizzazione di accesso non ordinato (UAV) con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV. Questo consente di utilizzare gli algoritmi di trasparenza (OIT) indipendente dall'ordine, che forniscono risultati di rendering molto migliori quando più oggetti trasparenti sono in linea tra loro in una visualizzazione.

-   [Overview](#overview)
-   [Dettagli di implementazione](#implementation-details)
-   [Riepilogo API](#api-summary)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Le pipeline di grafica standard possono avere problemi a comporre correttamente più trame che contengono la trasparenza. Oggetti quali recinzioni di trasmissione, fumo, incendi, vegetazione e vetro colorato usano la trasparenza per ottenere l'effetto desiderato. Si verificano problemi quando più trame che contengono la trasparenza sono allineate l'una all'altra (fumo davanti a una recinzione davanti a una costruzione di vetro che contiene la vegetazione, come esempio). Il rasterizzatore-viste ordinate (ROV) consente agli algoritmi OIT sottostanti di usare le funzionalità dell'hardware per tentare di risolvere correttamente l'ordine di trasparenza. La trasparenza viene gestita dal pixel shader.

Le visualizzazioni ordinate rasterizzatore (ROV) consentono al codice pixel shader di contrassegnare i binding UAV con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV.

Rov garantiscono l'ordine degli accessi UAV per qualsiasi coppia di chiamate pixel shader sovrapposte. In questo caso "sovrapposta" significa che le chiamate vengono generate dalle stesse chiamate di disegni e condividono la stessa coordinata pixel in modalità di esecuzione con frequenza in pixel e lo stesso pixel e la stessa coordinata di esempio in modalità frequenza di campionamento.

L'ordine in cui vengono eseguiti gli accessi ROV sovrapposti delle chiamate pixel shader è identico all'ordine in cui viene inviata la geometria. Ciò significa che, per le chiamate di pixel shader sovrapposte, le Scritture ROV eseguite da una chiamata di pixel shader devono essere disponibili per essere lette da una chiamata successiva e non devono influire sulle letture da una chiamata precedente. Le letture ROV eseguite da una chiamata di pixel shader devono riflettere le Scritture da una chiamata precedente e non devono riflettere le Scritture da una chiamata successiva. Questa operazione è importante per UAV perché vengono omesse in modo esplicito dalle garanzie di invarianza dell'output normalmente impostate dall'ordine fisso dei risultati della pipeline grafica.

## <a name="implementation-details"></a>Dettagli dell'implementazione

Le viste ordinate rasterizzatore (ROV) sono dichiarate con i nuovi oggetti HLSL (High Level Shader Language) seguenti e sono disponibili solo per l'pixel shader:

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

Usare questi oggetti allo stesso modo degli altri oggetti UAV, ad esempio e così `RWBuffer` via.

## <a name="api-summary"></a>Riepilogo dell'API

Rov sono un costrutto solo HLSL che applica una semantica di comportamento diversa a UAV. Tutte le API rilevanti per UAV sono rilevanti anche per rov. Si noti che il metodo, le strutture e la classe helper seguenti fanno riferimento al rasterizzatore:

-   [**D3D12 \_ RASTERIZZAtore \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) : struttura che contiene la descrizione del rasterizzatore.
-   [**D3D12 \_ FUNZIONALITÀ \_ dati \_ D3D12 \_ Opzioni**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : struttura che contiene un valore booleano che indica il supporto.
-   [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : metodo per accedere alle funzionalità supportate.
-   [**CD3DX12 \_ RASTERIZZAtore \_ desc**](cd3dx12-rasterizer-desc.md) : classe helper per la creazione di descrizioni del rasterizzatore.
-   [**D3D12 \_ \_Stato della pipeline grafica \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) : struttura che contiene lo stato della pipeline.

## <a name="related-topics"></a>Argomenti correlati

* [Rasterizzazione conservativa](conservative-rasterization.md)
* [Rendering](rendering.md)
* [Associazione di risorse in HLSL](resource-binding-in-hlsl.md)
* [Modello Shader 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)