---
title: log - ps
description: Logodato di precisione completa(x). | log - ps
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4be7061b6e2e0bfa4fd86ffaeef1651cd114996bb9252192582f4c447aac09ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854151"
---
# <a name="log---ps"></a>log - ps

Logodato di precisione completa(x).

## <a name="syntax"></a>Sintassi



| log dst, src |
|--------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito dello swizzle di replica. ovvero è necessario specificare esattamente uno dei componenti .x, .y, .z, .w swizzle (o .r, .g, .b, .a equivalents).

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| log                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Il frammento di codice seguente illustra le operazioni eseguite.


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



Questa istruzione accetta un'origine scalare il cui bit di segno viene ignorato. Il risultato viene replicato in tutti e quattro i canali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




