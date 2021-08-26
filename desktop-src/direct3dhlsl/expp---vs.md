---
title: expp - vs
description: Fornisce una precisione parziale esponenziale 2x.
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e8717edc045f50cc572d675dbec405b01fda49503349e9716210dfcae23fb277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982451"
---
# <a name="expp---vs"></a>expp - vs

Fornisce una precisione parziale esponenziale di 2<sup>x</sup>.

## <a name="syntax"></a>Sintassi



| expp dst, src. {x\|y\|z\|w} |
|----------------------------|



 

Dove:

-   dst è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito dello swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti .x, .y, .z, .w swizzle (o .r, .g, .b, .a equivalents).
-   {x \| y \| z \| w} è lo swizzle di replica richiesto nel registro di origine.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| expp                   | x    | x    | x    | x     | x    | x     |



 

### <a name="vs_1_1"></a>vs \_ 1 \_ 1

[L'istruzione exp - vs](exp---vs.md) funziona in modo diverso a seconda delle versioni del vertex shader.

In vs \_ 1 \_ 1, l'istruzione expp restituisce i risultati seguenti:


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



In vs \_ 2 \_ 0 e versione successiva, l'istruzione expp restituisce i risultati seguenti:


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a>vs \_ 2 \_ 0

In vs \_ 2 \_ 0 e versione successiva, l'istruzione funziona nel modo seguente:


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



L'istruzione fornisce almeno 10 bit di precisione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




