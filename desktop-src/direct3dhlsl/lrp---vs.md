---
title: lrp - vs
description: Interpola in modo lineare tra il secondo e il terzo registro di origine in base a una proporzione specificata nel primo registro di origine. | lrp - vs
ms.assetid: 8438bcf3-9b00-4963-b2a3-54fd1c345961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d154f78b3e8ae5d3b7b8e553435d962ad3dbea9fe86f8dd772bf165c5eb542be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119185"
---
# <a name="lrp---vs"></a>lrp - vs

Interpola in modo lineare tra il secondo e il terzo registro di origine in base a una proporzione specificata nel primo registro di origine.

## <a name="syntax"></a>Sintassi



| lrp dst, src0, src1, src2 |
|---------------------------|



 

dove

-   dst è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.
-   src2 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Lrp                    |      | x    | x    | x     | x    | x     |



 

Questa istruzione esegue l'interpolazione lineare in base alla formula seguente.


```
dest.x = src0.x * (src1.x - src2.x) + src2.x;
dest.y = src0.y * (src1.y - src2.y) + src2.y;
dest.z = src0.z * (src1.z - src2.z) + src2.z;
dest.w = src0.w * (src1.w - src2.w) + src2.w;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




