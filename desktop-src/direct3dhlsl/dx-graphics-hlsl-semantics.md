---
title: Semantica
description: Una semantica è una stringa collegata a un input o output dello shader che fornisce informazioni sull'uso previsto di un parametro.
ms.assetid: 6f5c504c-1940-4d1c-b594-a2132599376b
keywords:
- Binormal, semantica (DirectX HLSL)
- BLENDINDICES, semantica (DirectX HLSL)
- BLENDWEIGHT, semantica (DirectX HLSL)
- COLORE, semantica (DirectX HLSL)
- NEBBIA, semantica (DirectX HLSL)
- POSITIONt, semantica (DirectX HLSL)
- PSIZE, semantica (DirectX HLSL)
- TANGENTE, semantica (DirectX HLSL)
- TESSFACTOR, semantica (DirectX HLSL)
- TEXCOORD, semantica (DirectX HLSL)
- VFACE, semantica (DirectX HLSL)
- VPOS, semantica (DirectX HLSL)
- Semantica di System-Value
- Semantica di valori di sistema
- ClipDistance, semantica (DirectX HLSL)
- Code coverage, semantica (DirectX HLSL)
- CullDistance, semantica (DirectX HLSL)
- Profondità, semantica (DirectX HLSL)
- InstanceID, semantica (DirectX HLSL)
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
- Semantica di SV_DispatchThreadID (DirectX HLSL)
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
ms.openlocfilehash: 510f718608363c547c8333279826cc8bac141358
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234559"
---
# <a name="semantics"></a>Semantica

Una semantica è una stringa collegata a un input o output dello shader che fornisce informazioni sull'uso previsto di un parametro. La semantica è obbligatoria per tutte le variabili passate tra le fasi dello shader. Di seguito è riportata la sintassi per l'aggiunta di una semantica a una variabile shader ([sintassi variabile (DirectX HLSL)](dx-graphics-hlsl-variable-syntax.md)).

In generale, i dati passati tra le fasi della pipeline sono completamente generici e non vengono interpretati in modo univoco dal sistema. la semantica arbitraria è consentita e non ha un significato speciale. I parametri (in Direct3D 10 e versioni successive) che contengono la semantica speciale sono detti [semantica di valori di sistema](#system-value-semantics).

## <a name="semantics-supported-in-direct3d-9-and-direct3d-10-and-later"></a>Semantica supportata in Direct3D 9 e Direct3D 10 e versioni successive

I tipi di semantica seguenti sono supportati sia in Direct3D 9 che in Direct3D 10 e versioni successive.

- [Semantica vertex shader](#vertex-shader-semantics)
- [Semantica pixel shader](#pixel-shader-semantics)

### <a name="vertex-shader-semantics"></a>Semantica vertex shader

Queste semantiche hanno un significato quando sono associate a un parametro vertex shader. Queste semantiche sono supportate sia in Direct3D 9 che in Direct3D 10 e versioni successive.

| Input | Descrizione | Type |
|-|-|-|
| N binormale \[\] | Binormale | float4 |
| BLENDINDICES \[ n\] | Indici Blend | uint |
| BLENDWEIGHT \[ n\] | Ponderazioni di Blend | float |
| COLORE \[ n\] | Colore diffuso e speculare | float4 |
| NORMALE \[ n\] | Vettore normale | float4 |
| POSIZIONE \[ n\] | Posizione del vertice nello spazio degli oggetti. | float4 |
| POSIZIONE | Posizione del vertice trasformato. | float4 |
| PSIZE \[ n\] | Dimensioni dei punti | float |
| TANGENTE \[ n\] | Tangente | float4 |
| TEXCOORD \[ n\] | Coordinate di trama | float4 |
| Output | Descrizione | Type |
| COLORE \[ n\] | Colore diffuso o speculare | float4 |
| NEBBIA | Nebbia vertice | float |
| POSIZIONE \[ n\] | Posizione di un vertice nello spazio omogeneo. Calcolare la posizione nello spazio dello schermo dividendo (x, y, z) per w. Ogni vertex shader deve scrivere un parametro con questa semantica. | float4 |
| PSIZE | Dimensioni dei punti | float |
| TESSFACTOR \[ n\] | Fattore a mosaico | float |

`n` è un numero intero facoltativo compreso tra 0 e il numero di risorse supportate. Ad esempio, POSITION0, TEXCOORD1 e così via.

### <a name="pixel-shader-semantics"></a>Semantica pixel shader

Queste semantiche hanno un significato quando sono associate a un parametro di input di pixel shader. Queste semantiche sono supportate sia in Direct3D 9 che in Direct3D 10 e versioni successive.

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
<td>COLORE [n]</td>
<td>Colore speculare o diffuso.</td>
<td>float4</td>
</tr>
<tr class="even">
<td>TEXCOORD [n]</td>
<td>Coordinate di trama</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>VFACE</td>
<td>Scalare a virgola mobile che indica una primitiva con supporto. Un valore negativo viene rivolto all'indietro, mentre un valore positivo è volto alla fotocamera.
<blockquote>
[!Note]<br />
Questa semantica è disponibile nel <a href="dx-graphics-hlsl-sm3.md">modello Direct3D 9 shader 3,0</a>. Per Direct3D 10 e versioni successive, usare invece <a href="#semantics-supported-only-for-direct3d-10-and-newer">SV_IsFrontFace</a> .
</blockquote>
<br/></td>
<td>float</td>
</tr>
<tr class="even">
<td>VPOS</td>
<td>Posizione in pixel (x, y) nello spazio dello schermo. Per convertire uno shader Direct3D 9 (che usa questa semantica) in uno shader Direct3D 10 e versioni successive, vedere <a href="#direct3d-9-vpos-and-direct3d-10-sv_position">Direct3D 9 vPOS e Direct3D 10 SV_Position</a>)</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Output</td>
<td>Descrizione</td>
<td>Type</td>
</tr>
<tr class="even">
<td>COLORE [n]</td>
<td>Colore di output</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>PROFONDITÀ [n]</td>
<td>Profondità di output</td>
<td>float</td>
</tr>
</tbody>
</table>

`n` è un numero intero facoltativo compreso tra 0 e il numero di risorse supportate. Ad esempio, PSIZE0, COLOR1 e così via.

La semantica di colore è valida solo in modalità di compatibilità shader, ovvero quando lo shader viene creato con D3D10 \_ shader Abilita la \_ compatibilità con le \_ versioni precedenti \_ .

## <a name="semantics-supported-only-for-direct3d-10-and-newer"></a>Semantica supportata solo per Direct3D 10 e versioni successive.

I tipi di semantica seguenti sono stati introdotti di recente per Direct3D 10 e non sono disponibili per Direct3D 9.

- [Semantica di valori di sistema](#system-value-semantics)

### <a name="system-value-semantics"></a>Semantica di System-Value

La semantica del valore di sistema è una novità di Direct3D 10. Tutti i valori di sistema iniziano con un \_ prefisso SV, un esempio comune è \_ la posizione SV, interpretata dalla fase di rasterizzazione. I valori di sistema sono validi in altre parti della pipeline. Ad esempio, \_ è possibile specificare la posizione SV come input per un vertex shader e un output. I pixel shader possono scrivere solo nei parametri con la \_ profondità SV e la \_ semantica del valore del sistema di destinazione Sv.

Altri valori di sistema (SV \_ VertexID, SV \_ instanceId, SV \_ IsFrontFace) possono essere inseriti solo nel primo shader attivo nella pipeline che può interpretare il valore specifico; dopo che la funzione shader deve passare i valori alle fasi successive.

SV \_ PrimitiveID è un'eccezione a questa regola di input solo nel primo shader attivo nella pipeline che può interpretare il valore specifico. l'hardware può fornire lo stesso valore ID dell'input alla fase di Hull shader, alla fase Domain-shader e dopo tale fase è la prima fase abilitata: geometria-shader o fase pixel shader.

Se la suddivisione a mosaico è abilitata, sono presenti la fase Hull-shader e la fase Domain shader. Per una determinata patch, lo stesso PrimitiveID si applica alla chiamata allo scafo dello shader della patch e a tutte le chiamate dello shader del dominio tassellati. Lo stesso PrimitiveID viene inoltre propagato alla fase attiva successiva; geometria-fase shader o fase pixel shader se abilitata.

Se il geometry shader immette SV \_ PrimitiveID e perché può restituire zero o una o più primitive per chiamata, lo shader deve programmare la propria scelta del \_ valore SV PrimitiveID per ogni primitiva di output se una pixel shader successiva immette SV \_ PrimtiveID.

Come altro esempio, SV \_ PrimitiveID non può essere interpretato dalla fase vertex shader perché un vertice può essere un membro di più primitive.

Questa semantica è stata aggiunta a Direct3D 10; non sono disponibili in Direct3D 9.

Semantica del valore di sistema per la fase di rasterizzazione.

| Semantica System-Value | Descrizione | Type |
|-|-|-|
| SV \_ Clipdistance \[ n\] | Ritagliare i dati relativi alla distanza. \_I valori SV Clipdistance sono considerati come una distanza con segno float32 a un piano. Il programma di installazione primitive richiama solo la rasterizzazione su pixel per i quali le distanze del piano interpolato sono >= 0. È possibile implementare contemporaneamente più piani di ritaglio, dichiarando più componenti di uno o più elementi Vertex come SV \_ Clipdistance. I valori combinati della distanza di ritaglio e di abbattimento sono al massimo i componenti per il numero di clip \# \_ \_ o di raccolta D3D \_ \_ \_ in alla maggior parte dei \# \_ \_ registri di \_ \_ numero di \_ elementi \_ di clip o Disponibile per tutti gli shader per la lettura o la scrittura, ad eccezione del vertex shader che può scrivere il valore ma non accettarlo come input.<br/> L'attributo **clipplanes** funziona come SV \_ Clipdistance ma funziona su tutti i [livelli di funzionalità](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) hardware 9 \_ x e versioni successive. Per altre informazioni, vedere la pagina [relativa ai piani di ritaglio utente su hardware di livello funzionalità 9](./user-clip-planes-on-10level9.md).<br/> | float |
| SV \_ CullDistance \[ n\] | Dati della distanza di eliminazione. Quando ai componenti degli elementi Vertex viene assegnata questa etichetta, questi valori vengono considerati come una distanza con segno float32 a un piano. Le primitive verranno eliminate completamente se le distanze del piano per tutti i vertici della primitiva sono < 0. È possibile usare contemporaneamente più piani di eliminazione, dichiarando più componenti di uno o più elementi Vertex come SV \_ CullDistance. I valori combinati della distanza di ritaglio e di abbattimento sono al massimo i componenti per il numero di clip \# \_ \_ o di raccolta D3D \_ \_ \_ in alla maggior parte dei \# \_ \_ registri di \_ \_ numero di \_ elementi \_ di clip o Disponibile per tutti gli shader per la lettura o la scrittura, ad eccezione del vertex shader che può scrivere il valore ma non accettarlo come input.<br/> | float |
| \_Copertura SV | Maschera che può essere specificata nell'input, nell'output o in entrambe le pixel shader. <br/> Per \_ la copertura SV in una pixel shader, l'output è supportato in PS \_ 4 \_ 1 o versione successiva. <br/> Per \_ la copertura SV in una pixel shader, l'input richiede PS \_ 5 \_ 0 o versione successiva. <br/> | uint |
| \_Profondità SV | Dati del buffer di profondità. Può essere scritto da pixel shader. | float |
| \_DEPTHGREATEREQUAL SV | In una pixel shader, consente l'output della profondità, purché sia maggiore o uguale al valore determinato dal rasterizzatore. Consente di modificare la profondità senza disabilitare l'inizio della Z. | float |
| \_DEPTHLESSEQUAL SV | In una pixel shader, consente l'output della profondità, purché sia minore o uguale al valore determinato dal rasterizzatore. Consente di modificare la profondità senza disabilitare l'inizio della Z. | float |
| [\_DISPATCHTHREADID SV](sv-dispatchthreadid.md) | Definisce l'offset del thread globale all'interno della chiamata di invio, per dimensione del gruppo. Disponibile come input per compute shader. (sola lettura) | uint3 |
| [\_DOMAINLOCATION SV](sv-domainlocation.md) | Definisce la posizione sullo scafo del punto di dominio corrente valutato. Disponibile come input per lo shader del dominio. (sola lettura) | float2 \| 3 |
| [\_GROUPID SV](sv-groupid.md) | Definisce l'offset di gruppo all'interno di una chiamata di invio, per dimensione della chiamata di invio. Disponibile come input per compute shader. (sola lettura) | uint3 |
| [\_GROUPINDEX SV](sv-groupindex.md) | Fornisce un indice bidimensionale per un thread specificato all'interno di un determinato gruppo. Disponibile come input per compute shader. (sola lettura) | uint |
| [\_GROUPTHREADID SV](sv-groupthreadid.md) | Definisce l'offset del thread all'interno del gruppo, per dimensione del gruppo. Disponibile come input per compute shader. (sola lettura) | uint3 |
| [\_GSINSTANCEID SV](sv-gsinstanceid.md) | Definisce l'istanza di Geometry shader. Disponibile come input per il geometry shader. L'istanza è necessaria perché un geometry shader può essere richiamato fino a 32 volte sulla stessa primitiva Geometry. | uint |
| \_INNERCOVERAGE SV | Rappresenta le informazioni di rasterizzazione conservative sottostimate, ad esempio se un pixel è garantito per essere completamente coperto. Può essere letto o scritto dal pixel shader. | |
| [\_INSIDETESSFACTOR SV](sv-insidetessfactor.md) | Definisce l'importo a mosaico all'interno di una superficie della patch. Disponibile nello scafo dello shader per la scrittura e disponibile nello shader del dominio per la lettura. | float \| float \[ 2\] |
| ID istanza SV \_ | Identificatore per istanza generato automaticamente dal runtime (vedere [Using System-Generated values (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Disponibile per tutti gli shader. | |
| \_ISFRONTFACE SV | Specifica se un triangolo è di fronte. Per le righe e i punti, il valore di IsFrontFace è true. L'eccezione è costituita dalle linee disegnate da triangoli (modalità wireframe), che imposta IsFrontFace in modo analogo alla rasterizzazione del triangolo in modalità a tinta unita. Può essere scritto da Geometry shader e letto dal pixel shader. | bool |
| [\_OUTPUTCONTROLPOINTID SV](sv-outputcontrolpointid.md) | Definisce l'indice dell'ID del punto di controllo utilizzato da una chiamata al punto di ingresso principale dello scafo dello shader. Può essere letto solo da Hull shader. | uint |
| \_Posizione SV | Quando \_ la posizione SV viene dichiarata per l'input in uno shader, può essere specificata una delle due modalità di interpolazione: linearNoPerspective o linearNoPerspectiveCentroid, in cui il secondo causa l'inserimento di valori xyzw con blocco centrale durante l'anti-aliasing di multicampionamento. Quando viene usato in uno shader, SV \_ position descrive la posizione dei pixel. Disponibile in tutti gli shader per ottenere il pixel Center con un offset 0,5. | float4 |
| \_PRIMITIVEID SV | Identificatore per primitiva generato automaticamente dal runtime (vedere [uso di valori System-Generated (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Può essere scritto in base agli shader di geometria o pixel e letto dalla geometria, dal pixel, dallo scafo o dal dominio. | uint |
| \_RENDERTARGETARRAYINDEX SV | Render: indice della matrice di destinazione. Applicato all'output dello shader Geometry e indica la sezione della matrice della destinazione di rendering in base alla quale verrà disegnata la primitiva dall'pixel shader. SV \_ RenderTargetArrayIndex è valido solo se la destinazione di rendering è una risorsa di matrice. Questa semantica si applica solo alle primitive. Se una primitiva ha più di un vertice, viene usato il valore del vertice di primo livello. Questo valore indica anche quale sezione della matrice di una visualizzazione profondità/stencil viene utilizzata per finalità di lettura/scrittura.<br/> Può essere scritto da Geometry shader e letto dal pixel shader.<br/> Se [D3D11_FEATURE_DATA_D3D11_OPTIONS3:: VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) è `true` , viene \_ applicato SV RenderTargetArrayIndex a qualsiasi shader che alimenta il rasterizzatore. | uint |
| \_SAMPLEINDEX SV | Dati dell'indice di frequenza di esempio. Disponibile per la lettura o la scrittura solo da parte del pixel shader. | uint |
| \_STENCILREF SV | Rappresenta il valore di riferimento dello stencil pixel shader corrente. Può essere scritto solo dal pixel shader. | uint |
| SV \_ target \[ n \] , dove 0 <= n <= 7 | Valore di output che verrà archiviato in una destinazione di rendering. L'indice indica quale delle 8 destinazioni di rendering eventualmente associato in cui scrivere. Il valore è disponibile per tutti gli shader. | float \[ 2 \| 3 \| 4\] |
| [\_TESSFACTOR SV](sv-tessfactor.md) | Definisce l'importo a mosaico per ogni bordo di una patch. Disponibile per la scrittura nello scafo dello shader e la lettura nello shader del dominio. | float \[ 2 \| 3 \| 4\] |
| \_VERTEXID SV | Identificatore per vertice generato automaticamente dal runtime (vedere [Using System-Generated values (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Disponibile come input solo per vertex shader. | uint |
| \_VIEWPORTARRAYINDEX SV | Indice matrice viewport. Applicato all'output di Geometry shader e indica il viewport da usare per la primitiva attualmente in fase di scrittura. Può essere letto dal pixel shader. La primitiva verrà trasformata e ritagliata rispetto al viewport specificato dall'indice prima che venga passata al rasterizzatore. Questa semantica si applica solo alle primitive. Se una primitiva ha più di un vertice, viene usato il valore del vertice di primo livello. <br/> Se [D3D11_FEATURE_DATA_D3D11_OPTIONS3:: VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) è `true` , viene \_ applicato SV ViewportArrayIndex a qualsiasi shader che alimenta il rasterizzatore. | uint |
| \_SHADINGRATE SV | Definisce, tramite [i valori](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate)di frequenza ombreggiatura, il numero di pixel scritti da uno pixel shader chiamata per i dispositivi di livello 2 o superiore della [Variabile ombreggiatura](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) . Può essere letto dal pixel shader. Può essere scritto da un vertice o un geometry shader. | uint |

### <a name="limitations-when-writing-sv_depth"></a>Limitazioni durante la scrittura della \_ profondità SV:

- Quando il multisampling (MultisampleEnable è **true** in [**D3D10 \_ rasterizzator \_ desc**](/windows/win32/api/d3d10/ns-d3d10-d3d10_rasterizer_desc)) e si scrive un valore di profondità (usando un pixel shader), il valore singolo scritto viene usato anche nel [test di profondità](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md). Pertanto, la possibilità di eseguire il rendering di bordi primitivi con una risoluzione più elevata viene persa durante il campionamento multiplo.
- Quando si usa il controllo di flusso dinamico, non è possibile determinare in fase di compilazione se uno shader che scrive la \_ profondità SV in alcuni percorsi garantirà la scrittura \_ della profondità SV in ogni esecuzione. La mancata scrittura \_ della profondità SV quando viene dichiarata produce un comportamento non definito, che può includere o meno l'eliminazione del pixel.
- Qualsiasi valore di float32, tra cui +/-INF e NaN, può essere scritto in \_ profondità SV.
- La scrittura della \_ profondità SV è ancora valida quando si esegue la fusione dual source color.

## <a name="migration-from-direct3d-9-to-direct3d-10-and-later"></a>Migrazione da Direct3D 9 a Direct3D 10 e versioni successive

Quando si esegue la migrazione del codice da Direct3D 9 a Direct3D 10 e versioni successive, è necessario considerare i problemi seguenti:

### <a name="mapping-to-direct3d-9-semantics"></a>Mapping alla semantica di Direct3D 9

Alcune della semantica Direct3D 10 e successive vengono mappate direttamente alla semantica di Direct3D 9.

| Semantica Direct3D 10 | Semantica equivalente a Direct3D 9 |
|-|-|
| \_Profondità SV | DEPTH |
| \_Posizione SV | POSITION |
| \_Destinazione SV | Colore |

> [!] Nota per gli sviluppatori Direct3D 9: per gli obiettivi Direct3D 9, la semantica dello shader deve essere mappata alla semantica Direct3D 9 valida. Per la compatibilità con le versioni precedenti, POSITION0 (e i relativi nomi Variant) viene considerato come la \_ posizione SV, il colore viene considerato come \_ destinazione Sv.

- [Mapping alla semantica di Direct3D 9](#mapping-to-direct3d-9-semantics)
- [Posizione Direct3D 9 VPOS e Direct3D 10 SV \_](#direct3d-9-vpos-and-direct3d-10-sv_position)
- [Piani di ritaglio utente in HLSL](#user-clip-planes-in-hlsl)

### <a name="direct3d-9-vpos-and-direct3d-10-sv_position"></a>Posizione Direct3D 9 VPOS e Direct3D 10 SV \_

La posizione SV di D3D10 semantica \_ fornisce funzionalità simili alla semantica vPOS di Direct3D 9 Shader Model 3. Ad esempio, in Direct3D 9 viene usata la sintassi seguente per un pixel shader usando le coordinate dello spazio dello schermo:

```HLSL
float4 psMainD3D9( float4 screenSpace : VPOS ) : COLOR
{
    // code here 
}
```

VPOS è stato aggiunto per il supporto del modello Shader 3, per specificare le coordinate dello spazio dello schermo, perché la semantica di posizione è stata progettata per le coordinate dello spazio degli oggetti.

In Direct3D 10 e versioni successive, la \_ semantica di posizione SV (se usata nel contesto di un pixel shader) specifica le coordinate dello spazio dello schermo (offset per 0,5). Di conseguenza, lo shader Direct3D 9 sarebbe approssimativamente equivalente (senza accounting per l'offset 0,5) come segue:

```HLSL
float4 psMainD3D10( float4 screenSpace : SV_Position ) : COLOR
{
    // code here
}
```

Quando si esegue la migrazione da Direct3D 9 a Direct3D 10 e versioni successive, è necessario tenere presente questo durante la conversione degli shader.

### <a name="user-clip-planes-in-hlsl"></a>Piani di ritaglio utente in HLSL

A partire da Windows 8, è possibile usare l'attributo della funzione **clipplanes** in una [dichiarazione di funzione](dx-graphics-hlsl-function-syntax.md) HLSL anziché SV Clipdistance per fare in modo che \_ lo shader funzioni con il [livello di funzionalità](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, nonché con il livello di funzionalità 10 e versioni successive. Per altre informazioni, vedere la pagina [relativa ai piani di ritaglio utente su hardware di livello funzionalità 9](./user-clip-planes-on-10level9.md).

## <a name="related-topics"></a>Argomenti correlati

* [Sintassi del linguaggio](dx-graphics-hlsl-language-syntax.md)
* [Variabili (DirectX HLSL)](dx-graphics-hlsl-variables.md)