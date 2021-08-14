---
title: Modifiche al bytecode in SM5.1
description: SM5.1 modifica il modo in cui i registri delle risorse vengono dichiarati e a cui viene fatto riferimento nelle istruzioni.
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93d7d8533bac3750e743166a9d64b687fc06f0fbf21931d44e7d83d462cf15a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794559"
---
# <a name="bytecode-changes-in-sm51"></a>Modifiche al bytecode in SM5.1

SM5.1 modifica il modo in cui i registri delle risorse vengono dichiarati e a cui viene fatto riferimento nelle istruzioni.

SM5.1 si sposta verso la dichiarazione di un registro "variabile", simile a come viene eseguita per i registri di memoria condivisa di gruppo, illustrata nell'esempio seguente:

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

Il disassembly di questo esempio è il seguente:

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim Space Slot  Elements
// ------------------------------ ---------- ------- ----------- ----- ---- ---------
// samp0                             sampler      NA          NA     0    5         1
// tex0                              texture  float4          2d     0    5         1
// tex1[0][5][3]                     texture  float4          2d     0   10 unbounded
// tex2[8]                           texture  float4          2d     1    0         8
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
// Approximately 12 instruction slots used
```

Ogni intervallo di risorse shader ha ora un ID (un nome) nel bytecode dello shader. Ad esempio, la matrice di trame tex1 diventa "t1" nel codice byte dello shader. L'impostazione di ID univoci per ogni intervallo di risorse consente due operazioni:

-   Identificare in modo univoco l'intervallo di risorse (vedere dcl resource texture2d) indicizzato in un'istruzione \_ \_ (vedere l'istruzione di esempio).
-   Associare un set di attributi alla dichiarazione, ad esempio il tipo di elemento, le dimensioni dello stride, la modalità di operazione raster e così via.

Si noti che l'ID dell'intervallo non è correlato alla dichiarazione del limite inferiore HLSL.

L'ordine delle associazioni di risorse di reflection e delle istruzioni di dichiarazione dello shader è lo stesso per facilitare l'identificazione della corrispondenza tra variabili HLSL e ID bytecode.

Ogni istruzione di dichiarazione in SM5.1 usa un operando 3D per definire: ID intervallo, limiti inferiore e superiore. Viene generato un token aggiuntivo per specificare lo spazio di registrazione. È possibile generare anche altri token per trasmettere proprietà aggiuntive dell'intervallo, ad esempio l'istruzione cbuffer o di dichiarazione del buffer strutturato genera le dimensioni del cbuffer o della struttura. I dettagli esatti della codifica sono disponibili in d3d12TokenizedProgramFormat.h e D3D10ShaderBinary::CShaderCodeParser.

Le istruzioni SM5.1 non generano informazioni aggiuntive sull'operando di risorsa come parte dell'istruzione (come in SM5.0). Queste informazioni vengono ora spostate nelle istruzioni di dichiarazione. In SM5.0 le istruzioni per l'indicizzazione delle risorse richiedevano la descrizione degli attributi delle risorse nei token del codice operativo estesi, poiché l'indicizzazione offuscava l'associazione alla dichiarazione. In SM5.1 ogni ID (ad esempio 't1') è associato in modo non ambiguo a una singola dichiarazione che descrive le informazioni sulle risorse necessarie. Di conseguenza, i token opcode estesi usati nelle istruzioni per descrivere le informazioni sulle risorse non vengono più generati.

Nelle istruzioni non di dichiarazione, un operando di risorsa per campionatori, SPV e UAV è un operando 2D. Il primo indice è una costante letterale che specifica l'ID intervallo. Il secondo indice rappresenta il valore linearizzato dell'indice. Il valore viene calcolato in relazione all'inizio dello spazio del registro corrispondente (non rispetto all'inizio dell'intervallo logico) per correlare meglio con la firma radice e ridurre il carico del compilatore del driver di regolazione dell'indice.

Un operando di risorsa per CBV è un operando 3D: ID letterale dell'intervallo, indice del cbuffer, offset nell'istanza specifica di cbuffer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di HLSL Shader Model 5.1 per Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 5.1](shader-model-5-1.md)
</dt> </dl>

 

 




