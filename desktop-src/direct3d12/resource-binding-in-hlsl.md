---
title: Associazione di risorse in HLSL
description: In questo argomento vengono descritte alcune funzionalità specifiche dell'utilizzo del modello shader HLSL (High Level Shader Language) 5,1 con Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 749fed319f9ffe840f2b06512e337efa28081e24
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548854"
---
# <a name="resource-binding-in-hlsl"></a>Associazione di risorse in HLSL

In questo argomento vengono descritte alcune funzionalità specifiche dell'utilizzo del [modello shader](/windows/desktop/direct3dhlsl/shader-model-5-1) HLSL (High Level Shader Language) 5,1 con Direct3D 12. Tutti i componenti hardware Direct3D 12 supportano il modello di shader 5,1, pertanto il supporto per questo modello non dipende dal livello di funzionalità hardware.

-   [Tipi di risorse e matrici](#resource-types-and-arrays)
-   [Matrici di descrittori e matrici di trama](#descriptor-arrays-and-texture-arrays)
-   [Alias delle risorse](#resource-aliasing)
-   [Divergenze e derivati](#divergence-and-derivatives)
-   [UAV in pixel shader](#uavs-in-pixel-shaders)
-   [Buffer costanti](#constant-buffers)
-   [Modifiche bytecode in SM 5.1](#bytecode-changes-in-sm51)
-   [Dichiarazioni HLSL di esempio](#example-hlsl-declarations)
-   [Argomenti correlati](#related-topics)

## <a name="resource-types-and-arrays"></a>Tipi di risorse e matrici

La sintassi delle risorse del modello shader 5 (SM 5.0) usa la `register` parola chiave per inoltrare informazioni importanti sulla risorsa al compilatore HLSL. Nell'istruzione seguente, ad esempio, viene dichiarata una matrice di quattro trame associata a slot T3, T4, T5 e T6. T3 è l'unico slot di registro presente nell'istruzione, che è semplicemente il primo nella matrice di quattro.

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

La sintassi delle risorse del modello di shader 5,1 (SM 5.1) in HLSL è basata sulla sintassi esistente per le risorse di registro, per semplificare il porting. Le risorse Direct3D 12 in HLSL sono associate a registri virtuali all'interno di spazi di registro logici:

-   t: per le visualizzazioni delle risorse dello shader (SRV)
-   s – per i sampler
-   u: per le visualizzazioni di accesso non ordinato (UAV)
-   b: per le visualizzazioni dei buffer costanti (CBV)

La firma radice che fa riferimento allo shader deve essere compatibile con gli slot di registro dichiarati. Ad esempio, la parte seguente di una firma radice è compatibile con l'uso di slot di trama da T3 a T6, perché descrive una tabella di descrittori con slot T0 tramite T98.

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

Una dichiarazione di risorsa può essere un valore scalare, una matrice 1D o una matrice multidimensionale:

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

SM 5.1 USA gli stessi tipi di risorse e tipi di elemento di SM 5.0. I limiti delle dichiarazioni di SM 5.1 sono più flessibili e vincolati solo dai limiti di runtime o hardware. La `space` parola chiave specifica a quale spazio del registro logico è associato la variabile dichiarata. Se la `space` parola chiave viene omessa, l'indice dello spazio predefinito pari a 0 viene assegnato in modo implicito all'intervallo (pertanto l' `tex2` intervallo sopra riportato si trova in `space0` ). `register(t3,  space0)` non sarà mai in conflitto con `register(t3,  space1)` , né con alcuna matrice in un altro spazio che potrebbe includere T3.

Una risorsa di matrice può avere una dimensione senza limiti, che viene dichiarata specificando la prima dimensione da vuota o 0:

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

La tabella descrittore corrispondente potrebbe essere:

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

Una matrice senza limiti in HLSL non corrisponde a un set di numeri fissi con `numDescriptors` nella tabella descrittore e le dimensioni fisse in HLSL corrispondono a una dichiarazione non associata nella tabella del descrittore.

Sono consentite matrici multidimensionali, incluse le dimensioni non associate. Queste matrici multidimensionali sono bidimensionali nello spazio del registro.

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

L'aliasing degli intervalli di risorse non è consentito. In altre parole, per ogni tipo di risorsa (t, s, u, b), gli intervalli di registro dichiarati non devono sovrapporsi. Che include anche gli intervalli non associati. Gli intervalli dichiarati in diversi spazi di registro non si sovrappongono. Si noti che l'unbounded `tex2` (sopra) risiede in `space0` , mentre unbounded `tex3` risiede in, in `space1` modo che non si sovrappongano.

L'accesso alle risorse dichiarate come matrici è semplice quanto l'indicizzazione.

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

Esiste una restrizione predefinita importante per l'uso degli indici ( `myMaterialID` e `samplerID` nel codice precedente), in quanto non è consentito variare in un' [onda](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology). Anche la modifica dell'indice in base alle istanze viene conteggiata come variabile.

Se è necessario modificare l'indice, specificare il `NonUniformResourceIndex` qualificatore sull'indice, ad esempio:

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

In alcuni componenti hardware l'uso di questo qualificatore genera codice aggiuntivo per applicare la correttezza (inclusi tutti i thread) ma con un minor costo in termini di prestazioni. Se un indice viene modificato senza questo qualificatore e all'interno di un'operazione di estrazione/invio, i risultati non sono definiti.

## <a name="descriptor-arrays-and-texture-arrays"></a>Matrici di descrittori e matrici di trama

Le matrici di trame sono disponibili da DirectX 10. Le matrici di trama richiedono un descrittore, tuttavia tutte le sezioni di matrici devono condividere lo stesso formato, larghezza, altezza e numero di MIP. Inoltre, la matrice deve occupare un intervallo contiguo nello spazio degli indirizzi virtuali. Il codice seguente illustra un esempio di accesso a una matrice di trame da uno shader.

``` syntax
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

In una matrice di trame, l'indice può variare liberamente, senza alcuna necessità di qualificatori, ad esempio `NonUniformResourceIndex` .

La matrice di descrittori equivalente sarà:

``` syntax
Texture2D<float4> myTex2DArray[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

Si noti che l'uso imbarazzante di un valore float per l'indice della matrice viene sostituito con `myTex2D[2]` . Inoltre, le matrici di descrittori offrono maggiore flessibilità con le dimensioni. Il tipo, `Texture2D` è questo esempio, non può variare, ma il formato, la larghezza, l'altezza e il conteggio MIP possono variare a seconda di ogni descrittore.

È legittimo avere una matrice di descrittori di matrici di trame:

``` syntax
Texture2DArray<float4> myTex2DArrayOfArrays[2] : register(t0);
```

Non è lecito dichiarare una matrice di strutture, ogni struttura contenente descrittori, ad esempio il codice seguente non è supportata.

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

Questa operazione avrebbe consentito il layout della memoria **abcabcabc...**, ma è una limitazione del linguaggio e non è supportata. Un metodo supportato per eseguire questa operazione è il seguente, anche se il layout della memoria in questo caso è **AAA... BBB... CCC...**

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

Per ottenere il layout di **abcabcabc...** Memory, utilizzare una tabella descrittore senza utilizzare la `myStruct` struttura.

## <a name="resource-aliasing"></a>Alias delle risorse

Gli intervalli di risorse specificati negli shader HLSL sono intervalli logici. Sono associate a intervalli di heap concreti in fase di esecuzione tramite il meccanismo di firma radice. In genere, un intervallo logico viene mappato a un intervallo di heap che non si sovrappone ad altri intervalli di heap. Tuttavia, il meccanismo di firma radice rende possibile l'alias (sovrapposizione) degli intervalli di heap dei tipi compatibili. È ad esempio `tex2` possibile `tex3` eseguire il mapping degli intervalli di e dall'esempio precedente allo stesso intervallo di heap (o sovrapposto), che ha l'effetto di eseguire l'aliasing delle trame nel programma HLSL. Se si desidera questo tipo di alias, lo shader deve essere compilato con \_ \_ l'opzione alias delle risorse di D3D10 shader \_ \_ , impostata tramite l'opzione *alias/res \_ May \_* per lo [strumento compilatore di effetti](/windows/desktop/direct3dtools/fxc) (FXC). L'opzione fa sì che il compilatore produca codice corretto impedendo determinate ottimizzazioni di carico/archivio nel presupposto che le risorse possano essere alias.

## <a name="divergence-and-derivatives"></a>Divergenze e derivati

SM 5.1 non impone limitazioni per l'indice delle risorse. ovvero, ` tex2[idx].Sample(…)` -l'indice IDX può essere una costante letterale, una costante cbuffer o un valore interpolato. Sebbene il modello di programmazione fornisca una grande flessibilità, è necessario tenere presenti i problemi seguenti:

-   Se l'indice è diverso da un quad, le quantità derivate e derivate calcolate dall'hardware, ad esempio LOD, potrebbero non essere definite. Il compilatore HLSL esegue il massimo sforzo per emettere un avviso in questo caso, ma non impedisce la compilazione di uno shader. Questo comportamento è simile all'elaborazione di derivati in un flusso di controllo divergente.
-   Se l'indice di risorsa è divergente, le prestazioni vengono diminuite rispetto al caso di un indice uniforme, perché l'hardware deve eseguire operazioni su diverse risorse. Gli indici di risorse che possono essere divergenti devono essere contrassegnati con la `NonUniformResourceIndex` funzione nel codice HLSL. In caso contrario, i risultati non sono definiti.

## <a name="uavs-in-pixel-shaders"></a>UAV in pixel shader

SM 5.1 non impone vincoli sugli intervalli di UAV nei pixel shader come nel caso di SM 5.0.

## <a name="constant-buffers"></a>Buffer costanti

La sintassi di SM 5.1 Constant buffers (cbuffer) è cambiata da SM 5.0 per consentire agli sviluppatori di indicizzare i buffer costanti. Per abilitare i buffer di costanti indicizzabili, in SM 5.1 è stato introdotto il `ConstantBuffer` costrutto "template":

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

Il codice precedente dichiara la variabile del buffer costante `myCB1` di tipo `Foo` e dimensione 6 e una variabile di buffer costante scalare `myCB2` . È ora possibile indicizzare una variabile di buffer costante nello shader come segue:

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

I campi ' a' è b ' non diventano variabili globali, bensì devono essere considerati come campi. Per compatibilità con le versioni precedenti, SM 5.1 supporta il vecchio concetto di cbuffer per cBuffers scalare. L'istruzione seguente rende le variabili globali di sola lettura ' a' è b ' come in SM 5.0. Non è tuttavia possibile indicizzare un cbuffer di questo tipo obsoleto.

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

Attualmente, il compilatore shader supporta il `ConstantBuffer` modello solo per le strutture definite dall'utente.

Per motivi di compatibilità, il compilatore HLSL può assegnare automaticamente i registri delle risorse per gli intervalli dichiarati in `space0` . Se ' Space ' viene omesso nella clausola Register, viene usato il valore predefinito `space0` . Il compilatore usa l'euristica per il primo foro per assegnare i registri. L'assegnazione può essere recuperata tramite l'API di reflection, che è stata estesa per aggiungere il campo *spazio* per lo spazio, mentre il campo *BindPoint* indica il limite inferiore dell'intervallo di registro delle risorse.

## <a name="bytecode-changes-in-sm51"></a>Modifiche bytecode in SM 5.1

SM 5.1 modifica il modo in cui i registri delle risorse vengono dichiarati e viene fatto riferimento nelle istruzioni. La sintassi prevede la dichiarazione di una "variabile" del registro, in modo analogo al modo in cui viene eseguita per i registri di memoria condivisa del gruppo:

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

Questa operazione verrà disassemblata in:

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots are used.
```

Ogni intervallo di risorse shader dispone ora di un ID (un nome) univoco per il bytecode dello shader. Ad esempio, Tex1 (T10) texture array diventa ' T'1' nel bytecode dello shader. L'assegnazione di ID univoci a ogni intervallo di risorse consente due elementi:

-   Identificare in modo univoco l'intervallo di risorse (vedere \_ la pagina relativa \_ all'indicizzazione della risorsa DCL Texture2D) in un'istruzione (vedere l'istruzione di esempio).
-   Associazione di un set di attributi alla dichiarazione, ad esempio il tipo di elemento, le dimensioni stride, la modalità operativa raster e così via.

Si noti che l'ID dell'intervallo non è correlato alla dichiarazione di limite inferiore HLSL.

L'ordine delle associazioni di risorse di Reflection (elenco all'inizio) e le istruzioni per la dichiarazione dello shader (DCL \_ \* ) sono le stesse per facilitare l'identificazione della corrispondenza tra le variabili HLSL e gli ID bytecode.

Ogni istruzione di dichiarazione in SM 5.1 utilizza un operando 3D per definire: ID intervallo, limiti inferiori e superiori. Viene emesso un token aggiuntivo per specificare lo spazio del registro. È possibile che vengano generati anche altri token per fornire proprietà aggiuntive dell'intervallo, ad esempio cbuffer o l'istruzione di dichiarazione del buffer strutturato genera la dimensione di cbuffer o della struttura. I dettagli esatti della codifica sono disponibili in d3d12TokenizedProgramFormat. h e **D3D10ShaderBinary:: CShaderCodeParser**.

Le istruzioni di SM 5.1 non emetteranno Informazioni aggiuntive sull'operando delle risorse come parte dell'istruzione (ad esempio, SM 5.0). Queste informazioni sono ora incluse nelle istruzioni di dichiarazione. In SM 5.0, le istruzioni per l'indicizzazione delle risorse gli attributi delle risorse devono essere descritte in token opcode estesi, perché l'indicizzazione ha offuscato l'associazione alla dichiarazione. In SM 5.1 ogni ID (ad esempio,' t 1') viene associato in modo non ambiguo a una singola dichiarazione che descrive le informazioni necessarie sulle risorse. Pertanto, i token opcode estesi usati sulle istruzioni per descrivere le informazioni sulle risorse non vengono più generati.

Nelle istruzioni di non dichiarazione, un operando di risorsa per Samplers, SRVs e UAV è un operando 2D. Il primo indice è una costante letterale che specifica l'ID intervallo. Il secondo indice rappresenta il valore linearizzato dell'indice. Il valore viene calcolato in relazione all'inizio dello spazio di registro corrispondente (non relativo all'inizio dell'intervallo logico) per una migliore correlazione con la firma radice e per ridurre il carico del compilatore del driver per la modifica dell'indice.

Un operando di risorsa per CBVs è un operando 3D, che contiene l'ID letterale dell'intervallo, l'indice del buffer costante e l'offset nell'istanza specifica del buffer costante.

## <a name="example-hlsl-declarations"></a>Dichiarazioni HLSL di esempio

I programmi HLSL non devono conoscere alcuna firma radice. Possono assegnare associazioni allo spazio di binding "Register" virtuale, t \# per SRVs, u \# per UAV, b \# per CBVs, s per i \# Samplers, oppure affidarsi al compilatore per selezionare le assegnazioni (ed eseguire query sui mapping risultanti utilizzando la reflection dello shader in seguito). La firma radice esegue il mapping delle tabelle descrittore, dei descrittori radice e delle costanti radice allo spazio di registro virtuale.

Di seguito sono riportate alcune dichiarazioni di esempio che possono essere disponibili in HLSL shader. Si noti che non sono presenti riferimenti a firme radice o tabelle descrittori.

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzazione dinamica con HLSL 5,1](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[Effect-strumento compilatore](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[Funzionalità del modello HLSL shader 5,1 per Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Visualizzazioni ordinate del rasterizzatore](rasterizer-order-views.md)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> <dt>

[Firme radice](root-signatures.md)
</dt> <dt>

[Modello Shader 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md)
</dt> <dt>

[Specifica delle firme radice in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 