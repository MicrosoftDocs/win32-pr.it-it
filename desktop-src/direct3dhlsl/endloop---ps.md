---
title: endloop - ps
description: Fine di un ciclo - ps... blocco endloop.
ms.assetid: 8d05d0b3-88d2-44e3-a22d-54d8a8ceb5f4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b35daa5ca00db04b6e69dc70dd1a07aaf1287c2f9188819d5b65af9773edfe1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982491"
---
# <a name="endloop---ps"></a>endloop - ps

Fine di un [ciclo - ps](loop---ps.md)... blocco endloop.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| endloop               |      |      |      |      |      |      |       | x    | x     |



 

endloop deve seguire l'ultima istruzione di [un ciclo - blocco ps.](loop---ps.md)

## <a name="example"></a>Esempio


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




