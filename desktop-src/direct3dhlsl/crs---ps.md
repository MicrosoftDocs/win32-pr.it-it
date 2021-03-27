---
title: CRS-PS
description: Calcola un prodotto incrociato usando la regola a destra. | CRS-PS
ms.assetid: 602fa7cc-4e2b-4d90-90d8-df00d5812c81
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6098c8bf01bf0d8cce886276c1d1081720ea667
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352566"
---
# <a name="crs---ps"></a>CRS-PS

Calcola un prodotto incrociato usando la regola a destra.

## <a name="syntax"></a>Sintassi



| CRS DST, src0, src1 |
|---------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| CRS                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Questa istruzione funziona come illustrato di seguito.


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



Alcune restrizioni sull'utilizzo:

-   src0 non può essere lo stesso registro di dest.
-   src1 non può essere lo stesso registro di dest.
-   il valore di src0 non può essere swizzle diverso da quello predefinito swizzle (xyzw).
-   il valore di src1 non può essere swizzle diverso da quello predefinito swizzle (xyzw).
-   il dest deve avere esattamente una delle sette maschere seguenti:. x \| . y \| . z \| . XY \| . xz \| . YZ \| . xyz.
-   il valore di dest deve essere un registro temporaneo.
-   il nome di destinazione non deve corrispondere a src0 o src1

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




