---
title: Semantica
description: Una semantica è una stringa associata a un input o output dello shader che fornisce informazioni sull'uso previsto di un parametro.
ms.assetid: 6f5c504c-1940-4d1c-b594-a2132599376b
keywords:
- BINORMAL, semantica (DirectX HLSL)
- BLENDINDICES, semantica (DirectX HLSL)
- BLENDWEIGHT, semantica (DirectX HLSL)
- COLOR, semantica (DirectX HLSL)
- SEMANTIC, semantica (DirectX HLSL)
- POSITIONT, semantica (DirectX HLSL)
- PSIZE, semantica (HLSL DirectX)
- TANGENT, semantica (DirectX HLSL)
- TESSFACTOR, semantica (HLSL DirectX)
- TEXCOORD, semantica (DirectX HLSL)
- VFACE, semantica (DirectX HLSL)
- VPOS, semantica (DirectX HLSL)
- System-Value semantica
- Semantica dei valori di sistema
- ClipDistance, semantica (DirectX HLSL)
- Code coverage, semantica (DirectX HLSL)
- CullDistance, semantica (DirectX HLSL)
- Profondità, semantica (DirectX HLSL)
- InstanceID, semantica (HLSL DirectX)
- IsFrontFace, semantica (DirectX HLSL)
- Posizione, semantica (DirectX HLSL)
- PrimitiveID, semantica (DirectX HLSL)
- RenderTargetArrayIndex, semantica (DirectX HLSL)
- Destinazione, semantica (DirectX HLSL)
- SampleIndex, semantica (DirectX HLSL)
- VertexID, semantica (DirectX HLSL)
- ViewportArrayIndex, semantica (DirectX HLSL)
- SV_ClipDistance, semantica (DirectX HLSL)
- SV_CullDistance, semantica (DirectX HLSL)
- SV_Depth, semantica (DirectX HLSL)
- SV_DepthGreaterEqual, semantica (DirectX HLSL)
- SV_DepthLessEqual, semantica (DirectX HLSL)
- SV_IsFrontFace, semantica (DirectX HLSL)
- SV_Position, semantica (DirectX HLSL)
- SV_RenderTargetArrayIndex, semantica (DirectX HLSL)
- SV_Target, semantica (DirectX HLSL)
- SV_ViewportArrayIndex, semantica (DirectX HLSL)
- SV_InstanceID, semantica (DirectX HLSL)
- SV_PrimitiveID, semantica (DirectX HLSL)
- SV_VertexID, semantica (DirectX HLSL)
- SV_Coverage, semantica (DirectX HLSL)
- SV_SampleIndex, semantica (DirectX HLSL)
- SV_InnerCoverage, semanitcs (DirectX HLSL)
- SV_StencilRef, semantica (DirectX HLSL)
- SV_GroupID, semantica (DirectX HLSL)
- SV_GroupThreadID, semantica (DirectX HLSL)
- SV_DispatchThreadID semantica (DirectX HLSL)
- SV_GroupIndex, semantica (DirectX HLSL)
- SV_OutputControlPointID, semantica (DirectX HLSL)
- SV_TessFactor, semantica (DirectX HLSL)
- SV_InsideTessFactor, semantica (DirectX HLSL)
- SV_DomainLocation, semantica (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e8979b4e4842a4c84317b456802ed8f1beefea35
ms.sourcegitcommit: 1d3c59a7066a75facc0565027251cad1ca1dd9c9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/18/2021
ms.locfileid: "107594166"
---
# <a name="semantics"></a>Semantica

Una semantica è una stringa associata a un input o output dello shader che fornisce informazioni sull'uso previsto di un parametro. La semantica è necessaria per tutte le variabili passate tra le fasi dello shader. La sintassi per l'aggiunta di una semantica a una variabile shader è illustrata qui ([Sintassi delle variabili (DirectX HLSL).](dx-graphics-hlsl-variable-syntax.md)

In generale, i dati passati tra le fasi della pipeline sono completamente generici e non vengono interpretati in modo univoco dal sistema. È consentita una semantica arbitraria che non ha un significato speciale. I parametri (in Direct3D 10 e versioni successive) che contengono questa semantica speciale sono definiti [semantica dei valori di sistema.](#system-value-semantics)

## <a name="semantics-supported-in-direct3d-9-and-direct3d-10-and-later"></a>Semantica supportata in Direct3D 9 e Direct3D 10 e versioni successive

I tipi di semantica seguenti sono supportati sia in Direct3D 9 che in Direct3D 10 e versioni successive.

- [Semantica vertex shader](#vertex-shader-semantics)
- [Semantica pixel shader](#pixel-shader-semantics)

### <a name="vertex-shader-semantics"></a>Semantica vertex shader

Questa semantica ha significato quando è associata a un parametro vertex shader. Questa semantica è supportata sia in Direct3D 9 che in Direct3D 10 e versioni successive.

| Input | Descrizione | Type |
|-|-|-|
| BINORMAL \[ n\] | Binormale | float4 |
| BLENDINDICES \[ n\] | Indici di blend | uint |
| BLENDWEIGHT \[ n\] | Pesi di blend | float |
| COLOR \[ n\] | Colore diffuso e speculare | float4 |
| NORMAL \[ n\] | Vettore normale | float4 |
| POSITION \[ n\] | Posizione del vertice nello spazio dell'oggetto. | float4 |
| POSITIONT | Posizione del vertice trasformata. | float4 |
| PSIZE \[ n\] | Dimensioni dei punti | float |
| TANGENT \[ N\] | Tangente | float4 |
| TEXCOORD \[ n\] | Coordinate della trama | float4 |

| Output | Descrizione | Type |
|-|-|-|
| COLOR \[ n\] | Colore diffuso o speculare | float4 |
| Nebbia | Vertice vertice | float |
| POSITION \[ n\] | Posizione di un vertice nello spazio omogeneo. Calcolare la posizione nello spazio dello schermo dividendo (x,y,z) per w. Ogni vertex shader deve scrivere un parametro con questa semantica. | float4 |
| PSIZE | Dimensioni dei punti | float |
| TESSFACTOR \[ n\] | Fattore a tessellazione | float |

`n` è un numero intero facoltativo compreso tra 0 e il numero di risorse supportate. Ad esempio, POSITION0, TEXCOORD1 e così via.

### <a name="pixel-shader-semantics"></a>Semantica pixel shader

Questa semantica ha significato quando è associata a un parametro di input pixel shader. Questa semantica è supportata sia in Direct3D 9 che in Direct3D 10 e versioni successive.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Input</th>
<th>Descrizione</th>
<th>Type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COLOR[n]</td>
<td>Colore diffuso o speculare.</td>
<td>float4</td>
</tr>
<tr class="even">
<td>TEXCOORD[n]</td>
<td>Coordinate della trama</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>VFACE</td>
<td>Scalare a virgola mobile che indica una primitiva rivolta verso il retro. Un valore negativo si trova all'indietro, mentre un valore positivo si trova di fronte alla fotocamera.
<blockquote>
[!Note]<br />
Questa semantica è disponibile in <a href="dx-graphics-hlsl-sm3.md">Direct3D 9 Shader Model 3.0.</a> Per Direct3D 10 e versioni successive, <a href="#semantics-supported-only-for-direct3d-10-and-newer">usare SV_IsFrontFace.</a>
</blockquote>
<br/></td>
<td>float</td>
</tr>
<tr class="even">
<td>VPOS</td>
<td>Posizione in pixel (x,y) nello spazio dello schermo. Per convertire uno shader Direct3D 9 (che usa questa semantica) in uno shader Direct3D 10 e versioni successive, vedere <a href="#direct3d-9-vpos-and-direct3d-10-sv_position">Direct3D 9 VPOS e Direct3D 10 SV_Position</a>)</td>
<td>float2</td>
</tr>
</tbody>
</table>

<table>
<th>Output</th>
<th>Descrizione</th>
<th>Type</th>
</tr>
<td>COLOR[n]</td>
<td>Colore di output</td>
<td>float4</td>
</tr>
<td>DEPTH[n]</td>
<td>Profondità dell'output</td>
<td>float</td>
</tr>
</table>

`n` è un numero intero facoltativo compreso tra 0 e il numero di risorse supportate. Ad esempio, PSIZE0, COLOR1 e così via.

La semantica COLOR è valida solo in modalità di compatibilità shader, ovvero quando lo shader viene creato usando D3D10 \_ SHADER \_ ENABLE \_ BACKWARDS \_ COMPATIBILITY.

## <a name="semantics-supported-only-for-direct3d-10-and-newer"></a>Semantica supportata solo per Direct3D 10 e versioni più recente.

I tipi di semantica seguenti sono stati appena introdotti per Direct3D 10 e non sono disponibili per Direct3D 9.

- [Semantica dei valori di sistema](#system-value-semantics)

### <a name="system-value-semantics"></a>System-Value semantica

La semantica dei valori di sistema è una novità di Direct3D 10. Tutti i valori di sistema iniziano con un prefisso SV, un esempio comune è SV POSITION, che viene interpretato \_ \_ dalla fase di rasterizzazione. I valori di sistema sono validi in altre parti della pipeline. Ad esempio, la posizione SV può essere specificata come \_ input per un vertex shader e come output. I pixel shader possono scrivere solo nei parametri con la semantica dei valori di sistema SV Depth e \_ SV \_ Target.

Altri valori di sistema (SV \_ VertexID, SV \_ InstanceID, SV IsFrontFace) possono essere immessi solo nel primo shader attivo nella pipeline in grado di interpretare il valore specifico. Successivamente, la funzione shader deve passare i valori alle \_ fasi successive.

PrimitiveID SV è un'eccezione a questa regola di essere solo input nel primo shader attivo nella pipeline in grado di interpretare il valore specifico. L'hardware può fornire lo stesso valore ID dell'input per la fase di hull shader, la fase domain-shader e successivamente qualsiasi fase sia la prima abilitata: fase geometry shader o \_ fase pixel shader.

Se la funzionalità a tessellazione è abilitata, sono presenti la fase hull-shader e la fase domain-shader. Per una determinata patch, lo stesso PrimitiveID si applica alla chiamata dello shader con scafo della patch e a tutte le chiamate di shader di dominio a tessellazione. Lo stesso PrimitiveID si propaga anche alla fase attiva successiva. fase geometry shader o fase pixel shader se abilitata.

Se il geometry shader input SV PrimitiveID e poiché può eseguire l'output di zero o una o più primitive per ogni chiamata, lo shader deve programmare la propria scelta del valore SV PrimitiveID per ogni primitiva di output se un pixel shader successivo \_ \_ input SV \_ PrimtiveID.

Come altro esempio, SV PrimitiveID non può essere interpretato dalla fase vertex shader perché un vertice può essere \_ membro di più primitive.

Questa semantica è stata aggiunta a Direct3D 10. non sono disponibili in Direct3D 9.

Semantica dei valori di sistema per la fase di rasterizzazione.

| System-Value semantica | Descrizione | Type |
|-|-|-|
| SV \_ ClipDistance \[ n\] | Ritagliare i dati sulla distanza. Si presuppone che i valori SV ClipDistance siano ognuno una distanza con segno \_ float32 da un piano. La configurazione primitiva richiama la rasterizzazione solo sui pixel per i quali le distanze del piano interpolato sono >= 0. Più piani di ritaglio possono essere implementati contemporaneamente, dichiarando più componenti di uno o più elementi vertice come \_ ClipDistance SV. I valori combinati clip e distanza cull sono al massimo componenti CLIP D3D O CULL DISTANCE COUNT nella maggior parte dei registri \# \_ \_ CLIP \_ D3D O \_ \_ \# \_ \_ \_ CULL DISTANCE ELEMENT \_ \_ \_ COUNT. Disponibile per tutti gli shader in cui leggere o scrivere, ad eccezione del vertex shader che può scrivere il valore ma non accettarlo come input.<br/> **L'attributo clipplanes** funziona come SV ClipDistance, ma funziona su tutti i livelli di funzionalità \_ hardware 9 x e versioni [](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) \_ successive. Per altre informazioni, vedere [Piani di ritaglio utente nell'hardware del livello di funzionalità 9.](./user-clip-planes-on-10level9.md)<br/> | float |
| SV \_ CullDistance \[ n\] | Dati relativi alla distanza dell'interruzione. Quando ai componenti degli elementi vertice viene data questa etichetta, si presuppone che ognuno di questi valori sia una distanza float32 con segno da un piano. Le primitive verranno completamente eliminate se le distanze del piano per tutti i vertici nella primitiva sono < 0. È possibile usare più piani di cull contemporaneamente, dichiarando più componenti di uno o più elementi vertice come SV \_ CullDistance. I valori combinati clip e distanza cull sono al massimo componenti CLIP D3D O CULL DISTANCE COUNT nella maggior parte dei registri \# \_ \_ CLIP \_ D3D O \_ \_ \# \_ \_ \_ CULL DISTANCE ELEMENT \_ \_ \_ COUNT. Disponibile per tutti gli shader in cui leggere o scrivere, ad eccezione del vertex shader che può scrivere il valore ma non accettarlo come input.<br/> | float |
| Copertura \_ SV | Maschera che può essere specificata in input, output o in entrambe le pixel shader. <br/> Per la copertura SV \_ in un pixel shader, OUTPUT è supportato in ps \_ 4 \_ 1 o versione successiva. <br/> Per la copertura SV \_ in un pixel shader, INPUT richiede ps \_ 5 \_ 0 o versione successiva. <br/> | uint |
| Profondità \_ SV | Dati del buffer di profondità. Può essere scritto pixel shader. | float |
| SV \_ DepthGreaterEqual | In un pixel shader, consente la profondità di output, purché sia maggiore o uguale al valore determinato dal rasterizzatore. Abilita la regolazione della profondità senza disabilitare la prima Z. | float |
| SV \_ DepthLessEqual | In un pixel shader, consente la profondità di output, purché sia minore o uguale al valore determinato dal rasterizzatore. Abilita la regolazione della profondità senza disabilitare la Z iniziale. | float |
| [SV \_ DispatchThreadID](sv-dispatchthreadid.md) | Definisce l'offset del thread globale all'interno della chiamata Dispatch, per dimensione del gruppo. Disponibile come input per il calcolo dello shader. (sola lettura) | uint3 |
| [SV \_ DomainLocation](sv-domainlocation.md) | Definisce la posizione sulla scafo del punto di dominio corrente da valutare. Disponibile come input per lo shader del dominio. (sola lettura) | float2 \| 3 |
| [SV \_ GroupID](sv-groupid.md) | Definisce l'offset del gruppo all'interno di una chiamata Dispatch, per dimensione della chiamata di invio. Disponibile come input per lo shader di calcolo. (sola lettura) | uint3 |
| [SV \_ GroupIndex](sv-groupindex.md) | Fornisce un indice flat per un determinato thread all'interno di un determinato gruppo. Disponibile come input per lo shader di calcolo. (sola lettura) | uint |
| [SV \_ GroupThreadID](sv-groupthreadid.md) | Definisce l'offset del thread all'interno del gruppo, per dimensione del gruppo. Disponibile come input per lo shader di calcolo. (sola lettura) | uint3 |
| [SV \_ GSInstanceID](sv-gsinstanceid.md) | Definisce l'istanza dello shader geometry. Disponibile come input per lo shader geometry. L'istanza è necessaria perché uno shader geometry può essere richiamato fino a 32 volte nella stessa primitiva geometry. | uint |
| SV \_ InnerCoverage | Rappresenta le informazioni di rasterizzazione conservatrici sottostimate( ad esempio se un pixel è garantito per essere completamente coperto). Può essere letto o scritto dal pixel shader. | |
| [SV \_ InsideTessFactor](sv-insidetessfactor.md) | Definisce la quantità di tassellamento all'interno di una superficie patch. Disponibile nello hull shader per la scrittura e disponibile nel domain shader per la lettura. | float \| float \[ 2\] |
| SV \_ InstanceID | Identificatore per istanza generato automaticamente dal runtime (vedere [Using System-Generated Values (Direct3D 10) (Uso di valori di System-Generated (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Disponibile per tutti gli shader. | |
| SV \_ IsFrontFace | Specifica se un triangolo è rivolto verso l'avanti. Per le linee e i punti, IsFrontFace ha il valore true. L'eccezione è data da linee disegnate da triangoli (modalità wireframe), che imposta IsFrontFace nello stesso modo in cui rasterizza il triangolo in modalità a tinta unita. Può essere scritto in dallo shader geometry e letto dal pixel shader. | bool |
| [SV \_ OutputControlPointID](sv-outputcontrolpointid.md) | Definisce l'indice dell'ID del punto di controllo gestito da una chiamata del punto di ingresso principale dello shader di tipo hull. Può essere letto solo dallo shader di tipo hull. | uint |
| Posizione \_ SV | Quando la posizione SV viene dichiarata per l'input in uno shader, può avere una delle due modalità di \_ interpolazione specificate: linearNoPerspective o linearNoPerspectiveCentroid, in cui quest'ultima fa sì che i valori xyzw allineati al centroide siano forniti durante l'anti-aliasing multicampionamento. Se usato in uno shader, SV \_ Position descrive la posizione in pixel. Disponibile in tutti gli shader per ottenere il centro del pixel con un offset di 0,5. | float4 |
| SV \_ PrimitiveID | Identificatore per primitiva generato automaticamente dal runtime (vedere [Using System-Generated Values (Direct3D 10) (Uso](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)dei valori di System-Generated (Direct3D 10) ). Può essere scritto da geometry shader o pixel shader e letto da geometry, pixel, hull o domain shader. | uint |
| SV \_ RenderTargetArrayIndex | Indice della matrice di destinazione di rendering. Applicato all'output geometry shader e indica la sezione della matrice di destinazione di rendering su cui verrà disegnata la primitiva dal pixel shader. SV \_ RenderTargetArrayIndex è valido solo se la destinazione di rendering è una risorsa di matrice. Questa semantica si applica solo alle primitive. se una primitiva ha più vertici, viene usato il valore del vertice iniziale. Questo valore indica anche quale sezione di matrice di una visualizzazione di profondità/stencil viene usata per scopi di lettura/scrittura.<br/> Può essere scritto dallo shader geometry e letto dal pixel shader.<br/> Se [D3D11_FEATURE_DATA_D3D11_OPTIONS3::VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) è , SV RenderTargetArrayIndex viene applicato a qualsiasi shader che alimenta il `true` \_ rasterizzatore. | uint |
| SV \_ SampleIndex | Dati dell'indice di frequenza di esempio. Disponibile per la lettura o la scrittura da parte del pixel shader solo. | uint |
| SV \_ StencilRef | Rappresenta il valore di riferimento pixel shader dello stencil corrente. Può essere scritto solo dal pixel shader. | uint |
| Destinazione SV \_ \[ n , dove \] 0 <= n <= 7 | Valore di output che verrà archiviato in una destinazione di rendering. L'indice indica in quale delle 8 destinazioni di rendering eventualmente associate scrivere. Il valore è disponibile per tutti gli shader. | float \[ 2 \| 3 \| 4\] |
| [SV \_ TessFactor](sv-tessfactor.md) | Definisce la quantità di tassellamento su ogni bordo di una patch. Disponibile per la scrittura nello shader hull e la lettura nel domain shader. | float \[ 2 \| 3 \| 4\] |
| SV \_ VertexID | Identificatore per vertice generato automaticamente dal runtime (vedere [Using System-Generated Values (Direct3D 10) (Uso di valori di System-Generated (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Disponibile come input solo per il vertex shader. | uint |
| SV \_ ViewportArrayIndex | Indice della matrice del viewport. Applicato all'output geometry shader e indica il viewport da usare per la primitiva attualmente in fase di scrittura. Può essere letto dal pixel shader. La primitiva verrà trasformata e ritagliata rispetto al viewport specificato dall'indice prima che venga passata al rasterizzatore. Questa semantica si applica solo alle primitive. Se una primitiva ha più di un vertice, viene usato il valore del vertice iniziale. <br/> Se [D3D11_FEATURE_DATA_D3D11_OPTIONS3::VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) è , la proprietà ViewportArrayIndex SV viene applicata a qualsiasi shader che alimenta il `true` \_ rasterizzatore. | uint |
| SV \_ ShadingRate | Definisce, tramite i valori [](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate)di velocità dell'ombreggiatura, il numero di pixel scritti da un pixel shader chiamata per i dispositivi a velocità di ombreggiatura variabile [di livello 2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) o superiore. Può essere letto dal pixel shader. Può essere scritto da un vertice o geometry shader. | uint |

### <a name="limitations-when-writing-sv_depth"></a>Limitazioni durante la scrittura di SV \_ Depth:

- Quando il multisampling (MultisampleEnable è **TRUE** in [**D3D10 \_ RASTERIZER \_ DESC)**](/windows/win32/api/d3d10/ns-d3d10-d3d10_rasterizer_desc)e si scrive un valore di profondità (usando un pixel shader), il singolo valore scritto viene usato anche nel [test](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md)di profondità, pertanto la possibilità di eseguire il rendering di bordi primitivi con una risoluzione superiore viene persa quando viene eseguito il multicampionamento.
- Quando si usa il controllo dinamico del flusso, non è possibile determinare in fase di compilazione se uno shader che scrive profondità SV in alcuni percorsi sarà in grado di scrivere profondità \_ SV \_ in ogni esecuzione. La mancata scrittura della profondità SV quando viene dichiarata comporta un comportamento indefinito (che può includere o meno \_ l'eliminazione del pixel).
- Qualsiasi valore float32, inclusi +/-INF e NaN, può essere scritto in Profondità \_ SV.
- La scrittura di profondità SV è ancora valida quando si esegue la fusione di \_ colori a doppia origine.

## <a name="migration-from-direct3d-9-to-direct3d-10-and-later"></a>Migrazione da Direct3D 9 a Direct3D 10 e versioni successive

Quando si esegue la migrazione del codice da Direct3D 9 a Direct3D 10 e versioni successive, è necessario considerare i problemi seguenti:

### <a name="mapping-to-direct3d-9-semantics"></a>Mapping alla semantica Direct3D 9

Alcune semantiche Direct3D 10 e successive vengono mappate direttamente alla semantica Direct3D 9.

| Semantica Direct3D 10 | Semantica equivalente direct3D 9 |
|-|-|
| Profondità \_ SV | DEPTH |
| Posizione \_ SV | POSITION |
| Destinazione \_ SV | Colore |

> [!] Nota per gli sviluppatori Direct3D 9: per le destinazioni Direct3D 9, la semantica dello shader deve essere mappata alla semantica Direct3D 9 valida. Per la compatibilità con le versioni precedenti POSITION0 (e i relativi nomi di varianti) viene considerato come SV \_ Position, COLOR viene considerato come SV \_ TARGET.

- [Mapping alla semantica Direct3D 9](#mapping-to-direct3d-9-semantics)
- [Direct3D 9 VPOS e Direct3D 10 \_ SV Position](#direct3d-9-vpos-and-direct3d-10-sv_position)
- [Piani di ritaglio utente in HLSL](#user-clip-planes-in-hlsl)

### <a name="direct3d-9-vpos-and-direct3d-10-sv_position"></a>Direct3D 9 VPOS e Direct3D 10 \_ SV Position

La posizione SV semantica D3D10 offre funzionalità simili alla \_ semantica VPOS direct3D 9 shader model 3. Ad esempio, in Direct3D 9 viene usata la sintassi seguente per un pixel shader usando le coordinate dello spazio dello schermo:

```HLSL
float4 psMainD3D9( float4 screenSpace : VPOS ) : COLOR
{
    // code here 
}
```

VPOS è stato aggiunto per il supporto del modello shader 3, per specificare le coordinate dello spazio dello schermo, poiché la semantica POSITION era destinata alle coordinate dello spazio oggetto.

In Direct3D 10 e versioni successive, la semantica SV Position (se usata nel contesto di un pixel shader) specifica le coordinate dello spazio dello schermo (offset di \_ 0,5). Pertanto, lo shader Direct3D 9 sarebbe approssimativamente equivalente (senza l'offset 0,5) a quanto segue:

```HLSL
float4 psMainD3D10( float4 screenSpace : SV_Position ) : COLOR
{
    // code here
}
```

Quando si esegue la migrazione da Direct3D 9 a Direct3D 10 e versioni successive, è necessario tenere presente questo problema durante la conversione degli shader.

### <a name="user-clip-planes-in-hlsl"></a>Piani di ritaglio utente in HLSL

A partire da Windows 8, è possibile usare l'attributo della [](dx-graphics-hlsl-function-syntax.md) funzione **clipplanes** in una dichiarazione di funzione HLSL anziché SV ClipDistance per fare in modo che lo shader funzioni sul livello di funzionalità 9 x e sul livello di funzionalità \_ [](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 10 o \_ superiore. Per altre informazioni, vedi [Piani di ritaglio utente sull'hardware a livello di funzionalità 9.](./user-clip-planes-on-10level9.md)

## <a name="related-topics"></a>Argomenti correlati

* [Sintassi del linguaggio](dx-graphics-hlsl-language-syntax.md)
* [Variabili (DirectX HLSL)](dx-graphics-hlsl-variables.md)
