---
description: Definisce un set di chiavi di animazione. Una chiave matrice è utile per set di dati di animazione che devono essere rappresentati come matrici di trasformazione.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05728f124ae01962a1291547f8fe8b7fcebd175a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305059"
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

-   Tipo di chiave-specifica se le chiavi sono rotazione, scala, posizione o chiavi della matrice (usando rispettivamente i numeri interi 0, 1, 2 o 3).
-   nKeys: numero di chiavi.
-   chiavi: matrice di chiavi. Vedere [**TimedFloatKeys**](timedfloatkeys.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



