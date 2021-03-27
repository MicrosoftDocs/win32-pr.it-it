---
title: Scrittura di shader HLSL in Direct3D 9
description: Scrittura di shader HLSL in Direct3D 9
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 504a1d9ff5a2aa2b37227f0016cdc97d28d967fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047132"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a>Scrittura di shader HLSL in Direct3D 9

-   [Nozioni di base sui vertex shader](#vertex-shader-basics)
-   [Nozioni di base su pixel shader](#pixel-shader-basics)
    -   [Stati della fase trama e del campionatore](#texture-stage-and-sampler-states)
    -   [Input pixel shader](#pixel-shader-inputs)
    -   [Output pixel shader](#pixel-shader-outputs)
-   [Input shader e variabili dello shader](#shader-inputs-and-shader-variables)
    -   [Dichiarazione di variabili shader](#declaring-shader-variables)
    -   [Input shader uniformi](#uniform-shader-inputs)
    -   [Variazione degli input e della semantica degli shader](#varying-shader-inputs-and-semantics)
    -   [Oggetti Sampler e texture](#samplers-and-texture-objects)
-   [Scrittura di funzioni](#writing-functions)
-   [Controllo di flusso](#flow-control)
-   [Argomenti correlati](#related-topics)

## <a name="vertex-shader-basics"></a>Nozioni di base Vertex-Shader

Quando è in esecuzione, un vertex shader programmabile sostituisce l'elaborazione dei vertici eseguita dalla pipeline grafica Microsoft Direct3D. Quando si usa un vertex shader, le informazioni di stato relative alle operazioni di trasformazione e illuminazione vengono ignorate dalla pipeline della funzione fissa. Quando vertex shader è disabilitato e viene restituita l'elaborazione della funzione fissa, vengono applicate tutte le impostazioni dello stato corrente.

Il mosaico di primitive di ordine deve essere eseguito prima dell'esecuzione del vertex shader. Le implementazioni che eseguono il mosaico della superficie dopo l'elaborazione dello shader devono eseguire questa operazione in modo che non risulti evidente per l'applicazione e il codice dello shader.

Come minimo, un vertex shader deve restituire la posizione del vertice nello spazio di clip omogeneo. Facoltativamente, il vertex shader può restituire le coordinate di trama, il colore del vertice, l'illuminazione dei vertici, i fattori di nebbia e così via.

## <a name="pixel-shader-basics"></a>Nozioni di base Pixel-Shader

L'elaborazione dei pixel viene eseguita da pixel shader sui singoli pixel. I pixel shader funzionano in concerto con i vertex shader; l'output di un vertex shader fornisce gli input per un pixel shader. Dopo l'esecuzione dello shader, si verificano altre operazioni sui pixel, ovvero la fusione di nebbia, le operazioni dello stencil e la combinazione di destinazione di rendering.

### <a name="texture-stage-and-sampler-states"></a>Stati della fase trama e del campionatore

Un pixel shader sostituisce completamente la funzionalità di combinazione di pixel specificata dal Blender a più trame, incluse le operazioni definite in precedenza dagli Stati della fase della trama. Le operazioni di campionamento e filtro delle trame controllate dagli Stati della fase di trama standard per minification, ingrandimento, filtro MIP e modalità di indirizzamento a capo possono essere inizializzate in shader. L'applicazione è gratuita per modificare questi stati senza richiedere la rigenerazione dello shader attualmente associato. L'impostazione dello stato può essere semplificata anche se gli shader sono progettati in un effetto.

### <a name="pixel-shader-inputs"></a>Input pixel shader

Per pixel shader versioni PS \_ 1 \_ 1-PS \_ 2 \_ 0, i colori a tinta diffusa e speculare sono saturi (clampati) nell'intervallo compreso tra 0 e 1 prima dell'uso da parte dello shader.

Si presuppone che i valori dei colori input per la pixel shader siano corretti, ma ciò non è garantito (per tutti i componenti hardware). I colori campionati dalle coordinate di trama vengono iterati in modo corretto e vengono fissati nell'intervallo da 0 a 1 durante l'iterazione.

### <a name="pixel-shader-outputs"></a>Output pixel shader

Per pixel shader versioni PS \_ 1 \_ 1-PS \_ 1 \_ 4, il risultato emesso dall'pixel shader è il contenuto del registro R0. Ciò che contiene quando lo shader completa l'elaborazione viene inviato alla fase di nebbia e al Blender di destinazione di rendering.

Per pixel shader versioni PS \_ 2 \_ 0 e successive, il colore di output viene emesso da OC0-oC4.

## <a name="shader-inputs-and-shader-variables"></a>Input shader e variabili dello shader

-   [Dichiarazione di variabili shader](#declaring-shader-variables)
-   [Input shader uniformi](#uniform-shader-inputs)
-   [Variazione degli input e della semantica degli shader](#varying-shader-inputs-and-semantics)
-   [Oggetti Sampler e texture](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a>Dichiarazione di variabili shader

La dichiarazione di variabile più semplice include un tipo e un nome di variabile, ad esempio questa dichiarazione a virgola mobile:


```
float fVar;
```



È possibile inizializzare una variabile nella stessa istruzione.


```
float fVar = 3.1f;
```



È possibile dichiarare una matrice di variabili,


```
int iVar[3];
```



o dichiarati e inizializzati nella stessa istruzione.


```
int iVar[3] = {1,2,3};
```



Di seguito sono riportate alcune dichiarazioni che illustrano molte delle caratteristiche delle variabili HLSL (High-Level Shader Language):


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



Le dichiarazioni di dati possono usare qualsiasi tipo valido, tra cui:

-   [Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
-   [Tipo Vector (DirectX HLSL)](dx-graphics-hlsl-vector.md)
-   [Tipo matrice (DirectX HLSL)](dx-graphics-hlsl-matrix.md)
-   [Tipo shader (DirectX HLSL)](dx-graphics-hlsl-shader.md)
-   [Tipo campionatore (DirectX HLSL)](dx-graphics-hlsl-sampler.md)
-   [Tipo definito dall'utente (DirectX HLSL)](dx-graphics-hlsl-user-defined.md)

Uno shader può includere variabili, argomenti e funzioni di primo livello.


```
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```



Le variabili di primo livello sono dichiarate al di fuori di tutte le funzioni. Gli argomenti di primo livello sono parametri di una funzione di primo livello. Una funzione di primo livello è qualsiasi funzione chiamata dall'applicazione (in contrapposizione a una funzione chiamata da un'altra funzione).

### <a name="uniform-shader-inputs"></a>Input shader uniformi

I vertex e i pixel shader accettano due tipi di dati di input: variabile e uniforme. L'input variabile è costituito dai dati univoci per ogni esecuzione dello shader. Per un vertex shader, i dati variabili (ad esempio, position, Normal e così via) provengono dai flussi dei vertici. I dati uniformi, ad esempio colore materiale, trasformazione globale e così via, sono costanti per più esecuzioni di uno shader. Per coloro che hanno familiarità con i modelli shader dell'assembly, i dati uniformi vengono specificati dai registri costanti e dai dati variabili in base ai registri v e t.

I dati uniformi possono essere specificati da due metodi. Il metodo più comune consiste nel dichiarare le variabili globali e utilizzarle in uno shader. Qualsiasi utilizzo di variabili globali all'interno di uno shader comporta l'aggiunta di tale variabile all'elenco di variabili uniformi richieste da tale shader. Il secondo metodo consiste nel contrassegnare un parametro di input della funzione shader di primo livello come uniforme. Questo contrassegno specifica che la variabile specificata deve essere aggiunta all'elenco di variabili uniformi.

Le variabili uniformi utilizzate da uno shader vengono restituite all'applicazione tramite la tabella Constant. La tabella Constant è il nome della tabella dei simboli che definisce il modo in cui le variabili uniformi utilizzate da uno shader si adattano ai registri costanti. I parametri di funzione uniformi vengono visualizzati nella tabella delle costanti preceduto da un segno di dollaro ($), a differenza delle variabili globali. Il simbolo del dollaro è necessario per evitare conflitti di nomi tra input uniformi locali e variabili globali con lo stesso nome.

La tabella Constant contiene i percorsi di registro costanti di tutte le variabili uniformi utilizzate dallo shader. La tabella include anche le informazioni sul tipo e il valore predefinito, se specificato.

### <a name="varying-shader-inputs-and-semantics"></a>Variazione degli input e della semantica degli shader

I parametri di input variabili (di una funzione shader di primo livello) devono essere contrassegnati con una parola chiave semantica o uniforme che indica che il valore è costante per l'esecuzione dello shader. Se un input dello shader di primo livello non è contrassegnato con una parola chiave semantica o uniforme, la compilazione dello shader non verrà completata.

La semantica di input è un nome usato per collegare l'input specificato a un output della parte precedente della pipeline grafica. Il POSITION0 semantico di input, ad esempio, viene usato dai vertex shader per specificare dove devono essere collegati i dati di posizione del buffer dei vertici.

I pixel e i vertex shader hanno set diversi di semantica di input a causa delle diverse parti della pipeline grafica che si nutrono in ogni unità shader. La semantica di input del vertex shader descrive le informazioni per ogni vertice (ad esempio, posizione, normale, coordinate di trama, colore, tangente, binormale e così via) da caricare da un buffer di vertici in un modulo che può essere utilizzato dal vertex shader. La semantica di input viene mappata direttamente all'utilizzo delle dichiarazioni dei vertici e all'indice di utilizzo.

La semantica di input del pixel shader descrive le informazioni fornite per pixel dall'unità di rasterizzazione. I dati vengono generati dall'interpolazione tra gli output del vertex shader per ogni vertice della primitiva corrente. La semantica di input pixel shader di base collega le informazioni sul colore di output e sulle coordinate di trama ai parametri di input.

La semantica di input può essere assegnata all'input dello shader tramite due metodi:

-   Aggiunta di due punti e del nome semantico alla dichiarazione di parametro.
-   Definizione di una struttura di input con semantica di input assegnata a ogni membro della struttura.

I vertex e i pixel shader forniscono i dati di output alla fase successiva della pipeline grafica. La semantica di output viene utilizzata per specificare la modalità di collegamento dei dati generati dallo shader agli input della fase successiva. La semantica di output per un vertex shader, ad esempio, viene usata per collegare gli output degli interpolatori nell'rasterizzatore per generare i dati di input per la pixel shader. Gli output pixel shader sono i valori forniti all'unità di fusione alfa per ogni destinazione di rendering o il valore di profondità scritto nel buffer di profondità.

La semantica di output di vertex shader viene usata per collegare lo shader sia al pixel shader che alla fase di rasterizzazione. Un vertex shader utilizzato dal rasterizzatore e non esposto all'pixel shader deve generare come minimo i dati di posizione. I vertex shader che generano dati di coordinate e coordinate di trama forniscono i dati a un pixel shader dopo che è stata eseguita l'interpolazione.

La semantica di output di pixel shader associa i colori di output di un pixel shader con la destinazione di rendering corretta. Il colore di output del pixel shader è collegato alla fase Alpha Blend, che determina la modalità di modifica delle destinazioni di rendering della destinazione. È possibile utilizzare l'output pixel shader Depth per modificare i valori di profondità di destinazione nel percorso raster corrente. L'output di profondità e più destinazioni di rendering sono supportati solo con alcuni modelli shader.

La sintassi per la semantica di output è identica alla sintassi per la specifica della semantica di input. La semantica può essere specificata direttamente nei parametri dichiarati come parametri "out" o assegnati durante la definizione di una struttura restituita come parametro "out" o come valore restituito di una funzione.

Semantica che identifica da dove provengono i dati. La semantica è identificatori facoltativi che identificano gli input e gli output dello shader. La semantica viene visualizzata in una delle tre posizioni seguenti:

-   Dopo un membro della struttura.
-   Dopo un argomento nell'elenco di argomenti di input di una funzione.
-   Dopo l'elenco di argomenti di input della funzione.

In questo esempio viene utilizzata una struttura per fornire uno o più input di vertex shader e un'altra struttura per fornire uno o più output del vertex shader. Ogni membro della struttura usa una semantica.


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



La struttura di input identifica i dati dal buffer dei vertici che forniranno gli input dello shader. Questo shader esegue il mapping dei dati dagli elementi position, Normal e BlendWeight del buffer dei vertici ai registri del vertex shader. Il tipo di dati di input non deve corrispondere esattamente al tipo di dati della dichiarazione dei vertici. Se non corrisponde esattamente, i dati dei vertici verranno automaticamente convertiti nel tipo di dati di HLSL quando vengono scritti nei registri dello shader. Ad esempio, se i dati normali sono stati definiti come di tipo UINT dall'applicazione, verranno convertiti in float3 quando vengono letti dallo shader.

Se i dati nel flusso di vertici contengono meno componenti rispetto al tipo di dati shader corrispondente, i componenti mancanti verranno inizializzati su 0 (ad eccezione di w, che viene inizializzato su 1).

La semantica di input è simile ai valori in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).

La struttura di output identifica i parametri di output del vertex shader della posizione e del colore. Questi output verranno usati dalla pipeline per la rasterizzazione dei triangolari (nell'elaborazione primitiva). L'output contrassegnato come dati di posizione denota la posizione di un vertice nello spazio omogeneo. Come minimo, un vertex shader deve generare dati di posizione. La posizione dello spazio sullo schermo viene calcolata dopo il completamento del vertex shader dividendo la coordinata (x, y, z) per w. Nello spazio dello schermo,-1 e 1 sono i valori x e y minimo e massimo dei limiti del viewport, mentre z viene usato per il test del buffer z.

La semantica di output è simile anche ai valori in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage). In generale, una struttura di output per un vertex shader può essere usata anche come struttura di input per un pixel shader, purché il pixel shader non legga da alcuna variabile contrassegnata con la posizione, la dimensione del punto o la semantica di nebbia. Queste semantiche sono associate a valori scalari per vertice che non vengono usati da un pixel shader. Se questi valori sono necessari per il pixel shader, possono essere copiati in un'altra variabile di output che usa una semantica di pixel shader.

Le variabili globali vengono assegnate ai registri automaticamente dal compilatore. Le variabili globali sono denominate anche parametri uniformi perché il contenuto della variabile è lo stesso per tutti i pixel elaborati ogni volta che viene chiamato lo shader. I registri sono contenuti nella tabella Constant, che può essere letta usando l'interfaccia [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) .

La semantica di input per i pixel shader esegue il mapping dei valori in registri hardware specifici per il trasporto tra vertex shader e pixel shader. Ogni tipo di registro ha proprietà specifiche. Poiché attualmente sono disponibili solo due semantiche per le coordinate di colore e trama, la maggior parte dei dati può essere contrassegnata come coordinata di trama anche in caso contrario.

Si noti che la struttura di output del vertex shader usava un input con dati sulla posizione, che non viene usato dal pixel shader. HLSL consente dati di output validi di un vertex shader che non sono dati di input validi per un pixel shader, a condizione che non vi si faccia riferimento nell'pixel shader.

Gli argomenti di input possono essere anche matrici. La semantica viene incrementata automaticamente dal compilatore per ogni elemento della matrice. Si consideri, ad esempio, la seguente dichiarazione esplicita:


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



La dichiarazione esplicita riportata in precedenza equivale alla seguente dichiarazione che avrà una semantica incrementata automaticamente dal compilatore:


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



Analogamente alla semantica di input, la semantica di output identifica l'utilizzo dei dati per pixel shader dati di output. Molti pixel shader scrivono su un solo colore di output. I pixel shader possono anche scrivere un valore di profondità in una o più destinazioni di rendering contemporaneamente (fino a quattro). Analogamente ai vertex shader, i pixel shader usano una struttura per restituire più di un output. Questo shader scrive 0 nei componenti colore, oltre che nel componente profondità.


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



I colori di output del pixel shader devono essere di tipo float4. Quando si scrivono più colori, tutti i colori di output devono essere utilizzati in modo contiguo. In altre parole, [COLOR1](dx-graphics-hlsl-semantics.md) non può essere un output, a meno che [COLOR0](dx-graphics-hlsl-semantics.md) non sia già stato scritto. L'output di profondità del pixel shader deve essere di tipo float1.

### <a name="samplers-and-texture-objects"></a>Oggetti Sampler e texture

Un campionatore contiene lo stato del campionatore. Stato campionatore specifica la trama da campionare e controlla il filtro eseguito durante il campionamento. Per campionare una trama sono necessari tre elementi:

-   Trama
-   Campionatore (con stato campionatore)
-   Un'istruzione di campionamento

I sampler possono essere inizializzati con trame e lo stato del campionatore come illustrato di seguito:


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



Di seguito è riportato un esempio di codice per campionare una trama 2D:


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



La trama viene dichiarata con una variabile di trama tex0.

In questo esempio viene dichiarata una variabile Sampler denominata s \_ 2D. Il campionatore contiene lo stato del campionatore all'interno di parentesi graffe. Include la trama che verrà campionata e, facoltativamente, lo stato del filtro, ovvero le modalità a capo, le modalità di filtro e così via. Se lo stato del campionatore viene omesso, viene applicato uno stato campionatore predefinito che specifica il filtro lineare e una modalità a capo automatico per le coordinate di trama. La funzione sampler accetta una coordinata di trama a virgola mobile a due componenti e restituisce un colore a due componenti. Questa operazione viene rappresentata con il tipo restituito float2 e rappresenta i dati nei componenti rosso e verde.

Sono definiti quattro tipi di Sampler (vedere [parole chiave](dx-graphics-hlsl-appendix.md)) e le ricerche di trama vengono eseguite dalle funzioni intrinseche: [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**Tex3D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE (s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md). Di seguito è riportato un esempio di campionamento 3D:


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



Questa dichiarazione del campionatore usa lo stato del campionatore predefinito per le impostazioni di filtro e la modalità di indirizzo.

Di seguito è riportato l'esempio di campionamento del cubo corrispondente:


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



Infine, di seguito è riportato l'esempio di campionamento 1D:


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



Poiché il runtime non supporta le trame 1D, il compilatore userà una trama 2D con la consapevolezza che la coordinata y non è importante. Poiché [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) viene implementato come ricerca di trama 2D, il compilatore è libero di scegliere il componente y in modo efficiente. In alcuni rari scenari, il compilatore non può scegliere un componente y efficiente, nel qual caso emetterà un avviso.


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



Questo particolare esempio è inefficiente perché il compilatore deve spostare la coordinata di input in un altro registro, perché una ricerca 1D viene implementata come ricerca 2D e la coordinata di trama viene dichiarata come float1. Se il codice viene riscritto usando un input float2 anziché un float1, il compilatore può usare la coordinata di trama di input perché sa che y è inizializzato su un elemento.


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



Tutte le ricerche di trama possono essere aggiunte con "bias" o "proj", ovvero [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**TEXCUBEPROJ (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md). Con il suffisso "proj", la coordinata di trama è divisa per il componente w. Con "bias", il livello MIP viene spostato dal componente w. Pertanto, tutte le ricerche di trama con un suffisso accettano sempre un input float4. [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) e [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignorano rispettivamente i componenti YZ e z.

I sampler possono anche essere usati in una matrice, sebbene nessun back-end supporta attualmente l'accesso alla matrice dinamica dei Sampler. Pertanto, il codice seguente è valido perché può essere risolto in fase di compilazione:


```
tex2D(s[0],tex)
```



Tuttavia, questo esempio non è valido.


```
tex2D(s[a],tex)
```



L'accesso dinamico dei Sampler è utile principalmente per la scrittura di programmi con cicli letterali. Il codice seguente illustra l'accesso all'array del campionatore:


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> L'uso del runtime di debug di Microsoft Direct3D consente di rilevare le mancate corrispondenze tra il numero di componenti in una trama e un campionatore.

 

## <a name="writing-functions"></a>Scrittura di funzioni

Le funzioni interrompono le attività di grandi dimensioni in quelle più piccole. È più facile eseguire il debug delle attività di piccole dimensioni e può essere riutilizzata, una volta collaudato. Le funzioni possono essere utilizzate per nascondere i dettagli di altre funzioni, che rendono più semplice il completamento di un programma composto da funzioni.

Le funzioni HLSL sono simili alle funzioni C in diversi modi: contengono entrambi una definizione e un corpo della funzione ed entrambi dichiarano tipi restituiti ed elenchi di argomenti. Analogamente alle funzioni C, la convalida HLSL esegue il controllo dei tipi sugli argomenti, i tipi di argomento e il valore restituito durante la compilazione dello shader.

Diversamente dalle funzioni C, le funzioni del punto di ingresso di HLSL usano la semantica per associare gli argomenti della funzione agli input e agli output dello shader (le funzioni HLSL chiamate semantica ignorano internamente). Questo consente di associare più facilmente i dati del buffer a uno shader e di associare gli output dello shader agli input dello shader.

Una funzione contiene una dichiarazione e un corpo e la dichiarazione deve precedere il corpo.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



La dichiarazione di funzione include tutto ciò che precede le parentesi graffe:


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Una dichiarazione di funzione contiene:

-   Tipo restituito
-   Nome di funzione
-   Elenco di argomenti (facoltativo)
-   Una semantica di output (facoltativo)
-   Annotazione (facoltativa)

Il tipo restituito può essere uno dei tipi di dati di base di HLSL, ad esempio float4:


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



Il tipo restituito può essere una struttura che è già stata definita:


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



Se la funzione non restituisce un valore, void può essere utilizzato come tipo restituito.


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



Il tipo restituito viene sempre visualizzato per primo in una dichiarazione di funzione.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Un elenco di argomenti dichiara gli argomenti di input per una funzione. Può anche dichiarare i valori che verranno restituiti. Alcuni argomenti sono entrambi argomenti di input e di output. Di seguito è riportato un esempio di uno shader che accetta quattro argomenti di input.


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



Questa funzione restituisce un colore finale, ovvero una combinazione di un campione di trama e il colore chiaro. La funzione accetta quattro input. Due input hanno una semantica: LightDir ha la semantica [TEXCOORD1](dx-graphics-hlsl-semantics.md) e texcrd ha la semantica [TEXCOORD0](dx-graphics-hlsl-semantics.md) . La semantica significa che i dati per queste variabili proverranno dal buffer dei vertici. Anche se la variabile LightDir ha una semantica [TEXCOORD1](dx-graphics-hlsl-semantics.md) , il parametro non è probabilmente una coordinata di trama. Il tipo semantico TEXCOORDn viene spesso usato per fornire una semantica per un tipo che non è predefinito (non esiste alcuna semantica di input del vertex shader per una direzione di luce).

Gli altri due input LightColor e SAMP sono contrassegnati con la parola chiave [Uniform](dx-graphics-hlsl-appendix.md) . Si tratta di costanti uniformi che non cambiano tra le chiamate di estrazione. I valori per questi parametri provengono dalle variabili globali dello shader.

Gli argomenti possono essere etichettati come input con la parola chiave in e gli argomenti di output con la parola chiave out. Gli argomenti non possono essere passati per riferimento. Tuttavia, un argomento può essere un input e un output se viene dichiarato con la parola chiave InOut. Gli argomenti passati a una funzione contrassegnati con la parola chiave InOut sono considerati copie dell'originale fino a quando non viene restituita la funzione e vengono copiati di nuovo. Di seguito è riportato un esempio di utilizzo di Inout:


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



Questa funzione incrementa i valori in A e B e li restituisce.

Il corpo della funzione è tutto il codice dopo la dichiarazione di funzione.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



Il corpo è costituito da istruzioni racchiuse tra parentesi graffe. Il corpo della funzione implementa tutte le funzionalità usando variabili, valori letterali, espressioni e istruzioni.

Il corpo dello shader esegue due operazioni: esegue una moltiplicazione della matrice e restituisce un risultato float4. La moltiplicazione della matrice viene eseguita con la funzione [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) , che esegue una moltiplicazione della matrice 4x4. **mul (DirectX HLSL)** viene chiamato funzione intrinseca perché è già incorporato nella libreria HLSL di funzioni. Le funzioni intrinseche verranno analizzate più dettagliatamente nella sezione successiva.

La matrice Multiply combina un vettore di input POS e una matrice composita WorldViewProj. Il risultato è la posizione in cui i dati vengono trasformati nello spazio dello schermo. Si tratta dell'elaborazione del vertex shader minima che è possibile eseguire. Se si usa la pipeline della funzione fissa anziché un vertex shader, è possibile che i dati dei vertici vengano disegnati dopo questa trasformazione.

L'ultima istruzione in un corpo della funzione è un'istruzione return. Analogamente a C, questa istruzione restituisce il controllo dalla funzione all'istruzione che ha chiamato la funzione.

I tipi restituiti della funzione possono essere qualsiasi tipo di dati semplice definito in HLSL, tra cui bool, int Half, float e Double. I tipi restituiti possono essere uno dei tipi di dati complessi, ad esempio vettori e matrici. I tipi HLSL che fanno riferimento a oggetti non possono essere utilizzati come tipi restituiti. Sono inclusi PixelShader, vertexshader, texture e Sampler.

Di seguito è riportato un esempio di una funzione che usa una struttura per un tipo restituito.


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



Il tipo restituito float4 è stato sostituito con la struttura di Visual Studio \_ output, che ora contiene un singolo membro float4.

Un'istruzione return segnala la fine di una funzione. Si tratta dell'istruzione return più semplice. Restituisce il controllo dalla funzione al programma chiamante. Non restituisce alcun valore.


```
void main()
{
    return ;
}
```



Un'istruzione Return può restituire uno o più valori. In questo esempio viene restituito un valore letterale:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



In questo esempio viene restituito il risultato scalare di un'espressione:


```
return  light.enabled = true ;
```



In questo esempio viene restituito un float4 costruito da una variabile locale e un valore letterale:


```
return  float4(color.rgb, 1) ;
```



In questo esempio viene restituito un float4 costruito dal risultato restituito da una funzione intrinseca e alcuni valori letterali:


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



In questo esempio viene restituita una struttura che contiene uno o più membri:


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a>Controllo di flusso

La maggior parte dei vertici e dei pixel shader hardware correnti è progettata per eseguire uno shader riga per riga, eseguendo ogni istruzione una sola volta. HLSL supporta il controllo di flusso, che include la diramazione statica, le istruzioni Predicate, il ciclo statico, la diramazione dinamica e il ciclo dinamico.

In precedenza, l'utilizzo di un'istruzione if ha prodotto codice shader in linguaggio assembly che implementa sia il lato if che il lato else del flusso di codice. Di seguito è riportato un esempio del codice in HLSL compilato per vs \_ 1 \_ 1:


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



Ecco il codice assembly risultante:


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



Alcuni componenti hardware consentono il ciclo statico o dinamico, ma la maggior parte richiede l'esecuzione lineare. Nei modelli che non supportano il ciclo, è necessario annullare la registrazione di tutti i cicli. Un esempio è l'esempio di esempio [DepthOfField](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) che usa cicli non registrati anche per gli \_ shader PS 1 \_ 1.

HLSL include ora il supporto per ognuno di questi tipi di controllo di flusso:

-   diramazione statica
-   istruzioni Predicate
-   ciclo statico
-   diramazione dinamica
-   cicli dinamici

La diramazione statica consente l'attivazione o la disattivazione di blocchi di codice dello shader in base a una costante shader booleana. Si tratta di un metodo pratico per abilitare o disabilitare i percorsi di codice in base al tipo di oggetto di cui è in corso il rendering. Tra le chiamate di estrazione, è possibile decidere quali funzionalità si desidera supportare con lo shader corrente, quindi impostare i flag booleani necessari per ottenere tale comportamento. Tutte le istruzioni disabilitate da una costante booleana vengono ignorate durante l'esecuzione dello shader.

Il supporto di branching più noto è la diramazione dinamica. Con la diramazione dinamica, la condizione di confronto si trova in una variabile, il che significa che il confronto viene eseguito per ogni vertice o ogni pixel in fase di esecuzione (in contrapposizione al confronto che si verifica in fase di compilazione o tra due chiamate di richiamo). L'impatto sulle prestazioni è il costo del ramo più il costo delle istruzioni sul lato del ramo creato. La diramazione dinamica è implementata nel modello Shader 3 o versione successiva. L'ottimizzazione degli shader che funzionano con questi modelli è simile all'ottimizzazione del codice eseguito su una CPU.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 