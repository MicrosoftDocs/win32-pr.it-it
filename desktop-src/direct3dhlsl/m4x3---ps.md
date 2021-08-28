---
title: m4x3 - ps
description: Moltiplica un vettore a 4 componenti per una matrice 4x3. | m4x3 - ps
ms.assetid: cf9ae4c3-6cdf-4c6f-b34c-0ebd3c8a4123
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e291c268aae4173cb3ace4fc00beb5f1a3aa9f0b3d335f80891a851bcab41b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982031"
---
# <a name="m4x3---ps"></a>m4x3 - ps

Moltiplica un vettore a 4 componenti per una matrice 4x3.

## <a name="syntax"></a>Sintassi



| m4x3 dst, src0, src1 |
|----------------------|



 

dove

-   dst è il registro di destinazione. Il risultato è un vettore a 3 componenti.
-   src0 è un registro di origine che rappresenta un vettore a 4 componenti.
-   src1 è un registro di origine che rappresenta una matrice 4x3, che corrisponde al primo dei 3 registri consecutivi.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m4x3                  |      |      |      |      | x    | x    | x     | x    | x     |



 

La maschera xyz è necessaria per il registro di destinazione. I modificatori negate e swizzle sono consentiti per src0, ma non per src1.

Il frammento di codice seguente illustra le operazioni eseguite.


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
```



Il vettore di input si trova nel registro src0. La matrice 4x3 di input si trova nel registro src1 e nei due registri successivi superiori, come illustrato nell'espansione seguente. Viene prodotto un risultato 3D, lasciando inalterato l'altro elemento del registro di destinazione (dest.w).

Questa operazione viene comunemente usata per trasformare un vettore di posizione da una matrice che non ha alcun effetto proiettativo, ad esempio si verifica nelle trasformazioni dello spazio del modello. Questa istruzione viene implementata come set di prodotti punto, come illustrato di seguito.


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



I modificatori Swizzle e negate non sono validi per il registro src1. Il registro dst e src0 non può essere lo stesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




