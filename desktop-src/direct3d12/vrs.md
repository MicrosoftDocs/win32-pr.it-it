---
title: Ombreggiatura a frequenza variabile (VRS)
description: L' &mdash; ombreggiatura a frequenza variabile o l'ombreggiatura di pixel grossolani &mdash; è un meccanismo che consente di allocare prestazioni/potenza di rendering a frequenze che variano in base all'immagine sottoposta a rendering.
ms.localizationpriority: high
ms.topic: article
ms.date: 04/08/2019
ms.openlocfilehash: be2367ceb72d2e693d86b6f279b627f3bffa9e1c
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104548903"
---
# <a name="variable-rate-shading-vrs"></a>Ombreggiatura a frequenza variabile (VRS)

## <a name="the-motivation-for-vrs"></a>Motivazione per VRS
A causa dei vincoli di prestazioni, un renderer di grafica non può sempre permettersi di fornire lo stesso livello di qualità a ogni parte dell'immagine di output. L' &mdash; ombreggiatura a frequenza variabile o l'ombreggiatura di pixel grossolani &mdash; è un meccanismo che consente di allocare prestazioni/potenza di rendering a frequenze che variano in base all'immagine sottoposta a rendering.

In alcuni casi, la frequenza di ombreggiatura può essere ridotta con una riduzione minima o minima della qualità di output percettibile; un miglioramento delle prestazioni è sostanzialmente gratuito.

## <a name="without-vrsmdashmulti-sample-anti-aliasing-with-supersampling"></a>Senza l' &mdash; anti-aliasing VRS multisample con supercampionamento
Senza ombreggiatura a frequenza variabile, l'unico mezzo per controllare la velocità di ombreggiatura è con l'anti-aliasing di più campioni (MSAA) con esecuzione basata su campione (noto anche come supercampionamento).

MSAA è un meccanismo per la riduzione degli alias geometrici e per il miglioramento della qualità di rendering di un'immagine rispetto alla mancata utilizzo di MSAA. Il numero di campioni MSAA, che può essere 1x, 2x, 4x, 8x o 16x, determina il numero di campioni allocati per ogni pixel di destinazione di rendering. Il numero di campioni MSAA deve essere noto prima quando viene allocata la destinazione e non può essere modificato successivamente.

Il sovracampionamento fa in modo che il pixel shader venga richiamato una volta per ogni campione, con una qualità superiore, ma anche un costo superiore per le prestazioni rispetto all'esecuzione per pixel.

L'applicazione può controllare la velocità di ombreggiatura scegliendo tra l'esecuzione in base al pixel o MSAA-con-supercampionamento. Queste due opzioni non forniscono un controllo molto preciso. Inoltre, è possibile che si desideri una frequenza di ombreggiatura inferiore per una determinata classe di oggetti rispetto al resto dell'immagine. Tali oggetti possono includere un oggetto alla base di un elemento HUD o una trasparenza, una sfocatura (profondità di campo, movimento e così via) o una distorsione ottica a causa di un'ottica VR. Tuttavia, ciò non sarebbe possibile, perché la qualità e i costi dell'ombreggiatura sono corretti sull'intera immagine.

## <a name="with-variable-rate-shading-vrs"></a>Con ombreggiatura a frequenza variabile (VRS)
Il modello di ombreggiatura a frequenza variabile (VRS) estende il supercampionamento-con-MSAA nella direzione opposta, ovvero "pixel grossolano", aggiungendo il concetto di ombreggiatura grossolana. Questo è il punto in cui l'ombreggiatura può essere eseguita con una frequenza più grossolana di un pixel. In altre parole, un gruppo di pixel può essere ombreggiato come una singola unità e il risultato viene quindi trasmesso a tutti gli esempi nel gruppo.

Un'API di ombreggiatura grossolana consente all'applicazione di specificare il numero di pixel che appartengono a un gruppo ombreggiato o un *pixel grossolano*. È possibile variare le dimensioni in pixel grossolani dopo avere allocato la destinazione di rendering. In questo modo, parti diverse dello schermo o passaggi di estrazione diversi possono avere frequenze ombreggiate diverse.

Di seguito è riportata una tabella che descrive il livello MSAA supportato con le dimensioni dei pixel grossolani. Alcune non sono supportate in nessuna piattaforma; mentre altre sono abilitate in modo condizionale in base a una funzionalità (*AdditionalShadingRatesSupported*), indicata da "Cap".

![coarsePixelSizeSupport](images/CoarsePixelSizeSupport.PNG "Dimensioni in pixel grossolani")

Per i livelli di funzionalità descritti nella sezione successiva, non è disponibile una combinazione di numero grossolano di dimensioni in pixel e campione, in cui l'hardware deve tenere traccia di più di 16 campioni per pixel shader chiamata. Tali combinazioni sono ombreggiate in mezzitoni nella tabella precedente.

## <a name="feature-tiers"></a>Livelli di funzionalità
Sono disponibili due livelli per l'implementazione di VRS e due funzionalità su cui è possibile eseguire una query. Ogni livello viene descritto più dettagliatamente dopo la tabella.

![livelli](images/Tiers.PNG "Livelli VRS")

### <a name="tier-1"></a>Livello 1
- La velocità di ombreggiatura può essere specificata solo in base al singolo progetto; non è più granulare.
- La frequenza di ombreggiatura si applica in modo uniforme a quanto viene disegnato indipendentemente da dove si trova all'interno della destinazione di rendering.

### <a name="tier-2"></a>Livello 2
- La velocità di ombreggiatura può essere specificata in base al singolo progetto, come nel livello 1. Può anche essere specificato tramite una combinazione di base per ogni singola estrazione e di:
  - Semantica da ogni vertice che provoca e
  - immagine dello spazio dello schermo.
- Le frequenze di ombreggiatura delle tre origini vengono combinate usando un set di combinatori.
- Le dimensioni del riquadro immagine dello spazio dello schermo sono 16x16 o inferiori.
- Viene garantita la recapito esatta della frequenza di ombreggiatura richiesta dall'applicazione (per la precisione dei filtri temporali e di altri tipi di ricostruzione).
- L'input SV_ShadingRate PS è supportato.
- La frequenza di ombreggiatura per vertice (anche noto come per primitiva) è valida quando un viewport viene usato e `SV_ViewportArrayIndex` non viene scritto.
- Se la funzionalità *SupportsPerVertexShadingRateWithMultipleViewports* è impostata su, è possibile utilizzare la frequenza di vertice per singolo oggetto con più di un viewport `true` . In tal caso, è inoltre possibile utilizzare tale frequenza quando `SV_ViewportArrayIndex` viene scritto in.

### <a name="list-of-capabilities"></a>Elenco di funzionalità
- *AdditionalShadingRatesSupported*
  - Tipo booleano.
  - Indica se le dimensioni dei pixel grossolani 4, 4x2 e 4x4 sono supportate per il rendering con campionamento singolo. e indica se le dimensioni del pixel grossolano 4 sono supportate per 2x MSAA.
- *SupportsPerVertexShadingRateWithMultipleViewports*
  - Tipo booleano.
  - Indica se è possibile utilizzare più di un viewport con la frequenza di ombreggiatura per vertice (anche nota come per primitiva).

## <a name="specifying-shading-rate"></a>Specifica della velocità di ombreggiatura
Per una maggiore flessibilità nelle applicazioni, è disponibile un'ampia gamma di meccanismi per controllare la velocità di ombreggiatura. Sono disponibili diversi meccanismi a seconda del livello di funzionalità hardware.

### <a name="command-list"></a>Elenco comandi
Questo è il meccanismo più semplice per impostare la velocità di ombreggiatura. È disponibile in tutti i livelli.

L'applicazione può specificare una dimensione in pixel grossolana usando il [metodo **ID3D12GraphicsCommandList5:: RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate). Tale API accetta un solo argomento enum. L'API fornisce un controllo generale del livello di qualità per il rendering &mdash; della possibilità di impostare la velocità di ombreggiatura per ogni singolo progetto.

I valori per questo stato vengono espressi tramite l'enumerazione [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) .

#### <a name="coarse-pixel-size-support"></a>Supporto delle dimensioni del pixel grossolano
Le frequenze di ombreggiatura 1x1, 1x2, 2x2 e 2x2 sono supportate in tutti i livelli.

È disponibile una funzionalità, *AdditionalShadingRatesSupported*, per indicare se 4, 4x2 e 4x4 sono supportati nel dispositivo.

### <a name="screen-space-image-image-based"></a>Immagine dello spazio dello schermo (basata su immagini)
Nel livello 2 e versioni successive è possibile specificare la frequenza di ombreggiatura in pixel con un'immagine dello spazio sullo schermo.

L'immagine dello spazio dello schermo consente all'applicazione di creare un'immagine di "maschera del livello di dettaglio (LOD) che indica le aree di qualità variabile, ad esempio le aree che saranno coperte da sfocatura di movimento, sfocatura di profondità del campo, oggetti trasparenti o elementi dell'interfaccia utente HUD. La risoluzione dell'immagine è in macroblocchi; non si trova nella risoluzione della destinazione di rendering. In altre parole, i dati della frequenza di ombreggiatura vengono specificati a una granularità dei riquadri 8x8 Virtual o 16x16 pixel, come indicato dalle dimensioni del riquadro VRS.

#### <a name="tile-size"></a>Dimensioni del riquadro
L'applicazione può eseguire una query su un'API per recuperare le dimensioni del riquadro VRS supportate per il dispositivo.

I riquadri sono quadrati e le dimensioni si riferiscono alla larghezza o all'altezza del riquadro nei Texel.

Se l'hardware non supporta l'ombreggiatura a frequenza variabile di livello 2, la query della funzionalità per le dimensioni del riquadro restituisce 0.

Se *l'hardware supporta* l'ombreggiatura a frequenza variabile di livello 2, le dimensioni del riquadro corrispondono a uno di questi valori.

- 8
- 16
- 32

#### <a name="screen-space-image-size"></a>Dimensioni dell'immagine dello spazio dello schermo
Per una destinazione di rendering di dimensioni {rtWidth, rtHeight}, usando una dimensione del riquadro specificata denominata **VRSTileSize**, l'immagine dello spazio dello schermo che verrà coperta è di queste dimensioni.

```cpp
{ ceil((float)rtWidth / VRSTileSize), ceil((float)rtHeight / VRSTileSize) }
```

La parte superiore sinistra dell'immagine dello spazio dello schermo (0, 0) è bloccata nella parte superiore sinistra della destinazione di rendering (0,0).

Per cercare la coordinata (x, y) di un riquadro che corrisponde a una posizione specifica nella destinazione di rendering, dividere le coordinate dello spazio della finestra (x, y) in base alle dimensioni del riquadro, ignorando i bit frazionari.

Se l'immagine dello spazio dello schermo è maggiore di quella necessaria per una determinata destinazione di rendering, le parti aggiuntive a destra e/o in basso non vengono usate.

Se l'immagine dello spazio dello schermo è troppo piccola per una determinata destinazione di rendering, qualsiasi tentativo di lettura dall'immagine oltre gli extent effettivi genera una frequenza di ombreggiatura predefinita di 1x1. Ciò è dovuto al fatto che la parte superiore sinistra dell'immagine dello spazio dello schermo (0,0) è bloccata in alto a sinistra della destinazione di rendering (0,0) e "lettura oltre gli extent della destinazione di rendering" significa che la lettura dei valori per x e y è troppo grande.

#### <a name="format-layout-resource-properties"></a>Formato, layout, proprietà delle risorse
Il formato di questa superficie è una superficie a 8 bit a canale singolo ([**DXGI_FORMAT_R8_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

La risorsa è **TEXTURE2D** della dimensione.

Non può essere arrayed o mipped. Deve disporre in modo esplicito di un livello MIP.

Il numero di esempio è 1 e la qualità di esempio è 0.

Il layout della trama è **sconosciuto**. Non può essere implicitamente un layout di riga, perché non è consentito l'adattatore incrociato.

Il modo previsto per il popolamento dei dati dell'immagine dello spazio dello schermo è
1. Scrivere i dati usando un compute shader; l'immagine dello spazio dello schermo è associata come UAV o
2. Copiare i dati nell'immagine dello spazio dello schermo.

Quando si crea l'immagine dello spazio dello schermo, questi flag sono consentiti.

- NONE
- ALLOW_UNORDERED_ACCESS
- DENY_SHADER_RESOURCE

Questi flag non sono consentiti.

- ALLOW_RENDER_TARGET
- ALLOW_DEPTH_STENCIL
- ALLOW_CROSS_ADAPTER
- ALLOW_SIMULTANEOUS_ACCESS
- VIDEO_DECODE_REFERENCE_ONLY

Il tipo di heap della risorsa non può essere UPLOAD né READBACK.

Non è possibile SIMULTANEOUS_ACCESS la risorsa. La risorsa non è consentita come adattatore incrociato.

#### <a name="data"></a>Data
Ogni byte dell'immagine dello spazio dello schermo corrisponde a un valore dell'enumerazione [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)  .

#### <a name="resource-state"></a>Stato della risorsa
Una risorsa deve essere passata in uno stato di sola lettura quando viene usata come immagine dello spazio sullo schermo. A questo scopo viene definito uno stato di sola lettura, [**D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

La risorsa immagine viene passata da tale stato per diventare nuovamente scrivibile.

#### <a name="setting-the-image"></a>Impostazione dell'immagine
L'immagine dello spazio dello schermo per specificare la frequenza dello shader viene impostata nell'elenco dei comandi.

Una risorsa che è stata impostata come origine della frequenza ombreggiatura non può essere letta o scritta da alcuna fase dello shader.

`null`È possibile impostare un'immagine dello spazio sullo schermo per specificare la frequenza dello shader. Questo ha l'effetto che 1x1 viene usato in modo coerente come contributo dall'immagine dello spazio sullo schermo. L'immagine dello spazio sullo schermo può essere inizialmente considerata come impostata su `null` .

#### <a name="promotion-and-decay"></a>Promozione e decadimento
Una risorsa immagine dello spazio sullo schermo non presenta alcuna implicazione speciale rispetto alla promozione o al decadimento.

### <a name="per-primitive-attribute"></a>Attributo per primitive
Un attributo per primitiva aggiunge la possibilità di specificare un termine di frequenza ombreggiatura come attributo da un vertice che provoca un errore. Questo attributo è ombreggiato &mdash; , ovvero viene propagato a tutti i pixel del triangolo o della primitiva della linea corrente. L'uso di un attributo per primitivo può consentire un controllo più granulare della qualità dell'immagine rispetto agli altri identificatori di velocità ombreggiatura.

L'attributo per primitivo è una semantica impostabile denominata `SV_ShadingRate` . `SV_ShadingRate` esiste come parte del [modello HLSL shader 6,4](/windows/desktop/direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12).

Se un set di VS o GS `SV_ShadingRate` , ma VRS non è abilitato, l'impostazione semantica non ha alcun effetto. Se non viene specificato alcun valore per `SV_ShadingRate` la primitiva, viene utilizzato un valore di frequenza ombreggiatura pari a 1x1 come contributo per primitivo.

### <a name="combining-shading-rate-factors"></a>Combinazione di fattori di frequenza ombreggiatura
Le varie origini della frequenza ombreggiatura vengono applicate in sequenza usando questo diagramma.

![combinatori](images/Combiners.PNG "Combinatori ombreggiatura")

Ogni coppia di A e B viene combinata utilizzando un combinatore.

\* Quando si specifica una frequenza dello shader per attributo vertex.

- Se viene usato un geometry shader, è possibile specificare la frequenza di ombreggiatura.
- Se non si usa un geometry shader, la frequenza di ombreggiatura viene specificata dal vertice che provoca l'ombreggiatura.

#### <a name="list-of-combiners"></a>Elenco di combinatori
Sono supportati i combinatori seguenti. Utilizzando un combinatore (C) e due input (A e B).

- **PassThrough**. C. XY = A. XY.
- **Eseguire l'override** di. C. XY = B. XY.
- **Qualità superiore**. C. XY = min (A. XY, B. XY).
- **Qualità inferiore**. C. XY = Max (A. XY, B. XY).
- **Applicare il costo B rispetto A un**. C. XY = min (maxRate, A. XY + B. XY).

dove `maxRate` è la dimensione massima consentita del pixel grossolano sul dispositivo. Questo sarebbe

- **D3D12_AXIS_SHADING_RATE_2X** (ovvero, un valore pari a 1), se AdditionalShadingRatesSupported è `false` .
- **D3D12_AXIS_SHADING_RATE_4X** (ovvero, un valore pari a 2), se AdditionalShadingRatesSupported è `true` .

La scelta del combinatore per l'ombreggiatura a frequenza variabile viene impostata nell'elenco dei comandi tramite [**ID3D12GraphicsCommandList5:: RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate).

Se non sono mai impostati combinatori, rimangono in corrispondenza del valore predefinito, ovvero PASSTHROUGH.

Se l'origine a un combinatore è una [**D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate), che non è consentita nella tabella di supporto, l'input viene purificato a una *velocità di ombreggiatura supportata.*

Se l'output di un combinatore non corrisponde a una velocità di ombreggiatura supportata sulla piattaforma, il risultato viene purificato a una *velocità di ombreggiatura supportata.*

### <a name="default-state-and-state-clearing"></a>Stato predefinito e cancellazione dello stato
Tutte le origini di frequenza ombreggiatura, ovvero

- frequenza specificata per lo stato della pipeline, specificata nell'elenco dei comandi.
- frequenza specificata per l'immagine dello spazio dello schermo e
- attributo per primitivo

il valore predefinito è **D3D12_SHADING_RATE_1X1**. I combinatori predefiniti sono {PASSTHROUGH, PASSTHROUGH}.

Se non viene specificata alcuna immagine dello spazio dello schermo, viene dedotta una frequenza di ombreggiatura di 1x1 da tale origine.

Se non è specificato alcun attributo per primitive, viene dedotto un tasso di ombreggiatura di 1x1 da tale origine.

[ID3D12CommandList:: ClearState](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate) Reimposta la frequenza specificata dallo stato della pipeline sul valore predefinito e la selezione dell'immagine dello spazio dello schermo sul valore predefinito "nessuna immagine dello spazio dello schermo".

## <a name="querying-shading-rate-by-using-sv_shadingrate"></a>Esecuzione di query sulla frequenza ombreggiatura utilizzando SV_ShadingRate
È utile sapere quale frequenza di ombreggiatura è stata selezionata dall'hardware in una determinata chiamata a pixel shader. Questo potrebbe consentire una serie di ottimizzazioni nel codice PS. Una variabile di sistema solo PS, `SV_ShadingRate` , fornisce informazioni sulla velocità di ombreggiatura.

### <a name="type"></a>Tipo
Il tipo di questa semantica è uint.

### <a name="data-interpretation"></a>Interpretazione dei dati
I dati vengono interpretati come valore dell'enumerazione [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) .

### <a name="if-vrs-is-not-being-used"></a>Se VRS non è in uso
Se non si usa l'ombreggiatura in pixel grossolani, `SV_ShadingRate` viene letto come valore di 1x1, che indica i pixel di precisione.

### <a name="behavior-under-sample-based-execution"></a>Comportamento nell'esecuzione basata su esempio
Un pixel shader non riesce a compilare se immette `SV_ShadingRate` e usa anche l'esecuzione basata su campione &mdash; , ad esempio, inserendo `SV_SampleIndex` o usando la parola chiave di interpolazione di esempio.

> ### <a name="remarks-on-deferred-shading"></a>Osservazioni sull'ombreggiatura posticipata
>
> Un passaggio di illuminazione dell'applicazione ombreggiatura posticipata potrebbe dover sapere quale frequenza di ombreggiatura è stata usata per l'area dello schermo. In questo modo, le spedite del pass di illuminazione possono essere avviate a una velocità più grossolana. La `SV_ShadingRate` variabile può essere utilizzata per eseguire questa operazione se viene scritta in gbuffer.

## <a name="depth-and-stencil"></a>Depth e stencil
Quando si utilizza l'ombreggiatura in pixel grossolani, la profondità e lo stencil e il code coverage vengono sempre calcolati e emessi alla risoluzione di esempio completa.

## <a name="using-the-shading-rate-requested"></a>Uso della velocità di ombreggiatura richiesta
Per tutti i livelli, si prevede che se è richiesta una frequenza di ombreggiatura ed è supportata nella combinazione di dispositivo e MSAA, si tratta della velocità di ombreggiatura fornita dall'hardware.

Una frequenza di ombreggiatura richiesta indica una frequenza di ombreggiatura calcolata come output dei combinatori (vedere la sezione [combinazione di fattori di frequenza di ombreggiatura](#combining-shading-rate-factors) in questo argomento).

Una frequenza di ombreggiatura supportata è 1x1, 1x2, 2x1 o 2x2 in un'operazione di rendering in cui il numero di campioni è minore o uguale a quattro. Se la funzionalità *AdditionalShadingRatesSupported* è `true` , le tariffe di ombreggiatura di 4, 4x2 e 4x4 sono supportate anche per alcuni conteggi di esempio (vedere la tabella nella sezione [with variable-rate shading (VRS)](#with-variable-rate-shading-vrs) in questo argomento).

## <a name="screen-space-derivatives"></a>Derivati dallo spazio dello schermo
I calcoli delle sfumature pixel-to-adiacent pixel sono interessati dall'ombreggiatura dei pixel grossolani. Se, ad esempio, vengono utilizzati 2x2 pixel grossolani, una sfumatura avrà una dimensione doppia rispetto a quando non vengono utilizzati i pixel grossolani. L'applicazione potrebbe voler modificare gli shader per compensare questa &mdash; o meno, a seconda delle funzionalità desiderate.

Poiché i MIP vengono scelti in base a uno spazio derivato dallo schermo, l'utilizzo dell'ombreggiatura di pixel grossolani influiscono sulla selezione MIP. L'utilizzo dell'ombreggiatura in pixel grossolano causa la selezione di MIP meno dettagliati rispetto a quando non vengono usati pixel grossolani.

## <a name="attribute-interpolation"></a>Interpolazione degli attributi
Gli input per un pixel shader possono essere interpolati in base ai vertici di origine. Poiché l'ombreggiatura a frequenza variabile influiscono sulle aree della destinazione scritta da ogni chiamata del pixel shader, interagisce con l'interpolazione degli attributi. I tre tipi di interpolazione sono Center, baricentro e Sample.

### <a name="center"></a>Center
La posizione di interpolazione centrale per un pixel grossolano è il centro geometrico dell'area dei pixel grossolani completa. `SV_Position` viene sempre interpolato al centro dell'area dei pixel grossolani.

### <a name="centroid"></a>Centro
Quando si usa l'ombreggiatura in pixel grossolani con MSAA, per ogni pixel sottile verranno comunque scritte nel numero completo di campioni allocati per il livello MSAA di destinazione. Quindi, la posizione di interpolazione centrale considererà tutti i campioni per i pixel sottili all'interno di pixel grossolani. Detto questo, il percorso di interpolazione del centro viene definito come primo campione trattato, in ordine crescente di indice di esempio. Il code coverage effettivo dell'esempio è e-ed è il bit corrispondente dello stato SampleMask del rasterizzatore.

> [!NOTE]
> Quando si usa l'ombreggiatura in pixel grossolani nel livello 1, SampleMask è sempre una maschera completa. Se SampleMask è configurato per non essere una maschera completa, l'ombreggiatura del pixel grossolano è disabilitata nel livello 1.

### <a name="sample-based-execution"></a>Esecuzione basata su esempio
L'esecuzione basata su campionamento o il *sovracampionamento* &mdash; causato dall'utilizzo della funzionalità di interpolazione di esempio &mdash; può essere utilizzato con l'ombreggiatura di pixel grossolani e determina la richiamata del pixel shader per campione. Per le destinazioni del conteggio campione N, il pixel shader viene richiamato N volte per fine pixel.

### <a name="evaluateattributesnapped"></a>EvaluateAttributeSnapped
Gli intrinseci del modello pull non sono compatibili con l'ombreggiatura in pixel grossolana nel livello 1. Se viene eseguito un tentativo di usare oggetti intrinseci del modello pull con ombreggiatura di pixel grossolana sul livello 1, l'ombreggiatura di pixel grossolani viene disabilitata automaticamente.

L'oggetto intrinseco può `EvaluateAttributeSnapped` essere utilizzato con l'ombreggiatura in pixel grossolana nel livello 2. La sintassi è identica a quella che è sempre stata.

```hlsl
numeric EvaluateAttributeSnapped(   
    in attrib numeric value, 
    in int2 offset);
```

Per context, `EvaluateAttributeSnapped` presenta un parametro offset con due campi. Quando viene usato senza ombreggiatura di pixel grossolani, vengono usati solo i quattro bit di ordine inferiore all'esterno della 32 completa. Questi quattro bit rappresentano l'intervallo [-8, 7]. Questo intervallo si estende su una griglia 16x16 all'interno di un pixel. L'intervallo è tale che i bordi superiore e sinistro del pixel sono inclusi e i bordi inferiore e destro non lo sono. Offset (-8,-8) si trova nell'angolo superiore sinistro e offset (7, 7) è nell'angolo inferiore destro. Offset (0, 0) è il centro del pixel.

Se usato con ombreggiatura in pixel grossolano, `EvaluateAttributeSnapped` il parametro offset di è in grado di specificare una più ampia gamma di posizioni. Il parametro offset seleziona una griglia 16x16 per ogni pixel fine e sono presenti più pixel sottili. L'intervallo di esprimibile e il numero di bit conseguente utilizzati dipendono dalle dimensioni dei pixel grossolani. Sono inclusi i bordi superiore e sinistro del pixel grossolano e i bordi inferiore e destro non lo sono.

La tabella seguente descrive l'interpretazione del `EvaluateAttributeSnapped` parametro offset per ogni dimensione in pixel grossolani.

#### <a name="evaluateattributesnappeds-offset-range"></a>Intervallo di offset di EvaluateAttributeSnapped

|Dimensioni pixel grossolane  |Intervallo indicizzabile             |Dimensione intervallo rappresentabile  |Numero di bit necessari {x, y}  |Maschera binaria di bit utilizzabili          |    
|------------------:|---------------------------:|-------------------------:|-----------------------------:|-----------------------------------:|    
|1x1 (fine)         |{ \[ -8, 7 \] , \[ -8, 7 \] }      |{16, 16}                  |{4, 4}                        |{000000000000xxxx, 000000000000xxxx}|    
|1x2                |{ \[ -8, 7 \] , \[ -16, 15 \] }    |{16, 32}                  |{4, 5}                        |{000000000000xxxx, 00000000000xxxxx}|    
|2x1                |{ \[ -16, 15 \] , \[ -8, 7 \] }    |{32, 16}                  |{5, 4}                        |{00000000000xxxxx, 000000000000xxxx}|    
|2x2                |{ \[ -16, 15 \] , \[ -16, 15 \] }  |{32, 32}                  |{5, 5}                        |{00000000000xxxxx, 00000000000xxxxx}|    
|4                |{ \[ -16, 15 \] , \[ -32, 31 \] }  |{32, 64}                  |{5, 6}                        |{00000000000xxxxx, 0000000000xxxxxx}|    
|4x2                |{ \[ -32, 31 \] , \[ -16, 15 \] }  |{64, 32}                  |{6, 5}                        |{0000000000xxxxxx, 00000000000xxxxx}|    
|4x4                |{ \[ -32, 31 \] , \[ -32, 31 \] }  |{64, 64}                  |{6, 6}                        |{0000000000xxxxxx, 0000000000xxxxxx}|   

Le tabelle seguenti sono una guida per la conversione a dalla rappresentazione a virgola fissa a quella decimale e frazionaria. Il primo bit utilizzabile nella maschera binaria è il bit di segno e il resto della maschera binaria comprende la parte numerica.

Lo schema numerico per i valori a quattro bit passati a `EvaluateAttributeSnapped` non è specifico per l'ombreggiatura a frequenza variabile. Questa operazione viene ripetuta qui per completezza.

Per i valori a quattro bit.

| Valore binario | Decimal  | Precisione |
|-------------:|---------:|-----------:|
|         1000 |-0,5 f     |-8/16     |
|         1001 |-0.4375 f  |-7/16|    |
|         1010 |-0.375 f   |-6/16|    |
|         1011 |-0.3125 f  |-5/16     |
|         1100 |-0,25 f    |-4/16     |
|         1101 |-0.1875 f  |-3/16     |
|         1110 |-0,125 f   |-2/16     |
|         1111 |-0.0625 f  |-1/16      |
|         0000 |0,0 f      |0 / 16      |
|         0001 |-0.0625 f  |1 / 16      |
|         0010 |-0,125 f   |2 / 16      |
|         0011 |-0.1875 f  |3 / 16      |
|         0100 |-0,25 f    |4 / 16      |
|         0101 |-0.3125 f  |5 / 16      |
|         0110 |-0.375 f   |6 / 16      |
|         0111 |-0.4375 f  |7 / 16      |

Per i valori a cinque bit.

| Valore binario | Decimal  | Precisione |
|-------------:|---------:|-----------:|
|        10000 |-1        |-16/16    |
|        10001 |-0,9375   |-15/16    |
|        10010 |-0,875    |-14/16    |
|        10011 |-0,8125   |-13/16    |
|        10100 |-0.75     |-12/16    |
|        10101 |-0,6875   |-11/16    |
|        10110 |-0,625    |-10/16    |
|        10111 |-0,5625   |-9/16     |
|        11000 |-0,5      |-8/16     |
|        11001 |-0,4375   |-7/16     |
|        11010 |-0,375    |-6/16     |
|        11011 |-0,3125   |-5/16     |
|        11100 |-0.25     |-4/16     |
|        11101 |-0,1875   |-3/16     |
|        11110 |-0,125    |-2/16     |
|        11111 |-0,0625   |-1/16     |
|        00000 |0         |0 / 16      |
|        00001 |0,0625    |1 / 16      |
|        00010 |0,125     |2 / 16      |
|        00011 |0,1875    |3 / 16      |
|        00100 |0,25      |4 / 16      |
|        00101 |0,3125    |5 / 16      |
|        00110 |0,375     |6 / 16      |
|        00111 |0,4375    |7 / 16      |
|        01000 |0.5       |8 / 16      |
|        01001 |0,5625    |9 / 16      |
|        01010 |0,625     |10 / 16     |
|        01011 |0,6875    |11 / 16     |
|        01100 |0,75      |12 / 16     |
|        01101 |0,8125    |13 / 16     |
|        01110 |0,875     |14 / 16     |
|        01111 |0,9375    |15 / 16     |

Per i valori a sei bit.

| Valore binario | Decimal  | Precisione |
|-------------:|---------:|-----------:|
|       100000 |-2        |-32/16    |
|       100001 |-1,9375   |-31/16    |
|       100010 |-1,875    |-30/16    |
|       100011 |-1,8125   |-29/16    |
|       100100 |-1,75     |-28/16    |
|       100101 |-1,6875   |-27/16    |
|       100110 |-1,625    |-26/16    |
|       100111 |-1,5625   |-25/16    |
|       101000 |-1,5      |-24/16    |
|       101001 |-1,4375   |-23/16    |
|       101010 |-1,375    |-22/16    |
|       101011 |-1,3125   |-21/16    |
|       101100 |-1.25     |-20/16    |
|       101101 |-1,1875   |-19/16    |
|       101110 |-1,125    |-18/16    |
|       101111 |-1,0625   |-17/16    |
|       110000 |-1        |-16/16    |
|       110001 |-0,9375   |-15/16    |
|       110010 |-0,875    |-14/16    |
|       110011 |-0,8125   |-13/16    |
|       110100 |-0.75     |-12/16    |
|       110101 |-0,6875   |-11/16    |
|       110110 |-0,625    |-10/16    |
|       110111 |-0,5625   |-9/16     |
|       111000 |-0,5      |-8/16     |
|       111001 |-0,4375   |-7/16     |
|       111010 |-0,375    |-6/16     |
|       111011 |-0,3125   |-5/16     |
|       111100 |-0.25     |-4/16     |
|       111101 |-0,1875   |-3/16     |
|       111110 |-0,125    |-2/16     |
|       111111 |-0,0625   |-1/16     |
|       000000 |0         |0 / 16      |
|       000001 |0,0625    |1 / 16      |
|       000010 |0,125     |2 / 16      |
|       000011 |0,1875    |3 / 16      |
|       000100 |0,25      |4 / 16      |
|       000101 |0,3125    |5 / 16      |
|       000110 |0,375     |6 / 16      |
|       000111 |0,4375    |7 / 16      |
|       001000 |0.5       |8 / 16      |
|       001001 |0,5625    |9 / 16      |
|       001010 |0,625     |10 / 16     |
|       001011 |0,6875    |11 / 16     |
|       001100 |0,75      |12 / 16     |
|       001101 |0,8125    |13 / 16     |
|       001110 |0,875     |14 / 16     |
|       001111 |0,9375    |15 / 16     |
|       010000 |1         |16 / 16     |
|       010001 |1,0625    |17 / 16     |
|       010010 |1,125     |18 / 16     |
|       010011 |1,1875    |19 / 16     |
|       010100 |1,25      |20 / 16     |
|       010101 |1,3125    |21 / 16     |
|       010110 |1,375     |22 / 16     |
|       010111 |1,4375    |23 / 16     |
|       011000 |1.5       |24 / 16     |
|       011001 |1,5625    |25 / 16     |
|       011010 |1,625     |26 / 16     |
|       011011 |1,6875    |27 / 16     |
|       011100 |1,75      |28 / 16     |
|       011101 |1,8125    |29 / 16     |
|       011110 |1,875     |30 / 16     |
|       011111 |1,9375    |31 / 16     |

Analogamente a quanto avviene con i pixel sottili, la `EvaluateAttributeSnapped` griglia delle posizioni valutabili è centrata sul centro dei pixel grossolani quando si usa l'ombreggiatura in pixel grossolani.

## <a name="setsamplepositions"></a>SetSamplePositions
Quando l'API [**ID3D12GraphicsCommandList1:: SetSamplePositions**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) viene usata con l'ombreggiatura grossolana, l'API imposta le posizioni di esempio per i pixel sottili.

## <a name="sv_coverage"></a>SV_Coverage
Se `SV_Coverage` viene dichiarato come input o output dello shader nel livello 1, l'ombreggiatura del pixel grossolano è disabilitata.

È possibile utilizzare la `SV_Coverage` semantica con ombreggiatura in pixel grossolana sul livello 2 e riflette gli esempi di una destinazione MSAA in fase di scrittura.

Quando si usa l'ombreggiatura in pixel grossolani che &mdash; consente a più pixel di origine di includere un riquadro &mdash; , la maschera di copertura rappresenta tutti gli esempi che provengono da tale riquadro.

Data la compatibilità dell'ombreggiatura del pixel grossolano con MSAA, il numero di bit di code coverage che è necessario specificare può variare. Ad esempio, con una risorsa MSAA 4x che usa [**D3D12_SHADING_RATE_2x2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate), ogni pixel grossolano scrive su quattro pixel sottili e ogni pixel sottile ha quattro campioni. Ciò significa che ogni pixel grossolano scrive in un totale di 4 * 4 = 16 campioni.

### <a name="number-of-coverage-bits-needed"></a>Numero di bit di code coverage necessari
Nella tabella seguente viene indicato il numero di bit di code coverage necessari per ogni combinazione di dimensioni in pixel grossolana e livello MSAA.

![NumberOfCoverageBits](images/NumberOfCoverageBits.PNG "Bit di code coverage")

Come indicato nella tabella, non è possibile usare i pixel grossolani per scrivere in più di 16 campioni alla volta usando la funzionalità di ombreggiatura a frequenza variabile esposta tramite Direct3D 12. Questa restrizione è dovuta ai vincoli di Direct3D 12 relativi ai livelli di MSAA consentiti con le dimensioni dei pixel grossolani (vedere la tabella nella sezione [con l'ombreggiatura a frequenza variabile (VRS)](#with-variable-rate-shading-vrs) in questo argomento).

### <a name="ordering-and-format-of-bits-in-the-coverage-mask"></a>Ordinamento e formato dei bit nella maschera di copertura
I bit della maschera di code coverage rispettano un ordine ben definito. La maschera è costituita da code coverage dai pixel da sinistra a destra, quindi dall'alto verso il basso (colonna-principale). I bit di code coverage sono i bit meno significativi della semantica di code coverage e vengono compressi in modo denso.

La tabella seguente illustra il formato della maschera di copertura per le combinazioni supportate di dimensioni in pixel grossolane e di MSAA.

![Coverage1x](images/Coverage1x.PNG "Copertura a 1x")

La tabella seguente descrive 2x MSAA pixel, in cui ogni pixel presenta due campioni di indici 0 e 1.

Il posizionamento delle etichette degli esempi sui pixel è a scopo illustrativo e non trasmette necessariamente le posizioni spaziali {X, Y} degli esempi su tale pixel; in particolare, dato che le posizioni di esempio possono essere modificate a livello di codice. Agli esempi viene fatto riferimento tramite l'indice in base zero.

![Coverage2x](images/Coverage2x.PNG "Copertura a 2x")

La tabella seguente mostra 4x pixel MSAA, in cui ogni pixel ha quattro campioni di indici 0, 1, 2 e 3.

![Coverage4x](images/Coverage4x.PNG "Copertura a 4x")

## <a name="discard"></a>Discard
Quando si usa la semantica HLSL `discard` con ombreggiatura in pixel grossolani, i pixel grossolani vengono scartati.

## <a name="target-independent-rasterization-tir"></a>Rasterizzazione indipendente dalla destinazione (TIR)
TIR non è supportato quando si usa l'ombreggiatura in pixel grossolani.

## <a name="raster-order-views-rovs"></a>Viste degli ordini raster (ROV)
Gli Interlock ROV vengono specificati come operativi con granularità fine pixel. Se viene eseguita un'ombreggiatura per esempio, gli Interlock funzionano con la granularità di esempio.

## <a name="conservative-rasterization"></a>Rasterizzazione conservativa
È possibile utilizzare la rasterizzazione conservativa con ombreggiatura a frequenza variabile. Quando si usa la rasterizzazione conservativa con ombreggiatura in pixel grossolani, i pixel sottili all'interno di pixel grossolani vengono rasterizzati in maniera prudenziale, con una copertura completa.

### <a name="coverage"></a>Copertura
Quando si utilizza la rasterizzazione conservativa, la semantica di code coverage contiene maschere complete per i pixel sottili analizzati e 0 per i pixel sottili non analizzati.

## <a name="bundles"></a>Bundle
È possibile chiamare API ombreggiate a frequenza variabile in un bundle.

## <a name="render-passes"></a>Passaggi di rendering
È possibile chiamare le API di ombreggiatura a frequenza variabile in un [passaggio di rendering](/windows/desktop/direct3d12/direct3d-12-render-passes).

## <a name="calling-the-vrs-apis"></a>Chiamata delle API VRS
Questa sezione seguente descrive il modo in cui l'ombreggiatura a frequenza variabile è accessibile all'applicazione tramite Direct3D 12.

### <a name="capability-querying"></a>Esecuzione di query sulle funzionalità

Per eseguire una query per la funzionalità di ombreggiatura a frequenza variabile dell'adapter, chiamare [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) con [**D3D12_FEATURE::D 3D12_FEATURE_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)e fornire una [struttura **D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) per la funzione da inserire automaticamente. La struttura **D3D12_FEATURE_DATA_D3D12_OPTIONS6** contiene diversi membri, tra cui uno che corrisponde al tipo enumerato [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) (D3D12_FEATURE_DATA_D3D12_OPTIONS6:: VariableShadingRateTier) e uno che indica se l'elaborazione in background è supportata (D3D12_FEATURE_DATA_D3D12_OPTIONS6:: BackgroundProcessingSupported).

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

### <a name="shading-rates"></a>Frequenze ombreggiate

I valori nell'enumerazione [ **D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) sono organizzati in modo che le frequenze di ombreggiatura siano facilmente decomponibili in due assi, in cui i valori di ogni asse sono rappresentati in modo compatto nello spazio logaritmico in base all' [enumerazione **D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate).

È possibile creare una macro per comporre due frequenze di ombreggiatura dell'asse in una frequenza ombreggiata come questa.

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

Questi possono essere usati per analizzare e comprendere `SV_ShaderRate` .

> [!NOTE]
> Questa interpretazione dei dati è incentrata sulla descrizione dell'immagine dello spazio sullo schermo, che può essere modificata dagli shader. Questo argomento viene illustrato più avanti nelle sezioni precedenti. Non è tuttavia necessario avere una definizione coerente delle dimensioni dei pixel grossolani da usare ovunque, ad esempio quando si imposta la frequenza di ombreggiatura a livello di comando.

### <a name="setting-command-level-shading-rate-and-combiners"></a>Impostazione della frequenza di ombreggiatura e combinatori a livello di comando
La frequenza di ombreggiatura e, facoltativamente, i combinatori vengono specificati tramite il metodo [**ID3D12GraphicsCommandList5:: RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate) . Si passa un valore [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) per la velocità ombreggiatura di base e una matrice facoltativa di valori [D3D12_SHADING_RATE_COMBINER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner) .

### <a name="preparing-the-screen-space-image"></a>Preparazione dell'immagine dello spazio dello schermo
Lo stato della risorsa di sola lettura che designa un'immagine del tasso di ombreggiatura utilizzabile viene definito come [D3D12_RESOURCE_STATES::D 3D12_RESOURCE_STATE_SHADING_RATE_SOURCE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

### <a name="setting-the-screen-space-image"></a>Impostazione dell'immagine dello spazio dello schermo
È possibile specificare l'immagine dello spazio dello schermo tramite il metodo [**ID3D12GraphicsCommandList5:: RSSetShadingRateImage**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrateimage) .

```cpp
m_commandList->RSSetShadingRateImage(screenSpaceImage);
```

### <a name="querying-the-tile-size"></a>Esecuzione di query sulle dimensioni del riquadro
È possibile eseguire una query sulle dimensioni del riquadro dal membro [**D3D12_FEATURE_DATA_D3D12_OPTIONS6:: ShadingRateImageTileSize**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) . Vedere le [query sulle funzionalità](#capability-querying) sopra indicate.

Viene recuperata una dimensione, perché le dimensioni orizzontali e verticali sono sempre uguali. Se la funzionalità del sistema è [**D3D12_SHADING_RATE_TIER_NOT_SUPPORTED**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier), le dimensioni del riquadro restituite sono pari a 0.
