---
title: M3X3-PS
description: Moltiplica un vettore a 3 componenti per una matrice 3x3. | M3X3-PS
ms.assetid: 71342e05-69a6-41f4-bafb-643f0ceb0a59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ac72acd2133c8b34393bdd1ab7de8aec1df4db5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981911"
---
# <a name="m3x3---ps"></a>M3X3-PS

Moltiplica un vettore a 3 componenti per una matrice 3x3.

## <a name="syntax"></a>Sintassi



| M3X3 DST, src0, src1 |
|----------------------|



 

dove

-   DST è il registro di destinazione. Result è un vettore a 3 componenti.
-   src0 è un registro di origine che rappresenta un vettore a 3 componenti.
-   src1 è un registro di origine che rappresenta una matrice 3x3, che corrisponde al primo di 3 registri consecutivi.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x3                  |      |      |      |      | x    | x    | x     | x    | x     |



 

La maschera XYZ è obbligatoria per il registro di destinazione. I modificatori negate e swizzle sono consentiti per src0 ma non per src1.

Il frammento di codice seguente mostra le operazioni eseguite.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



Il vettore di input si trova in Register src0. La matrice di input 3x3 si trova in Register src1 e i successivi due registri successivi, come illustrato nell'espansione riportata di seguito. Viene generato un risultato 3D, lasciando l'altro elemento del registro di destinazione (dest. w) non interessato.

Questa operazione viene in genere usata per trasformare i vettori normali durante i calcoli di illuminazione. Questa istruzione viene implementata come un set di prodotti punto, come illustrato di seguito.


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




