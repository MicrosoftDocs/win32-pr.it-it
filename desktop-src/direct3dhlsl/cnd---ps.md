---
title: CND-PS
description: Sceglie in modo condizionale tra src1 e src2, in base al confronto src0 0,5.
ms.assetid: 7a3b49e9-d146-47dc-99a8-4f336db7d0d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1fd3a14e2ac4bd283a4e67724fbb42ac965ea707
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117197"
---
# <a name="cnd---ps"></a>CND-PS

Sceglie in modo condizionale tra src1 e src2, in base al confronto src0 > 0,5.

## <a name="syntax"></a>Sintassi



| CND DST, src0, src1, src2 |
|---------------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.
-   src2 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| CND                   | x    | x    | x    | x    |      |      |       |      |       |



 

Per le versioni da 1 \_ a 1 \_ 3, src0 deve essere R0. a.


```
// Version 1_1 to 1_3
if (r0.a > 0.5)
  dest = src1
else
  dest = src2
```



La versione 1 \_ 4 confronta ogni canale separatamente.


```
for each component in src0
{
   if (src0.component > 0.5)
     dest.component = src1.component
   else
     dest.component = src2.component
}
```



In questi esempi viene illustrato un confronto a quattro canali eseguito in uno \_ shader versione 1 4, nonché un confronto a canale singolo possibile in uno shader della versione 1 \_ .


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



La versione 1 \_ 1 a 1 \_ 3 viene confrontata solo con il canale alfa replicato di R0.


```
ps_1_1
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1
mov r0, c0
cnd r1, r0.a, c1, c2   // r1 gets assigned 0,0,0,0 because 
                       // r0.a > 0.5, therefore r1.xyzw = c1.xyzw
```



In questo esempio vengono confrontati due valori, A e B. Nell'esempio si presuppone che un sia caricato in V0 e B sia caricato nella versione 1. Sia a che B devono essere compresi nell'intervallo da-1 a + 1 e, poiché i registri colori (VN) sono definiti come compresi tra 0 e 1, in questo esempio la restrizione viene soddisfatta.


```
ps_1_1                // Version instruction
sub r0, v0, v1_bias   // r0 = A - (B - 0.5)
cnd r0, r0.a, c0, c1  // r0 = ( A > B ? c0 : c1 )

// r0 = c0 if A > B, otherwise, r0 = c1
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




