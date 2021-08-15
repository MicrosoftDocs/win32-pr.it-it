---
title: m3x3 - vs
description: Moltiplica un vettore a 3 componenti per una matrice 3x3. | m3x3 - vs
ms.assetid: 6a749ed0-097d-4354-bc70-fbcd879eafab
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 11c1caa682751c3c4d112efd07643233e9cac91392c9e3bb9c575b1f89f5b53f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562061"
---
# <a name="m3x3---vs"></a>m3x3 - vs

Moltiplica un vettore a 3 componenti per una matrice 3x3.

## <a name="syntax"></a>Sintassi



| m3x3 dst, src0, src1 |
|----------------------|



 

dove

-   dst è il registro di destinazione. Il risultato è un vettore a 3 componenti.
-   src0 è un registro di origine che rappresenta un vettore a 3 componenti.
-   src1 è un registro di origine che rappresenta una matrice 3x3, che corrisponde al primo di 3 registri consecutivi.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| m3x3                   | x    | x    | x    | x     | x    | x     |



 

La maschera xyz è necessaria per il registro di destinazione. I modificatori di negazione e swizzle sono consentiti per src0 ma non per src1.

Nel frammento di codice seguente vengono illustrate le operazioni eseguite.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



Il vettore di input si trova nel registro src0. La matrice di input 3x3 si trova nel registro src1 e nei due registri successivi, come illustrato nell'espansione seguente. Viene prodotto un risultato 3D, lasciando inalterato l'altro elemento del registro di destinazione (dest.w).

Questa operazione viene comunemente usata per trasformare vettori normali durante i calcoli di illuminazione. Questa istruzione viene implementata come coppia di prodotti punto, come illustrato di seguito.


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




