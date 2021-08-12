---
title: sub - ps
description: Sottrae le origini. | sub - ps
ms.assetid: e130724f-63bf-4d7f-bc9f-6a4441a788b8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5fc4faa24f95824a77e9a1e92b9a15479d2e509212c52c9309c38fcc42cf6b3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285719"
---
# <a name="sub---ps"></a>sub - ps

Sottrae le origini.

## <a name="syntax"></a>Sintassi



| sub dst, src0, src1 |
|---------------------|



 

dove

-   dst è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| sub                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Questa istruzione esegue la sottrazione illustrata in questa formula.


```
dest = src0 - src1
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




