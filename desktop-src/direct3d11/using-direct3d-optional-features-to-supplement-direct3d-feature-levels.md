---
title: Uso dei dati delle funzionalità Direct3D 11 per integrare i livelli di funzionalità Direct3D
description: Informazioni su come controllare il supporto dei dispositivi per le funzionalità facoltative, incluse le funzionalità aggiunte nelle versioni recenti di Windows.
ms.assetid: 91D9706A-47C5-4220-8AC7-167095E74F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c2e7392f576b8c0dca059a4ef2fdd2ee6415230e5fd41e497d60899332f674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124049"
---
# <a name="using-direct3d-11-feature-data-to-supplement-direct3d-feature-levels"></a>Uso dei dati delle funzionalità Direct3D 11 per integrare i livelli di funzionalità Direct3D

Informazioni su come controllare il supporto dei dispositivi per le funzionalità facoltative, incluse le funzionalità aggiunte nelle versioni recenti di Windows.

[I livelli di funzionalità Direct3D](overviews-direct3d-11-devices-downlevel-intro.md) indicano set ben definiti di funzionalità GPU che corrispondono approssimativamente a diverse generazioni di hardware grafico. Questo semplifica notevolmente l'attività di controllo delle capaibilità hardware e offre anche un'esperienza coerente in un'ampia gamma di dispositivi diversi.

Per considerare parte della varianza tra diverse implementazioni hardware, tra cui hardware legacy, hardware mobile e hardware moderno, alcune funzionalità sono considerate facoltative. Il supporto per queste funzionalità può essere determinato chiamando [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) e fornendo la struttura FEATURE DATA D3D11 \_ \_ \_ \* pertinente. Questo argomento descrive le varie funzionalità facoltative di Direct3D 11, il modo in cui alcune di esse funzionano insieme e come evitare di controllare ogni singola funzionalità facoltativa.

## <a name="how-to-check-for-optional-feature-support"></a>Come verificare il supporto delle funzionalità facoltativo

Chiamare [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport), fornendo la struttura che rappresenta la funzionalità facoltativa che si desidera usare. Se il metodo restituisce **S \_ OK,** significa che si è in una versione del runtime Direct3D che supporta la funzionalità facoltativa. Se restituisce **E \_ INVALIDARG,** significa che si è in una versione del runtime Direct3D 11 da prima dell'aggiunta della funzionalità facoltativa. Ciò significa che la funzionalità facoltativa non è disponibile, insieme ad altre funzionalità facoltative introdotte nella stessa versione di Direct3D 11 o versione successiva.

## <a name="can-i-minimize-the-work-required-for-feature-support-checks"></a>È possibile ridurre al minimo il lavoro necessario per i controlli di supporto delle funzionalità?

Oltre a disporre del runtime Direct3D 11 corretto (in genere associato a una versione Windows), il driver di grafica deve essere sufficientemente recente da supportare la funzionalità facoltativa. Le specifiche WDDM richiedono il supporto di funzionalità facoltative se l'hardware è in grado di supportarlo. Pertanto, quando un driver di grafica supporta una delle funzionalità facoltative aggiunte in una particolare versione di Windows, significa in genere che il driver di grafica supporta le altre funzionalità aggiunte in tale versione di Windows. Ad esempio, se un driver di dispositivo supporta le ombreggiature sul livello di funzionalità 9, si sa che il driver di dispositivo è almeno WDDM 1.2.

**Nota**  Se un dispositivo Microsoft Direct3D supporta il livello di funzionalità [](overviews-direct3d-11-devices-downlevel-intro.md) 11.1, tutte le funzionalità facoltative indicate da [**D3D11 FEATURE DATA \_ \_ \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) sono supportate automaticamente ad eccezione di **SAD4ShaderInstructions** e **ExtendedDoublesShaderInstructions**.

Il runtime imposta sempre i raggruppamenti di membri seguenti in modo identico. In altri, tutti i valori in un raggruppamento sono **TRUE** **o FALSE** insieme:

-   **DiscardAPIsSeenByDriver** e **FlagsForUpdateAndCopySeenByDriver**
-   **ClearView,** **CopyWithOverlap,** **ConstantBufferPartialUpdate,** **ConstantBufferOffsetting** e **MapNoOverwriteOnDynamicConstantBuffer**
-   **MapNoOverwriteOnDynamicBufferSRV** e **MultisampleRTVWithForcedSampleCountOne**

Opzioni del livello di funzionalità **11.2 ([**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)):** le funzionalità facoltative indicate da questo campo sono indipendenti e devono essere controllate singolarmente.

### <a name="feature-support-on-windows-rt-81-and-windows-phone-81-devices"></a>Supporto delle funzionalità Windows RT 8.1 e Windows Phone 8.1

Windows RT tablet possono supportare un'ampia gamma di livelli di funzionalità e funzionalità facoltative, sono ottimizzati per ridurre il consumo di energia e usano grafica integrata anziché GPU discrete. Windows Le app dello Store per i dispositivi ARM devono supportare il livello di funzionalità 9.1. Le app DirectX per Windows RT devono sfruttare le funzionalità facoltative che consentono di risparmiare energia e cicli, ad esempio la semplice creazione di istanze, quando sono disponibili.

Windows Phone 8 dispositivi mobili supportano funzionalità di livello 9.3 con funzionalità facoltative specifiche. Vedere [Direct3D feature level \_ 9 3 per Windows Phone 8](/previous-versions/windows/apps/jj714085(v=vs.105)).

## <a name="what-are-the-direct3d-11-optional-features"></a>Quali sono le funzionalità facoltative di Direct3D 11?

Il resto di questo articolo descrive le funzionalità facoltative disponibili in Direct3D 11.2. Le funzionalità vengono descritte in ordine cronologico da quando sono state aggiunte, in modo da avere un'idea delle funzionalità presenti nelle diverse versioni di Direct3D 11.

## <a name="optional-compute-shader-support-for-feature-level-10"></a>Supporto di compute shader facoltativo per il livello di funzionalità 10

La funzionalità seguente è sempre disponibile per i dispositivi con livello di funzionalità 10:

**[**D3D11 \_ FEATURE \_ DATA \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options):** se è **TRUE,** il dispositivo supporta gli shader di calcolo. Include il supporto per buffer non elaborati e strutturati.

Quando il dispositivo a livello di funzionalità 10 0 o 10 1 supporta questa funzionalità, non è garantito che supporti \_ \_ compute shader 4.1. Le app devono essere preparate per il fall back in un compute shader 4.0 se [**ID3D11Device::CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader) genera un'eccezione con un programma compute shader 4.1.

## <a name="optional-capabilities-for-feature-level-9"></a>Funzionalità facoltative per il livello di funzionalità 9

Vengono aggiunte le funzionalità seguenti per il livello di funzionalità 9 a partire da Windows 8:

**[**D3D11 \_ FEATURE \_ DATA \_ D3D9 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options):** indica il supporto per l'indirizzamento della trama con trame non power-of-2. Se questa opzione è supportata, È possibile usare D3D11 \_ TEXTURE ADDRESS MODE WRAP con tali \_ \_ \_ trame.

**[**D3D11 \_ FEATURE \_ DATA \_ D3D9 \_ SHADOW \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support):** indica il supporto per i campionatori di confronto nei modelli shader 4.0 livello di funzionalità 9 x \_ shader. Viene usato per il test di profondità nei pixel shader, consentendo il supporto per tecniche comuni come il mapping delle ombreggiatura e gli stencil.

La funzionalità seguente è stata aggiunta per i dispositivi con livello di funzionalità 9 a partire Windows 8.1:

**[**D3D11 \_ FEATURE \_ DATA \_ D3D9 \_ SIMPLE \_ INSTANCING \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support):** indica il supporto per funzionalità di istanze semplici che potrebbero essere disponibili nell'hardware DirectX a 9 livelli. La semplice instancing indica che tutti i membri **InstanceDataStepRate** delle strutture [**D3D11 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_input_element_desc) usate per definire il layout di input devono essere uguali a 1. I dispositivi che supportano il livello di funzionalità 9.3 o versione successiva includono già il supporto completo per l'instancing.

## <a name="optional-floating-point-precision-support-for-shader-programs"></a>Supporto facoltativo della precisione a virgola mobile per i programmi shader

**[**D3D11 \_ FEATURE DATA SHADER MIN PRECISION \_ \_ \_ \_ \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support):** i campi in questo struct indicano la lunghezza dei numeri a virgola mobile quando è abilitata la precisione minima oppure 0 se è supportata solo la precisione a virgola mobile a 32 bit completa.

Per i dispositivi con livello di funzionalità 9, la precisione minima per il vertex shader può essere diversa da pixel shader. La precisione per il vertex shader è indicata nel **campo AllOtherShaderStagesMinPrecision.**

**[**D3D11 \_ FEATURE \_ DATA \_ DOUBLES:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)** i dispositivi con livello di funzionalità 11 possono supportare calcoli a precisione doppia all'interno dei programmi del modello shader 5.0. Il supporto per i calcoli a precisione doppia all'interno dello shader significa che i valori float possono essere convertiti in valori double all'interno del programma compute shader, offrendo il vantaggio di un calcolo di precisione più elevato all'interno di ogni passaggio dello shader. I numeri a precisione doppia devono essere convertiti nuovamente in valori float prima di essere scritti nel buffer di output. Si noti che la divisione a precisione doppia non è necessariamente supportata.

## <a name="additional-capabilities-for-direct3d-112"></a>Funzionalità aggiuntive per Direct3D 11.2

Direct3D 11.2 aggiunge quattro nuove funzionalità facoltative che possono essere supportate dai dispositivi Direct3D 11. Queste funzionalità sono nella struttura [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS1:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1)

**TiledResourcesTier:** Indica il supporto per le risorse affiancate e indica il livello di livello supportato.

**MinMaxFiltering:** Indica il supporto per le opzioni di filtro \_ D3D11 FILTER MINIMUM e \_ \_ \* D3D11 FILTER MAXIMUM, che confrontano il risultato del filtro con il valore minimo \_ \_ \_ \* (o massimo). Vedere [**D3D11 \_ FILTER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter).

**ClearViewAlsoSupportsDepthOnlyFormats:** Indica il supporto per la cancellazione delle visualizzazioni delle risorse del buffer di profondità.

**MapOnDefaultBuffers:** Indica il supporto per il mapping dei buffer di destinazione di rendering creati con il flag **D3D11 \_ USAGE \_ DEFAULT.**

## <a name="tile-based-rendering"></a>Rendering basato su riquadri

**[**D3D11 \_ FEATURE DATA ARCHITECTURE \_ \_ \_ INFO**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info):** indica se il dispositivo grafico esegue in batch i comandi di rendering ed esegue il rendering basato su riquadri per impostazione predefinita. Può essere usato come suggerimento per l'ottimizzazione del motore di grafica.

## <a name="optional-features-for-development-and-debugging"></a>Funzionalità facoltative per lo sviluppo e il debug

**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS::D iscardAPIsSeenByDriver:** è possibile monitorare questo membro durante lo sviluppo per escludere i driver legacy nell'hardware in cui [**DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) e [**DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) potrebbero essere stati altrimenti utili.

**[**D3D11 \_ FEATURE DATA MARKER \_ \_ \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support):** questa opzione è supportata se l'hardware e il driver supportano il contrassegno dei dati per la profilatura GPU.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 