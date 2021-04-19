---
title: Specifica delle firme radice in HLSL
description: Specificare le firme radice nel modello di shader HLSL 5.1 è un'alternativa a specificarle nel codice C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad0da9f84d68fc1acbf53332d1cae4075f0faa
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492283"
---
# <a name="specifying-root-signatures-in-hlsl"></a>Specifica delle firme radice in HLSL

Specificare le firme radice nel modello di shader HLSL 5.1 è un'alternativa a specificarle nel codice C++.

-   [Esempio di firma radice HLSL](#an-example-hlsl-root-signature)
    -   [Firma radice versione 1.0](#root-signature-version-10)
    -   [Firma radice versione 1.1](#root-signature-version-11)
-   [Flag radice](#rootflags)
-   [Costanti radice](#root-constants)
-   [Visibilità](#visibility)
-   [CBV a livello di radice](#root-level-cbv)
-   [SRV a livello di radice](#root-level-srv)
-   [UAV a livello di radice](#root-level-uav)
-   [Tabella dei descrittori](#descriptor-table)
-   [Campionatore statico](#static-sampler)
-   [Compilazione di una firma radice HLSL](#compiling-an-hlsl-root-signature)
-   [Modifica delle firme radice con il compilatore FXC](#manipulating-root-signatures-with-the-fxc-compiler)
-   [Note](#notes)
-   [Argomenti correlati](#related-topics)

## <a name="an-example-hlsl-root-signature"></a>Esempio di firma radice HLSL

Una firma radice può essere specificata in HLSL come stringa. La stringa contiene una raccolta di clausole delimitati da virgole che descrivono i componenti costitutivi della firma radice. La firma radice deve essere identica tra gli shader per qualsiasi oggetto di stato della pipeline (PSO). Ecco un esempio:

### <a name="root-signature-version-10"></a>Firma radice versione 1.0

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

Questa definizione darebbe la firma radice seguente, notando:

-   Uso dei parametri predefiniti.
-   b0 e (b0, space=1) non sono in conflitto
-   u0 è visibile solo allo shader geometry
-   Gli alias u4 e u5 sono alias dello stesso descrittore in un heap

![una firma radice specificata usando il linguaggio shader di alto livello](images/hlsl-root-signature.png)

### <a name="root-signature-version-11"></a>Firma radice versione 1.1

[La versione 1.1 della firma radice](root-signature-version-1-1.md) abilita le ottimizzazioni dei driver per i descrittori e i dati della firma radice.

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

Il linguaggio di firma radice HLSL corrisponde strettamente alle API di firma radice C++ e ha una potenza espressiva equivalente. La firma radice viene specificata come sequenza di clausole, separate da virgola. L'ordine delle clausole è importante, in quanto l'ordine di analisi determina la posizione dello slot nella firma radice. Ogni clausola accetta uno o più parametri denominati. L'ordine dei parametri, tuttavia, non è importante.

## <a name="rootflags"></a>RootFlags

La *clausola RootFlags* facoltativa accetta 0 (il valore predefinito per indicare nessun flag) o uno o più valori di flag radice predefiniti, connessi tramite l'operatore OR ' \| '. I valori dei flag radice consentiti sono definiti da [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

Ad esempio:

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a>Costanti radice

La *clausola RootConstants* specifica le costanti radice nella firma radice. Due parametri obbligatori sono: *num32BitConstants* e *bReg* (il registro corrispondente a *BaseShaderRegister* nelle API C++) di *cbuffer*. I parametri space (*RegisterSpace* nelle API C++) e visibility (*ShaderVisibility* in C++) sono facoltativi e i valori predefiniti sono:

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

Ad esempio:

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a>Visibilità

Visibility è un parametro facoltativo che può avere uno dei valori di [**D3D12 \_ SHADER \_ VISIBILITY.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)

SHADER \_ VISIBILITY ALL trasmette gli argomenti radice a tutti gli \_ shader. In alcuni hardware questa operazione non ha alcun costo, ma su altri componenti hardware è necessario creare una fork dei dati in tutte le fasi dello shader. L'impostazione di una delle opzioni, ad esempio SHADER \_ VISIBILITY \_ VERTEX, limita l'argomento radice a una singola fase dello shader.

L'impostazione degli argomenti radice nelle fasi di uno shader singolo consente di usare lo stesso nome di associazione in fasi diverse. Ad esempio, un'associazione SRV di `t0,SHADER_VISIBILITY_VERTEX` e l'associazione SRV `t0,SHADER_VISIBILITY_PIXEL` di sarebbero valide. Tuttavia, se l'impostazione di visibilità fosse per una `t0,SHADER_VISIBILITY_ALL` delle associazioni, la firma radice non sarebbe valida.

## <a name="root-level-cbv"></a>CBV a livello di radice

La `CBV` clausola (visualizzazione buffer costante) specifica una voce Reg di buffer b-register costante a livello radice. Si noti che si tratta di una voce scalare. Non è possibile specificare un intervallo per il livello radice.

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a>SRV a livello di radice

La `SRV` clausola (visualizzazione delle risorse shader) specifica una voce reg T-register SRV a livello di radice. Si noti che si tratta di una voce scalare. Non è possibile specificare un intervallo per il livello radice.

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a>UAV a livello di radice

La `UAV` clausola (visualizzazione di accesso non ordinato) specifica una voce reg UAV u-register a livello di radice. Si noti che si tratta di una voce scalare. Non è possibile specificare un intervallo per il livello radice.

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Ad esempio:

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a>Tabella dei descrittori

La clausola è di per sé un elenco di clausole della tabella dei descrittori delimitati da virgole, nonché un `DescriptorTable` parametro di visibilità facoltativo. Le *clausole DescriptorTable* includono CBV, SRV, UAV e Sampler. Si noti che i parametri sono diversi da quelli delle clausole a livello di radice.

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

La tabella del descrittore `CBV` ha la sintassi seguente:

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Ad esempio:

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

Il parametro *obbligatorio bReg* specifica il reg iniziale dell'intervallo cbuffer. Il *parametro numDescriptors* specifica il numero di descrittori nell'intervallo cbuffer contiguo. il valore predefinito è 1. La voce dichiara un intervallo cbuffer ` [Reg, Reg + numDescriptors - 1]` , quando *numDescriptors* è un numero. Se *numDescriptors* è uguale a "unbounded", l'intervallo è , il che significa che l'app deve assicurarsi che non faccia riferimento a un'area non `[Reg, UINT_MAX]` in limiti. Il *campo offset* rappresenta il parametro *OffsetInDescriptorsFromTableStart* nelle API C++, ovvero l'offset (in descrittori) dall'inizio della tabella. Se l'offset è impostato su DESCRIPTOR RANGE OFFSET APPEND (impostazione predefinita), significa che l'intervallo è \_ \_ direttamente successivo \_ all'intervallo precedente. Tuttavia, l'immissione di offset specifici consente la sovrapposizione degli intervalli, consentendo l'alias del registro.

La tabella del descrittore `SRV` ha la sintassi seguente:

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

È simile alla voce della tabella del `CBV` descrittore, ma l'intervallo specificato è per le visualizzazioni delle risorse shader.

La tabella del descrittore `UAV` ha la sintassi seguente:

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

È simile alla voce della tabella del `CBV` descrittore, ma l'intervallo specificato è per le viste di accesso non ordinate.

La tabella dei descrittori `Sampler` ha la sintassi seguente:

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

È simile alla voce della tabella del `CBV` descrittore, ma l'intervallo specificato è per i campionatori shader. Si noti che i campionatori non possono essere misti con altri tipi di descrittori nella stessa tabella dei descrittori(poiché si tratta di un heap descrittore separato).

## <a name="static-sampler"></a>Campionatore statico

Il campionatore statico rappresenta la [**struttura DESC D3D12 \_ STATIC \_ SAMPLER. \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) Il parametro obbligatorio per *StaticSampler* è un reg scalare, sampler s-register. Altri parametri sono facoltativi con i valori predefiniti illustrati di seguito. La maggior parte dei campi accetta un set di enumerazioni predefinite.

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

Ad esempio:

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

Le opzioni dei parametri sono molto simili alle chiamate API C++, ad eccezione di *borderColor*, che è limitato a un'enumerazione in HLSL.

Il campo del filtro può essere uno di [**D3D12 \_ FILTER.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)

I campi dell'indirizzo possono essere ognuno di [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).

La funzione di confronto può essere una di [**D3D12 \_ COMPARISON \_ FUNC.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)

Il campo del colore del bordo può essere uno di [**D3D12 \_ STATIC \_ BORDER \_ COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).

La visibilità può essere una [**di D3D12 \_ SHADER \_ VISIBILITY.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)

## <a name="compiling-an-hlsl-root-signature"></a>Compilazione di una firma radice HLSL

Esistono due meccanismi per compilare una firma radice HLSL. In primo luogo, è possibile associare una stringa di firma radice a un particolare shader tramite l'attributo *RootSignature* (nell'esempio seguente, usando il punto di ingresso **MyRS1):**

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

Il compilatore creerà e verificherà il BLOB della firma radice per lo shader e lo incorpora insieme al codice byte dello shader nel BLOB shader. Il compilatore supporta la sintassi della firma radice per il modello shader 5.0 e versioni successive. Se una firma radice è incorporata in uno shader del modello di shader 5.0 e tale shader viene inviato al runtime D3D11, a differenza di D3D12, la parte della firma radice verrà automaticamente ignorata da D3D11.

L'altro meccanismo è creare un BLOB di firma radice autonomo, ad esempio per riutilizzarlo con un set di shader di grandi dimensioni, risparmiando spazio. [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) supporta i modelli di shader **rootsig \_ 1 \_ 0** e **rootsig \_ \_ 1 1.** Il nome della stringa di definizione viene specificato tramite il consueto argomento /E. Ad esempio:

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

Si noti che la stringa di firma radice definita può essere passata anche nella riga di comando, ad esempio /D MyRS1="...".

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a>Modifica delle firme radice con il compilatore FXC

Il compilatore FXC crea il byte-code dello shader dai file di origine HLSL. Esistono molti parametri facoltativi per questo compilatore. Fare riferimento a [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).

Per la gestione delle firme radice di HLSL, la tabella seguente fornisce alcuni esempi di uso di FXC.



| Linea | Riga di comando                                                                 | Descrizione                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | Compila uno shader per la destinazione pixel shader 5.1, l'origine dello shader si trova nel file shaderWithRootSig.hlsl, che include una firma radice. La firma shader e radice vengono compilate come BLOB separati nel file binario rs1.fxo.    |
| 2    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | Estrae la firma radice dal file creato dalla riga 1, quindi il file rs1.rs.fxo contiene solo una firma radice.                                                                                                                      |
| 3    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | Rimuove la firma radice dal file creato dalla riga 1, in modo che il file rs1.stripped.fxo contenga uno shader senza firma radice.                                                                                                       |
| 4    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | Combina uno shader e una firma radice in file separati in un file binario contenente entrambi i BLOB. In questo esempio rs1.new.fx0 sarebbe identico a rs1.fx0 nella riga 1.                                                           |
| 5    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | Crea un file binario di firma radice autonomo da un'origine che può contenere più di una semplice firma radice. Si noti la destinazione rootsig 1 0 e che RS1 è il nome della stringa della macro root \_ \_ signature (define) nel file \# HLSL. |



 

La funzionalità disponibile tramite FXC è disponibile anche a livello di codice usando la [**funzione D3DCompile.**](/windows/desktop/direct3dhlsl/d3dcompile) Questa chiamata compila uno shader con una firma radice o una firma radice autonoma (impostando la destinazione rootsig \_ 1 \_ 0). [**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) e [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) possono estrarre e collegare firme radice a un BLOB esistente.  D3D BLOB ROOT SIGNATURE viene usato per specificare il tipo di parte \_ \_ BLOB della firma \_ radice. [**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) rimuove la firma radice (usando il flag D3DCOMPILER \_ STRIP \_ ROOT \_ SIGNATURE) dal BLOB.

## <a name="notes"></a>Note

> [!Note]  
> Mentre la compilazione offline degli shader è fortemente consigliata, se gli shader devono essere compilati in fase di esecuzione, fare riferimento alle osservazioni per [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).

 

> [!Note]  
> Gli asset HLSL esistenti non devono essere modificati per gestire le firme radice da usare con esse.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzazione dinamica con HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[Funzionalità di HLSL Shader Model 5.1 per Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> <dt>

[Associazione di risorse in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Firme radice](root-signatures.md)
</dt> <dt>

[Modello shader 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md)
</dt> <dt>

[Caricamenti Unordered Access View tipi](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 
