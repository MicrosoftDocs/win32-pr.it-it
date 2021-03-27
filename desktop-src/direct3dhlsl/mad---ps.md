---
title: MAD-PS
description: Moltiplicare e aggiungere istruzioni. Imposta il registro di destinazione su (src0 \ src1) + src2.
ms.assetid: 0bcf5dcc-3657-4ee0-9aeb-bd2d8feea7a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3570f5826f91b35b07478e1ea34940a27d706cf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398258"
---
# <a name="mad---ps"></a>MAD-PS

Moltiplicare e aggiungere istruzioni. Imposta il registro di destinazione su (src0 \* src1) + src2.

## <a name="syntax"></a>Sintassi



| MAD DST, src0, src1, src2 |
|---------------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.
-   src2 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| pazzo                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Il frammento di codice seguente mostra le operazioni eseguite.


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




