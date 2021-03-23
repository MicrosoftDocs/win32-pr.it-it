---
title: Specifica delle firme radice in HLSL
description: La specifica delle firme radice nel modello HLSL shader 5,1 rappresenta un'alternativa alla relativa specifica nel codice C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236876e22c3e1e0bb849ec1e1bc7d45692c900d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548785"
---
# <a name="specifying-root-signatures-in-hlsl"></a>Specifica delle firme radice in HLSL

La specifica delle firme radice nel modello HLSL shader 5,1 rappresenta un'alternativa alla relativa specifica nel codice C++.

-   [Esempio di firma radice HLSL](#an-example-hlsl-root-signature)
    -   [Firma radice versione 1,0](#root-signature-version-10)
    -   [Firma radice versione 1,1](#root-signature-version-11)
-   [RootFlags](#rootflags)
-   [Costanti radice](#root-constants)
-   [Visibilità](#visibility)
-   [CBV a livello di radice](#root-level-cbv)
-   [SRV a livello radice](#root-level-srv)
-   [UAV a livello radice](#root-level-uav)
-   [Tabella descrittori](#descriptor-table)
-   [Campionatore statico](#static-sampler)
-   [Compilazione di una firma radice HLSL](#compiling-an-hlsl-root-signature)
-   [Modifica delle firme radice con il compilatore FXC](#manipulating-root-signatures-with-the-fxc-compiler)
-   [Note](#notes)
-   [Argomenti correlati](#related-topics)

## <a name="an-example-hlsl-root-signature"></a>Esempio di firma radice HLSL

Una firma radice può essere specificata in HLSL come stringa. La stringa contiene una raccolta di clausole separate da virgole che descrivono i componenti costitutivi della firma radice. La firma radice deve essere identica tra gli shader per un qualsiasi oggetto di stato della pipeline (PSO). Ecco un esempio:

### <a name="root-signature-version-10"></a>Firma radice versione 1,0

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

### <a name="root-signature-version-11"></a>Firma radice versione 1,1

La [firma radice versione 1,1](root-signature-version-1-1.md) Abilita le ottimizzazioni dei driver nei descrittori e nei dati della firma radice.

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

Questa definizione darebbe la seguente firma radice, annotando:

-   Uso dei parametri predefiniti.
-   B0 e (B0, spazio = 1) non sono in conflitto
-   U0 è visibile solo per il geometry shader
-   il valore di U4 e U5 è associato allo stesso descrittore in un heap

![firma radice specificata utilizzando il linguaggio shader di alto livello](images/hlsl-root-signature.png)

Il linguaggio di firma radice HLSL corrisponde strettamente alle API della firma radice C++ e ha una potenza espressiva equivalente. La firma radice viene specificata come sequenza di clausole, separate da virgola. L'ordine delle clausole è importante, in quanto l'ordine di analisi determina la posizione dello slot nella firma radice. Ogni clausola accetta uno o più parametri denominati. Tuttavia, l'ordine dei parametri non è importante.

## <a name="rootflags"></a>RootFlags

La clausola *RootFlags* facoltativa accetta 0 (il valore predefinito per indicare nessun flag) o uno o più valori di flag radice predefiniti connessi tramite l' \| operatore OR. I valori dei flag radice consentiti sono definiti dai [**\_ \_ \_ flag della firma radice D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

Ad esempio:

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a>Costanti radice

La clausola *RootConstants* specifica le costanti radice nella firma radice. Due parametri obbligatori sono: *num32BitConstants* e *bReg* (il registro corrispondente a *BaseShaderRegister* nelle API C++) del *cbuffer*. Lo spazio (*RegisterSpace* nelle API c++) e i parametri Visibility (*ShaderVisibility* in c++) sono facoltativi e i valori predefiniti sono:

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

Ad esempio:

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a>Visibilità

Visibility è un parametro facoltativo che può avere uno dei valori di [**D3D12 \_ shader \_ visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).

\_ \_ La visibilità dello shader trasmette tutti gli argomenti radice a tutti gli shader. In alcuni componenti hardware non è previsto alcun costo, ma su altri hardware è previsto un costo per la divisione dei dati in tutte le fasi dello shader. Impostando una delle opzioni, ad esempio \_ \_ il vertice di visibilità dello shader, il limite dell'argomento radice viene limitato a una singola fase dello shader.

L'impostazione degli argomenti radice sulle fasi di una singola shader consente di utilizzare lo stesso nome di binding in fasi diverse. Ad esempio, un'associazione SRV di `t0,SHADER_VISIBILITY_VERTEX` e l'associazione SRV di `t0,SHADER_VISIBILITY_PIXEL` sarebbero validi. Tuttavia, se l'impostazione di visibilità era `t0,SHADER_VISIBILITY_ALL` per una delle associazioni, la firma radice non sarebbe valida.

## <a name="root-level-cbv"></a>CBV a livello di radice

La `CBV` clausola (visualizzazione del buffer costante) specifica una voce del registro di livello radice b-register reg. Si noti che si tratta di una voce scalare; non è possibile specificare un intervallo per il livello radice.

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a>SRV a livello radice

La `SRV` clausola (visualizzazione risorse shader) specifica una voce reg t-Register di livello radice. Si noti che si tratta di una voce scalare; non è possibile specificare un intervallo per il livello radice.

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a>UAV a livello radice

La `UAV` clausola (visualizzazione di accesso non ordinato) specifica una voce del registro di stato di un UAV u-Register a livello radice. Si noti che si tratta di una voce scalare; non è possibile specificare un intervallo per il livello radice.

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Ad esempio:

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a>Tabella descrittori

La `DescriptorTable` clausola è a sua volta un elenco di clausole della tabella descrittore separate da virgole, oltre a un parametro di visibilità facoltativo. Le clausole *DescriptorTable* includono CBV, SRV, UAV e Sampler. Si noti che i parametri sono diversi da quelli delle clausole di livello radice.

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

La tabella descrittore `CBV` presenta la sintassi seguente:

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Ad esempio:

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

Il parametro obbligatorio *bReg* specifica il reg iniziale dell'intervallo di cbuffer. Il parametro *descrittori numerici* specifica il numero di descrittori nell'intervallo cbuffer contiguo; il valore predefinito è 1. La voce dichiara un intervallo di cbuffer ` [Reg, Reg + numDescriptors - 1]` , quando *descrittori numerici* è un numero. Se *descrittori numerici* è uguale a "unbounded", l'intervallo è `[Reg, UINT_MAX]` , il che significa che l'app deve assicurarsi che non faccia riferimento a un'area non associata. Il campo *offset* rappresenta il parametro *OffsetInDescriptorsFromTableStart* nelle API C++, ovvero l'offset (nei descrittori) dall'inizio della tabella. Se l'offset è impostato su offset intervallo descrittore \_ \_ \_ (impostazione predefinita), significa che l'intervallo è immediatamente successivo all'intervallo precedente. Tuttavia, l'immissione di offset specifici consente la sovrapposizione degli intervalli, consentendo l'aliasing del registro.

La tabella descrittore `SRV` presenta la sintassi seguente:

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Questa operazione è simile alla voce della tabella descrittore `CBV` , ad eccezione dell'intervallo specificato per le visualizzazioni delle risorse dello shader.

La tabella descrittore `UAV` presenta la sintassi seguente:

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Questa operazione è simile alla voce della tabella descrittore `CBV` , ad eccezione dell'intervallo specificato per le visualizzazioni di accesso non ordinato.

La tabella descrittore `Sampler` presenta la sintassi seguente:

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

Questa operazione è simile alla voce della tabella descrittore `CBV` , ad eccezione dell'intervallo specificato per i sampler shader. Si noti che i sampler non possono essere combinati con altri tipi di descrittori nella stessa tabella dei descrittori (poiché si trovano in un heap descrittore separato).

## <a name="static-sampler"></a>Campionatore statico

Il campionatore statico rappresenta la struttura [**\_ \_ \_ Desc del campionatore statico D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) . Il parametro obbligatorio per *StaticSampler* è un reg del campionatore s-Register scalare. Altri parametri sono facoltativi con i valori predefiniti indicati di seguito. La maggior parte dei campi accetta un set di enumerazioni predefinite.

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

Le opzioni dei parametri sono molto simili alle chiamate API C++, ad eccezione di *BorderColor*, che è limitata a un'enumerazione in HLSL.

Il campo filtro può essere un [**\_ filtro D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).

I campi dell'indirizzo possono essere ognuno di uno della [**\_ \_ \_ modalità di indirizzamento della trama D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).

La funzione di confronto può essere uno dei [**D3D12 di \_ confronto \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).

Il campo colore bordo può essere uno dei [**\_ colori del \_ bordo \_ statico D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).

La visibilità può essere una delle [**D3D12 \_ shader \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).

## <a name="compiling-an-hlsl-root-signature"></a>Compilazione di una firma radice HLSL

Esistono due meccanismi per compilare una firma radice HLSL. In primo luogo, è possibile allegare una stringa di firma radice a un particolare shader tramite l'attributo *RootSignature* (nell'esempio seguente, usando il punto di ingresso **MyRS1** ):

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

Il compilatore creerà e verificherà il BLOB della firma radice per lo shader e lo integrerà insieme al codice byte dello shader nel BLOB dello shader. Il compilatore supporta la sintassi della firma radice per il modello di shader 5,0 e versioni successive. Se una firma radice è incorporata in uno shader model 5,0 Shader e tale shader viene inviato al runtime D3D11, invece di D3D12, la parte relativa alla firma radice verrà ignorata automaticamente da D3D11.

L'altro meccanismo consiste nel creare un BLOB di firma radice autonomo, ad esempio per riutilizzarlo con un ampio set di shader, risparmiando spazio. Lo [strumento di compilazione degli effetti](/windows/desktop/direct3dtools/fxc) (FXC) supporta entrambi i modelli **rootsig \_ 1 \_ 0** e **rootsig \_ 1 \_ 1** shader. Il nome della stringa define viene specificato tramite il consueto argomento/E. Ad esempio:

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

Si noti che la stringa di firma radice define può essere passata anche nella riga di comando, ad esempio/D MyRS1 = "...".

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a>Modifica delle firme radice con il compilatore FXC

Il compilatore FXC crea il codice byte dello shader dai file di origine HLSL. Per questo compilatore sono disponibili numerosi parametri facoltativi, fare riferimento allo [strumento di compilazione degli effetti](/windows/desktop/direct3dtools/fxc).

Per la gestione delle firme radice create da HLSL, nella tabella seguente vengono forniti alcuni esempi di utilizzo di FXC.



| Linea | Riga di comando                                                                 | Descrizione                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | Compila uno shader per la destinazione pixel shader 5,1, l'origine dello shader si trova nel file shaderWithRootSig. HLSL, che include una firma radice. Lo shader e la firma radice vengono compilati come BLOB separati nel file binario RS1. FXO.    |
| 2    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | Estrae la firma radice dal file creato dalla riga 1, quindi il file RS1. RS. FXO contiene solo una firma radice.                                                                                                                      |
| 3    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | Rimuove la firma radice dal file creato dalla riga 1, quindi il file RS1. Stripped. FXO contiene uno shader senza firma radice.                                                                                                       |
| 4    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | Combina uno shader e una firma radice che si trovano in file distinti in un file binario contenente entrambi i BLOB. In questo esempio RS1. New. FX0 sarà identico a RS1. FX0 nella riga 1.                                                           |
| 5    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | Crea un file binario della firma radice autonomo da un'origine che può contenere più di una sola firma radice. Si noti la \_ destinazione rootsig 1 \_ 0 e che RS1 è il nome della stringa della macro della firma radice ( \# define) nel file HLSL. |



 

La funzionalità disponibile tramite FXC è disponibile anche a livello di programmazione tramite la funzione [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) . Questa chiamata compila uno shader con una firma radice o una firma radice autonoma (impostando la \_ destinazione rootsig 1 \_ 0). [**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) e [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) possono estrarre e alleghi le firme radice a un BLOB esistente.\_ \_ La firma radice BLOB D3D \_ viene utilizzata per specificare il tipo di parte BLOB della firma radice. [**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) rimuove la firma radice (usando il \_ \_ \_ flag di firma radice di D3DCOMPILER Strip) dal BLOB.

## <a name="notes"></a>Note

> [!Note]  
> Mentre la compilazione offline degli shader è fortemente consigliata, se gli shader devono essere compilati in fase di esecuzione, fare riferimento alle note relative a [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).

 

> [!Note]  
> Non è necessario modificare gli asset HLSL esistenti per gestire le firme radice da usare con loro.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzazione dinamica con HLSL 5,1](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[Funzionalità del modello HLSL shader 5,1 per Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> <dt>

[Associazione di risorse in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Firme radice](root-signatures.md)
</dt> <dt>

[Modello Shader 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md)
</dt> <dt>

[Caricamenti Unordered Access View tipizzati](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 