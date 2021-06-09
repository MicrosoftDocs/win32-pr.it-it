---
title: Modello shader 3 (informazioni di riferimento su HLSL)
description: I vertex shader e i pixel shader sono notevolmente semplificati rispetto alle versioni precedenti dello shader.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d87c791694e91de135052b4172e3bd5f55577d7
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827100"
---
# <a name="shader-model-3-hlsl-reference"></a>Modello shader 3 (informazioni di riferimento su HLSL)

I vertex shader e i pixel shader sono notevolmente semplificati rispetto alle versioni precedenti dello shader. Se si implementano shader nell'hardware, non è possibile usare vs \_ 3 0 o \_ ps \_ 3 0 con altre versioni dello shader e non è possibile usare alcun tipo di shader con la pipeline di funzioni \_ fisse. Queste modifiche consentono di semplificare i driver e il runtime. L'unica eccezione è che gli shader solo software e 3 0 possono essere usati con qualsiasi \_ \_ pixel shader versione. Inoltre, se si usa uno shader solo software rispetto a 3 0 con una versione precedente di pixel shader, il vertex shader può usare solo la semantica di output compatibile con i codici \_ \_ FVF (Flexible Vertex Format).

La semantica usata per gli output di vertex shader deve essere usata pixel shader input. La semantica viene usata per eseguire il mapping degli output del vertex shader agli input pixel shader, analogamente al modo in cui viene eseguito il mapping della dichiarazione dei vertici ai registri di input del vertex shader e ai modelli shader precedenti. Vedere Match Semantics on vs 3.0 and ps 3.0 Shaders (Semantica di corrispondenza in vs 3.0 e ps 3.0 Shader).

Sono stati aggiunti altri stati di rendering della modalità di ritorno a capo per coprire la possibilità di coordinate di trama aggiuntive in questo nuovo schema. Gli attributi con D3DDECLUSAGE TEXCOORD e l'indice di utilizzo da 0 a 15 vengono interpolati in modalità di ritorno a capo quando viene impostato il corrispondente \_ [**\_ WRAP \* D3DRS.**](/windows/desktop/direct3d9/d3drenderstatetype)

-   [Funzionalità di Vertex Shader Model 3](#vertex-shader-model-3-features)
-   [Funzionalità di Pixel Shader Model 3](#pixel-shader-model-3-features)
-   [Semantica di corrispondenza per gli \_ shader 3 \_ 0 e ps \_ 3 \_ 0](/windows)
-   [Modifiche alla modalità nebbia, profondità e ombreggiatura](#fog-depth-and-shading-mode-changes)
-   [Conversioni a virgola mobile e interi](#floating-point-and-integer-conversions)
-   [Specifica della precisione completa o parziale](#specifying-full-or-partial-precision)
-   [Vertici software e pixel shader](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a>Funzionalità di Vertex Shader Model 3

I tipi di registro di output vertex shader sono stati compressi in dodici registri (vedere [Registri di output](dx9-graphics-reference-asm-vs-registers-output.md)). Ogni registro usato deve essere dichiarato usando l'istruzione [dcl](dcl-usage---ps.md) e una semantica ,ad esempio dcl \_ color0 o0.xyzw.

Il modello di vertex shader a \_ 3 0 (rispetto a 3 0) si espande sulle funzionalità di vs 2 0 con l'indicizzazione dei registri più potente, un set di registri di output semplificati, la possibilità di campionare una trama in un vertex shader e la possibilità di controllare la velocità con cui vengono inizializzati \_ \_ gli input dello \_ \_ shader.

### <a name="index-any-register"></a>Indicizza qualsiasi registro

Tutti i registri ( [Registro di input](dx9-graphics-reference-asm-vs-registers-input.md) e Registri di [output](dx9-graphics-reference-asm-vs-registers-output.md)) possono essere indicizzati usando loop [counter register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (solo i registri costanti possono essere indicizzati nelle versioni precedenti).

È necessario dichiarare i registri di input e output prima di indicizzarli. Tuttavia, non è possibile indicizzare alcun registro di output dichiarato con una semantica delle dimensioni di posizione o punto. In realtà, se si usa l'indicizzazione, la semantica di posizione e psize devono essere dichiarate rispettivamente nei registri o0 e o1.

È consentito indicizzare solo un intervallo continuo di registri. in altri, non è possibile indicizzare i registri che non sono stati dichiarati. Anche se questa restrizione può essere poco pratico, consente di eseguire l'ottimizzazione dell'hardware. Il tentativo di indicizzare i registri non contigui produrrà risultati non definiti. La convalida dello shader non applica questa restrizione.

### <a name="simplify-output-registers"></a>Semplificare i registri di output

Tutti i vari tipi di registri di output sono stati compressi in dodici registri di output: 1 per la posizione, 2 per il colore, 8 per la trama e 1 per le dimensioni della nebbia o del punto. Questi registri interpoleranno tutti i dati che contengono per il pixel shader. Le dichiarazioni del registro di output sono obbligatorie e la semantica viene assegnata a ogni registro.

I registri possono essere suddivisi nel modo seguente:

-   Almeno un registro deve essere dichiarato come registro di posizione a quattro componenti. Questo è l'unico registro vertex shader necessario.
-   I primi dieci registri utilizzati da uno shader possono usare un massimo di quattro componenti (xyzw).
-   L'ultimo registro (o dodicesimo) può contenere solo un valore scalare (ad esempio dimensioni in punti).

Per un elenco dei registri, vedere [Registri - vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).

### <a name="texture-sample-in-a-vertex-shader"></a>Esempio di trama in un vertex shader

Vertex shader 3 0 supporta la ricerca di trame nel \_ vertex shader [usando texldl - rispetto a](texldl---vs.md).

## <a name="pixel-shader-model-3-features"></a>Funzionalità di Pixel Shader Model 3

I pixel shader colori e trame sono stati compressi in dieci registri di input (vedere [Tipi di registro di input](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)). Il registro viso è un registro scalare a virgola mobile. Solo il segno di questo registro è valido. Se il segno è negativo, la primitiva è un viso posteriore. Può essere usato all'interno di un pixel shader per ottenere l'illuminazione a due lati, ad esempio. Il Registro posizioni fa riferimento ai pixel correnti (x,y).

I registri delle costanti shader possono essere impostati usando:

-   [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a>Semantica di corrispondenza per gli \_ shader 3 \_ 0 e ps \_ 3 \_ 0

Esistono alcune restrizioni sull'utilizzo semantico rispetto a \_ 3 \_ 0 e ps \_ 3 \_ 0. In generale, è necessario prestare attenzione quando si usa una semantica per un input shader che corrisponde a una semantica usata in un output dello shader.

Ad esempio, questo pixel shader più nomi in un unico registro:


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



Ogni registro ha una semantica diversa. Si noti che è anche possibile assegnare ai nomi v0.x e v0.yz una semantica diversa (più) a causa dell'uso della maschera di scrittura.

Dato il pixel shader, non è possibile associare lo shader seguente rispetto a \_ \_ 3 0:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



Questi due shader sono in conflitto con l'uso delle semantiche [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) e **D3DDECLUSAGE \_ TEXCOORD1.**

Riscrivere il vertex shader in questo modo per evitare la collisione semantica:


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



Analogamente, un nome semantico dichiarato in registri di input diversi nel pixel shader (v0 e v1 nel pixel shader) non può essere usato in un singolo registro di output in questo vertex shader. Ad esempio, questo vertex shader non può essere associato al pixel shader perché D3DDECLUSAGE TEXCOORD1 viene usato sia per i registri di input pixel shader (v0, v1) che per il registro di output del \_ vertex shader o3.


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



D'altra parte, questo vertex shader non può essere associato al pixel shader perché la maschera di output per un parametro con una semantica specificata non fornisce i dati richiesti dal pixel shader:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



Questo vertex shader non fornisce un output con uno dei nomi semantici richiesti dal pixel shader, quindi l'associazione dello shader non è valida:


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



## <a name="fog-depth-and-shading-mode-changes"></a>Modifiche alla modalità nebbia, profondità e ombreggiatura

Quando D3DRS SHADEMODE è impostato per l'ombreggiatura piatta durante il ritaglio e la rasterizzazione del triangolo, gli attributi con \_ D3DDECLUSAGE COLOR vengono interpolati come ombreggiatura \_ piatta. Se i componenti di un registro vengono dichiarati con una semantica dei colori, ma ad altri componenti dello stesso registro viene data una semantica diversa, l'interpolazione dell'ombreggiatura flat (lineare o flat) non sarà definita nei componenti del registro senza una semantica del colore.

Se si desidera il rendering della nebbia, gli \_ \_ shader ps 3 0 e ps \_ 3 \_ 0 devono implementare la nebbia. Non viene eseguito alcun calcolo della nebbia all'esterno degli shader. Non è presente alcun registro di nebbia in confronto a 3 0 e sono state aggiunte altre semantiche D3DDECLUSAGE FOG (per il fattore di blend della nebbia calcolato per vertice) e \_ \_ \_ D3DDECLUSAGE DEPTH (per passare un valore di profondità al pixel shader per calcolare il fattore di blend della \_ nebbia).

Lo stato della fase della trama D3DTSS TEXCOORDINDEX viene ignorato quando si usa \_ pixel shader 3.0.

Per supportare queste modifiche, sono stati aggiunti i valori seguenti:


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



## <a name="floating-point-and-integer-conversions"></a>Conversioni a virgola mobile e interi

La matematica a virgola mobile avviene a precisione e intervalli diversi (16 bit, 24 bit e 32 bit) in parti diverse della pipeline. Un valore maggiore dell'intervallo dinamico della pipeline che entra nella pipeline (ad esempio, una mappa di trama float a 32 bit viene campionata in una pipeline float a 24 bit in ps \_ 2 0) crea un risultato non \_ definito. Per un comportamento prevedibile, è necessario impostare tale valore sul valore massimo dell'intervallo dinamico.

La conversione da un valore a virgola mobile a un numero intero avviene in diverse posizioni, ad esempio:

-   Quando si incontra una [mova- o un'istruzione.](mova---vs.md)
-   Durante l'indirizzamento della trama.
-   Quando si scrive in una destinazione di rendering non a virgola mobile.

## <a name="specifying-full-or-partial-precision"></a>Specifica della precisione completa o parziale

Sia ps \_ 3 \_ 0 che ps 2 x forniscono il supporto \_ per due livelli di \_ precisione:



| ps \_ 3 \_ 0 | ps \_ 2 \_ 0 | Precisione         | Valore                |
|----------|----------|-------------------|----------------------|
| x        |          | Full              | fp32 o versione successiva       |
| x        |          | Precisione parziale | fp16=s10e5           |
| x        | x        | Full              | fp24=s16e7 o versione successiva |
| x        | x        | Precisione parziale | fp16=s10e5           |



 

ps \_ 3 \_ 0 supporta una precisione maggiore rispetto a ps \_ 2 \_ 0. Per impostazione predefinita, tutte le operazioni vengono eseguite al livello di precisione completo.

La precisione parziale (vedere [Modificatori di registro](dx9-graphics-reference-asm-ps-registers-modifiers.md)pixel shader) viene richiesta aggiungendo il modificatore pp al codice dello shader (a condizione che l'implementazione \_ sottostante lo supporti). Le implementazioni sono sempre liberi di ignorare il modificatore ed eseguire le operazioni interessate con la massima precisione.

Il \_ modificatore pp può verificarsi in due contesti:

-   In una dichiarazione di coordinate di trama per passare coordinate di trama a precisione parziale al pixel shader. Può essere usato quando la trama coordina l'inoltro dei dati di colore al pixel shader, che può essere più veloce con precisione parziale rispetto alla precisione completa in alcune implementazioni.
-   In qualsiasi istruzione per richiedere l'uso di precisione parziale, incluse le istruzioni di caricamento della trama. Ciò indica che l'implementazione può eseguire l'istruzione con precisione parziale e archiviare un risultato a precisione parziale. In assenza di un modificatore esplicito, l'istruzione deve essere eseguita con precisione completa (indipendentemente dalla precisione degli operandi di input).

Un'applicazione potrebbe scegliere deliberatamente di trovare un compromesso tra precisione e prestazioni. Esistono diversi tipi di dati di input shader che sono candidati naturali per l'elaborazione con precisione parziale:

-   Gli iteratori di colore sono ben rappresentati da valori a precisione parziale.
-   I valori di trama della maggior parte dei formati possono essere rappresentati in modo accurato da valori a precisione parziale(i valori campionati da trame in formato a virgola mobile a 32 bit sono un'eccezione ovvia).
-   Le costanti possono essere rappresentate da una rappresentazione a precisione parziale in base alle esigenze dello shader.

In tutti questi casi lo sviluppatore può scegliere di specificare una precisione parziale per elaborare i dati, sapendo che non viene persa alcuna precisione dei dati di input. In alcuni casi, uno shader può richiedere che i passaggi interni di un calcolo siano eseguiti con la massima precisione anche quando i valori di input e di output finale non hanno una precisione maggiore di parziale.

## <a name="software-vertex-and-pixel-shaders"></a>Vertex software e pixel shader

Le implementazioni software (fase di esecuzione e riferimento per vertex shader e informazioni di riferimento per i pixel shader) degli shader versione 2 0 e successive hanno una convalida \_ più disincisa. Ciò è utile a scopo di debug e prototipazione. L'applicazione indica al runtime/assembler che è necessario un po' di convalida con il \_ flag sw nell'assembler (ad esempio, vs \_ 2 \_ sw). Uno shader software non funziona con l'hardware.

vs 2 sw è un'avaie ai limiti massimi di vs \_ \_ \_ 2 \_ x; analogamente, ps 2 sw è un'avarita al limite massimo di \_ \_ ps \_ 2 \_ x. In particolare, le convalide seguenti sono di tipo relaxed:



| Modello shader                                           |  Risorsa                                    |  Limite                                                                                                                                  |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Conteggi delle istruzioni                   | Nessuna limitazione                                                                                                                         |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Registri costanti Float             | 8192                                                                                                                              |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Registri costanti Integer           | 2048                                                                                                                              |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Registri costanti booleani           | 2048                                                                                                                              |
| ps \_ 2 \_ sw                                  | Profondità di lettura dipendente                 | Nessuna limitazione                                                                                                                         |
| vs \_ 2 \_ sw                                  | istruzioni ed etichette per il controllo di flusso | Nessuna limitazione                                                                                                                         |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Inizio/passaggio/conteggio del ciclo               | Le dimensioni dei passaggi di inizio e iterazione per le istruzioni rep e loop sono interi con segno a 32 bit. Il conteggio può essere fino a MAX \_ INT/64. |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Limiti delle porte                          | I limiti delle porte per tutti i file di registro sono di tipo relaxed.                                                                                   |
| vs \_ 3 \_ sw                                  | Numero di interpolatori              | 16 registri di output in vs \_ 3 \_ sw.                                                                                                 |
| ps \_ 3 \_ sw                                  | Numero di interpolatori              | 14(16-2) registri di input per ps \_ 3 \_ sw.                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
