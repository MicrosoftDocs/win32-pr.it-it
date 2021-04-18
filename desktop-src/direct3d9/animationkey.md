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
# <a name="animationkey"></a><span data-ttu-id="f5c82-104">AnimationKey</span><span class="sxs-lookup"><span data-stu-id="f5c82-104">AnimationKey</span></span>

<span data-ttu-id="f5c82-105">Definisce un set di chiavi di animazione.</span><span class="sxs-lookup"><span data-stu-id="f5c82-105">Defines a set of animation keys.</span></span> <span data-ttu-id="f5c82-106">Una chiave matrice è utile per set di dati di animazione che devono essere rappresentati come matrici di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="f5c82-106">A matrix key is useful for sets of animation data that need to be represented as transformation matrices.</span></span>

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

<span data-ttu-id="f5c82-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="f5c82-107">Where:</span></span>

-   <span data-ttu-id="f5c82-108">Tipo di chiave-specifica se le chiavi sono rotazione, scala, posizione o chiavi della matrice (usando rispettivamente i numeri interi 0, 1, 2 o 3).</span><span class="sxs-lookup"><span data-stu-id="f5c82-108">keyType - Specifies whether the keys are rotation, scale, position, or matrix keys (using the integers 0, 1, 2, or 3, respectively).</span></span>
-   <span data-ttu-id="f5c82-109">nKeys: numero di chiavi.</span><span class="sxs-lookup"><span data-stu-id="f5c82-109">nKeys - Number of keys.</span></span>
-   <span data-ttu-id="f5c82-110">chiavi: matrice di chiavi.</span><span class="sxs-lookup"><span data-stu-id="f5c82-110">keys - An array of keys.</span></span> <span data-ttu-id="f5c82-111">Vedere [**TimedFloatKeys**](timedfloatkeys.md).</span><span class="sxs-lookup"><span data-stu-id="f5c82-111">See [**TimedFloatKeys**](timedfloatkeys.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f5c82-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5c82-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c82-113">Modelli</span><span class="sxs-lookup"><span data-stu-id="f5c82-113">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



