---
title: m3x2 - ps
description: Moltiplica un vettore a 3 componenti per una matrice 3x2. | m3x2 - ps
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59bf908a2858e46f9c1e339db32d3e6e57062bc280b8223a9fcb66a527380773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672641"
---
# <a name="m3x2---ps"></a>m3x2 - ps

Moltiplica un vettore a 3 componenti per una matrice 3x2.

## <a name="syntax"></a>Sintassi



| m3x2 dst, src0, src1 |
|----------------------|



 

dove

-   dst è il registro di destinazione. Il risultato è un vettore a 2 componenti.
-   src0 è un registro di origine che rappresenta un vettore a 3 componenti.
-   src1 è un registro di origine che rappresenta una matrice 3x2, che corrisponde al primo di 2 registri consecutivi.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x2                  |      |      |      |      | x    | x    | x     | x    | x     |



 

La maschera xy è necessaria per il registro di destinazione. I modificatori di negazione e swizzle sono consentiti per src0 ma non per src1.

Le equazioni seguenti illustrano il funzionamento dell'istruzione :


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



Il vettore di input si trova nel registro src0. La matrice di input 3x2 si trova nel registro src1 e nel registro superiore successivo nello stesso file di registro, come illustrato nell'espansione seguente. Viene prodotto un risultato 2D, lasciando inalterati gli altri elementi del registro di destinazione (dest.z e dest.w).

Questa operazione viene comunemente usata per le trasformazioni 2D. Questa istruzione viene implementata come coppia di prodotti punto, come illustrato di seguito.


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



I modificatori Swizzle e Negate non sono validi per il registro src1. I registri dst e src0 o uno qualsiasi dei registri src1+i non possono essere uguali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




