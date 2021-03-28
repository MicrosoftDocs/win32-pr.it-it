---
title: M3x4-PS
description: Moltiplica un vettore a 3 componenti per una matrice 3x4. | M3x4-PS
ms.assetid: b749d3cd-2acf-450c-94f2-fea5e1c8f4d2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c245f4765853301a7c8319c8038b9ed342e3715
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981959"
---
# <a name="m3x4---ps"></a>M3x4-PS

Moltiplica un vettore a 3 componenti per una matrice 3x4.

## <a name="syntax"></a>Sintassi



| M3x4 DST, src0, src1 |
|----------------------|



 

dove

-   DST è il registro di destinazione. Result è un vettore a 4 componenti.
-   src0 è un registro di origine che rappresenta un vettore a 3 componenti.
-   src1 è un registro di origine che rappresenta una matrice 3x4, che corrisponde al primo di 4 registri consecutivi.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x4                  |      |      |      |      | x    | x    | x     | x    | x     |



 

Per il registro di destinazione è richiesta la maschera xyzw (impostazione predefinita). I modificatori negate e swizzle sono consentiti per src0 ma non per src1.

Il frammento di codice seguente mostra le operazioni eseguite.


```
 
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z);
```



Il vettore di input si trova in Register src0. La matrice di input 3x4 si trova nel registro src1 e i successivi due registri superiori, come illustrato nell'espansione riportata di seguito.

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

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




