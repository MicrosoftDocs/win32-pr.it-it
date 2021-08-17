---
title: m4x4 - ps
description: Moltiplica un vettore a 4 componenti per una matrice 4x4. | m4x4 - ps
ms.assetid: 2a9915a3-f396-4108-97f7-d70c5262ff59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f7dfba3713bcd376c369a17d4856b64965e2e83c22ff03b282d4c9880d6c8700
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906860"
---
# <a name="m4x4---ps"></a>m4x4 - ps

Moltiplica un vettore a 4 componenti per una matrice 4x4.

## <a name="syntax"></a>Sintassi



| m4x4 dst, src0, src1 |
|----------------------|



 

dove

-   dst è il registro di destinazione. Il risultato è un vettore a 4 componenti.
-   src0 è un registro di origine che rappresenta un vettore a 4 componenti.
-   src1 è un registro di origine che rappresenta una matrice 4x4, che corrisponde al primo di 4 registri consecutivi.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m4x4                  |      |      |      |      | x    | x    | x     | x    | x     |



 

La maschera xyzw (predefinita) è obbligatoria per il registro di destinazione. I modificatori di negazione e swizzle sono consentiti per src0, ma non per src1.

I modificatori Swizzle e Negate non sono validi per il registro src0. I registri dst e src0 non possono essere uguali.

Il frammento di codice seguente illustra le operazioni eseguite.


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z) + (src0.w*src4.w);
```



Il vettore di input si trova nel registro src0. La matrice di input 4x4 si trova nel registro src1 e nei tre registri successivi superiori, come illustrato nell'espansione seguente.

Questa operazione viene in genere usata per trasformare una posizione in base a una matrice di proiezione. Questa istruzione viene implementata come set di prodotti punto, come illustrato di seguito.


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




