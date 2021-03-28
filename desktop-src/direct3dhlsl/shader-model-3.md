---
title: Shader Model 3 (riferimento HLSL)
description: I vertex shader e i pixel shader sono notevolmente semplificati rispetto alle versioni precedenti dello shader.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3517266ace77b9235604770d9b42d10cd80e2d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399208"
---
# <a name="shader-model-3-hlsl-reference"></a>Shader Model 3 (riferimento HLSL)

I vertex shader e i pixel shader sono notevolmente semplificati rispetto alle versioni precedenti dello shader. Se si stanno implementando shader in hardware, non è possibile usare vs \_ 3 \_ 0 o PS \_ 3 \_ 0 con altre versioni di shader e non è possibile usare uno shader con la pipeline della funzione fissa. Queste modifiche consentono di semplificare i driver e il Runtime. L'unica eccezione è che gli shader solo software e \_ 3 \_ 0 possono essere utilizzati con qualsiasi versione pixel shader. Inoltre, se si utilizza uno shader solo software e \_ 3 \_ 0 con una versione precedente di pixel shader, il vertex shader può utilizzare solo la semantica di output compatibile con i codici FVF (Flexible Vertex Format).

La semantica utilizzata per gli output di vertex shader deve essere utilizzata su input pixel shader. La semantica viene usata per eseguire il mapping degli output del vertex shader agli input pixel shader, in modo analogo al modo in cui viene eseguito il mapping della dichiarazione del vertice ai registri di input del vertex shader e ai modelli shader precedenti. Vedere semantica di corrispondenza sugli shader vs 3,0 e PS 3,0.

Sono stati aggiunti stati di rendering della modalità a capo aggiuntivo per coprire la possibilità di ulteriori coordinate di trama in questo nuovo schema. Gli attributi con D3DDECLUSAGE \_ TEXCOORD e l'indice di utilizzo da 0 a 15 vengono interpolati in modalità a capo quando viene impostato il [**ritorno a \_ capo \* D3DRS**](/windows/desktop/direct3d9/d3drenderstatetype) corrispondente.

-   [Funzionalità di Vertex Shader Model 3](#vertex-shader-model-3-features)
-   [Funzionalità del pixel shader modello 3](#pixel-shader-model-3-features)
-   [Semantica di corrispondenza in Visual Studio \_ 3 \_ 0 e PS \_ 3 \_ 0 Shader](/windows)
-   [Modifiche della modalità nebbia, profondità e ombreggiatura](#fog-depth-and-shading-mode-changes)
-   [Conversioni a virgola mobile e Integer](#floating-point-and-integer-conversions)
-   [Specifica della precisione completa o parziale](#specifying-full-or-partial-precision)
-   [Vertex e pixel shader software](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a>Funzionalità di Vertex Shader Model 3

I tipi di registro di output vertex shader sono stati compressi in dodici registri (vedere [log di output](dx9-graphics-reference-asm-vs-registers-output.md)). Ogni registro utilizzato deve essere dichiarato utilizzando l'istruzione [DCL](dcl-usage---ps.md) e una semantica (ad esempio, DCL \_ Color0 o0. xyzw).

Il \_ modello di vertex shader 3 0 (vs \_ 3 \_ 0) si espande sulle funzionalità di vs \_ 2 \_ 0 con un'indicizzazione dei registri più potente, un set di registri di output semplificati, la possibilità di campionare una trama in un vertex shader e la possibilità di controllare la velocità con cui vengono inizializzati gli input dello shader.

### <a name="index-any-register"></a>Indicizzare qualsiasi registro

Tutti i registri (registri di [input](dx9-graphics-reference-asm-vs-registers-input.md) e di [output](dx9-graphics-reference-asm-vs-registers-output.md)) possono essere indicizzati tramite il registro del [contatore di cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md) . solo i registri costanti possono essere indicizzati nelle versioni precedenti.

Prima di indicizzarle, è necessario dichiarare i registri di input e di output. Tuttavia, non è possibile indicizzare alcun registro di output dichiarato con una semantica di posizione o dimensione del punto. Infatti, se si usa l'indicizzazione, la semantica position e psize deve essere dichiarata rispettivamente nei registri o0 e O1.

È consentito solo indicizzare un intervallo continuo di registri; ovvero non è possibile indicizzare tra i registri che non sono stati dichiarati. Sebbene questa restrizione possa risultare scomoda, consente di eseguire l'ottimizzazione dell'hardware. Il tentativo di eseguire l'indicizzazione tra registri non contigui produrrà risultati non definiti. La convalida dello shader non impone questa restrizione.

### <a name="simplify-output-registers"></a>Semplificare i registri di output

Tutti i vari tipi di registri di output sono stati compressi in dodici registri di output: 1 per posizione, 2 per colore, 8 per trama e 1 per nebbia o dimensione punto. Questi registri eseguiranno l'interpolazione di tutti i dati che contengono per la pixel shader. Le dichiarazioni di registro di output sono obbligatorie e la semantica viene assegnata a ogni registro.

I registri possono essere suddivisi come segue:

-   Almeno un registro deve essere dichiarato come una posizione a quattro componenti. Si tratta dell'unico registro vertex shader obbligatorio.
-   I primi dieci registri utilizzati da uno shader possono usare un massimo di quattro componenti (xyzw).
-   Il registro ultimo (o dodicesimo) può contenere solo un valore scalare, ad esempio la dimensione del punto.

Per un elenco dei registri, vedere [Registers-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).

### <a name="texture-sample-in-a-vertex-shader"></a>Esempio di trama in un vertex shader

Vertex Shader 3 \_ 0 supporta la ricerca di trame nel vertex shader usando [texldl-vs](texldl---vs.md).

## <a name="pixel-shader-model-3-features"></a>Funzionalità del pixel shader modello 3

I registri colori e trama pixel shader sono stati compressi in dieci registri di input (vedere [tipi di registro di input](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)). Il registro visi è un registro scalare a virgola mobile. Solo il segno di questo registro è valido. Se il segno è negativo, la primitiva è una faccia posteriore. Questa operazione può essere utilizzata all'interno di un pixel shader per ottenere l'illuminazione a due lati, ad esempio. Il registro di posizione fa riferimento ai pixel correnti (x, y).

I registri costanti dello shader possono essere impostati utilizzando:

-   [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a>Semantica di corrispondenza in Visual Studio \_ 3 \_ 0 e PS \_ 3 \_ 0 Shader

Esistono alcune restrizioni sull'utilizzo semantico con vs \_ 3 \_ 0 e PS \_ 3 \_ 0. In generale, è necessario prestare attenzione quando si usa una semantica per un input dello shader che corrisponde a una semantica usata in un output dello shader.

Ad esempio, questo pixel shader comprime più nomi in un unico registro:


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



Ogni registro presenta una semantica diversa. Si noti che è anche possibile denominare V0. x e V0. YZ con una semantica diversa (multipla) a causa dell'uso della maschera di scrittura.

Data la pixel shader, \_ non è possibile associare il seguente shader a Visual Studio 3 \_ 0:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



Questi due shader sono in conflitto con l'uso della semantica [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) e **D3DDECLUSAGE \_ TEXCOORD1** .

Riscrivere il vertex shader come questo per evitare la collisione semantica:


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



Analogamente, non è possibile usare un nome semantico dichiarato in registri di input diversi nel pixel shader (V0 e V1 nel pixel shader) in un unico registro di output in questo vertex shader. Questo vertex shader, ad esempio, non può essere associato al pixel shader perché D3DDECLUSAGE \_ TEXCOORD1 viene usato per i registri di input pixel shader (V0, V1) e il registro di output di vertex shader.


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



D'altra parte, questo vertex shader non può essere associato al pixel shader perché la maschera di output per un parametro con una semantica specificata non fornisce i dati richiesti dall'pixel shader:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



Questo vertex shader non fornisce un output con uno dei nomi semantici richiesti dall'pixel shader, quindi l'associazione dello shader non è valida:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a>Modifiche della modalità nebbia, profondità e ombreggiatura

Quando D3DRS \_ MODOOMBRA è impostato per l'ombreggiatura flat durante la rasterizzazione e la rasterizzazione dei triangolari, gli attributi con \_ colore D3DDECLUSAGE vengono interpolati come ombreggiatura piatta. Se uno o più componenti di un registro sono dichiarati con una semantica di colore, ma a altri componenti dello stesso registro viene assegnata una semantica diversa, l'interpolazione dell'ombreggiatura piatta (lineare rispetto a quella Flat) non sarà definita nei componenti di tale registro senza una semantica di colore.

Se si desidera il rendering di nebbia, gli \_ shader vs 3 \_ 0 e PS \_ 3 \_ 0 devono implementare la nebbia. Nessun calcolo di nebbia viene eseguito all'esterno degli shader. Non esiste alcun registro di nebbia in vs \_ 3 \_ 0 e la semantica aggiuntiva D3DDECLUSAGE \_ Fog (per il fattore di Blend di nebbia calcolato per vertice) e \_ la profondità D3DDECLUSAGE (per passare un valore di profondità al pixel shader per calcolare il fattore di Blend di nebbia) sono state aggiunte.

Lo stato della fase trama D3DTSS \_ TEXCOORDINDEX viene ignorato quando si usa pixel shader 3,0.

Per soddisfare queste modifiche sono stati aggiunti i valori seguenti:


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a>Conversioni a virgola mobile e Integer

La matematica a virgola mobile si verifica con precisione e intervalli diversi (a 16 bit, a 24 bit e a 32 bit) in parti diverse della pipeline. Un valore maggiore dell'intervallo dinamico della pipeline che immette la pipeline (ad esempio, una mappa di trama float a 32 bit viene campionata in una pipeline float a 24 bit in PS \_ 2 \_ 0) crea un risultato non definito. Per un comportamento prevedibile, è necessario bloccare tale valore all'intervallo dinamico massimo.

La conversione da un valore a virgola mobile a un numero intero si verifica in diversi punti, ad esempio:

-   Quando si incontra un'istruzione [mova-vs](mova---vs.md) .
-   Durante l'indirizzamento della trama.
-   Quando si scrive in una destinazione di rendering non a virgola mobile.

## <a name="specifying-full-or-partial-precision"></a>Specifica della precisione completa o parziale

PS \_ 3 \_ 0 e PS \_ 2 \_ x offrono supporto per due livelli di precisione:



|          |          |                   |                      |
|----------|----------|-------------------|----------------------|
| PS \_ 3 \_ 0 | PS \_ 2 \_ 0 | Precision         | Valore                |
| x        |          | Full              | FP32 o versione successiva       |
| x        |          | Precisione parziale | FP16 = s10e5           |
| x        | x        | Full              | fp24 = s16e7 o versione successiva |
| x        | x        | Precisione parziale | FP16 = s10e5           |



 

PS \_ 3 \_ 0 supporta una precisione maggiore di quella di PS \_ 2 \_ 0. Per impostazione predefinita, tutte le operazioni si verificano a livello di precisione totale.

La precisione parziale (vedere [modificatori del registro pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers.md)) viene richiesta aggiungendo il \_ modificatore PP al codice dello shader (purché l'implementazione sottostante la supporti). Le implementazioni sono sempre libere di ignorare il modificatore ed eseguire le operazioni interessate con la massima precisione.

Il \_ modificatore di PP può essere eseguito in due contesti:

-   In una dichiarazione di coordinata di trama per passare le coordinate di trama a precisione parziale al pixel shader. Questo può essere usato quando le coordinate di trama inoltrano i dati di colore al pixel shader, che può essere più veloce con precisione parziale rispetto alla precisione completa in alcune implementazioni.
-   Su qualsiasi istruzione per richiedere l'uso della precisione parziale, incluse le istruzioni per il caricamento della trama. Ciò indica che l'implementazione è autorizzata a eseguire l'istruzione con precisione parziale e archiviare un risultato di precisione parziale. In assenza di un modificatore esplicito, l'istruzione deve essere eseguita a precisione completa (indipendentemente dalla precisione degli operandi di input).

Un'applicazione può scegliere intenzionalmente di comportare la precisione per le prestazioni. Esistono diversi tipi di dati di input dello shader che sono candidati naturali per l'elaborazione della precisione parziale:

-   Gli iteratori di colore sono rappresentati correttamente da valori con precisione parziale.
-   I valori di trama dalla maggior parte dei formati possono essere rappresentati in modo accurato da valori a precisione parziale (i valori campionati da trame 32 in formato a virgola mobile sono un'eccezione ovvia).
-   Le costanti possono essere rappresentate dalla rappresentazione a precisione parziale, in base alle esigenze dello shader.

In tutti questi casi lo sviluppatore può scegliere di specificare la precisione parziale per elaborare i dati, sapendo che non viene persa la precisione dei dati di input. In alcuni casi, è possibile che uno shader richieda che i passaggi interni di un calcolo vengano eseguiti con la massima precisione anche quando i valori di input e di output finale non hanno una precisione parziale.

## <a name="software-vertex-and-pixel-shaders"></a>Vertex e pixel shader software

Le implementazioni del software (Runtime e riferimento per vertex shader e informazioni di riferimento per i pixel shader) della versione 2 \_ 0 Shader e versioni successive presentano una convalida attenuata. Questa operazione è utile a scopo di debug e creazione di prototipi. L'applicazione indica al runtime/assembler che necessita di una convalida attenuata usando il \_ flag SW nell'assembler (ad esempio, vs \_ 2 \_ SW). Uno shader software non funzionerà con l'hardware.

vs \_ 2 \_ SW è un relax fino al limite massimo di vs \_ 2 \_ x; Analogamente, PS \_ 2 \_ SW è un rilassamento per i limiti massimi di PS \_ 2 \_ x. In particolare, le convalide seguenti sono rilassate:



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Modello di shader                               | Risorsa                             | Limite                                                                                                                             |
| vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Conteggi istruzioni                   | Nessuna limitazione                                                                                                                         |
| vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Registri costanti float             | 8192                                                                                                                              |
| vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Registri costanti Integer           | 2048                                                                                                                              |
| vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Registri costanti booleani           | 2048                                                                                                                              |
| PS \_ 2 \_ SW                                  | Profondità lettura dipendente                 | Nessuna limitazione                                                                                                                         |
| vs \_ 2 \_ SW                                  | istruzioni ed etichette per il controllo di flusso | Nessuna limitazione                                                                                                                         |
| vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Inizio/passaggio/conteggi ciclo               | Le dimensioni del passaggio di iterazione e inizio iterazione per le istruzioni Rep e loop sono interi con segno a 32 bit. Il numero può essere massimo di \_ int/64. |
| vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Limiti della porta                          | I limiti della porta per tutti i file di registro sono rilassati.                                                                                   |
| Visual Studio \_ 3 \_ SW                                  | Numero di interpolatori              | 16 registri di output in vs \_ 3 \_ SW.                                                                                                 |
| PS \_ 3 \_ SW                                  | Numero di interpolatori              | 14 (16-2) registri di input per PS \_ 3 \_ SW.                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 