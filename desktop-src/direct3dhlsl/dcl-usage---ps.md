---
title: dcl_semantics (SM3-PS ASM)
description: Dichiarare l'associazione tra l'output del vertex shader e l'input pixel shader.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 944ddd2b581c6179ac4a3fe22f2b687f85aecfdc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118067"
---
# <a name="dcl_semantics-sm3---ps-asm"></a>\_semantica di DCL (SM3-PS ASM)

Dichiarare l'associazione tra l'output del vertex shader e l'input pixel shader.

## <a name="syntax"></a>Sintassi



|                                                   |
|---------------------------------------------------|
| \_maschera di semantica di DCL \[ \_ \] \[ . \_\] |



 

Dove:

-   \_semantica: identifica l'utilizzo previsto dei dati e può essere uno qualsiasi dei valori in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (senza il \_ prefisso D3DDECLUSAGE). Inoltre, un indice Integer può essere aggiunto alla semantica per distinguere i parametri che usano una semantica simile.
-   \[\_[](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) Centro \] modificatore di istruzione facoltativo. È supportato nelle istruzioni di utilizzo di DCL \_ che dichiarano i registri di input e le istruzioni per la ricerca di trame. Il baricentro viene aggiunto senza spazio.
-   DST: Registro di destinazione. Vedere [ \_ registri PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).
-   \_maschera di scrittura: lo stesso registro di output può essere dichiarato più volte, ogni volta con una maschera di scrittura univoca (pertanto è possibile applicare una semantica diversa ai singoli componenti). Tuttavia, la stessa semantica non può essere utilizzata più volte in una dichiarazione. Ciò significa che i vettori devono essere costituiti da quattro componenti o meno e non possono superare i limiti di registro a quattro componenti (singoli registri di output). Quando si \_ Usa la semantica psize, deve avere una maschera di scrittura completa perché è considerata scalare. Quando \_ si usa la semantica di posizione, deve avere una maschera di scrittura completa perché tutti e quattro i componenti devono essere scritti.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| utilizzo di DCL \_            |      |      |      |      |      |      |       | x    | x     |



 

Tutte le \_ istruzioni di utilizzo di DCL devono essere visualizzate prima della prima istruzione eseguibile.

## <a name="declaration-examples"></a>Esempi di dichiarazione


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[Esempio antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)
</dt> </dl>

 

 