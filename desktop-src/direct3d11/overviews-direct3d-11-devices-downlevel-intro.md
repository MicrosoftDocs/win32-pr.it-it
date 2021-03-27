---
title: Livelli di funzionalità Direct3D
description: In questo argomento vengono illustrati i livelli di funzionalità Direct3D.
ms.assetid: 5ad0525c-249f-452d-950b-df8fa2addde2
keywords:
- Livello di funzionalità DX
- Livello di funzionalità DirectX
- livello funzionalità, DX
- livello funzionalità, DirectX
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 82667a7a2e02d675185fd65c318aeed10db79844
ms.sourcegitcommit: 85bd7112570865dd2136e0d05bd0a4132e6313ec
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/02/2020
ms.locfileid: "104047503"
---
# <a name="direct3d-feature-levels"></a>Livelli di funzionalità Direct3D

Per gestire la diversità di schede video in computer nuovi ed esistenti, in Microsoft Direct3D 11 è stato introdotto il concetto di livelli di funzionalità. In questo argomento vengono illustrati i livelli di funzionalità Direct3D.

Ogni scheda video implementa un certo livello di funzionalità di Microsoft DirectX (DX), a seconda delle GPU (Graphics Processing Unit) installate. Nelle versioni precedenti di Microsoft Direct3D, era possibile individuare la versione di Direct3D in cui è stata implementata la scheda video e quindi programmare l'applicazione di conseguenza.

Con Direct3D 11, viene introdotto un nuovo paradigma denominato livelli di funzionalità. I livelli di funzionalità sono set ben definiti di funzionalità GPU, Ad esempio, il \_ livello di funzionalità di 9 1 implementa la funzionalità implementata in Microsoft Direct3D 9, che espone le funzionalità dei modelli shader [PS \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-x.md) e [vs \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-vs-2-x.md), mentre il \_ livello di funzionalità 11 0 implementa la funzionalità implementata in Direct3D 11.

A questo punto, quando si crea un dispositivo, è possibile provare a creare un dispositivo per il livello di funzionalità che si desidera richiedere. Se la creazione del dispositivo funziona, il livello di funzionalità esiste, in caso contrario, l'hardware non supporta tale livello di funzionalità. È possibile provare a ricreare un dispositivo a un livello di funzionalità inferiore oppure è possibile scegliere di uscire dall'applicazione. Per ulteriori informazioni sulla creazione di un dispositivo, vedere la funzione [**D3D11CreateDevice**](/windows/win32/api/D3D11/nf-d3d11-d3d11createdevice) .

Usando i livelli di funzionalità, è possibile sviluppare un'applicazione per Direct3D 9, Microsoft Direct3D 10 o Direct3D 11, quindi eseguirla su un hardware di 9, 10 o 11 (con alcune eccezioni. ad esempio, le nuove funzionalità 11 non verranno eseguite su una scheda 9 esistente). Di seguito sono riportate alcune altre proprietà di base dei livelli di funzionalità:

- Una GPU che consente la creazione di un dispositivo soddisfa o supera la funzionalità del livello di funzionalità.
- Un livello di funzionalità include sempre la funzionalità dei livelli di funzionalità precedenti o inferiori.
- Un livello di funzionalità non implica prestazioni, solo funzionalità. Le prestazioni dipendono dall'implementazione dell'hardware.
- Scegliere un livello di funzionalità quando si crea un dispositivo Direct3D 11.

Per informazioni sulle limitazioni della creazione di dispositivi di tipo non hardware a determinati livelli di funzionalità, vedere [limitazioni della creazione di dispositivi Warp e Reference](overviews-direct3d-11-devices-limitations.md).

Per semplificare la scelta del livello di funzionalità da progettare con, confrontare le funzionalità per ogni livello di funzionalità.

Nella sezione di [riferimento 10Level9](d3d11-graphics-reference-10level9.md) sono elencate le differenze tra il comportamento di diversi metodi [**ID3D11Device**](/windows/win32/api/D3D11/nn-d3d11-id3d11device) e [**sul ID3D11DeviceContext**](/windows/win32/api/D3D11/nn-d3d11-id3d11devicecontext) a diversi livelli di funzionalità di 10Level9.

## <a name="formats-of-version-numbers"></a>Formati dei numeri di versione

Sono disponibili tre formati per le versioni Direct3D, i modelli shader e i livelli di funzionalità.

- Nelle versioni Direct3D viene utilizzato un punto; ad esempio, Direct3D 12,0.
- I modelli shader utilizzano un punto; ad esempio, il modello di shader 5,1.
- I livelli di funzionalità usano un carattere di sottolineatura; ad esempio, il livello di funzionalità 12 \_ 0.

## <a name="feature-support-for-feature-levels-12_1-through-9_3"></a>Supporto delle funzionalità per i livelli di funzionalità 12_1 tramite 9_3

Sono disponibili le funzionalità seguenti per i livelli di funzionalità elencati. Le intestazioni nella riga superiore sono livelli di funzionalità Direct3D. Le intestazioni nella colonna a sinistra sono features. Vedere anche [le note a piè di pagina per le tabelle](#footnotes-for-the-tables).

| \\Livello funzionalità funzionalità | 12 \_ 1<sup>0</sup> | 12 \_ 0<sup>0</sup> | 11 \_ 1<sup>1</sup> | 11 \_ 0 | 10 \_ 1 | 10 \_ 0 | 9 \_ 3<sup>7</sup> |
|-|-|-|-|-|-|-|-|
| Modello shader (D3D11) | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 5,0<sup>2</sup> | 4.x | 4.0 | 2,0 (4 \_ 0 \_ livello \_ 9 \_ 3) \[ vs \_ 2 \_ a/PS \_ 2 \_ x \] <sup>5</sup> |
| Modello shader (D3D12) | 5,1<sup>2</sup> | 5,1<sup>2</sup> | 5,1<sup>2</sup> | 5,1<sup>2</sup> | N/D | N/D | N/D |
| [Risorse affiancate](tiled-resources.md) | Livello 2<sup>6</sup> | Livello 2<sup>6</sup> | Facoltativo | Facoltativo | No | No | No |
| [Rasterizzazione conservativa](conservative-rasterization.md) | Tier1<sup>6</sup> | Facoltativo | Facoltativo | No | No | No | No |
| [Visualizzazioni degli ordini di rasterizzatore](rasterizer-order-views.md) | sì | Facoltativo | Facoltativo | No | No | No | No |
| [Filtri min/max](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Sì | sì | Facoltativo | No | No | No | No |
| Buffer predefinito mappa | Facoltativo | Facoltativo | Facoltativo | Facoltativo | No | No | No |
| [Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md) | Facoltativo | Facoltativo | Facoltativo | No | No | No | No |
| Caricamenti Unordered Access View tipizzati | 18 formati, più facoltativi | 18 formati, più facoltativi | 3 formati, più facoltativi | 3 formati, più facoltativi | No | No | No |
| [Geometry shader](/previous-versions/bb205146(v=vs.85)) | Sì | Sì | Sì | Sì | Sì | Sì | No |
| [Flusso in uscita](./d3d10-graphics-programming-guide-output-stream-stage.md) | Sì | Sì | Sì | Sì | Sì | Sì | No |
| [DirectCompute/compute shader](direct3d-11-advanced-stages-compute-shader.md) | Sì | Sì | Sì | sì | Facoltativo | Facoltativo | N/D |
| <b>\\Livello funzionalità funzionalità</b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| [Hull e Domain shader](direct3d-11-advanced-stages-tessellation.md) | Sì | Sì | Sì | Sì | No | No | No |
| [Matrici di risorse di trama](overviews-direct3d-11-resources-textures-intro.md) | Sì | Sì | Sì | Sì | Sì | Sì | No |
| [Matrici di risorse mappa cubi](overviews-direct3d-11-resources-textures-intro.md) | Sì | Sì | Sì | Sì | Sì | No | No |
| [Compressione BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Sì | Sì | Sì | Sì | Sì | Sì | No |
| [Compressione BC6H/BC7](texture-block-compression-in-direct3d-11.md) | Sì | Sì | Sì | Sì | No | No | No |
| [Da Alpha a code coverage](./d3d10-graphics-programming-guide-blend-state.md) | Sì | Sì | Sì | Sì | Sì | Sì | No |
| [Formati estesi (BGRA e così via)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sì | Sì | Sì | sì | Facoltativo | Facoltativo | Sì |
| [Formato High Color 10 bit XR](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sì | Sì | Sì | sì | Facoltativo | Facoltativo | N/D |
| [Operazioni logiche (Unione di output)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Sì | Sì | Sì | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | No |
| Rasterizzazione indipendente dalla destinazione | Sì | Sì | Sì | No | No | No | No |
| [Destinazione di rendering multipla (MRT) con ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Sì | Sì | Sì | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | No |
| Slot UAV | 64 | 64 | 64 | 8 | 1 | 1 | N/D |
| <b>\\Livello funzionalità funzionalità</b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| UAV in ogni fase | Sì | Sì | Sì | No | No | No | N/D |
| [Numero massimo di campioni forzati per il rendering con solo UAV](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 16 | 16 | 16 | 8 | N/D | N/D | N/D |
| Offset del buffer costante e aggiornamenti parziali | Sì | Sì | Sì | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | Sì<sup>1</sup> |
| formati a 16 bit per pixel (BPP) | Sì | Sì | Sì | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> |
| Dimensione di trama massima | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Dimensione max mappa cubi | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Extent volume massimo | 2048 | 2048 | 2048 | 2048 | 2048 | 2048 | 256 |
| Ripetizione trama massima | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 8192 |
| Anisotropia max | 16 | 16 | 16 | 16 | 16 | 16 | 16 |
| Numero massimo primitive | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 1048575 |
| Numero massimo di vertex index | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 2 ^ 32-1 | 1048575 |
| Numero massimo di slot di input | 32 | 32 | 32 | 32 | 32 | 16 | 16 |
| Destinazioni di rendering simultanee | 8 | 8 | 8 | 8 | 8 | 8 | 4 |
| Query di occlusione | Sì | Sì | Sì | Sì | Sì | Sì | Sì |
| <b>\\Livello funzionalità funzionalità</b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| Blend Alpha separata | Sì | Sì | Sì | Sì | Sì | Sì | Sì |
| Mirror una volta | Sì | Sì | Sì | Sì | Sì | Sì | Sì |
| Elementi Vertex sovrapposti | Sì | Sì | Sì | Sì | Sì | Sì | Sì |
| Maschere di scrittura indipendenti | Sì | Sì | Sì | Sì | Sì | Sì | Sì |
| Instancing | Sì | Sì | Sì | Sì | Sì | Sì | Sì<sup>7</sup> |
| Non alimentatori-di-2 in modo condizionale<sup>3</sup> | No | No | No | No | No | No | Sì |
| Non alimentatori-di-2 in modo non condizionale<sup>4</sup> | Sì | Sì | Sì | Sì | Sì | Sì | No |

## <a name="feature-support-for-feature-levels-9_2-and-9_1"></a>Supporto delle funzionalità per i livelli di funzionalità 9_2 e 9_1

Sono disponibili le funzionalità seguenti per i livelli di funzionalità elencati. Le intestazioni nella riga superiore sono livelli di funzionalità Direct3D. Le intestazioni nella colonna a sinistra sono features. Vedere anche [le note a piè di pagina per le tabelle](#footnotes-for-the-tables).

| \\Livello funzionalità funzionalità | 9 \_ 2 | 9 \_ 1 |
|-|-|-|
| Modello shader (D3D11) | 2,0 (4 \_ 0 \_ livello \_ 9 \_ 1) | 2,0 (4 \_ 0 \_ livello \_ 9 \_ 1) |
| Modello shader (D3D12) | N/D | N/D |
| [Risorse affiancate](tiled-resources.md) | No | No |
| [Rasterizzazione conservativa](conservative-rasterization.md) | No | No |
| [Visualizzazioni degli ordini di rasterizzatore](rasterizer-order-views.md) | No | No |
| [Filtri min/max](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | No | No |
| Buffer predefinito mappa | No | No |
| [Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md) | No | No |
| Caricamenti Unordered Access View tipizzati | No | No |
| [Geometry shader](/previous-versions/bb205146(v=vs.85)) | No | No |
| [Flusso in uscita](./d3d10-graphics-programming-guide-output-stream-stage.md) | No | No |
| [DirectCompute/compute shader](direct3d-11-advanced-stages-compute-shader.md) | N/D | N/D |
| [Hull e Domain shader](direct3d-11-advanced-stages-tessellation.md) | No | No |
| [Matrici di risorse di trama](overviews-direct3d-11-resources-textures-intro.md) | No | No |
| [Matrici di risorse mappa cubi](overviews-direct3d-11-resources-textures-intro.md) | No | No |
| [Compressione BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | No | No |
| <b>\\Livello funzionalità funzionalità</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| [Compressione BC6H/BC7](texture-block-compression-in-direct3d-11.md) | No | No |
| [Da Alpha a code coverage](./d3d10-graphics-programming-guide-blend-state.md) | No | No |
| [Formati estesi (BGRA e così via)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sì | Sì |
| [Formato High Color 10 bit XR](overviews-direct3d-11-devices-downlevel-exceptions.md) | N/D | N/D |
| [Operazioni logiche (Unione di output)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | No | No |
| Rasterizzazione indipendente dalla destinazione | No | No |
| [Destinazione di rendering multipla (MRT) con ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | No | No |
| Slot UAV | N/D | N/D |
| UAV in ogni fase | N/D | N/D |
| [Numero massimo di campioni forzati per il rendering con solo UAV](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | N/D | N/D |
| Offset del buffer costante e aggiornamenti parziali | Sì<sup>1</sup> | Sì<sup>1</sup> |
| formati a 16 bit per pixel (BPP) | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> |
| Dimensione di trama massima | 2048 | 2048 |
| Dimensione max mappa cubi | 512 | 512 |
| Extent volume massimo | 256 | 256 |
| Ripetizione trama massima | 2048 | 128 |
| <b>\\Livello funzionalità funzionalità</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| Anisotropia max | 16 | 2 |
| Numero massimo primitive | 1048575 | 65535 |
| Numero massimo di vertex index | 1048575 | 65534 |
| Numero massimo di slot di input | 16 | 16 |
| Destinazioni di rendering simultanee | 1 | 1 |
| Query di occlusione | Sì | No |
| Blend Alpha separata | Sì | No |
| Mirror una volta | Sì | No |
| Elementi Vertex sovrapposti | Sì | No |
| Maschere di scrittura indipendenti | No | No |
| Instancing | No | No |
| Non alimentatori-di-2 in modo condizionale<sup>3</sup> | Sì | Sì |
| Non alimentatori-di-2 in modo non condizionale<sup>4</sup> | No | No |

## <a name="footnotes-for-the-tables"></a>Note a piè di pagina per le tabelle

<sup>0</sup> richiede il runtime Direct3D 11,3 o Direct3D 12.

<sup>1</sup> richiede il runtime Direct3D 11,1.

<sup>2</sup> il modello di shader 5,0 e versioni successive può supportare facoltativamente gli shader a precisione doppia, gli shader a precisione doppia estesi, l'istruzione **SAD4** shader e gli shader con precisione parziale. Per determinare le opzioni del modello shader 5,0 disponibili per DirectX 11, chiamare [**ID3D11Device:: CheckFeatureSupport**](/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Una certa compatibilità dipende dall'hardware in cui viene eseguito. Il modello di shader 5,1 e versioni successive sono supportati solo tramite l'API DirectX 12, indipendentemente dal livello di funzionalità in uso. DirectX 11 supporta solo fino al modello shader 5,0. L'API DirectX 12 passa solo al livello di funzionalità 11 \_ 0.

<sup>3</sup> a livello di funzionalità 9 \_ 1, 9 \_ 2 e 9 \_ 3, il dispositivo di visualizzazione supporta l'uso di trame 2D con dimensioni che non sono potenze di due in due condizioni. In primo luogo, è possibile creare solo un livello MIP-map per ogni trama e, in secondo luogo, non sono consentite modalità di campionamento a capo per le trame, ovvero i membri **Address**, **AddressV** e **AddressW** di [**d3d11 \_ Sampler \_ desc**](/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc) non possono essere impostati su [**d3d11 \_ texture \_ Address \_ Wrap**](/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode).

<sup>4</sup> a livello di funzionalità 10 \_ 0, 10 \_ 1 e 11 \_ 0, il dispositivo di visualizzazione supporta in modo incondizionato l'uso di trame 2D con dimensioni che non sono potenze di due.

<sup>5</sup> vertex shader 2a con istruzioni 256, 32 registri temporanei, controllo del flusso statico di profondità 4, controllo dinamico del flusso di profondità 24 e D3DVS20CAPS \_ predicazione. Pixel shader 2x con istruzioni 512, 32 registri temporanei, controllo del flusso statico di profondità 4, controllo dinamico del flusso di profondità 24, D3DPS20CAPS \_ ARBITRARYSWIZZLE, D3DPS20CAPS \_ GRADIENTINSTRUCTIONS, D3DPS20CAPS \_ predicazione, D3DPS20CAPS NODEPENDENTREADLIMIT \_ e D3DPS20CAPS NOTEXINSTRUCTIONLIMIT \_ .

<sup>6</sup> livelli superiori facoltativi.

<sup>7</sup> per 9_3 a livello di funzionalità, gli unici metodi di rendering **supportati sono,** **DrawIndexed** e **DrawIndexInstanced**. Anche per il livello di funzionalità 9_3, il rendering dell'elenco di punti è supportato solo per il rendering tramite il metodo di **estrazione**.

Per informazioni dettagliate sul supporto del formato a diversi livelli di funzionalità hardware, vedere:

- [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 12,1](../direct3ddxgi/hardware-support-for-direct3d-12-1-formats.md)
- [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 12,0](../direct3ddxgi/hardware-support-for-direct3d-12-0-formats.md)
- [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 11,1](../direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware.md)
- [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 11,0](../direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware.md)
- [Supporto hardware per i formati 10Level9 Direct3D](/previous-versions/ff471324(v=vs.85))
- [Supporto hardware per formati Direct3D 10,1](/previous-versions/cc627091(v=vs.85))
- [Supporto hardware per i formati Direct3D 10](/previous-versions/cc627090(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

* [Direct3D 11 su hardware di livello inferiore](overviews-direct3d-11-devices-downlevel.md)
* [Livelli di funzionalità hardware (Direct3D 12)](../direct3d12/hardware-feature-levels.md)
