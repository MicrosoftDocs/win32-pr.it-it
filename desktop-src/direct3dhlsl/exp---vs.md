---
title: exp - vs
description: Fornisce una precisione completa esponenziale 2x. | exp - vs
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2b5b27067e83cbfd7604165ec1191d3371634aac15781a719377c92c69e29e6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067951"
---
# <a name="exp---vs"></a>exp - vs

Fornisce una precisione completa esponenziale di 2<sup>x</sup>.

## <a name="syntax"></a>Sintassi



| exp dst, src |
|--------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito dello swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti .x, .y, .z, .w swizzle (o .r, .g, .b, .a equivalents). Vedere [Source Register Swizzling ( Swizzling del registro di origine).](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md)

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| exp                    | x    | x    | x    | x     | x    | x     |



 

Questa istruzione fornisce almeno 21 bit di precisione.

Il frammento di codice seguente illustra le operazioni eseguite:


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




