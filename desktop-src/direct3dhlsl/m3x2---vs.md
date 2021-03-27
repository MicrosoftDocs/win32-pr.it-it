---
title: M3X2-vs
description: Moltiplica un vettore a 3 componenti per una matrice 3x2. | M3X2-vs
ms.assetid: 4ef3bd47-3e38-4d9d-a8f5-6ee9c08de69c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 870a8d4918870930faa536ead01dab2947d5faea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234697"
---
# <a name="m3x2---vs"></a>M3X2-vs

Moltiplica un vettore a 3 componenti per una matrice 3x2.

## <a name="syntax"></a>Sintassi



| M3X2 DST, src0, src1 |
|----------------------|



 

dove

-   DST è il registro di destinazione. Il risultato è un vettore a 2 componenti.
-   src0 è un registro di origine che rappresenta un vettore a 3 componenti.
-   src1 è un registro di origine che rappresenta una matrice 3x2, che corrisponde al primo di due registri consecutivi.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| m3x2                   | x    | x    | x    | x     | x    | x     |



 

La maschera XY è obbligatoria per il registro di destinazione. I modificatori negate e swizzle sono consentiti per src0 ma non per src1.

Le equazioni seguenti illustrano il funzionamento dell'istruzione:


```
dest.x = (src0.x * src1.x) + (src0.x * src1.y) + (src0.x * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
```



Il vettore di input si trova in Register src0. La matrice di input 3x2 si trova in Register src1 e il successivo registro superiore nello stesso file di registro, come illustrato nella seguente espansione. Viene generato un risultato 2D, lasciando inalterati gli altri elementi del registro di destinazione (dest. z e dest. w).

Questa operazione viene comunemente utilizzata per le trasformazioni 2D. Questa istruzione viene implementata come coppia di prodotti punto, come illustrato di seguito.


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



I modificatori swizzle e negazioni non sono validi per il registro src1. Il registro dest e src0, o uno qualsiasi dei registri src1 + i, non può essere lo stesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




