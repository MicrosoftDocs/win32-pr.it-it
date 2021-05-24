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
ms.openlocfilehash: 64a64d08518cb987850c87da3fb19c264519a7f7
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335385"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a>Scrittura di shader HLSL in Direct3D 9

-   [Nozioni di base su vertex shader](#vertex-shader-basics)
-   [Nozioni di base sul pixel shader](#pixel-shader-basics)
    -   [Stati della fase della trama e del campionatore](#texture-stage-and-sampler-states)
    -   [Input pixel shader](#pixel-shader-inputs)
    -   [Output pixel shader](#pixel-shader-outputs)
-   [Input e variabili shader](#shader-inputs-and-shader-variables)
    -   [Dichiarazione di variabili shader](#declaring-shader-variables)
    -   [Input uniform shader](#uniform-shader-inputs)
    -   [Variazione di input e semantica di shader](#varying-shader-inputs-and-semantics)
    -   [Campionatori e oggetti Texture](#samplers-and-texture-objects)
-   [Scrittura di funzioni](#writing-functions)
-   [Controllo di flusso](#flow-control)
-   [Argomenti correlati](#related-topics)

## <a name="vertex-shader-basics"></a>Vertex-Shader di base

Quando è in funzione, un vertex shader programmabile sostituisce l'elaborazione dei vertici eseguita dalla pipeline grafica Microsoft Direct3D. Quando si usa un vertex shader, le informazioni sullo stato relative alle operazioni di trasformazione e illuminazione vengono ignorate dalla pipeline di funzioni fisse. Quando il vertex shader è disabilitato e viene restituita l'elaborazione di funzioni fisse, vengono applicate tutte le impostazioni dello stato corrente.

Prima dell'esecuzione del vertex shader, è necessario eseguire il tessellamento delle primitive di ordine elevato. Le implementazioni che eseguono la tessellazione della superficie dopo l'elaborazione dello shader devono eseguire questa operazione in modo non evidente per il codice dell'applicazione e dello shader.

Come minimo, un vertex shader deve eseguire l'output della posizione del vertice nello spazio di ritaglio omogeneo. Facoltativamente, il vertex shader può eseguire l'output delle coordinate della trama, del colore dei vertici, dell'illuminazione dei vertici, dei fattori del vertice e così via.

## <a name="pixel-shader-basics"></a>Pixel-Shader di base

L'elaborazione dei pixel viene eseguita dai pixel shader su singoli pixel. I pixel shader funzionano insieme ai vertex shader; l'output di un vertex shader fornisce gli input per un pixel shader. Altre operazioni sui pixel (fusione della nebbia, operazioni di stencil e fusione della destinazione di rendering) si verificano dopo l'esecuzione dello shader.

### <a name="texture-stage-and-sampler-states"></a>Stati della fase di trama e del campionatore

Un pixel shader sostituisce completamente la funzionalità di fusione dei pixel specificata dal blender a più trame, incluse le operazioni definite in precedenza dagli stati della fase di trama. Le operazioni di campionamento e filtro trame controllate dagli stati della fase di trama standard per la minificazione, l'ingrandimento, il filtro mip e le modalità di indirizzamento del wrapping, possono essere inizializzate negli shader. L'applicazione è libera di modificare questi stati senza richiedere la rigenerazione dello shader attualmente associato. L'impostazione dello stato può essere resa ancora più semplice se gli shader sono progettati all'interno di un effetto.

### <a name="pixel-shader-inputs"></a>Input pixel shader

Per pixel shader versioni ps 1 - ps 2 0, i colori diffusi e \_ \_ speculari vengono \_ saturati (con chiusura) nell'intervallo da 0 a 1 prima dell'uso da parte dello \_ shader.

Si presuppone che i valori dei pixel shader siano corretti dal punto di vista, ma questo non è garantito (per tutto l'hardware). I colori campionati dalle coordinate della trama vengono iterati in modo corretto dal punto di vista e sono ancorati all'intervallo da 0 a 1 durante l'iterazione.

### <a name="pixel-shader-outputs"></a>Output pixel shader

Per pixel shader versioni ps \_ \_ 1 1 - ps 1 4, il risultato generato dal pixel shader è il contenuto del \_ \_ registro r0. Tutto ciò che contiene al termine dell'elaborazione dello shader viene inviato alla fase della nebbia e al blender di destinazione di rendering.

Per pixel shader versioni ps 2 0 e successive, il colore di output viene generato da \_ \_ oC0 - oC4.

## <a name="shader-inputs-and-shader-variables"></a>Input shader e variabili shader

-   [Dichiarazione di variabili shader](#declaring-shader-variables)
-   [Input uniform shader](#uniform-shader-inputs)
-   [Variazione di input e semantica di shader](#varying-shader-inputs-and-semantics)
-   [Campionatori e oggetti Texture](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a>Dichiarazione di variabili shader

La dichiarazione di variabile più semplice include un tipo e un nome di variabile, ad esempio questa dichiarazione a virgola mobile:


```
float fVar;
```



È possibile inizializzare una variabile nella stessa istruzione.


```
float fVar = 3.1f;
```



È possibile dichiarare una matrice di variabili.


```
int iVar[3];
```



o dichiarato e inizializzato nella stessa istruzione.


```
int iVar[3] = {1,2,3};
```



Di seguito sono illustrate alcune dichiarazioni che illustrano molte delle caratteristiche delle variabili HLSL (High-Level Shader Language):


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



Le dichiarazioni di dati possono usare qualsiasi tipo valido, tra cui:

-   [Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
-   [Tipo di vettore (DirectX HLSL)](dx-graphics-hlsl-vector.md)
-   [Tipo matrice (DirectX HLSL)](dx-graphics-hlsl-matrix.md)
-   [Tipo shader (DirectX HLSL)](dx-graphics-hlsl-shader.md)
-   [Tipo di campionatore (DirectX HLSL)](dx-graphics-hlsl-sampler.md)
-   [Tipo definito dall'utente (DirectX HLSL)](dx-graphics-hlsl-user-defined.md)

Uno shader può avere variabili, argomenti e funzioni di primo livello.


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



Le variabili di primo livello vengono dichiarate all'esterno di tutte le funzioni. Gli argomenti di primo livello sono parametri di una funzione di primo livello. Una funzione di primo livello è qualsiasi funzione chiamata dall'applicazione (a differenza di una funzione chiamata da un'altra funzione).

### <a name="uniform-shader-inputs"></a>Input uniform shader

I vertex shader e i pixel shader accettano due tipi di dati di input: variabili e uniformi. L'input variabile è dato da dati univoci per ogni esecuzione dello shader. Per un vertex shader, i dati variabili (ad esempio posizione, normale e così via) provengono dai flussi dei vertici. I dati uniformi ,ad esempio il colore del materiale, la trasformazione del mondo e così via, sono costanti per più esecuzioni di uno shader. Per gli utenti che hanno familiarità con i modelli di shader dell'assembly, i dati uniformi vengono specificati da registri costanti e dati variabili dai registri v e t.

I dati uniformi possono essere specificati da due metodi. Il metodo più comune è dichiarare le variabili globali e usarle all'interno di uno shader. Qualsiasi uso di variabili globali all'interno di uno shader comporta l'aggiunta di tale variabile all'elenco di variabili uniformi richieste dallo shader. Il secondo metodo è contrassegnare un parametro di input della funzione shader di primo livello come uniforme. Questo contrassegno specifica che la variabile specificata deve essere aggiunta all'elenco di variabili uniformi.

Le variabili uniformi usate da uno shader vengono comunicate all'applicazione tramite la tabella delle costanti. La tabella delle costanti è il nome della tabella dei simboli che definisce il modo in cui le variabili uniformi usate da uno shader si adattano ai registri costanti. I parametri uniformi della funzione vengono visualizzati nella tabella delle costanti preceduti da un segno di dollaro ($), a differenza delle variabili globali. Il simbolo del dollaro è necessario per evitare conflitti di nome tra input uniformi locali e variabili globali con lo stesso nome.

La tabella delle costanti contiene le posizioni dei registri costanti di tutte le variabili uniformi usate dallo shader. La tabella include anche le informazioni sul tipo e il valore predefinito, se specificato.

### <a name="varying-shader-inputs-and-semantics"></a>Variazione di input e semantica di shader

I parametri di input variabili (di una funzione shader di primo livello) devono essere contrassegnati con una parola chiave semantica o uniforme che indica che il valore è costante per l'esecuzione dello shader. Se un input dello shader di primo livello non è contrassegnato con una parola chiave semantica o uniforme, la compilazione dello shader avrà esito negativo.

La semantica di input è un nome usato per collegare l'input specificato a un output della parte precedente della pipeline grafica. Ad esempio, la semantica di input POSITION0 viene usata dai vertex shader per specificare dove devono essere collegati i dati di posizione dal vertex buffer.

I pixel shader e i vertex shader hanno set diversi di semantica di input a causa delle diverse parti della pipeline grafica che si inserire in ogni unità shader. La semantica di input del vertex shader descrive le informazioni per vertice (ad esempio: posizione, normale, coordinate della trama, colore, tangente, binormale e così via) da caricare da un buffer dei vertici in un modulo che può essere utilizzato dal vertex shader. La semantica di input esegue direttamente il mapping all'utilizzo della dichiarazione dei vertici e all'indice di utilizzo.

La semantica di input del pixel shader descrive le informazioni fornite per pixel dall'unità di rasterizzazione. I dati vengono generati interpolando tra gli output del vertex shader per ogni vertice della primitiva corrente. La semantica pixel shader input di base collega le informazioni sul colore di output e sulle coordinate della trama ai parametri di input.

La semantica di input può essere assegnata all'input dello shader tramite due metodi:

-   Aggiunta di due punti e del nome semantico alla dichiarazione del parametro.
-   Definizione di una struttura di input con semantica di input assegnata a ogni membro della struttura.

I vertex shader e i pixel shader forniscono dati di output alla fase successiva della pipeline grafica. La semantica di output viene usata per specificare il modo in cui i dati generati dallo shader devono essere collegati agli input della fase successiva. Ad esempio, la semantica di output per un vertex shader viene usata per collegare gli output degli interpolatori nel rasterizzatore per generare i dati di input per l'pixel shader. Gli pixel shader output sono i valori forniti all'unità di fusione alfa per ognuna delle destinazioni di rendering o il valore di profondità scritto nel buffer di profondità.

La semantica di output del vertex shader viene usata per collegare lo shader sia al pixel shader che alla fase di rasterizzazione. Un vertex shader utilizzato dal rasterizzatore e non esposto al pixel shader deve generare almeno i dati di posizione. I vertex shader che generano dati di coordinate e colori della trama forniscono i dati a un pixel shader al termine dell'interpolazione.

La semantica di output del pixel shader associa i colori di output di un pixel shader alla destinazione di rendering corretta. Il pixel shader di output è collegato alla fase di alpha blend, che determina come vengono modificate le destinazioni di rendering di destinazione. L pixel shader di profondità può essere usato per modificare i valori di profondità di destinazione nella posizione raster corrente. L'output di profondità e più destinazioni di rendering sono supportati solo con alcuni modelli di shader.

La sintassi per la semantica di output è identica alla sintassi per specificare la semantica di input. La semantica può essere specificata direttamente nei parametri dichiarati come parametri "out" o assegnata durante la definizione di una struttura restituita come parametro "out" o come valore restituito di una funzione.

La semantica identifica la origine dei dati. La semantica è un identificatore facoltativo che identifica gli input e gli output dello shader. La semantica viene visualizzata in una delle tre posizioni seguenti:

-   Dopo un membro della struttura.
-   Dopo un argomento nell'elenco di argomenti di input di una funzione.
-   Dopo l'elenco di argomenti di input della funzione.

Questo esempio usa una struttura per fornire uno o più input di vertex shader e un'altra struttura per fornire uno o più output di vertex shader. Ogni membro della struttura usa una semantica.


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



La struttura di input identifica i dati del vertex buffer che fornirà gli input dello shader. Questo shader esegue il mapping dei dati degli elementi position, normal e blendweight del buffer dei vertici nei registri vertex shader. Il tipo di dati di input non deve corrispondere esattamente al tipo di dati della dichiarazione del vertice. Se non corrisponde esattamente, i dati dei vertici verranno convertiti automaticamente nel tipo di dati HLSL quando vengono scritti nei registri shader. Ad esempio, se i dati normali fossero definiti come di tipo UINT dall'applicazione, verrebbero convertiti in float3 quando vengono letti dallo shader.

Se i dati nel flusso dei vertici contengono meno componenti del tipo di dati shader corrispondente, i componenti mancanti verranno inizializzati su 0 (ad eccezione di w, che viene inizializzato su 1).

La semantica di input è simile ai valori in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).

La struttura di output identifica i parametri di output del vertex shader di posizione e colore. Questi output verranno usati dalla pipeline per la rasterizzazione del triangolo (nell'elaborazione primitiva). L'output contrassegnato come dati di posizione indica la posizione di un vertice nello spazio omogeneo. Come minimo, un vertex shader deve generare dati di posizione. La posizione dello spazio dello schermo viene calcolata dopo il completamento del vertex shader dividendo la coordinata (x, y, z) per w. Nello spazio dello schermo , -1 e 1 sono i valori minimo e massimo x e y dei limiti del viewport, mentre z viene usato per il test z-buffer.

La semantica di output è simile ai valori in [**D3DDECLUSAGE.**](/windows/desktop/direct3d9/d3ddeclusage) In generale, una struttura di output per un vertex shader può essere usata anche come struttura di input per un pixel shader, a condizione che il pixel shader non letta da alcuna variabile contrassegnata con la semantica di posizione, dimensione del punto o osa. Questa semantica è associata a valori scalari per vertice che non vengono usati da un pixel shader. Se questi valori sono necessari per il pixel shader, possono essere copiati in un'altra variabile di output che usa una pixel shader semantica.

Le variabili globali vengono assegnate automaticamente ai registri dal compilatore. Le variabili globali sono chiamate anche parametri uniformi perché il contenuto della variabile è lo stesso per tutti i pixel elaborati ogni volta che viene chiamato lo shader. I registri sono contenuti nella tabella delle costanti, che può essere letta usando [**l'interfaccia ID3DXConstantTable.**](/windows/desktop/direct3d9/id3dxconstanttable)

La semantica di input per i pixel shader esegue il mapping dei valori in registri hardware specifici per il trasporto tra vertex shader e pixel shader. Ogni tipo di registro ha proprietà specifiche. Poiché attualmente esistono solo due semantiche per le coordinate di colore e trama, è comune che la maggior parte dei dati sia contrassegnata come coordinata di trama anche quando non lo è.

Si noti che la struttura di output del vertex shader ha usato un input con dati di posizione, che non viene usato dal pixel shader. HLSL consente dati di output validi di un vertex shader che non sono dati di input validi per un pixel shader, purché non vi sia riferimento nel pixel shader.

Gli argomenti di input possono anche essere matrici. La semantica viene incrementata automaticamente dal compilatore per ogni elemento della matrice. Si consideri, ad esempio, la dichiarazione esplicita seguente:


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



La dichiarazione esplicita specificata in precedenza equivale alla dichiarazione seguente che avrà una semantica incrementata automaticamente dal compilatore:


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



Proprio come la semantica di input, la semantica di output identifica l'utilizzo dei pixel shader di output. Molti pixel shader scrivono in un solo colore di output. I pixel shader possono anche scrivere un valore di profondità in una o più destinazioni di rendering contemporaneamente (fino a quattro). Analogamente ai vertex shader, i pixel shader usano una struttura per restituire più di un output. Questo shader scrive 0 nei componenti di colore e nel componente di profondità.


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



I colori di output del pixel shader devono essere di tipo float4. Quando si scrivono più colori, tutti i colori di output devono essere utilizzati in modo contiguo. In altre parole, [COLOR1 non può](dx-graphics-hlsl-semantics.md) essere un output a meno [che COLOR0](dx-graphics-hlsl-semantics.md) non sia già stato scritto. L'output della profondità del pixel shader deve essere di tipo float1.

### <a name="samplers-and-texture-objects"></a>Campionatori e oggetti Texture

Un campionatore contiene lo stato del campionatore. Lo stato del campionatore specifica la trama da campionare e controlla il filtro eseguito durante il campionamento. Per campionare una trama sono necessari tre elementi:

-   Trama
-   Un campionatore (con stato sampler)
-   Istruzione di campionamento

I campionatori possono essere inizializzati con trame e stato del campionatore, come illustrato di seguito:


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



Ecco un esempio del codice per campionare una trama 2D:


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



La trama viene dichiarata con una variabile di trama tex0.

In questo esempio viene dichiarata una variabile sampler denominata s \_ 2D. Il campionatore contiene lo stato del campionatore all'interno delle parentesi graffe. Include la trama che verrà campionata e, facoltativamente, lo stato del filtro, ovvero le modalità di ritorno a capo, le modalità di filtro e così via. Se lo stato del campionatore viene omesso, viene applicato uno stato del campionatore predefinito che specifica un filtro lineare e una modalità di ritorno a capo per le coordinate della trama. La funzione sampler accetta una coordinata di trama a virgola mobile a due componenti e restituisce un colore a due componenti. Viene rappresentato con il tipo restituito float2 e rappresenta i dati nei componenti rosso e verde.

Sono definiti quattro tipi di campionatori (vedere Parole chiave [)](dx-graphics-hlsl-appendix.md)e le ricerche trame vengono eseguite dalle funzioni intrinseche: [**tex1D(s, t) (DirectX HLSL),**](dx-graphics-hlsl-tex1d.md) [**tex2D(s, t) (DirectX HLSL),**](dx-graphics-hlsl-tex2d.md) [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL).**](dx-graphics-hlsl-texcube.md) Ecco un esempio di campionamento 3D:


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



Questa dichiarazione del campionatore usa lo stato del campionatore predefinito per le impostazioni del filtro e la modalità indirizzo.

Ecco l'esempio di campionamento del cubo corrispondente:


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



Infine, ecco l'esempio di campionamento 1D:


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



Poiché il runtime non supporta trame 1D, il compilatore userà una trama 2D con la consapevolezza che la coordinata y non è importante. Poiché [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) viene implementato come ricerca trame 2D, il compilatore è libero di scegliere il componente y in modo efficiente. In alcuni rari scenari, il compilatore non può scegliere un componente y efficiente, nel qual caso verrà generato un avviso.


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



Questo particolare esempio è inefficiente perché il compilatore deve spostare la coordinata di input in un altro registro (perché una ricerca 1D viene implementata come ricerca 2D e la coordinata di trama è dichiarata come float1). Se il codice viene riscritto usando un input float2 anziché float1, il compilatore può usare la coordinata di trama di input perché sa che y viene inizializzato su qualcosa.


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



Tutte le ricerche trame possono essere aggiunte con "bias" o "proj", ovvero [**tex2Dbias (DirectX HLSL),**](dx-graphics-hlsl-tex2dbias.md) [**texCUBEproj (DirectX HLSL).**](dx-graphics-hlsl-texcubeproj.md) Con il suffisso "proj", la coordinata della trama viene divisa per il componente w. Con "bias", il livello mip viene spostato dal componente w. Pertanto, tutte le ricerche trame con un suffisso accettano sempre un input float4. [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) e [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignorano rispettivamente i componenti yz e z.

I campionatori possono essere usati anche nella matrice, anche se nessun back-end supporta attualmente l'accesso dinamico alle matrici dei campionatori. Pertanto, quanto segue è valido perché può essere risolto in fase di compilazione:


```
tex2D(s[0],tex)
```



Questo esempio, tuttavia, non è valido.


```
tex2D(s[a],tex)
```



L'accesso dinamico dei campionatori è utile principalmente per la scrittura di programmi con cicli letterali. Il codice seguente illustra l'accesso alla matrice sampler:


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
> L'uso del runtime di debug Microsoft Direct3D consente di rilevare le mancate corrispondenze tra il numero di componenti in una trama e un campionatore.

 

## <a name="writing-functions"></a>Scrittura di funzioni

Le funzioni suddivideno le attività di grandi dimensioni in attività più piccole. Piccole attività sono più facili da eseguire il debug e possono essere riutilizzate, una volta dimostrate. Le funzioni possono essere usate per nascondere i dettagli di altre funzioni, in modo da semplificare l'esecuzione di un programma composto da funzioni.

Le funzioni HLSL sono simili alle funzioni C in diversi modi: entrambe contengono una definizione e un corpo di funzione ed entrambi dichiarano tipi restituiti ed elenchi di argomenti. Analogamente alle funzioni C, la convalida HLSL esegue il controllo dei tipi per gli argomenti, i tipi di argomento e il valore restituito durante la compilazione dello shader.

A differenza delle funzioni C, le funzioni del punto di ingresso HLSL usano la semantica per associare gli argomenti della funzione agli input e agli output dello shader (le funzioni HLSL chiamate internamente ignorano la semantica). In questo modo è più semplice associare i dati del buffer a uno shader e associare gli output dello shader agli input dello shader.

Una funzione contiene una dichiarazione e un corpo e la dichiarazione deve precedere il corpo.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



La dichiarazione di funzione include tutti gli elementi prima delle parentesi graffe:


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Una dichiarazione di funzione contiene:

-   Tipo restituito
-   Nome di una funzione
-   Elenco di argomenti (facoltativo)
-   Semantica di output (facoltativa)
-   Annotazione (facoltativa)

Il tipo restituito può essere uno qualsiasi dei tipi di dati di base HLSL, ad esempio float4:


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



Il tipo restituito può essere una struttura già definita:


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



Se la funzione non restituisce un valore, è possibile usare void come tipo restituito.


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



Un elenco di argomenti dichiara gli argomenti di input per una funzione. Può anche dichiarare i valori che verranno restituiti. Alcuni argomenti sono sia argomenti di input che di output. Di seguito è riportato un esempio di shader che accetta quattro argomenti di input.


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



Questa funzione restituisce un colore finale, che è una combinazione di un campione di trama e del colore chiaro. La funzione accetta quattro input. Due input hanno semantica: LightDir ha la semantica [TEXCOORD1](dx-graphics-hlsl-semantics.md) e texcrd ha la [semantica TEXCOORD0.](dx-graphics-hlsl-semantics.md) La semantica indica che i dati per queste variabili provengono dal vertex buffer. Anche se la variabile LightDir ha una semantica [TEXCOORD1,](dx-graphics-hlsl-semantics.md) è probabile che il parametro non sia una coordinata di trama. Il tipo semantico TEXCOORDn viene spesso usato per fornire una semantica per un tipo non predefinito (non esiste una semantica di input vertex shader per una direzione di luce).

Gli altri due input LightColor e samp sono etichettati con la [parola chiave uniform.](dx-graphics-hlsl-appendix.md) Si tratta di costanti uniformi che non cambieranno tra le chiamate di disegno. I valori per questi parametri provengono da variabili globali dello shader.

Gli argomenti possono essere etichettati come input con la parola chiave in e gli argomenti di output con la parola chiave out. Gli argomenti non possono essere passati per riferimento. Tuttavia, un argomento può essere sia un input che un output se viene dichiarato con la parola chiave inout. Gli argomenti passati a una funzione contrassegnati con la parola chiave inout vengono considerati copie dell'originale fino a quando la funzione non viene restituita e vengono copiati nuovamente. Di seguito è riportato un esempio di uso di inout:


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

Il corpo dello shader esegue due operazioni: esegue una moltiplicazione di matrice e restituisce un risultato float4. La moltiplicazione della matrice viene eseguita con la [**funzione mul (DirectX HLSL),**](dx-graphics-hlsl-mul.md) che esegue una moltiplicazione di matrice 4x4. **mul (DirectX HLSL)** è detto funzione intrinseca perché è già incorporata nella libreria di funzioni HLSL. Le funzioni intrinseche verranno trattate in modo più dettagliato nella sezione successiva.

La moltiplicazione matrice combina un vettore di input Pos e una matrice composita WorldViewProj. Il risultato è la posizione dei dati trasformati nello spazio dello schermo. Si tratta dell'elaborazione minima di vertex shader che è possibile eseguire. Se si usa la pipeline di funzioni fisse invece di un vertex shader, è possibile disegnare i dati dei vertici dopo aver effettuato questa trasformazione.

L'ultima istruzione nel corpo di una funzione è un'istruzione return. Analogamente a C, questa istruzione restituisce il controllo dalla funzione all'istruzione che ha chiamato la funzione.

I tipi restituiti di funzione possono essere qualsiasi tipo di dati semplice definito in HLSL, inclusi bool, int half, float e double. I tipi restituiti possono essere uno dei tipi di dati complessi, ad esempio vettori e matrici. I tipi HLSL che fanno riferimento a oggetti non possono essere usati come tipi restituiti. Sono inclusi pixelshader, vertexshader, texture e sampler.

Di seguito è riportato un esempio di funzione che usa una struttura per un tipo restituito.


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



Il tipo restituito float4 è stato sostituito con la struttura VS \_ OUTPUT, che ora contiene un singolo membro float4.

Un'istruzione return segnala la fine di una funzione. Si tratta dell'istruzione return più semplice. Restituisce il controllo dalla funzione al programma chiamante. Non restituisce alcun valore.


```
void main()
{
    return ;
}
```



Un'istruzione return può restituire uno o più valori. In questo esempio viene restituito un valore letterale:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



In questo esempio viene restituito il risultato scalare di un'espressione:


```
return  light.enabled;
```



Questo esempio restituisce un valore float4 costruito da una variabile locale e un valore letterale:


```
return  float4(color.rgb, 1) ;
```



Questo esempio restituisce un valore float4 costruito dal risultato restituito da una funzione intrinseca e alcuni valori letterali:


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



Questo esempio restituisce una struttura che contiene uno o più membri:


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

La maggior parte dei vertici e pixel shader hardware è progettata per eseguire uno shader riga per riga, eseguendo ogni istruzione una sola volta. HLSL supporta il controllo di flusso, che include la diramazione statica, le istruzioni predicate, il ciclo statico, la diramazione dinamica e il ciclo dinamico.

In precedenza, l'uso di un'istruzione if generava codice shader in linguaggio assembly che implementava sia il lato if che il lato else del flusso di codice. Di seguito è riportato un esempio di nel codice HLSL compilato per vs \_ 1 \_ 1:


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



Di seguito è riportato il codice assembly risultante:


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



Alcuni componenti hardware consentono il ciclo statico o dinamico, ma la maggior parte richiede l'esecuzione lineare. Nei modelli che non supportano il ciclo, è necessario annullare la registrazione di tutti i cicli. Un esempio è [l'esempio DepthOfField](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) che usa cicli non srotodati anche per shader ps \_ \_ 1 1.

HLSL include ora il supporto per ognuno di questi tipi di controllo di flusso:

-   diramazione statica
-   istruzioni predicate
-   ciclo statico
-   diramazione dinamica
-   ciclo dinamico

La diramazione statica consente di attivare o disattivare i blocchi di codice shader in base a una costante shader booleana. Si tratta di un metodo pratico per abilitare o disabilitare i percorsi del codice in base al tipo di oggetto di cui è in corso il rendering. Tra le chiamate di disegno, è possibile decidere quali funzionalità si vuole supportare con lo shader corrente e quindi impostare i flag booleani necessari per ottenere tale comportamento. Tutte le istruzioni disabilitate da una costante booleana vengono ignorate durante l'esecuzione dello shader.

Il supporto di diramazione più familiare è la diramazione dinamica. Con la diramazione dinamica, la condizione di confronto si trova in una variabile, il che significa che il confronto viene eseguito per ogni vertice o ogni pixel in fase di esecuzione (a differenza del confronto che si verifica in fase di compilazione o tra due chiamate di disegno). L'effetto sulle prestazioni è il costo del ramo più il costo delle istruzioni sul lato del ramo assunto. La diramazione dinamica viene implementata nel modello shader 3 o versione successiva. L'ottimizzazione degli shader che funzionano con questi modelli è simile all'ottimizzazione del codice eseguito in una CPU.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
