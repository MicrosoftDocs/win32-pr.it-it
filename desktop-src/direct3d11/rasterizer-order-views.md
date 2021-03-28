---
title: Visualizzazioni degli ordini di rasterizzatore
description: Le visualizzazioni ordinate del rasterizzatore (ROV) consentono al codice pixel shader di contrassegnare i binding UAV con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV.
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118191"
---
# <a name="rasterizer-order-views"></a>Visualizzazioni degli ordini di rasterizzatore

Le visualizzazioni ordinate del rasterizzatore (ROV) consentono al codice pixel shader di contrassegnare i binding UAV con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV. In questo modo è possibile utilizzare gli algoritmi OIT (Order Independent Transparency), che forniscono risultati di rendering migliori quando più oggetti trasparenti sono in linea tra loro in una vista.

-   [Overview](#overview)
-   [Dettagli di implementazione](#implementation-details)
-   [Riepilogo API](#api-summary)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Le pipeline di grafica standard possono avere problemi a comporre correttamente più trame che contengono la trasparenza. Oggetti quali recinzioni di trasmissione, fumo, incendi, vegetazione e vetro colorato usano la trasparenza per ottenere l'effetto desiderato. Si verificano problemi quando più trame che contengono la trasparenza sono allineate l'una all'altra (fumo davanti a una recinzione davanti a una costruzione di vetro che contiene la vegetazione, come esempio). Le visualizzazioni ordinate del rasterizzatore (ROV) consentono agli algoritmi OIT sottostanti di usare le funzionalità dell'hardware per tentare di risolvere correttamente l'ordine di trasparenza. La trasparenza viene gestita dal pixel shader.

Le visualizzazioni ordinate del rasterizzatore (ROV) consentono al codice pixel shader di contrassegnare i binding UAV con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV.

Rov garantiscono l'ordine degli accessi UAV per qualsiasi coppia di chiamate pixel shader sovrapposte. In questo caso "sovrapposta" significa che le chiamate vengono generate dalle stesse chiamate di disegni e condividono la stessa coordinata pixel in modalità di esecuzione con frequenza in pixel e lo stesso pixel e la stessa coordinata di esempio in modalità frequenza di campionamento.

L'ordine in cui vengono eseguiti gli accessi ROV sovrapposti delle chiamate pixel shader è identico all'ordine in cui viene inviata la geometria. Ciò significa che, per le chiamate di pixel shader sovrapposte, le Scritture ROV eseguite da una chiamata di pixel shader devono essere disponibili per essere lette da una chiamata successiva e non devono influire sulle letture da una chiamata precedente. Le letture ROV eseguite da una chiamata di pixel shader devono riflettere le Scritture da una chiamata precedente e non devono riflettere le Scritture da una chiamata successiva. Questa operazione è importante per UAV perché vengono omesse in modo esplicito dalle garanzie di invarianza dell'output normalmente impostate dall'ordine fisso dei risultati della pipeline grafica.

## <a name="implementation-details"></a>Dettagli dell'implementazione

Le visualizzazioni ordinate del rasterizzatore (ROV) sono dichiarate con i nuovi oggetti HLSL (High Level Shader Language) seguenti e sono disponibili solo per l'pixel shader:

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

-   [**D3d11 \_ RASTERIZZAtore \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : struttura che contiene la descrizione del rasterizzatore, notando la \_ \_ classe helper DESC2 CD3D12 rasterizzator per la creazione di descrizioni del rasterizzatore.
-   [**D3d11 \_ FEATURE \_ data \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : struttura che contiene il valore booleano `ROVsSupported` che indica il supporto.
-   [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : metodo per accedere alle funzionalità supportate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di Direct3D 11,3](direct3d-11-3-features.md)
</dt> <dt>

[Modello Shader 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 