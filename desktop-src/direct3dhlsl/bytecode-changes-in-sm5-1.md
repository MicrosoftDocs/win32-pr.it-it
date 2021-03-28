---
title: Modifiche bytecode in SM 5.1
description: SM 5.1 modifica il modo in cui i registri delle risorse vengono dichiarati e viene fatto riferimento nelle istruzioni.
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d66db788b0012a1c3221e37d4c2dd4e41566c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332788"
---
# <a name="bytecode-changes-in-sm51"></a>Modifiche bytecode in SM 5.1

SM 5.1 modifica il modo in cui i registri delle risorse vengono dichiarati e viene fatto riferimento nelle istruzioni.

SM 5.1 si sposta verso la dichiarazione di una "variabile" del registro, in modo analogo al modo in cui viene eseguita per i registri di memoria condivisa del gruppo, illustrata nell'esempio seguente:

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

Il disassembly di questo esempio segue:

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

Ogni intervallo di risorse shader dispone ora di un ID (un nome) nel bytecode dello shader. Ad esempio, Tex1 texture array diventa ' T'1' nel codice byte dello shader. L'assegnazione di ID univoci a ogni intervallo di risorse consente due elementi:

-   Identificare in modo univoco l'intervallo di risorse (vedere \_ la pagina relativa \_ all'indicizzazione della risorsa DCL Texture2D) in un'istruzione (vedere l'istruzione di esempio).
-   Alleghi set di attributi alla dichiarazione, ad esempio il tipo di elemento, le dimensioni stride, la modalità operativa raster e così via.

Si noti che l'ID dell'intervallo non è correlato alla dichiarazione di limite inferiore HLSL.

L'ordine delle associazioni delle risorse di reflection e delle istruzioni di dichiarazione dello shader è lo stesso per facilitare l'identificazione della corrispondenza tra le variabili HLSL e gli ID bytecode.

Ogni istruzione di dichiarazione in SM 5.1 utilizza un operando 3D per definire: ID intervallo, limiti inferiori e superiori. Viene emesso un token aggiuntivo per specificare lo spazio del registro. È possibile che vengano generati anche altri token per fornire proprietà aggiuntive dell'intervallo, ad esempio cbuffer o l'istruzione di dichiarazione del buffer strutturato genera la dimensione di cbuffer o della struttura. I dettagli esatti della codifica sono disponibili in d3d12TokenizedProgramFormat. h e D3D10ShaderBinary:: CShaderCodeParser.

Le istruzioni di SM 5.1 non emetteranno Informazioni aggiuntive sull'operando delle risorse come parte dell'istruzione (ad esempio, SM 5.0). Queste informazioni vengono ora spostate nelle istruzioni di dichiarazione. In SM 5.0, le istruzioni per l'indicizzazione delle risorse gli attributi delle risorse devono essere descritte in token opcode estesi, perché l'indicizzazione ha offuscato l'associazione alla dichiarazione. In SM 5.1 ogni ID (ad esempio,' t 1') viene associato in modo non ambiguo a una singola dichiarazione che descrive le informazioni necessarie sulle risorse. Pertanto, i token opcode estesi usati sulle istruzioni per descrivere le informazioni sulle risorse non vengono più generati.

Nelle istruzioni di non dichiarazione, un operando di risorsa per Samplers, SRVs e UAV è un operando 2D. Il primo indice è una costante letterale che specifica l'ID intervallo. Il secondo indice rappresenta il valore linearizzato dell'indice. Il valore viene calcolato in relazione all'inizio dello spazio di registro corrispondente (non relativo all'inizio dell'intervallo logico) per una migliore correlazione con la firma radice e per ridurre il carico del compilatore del driver per la modifica dell'indice.

Un operando di risorsa per CBVs è un operando 3D: ID letterale dell'intervallo, indice di cbuffer, offset nell'istanza specifica di cbuffer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità del modello HLSL shader 5,1 per Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[Modello Shader 5,1](shader-model-5-1.md)
</dt> </dl>

 

 




