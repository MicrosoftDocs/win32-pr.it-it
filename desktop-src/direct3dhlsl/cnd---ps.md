---
title: cnd - ps
description: Sceglie in modo condizionale tra src1 e src2, in base al confronto src0 0.5.
ms.assetid: 7a3b49e9-d146-47dc-99a8-4f336db7d0d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cb31c873bf3a4e38048f57d75a30cec70021716d2aab43b683cb29aef25f7f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726961"
---
# <a name="cnd---ps"></a>cnd - ps

Sceglie in modo condizionale tra src1 e src2, in base al confronto src0 > 0.5.

## <a name="syntax"></a>Sintassi



| cnd dst, src0, src1, src2 |
|---------------------------|



 

dove

-   dst è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.
-   src2 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Cnd                   | x    | x    | x    | x    |      |      |       |      |       |



 

Per le versioni \_ da 1 a 1 \_ 3, src0 deve essere r0.a.


```
// Version 1_1 to 1_3
if (r0.a > 0.5)
  dest = src1
else
  dest = src2
```



La versione \_ 1 4 confronta ogni canale separatamente.


```
for each component in src0
{
   if (src0.component > 0.5)
     dest.component = src1.component
   else
     dest.component = src2.component
}
```



Questi esempi mostrano un confronto a quattro canali eseguito in uno shader versione 1 4, nonché un confronto a canale singolo possibile \_ in uno shader versione \_ 1 1.


```
ps_1_4
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1

cnd r1, c0, c1, c2   // r0 contains 1,1,1,0 because
// r1.x = c2.x because c0.x <= 0.5
// r1.y = c2.y because c0.y <= 0.5
// r1.z = c2.z because c0.z <= 0.5
// r1.w = c1.w because c0.w >  0.5
```



La versione \_ 1 da 1 a 1 3 viene confrontata solo con il canale alfa replicato \_ di r0.


```
ps_1_1
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1
mov r0, c0
cnd r1, r0.a, c1, c2   // r1 gets assigned 0,0,0,0 because 
                       // r0.a > 0.5, therefore r1.xyzw = c1.xyzw
```



In questo esempio vengono confrontati due valori, A e B. L'esempio presuppone che A sia caricato in v0 e che B sia caricato in v1. Sia A che B devono essere compresi nell'intervallo compreso tra -1 e +1 e poiché i registri colori (vn) sono definiti come compresi tra 0 e 1, la restrizione viene soddisfatta in questo esempio.


```
ps_1_1                // Version instruction
sub r0, v0, v1_bias   // r0 = A - (B - 0.5)
cnd r0, r0.a, c0, c1  // r0 = ( A > B ? c0 : c1 )

// r0 = c0 if A > B, otherwise, r0 = c1
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




