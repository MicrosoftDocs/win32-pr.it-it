---
title: M3x4-vs
description: Moltiplica un vettore a 3 componenti per una matrice 3x4. | M3x4-vs
ms.assetid: 8bec1ac5-376b-4eae-ba82-b42a6c0e7c4e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4018698dbe6ab986945a84c1fcf9ce0431bd0fc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981306"
---
# <a name="m3x4---vs"></a>M3x4-vs

Moltiplica un vettore a 3 componenti per una matrice 3x4.

## <a name="syntax"></a>Sintassi



| M3x4 DST, src0, src1 |
|----------------------|



 

dove

-   DST è il registro di destinazione. Result è un vettore a 4 componenti.
-   src0 è un registro di origine che rappresenta un vettore a 3 componenti.
-   src1 è un registro di origine che rappresenta una matrice 3x4, che corrisponde al primo di 4 registri consecutivi.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| m3x4                   | x    | x    | x    | x     | x    | x     |



 

Per il registro di destinazione è richiesta la maschera xyzw (impostazione predefinita). I modificatori negate e swizzle sono consentiti per src0 ma non per src1.

Nel frammento di codice seguente vengono illustrate le operazioni eseguite.


```
 
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z);
```



Il vettore di input si trova in Register src0. La matrice di input 3x4 è in Register src1 e i successivi tre registri superiori, come illustrato nell'espansione riportata di seguito.

Questa operazione viene in genere usata per trasformare un vettore di posizione in base a una matrice che ha un effetto proiettivo ma non applica alcuna traduzione. Questa istruzione viene implementata come coppia di prodotti punto, come illustrato di seguito.


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




