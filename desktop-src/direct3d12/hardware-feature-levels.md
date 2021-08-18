---
title: Livelli di funzionalità hardware
description: Descrive le funzionalità dei livelli di funzionalità hardware da \_ 11 a 12 \_ 1.
ms.assetid: B8304E29-A532-464E-8FAF-075228D8FB73
keywords:
- Livello di funzionalità DX
- Livello di funzionalità DirectX
- livello di funzionalità, DX
- livello di funzionalità, DirectX
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf069baca3d9ff56c0d3d98e79bb553df7e8acf1fadf7b5888c5b5d211f7a874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124149"
---
# <a name="hardware-feature-levels"></a>Livelli di funzionalità hardware

Descrive le funzionalità dei livelli di funzionalità hardware da \_ 11 a 12 \_ 1.

-   [Sistemi di numerazione](#numbering-systems)
-   [Supporto a livello di funzionalità](#feature-level-support)
-   [Supporto hardware per i formati DXGI](#hardware-support-for-dxgi-formats)
-   [Argomenti correlati](#related-topics)

Per gestire la diversità delle schede video in computer nuovi ed esistenti, Microsoft Direct3D 11 ha introdotto il concetto di livelli di funzionalità. Ogni scheda video implementa un determinato livello di funzionalità Microsoft DirectX (DX) a seconda delle unità di elaborazione grafica (GPU) installate. Un livello di funzionalità è un set ben definito di funzionalità GPU. Ad esempio, il livello di funzionalità 11 0 implementa \_ la funzionalità implementata in Direct3D 11.

A questo punto, quando si crea un dispositivo, è possibile provare a creare un dispositivo per il livello di funzionalità che si vuole richiedere. Se la creazione del dispositivo funziona, tale livello di funzionalità esiste, in caso contrario, l'hardware non supporta tale livello di funzionalità. È possibile provare a ricreare un dispositivo a un livello di funzionalità inferiore oppure è possibile scegliere di uscire dall'applicazione.

Le proprietà di base dei livelli di funzionalità sono:

-   Tutti i driver Direct3D 12 saranno di livello funzionalità 11 \_ 0 o superiore.
-   Una GPU che consente la creazione di un dispositivo soddisfa o supera la funzionalità di tale livello di funzionalità.
-   Un livello di funzionalità include sempre le funzionalità dei livelli di funzionalità precedenti o inferiori.
-   Un livello di funzionalità non implica prestazioni, ma solo funzionalità. Le prestazioni dipendono dall'implementazione dell'hardware.
-   Un livello di funzionalità viene scelto quando si chiama [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice).
-   Per informazioni più dettagliate sulle funzionalità  supportate(in particolare quelle contrassegnate come Facoltativo nella tabella seguente, il che significa che l'hardware potrebbe supportare la funzionalità ma non è necessario) chiamare [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Per informazioni sulle limitazioni relative alla creazione di dispositivi di tipo non hardware in determinati livelli di funzionalità, vedere Limitazioni relative alla creazione di [dispositivi WARP e di riferimento.](/windows/desktop/direct3d11/overviews-direct3d-11-devices-limitations) Per altre informazioni sull'introduzione dei livelli di funzionalità, vedere la documentazione di Direct3D 11 sui [livelli di funzionalità Direct3D.](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)

## <a name="numbering-systems"></a>Sistemi di numerazione

I livelli di funzionalità hardware *non sono* uguali alle versioni dell'API. Ad esempio, è presente un'API D3D11.3, ma non esiste alcun livello di funzionalità \_ hardware 11 3. I livelli di funzionalità sono definiti [**nell'enumerazione D3D \_ FEATURE \_ LEVEL.**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)

Esistono tre sistemi di numerazione distinti:

-   Le versioni Direct3D usano un punto. ad esempio Direct3D 12.0.
-   I modelli shader usano un punto; ad esempio, modello shader 5.1.
-   I livelli di funzionalità usano un carattere di sottolineatura; ad esempio, livello di funzionalità 12 \_ 0.

## <a name="feature-level-support"></a>Supporto a livello di funzionalità

Per ogni livello di funzionalità Direct3D sono disponibili le funzionalità seguenti.

Le intestazioni nella riga superiore sono livelli di funzionalità Direct3D. Le intestazioni nella colonna a sinistra sono caratteristiche.



| Livello \\ di funzionalità                                                                                                 | 12 \_ 1⁰                    | 12 \_ 0⁰                    | 11 \_ 1¹                   | 11 \_ 0                    |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------|---------------------------|--------------------------|--------------------------|
| Modello di shader                                                                                                             | 5.1                       | 5.1                       | 5.1²                     | 5.1²                     |
| [Livello di associazione delle risorse](hardware-support.md)                                                                            | Livello 2-                    | Livello 2-                    | Livello 1-                   | Livello 1-                   |
| [Risorse affiancate](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)                                                                        | Livello 2-                    | Livello 2-                    | Facoltativo                 | Facoltativo                 |
| [Rasterizzazione conservativa](conservative-rasterization.md)                                                             | Livello 1-                    | Facoltativo                  | Facoltativo                 | No                       |
| [Visualizzazioni ordinate del rasterizzatore](rasterizer-order-views.md)                                                                   | sì                       | Facoltativo                  | Facoltativo                 | No                       |
| [Filtri minimi/massimi](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)                                                                                      | Sì                       | sì                       | Facoltativo                 | No                       |
| Eseguire il mapping del buffer predefinito                                                                                                       | Facoltativo                  | Facoltativo                  | Facoltativo                 | Facoltativo                 |
| [Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md)                                 | Facoltativo                  | Facoltativo                  | Facoltativo                 | No                       |
| [Carichi Unordered Access View tipi](typed-unordered-access-view-loads.md)                                               | 18 formati, più facoltativi | 18 formati, più facoltativi | 3 formati, più facoltativi | 3 formati, più facoltativi |
| [Geometry shader](/previous-versions//bb205146(v=vs.85)) | Sì                       | Sì                       | Sì                      | Sì                      |
| [Flusso in uscita](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage)                                            | Sì                       | Sì                       | Sì                      | Sì                      |
| [DirectCompute/Compute Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)                                  | Sì                       | Sì                       | Sì                      | Sì                      |
| [Shader della base e del dominio](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                                           | Sì                       | Sì                       | Sì                      | Sì                      |
| [Matrici di risorse texture](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Sì                       | Sì                       | Sì                      | Sì                      |
| [Matrici di risorse di mappe cubi](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Sì                       | Sì                       | Sì                      | Sì                      |
| [Compressione da BC1 a BC7](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)                        | Sì                       | Sì                       | Sì                      | Sì                      |
| [Alpha-to-coverage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state)         | Sì                       | Sì                       | Sì                      | Sì                      |
| [Operazioni logiche (unione output)](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                                          | Sì                       | Sì                       | sì                      | Facoltativo                 |
| Rasterizzazione indipendente dalla destinazione                                                                                         | Sì                       | Sì                       | Sì                      | No                       |
| [Destinazione di rendering multipla (MRT) con ForcedSampleCount 1](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                      | Sì                       | Sì                       | sì                      | Facoltativo                 |
| [Numero massimo di campioni forzati per il rendering solo UAV](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                            | 16                        | 16                        | 16                       | 8                        |
| Dimensione massima trama                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Dimensione Max Cubemap                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Extent massimo volume                                                                                                        | 2048                      | 2048                      | 2048                     | 2048                     |
| Max Texture Repeat                                                                                                       | 16384                     | 16384                     | 16384                    | 16384                    |
| Max Anisotropy                                                                                                           | 16                        | 16                        | 16                       | 16                       |
| Numero massimo di primitive                                                                                                      | 2^32 – 1                  | 2^32 – 1                  | 2^32 – 1                 | 2^32 – 1                 |
| Max Vertex Index                                                                                                         | 2^32 – 1                  | 2^32 – 1                  | 2^32 – 1                 | 2^32 – 1                 |
| Numero massimo di slot di input                                                                                                          | 32                        | 32                        | 32                       | 32                       |
| Destinazioni di rendering simultanee                                                                                              | 8                         | 8                         | 8                        | 8                        |
| Query di occlusione                                                                                                        | Sì                       | Sì                       | Sì                      | Sì                      |
| Alpha Blend separato                                                                                                     | Sì                       | Sì                       | Sì                      | Sì                      |
| Eseguire il mirroring una sola volta                                                                                                              | Sì                       | Sì                       | Sì                      | Sì                      |
| Elementi vertici sovrapposti                                                                                              | Sì                       | Sì                       | Sì                      | Sì                      |
| Maschere di scrittura indipendenti                                                                                                  | Sì                       | Sì                       | Sì                      | Sì                      |
| Instancing                                                                                                               | Sì                       | Sì                       | Sì                      | Sì                      |



 

-   ⁰ richiede il runtime Direct3D 11.3 o Direct3D 12.
-   PIÙ Richiede il runtime Direct3D 11.1.
-   Il modello di shader 5.0 può facoltativamente supportare shader a precisione doppia, shader a doppia precisione estesi, l'istruzione **sad4** shader e shader a precisione parziale. Per determinare le opzioni del modello shader 5.0 disponibili, chiamare [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). La compatibilità dipende dall'hardware in esecuzione: il modello shader 5.1 è supportato solo su hardware che supporta l'API DirectX 12, indipendentemente dal livello di funzionalità in uso. L'hardware DirectX 11 supporta solo fino al modello shader 5.0. L'API DirectX 12 passa solo al livello di funzionalità 11 \_ 0.
-   I livelli superiori sono facoltativi.
-   I livelli di funzionalità 12 0 e \_ 12 1 richiedono \_ il runtime Direct3D 11.3 o Direct3D 12.
-   Il livello di funzionalità \_ 11 1 richiede il runtime Direct3D 11.1.
-   Il livello di funzionalità \_ 11 0 richiede il runtime Direct3D 11.0.

## <a name="hardware-support-for-dxgi-formats"></a>Supporto hardware per i formati DXGI

Per visualizzare le tabelle dei formati DXGI e delle funzionalità hardware, vedere:

-   [Supporto del formato DXGI per l'hardware Direct3D Feature Level 12.1](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
-   [Supporto del formato DXGI per l'hardware Direct3D a livello di funzionalità 12.0](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
-   [Supporto del formato DXGI per l'hardware Direct3D Feature Level 11.1](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
-   [Supporto del formato DXGI per l'hardware Direct3D a livello di funzionalità 11.0](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
-   [Supporto hardware per formati Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
-   [Supporto hardware per i formati Direct3D 10.1](/previous-versions//cc627091(v=vs.85))
-   [Supporto hardware per i formati Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di query sulla funzionalità](capability-querying.md)
</dt> <dt>

[Informazioni su Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 
