---
title: mad - vs
description: Moltiplica e aggiunge le origini.
ms.assetid: 059f0bf6-d143-4efc-b074-0ed026edb008
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a42a4f2d28ed8f0506909199b4c15c26ae3bc434ec250ddae9909ef53525583b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986401"
---
# <a name="mad---vs"></a>mad - vs

Moltiplica e aggiunge le origini.

## <a name="syntax"></a>Sintassi



| mad dst, src0, src1, src2 |
|---------------------------|



 

dove

-   dst è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.
-   src2 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| matto                    | x    | x    | x    | x     | x    | x     |



 

Nel frammento di codice seguente vengono illustrate le operazioni eseguite.


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




