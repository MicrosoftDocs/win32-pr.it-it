---
title: logp - vs
description: Logp e precisione parziale logp'(x).
ms.assetid: 8547ca8a-7bde-4e41-9e65-f7fcd65454c1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c33242ec23070a78e8adee159d35c19121dcc7c3dfe2c013c3d00adceb16477
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043779"
---
# <a name="logp---vs"></a>logp - vs

Logp e precisione parziale logp'(x).

## <a name="syntax"></a>Sintassi



| logp dst, src |
|---------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito di replicate swizzle, ovvero esattamente uno dei componenti .x, .y, .z, .w swizzle (o .r, .g, .b, .a equivalenti) deve essere specificato.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| logp                   | x    | x    | x    | x     | x    | x     |



 

Il frammento di codice seguente illustra le operazioni eseguite.


```
float f = abs(src);
if (f != 0)
    dest.x = dest.y = dest.z = dest.w = (float)(log(f)/log(2));
else
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;   
```



Questa istruzione fornisce una precisione parziale in base 2 del logaritmo, fino a 10 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




