---
title: m4x3 - vs
description: Moltiplica un vettore a 4 componenti per una matrice 4x3. | m4x3 - vs
ms.assetid: 12dd31bd-2078-44a1-912e-72c8f377bc4c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf4fb45fd38fe7d5acec95d750a050144a408c7fd1dedc44be858bc00aa58ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457421"
---
# <a name="m4x3---vs"></a>m4x3 - vs

Moltiplica un vettore a 4 componenti per una matrice 4x3.

## <a name="syntax"></a>Sintassi



| m4x3 dst, src0, src1 |
|----------------------|



 

dove

-   dst è il registro di destinazione. Il risultato è un vettore a 3 componenti.
-   src0 è un registro di origine che rappresenta un vettore a 4 componenti.
-   src1 è un registro di origine che rappresenta una matrice 4x3, che corrisponde al primo di 3 registri consecutivi.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| m4x3                   | x    | x    | x    | x     | x    | x     |



 

La maschera xyz è necessaria per il registro di destinazione. I modificatori di negazione e swizzle sono consentiti per src0, ma non per src1.

Nel frammento di codice seguente vengono illustrate le operazioni eseguite.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + (src0.w * src3.w);
```



Il vettore di input si trova nel registro src0. La matrice di input 4x3 si trova nel registro src1 e nei due registri successivi, come illustrato nell'espansione seguente. Viene prodotto un risultato 3D, lasciando inalterato l'altro elemento del registro di destinazione (dest.w).

Questa operazione viene comunemente usata per trasformare un vettore di posizione da una matrice che non ha alcun effetto proiettativo, ad esempio nelle trasformazioni dello spazio del modello. Questa istruzione viene implementata come coppia di prodotti punto, come illustrato di seguito.


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



I modificatori Swizzle e Negate non sono validi per il registro src1. Il registro dst e src0 non può essere lo stesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




