---
title: dcl_semantics (sm3 - ps asm)
description: Dichiarare l'associazione tra l'output del vertex shader e pixel shader input.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c506d2ad23003f93bbaea409cacc60b18c86534
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129708"
---
# <a name="dcl_semantics-sm3---ps-asm"></a>semantica dcl \_ (sm3 - ps asm)

Dichiarare l'associazione tra l'output del vertex shader e pixel shader input.

## <a name="syntax"></a>Sintassi

dcl \_ semantics \[ \_ centroid \] dst \[ .write \_ mask\]



 

Dove:

-   \_semantica: identifica l'utilizzo dei dati previsto e può essere uno dei valori in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (senza il prefisso D3DDECLUSAGE). \_ Inoltre, è possibile aggiungere un indice integer alla semantica per distinguere i parametri che usano una semantica simile.
-   \[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] è un modificatore di istruzione facoltativo. È supportato nelle istruzioni di utilizzo dcl che dichiarano i registri \_ di input e nelle istruzioni di ricerca trame. Il centroide viene aggiunto senza spazio.
-   dst: registro di destinazione. Vedere [ps \_ 3 \_ 0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).
-   write mask: lo stesso registro di output può essere dichiarato più volte, ogni volta con una maschera di scrittura univoca (in modo che sia possibile applicare una semantica diversa \_ ai singoli componenti). Tuttavia, la stessa semantica non può essere usata più volte in una dichiarazione. Ciò significa che i vettori devono essere quattro componenti o meno e non possono attraversare i limiti del registro a quattro componenti (registri di output singoli). Quando viene \_ usata la semantica psize, deve avere una maschera di scrittura completa perché è considerata scalare. Quando viene usata la semantica di posizione, deve avere una maschera di scrittura completa perché tutti e quattro i componenti \_ devono essere scritti.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Utilizzo di \_ dcl            |      |      |      |      |      |      |       | x    | x     |



 

Tutte le istruzioni di \_ utilizzo dcl devono essere visualizzate prima della prima istruzione eseguibile.

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

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[Esempio di antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)
</dt> </dl>

 

 
