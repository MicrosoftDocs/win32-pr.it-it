---
title: LRP-PS
description: Esegue l'interpolazione lineare tra il secondo e il terzo registro di origine in base a una proporzione specificata nel primo registro di origine. | LRP-PS
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aec1ac23cc6c86f768d435e4c8169117c1bbe899
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058568"
---
# <a name="lrp---ps"></a>LRP-PS

Esegue l'interpolazione lineare tra il secondo e il terzo registro di origine in base a una proporzione specificata nel primo registro di origine.

## <a name="syntax"></a>Sintassi



| LRP DST, src0, src1, src2 |
|---------------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.
-   src2 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| LRP                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Questa istruzione esegue l'interpolazione lineare in base alla formula seguente.


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




