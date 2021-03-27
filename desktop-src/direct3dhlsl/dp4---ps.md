---
title: DP4-PS
description: Calcola il prodotto del punto a quattro componenti dei registri di origine. | DP4-PS
ms.assetid: 83ef6097-cacf-4498-842b-3eb03e57bd6f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2562259af164b8680d54e9a120abaa405fd781c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058524"
---
# <a name="dp4---ps"></a>DP4-PS

Calcola il prodotto del punto a quattro componenti dei registri di origine.

## <a name="syntax"></a>Sintassi



| DP4 DST, src0, src1 |
|---------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DP4                   |      | x    | x    | x    | x    | x    | x     | x    | x     |



 

Il frammento di codice seguente mostra le operazioni eseguite:


```
dest.x = dest.y = dest.z = dest.w = 
    (src0.x * src1.x) + (src0.y * src1.y) + 
    (src0.z * src1.z) + (src0.w * src1.w);
```



Limitazioni per PS \_ 1 \_ 2 e PS \_ 1 \_ 3:

-   Ogni shader può utilizzare fino a un massimo di quattro istruzioni DP4.
-   Ogni istruzione DP4 viene conteggiata come due istruzioni aritmetiche.

Limitazioni per le \_ versioni 1 X:

-   Questa istruzione non può essere rilasciata perché DP4 viene eseguito sia nella pipeline vettoriale che in quella alfa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




