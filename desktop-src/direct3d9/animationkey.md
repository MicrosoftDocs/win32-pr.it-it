---
description: Definisce un set di chiavi di animazione. Una chiave matrice è utile per set di dati di animazione che devono essere rappresentati come matrici di trasformazione.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bad23a6cc519b0b0525cd0dac1b488184b3bf91e99359e252f44dca435ace529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118806406"
---
# <a name="animationkey"></a>AnimationKey

Definisce un set di chiavi di animazione. Una chiave matrice è utile per set di dati di animazione che devono essere rappresentati come matrici di trasformazione.

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

Dove:

-   keyType: specifica se le chiavi sono chiavi di rotazione, scala, posizione o matrice (usando rispettivamente i numeri interi 0, 1, 2 o 3).
-   nKeys : numero di chiavi.
-   keys: matrice di chiavi. Vedere [**TimedFloatKeys**](timedfloatkeys.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



