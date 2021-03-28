---
title: Utilizzo dei dati della funzionalità Direct3D 11 per integrare i livelli di funzionalità Direct3D
description: Informazioni su come controllare il supporto dei dispositivi per le funzionalità facoltative, incluse le funzionalità aggiunte nelle versioni recenti di Windows.
ms.assetid: 91D9706A-47C5-4220-8AC7-167095E74F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcc770812281ea89e8ebb68065aa68a00e1887d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338086"
---
# <a name="using-direct3d-11-feature-data-to-supplement-direct3d-feature-levels"></a>Utilizzo dei dati della funzionalità Direct3D 11 per integrare i livelli di funzionalità Direct3D

Informazioni su come controllare il supporto dei dispositivi per le funzionalità facoltative, incluse le funzionalità aggiunte nelle versioni recenti di Windows.

I [livelli di funzionalità Direct3D](overviews-direct3d-11-devices-downlevel-intro.md) indicano set ben definiti di funzionalità GPU che corrispondono approssimativamente a diverse generazioni di hardware grafico. In questo modo si semplifica notevolmente l'attività di controllo capaibilities hardware, oltre a offrire un'esperienza coerente in un'ampia gamma di dispositivi diversi.

Per tenere conto di parte della varianza tra implementazioni hardware diverse, tra cui hardware legacy, hardware per dispositivi mobili e hardware moderno, alcune funzionalità sono considerate facoltative. Il supporto per queste funzionalità può essere determinato chiamando [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) e specificando la \_ \_ struttura dei dati della funzionalità d3d11 pertinente \_ \* . In questo argomento vengono descritte le diverse funzionalità facoltative di Direct3D 11, il modo in cui alcune di esse operano insieme e come è possibile evitare di controllare ogni singola funzionalità facoltativa.

## <a name="how-to-check-for-optional-feature-support"></a>Come verificare il supporto delle funzionalità facoltative

Chiamare [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport), fornendo la struttura che rappresenta la funzionalità facoltativa che si vuole usare. Se il metodo restituisce **S \_ OK**, significa che si sta eseguendo una versione del runtime Direct3D che supporta la funzionalità facoltativa. Se restituisce **e \_ INVALIDARG**, significa che si sta usando una versione del runtime di Direct3D 11 da prima che sia stata aggiunta la funzionalità facoltativa. Ciò significa che la funzionalità facoltativa non è disponibile, insieme alle altre funzionalità facoltative introdotte nella stessa versione di Direct3D 11 o versioni successive.

## <a name="can-i-minimize-the-work-required-for-feature-support-checks"></a>È possibile ridurre al minimo il lavoro necessario per i controlli del supporto delle funzionalità?

Oltre a disporre del runtime Direct3D 11 corretto (in genere associato a una versione di Windows), il driver di grafica deve essere sufficientemente recente per supportare la funzionalità facoltativa. Le specifiche WDDM richiedono che le funzionalità opzionali siano supportate se l'hardware è in grado di supportarlo. Pertanto, quando un driver di grafica supporta una delle funzionalità facoltative che sono state aggiunte in una particolare versione di Windows, in genere significa che il driver di grafica supporta le altre funzionalità aggiunte in tale versione di Windows. Ad esempio, se un driver di dispositivo supporta le ombreggiature sul livello di funzionalità 9, si sa che il driver di dispositivo è almeno WDDM 1,2.

**Nota**    Se un dispositivo Microsoft Direct3D supporta il [livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 11,1, tutte le funzionalità facoltative indicate dalle [**\_ \_ \_ \_ Opzioni d3d11 dei dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) sono supportate automaticamente ad eccezione di **SAD4ShaderInstructions** e **ExtendedDoublesShaderInstructions**.

Il runtime imposta sempre i raggruppamenti seguenti dei membri in modo identico. Ovvero tutti i valori di un raggruppamento sono **true** o **false** insieme:

-   **DiscardAPIsSeenByDriver** e **FlagsForUpdateAndCopySeenByDriver**
-   **ClearView**, **CopyWithOverlap**, **ConstantBufferPartialUpdate**, **ConstantBufferOffsetting** e **MapNoOverwriteOnDynamicConstantBuffer**
-   **MapNoOverwriteOnDynamicBufferSRV** e **MultisampleRTVWithForcedSampleCountOne**

**Opzioni del livello di funzionalità 11,2 ([**d3d11 \_ feature \_ d3d11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)):** le funzionalità facoltative indicate da questo campo sono indipendenti e devono essere controllate singolarmente.

### <a name="feature-support-on-windows-rt-81-and-windows-phone-81-devices"></a>Supporto delle funzionalità nei dispositivi Windows RT 8,1 e Windows Phone 8,1

I dispositivi Tablet Windows RT sono in grado di supportare un'ampia gamma di livelli di funzionalità e funzionalità facoltative, sono ottimizzati per ridurre il consumo di energia e utilizzano grafica integrata anziché GPU discrete. Le app di Windows Store per i dispositivi ARM devono supportare il livello di funzionalità 9,1. Le app DirectX per Windows RT dovrebbero sfruttare le funzionalità facoltative che possono risparmiare energia e cicli, ad esempio le istanze semplici, quando sono disponibili.

Windows Phone 8 dispositivi mobili supportano il livello di funzionalità 9,3 con funzionalità opzionali specifiche. [ \_ Per Windows Phone 8, vedere livello di funzionalità Direct3D 9 3](/previous-versions/windows/apps/jj714085(v=vs.105)).

## <a name="what-are-the-direct3d-11-optional-features"></a>Quali sono le funzionalità facoltative di Direct3D 11?

Nella parte restante di questo articolo vengono descritte le funzionalità facoltative disponibili in Direct3D 11,2. Le funzionalità sono descritte in ordine cronologico quando sono state aggiunte, in modo da poter avere un'idea delle funzionalità di versioni diverse di Direct3D 11.

## <a name="optional-compute-shader-support-for-feature-level-10"></a>Supporto di Compute Shader facoltativo per il livello di funzionalità 10

La funzionalità seguente è sempre disponibile per i dispositivi di livello funzionalità 10:

**[**D3d11 \_ FEATURE \_ data \_ D3D10 \_ X \_ hardware \_ options**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options):** se il valore è **true**, il dispositivo supporta Compute Shader. Questo include il supporto per i buffer non elaborati e strutturati.

Quando il dispositivo a livello di funzionalità 10 \_ 0 o 10 \_ 1 supporta questa funzionalità, non è garantito che il dispositivo supporti compute shader 4,1. Le app devono essere preparate per eseguire il fallback a Compute Shader 4,0 se [**ID3D11Device:: CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader) genera un'eccezione con un programma compute shader 4,1.

## <a name="optional-capabilities-for-feature-level-9"></a>Funzionalità facoltative per il livello di funzionalità 9

Sono state aggiunte le funzionalità seguenti per il livello di funzionalità 9 a partire da Windows 8:

**[**D3d11 \_ feature \_ data \_ d3d9 \_ options**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options):** indica il supporto per l'indirizzamento di trama a capo con trame non di potenza 2. Se questa operazione è supportata, \_ \_ \_ \_ con tali trame è possibile usare il wrapping della modalità di indirizzo della trama d3d11.

**[**D3d11 \_ feature \_ data \_ d3d9 \_ shadow \_ support**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support):** indica il supporto per i sampler di confronto in Shader Model 4,0 funzionalità di livello 9 \_ x shader. Viene usato per i test di profondità in pixel shader, abilitando il supporto per tecniche comuni come il mapping ombreggiatura e gli stencil.

È stata aggiunta la seguente funzionalità per i dispositivi di livello 9 a partire da Windows 8.1:

**[**\_ Dati della funzionalità d3d11 \_ \_ d3d9 \_ \_ \_ supporto per istanze semplici**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support):** indica il supporto per le funzionalità di creazione di istanze semplici che potrebbero essere disponibili su hardware a livello DirectX 9. La creazione di istanze semplice significa che tutti i membri **InstanceDataStepRate** delle strutture [**d3d11 dell'elemento di \_ input \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_input_element_desc) utilizzati per definire il layout di input devono essere uguali a 1. I dispositivi che supportano il livello di funzionalità 9,3 o versioni successive includono già il supporto completo per le istanze.

## <a name="optional-floating-point-precision-support-for-shader-programs"></a>Supporto della precisione a virgola mobile facoltativa per i programmi shader

Supporto della precisione minima per **[**\_ \_ data \_ \_ \_ \_ shader della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support):** i campi in questo struct indicano la lunghezza dei numeri a virgola mobile quando è abilitata la precisione minima oppure 0 se è supportata solo la precisione a virgola mobile a 32 bit completa.

Per i dispositivi di livello 9 della funzionalità, la precisione minima del vertex shader può essere diversa da quella del pixel shader. La precisione per il vertex shader è indicata nel campo **AllOtherShaderStagesMinPrecision** .

**[**\_ \_ \_ Duplicazione dei dati della funzionalità d3d11: i**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)** dispositivi con livello di funzionalità 11 possono supportare calcoli a precisione doppia nei programmi del modello shader 5,0. Il supporto per calcoli a precisione doppia nello shader significa che i valori float possono essere convertiti in valori Double nel programma compute shader, offrendo il vantaggio di un calcolo con precisione più elevata all'interno di ogni passaggio dello shader. I numeri a precisione doppia devono essere riconvertiti in float prima di essere scritti nel buffer di output. Si noti che la divisione a precisione doppia non è necessariamente supportata.

## <a name="additional-capabilities-for-direct3d-112"></a>Funzionalità aggiuntive per Direct3D 11,2

Direct3D 11,2 aggiunge quattro nuove funzionalità facoltative che possono essere supportate dai dispositivi Direct3D 11. Queste funzionalità si trovano nella [**struttura \_ d3d11 \_ data \_ d3d11 \_ OPTIONS1 della funzionalità**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) :

**TiledResourcesTier:** Indica il supporto per le risorse affiancate e indica il livello supportato.

**MinMaxFiltering:** Indica il supporto per \_ le opzioni di filtro minimo e filtro d3d11 del filtro d3d11 \_ \_ \* \_ \_ \_ \* , che confrontano il risultato del filtro con il valore minimo (o massimo). Vedere [**\_ filtro d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter).

**ClearViewAlsoSupportsDepthOnlyFormats:** Indica il supporto per la cancellazione delle visualizzazioni delle risorse del buffer di profondità.

**MapOnDefaultBuffers:** Indica il supporto per il mapping dei buffer di destinazione di rendering creati con il flag **\_ \_ predefinito di utilizzo di d3d11** .

## <a name="tile-based-rendering"></a>Rendering basato su sezioni

**[**\_ Informazioni sull' \_ \_ architettura dei \_ dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info):** indica se il dispositivo di grafica raggruppa i comandi di rendering ed esegue il rendering basato sul riquadro per impostazione predefinita. Questa operazione può essere utilizzata come hint per l'ottimizzazione del motore di grafica.

## <a name="optional-features-for-development-and-debugging"></a>Funzionalità facoltative per lo sviluppo e il debug

**D3d11 \_ \_Opzioni di d3d11 dei dati delle funzionalità \_ \_ ::D iscardapisseenbydriver:** è possibile monitorare questo membro durante lo sviluppo per escludere i driver legacy sull'hardware in cui [**DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) e [**DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) potrebbero essere utili.

**[**\_ Supporto di \_ \_ marcatori \_ di dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support):** questo è supportato se l'hardware e il driver supportano il contrassegno dei dati per la profilatura della GPU.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 