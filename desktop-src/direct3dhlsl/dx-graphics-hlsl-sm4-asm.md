---
title: Assembly Shader Model 4
description: Assembly Shader Model 4
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044751"
---
# <a name="shader-model-4-assembly"></a>Assembly Shader Model 4

Shader Model 4 richiede di programmare gli shader in HLSL. Tuttavia, il compilatore shader compila il codice HLSL nell'assembly in esecuzione nel dispositivo. Se si usa PIX per Windows per eseguire il debug degli shader, è possibile scegliere di visualizzare il codice dello shader in HLSL o assembly. Questa sezione elenca le istruzioni di assembly Shader Model 4 e Shader Model 4,1 che possono verificarsi durante il debug di uno shader.

<dl>

[Modificatori di istruzione](instruction-modifiers.md)  
[add](add--sm4---asm-.md)  
[and](and--sm4---asm-.md)  
[break](break--sm4---asm-.md)  
[breakc](breakc--sm4---asm-.md)  
[call](call--sm4---asm-.md)  
[callc](callc--sm4---asm-.md)  
[case](case--sm4---asm-.md)  
[continuare](continue--sm4---asm-.md)  
[continuec](continuec--sm4---asm-.md)  
[tagliare](cut--sm4---asm-.md)  
[\_constantBuffer DCL](dcl-constantbuffer.md)  
[\_globalFlags DCL](dcl-globalflags.md)  
[\_immediateConstantBuffer DCL](dcl-immediateconstantbuffer.md)  
[\_indexableTemp DCL](dcl-indexabletemp.md)  
[\_indexRange DCL](dcl-indexrange.md)  
[\_input DCL](dcl-input.md)  
[\_input DCL \_ SV](dcl-input-sv.md)  
[\_vPrim di input DCL](dcl-input-vprim.md)  
[\_maxOutputVertexCount DCL](dcl-maxoutputvertexcount.md)  
[output di DCL \_](dcl-output.md)  
[\_oDepth output \_ DCL](dcl-output-odepth.md)  
[\_SGV output \_ DCL](dcl-output-sgv.md)  
[\_SIV output di DCL \_](dcl-output-siv.md)  
[\_outputTopology DCL](dcl-outputtopology.md)  
[\_risorsa DCL](dcl-resource.md)  
[\_campionatore DCL](dcl-sampler.md)  
[Temp di DCL \_](dcl-temps.md)  
[default](default--sm4---asm-.md)  
[derivazione \_ RTX](deriv-rtx--sm4---asm-.md)  
[derivazione \_ valore](deriv-rty--sm4---asm-.md)  
[rimuovere](discard--sm4---asm-.md)  
[div](div--sm4---asm-.md)  
[DP2](dp2--sm4---asm-.md)  
[dp3](dp3--sm4---asm-.md)  
[DP4](dp4--sm4---asm-.md)  
[else](else--sm4---asm-.md)  
[Emit](emit--sm4---asm-.md)  
[emitThenCut](emitthencut--sm4---asm-.md)  
[endif](endif--sm4---asm-.md)  
[endloop](endloop--sm4---asm-.md)  
[endswitch](endswitch--sm4---asm-.md)  
[eq](eq--sm4---asm-.md)  
[exp](exp--sm4---asm-.md)  
[FRC](frc--sm4---asm-.md)  
[ftoi](ftoi--sm4---asm-.md)  
[ftou](ftou--sm4---asm-.md)  
[ge](ge--sm4---asm-.md)  
[IAdd](iadd--sm4---asm-.md)  
[ibfe](dne--sm5---asm-.md)  
[IEQ](ieq--sm4---asm-.md)  
[if](if--sm4---asm-.md)  
[IgE](ige--sm4---asm-.md)  
[ILT](ilt--sm4---asm-.md)  
[imad](imad--sm4---asm-.md)  
[Imin](imin--sm4---asm-.md)  
[IMUL](imul--sm4---asm-.md)  
[ine](ine--sm4---asm-.md)  
[ineg](ineg--sm4---asm-.md)  
[ishl](ishl--sm4---asm-.md)  
[ISHR](ishr--sm4---asm-.md)  
[itof](itof--sm4---asm-.md)  
[label](label--sm4---asm-.md)  
[LD](ld--sm4---asm-.md)  
[log](log--sm4---asm-.md)  
[loop](loop--sm4---asm-.md)  
[lt](lt--sm4---asm-.md)  
[pazzo](mad--sm4---asm-.md)  
[max](max--sm4---asm-.md)  
[min](min--sm4---asm-.md)  
[MOV](mov--sm4---asm-.md)  
[movc](movc--sm4---asm-.md)  
[mul](mul--sm4---asm-.md)  
[ne](ne--sm4---asm-.md)  
[NOP](nop--sm4---asm-.md)  
[not](not--sm4---asm-.md)  
[or](or--sm4---asm-.md)  
[ResInfo](resinfo--sm4---asm-.md)  
[RET](ret--sm4---asm-.md)  
[retc](retc--sm4---asm-.md)  
[Round \_ ne](round-ne--sm4---asm-.md)  
[Round \_ NI](round-ni--sm4---asm-.md)  
[Round \_ pi](round-pi--sm4---asm-.md)  
[Round \_ z](round-z--sm4---asm-.md)  
[RSQ](rsq--sm4---asm-.md)  
[esempio](sample--sm4---asm-.md)  
[esempio \_ b](sample-b--sm4---asm-.md)  
[esempio \_ c](sample-c--sm4---asm-.md)  
[esempio \_ c \_ LZ](sample-c-lz--sm4---asm-.md)  
[esempio \_ d](sample-d--sm4---asm-.md)  
[esempio \_ l](sample-l--sm4---asm-.md)  
[SinCos](sincos--sm4---asm-.md)  
[sqrt](sqrt--sm4---asm-.md)  
[switch](switch--sm4---asm-.md)  
[udiv](udiv--sm4---asm-.md)  
[uge](uge--sm4---asm-.md)  
[Ultimate](ult--sm4---asm-.md)  
[Martina](umad--sm4---asm-.md)  
[Umax](umax--sm4---asm-.md)  
[Umin](umin--sm4---asm-.md)  
[umul](umul--sm4---asm-.md)  
[ushr](ushr--sm4---asm-.md)  
[utof](utof--sm4---asm-.md)  
[XOR](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a>Assembly del modello Shader 4,1

Il modello di Shader 4,1 supporta tutte le istruzioni per il modello di Shader 4,0 e le istruzioni aggiuntive seguenti:

<dl>

[gather4](gather4--sm4-1---asm-.md)  
[ld2dms](ld2dms--sm4-1---asm-.md)  
[trama](lod--sm4-1---asm-.md)  
[sampleinfo](sampleinfo--sm4-1---asm-.md)  
[samplepos](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ASM shader](dx9-graphics-reference-asm.md)
</dt> <dt>

[Modello Shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




