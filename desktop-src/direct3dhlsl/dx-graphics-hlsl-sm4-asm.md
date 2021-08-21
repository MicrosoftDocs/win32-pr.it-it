---
title: Assembly del modello shader 4
description: Assembly del modello shader 4
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 805ffe89b1f9d14ca70da0a8121353e6bf766b8b6e433441350d1b55c4531415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119955"
---
# <a name="shader-model-4-assembly"></a>Assembly del modello shader 4

Il modello shader 4 richiede la programmazione degli shader in HLSL. Tuttavia, il compilatore shader compila il codice HLSL nell'assembly eseguito nel dispositivo. Se si usa PIX per Windows eseguire il debug degli shader, è possibile scegliere di visualizzare il codice dello shader in HLSL o assembly. Questa sezione elenca le istruzioni dell'assembly Shader Model 4 e Shader Model 4.1 che possono verificarsi durante il debug di uno shader.

<dl>

[Modificatori di istruzione](instruction-modifiers.md)  
[add](add--sm4---asm-.md)  
[and](and--sm4---asm-.md)  
[break](break--sm4---asm-.md)  
[breakc](breakc--sm4---asm-.md)  
[call](call--sm4---asm-.md)  
[callc](callc--sm4---asm-.md)  
[case](case--sm4---asm-.md)  
[Continuare](continue--sm4---asm-.md)  
[continuec](continuec--sm4---asm-.md)  
[Tagliare](cut--sm4---asm-.md)  
[dcl \_ constantBuffer](dcl-constantbuffer.md)  
[dcl \_ globalFlags](dcl-globalflags.md)  
[dcl \_ immediateConstantBuffer](dcl-immediateconstantbuffer.md)  
[dcl \_ indexableTemp](dcl-indexabletemp.md)  
[dcl \_ indexRange](dcl-indexrange.md)  
[input \_ dcl](dcl-input.md)  
[dcl \_ input \_ sv](dcl-input-sv.md)  
[dcl \_ input vPrim](dcl-input-vprim.md)  
[dcl \_ maxOutputVertexCount](dcl-maxoutputvertexcount.md)  
[Output \_ dcl](dcl-output.md)  
[dcl \_ output \_ oDepth](dcl-output-odepth.md)  
[dcl \_ output \_ sgv](dcl-output-sgv.md)  
[dcl \_ output \_ siv](dcl-output-siv.md)  
[dcl \_ outputTopology](dcl-outputtopology.md)  
[Risorsa \_ dcl](dcl-resource.md)  
[Campionatore dcl \_](dcl-sampler.md)  
[dcl \_ temps](dcl-temps.md)  
[default](default--sm4---asm-.md)  
[deriv \_ rtx](deriv-rtx--sm4---asm-.md)  
[deriv \_ rty](deriv-rty--sm4---asm-.md)  
[Scartare](discard--sm4---asm-.md)  
[div](div--sm4---asm-.md)  
[dp2](dp2--sm4---asm-.md)  
[dp3](dp3--sm4---asm-.md)  
[dp4](dp4--sm4---asm-.md)  
[else](else--sm4---asm-.md)  
[Emettere](emit--sm4---asm-.md)  
[emitThenCut](emitthencut--sm4---asm-.md)  
[endif](endif--sm4---asm-.md)  
[endloop](endloop--sm4---asm-.md)  
[endswitch](endswitch--sm4---asm-.md)  
[eq](eq--sm4---asm-.md)  
[exp](exp--sm4---asm-.md)  
[Frc](frc--sm4---asm-.md)  
[ftoi](ftoi--sm4---asm-.md)  
[ftou](ftou--sm4---asm-.md)  
[ge](ge--sm4---asm-.md)  
[iadd](iadd--sm4---asm-.md)  
[ibfe](dne--sm5---asm-.md)  
[ieq](ieq--sm4---asm-.md)  
[if](if--sm4---asm-.md)  
[Ige](ige--sm4---asm-.md)  
[ilt](ilt--sm4---asm-.md)  
[Imad](imad--sm4---asm-.md)  
[imin](imin--sm4---asm-.md)  
[imul](imul--sm4---asm-.md)  
[Ine](ine--sm4---asm-.md)  
[ineg](ineg--sm4---asm-.md)  
[ishl](ishl--sm4---asm-.md)  
[ishr](ishr--sm4---asm-.md)  
[itof](itof--sm4---asm-.md)  
[label](label--sm4---asm-.md)  
[Ld](ld--sm4---asm-.md)  
[Registro](log--sm4---asm-.md)  
[Ciclo](loop--sm4---asm-.md)  
[lt](lt--sm4---asm-.md)  
[matto](mad--sm4---asm-.md)  
[max](max--sm4---asm-.md)  
[min](min--sm4---asm-.md)  
[Mov](mov--sm4---asm-.md)  
[movc](movc--sm4---asm-.md)  
[mul](mul--sm4---asm-.md)  
[ne](ne--sm4---asm-.md)  
[Nop](nop--sm4---asm-.md)  
[not](not--sm4---asm-.md)  
[or](or--sm4---asm-.md)  
[Resinfo](resinfo--sm4---asm-.md)  
[Ret](ret--sm4---asm-.md)  
[retc](retc--sm4---asm-.md)  
[round \_ ne](round-ne--sm4---asm-.md)  
[round \_ ni](round-ni--sm4---asm-.md)  
[round \_ pi](round-pi--sm4---asm-.md)  
[round \_ z](round-z--sm4---asm-.md)  
[Rsq](rsq--sm4---asm-.md)  
[Esempio](sample--sm4---asm-.md)  
[esempio \_ b](sample-b--sm4---asm-.md)  
[esempio \_ c](sample-c--sm4---asm-.md)  
[sample \_ c \_ lz](sample-c-lz--sm4---asm-.md)  
[sample \_ d](sample-d--sm4---asm-.md)  
[sample \_ l](sample-l--sm4---asm-.md)  
[Sincos](sincos--sm4---asm-.md)  
[Sqrt](sqrt--sm4---asm-.md)  
[switch](switch--sm4---asm-.md)  
[udiv](udiv--sm4---asm-.md)  
[Uge](uge--sm4---asm-.md)  
[Ult](ult--sm4---asm-.md)  
[umad](umad--sm4---asm-.md)  
[Umax](umax--sm4---asm-.md)  
[umin](umin--sm4---asm-.md)  
[umul](umul--sm4---asm-.md)  
[ushr](ushr--sm4---asm-.md)  
[utof](utof--sm4---asm-.md)  
[Xor](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a>Assembly del modello shader 4.1

Shader Model 4.1 supporta tutte le istruzioni shader Model 4.0 e le istruzioni aggiuntive seguenti:

<dl>

[gather4](gather4--sm4-1---asm-.md)  
[ld2dms](ld2dms--sm4-1---asm-.md)  
[Lod](lod--sm4-1---asm-.md)  
[sampleinfo](sampleinfo--sm4-1---asm-.md)  
[samplepos](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Asm Shader](dx9-graphics-reference-asm.md)
</dt> <dt>

[Modello shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




