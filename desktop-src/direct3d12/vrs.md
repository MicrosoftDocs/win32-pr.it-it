---
title: Ombreggiatura a velocità variabile (VRS)
description: L'ombreggiatura a velocità variabile o l'ombreggiatura dei pixel grosso modo grosso modo è un meccanismo che consente di allocare prestazioni/potenza di rendering a velocità variabili nell'immagine &mdash; &mdash; sottoposta a rendering.
ms.localizationpriority: high
ms.topic: article
ms.date: 04/08/2019
ms.openlocfilehash: 2f207cddee978915788291fc0ffe55160e6a93c6
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380765"
---
# <a name="variable-rate-shading-vrs"></a>Ombreggiatura a velocità variabile (VRS)

## <a name="the-motivation-for-vrs"></a>La motivazione per VRS
A causa dei vincoli di prestazioni, un renderer grafico non può sempre permettersi di offrire lo stesso livello di qualità a ogni parte dell'immagine di output. L'ombreggiatura a velocità variabile o l'ombreggiatura dei pixel grosso modo grosso modo è un meccanismo che consente di allocare prestazioni/potenza di rendering a velocità variabili nell'immagine &mdash; &mdash; sottoposta a rendering.

In alcuni casi, la velocità di ombreggiatura può essere ridotta con una riduzione ridotta o nessuna della qualità dell'output percettibile; con un miglioramento delle prestazioni essenzialmente gratuito.

## <a name="without-vrsmdashmulti-sample-anti-aliasing-with-supersampling"></a>Senza &mdash; anti-aliasing multicampionamento VRS con supercampionamento
Senza ombreggiatura a velocità variabile, l'unico modo per controllare la frequenza di ombreggiatura è l'anti-aliasing multicampionamento (MSAA) con esecuzione basata su campione (nota anche come supercampionamento).

MSAA è un meccanismo per ridurre gli alias geometrici e migliorare la qualità di rendering di un'immagine rispetto a non usare MSAA. Il numero di campioni MSAA, che possono essere 1x, 2x, 4x, 8x o 16x, regola il numero di campioni allocati per pixel di destinazione di rendering. Il numero di campioni MSAA deve essere noto in anticipo quando viene allocata la destinazione e non può essere modificato successivamente.

Il supercampionamento fa sì che pixel shader richiamato una volta per campione, a una qualità superiore ma anche a un costo delle prestazioni superiore rispetto all'esecuzione per pixel.

L'applicazione può controllare la frequenza di ombreggiatura scegliendo tra l'esecuzione basata su pixel o MSAA-with-supersampling. Queste due opzioni non forniscono un controllo molto fine. È anche possibile che si desideri una frequenza di ombreggiatura inferiore per una determinata classe di oggetti rispetto al resto dell'immagine. Tali oggetti possono includere un oggetto dietro un elemento HUD o una trasparenza, una sfocatura (profondità di campo, movimento e così via) o una distorsione ottica dovuta all'ottica VR. Ma ciò non sarebbe possibile, perché la qualità dell'ombreggiatura e i costi sono fissi per l'intera immagine.

## <a name="with-variable-rate-shading-vrs"></a>Con ombreggiatura a velocità variabile (VRS)
Il modello di ombreggiatura a velocità variabile (VRS) estende il sovracampionamento con MSAA nella direzione opposta, ovvero "pixel grossolano", aggiungendo il concetto di ombreggiatura grossolano. Qui l'ombreggiatura può essere eseguita con una frequenza più grossosa di un pixel. In altre parole, un gruppo di pixel può essere ombreggiato come singola unità e il risultato viene quindi trasmesso a tutti i campioni nel gruppo.

Un'API di ombreggiatura grosso modo consente all'applicazione di specificare il numero di pixel che appartengono a un gruppo ombreggiato o pixel grosso *modo.* Dopo aver allocato la destinazione di rendering, è possibile variare le dimensioni in pixel grosso modo. Pertanto, diverse parti dello schermo o passaggi di disegno diversi possono avere frequenze di ombreggiatura diverse.

Di seguito è riportata una tabella che descrive il livello MSAA supportato con le dimensioni in pixel grossoline. Alcune non sono supportate in alcuna piattaforma. mentre altre sono abilitate in modo condizionale in base a una funzionalità (*AdditionalShadingRatesSupported*), indicata da "Cap".

![La tabella mostra le dimensioni in pixel grosso modo per i livelli M S A A.](images/CoarsePixelSizeSupport.PNG "Dimensioni dei pixel grosso grosso modo")

Per i livelli di funzionalità illustrati nella sezione successiva, non esiste una combinazione di dimensioni di pixel grossole e numero di campioni in cui l'hardware deve tenere traccia di più di 16 campioni per pixel shader chiamata. Queste combinazioni sono ombreggiate per metà nella tabella precedente.

## <a name="feature-tiers"></a>Livelli di funzionalità
Esistono due livelli per l'implementazione della realtà virtuale e due funzionalità per cui è possibile eseguire query. Ogni livello viene descritto in modo più dettagliato dopo la tabella.

![La tabella mostra le funzionalità disponibili nei livelli 1 e 2.](images/Tiers.PNG "Livelli VRS")

### <a name="tier-1"></a>Livello 1
- La frequenza di ombreggiatura può essere specificata solo per ogni estrazione; non più granulare.
- La frequenza di ombreggiatura si applica in modo uniforme a ciò che viene disegnato indipendentemente dalla posizione all'interno della destinazione di rendering.

### <a name="tier-2"></a>Livello 2
- La frequenza di ombreggiatura può essere specificata per estrazione, come nel livello 1. Può anche essere specificato da una combinazione di base per ogni estrazione e di:
  - Semantica da ogni vertice che provoca e
  - un'immagine dello spazio dello schermo.
- Le percentuali di ombreggiatura delle tre origini vengono combinate usando un set di combinatori.
- Le dimensioni del riquadro dell'immagine dello spazio dello schermo sono 16x16 o inferiori.
- La velocità di ombreggiatura richiesta dall'applicazione è garantita per essere recapitata esattamente (per la precisione dei filtri temporali e di altri filtri di ricostruzione).
- SV_ShadingRate'input PS è supportato.
- La frequenza di ombreggiatura per vertice per vertice (nota anche come per primitiva), è valida quando viene usato un viewport e non viene `SV_ViewportArrayIndex` scritto in .
- La frequenza per-provocazione dei vertici può essere usata con più di un viewport se la funzionalità *SupportsPerVertexShadingRateWithMultipleViewports* è impostata su `true` . Inoltre, in questo caso, tale frequenza può essere usata quando `SV_ViewportArrayIndex` viene scritto in .

### <a name="list-of-capabilities"></a>Elenco di funzionalità
- *AdditionalShadingRatesSupported*
  - Tipo booleano.
  - Indica se le dimensioni dei pixel grosso modo 2x4, 4x2 e 4x4 sono supportate per il rendering a campionamento singolo; e se le dimensioni in pixel grosso modo 2x4 sono supportate per MSAA 2x.
- *SupportsPerVertexShadingRateWithMultipleViewports*
  - Tipo booleano.
  - Indica se è possibile usare più di un viewport con la frequenza di ombreggiatura per vertice (nota anche come per primitiva).

## <a name="specifying-shading-rate"></a>Specifica della frequenza di ombreggiatura
Per la flessibilità nelle applicazioni, sono disponibili diversi meccanismi per controllare la frequenza di ombreggiatura. Sono disponibili meccanismi diversi a seconda del livello di funzionalità hardware.

### <a name="command-list"></a>Elenco comandi
Si tratta del meccanismo più semplice per l'impostazione della frequenza di ombreggiatura. È disponibile in tutti i livelli.

L'applicazione può specificare una dimensione in pixel grossolano usando il metodo [ **ID3D12GraphicsCommandList5::RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate). Tale API accetta un solo argomento di enumerazione. L'API offre un controllo generale del livello di qualità per il rendering della possibilità di impostare la frequenza di ombreggiatura &mdash; in base al disegno.

I valori per questo [](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) stato vengono espressi tramite l D3D12_SHADING_RATE enumere.

#### <a name="coarse-pixel-size-support"></a>Supporto di dimensioni in pixel grossoline
Le frequenze di ombreggiatura 1x1, 1x2, 2x2 e 2x2 sono supportate in tutti i livelli.

È disponibile una funzionalità, *AdditionalShadingRatesSupported,* che indica se 2x4, 4x2 e 4x4 sono supportati nel dispositivo.

### <a name="screen-space-image-image-based"></a>Immagine dello spazio dello schermo (basata su immagine)
Nel livello 2 e superiore è possibile specificare la frequenza di ombreggiatura dei pixel con un'immagine dello spazio sullo schermo.

L'immagine dello spazio dello schermo consente all'applicazione di creare un'immagine di "livello di dettaglio" che indica aree di qualità variabile, ad esempio aree coperte da sfocatura del movimento, sfocatura profondità di campo, oggetti trasparenti o elementi dell'interfaccia utente HUD. La risoluzione dell'immagine è in blocchi macro; non è nella risoluzione della destinazione di rendering. In altre parole, i dati sulla frequenza di ombreggiatura vengono specificati con una granularità di riquadri di 8x8 o 16x16 pixel, come indicato dalle dimensioni del riquadro VRS.

#### <a name="tile-size"></a>Dimensioni del riquadro
L'applicazione può eseguire una query su un'API per recuperare le dimensioni del riquadro VRS supportate per il dispositivo.

I riquadri sono quadrati e le dimensioni si riferiscono alla larghezza o all'altezza del riquadro in texel.

Se l'hardware non supporta l'ombreggiatura a velocità variabile di livello 2, la query di funzionalità per le dimensioni del riquadro restituisce 0.

Se l'hardware *supporta* l'ombreggiatura a velocità variabile di livello 2, le dimensioni del riquadro sono uno di questi valori.

- 8
- 16
- 32

#### <a name="screen-space-image-size"></a>Dimensioni dell'immagine dello spazio sullo schermo
Per una destinazione di rendering di dimensioni {rtWidth, rtHeight}, usando una dimensione di riquadro specificata denominata **VRSTileSize**, l'immagine dello spazio dello schermo che la copre è di queste dimensioni.

```cpp
{ ceil((float)rtWidth / VRSTileSize), ceil((float)rtHeight / VRSTileSize) }
```

L'immagine dello spazio dello schermo in alto a sinistra (0, 0) viene bloccata in alto a sinistra della destinazione di rendering (0, 0).

Per cercare la coordinata (x,y) di un riquadro che corrisponde a una posizione specifica nella destinazione di rendering, dividere le coordinate dello spazio della finestra (x, y) per le dimensioni del riquadro, ignorando i bit frazionari.

Se l'immagine dello spazio dello schermo è più grande di quella che deve essere per una determinata destinazione di rendering, le parti aggiuntive a destra e/o in basso non vengono usate.

Se l'immagine dello spazio sullo schermo è troppo piccola per una determinata destinazione di rendering, qualsiasi tentativo di lettura dall'immagine oltre gli extent effettivi produce una velocità di ombreggiatura predefinita di 1x1. Ciò è dovuto al fatto che l'immagine dello spazio dello schermo in alto a sinistra (0, 0) è bloccata in alto a sinistra della destinazione di rendering (0, 0) e "la lettura oltre gli extent di destinazione di rendering" indica la lettura di valori troppo grandi per x e y.

#### <a name="format-layout-resource-properties"></a>Formato, layout, proprietà delle risorse
Il formato di questa superficie è una superficie a 8 bit a canale singolo ([**DXGI_FORMAT_R8_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

La risorsa è la dimensione **TEXTURE2D.**

Non può essere arrayed o mipped. Deve avere in modo esplicito un livello mip.

Ha il numero di campioni 1 e la qualità del campione 0.

Il layout della trama **è UNKNOWN.** Non può essere implicitamente un layout principale di riga, perché l'adattatore incrociato non è consentito.

Il modo previsto in cui vengono popolati i dati dell'immagine dello spazio sullo schermo è
1. Scrivere i dati usando uno shader di calcolo; l'immagine dello spazio dello schermo è associata come UAV o
2. Copiare i dati nell'immagine dello spazio sullo schermo.

Quando si crea l'immagine dello spazio sullo schermo, questi flag sono consentiti.

- NONE
- ALLOW_UNORDERED_ACCESS
- DENY_SHADER_RESOURCE

Questi flag non sono consentiti.

- ALLOW_RENDER_TARGET
- ALLOW_DEPTH_STENCIL
- ALLOW_CROSS_ADAPTER
- ALLOW_SIMULTANEOUS_ACCESS
- VIDEO_DECODE_REFERENCE_ONLY

Il tipo di heap della risorsa non può essere UPLOAD o READBACK.

La risorsa non può essere SIMULTANEOUS_ACCESS. La risorsa non può essere tra adapter.

#### <a name="data"></a>Data
Ogni byte dell'immagine dello spazio sullo schermo corrisponde a un valore [**dell'D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)  predefinita.

#### <a name="resource-state"></a>Stato della risorsa
Una risorsa deve essere passata a uno stato di sola lettura quando viene usata come immagine dello spazio sullo schermo. A questo scopo, [**viene D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)uno stato di sola lettura, D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE .

La risorsa immagine viene passata da tale stato per diventare nuovamente scrivibile.

#### <a name="setting-the-image"></a>Impostazione dell'immagine
L'immagine dello spazio sullo schermo per specificare la frequenza dello shader è impostata nell'elenco dei comandi.

Una risorsa impostata come origine della frequenza di ombreggiatura non può essere letta o scritta da alcuna fase dello shader.

È `null` possibile impostare un'immagine dello spazio sullo schermo per specificare la frequenza dello shader. Questo ha l'effetto che 1x1 viene usato in modo coerente come contributo dall'immagine dello spazio sullo schermo. L'immagine dello spazio sullo schermo può essere inizialmente considerata come impostata su `null` .

#### <a name="promotion-and-decay"></a>Promozione e decadimento
Una risorsa immagine dello spazio sullo schermo non ha implicazioni speciali per quanto riguarda la promozione o il decadimento.

### <a name="per-primitive-attribute"></a>Attributo per primitivo
Un attributo per primitivo aggiunge la possibilità di specificare un termine di frequenza di ombreggiatura come attributo da un vertice provocante. Questo attributo è a tinta piatta, cio' viene propagato a tutti i pixel nella primitiva del triangolo &mdash; o della linea corrente. L'uso di un attributo per primitivo può consentire un controllo più granulare della qualità dell'immagine rispetto agli altri identificatori di frequenza di ombreggiatura.

L'attributo per primitivo è una semantica impostabile denominata `SV_ShadingRate` . `SV_ShadingRate`esiste come parte di [HLSL Shader Model 6.4.](/windows/desktop/direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12)

Se vs o GS imposta , ma VRS non `SV_ShadingRate` è abilitato, l'impostazione semantica non ha alcun effetto. Se non viene specificato alcun valore per per primitiva, come contributo per primitiva viene assunto un valore di velocità di `SV_ShadingRate` ombreggiatura pari a 1x1.

### <a name="combining-shading-rate-factors"></a>Combinazione dei fattori di frequenza dell'ombreggiatura
Le varie origini della velocità di ombreggiatura vengono applicate in sequenza usando questo diagramma.

![Il diagramma mostra uno stato della pipeline, con etichetta A, con frequenza di ombreggiatura dei vertici provocante, etichettata B, applicata a un combinatore, quindi frequenza di ombreggiatura basata su immagine, etichettata B, applicata a un combinatore.](images/Combiners.PNG "Combinatori ombreggiatura")

Ogni coppia di A e B viene combinata usando un combinatore.

\* Quando si specifica una frequenza shader in base all'attributo vertice.

- Se si usa uno shader geometry, è possibile specificare la frequenza di ombreggiatura.
- Se non viene usato uno shader geometry, la velocità di ombreggiatura viene specificata dal vertice che provoca l'ombreggiatura.

#### <a name="list-of-combiners"></a>Elenco di combinatori
Sono supportati i combinatori seguenti. Uso di un combinatore (C) e di due input (A e B).

- **Pass-through**. C.xy = A.xy.
- **Eseguire l'override** di . C.xy = B.xy.
- **Di qualità superiore.** C.xy = min(A.xy, B.xy).
- **Qualità inferiore.** C.xy = max(A.xy, B.xy).
- **Applicare il costo B rispetto a A**. C.xy = min(maxRate, A.xy + B.xy).

dove `maxRate` è la dimensione massima consentita di pixel grosso modo nel dispositivo. Si tratta di

- **D3D12_AXIS_SHADING_RATE_2X** (ovvero, un valore pari a 1), se AdditionalShadingRatesSupported è `false` .
- **D3D12_AXIS_SHADING_RATE_4X** (ovvero, un valore pari a 2), se AdditionalShadingRatesSupported è `true` .

La scelta del combinatore per l'ombreggiatura a frequenza variabile viene impostata nell'elenco di comandi tramite [**ID3D12GraphicsCommandList5::RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate).

Se non viene impostato alcun combinatore, rimangono al valore predefinito, ovvero PASSTHROUGH.

Se l'origine di un combinatore è un [**D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate), che non è consentito nella tabella di supporto, l'input viene sanizionato in base a una frequenza di ombreggiatura *supportata.*

Se l'output di un combinatore non corrisponde a una frequenza di ombreggiatura supportata nella piattaforma, il risultato viene sanizionato in base a una frequenza di ombreggiatura *supportata.*

### <a name="default-state-and-state-clearing"></a>Stato predefinito e cancellazione dello stato
Tutte le origini della frequenza di ombreggiatura, in modo

- la frequenza specificata dallo stato della pipeline (specificata nell'elenco dei comandi),
- la frequenza specificata dall'immagine dello spazio sullo schermo e
- Attributo per primitivo

il valore predefinito è **D3D12_SHADING_RATE_1X1**. I combinatori predefiniti sono {PASSTHROUGH, PASSTHROUGH}.

Se non viene specificata alcuna immagine dello spazio sullo schermo, viene dedotto da tale origine una frequenza di ombreggiatura di 1x1.

Se non viene specificato alcun attributo per primitiva, viene dedotto da tale origine una frequenza di ombreggiatura di 1x1.

[ID3D12CommandList::ClearState](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate) reimposta la velocità specificata dallo stato della pipeline sul valore predefinito e la selezione dell'immagine dello spazio sullo schermo sul valore predefinito "nessuna immagine dello spazio sullo schermo".

## <a name="querying-shading-rate-by-using-sv_shadingrate"></a>Esecuzione di query sulla frequenza di ombreggiatura tramite SV_ShadingRate
È utile sapere quale frequenza di ombreggiatura è stata selezionata dall'hardware in qualsiasi pixel shader chiamata. In questo modo è possibile abilitare un'ampia gamma di ottimizzazioni nel codice PS. Una variabile di sistema solo PS, `SV_ShadingRate` , fornisce informazioni sulla frequenza di ombreggiatura.

### <a name="type"></a>Tipo
Il tipo di questa semantica è uint.

### <a name="data-interpretation"></a>Interpretazione dei dati
I dati vengono interpretati come un valore [**dell'enumerazione D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) dati.

### <a name="if-vrs-is-not-being-used"></a>Se VRS non viene usato
Se l'ombreggiatura dei pixel grosso modo non viene usata, viene letta come valore `SV_ShadingRate` 1x1, che indica pixel fini.

### <a name="behavior-under-sample-based-execution"></a>Comportamento nell'esecuzione basata su esempi
Un pixel shader la compilazione non riesce se viene immesso e usa anche l'esecuzione basata su campioni, ad esempio tramite l'input o la parola chiave `SV_ShadingRate` &mdash; di `SV_SampleIndex` interpolazione di esempio.

> ### <a name="remarks-on-deferred-shading"></a>Osservazioni sull'ombreggiatura posticipata
>
> È possibile che l'illuminazione di un'applicazione di ombreggiatura posticipata passi per sapere quale frequenza di ombreggiatura è stata usata per quale area dello schermo. In questo modo, i dispatch del passaggio di illuminazione possono essere avviati a una velocità più grosso modo. La `SV_ShadingRate` variabile può essere usata per eseguire questa operazione se viene scritta in gbuffer.

## <a name="depth-and-stencil"></a>Profondità e stencil
Quando si usa l'ombreggiatura dei pixel grosso modo, la profondità e lo stencil e la copertura vengono sempre calcolati ed emessi alla risoluzione del campione completa.

## <a name="using-the-shading-rate-requested"></a>Uso della frequenza di ombreggiatura richiesta
Per tutti i livelli, si prevede che se viene richiesta una velocità di ombreggiatura ed è supportata nella combinazione di livello dispositivo e MSAA, questa è la velocità di ombreggiatura disponibile dall'hardware.

Una frequenza di ombreggiatura richiesta indica una frequenza di ombreggiatura [](#combining-shading-rate-factors) calcolata come output dei combinatori (vedere la sezione Combinazione dei fattori di frequenza dell'ombreggiatura in questo argomento).

Una frequenza di ombreggiatura supportata è 1x1, 1x2, 2x1 o 2x2 in un'operazione di rendering in cui il numero di campioni è minore o uguale a quattro. Se la funzionalità *AdditionalShadingRatesSupported* è , sono supportate anche le frequenze di ombreggiatura `true` 2x4, 4x2 e 4x4 per alcuni conteggi di campioni( vedere la tabella nella sezione Con ombreggiatura a frequenza variabile [in](#with-variable-rate-shading-vrs) questo argomento).

## <a name="screen-space-derivatives"></a>Derivati dello spazio sullo schermo
I calcoli delle sfumature da pixel a pixel adiacenti sono interessati dall'ombreggiatura dei pixel grosso modo. Ad esempio, quando si usa 2x2 pixel grossoline, una sfumatura sarà il doppio rispetto a quando non vengono usati pixel grossoari. L'applicazione potrebbe voler modificare gli shader per compensare o meno questo problema, a &mdash; seconda della funzionalità desiderata.

Poiché i mip vengono scelti in base a un derivato dello spazio dello schermo, l'utilizzo dell'ombreggiatura dei pixel grosso modo influisce sulla selezione mip. L'utilizzo dell'ombreggiatura dei pixel grosso modo causa la selezione di mip meno dettagliati rispetto a quando non vengono usati pixel grossosi.

## <a name="attribute-interpolation"></a>Interpolazione di attributi
Gli input a un pixel shader possono essere interpolati in base ai relativi vertici di origine. Poiché l'ombreggiatura a velocità variabile influisce sulle aree della destinazione scritte da ogni chiamata del pixel shader, interagisce con l'interpolazione degli attributi. I tre tipi di interpolazione sono center, centroid e sample.

### <a name="center"></a>Center
La posizione di interpolazione centrale per un pixel grosso modo è il centro geometrico dell'intera area di pixel grosso modo. `SV_Position` viene sempre interpolato al centro dell'area di pixel grosso modo.

### <a name="centroid"></a>Baricentro
Quando l'ombreggiatura dei pixel grosso modo viene usata con MSAA, per ogni pixel fine verranno comunque scritti il numero completo di campioni allocati per il livello MSAA della destinazione. Quindi, la posizione di interpolazione centrale considererà tutti gli esempi per i pixel fini all'interno di pixel grosso modo. Detto questo, la posizione di interpolazione centroide è definita come primo campione coperto, in ordine crescente di indice del campione. Il code coverage effettivo dell'esempio è AND-ed con il bit corrispondente dello stato del rasterizzatore SampleMask.

> [!NOTE]
> Quando l'ombreggiatura dei pixel grosso modo viene usata nel livello 1, SampleMask è sempre una maschera completa. Se SampleMask è configurato per non essere una maschera completa, l'ombreggiatura dei pixel grosso modo è disabilitata nel livello 1.

### <a name="sample-based-execution"></a>Esecuzione basata su esempi
L'esecuzione basata su campione o il *supercampionamento* causato dall'uso della funzionalità di interpolazione di esempio può essere usato con l'ombreggiatura grossolano dei pixel e fa sì che il pixel shader sia richiamato per ogni &mdash; &mdash; campione. Per le destinazioni del conteggio dei campioni N, pixel shader viene richiamato N volte per pixel fine.

### <a name="evaluateattributesnapped"></a>EvaluateAttributeSnapped
Le funzioni intrinseche del modello pull non sono compatibili con l'ombreggiatura dei pixel grosso modo nel livello 1. Se si tenta di usare oggetti intrinseci del modello pull con ombreggiatura dei pixel grosso grosso modo nel livello 1, l'ombreggiatura dei pixel grosso modo grosso modo viene disabilitata automaticamente.

La funzione intrinseca può essere usata con l'ombreggiatura dei pixel grosso modo `EvaluateAttributeSnapped` nel livello 2. La sintassi è la stessa di sempre.

```hlsl
numeric EvaluateAttributeSnapped(   
    in attrib numeric value, 
    in int2 offset);
```

Per il contesto, `EvaluateAttributeSnapped` ha un parametro di offset con due campi. Se usato senza ombreggiatura dei pixel grosso modo, vengono usati solo i quattro bit di ordine inferiore dei trentadue completi. Questi quattro bit rappresentano l'intervallo [-8, 7]. Questo intervallo si estende su una griglia 16x16 all'interno di un pixel. L'intervallo è tale che vengono inclusi i bordi superiore e sinistro del pixel e i bordi inferiore e destro non lo sono. L'offset (-8, -8) si trova nell'angolo superiore sinistro e l'offset (7, 7) si trova nell'angolo inferiore destro. Offset (0, 0) è il centro del pixel.

Se usato con l'ombreggiatura dei pixel grosso modo, il parametro offset di è in grado di specificare una gamma `EvaluateAttributeSnapped` più ampia di posizioni. Il parametro offset seleziona una griglia 16x16 per ogni pixel fine e sono presenti più pixel fini. L'intervallo espressivo e il numero di bit usati dipendono dalle dimensioni dei pixel grossolano. Sono inclusi i bordi superiore e sinistro del pixel grosso e i bordi inferiore e destro non lo sono.

La tabella seguente descrive `EvaluateAttributeSnapped` l'interpretazione del parametro offset di per ogni dimensione di pixel grosso modo.

#### <a name="evaluateattributesnappeds-offset-range"></a>Intervallo di offset di EvaluateAttributeSnapped

|Dimensioni grossoline in pixel  |Intervallo indicizzabile             |Dimensioni dell'intervallo rappresentabili  |Numero di bit necessari {x, y}  |Maschera binaria dei bit utilizzabili          |    
|------------------:|---------------------------:|-------------------------:|-----------------------------:|-----------------------------------:|    
|1x1 (fine)         |{ \[ -8, 7 \] , \[ -8, 7 \] }      |{16, 16}                  |{4, 4}                        |{0000000000000xxxx, 00000000000xxxx}|    
|1x2                |{ \[ -8, 7 \] , \[ -16, 15 \] }    |{16, 32}                  |{4, 5}                        |{000000000000xxxx, 00000000000xxxxx}|    
|2x1                |{ \[ -16, 15 \] , \[ -8, 7 \] }    |{32, 16}                  |{5, 4}                        |{000000000000xxxxx, 0000000000xxxx}|    
|2x2                |{ \[ -16, 15 \] , \[ -16, 15 \] }  |{32, 32}                  |{5, 5}                        |{000000000000xxxxx, 0000000000xxxxx}|    
|2x4                |{ \[ -16, 15 \] , \[ -32, 31 \] }  |{32, 64}                  |{5, 6}                        |{000000000000xxxxx, 000000000xxxx}|    
|4x2                |{ \[ -32, 31 \] , \[ -16, 15 \] }  |{64, 32}                  |{6, 5}                        |{00000000000xxxxxx, 00000000000xxxxx}|    
|4x4                |{ \[ -32, 31 \] , \[ -32, 31 \] }  |{64, 64}                  |{6, 6}                        |{00000000000xxxxxx, 000000000xx}|   

Le tabelle seguenti sono una guida per la conversione da virgola fissa a rappresentazione decimale e frazionaria. Il primo bit utilizzabile nella maschera binaria è il bit di segno e il resto della maschera binaria comprende la parte numerica.

Lo schema dei numeri per i valori a quattro bit passati a `EvaluateAttributeSnapped` non è specifico dell'ombreggiatura a velocità variabile. Qui viene rieterato per completezza.

Per i valori a quattro bit.

| Valore binario | Decimal  | Precisione |
|-------------:|---------:|-----------:|
|         1000 |-0,5f     |-8 / 16     |
|         1001 |-0,4375f  |-7 / 16|    |
|         1010 |-0,375f   |-6 / 16|    |
|         1011 |-0,3125f  |-5 / 16     |
|         1100 |-0,25f    |-4 / 16     |
|         1101 |-0,1875f  |-3 / 16     |
|         1110 |-0,125f   |-2 / 16     |
|         1111 |-0,0625f  |-1 /16      |
|         0000 |0.0f      |0 / 16      |
|         0001 |-0,0625f  |1 / 16      |
|         0010 |-0,125f   |2 / 16      |
|         0011 |-0,1875f  |3 / 16      |
|         0100 |-0,25f    |4 / 16      |
|         0101 |-0,3125f  |5 / 16      |
|         0110 |-0,375f   |6 / 16      |
|         0111 |-0,4375f  |7 / 16      |

Per valori a cinque bit.

| Valore binario | Decimal  | Precisione |
|-------------:|---------:|-----------:|
|        10000 |-1        |-16 / 16    |
|        10001 |-0.9375   |-15 / 16    |
|        10010 |-0.875    |-14 / 16    |
|        10011 |-0.8125   |-13 / 16    |
|        10100 |-0.75     |-12 / 16    |
|        10101 |-0.6875   |-11 / 16    |
|        10110 |-0.625    |-10 / 16    |
|        10111 |-0.5625   |-9 / 16     |
|        11000 |-0.5      |-8 / 16     |
|        11001 |-0.4375   |-7 / 16     |
|        11010 |-0.375    |-6 / 16     |
|        11011 |-0.3125   |-5 / 16     |
|        11100 |-0.25     |-4 / 16     |
|        11101 |-0.1875   |-3 / 16     |
|        11110 |-0.125    |-2 / 16     |
|        11111 |-0.0625   |-1 / 16     |
|        00000 |0         |0 / 16      |
|        00001 |0.0625    |1 / 16      |
|        00010 |0,125     |2 / 16      |
|        00011 |0.1875    |3 / 16      |
|        00100 |0,25      |4 / 16      |
|        00101 |0.3125    |5 / 16      |
|        00110 |0.375     |6 / 16      |
|        00111 |0.4375    |7 / 16      |
|        01000 |0,5       |8 / 16      |
|        01001 |0.5625    |9 / 16      |
|        01010 |0.625     |10 / 16     |
|        01011 |0.6875    |11 / 16     |
|        01100 |0,75      |12 / 16     |
|        01101 |0.8125    |13 / 16     |
|        01110 |0.875     |14 / 16     |
|        01111 |0.9375    |15 / 16     |

Per i valori a sei bit.

| Valore binario | Decimal  | Precisione |
|-------------:|---------:|-----------:|
|       100000 |-2        |-32 / 16    |
|       100001 |-1.9375   |-31 / 16    |
|       100010 |-1.875    |-30 / 16    |
|       100011 |-1.8125   |-29 / 16    |
|       100100 |-1.75     |-28 / 16    |
|       100101 |-1.6875   |-27 / 16    |
|       100110 |-1.625    |-26 / 16    |
|       100111 |-1.5625   |-25 / 16    |
|       101000 |-1.5      |-24 / 16    |
|       101001 |-1.4375   |-23 / 16    |
|       101010 |-1.375    |-22 / 16    |
|       101011 |-1.3125   |-21 / 16    |
|       101100 |-1.25     |-20 / 16    |
|       101101 |-1.1875   |-19 / 16    |
|       101110 |-1.125    |-18 / 16    |
|       101111 |-1.0625   |-17 / 16    |
|       110000 |-1        |-16 / 16    |
|       110001 |-0.9375   |-15 / 16    |
|       110010 |-0.875    |-14 / 16    |
|       110011 |-0.8125   |-13 / 16    |
|       110100 |-0.75     |-12 / 16    |
|       110101 |-0.6875   |-11 / 16    |
|       110110 |-0.625    |-10 / 16    |
|       110111 |-0.5625   |-9 / 16     |
|       111000 |-0.5      |-8 / 16     |
|       111001 |-0.4375   |-7 / 16     |
|       111010 |-0.375    |-6 / 16     |
|       111011 |-0.3125   |-5 / 16     |
|       111100 |-0.25     |-4 / 16     |
|       111101 |-0.1875   |-3 / 16     |
|       111110 |-0.125    |-2 / 16     |
|       111111 |-0.0625   |-1 / 16     |
|       000000 |0         |0 / 16      |
|       000001 |0.0625    |1 / 16      |
|       000010 |0,125     |2 / 16      |
|       000011 |0.1875    |3 / 16      |
|       000100 |0,25      |4 / 16      |
|       000101 |0.3125    |5 / 16      |
|       000110 |0.375     |6 / 16      |
|       000111 |0.4375    |7 / 16      |
|       001000 |0,5       |8 / 16      |
|       001001 |0.5625    |9 / 16      |
|       001010 |0.625     |10 / 16     |
|       001011 |0.6875    |11 / 16     |
|       001100 |0,75      |12 / 16     |
|       001101 |0.8125    |13 / 16     |
|       001110 |0.875     |14 / 16     |
|       001111 |0.9375    |15 / 16     |
|       010000 |1         |16 / 16     |
|       010001 |1.0625    |17 / 16     |
|       010010 |1,125     |18 / 16     |
|       010011 |1.1875    |19 / 16     |
|       010100 |1,25      |20 / 16     |
|       010101 |1.3125    |21 / 16     |
|       010110 |1.375     |22 / 16     |
|       010111 |1.4375    |23 / 16     |
|       011000 |1.5       |24 / 16     |
|       011001 |1.5625    |25 / 16     |
|       011010 |1,625     |26 / 16     |
|       011011 |1.6875    |27 / 16     |
|       011100 |1,75      |28 / 16     |
|       011101 |1.8125    |29 / 16     |
|       011110 |1.875     |30 / 16     |
|       011111 |1.9375    |31 / 16     |

Come per i pixel fini, la griglia di posizioni valutabili di viene centrata al centro del pixel grosso modo quando si usa l'ombreggiatura dei pixel grosso `EvaluateAttributeSnapped` modo.

## <a name="setsamplepositions"></a>SetSamplePositions
Quando [**l'API ID3D12GraphicsCommandList1::SetSamplePositions**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) viene usata con l'ombreggiatura grosso modo, l'API imposta le posizioni del campione per i pixel fini.

## <a name="sv_coverage"></a>SV_Coverage
Se viene dichiarato come input o output dello shader nel livello 1, l'ombreggiatura dei pixel grosso modo `SV_Coverage` è disabilitata.

È possibile usare la semantica con ombreggiatura dei pixel grossolano nel livello 2 e riflette i campioni di una destinazione `SV_Coverage` MSAA da scrivere.

Quando viene usata l'ombreggiatura dei pixel grosso modo che consente a più pixel di origine di includere una tessera, la maschera di copertura rappresenta tutti i campioni &mdash; &mdash; provenienti da tale riquadro.

Data la compatibilità dell'ombreggiatura dei pixel grosso modo con MSAA, il numero di bit di copertura da specificare può variare. Ad esempio, con una risorsa MSAA 4x che usa D3D12_SHADING_RATE_2x2 , [**ogni**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)pixel grosso modo scrive in quattro pixel fini e ogni pixel fine ha quattro campioni. Ciò significa che ogni pixel grosso modo scrive in un totale di 4 * 4 = 16 campioni.

### <a name="number-of-coverage-bits-needed"></a>Numero di bit di code coverage necessari
La tabella seguente indica il numero di bit di code coverage necessari per ogni combinazione di dimensioni in pixel grosso modo e livello MSAA.

![La tabella mostra dimensioni in pixel grosso grosso modo, numero di pixel fini e livelli M S A A.](images/NumberOfCoverageBits.PNG "Bit di code coverage")

Come indicato nella tabella, non è possibile usare pixel grossolani per scrivere in più di 16 campioni alla volta usando la funzionalità di ombreggiatura a velocità variabile esposta tramite Direct3D 12. Questa restrizione è dovuta ai vincoli di Direct3D 12 relativi ai livelli MSAA consentiti con cui sono consentite dimensioni in pixel grossose (vedere la tabella nella sezione With [variable-rate shading (VRS)](#with-variable-rate-shading-vrs) in questo argomento.

### <a name="ordering-and-format-of-bits-in-the-coverage-mask"></a>Ordinamento e formato dei bit nella maschera di code coverage
I bit della maschera di copertura rispettano un ordine ben definito. La maschera è costituita da code coverage dai pixel da sinistra a destra, quindi dall'alto verso il basso (colonna principale). I bit di code coverage sono i bit di ordine basso della semantica di code coverage e sono densamente compattati.

La tabella seguente mostra il formato della maschera di copertura per le combinazioni supportate di dimensioni in pixel grossosse e livello MSAA.

![La tabella mostra dimensioni in pixel grossosse, diagramma di pixel grosso grosso modo e bit di copertura A A da 1 x M S A.](images/Coverage1x.PNG "Copertura a 1x")

La tabella seguente descrive 2 pixel MSAA, in cui ogni pixel ha due campioni di indici 0 e 1.

Il posizionamento delle etichette dei campioni sui pixel è a scopo illustrativo e non indica necessariamente le posizioni spaziali {X, Y} dei campioni su tale pixel. soprattutto dato che le posizioni di esempio possono essere modificate a livello di codice. Gli esempi sono indicati dall'indice in base 0.

![La tabella mostra dimensioni in pixel grossosse, diagramma di pixel grosso grosso modo e 2 bit di copertura M S A A.](images/Coverage2x.PNG "Copertura al 2x")

La tabella seguente mostra 4 pixel MSAA, in cui ogni pixel ha quattro campioni di indici 0, 1, 2 e 3.

![La tabella mostra dimensioni in pixel grossosse, diagramma di pixel grosso grosso modo e 4 bit di copertura M S A A.](images/Coverage4x.PNG "Copertura 4x")

## <a name="discard"></a>Discard
Quando la semantica HLSL viene usata con un'ombreggiatura dei pixel grosso modo grosso modo, i pixel grosso modo `discard` vengono eliminati.

## <a name="target-independent-rasterization-tir"></a>Rasterizzazione indipendente dalla destinazione (TIR)
TIR non è supportato quando si usa l'ombreggiatura dei pixel grosso modo.

## <a name="raster-order-views-rovs"></a>Visualizzazioni degli ordini raster (ROV)
Gli interlock ROV vengono specificati per operare con granularità fine in pixel. Se l'ombreggiatura viene eseguita per campione, gli interlock operano con una granularità del campione.

## <a name="conservative-rasterization"></a>Rasterizzazione conservativa
È possibile usare la rasterizzazione conservativa con ombreggiatura a frequenza variabile. Quando la rasterizzazione conservativa viene usata con l'ombreggiatura dei pixel grosso modo, i pixel fini all'interno di pixel grosso modo vengono rasterizzati conservativamente grazie alla copertura completa.

### <a name="coverage"></a>Copertura
Quando si usa la rasterizzazione conservativa, la semantica di code coverage contiene maschere complete per i pixel fini coperti e 0 per i pixel non coperti.

## <a name="bundles"></a>Pacchetti
È possibile chiamare le API di ombreggiatura a frequenza variabile in un bundle.

## <a name="render-passes"></a>Passaggi di rendering
È possibile chiamare le API di ombreggiatura a frequenza variabile in un passaggio [di rendering](/windows/desktop/direct3d12/direct3d-12-render-passes).

## <a name="calling-the-vrs-apis"></a>Chiamata delle API VRS
Questa sezione successiva descrive il modo in cui l'ombreggiatura a frequenza variabile è accessibile all'applicazione tramite Direct3D 12.

### <a name="capability-querying"></a>Esecuzione di query sulla funzionalità

Per eseguire una query per la funzionalità di ombreggiatura a frequenza variabile dell'adapter, chiamare [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) [**con D3D12_FEATURE::D 3D12_FEATURE_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)e specificare una struttura [ **D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) per la funzione da compilare automaticamente. La **struttura D3D12_FEATURE_DATA_D3D12_OPTIONS6** contiene diversi membri, tra cui uno del tipo enumerato [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) (D3D12_FEATURE_DATA_D3D12_OPTIONS6::VariableShadingRateTier) e uno che indica se l'elaborazione in background è supportata (D3D12_FEATURE_DATA_D3D12_OPTIONS6::BackgroundProcessingSupported).

Per eseguire una query per la funzionalità di livello 1, ad esempio, è possibile eseguire questa operazione.

```cpp
D3D12_FEATURE_DATA_D3D12_OPTIONS6 options;
return 
    SUCCEEDED(m_device->CheckFeatureSupport(
        D3D12_FEATURE_D3D12_OPTIONS6, 
        &options, 
        sizeof(options))) && 
    options.ShadingRateTier == D3D12_VARIABLE_SHADING_RATE_TIER_1;
```

### <a name="shading-rates"></a>Frequenze di ombreggiatura

I valori [ **nell'enumerazione D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) sono organizzati in modo che le frequenze di ombreggiatura siano facilmente scomposti in due assi, in cui i valori di ogni asse sono rappresentati in modo compatto nello spazio logaritmico in base [ **all'enumerazione D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate).

È possibile creare una macro per comporre due tassi di ombreggiatura degli assi in una velocità di ombreggiatura simile alla seguente.

```cpp
#define D3D12_MAKE_COARSE_SHADING_RATE(x,y) ((x) << 2 | (y))
D3D12_MAKE_COARSE_SHADING_RATE(
    D3D12_AXIS_SHADING_RATE_2X, 
    D3D12_AXIS_SHADING_RATE_1X)
```

La piattaforma fornisce anche queste macro, definite in `d3d12.h` .

```cpp
#define D3D12_GET_COARSE_SHADING_RATE_X_AXIS(x) ((x) >> 2 )
#define D3D12_GET_COARSE_SHADING_RATE_Y_AXIS(y) ((y) & 3 )
```

Possono essere usati per sezionare e comprendere `SV_ShaderRate` .

> [!NOTE]
> Questa interpretazione dei dati è orientata alla descrizione dell'immagine dello spazio dello schermo, che può essere manipolata dagli shader. Questo argomento viene illustrato più avanti nelle sezioni precedenti. Tuttavia, non esiste alcun motivo per non avere una definizione coerente delle dimensioni grossoline dei pixel da usare ovunque, anche quando si imposta la velocità di ombreggiatura a livello di comando.

### <a name="setting-command-level-shading-rate-and-combiners"></a>Impostazione della frequenza di ombreggiatura a livello di comando e dei combinatori
La frequenza di ombreggiatura e, facoltativamente, i combinatori vengono specificati tramite il [**metodo ID3D12GraphicsCommandList5::RSSetShadingRate.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate) Si passa un [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) per la frequenza di ombreggiatura di base e una matrice facoltativa di D3D12_SHADING_RATE_COMBINER [valori.](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner)

### <a name="preparing-the-screen-space-image"></a>Preparazione dell'immagine dello spazio sullo schermo
Lo stato della risorsa di sola lettura che designa un'immagine della frequenza di ombreggiatura utilizzabile è [definito come D3D12_RESOURCE_STATES::D 3D12_RESOURCE_STATE_SHADING_RATE_SOURCE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

### <a name="setting-the-screen-space-image"></a>Impostazione dell'immagine dello spazio sullo schermo
Specificare l'immagine dello spazio sullo schermo tramite il [**metodo ID3D12GraphicsCommandList5::RSSetShadingRateImage.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrateimage)

```cpp
m_commandList->RSSetShadingRateImage(screenSpaceImage);
```

### <a name="querying-the-tile-size"></a>Esecuzione di query sulla dimensione del riquadro
È possibile eseguire query sulla dimensione del riquadro [**dal membro D3D12_FEATURE_DATA_D3D12_OPTIONS6::ShadingRateImageTileSize.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) Vedere [Esecuzione di query sulla funzionalità precedente.](#capability-querying)

Viene recuperata una dimensione, poiché le dimensioni orizzontale e verticale sono sempre le stesse. Se la funzionalità del sistema è D3D12_SHADING_RATE_TIER_NOT_SUPPORTED [**,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier)le dimensioni del riquadro restituito sono 0.
