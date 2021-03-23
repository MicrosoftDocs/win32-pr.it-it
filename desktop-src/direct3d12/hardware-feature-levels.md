---
title: Livelli di funzionalità hardware
description: Descrive la funzionalità dei livelli di \_ funzionalità hardware da 11 a 12 \_ 1.
ms.assetid: B8304E29-A532-464E-8FAF-075228D8FB73
keywords:
- Livello di funzionalità DX
- Livello di funzionalità DirectX
- livello funzionalità, DX
- livello funzionalità, DirectX
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d464f6cc52539e31fee5e234af2c045dfff7e413
ms.sourcegitcommit: 218b1ff779402c3ebe1786679e1aa80a5c0d6c95
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104548781"
---
# <a name="hardware-feature-levels"></a>Livelli di funzionalità hardware

Descrive la funzionalità dei livelli di \_ funzionalità hardware da 11 a 12 \_ 1.

-   [Sistemi di numerazione](#numbering-systems)
-   [Supporto a livello di funzionalità](#feature-level-support)
-   [Supporto hardware per formati DXGI](#hardware-support-for-dxgi-formats)
-   [Argomenti correlati](#related-topics)

Per gestire la diversità di schede video in computer nuovi ed esistenti, in Microsoft Direct3D 11 è stato introdotto il concetto di livelli di funzionalità. Ogni scheda video implementa un certo livello di funzionalità di Microsoft DirectX (DX), a seconda delle GPU (Graphics Processing Unit) installate. Un livello di funzionalità è un set di funzionalità GPU ben definito. Ad esempio, il livello di funzionalità di 11 \_ 0 implementa la funzionalità implementata in Direct3D 11.

A questo punto, quando si crea un dispositivo, è possibile provare a creare un dispositivo per il livello di funzionalità che si desidera richiedere. Se la creazione del dispositivo funziona, il livello di funzionalità esiste, in caso contrario, l'hardware non supporta tale livello di funzionalità. È possibile provare a ricreare un dispositivo a un livello di funzionalità inferiore oppure è possibile scegliere di uscire dall'applicazione.

Le proprietà di base dei livelli di funzionalità sono:

-   Tutti i driver Direct3D 12 saranno a livello di funzionalità 11 \_ 0 o superiore.
-   Una GPU che consente la creazione di un dispositivo soddisfa o supera la funzionalità del livello di funzionalità.
-   Un livello di funzionalità include sempre la funzionalità dei livelli di funzionalità precedenti o inferiori.
-   Un livello di funzionalità non implica prestazioni, solo funzionalità. Le prestazioni dipendono dall'implementazione dell'hardware.
-   Un livello di funzionalità viene scelto quando si chiama [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice).
-   Per informazioni più dettagliate sulle funzionalità supportate, in particolare quelle contrassegnate come *facoltative* nella tabella seguente, il che significa che l'hardware potrebbe supportare la funzionalità, ma non è necessario, chiamare [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Per informazioni sulle limitazioni della creazione di dispositivi di tipo non hardware a determinati livelli di funzionalità, vedere [limitazioni della creazione di dispositivi Warp e Reference](/windows/desktop/direct3d11/overviews-direct3d-11-devices-limitations). Per altre informazioni sull'introduzione dei livelli di funzionalità, vedere la documentazione di Direct3D 11 sui [livelli di funzionalità di Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).

## <a name="numbering-systems"></a>Sistemi di numerazione

I livelli di funzionalità hardware *non* corrispondono a quelli delle versioni API. Ad esempio, è disponibile un'API di D3D 11.3, ma non esiste alcun \_ livello di funzionalità hardware 11 3. I livelli di funzionalità sono definiti nell'enumerazione del [**\_ \_ livello di funzionalità D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) .

Esistono tre sistemi di numerazione distinti:

-   Nelle versioni Direct3D viene utilizzato un punto; ad esempio, Direct3D 12,0.
-   I modelli shader utilizzano un punto; ad esempio, il modello di shader 5,1.
-   I livelli di funzionalità usano un carattere di sottolineatura; ad esempio, il livello di funzionalità 12 \_ 0.

## <a name="feature-level-support"></a>Supporto a livello di funzionalità

Le funzionalità seguenti sono disponibili per ogni livello di funzionalità Direct3D.

Le intestazioni nella riga superiore sono livelli di funzionalità Direct3D. Le intestazioni nella colonna a sinistra sono features.



| \\Livello funzionalità funzionalità                                                                                                 | 12 \_ 1 ⁰                    | 12 \_ 0 ⁰                    | 11 \_ 1 ¹                   | 11 \_ 0                    |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------|---------------------------|--------------------------|--------------------------|
| Modello di shader                                                                                                             | 5.1                       | 5.1                       | 5,1 ²                     | 5,1 ²                     |
| [Livello di associazione delle risorse](hardware-support.md)                                                                            | Livello 2 ³                    | Livello 2 ³                    | Tier1 ³                   | Tier1 ³                   |
| [Risorse affiancate](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)                                                                        | Livello 2 ³                    | Livello 2 ³                    | Facoltativo                 | Facoltativo                 |
| [Rasterizzazione conservativa](conservative-rasterization.md)                                                             | Tier1 ³                    | Facoltativo                  | Facoltativo                 | No                       |
| [Visualizzazioni ordinate del rasterizzatore](rasterizer-order-views.md)                                                                   | sì                       | Facoltativo                  | Facoltativo                 | No                       |
| [Filtri min/max](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)                                                                                      | Sì                       | sì                       | Facoltativo                 | No                       |
| Buffer predefinito mappa                                                                                                       | Facoltativo                  | Facoltativo                  | Facoltativo                 | Facoltativo                 |
| [Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md)                                 | Facoltativo                  | Facoltativo                  | Facoltativo                 | No                       |
| [Caricamenti Unordered Access View tipizzati](typed-unordered-access-view-loads.md)                                               | 18 formati, più facoltativi | 18 formati, più facoltativi | 3 formati, più facoltativi | 3 formati, più facoltativi |
| [Geometry shader](/previous-versions//bb205146(v=vs.85)) | Sì                       | Sì                       | Sì                      | Sì                      |
| [Flusso in uscita](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage)                                            | Sì                       | Sì                       | Sì                      | Sì                      |
| [DirectCompute/compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)                                  | Sì                       | Sì                       | Sì                      | Sì                      |
| [Hull e Domain shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                                           | Sì                       | Sì                       | Sì                      | Sì                      |
| [Matrici di risorse di trama](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Sì                       | Sì                       | Sì                      | Sì                      |
| [Matrici di risorse mappa cubi](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Sì                       | Sì                       | Sì                      | Sì                      |
| [Compressione da BC1 a BC7](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)                        | Sì                       | Sì                       | Sì                      | Sì                      |
| [Da Alpha a code coverage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state)         | Sì                       | Sì                       | Sì                      | Sì                      |
| [Operazioni logiche (Unione di output)](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                                          | Sì                       | Sì                       | sì                      | Facoltativo                 |
| Rasterizzazione indipendente dalla destinazione                                                                                         | Sì                       | Sì                       | Sì                      | No                       |
| [Destinazione di rendering multipla (MRT) con ForcedSampleCount 1](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                      | Sì                       | Sì                       | sì                      | Facoltativo                 |
| [Numero massimo di campioni forzati per il rendering con solo UAV](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                            | 16                        | 16                        | 16                       | 8                        |
| Dimensione di trama massima                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Dimensione max mappa cubi                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Extent volume massimo                                                                                                        | 2048                      | 2048                      | 2048                     | 2048                     |
| Ripetizione trama massima                                                                                                       | 16384                     | 16384                     | 16384                    | 16384                    |
| Anisotropia max                                                                                                           | 16                        | 16                        | 16                       | 16                       |
| Numero massimo primitive                                                                                                      | 2 ^ 32-1                  | 2 ^ 32-1                  | 2 ^ 32-1                 | 2 ^ 32-1                 |
| Numero massimo di vertex index                                                                                                         | 2 ^ 32-1                  | 2 ^ 32-1                  | 2 ^ 32-1                 | 2 ^ 32-1                 |
| Numero massimo di slot di input                                                                                                          | 32                        | 32                        | 32                       | 32                       |
| Destinazioni di rendering simultanee                                                                                              | 8                         | 8                         | 8                        | 8                        |
| Query di occlusione                                                                                                        | Sì                       | Sì                       | Sì                      | Sì                      |
| Blend Alpha separata                                                                                                     | Sì                       | Sì                       | Sì                      | Sì                      |
| Mirror una volta                                                                                                              | Sì                       | Sì                       | Sì                      | Sì                      |
| Elementi Vertex sovrapposti                                                                                              | Sì                       | Sì                       | Sì                      | Sì                      |
| Maschere di scrittura indipendenti                                                                                                  | Sì                       | Sì                       | Sì                      | Sì                      |
| Instancing                                                                                                               | Sì                       | Sì                       | Sì                      | Sì                      |



 

-   ⁰ richiede il runtime Direct3D 11,3 o Direct3D 12.
-   ¹ richiede il runtime Direct3D 11,1.
-   il modello di shader di ² 5,0 può supportare facoltativamente shader a precisione doppia, shader a precisione doppia estesa, l'istruzione **SAD4** shader e gli shader con precisione parziale. Per determinare le opzioni del modello di shader 5,0 disponibili, chiamare [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). Una certa compatibilità dipende dall'hardware in cui viene eseguito: il modello di shader 5,1 è supportato solo nell'hardware che supporta l'API DirectX 12, indipendentemente dal livello di funzionalità in uso. L'hardware DirectX 11 supporta solo fino al modello shader 5,0. L'API DirectX 12 passa solo al livello di funzionalità 11 \_ 0.
-   i livelli più elevati di ³ sono facoltativi.
-   I livelli di funzionalità 12 \_ 0 e 12 \_ 1 richiedono il runtime Direct3D 11,3 o Direct3D 12.
-   Il livello di funzionalità 11 \_ 1 richiede il runtime Direct3D 11,1.
-   Il livello di funzionalità 11 \_ 0 richiede il runtime Direct3D 11,0.

## <a name="hardware-support-for-dxgi-formats"></a>Supporto hardware per formati DXGI

Per visualizzare le tabelle dei formati DXGI e delle funzionalità hardware, fare riferimento a:

-   [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 12,1](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
-   [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 12,0](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
-   [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 11,1](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
-   [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 11,0](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
-   [Supporto hardware per i formati 10Level9 Direct3D](/previous-versions//ff471324(v=vs.85))
-   [Supporto hardware per formati Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
-   [Supporto hardware per i formati Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di query sulle funzionalità](capability-querying.md)
</dt> <dt>

[Informazioni su Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 
