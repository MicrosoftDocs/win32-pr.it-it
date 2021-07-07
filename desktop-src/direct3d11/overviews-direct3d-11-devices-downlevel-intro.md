---
title: Livelli di funzionalità Direct3D
description: Questo argomento illustra i livelli di funzionalità Direct3D.
ms.assetid: 5ad0525c-249f-452d-950b-df8fa2addde2
keywords:
- Livello di funzionalità DX
- Livello di funzionalità DirectX
- livello di funzionalità, DX
- livello di funzionalità, DirectX
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 9c4717d743e50e91376e57e5d13acbe2cfae41d8
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282470"
---
# <a name="direct3d-feature-levels"></a>Livelli di funzionalità Direct3D

> [!NOTE]
> **Alcune informazioni sono relative a un prodotto non definitivo, che potrebbe subire modifiche sostanziali prima del rilascio sul mercato. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.**

Per gestire la diversità delle schede video in computer nuovi ed esistenti, Microsoft Direct3D 11 introduce il concetto di livelli di funzionalità. Questo argomento illustra i livelli di funzionalità Direct3D.

Ogni scheda video implementa un determinato livello di funzionalità Microsoft DirectX (DX) a seconda delle GPU installate. Nelle versioni precedenti di Microsoft Direct3D era possibile trovare la versione di Direct3D implementata dalla scheda video e quindi programmare l'applicazione di conseguenza.

Con Direct3D 11, è stato introdotto un nuovo paradigma denominato livelli di funzionalità. I livelli di funzionalità sono set ben definiti di funzionalità GPU, Ad esempio, il livello di funzionalità 9 1 implementa la funzionalità implementata in Microsoft Direct3D 9, che espone le funzionalità dei modelli \_ di shader ps [ \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-x.md) e [vs \_ 2 \_ x](../direct3dhlsl/dx9-graphics-reference-asm-vs-2-x.md), mentre il livello di funzionalità 11 0 implementa la funzionalità implementata \_ in Direct3D 11.

A questo punto, quando si crea un dispositivo, è possibile provare a creare un dispositivo per il livello di funzionalità che si vuole richiedere. Se la creazione del dispositivo funziona, tale livello di funzionalità esiste; in caso contrario, l'hardware non supporta tale livello di funzionalità. È possibile provare a ricreare un dispositivo a un livello di funzionalità inferiore oppure è possibile scegliere di uscire dall'applicazione. Per altre informazioni sulla creazione di un dispositivo, vedi la [**funzione D3D11CreateDevice.**](/windows/win32/api/D3D11/nf-d3d11-d3d11createdevice)

Usando i livelli di funzionalità, è possibile sviluppare un'applicazione per Direct3D 9, Microsoft Direct3D 10 o Direct3D 11 e quindi eseguirla su hardware 9, 10 o 11 (con alcune eccezioni, ad esempio, le nuove 11 funzionalità non verranno eseguite in una scheda 9 esistente). Ecco un paio di altre proprietà di base dei livelli di funzionalità:

- Una GPU che consente la creazione di un dispositivo soddisfa o supera le funzionalità di tale livello di funzionalità.
- Un livello di funzionalità include sempre la funzionalità dei livelli di funzionalità precedenti o inferiori.
- Un livello di funzionalità non implica prestazioni, ma solo funzionalità. Le prestazioni dipendono dall'implementazione dell'hardware.
- Scegliere un livello di funzionalità quando si crea un dispositivo Direct3D 11.

Per informazioni sulle limitazioni per la creazione di dispositivi di tipo nonhardware in determinati livelli di funzionalità, vedere Limitazioni di creazione [di dispositivi WARP e di riferimento.](overviews-direct3d-11-devices-limitations.md)

Per facilitare la scelta del livello di funzionalità con cui progettare, confrontare le funzionalità per ogni livello di funzionalità.

La sezione 10Level9 Reference (Informazioni di riferimento su [10Level9)](d3d11-graphics-reference-10level9.md) elenca le differenze tra il comportamento dei vari metodi [**ID3D11Device**](/windows/win32/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/win32/api/D3D11/nn-d3d11-id3d11devicecontext) a vari livelli di funzionalità 10Level9.

## <a name="formats-of-version-numbers"></a>Formati dei numeri di versione

Sono disponibili tre formati per le versioni di Direct3D, i modelli di shader e i livelli di funzionalità.

- Le versioni direct3D usano un punto; ad esempio Direct3D 12.0.
- I modelli shader usano un punto. ad esempio, il modello shader 5.1.
- I livelli di funzionalità usano un carattere di sottolineatura. ad esempio il livello di funzionalità 12 \_ 0.

## <a name="feature-support-for-feature-levels-12_2-through-9_3"></a>Supporto delle funzionalità per i livelli di funzionalità da 12_2 a 9_3

Per i livelli di funzionalità elencati sono disponibili le funzionalità seguenti. Le intestazioni nella riga superiore sono livelli di funzionalità Direct3D. Le intestazioni nella colonna a sinistra sono caratteristiche. Vedere anche [Note a piè di pagina per le tabelle](#footnotes-for-the-tables).

| Livello \\ di funzionalità | 12 \_ 2<sup>8</sup> | 12 \_ 1<sup>0</sup> | 12 \_ 0<sup>0</sup> | 11 \_ 1<sup>1</sup> | 11 \_ 0 | 10 \_ 1 | 10 \_ 0 | 9 \_ 3<sup>7</sup> |
|-|-|-|-|-|-|-|-|-|
| Modello shader (D3D11) | N/D | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 5.0<sup>2</sup> | 4.x | 4.0 | 2.0 (4 \_ 0 \_ livello \_ 9 \_ 3) \[ rispetto a \_ 2 \_ a/ps \_ 2 x \_ \] <sup>5</sup> |
| Modello shader (D3D12) | 6.5 | 5.1<sup>2</sup> | 5.1<sup>2</sup> | 5.1<sup>2</sup> | 5.1<sup>2</sup> | N/D | N/D | N/D |
| [Risorse affiancate](tiled-resources.md) | Livello 3 | Livello<sup>2 6</sup> | Livello<sup>2 6</sup> | Facoltativo | Facoltativo | No | No | No |
| [Rasterizzazione conservativa](conservative-rasterization.md) | Livello 3 | Livello<sup>1 6</sup> | Facoltativo | Facoltativo | No | No | No | No |
| [Visualizzazioni degli ordini di rasterizzazione](rasterizer-order-views.md) | Sì | sì | Facoltativo | Facoltativo | No | No | No | No |
| [Filtri min/max](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | Sì | Sì | sì | Facoltativo | No | No | No | No |
| Eseguire il mapping del buffer predefinito | N/D | Facoltativo | Facoltativo | Facoltativo | Facoltativo | No | No | No |
| [Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md) | Facoltativo | Facoltativo | Facoltativo | Facoltativo | No | No | No | No |
| Caricamenti Unordered Access View tipi | 18 formati, più facoltativi | 18 formati, più facoltativi | 18 formati, più facoltativi | 3 formati, più facoltativi | 3 formati, più facoltativi | No | No | No |
| [Geometry shader](/previous-versions/bb205146(v=vs.85)) | Sì | Sì | Sì | Sì | Sì | Sì | Sì | No |
| [Flusso in uscita](./d3d10-graphics-programming-guide-output-stream-stage.md) | Sì | Sì | Sì | Sì | Sì | Sì | Sì | No |
| [DirectCompute/Compute Shader](direct3d-11-advanced-stages-compute-shader.md) | Sì | Sì | Sì | Sì | sì | Facoltativo | Facoltativo | N/D |
| <b>Livello \\ di funzionalità</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| [Shader della base e del dominio](direct3d-11-advanced-stages-tessellation.md) | Sì | Sì | Sì | Sì | Sì | No | No | No |
| [Matrici di risorse texture](overviews-direct3d-11-resources-textures-intro.md) | Sì | Sì | Sì | Sì | Sì | Sì | Sì | No |
| [Matrici di risorse della mappa cubi](overviews-direct3d-11-resources-textures-intro.md) | Sì | Sì | Sì | Sì | Sì | Sì | No | No |
| [Compressione BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | Sì | Sì | Sì | Sì | Sì | Sì | Sì | No |
| [Compressione BC6H/BC7](texture-block-compression-in-direct3d-11.md) | Sì | Sì | Sì | Sì | Sì | No | No | No |
| [Alpha-to-coverage](./d3d10-graphics-programming-guide-blend-state.md) | Sì | Sì | Sì | Sì | Sì | Sì | Sì | No |
| [Formati estesi (BGRA e così via)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sì | Sì | Sì | Sì | sì | Facoltativo | Facoltativo | Sì |
| [Formato High Color 10 bit XR](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sì | Sì | Sì | Sì | sì | Facoltativo | Facoltativo | N/D |
| [Operazioni per la logica (output merger)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Sì | Sì | Sì | Sì | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | No |
| Rasterizzazione indipendente dalla destinazione | Sì | Sì | Sì | Sì | No | No | No | No |
| [Più destinazione di rendering (MRT) con ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | Sì | Sì | Sì | Sì | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | No |
| Slot UAV | Livelli<sup>9</sup> | 64 | 64 | 64 | 8 | 1 | 1 | N/D |
| <b>Livello \\ di funzionalità</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1 1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| UAV in ogni fase | Sì | Sì | Sì | Sì | No | No | No | N/D |
| [Numero massimo di campioni forzati per il rendering solo UAV](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | 16 | 16 | 16 | 16 | 8 | N/D | N/D | N/D |
| Offset del buffer costante e aggiornamenti parziali | Sì | Sì | Sì | Sì | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | Sì<sup>1</sup> |
| Formati a 16 bit per pixel (bpp) | Sì | Sì | Sì | Sì | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> |
| Dimensione massima trama | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Dimensione Max Cubemap | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 4096 |
| Extent massimo volume | 2048 | 2048 | 2048 | 2048 | 2048 | 2048 | 2048 | 256 |
| Ripetizione massima trame | 16384 | 16384 | 16384 | 16384 | 16384 | 8192 | 8192 | 8192 |
| Max Anisotropy | 16 | 16 | 16 | 16 | 16 | 16 | 16 | 16 |
| Numero massimo primitive | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 1048575 |
| Indice massimo vertici | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 2^32 – 1 | 1048575 |
| Numero massimo di slot di input | 32 | 32 | 32 | 32 | 32 | 32 | 16 | 16 |
| Destinazioni di rendering simultanee | 8 | 8 | 8 | 8 | 8 | 8 | 8 | 4 |
| Query di occlusione | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì |
| <b>Livello \\ di funzionalità</b> | <b>12 \_ 2<sup>8</sup></b> | <b>12 \_ 1<sup>0</sup></b> | <b>12 \_ 0<sup>0</sup></b> | <b>11 \_ 1<sup>1</sup></b> | <b>11 \_ 0</b> | <b>10 \_ 1</b> | <b>10 \_ 0</b> | <b>9 \_ 3<sup>7</sup></b> |
| Alpha Blend separato | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì |
| Eseguire il mirroring una sola volta | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì |
| Elementi vertici sovrapposti | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì |
| Maschere di scrittura indipendenti | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì |
| Instancing | Sì | Sì | Sì | Sì | Sì | Sì | Sì | Sì<sup>7</sup> |
| Nonpowers-of-2 in modo condizionale<sup>3</sup> | No | No | No | No | No | No | No | Sì |
| Nonpowers-of-2 incondizionatamente<sup>4</sup> | Sì | Sì | Sì | Sì | Sì | Sì | Sì | No |

## <a name="feature-support-for-feature-levels-9_2-and-9_1"></a>Supporto delle funzionalità per i livelli di funzionalità 9_2 e 9_1

Per i livelli di funzionalità elencati sono disponibili le funzionalità seguenti. Le intestazioni nella riga superiore sono livelli di funzionalità Direct3D. Le intestazioni nella colonna a sinistra sono caratteristiche. Vedere anche [Note a piè di pagina per le tabelle](#footnotes-for-the-tables).

| Livello \\ di funzionalità | 9 \_ 2 | 9 \_ 1 |
|-|-|-|
| Modello shader (D3D11) | 2.0 (4 \_ 0 \_ livello \_ 9 \_ 1) | 2.0 (4 \_ 0 \_ livello \_ 9 \_ 1) |
| Modello shader (D3D12) | N/D | N/D |
| [Risorse affiancate](tiled-resources.md) | No | No |
| [Rasterizzazione conservativa](conservative-rasterization.md) | No | No |
| [Visualizzazioni degli ordini di rasterizzazione](rasterizer-order-views.md) | No | No |
| [Filtri min/max](/windows/win32/api/D3D11/ne-d3d11-d3d11_filter) | No | No |
| Eseguire il mapping del buffer predefinito | No | No |
| [Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md) | No | No |
| Caricamenti Unordered Access View tipi | No | No |
| [Geometry shader](/previous-versions/bb205146(v=vs.85)) | No | No |
| [Flusso in uscita](./d3d10-graphics-programming-guide-output-stream-stage.md) | No | No |
| [DirectCompute/Compute Shader](direct3d-11-advanced-stages-compute-shader.md) | N/D | N/D |
| [Shader della base e del dominio](direct3d-11-advanced-stages-tessellation.md) | No | No |
| [Matrici di risorse texture](overviews-direct3d-11-resources-textures-intro.md) | No | No |
| [Matrici di risorse della mappa cubi](overviews-direct3d-11-resources-textures-intro.md) | No | No |
| [Compressione BC4/BC5](../direct3d10/d3d10-graphics-programming-guide-resources-block-compression.md) | No | No |
| <b>Livello \\ di funzionalità</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| [Compressione BC6H/BC7](texture-block-compression-in-direct3d-11.md) | No | No |
| [Alpha-to-coverage](./d3d10-graphics-programming-guide-blend-state.md) | No | No |
| [Formati estesi (BGRA e così via)](overviews-direct3d-11-devices-downlevel-exceptions.md) | Sì | Sì |
| [Formato High Color 10 bit XR](overviews-direct3d-11-devices-downlevel-exceptions.md) | N/D | N/D |
| [Operazioni logiche (unione output)](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | No | No |
| Rasterizzazione indipendente dalla destinazione | No | No |
| [Destinazione di rendering multipla (MRT) con ForcedSampleCount 1](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | No | No |
| Slot UAV | N/D | N/D |
| UAV in ogni fase | N/D | N/D |
| [Numero massimo di campioni forzati per il rendering solo UAV](/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) | N/D | N/D |
| Offset costante del buffer e aggiornamenti parziali | Sì<sup>1</sup> | Sì<sup>1</sup> |
| Formati a 16 bit per pixel (bpp) | Facoltativo<sup>1</sup> | Facoltativo<sup>1</sup> |
| Dimensione massima trama | 2048 | 2048 |
| Dimensione Max Cubemap | 512 | 512 |
| Extent massimo volume | 256 | 256 |
| Max Texture Repeat | 2048 | 128 |
| <b>Livello \\ di funzionalità</b> | <b>9 \_ 2</b> | <b>9 \_ 1</b> |
| Max Anisotropy | 16 | 2 |
| Numero massimo di primitive | 1048575 | 65535 |
| Max Vertex Index | 1048575 | 65534 |
| Numero massimo di slot di input | 16 | 16 |
| Destinazioni di rendering simultanee | 1 | 1 |
| Query di occlusione | Sì | No |
| Alpha Blend separato | Sì | No |
| Eseguire il mirroring una sola volta | Sì | No |
| Elementi vertici sovrapposti | Sì | No |
| Maschere di scrittura indipendenti | No | No |
| Instancing | No | No |
| Nonpowers-of-2 in modo condizionale<sup>3</sup> | Sì | Sì |
| Nonpowers-of-2 incondizionatamente<sup>4</sup> | No | No |

## <a name="footnotes-for-the-tables"></a>Note a piè di pagina per le tabelle

<sup>0</sup> richiede il runtime Direct3D 11.3 o Direct3D 12.

<sup>1</sup> Richiede il runtime Direct3D 11.1.

<sup>2</sup> Il modello shader 5.0 e versione successiva può supportare facoltativamente shader a precisione doppia, shader a doppia precisione estesi, l'istruzione **sad4** shader e shader a precisione parziale. Per determinare le opzioni del modello shader 5.0 disponibili per DirectX 11, chiamare [**ID3D11Device::CheckFeatureSupport**](/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). La compatibilità dipende dall'hardware in esecuzione. Il modello shader 5.1 e versioni successive sono supportati solo tramite l'API DirectX 12, indipendentemente dal livello di funzionalità in uso. DirectX 11 supporta solo fino al modello shader 5.0. L'API DirectX 12 passa solo al livello di funzionalità 11 \_ 0.

<sup>3</sup> Ai livelli di funzionalità \_ 9 1, 9 2 e 9 3, il dispositivo di visualizzazione supporta l'uso di trame 2D con dimensioni che non sono potenza di due in due \_ \_ condizioni. In primo luogo, è possibile creare un solo livello di mappa MIP per ogni trama e, in secondo luogo, non è consentita alcuna modalità di incapsulamento del campionatore per le trame (ovvero, i membri **AddressU**, **AddressV** e **AddressW** di [**D3D11 \_ SAMPLER \_ DESC**](/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc) non possono essere impostati su [**D3D11 \_ TEXTURE ADDRESS \_ \_ WRAP).**](/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode)

<sup>4</sup> Ai livelli di funzionalità \_ 10 0, 10 1 e \_ 11 0, il dispositivo di visualizzazione supporta incondizionatamente l'uso di trame 2D con dimensioni che non sono di potenza di \_ due.

<sup>5</sup> Vertex shader 2a con 256 istruzioni, 32 registri temporanei, controllo di flusso statico di profondità 4, controllo dinamico del flusso di profondità 24 e PREDICAZIONE D3DVS20CAPS. \_ Pixel shader 2x con 512 istruzioni, 32 registri temporanei, controllo di flusso statico di profondità 4, controllo dinamico del flusso di profondità 24, \_ D3DPS20CAPS ARBITRARYSWIZZLE, \_ D3DPS20CAPS GRADIENTINSTRUCTIONS, PREDICATION D3DPS20CAPS, \_ D3DPS20CAPS \_ NODEPENDENTREADLIMIT e D3DPS20CAPS \_ NOTEXINSTRUCTIONLIMIT.

<sup>6</sup> Livelli superiori facoltativi.

<sup>7</sup> Per il livello di funzionalità 9_3, gli unici metodi di rendering supportati sono **Draw,** **DrawIndexed** e **DrawIndexInstanced.** Anche per il livello di funzionalità 9_3, il rendering dell'elenco di punti è supportato solo per il rendering tramite **Draw.**

<sup>8</sup> Richiede il runtime Direct3D 12.

<sup>9</sup> Nell'API Direct3D 12 sono previsti limiti al numero di descrittori in un heap CBV/SRV/UAV. Per [informazioni dettagliate, vedere](/windows/win32/direct3d12/hardware-support) Livelli hardware. Separatamente, è previsto un limite al numero di UAV in tutte le tabelle dei descrittori in tutte le fasi, che si basa sul livello [di binding delle risorse](https://microsoft.github.io/DirectX-Specs/d3d/ResourceBinding.html#levels-of-hardware-support).

Per informazioni dettagliate sul supporto del formato a diversi livelli di funzionalità hardware, vedere:

- [Supporto del formato DXGI per l'hardware Direct3D Feature Level 12.1](../direct3ddxgi/hardware-support-for-direct3d-12-1-formats.md)
- [Supporto del formato DXGI per l'hardware Direct3D a livello di funzionalità 12.0](../direct3ddxgi/hardware-support-for-direct3d-12-0-formats.md)
- [Supporto del formato DXGI per l'hardware Direct3D Feature Level 11.1](../direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware.md)
- [Supporto del formato DXGI per l'hardware Direct3D a livello di funzionalità 11.0](../direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware.md)
- [Supporto hardware per formati Direct3D 10Level9](/previous-versions/ff471324(v=vs.85))
- [Supporto hardware per i formati Direct3D 10.1](/previous-versions/cc627091(v=vs.85))
- [Supporto hardware per i formati Direct3D 10](/previous-versions/cc627090(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

* [Direct3D 11 su hardware di livello inferiore](overviews-direct3d-11-devices-downlevel.md)
* [Livelli di funzionalità hardware (Direct3D 12)](../direct3d12/hardware-feature-levels.md)
