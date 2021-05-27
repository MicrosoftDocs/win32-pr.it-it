---
title: Associazione di risorse in HLSL
description: Questo argomento descrive alcune funzionalità specifiche dell'uso del modello di shader HLSL (High Level Shader Language) 5.1 con Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 711ccdee71ff916445be68d03b84b7621aa04cf3
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550386"
---
# <a name="resource-binding-in-hlsl"></a>Associazione di risorse in HLSL

Questo argomento descrive alcune funzionalità specifiche dell'uso del modello di shader HLSL (High Level Shader Language) [5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) con Direct3D 12. Tutto l'hardware Direct3D 12 supporta il modello shader 5.1, quindi il supporto per questo modello non dipende dal livello di funzionalità hardware.

## <a name="resource-types-and-arrays"></a>Tipi di risorse e matrici

La sintassi delle risorse del modello shader 5 (SM5.0) usa la parola chiave per inoltrare informazioni importanti sulla risorsa `register` al compilatore HLSL. Ad esempio, l'istruzione seguente dichiara una matrice di quattro trame associate in corrispondenza degli slot t3, t4, t5 e t6. t3 è l'unico slot di registro visualizzato nell'istruzione , semplicemente il primo nella matrice di quattro.

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

La sintassi delle risorse del modello shader 5.1 (SM5.1) in HLSL si basa sulla sintassi esistente delle risorse di registro, per semplificare la portabilità. Le risorse Direct3D 12 in HLSL sono associate a registri virtuali all'interno di spazi dei registri logici:

-   t: per le visualizzazioni delle risorse shader (SRV)
-   s: per i campionatori
-   u: per le viste di accesso non ordinate (UAV)
-   b : per le visualizzazioni buffer costanti (CBV)

La firma radice che fa riferimento allo shader deve essere compatibile con gli slot di registro dichiarati. Ad esempio, la parte seguente di una firma radice sarebbe compatibile con l'uso di slot di trama da t3 a t6, in quanto descrive una tabella di descrittori con slot da t0 a t98.

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

Una dichiarazione di risorsa può essere scalare, matrice 1D o matrice multidimensionale:

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

SM5.1 usa gli stessi tipi di risorsa e tipi di elemento di SM5.0. I limiti delle dichiarazioni SM5.1 sono più flessibili e vincolati solo dai limiti di runtime/hardware. La `space` parola chiave specifica a quale spazio del registro logico è associata la variabile dichiarata. Se la parola chiave viene omessa, l'indice di spazio predefinito 0 viene assegnato in modo implicito all'intervallo , quindi l'intervallo precedente `space` `tex2` risiede in `space0` . `register(t3,  space0)` non sarà mai in conflitto con `register(t3,  space1)` , né con una matrice in un altro spazio che potrebbe includere t3.

Una risorsa matrice può avere una dimensione non associata, che viene dichiarata specificando la prima dimensione vuota oppure 0:

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

La tabella del descrittore corrispondente potrebbe essere:

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

Una matrice non associata in HLSL corrisponde a un numero fisso impostato con nella tabella del descrittore e una dimensione fissa in HLSL corrisponde a una dichiarazione non associata nella tabella del `numDescriptors` descrittore.

Sono consentite matrici multidimensionali, inclusa una dimensione non associata. Queste matrici multidimensionali vengono appiattite nello spazio del registro.

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

L'aliasing degli intervalli di risorse non è consentito. In altre parole, per ogni tipo di risorsa (t, s, u, b), gli intervalli di registri dichiarati non devono sovrapporsi. Sono inclusi anche gli intervalli non associati. Gli intervalli dichiarati in spazi di registro diversi non si sovrappongono mai. Si noti che unbounded (sopra) si trova in , mentre unbounded risiede in , in modo che non `tex2` `space0` si `tex3` `space1` sovrappongano.

L'accesso alle risorse dichiarate come matrici è semplice quanto l'indicizzazione.

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

Esiste un'importante restrizione predefinita per l'uso degli indici ( e nel codice precedente) in quanto non è consentito variare `myMaterialID` `samplerID` all'interno di [un'onda](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology). Anche la modifica dell'indice in base al numero di istanze varia.

Se è necessario variare l'indice, specificare il `NonUniformResourceIndex` qualificatore nell'indice, ad esempio:

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

In alcuni hardware l'uso di questo qualificatore genera codice aggiuntivo per applicare la correttezza (incluso tra i thread), ma a un costo delle prestazioni minore. Se un indice viene modificato senza questo qualificatore e all'interno di un oggetto draw/dispatch i risultati non sono definiti.

## <a name="descriptor-arrays-and-texture-arrays"></a>Matrici di descrittori e matrici di trame

Le matrici di trame sono disponibili a partire da DirectX 10. Le matrici di trame richiedono un descrittore, tuttavia tutte le sezioni della matrice devono condividere lo stesso formato, larghezza, altezza e conteggio mip. Inoltre, la matrice deve occupare un intervallo contiguo nello spazio degli indirizzi virtuali. Il codice seguente illustra un esempio di accesso a una matrice di trame da uno shader.

``` syntax
Texture2DArray<float4> myTex2DArray : register(t0); // t0
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

In una matrice di trame, l'indice può essere variato liberamente, senza la necessità di qualificatori come `NonUniformResourceIndex` .

La matrice di descrittori equivalente sarà:

``` syntax
Texture2D<float4> myArrayOfTex2D[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myArrayOfTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

Si noti che l'uso difficile di un float per l'indice di matrice viene sostituito con `myArrayOfTex2D[2]` . Inoltre, le matrici di descrittori offrono maggiore flessibilità con le dimensioni. Il tipo, in questo esempio, non può variare, ma il formato, la larghezza, l'altezza e il numero mip possono variare `Texture2D` tutti con ogni descrittore.

È legittimo avere una matrice di descrittori di matrici di trame:

``` syntax
Texture2DArray<float4> myArrayOfTex2DArrays[2] : register(t0);
```

Non è legittimo dichiarare una matrice di strutture, ogni struttura contenente descrittori, ad esempio il codice seguente non è supportata.

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

Ciò avrebbe consentito il layout di memoria **abcabcabc....**, ma è una limitazione del linguaggio e non è supportato. Un metodo supportato per eseguire questa operazione è il seguente, anche se il layout di memoria in questo caso **è aaa... Bbb... ccc...**.

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

Per ottenere il layout di memoria **abcabcabc....,** usare una tabella di descrizione senza usare la `myStruct` struttura .

## <a name="resource-aliasing"></a>Alias delle risorse

Gli intervalli di risorse specificati negli shader HLSL sono intervalli logici. Sono associati a intervalli di heap concreti in fase di esecuzione tramite il meccanismo di firma radice. In genere, un intervallo logico viene mappato a un intervallo di heap che non si sovrappone ad altri intervalli di heap. Tuttavia, il meccanismo di firma radice consente di creare un alias (sovrapposizione) di intervalli di heap di tipi compatibili. Ad esempio, gli intervalli e dell'esempio precedente possono essere mappati allo stesso intervallo heap (o sovrapposto), che ha l'effetto dell'aliasing delle trame nel programma `tex2` `tex3` HLSL. Se si desidera questo alias, lo shader deve essere compilato con l'opzione ALIAS MAY DELLE RISORSE SHADER D3D10, che viene impostata usando l'opzione \_ \_ \_ \_ */res \_ may \_ alias* per [lo strumento Effect-Compiler Tool](../direct3dtools/fxc.md) (FXC). L'opzione fa in modo che il compilatore produca codice corretto impedendo determinate ottimizzazioni di caricamento/archiviazione in base al presupposto che le risorse possano creare un alias.

## <a name="divergence-and-derivatives"></a>Divergenza e derivati

SM5.1 non impone limitazioni all'indice delle risorse. ad esempio, l'idx dell'indice può essere una costante ` tex2[idx].Sample(…)` letterale, una costante cbuffer o un valore interpolato. Anche se il modello di programmazione offre una tale flessibilità, esistono problemi da tenere presenti:

-   Se l'indice diverge in un quad, le quantità derivate e derivate calcolate dall'hardware, ad esempio loD, potrebbero non essere definite. Il compilatore HLSL fa il massimo sforzo per emettere un avviso in questo caso, ma non impedisce la compilazione di uno shader. Questo comportamento è simile al calcolo di derivati nel flusso di controllo divergente.
-   Se l'indice delle risorse è divergente, le prestazioni diminuiscono rispetto al caso di un indice uniforme, perché l'hardware deve eseguire operazioni su più risorse. Gli indici delle risorse che possono essere divergenti devono essere contrassegnati con la `NonUniformResourceIndex` funzione nel codice HLSL. In caso contrario, i risultati non sono definiti.

## <a name="uavs-in-pixel-shaders"></a>UAV nei pixel shader

SM5.1 non impone vincoli agli intervalli UAV nei pixel shader, come nel caso di SM5.0.

## <a name="constant-buffers"></a>Buffer costanti

La sintassi dei buffer costanti SM5.1 (cbuffer) è stata modificata da SM5.0 per consentire agli sviluppatori di indicizzare i buffer costanti. Per abilitare i buffer costanti indicizzabili, SM5.1 introduce il `ConstantBuffer` costrutto "modello":

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

Il codice precedente dichiara una variabile di buffer costante di tipo `myCB1` e `Foo` dimensioni 6 e una variabile di buffer costante `myCB2` scalare. Una variabile di buffer costante può ora essere indicizzata nello shader come:

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

I campi 'a' e 'b' non diventano variabili globali, ma devono essere trattati come campi. Per la compatibilità con le versioni precedenti, SM5.1 supporta il concetto di cbuffer precedente per i cbuffer scalari. L'istruzione seguente rende "a" e "b" variabili globali di sola lettura come in SM5.0. Tuttavia, un cbuffer di tipo precedente non può essere indicizzabile.

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

Attualmente, il compilatore shader supporta il modello solo per le `ConstantBuffer` strutture definite dall'utente.

Per motivi di compatibilità, il compilatore HLSL può assegnare automaticamente registri di risorse per gli intervalli dichiarati in `space0` . Se 'space' viene omesso nella clausola register, viene usato il `space0` valore predefinito. Il compilatore usa l'euristica first-hole-fits per assegnare i registri. L'assegnazione può essere recuperata tramite l'API reflection, che è stata estesa per aggiungere il campo *Spazio* per lo spazio, mentre il campo *BindPoint* indica il limite inferiore dell'intervallo del registro delle risorse.

## <a name="bytecode-changes-in-sm51"></a>Modifiche al bytecode in SM5.1

SM5.1 modifica il modo in cui i registri delle risorse vengono dichiarati e a cui si fa riferimento nelle istruzioni . La sintassi prevede la dichiarazione di un registro "variabile", simile a come viene eseguita per i registri di memoria condivisa di gruppo:

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

Verrà disassemblato in:

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

Ogni intervallo di risorse shader ha ora un ID (un nome) univoco per il bytecode dello shader. Ad esempio, la matrice di trame tex1 (t10) diventa 'T1' nel bytecode dello shader. L'impostazione di ID univoci per ogni intervallo di risorse consente due operazioni:

-   Identificare in modo univoco l'intervallo di risorse (vedere dcl \_ resource texture2d) indicizzato in un'istruzione \_ (vedere l'istruzione di esempio).
-   Associazione di un set di attributi alla dichiarazione, ad esempio tipo di elemento, dimensioni stride, modalità di funzionamento raster e così via.

Si noti che l'ID dell'intervallo non è correlato alla dichiarazione del limite inferiore HLSL.

L'ordine delle associazioni di risorse di reflection (elencate nella parte superiore) e delle istruzioni di dichiarazione dello shader (dcl ) è lo stesso per facilitare l'identificazione della corrispondenza tra le variabili HLSL e gli ID \_ \* bytecode.

Ogni istruzione di dichiarazione in SM5.1 usa un operando 3D per definire: ID intervallo, limiti inferiore e superiore. Viene generato un token aggiuntivo per specificare lo spazio del registro. È possibile generare anche altri token per trasmettere proprietà aggiuntive dell'intervallo, ad esempio l'istruzione cbuffer o la dichiarazione del buffer strutturato genera le dimensioni del cbuffer o della struttura. I dettagli esatti della codifica sono disponibili in d3d12TokenizedProgramFormat.h e **D3D10ShaderBinary::CShaderCodeParser**.

Le istruzioni SM5.1 non generano informazioni aggiuntive sull'operando di risorsa come parte dell'istruzione (come in SM5.0). Queste informazioni sono ora disponibili nelle istruzioni di dichiarazione. In SM5.0 le istruzioni per l'indicizzazione delle risorse richiedevano la descrizione degli attributi delle risorse nei token del codice operativo estesi, poiché l'indicizzazione offuscava l'associazione alla dichiarazione. In SM5.1 ogni ID (ad esempio 't1') è associato in modo non ambiguo a una singola dichiarazione che descrive le informazioni sulle risorse necessarie. Di conseguenza, i token opcode estesi usati nelle istruzioni per descrivere le informazioni sulle risorse non vengono più generati.

Nelle istruzioni non di dichiarazione, un operando di risorsa per campionatori, SPV e UAV è un operando 2D. Il primo indice è una costante letterale che specifica l'ID intervallo. Il secondo indice rappresenta il valore linearizzato dell'indice. Il valore viene calcolato in relazione all'inizio dello spazio del registro corrispondente (non rispetto all'inizio dell'intervallo logico) per correlare meglio con la firma radice e ridurre il carico di lavoro del compilatore del driver di regolazione dell'indice.

Un operando di risorsa per CBV è un operando 3D, contenente: ID letterale dell'intervallo, indice del buffer costante, offset nell'istanza specifica del buffer costante.

## <a name="example-hlsl-declarations"></a>Dichiarazioni HLSL di esempio

I programmi HLSL non devono conoscere le firme radice. Possono assegnare associazioni allo spazio di associazione "register" virtuale, t per IVS, u per UAV, b per \# CV, s per i campionatori o affidarsi al compilatore per selezionare le assegnazioni (ed eseguire query sui mapping risultanti usando la reflection dello shader in un secondo \# \# \# momento). La firma radice esegue il mapping di tabelle descrittori, descrittori radice e costanti radice a questo spazio del registro virtuale.

Di seguito sono riportate alcune dichiarazioni di esempio che possono essere presenti in uno shader HLSL. Si noti che non sono presenti riferimenti alle firme radice o alle tabelle dei descrittori.

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

* [Indicizzazione dinamica con HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
* [Strumento compilatore effetti](../direct3dtools/fxc.md)
* [Funzionalità del modello di shader HLSL 5.1 per Direct3D 12](../direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12.md)
* [Visualizzazioni ordinate del rasterizzatore](rasterizer-order-views.md)
* [Associazione di risorse](resource-binding.md)
* [Firme radice](root-signatures.md)
* [Modello shader 5.1](../direct3dhlsl/shader-model-5-1.md)
* [Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md)
* [Specifica delle firme radice in HLSL](specifying-root-signatures-in-hlsl.md)