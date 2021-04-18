---
title: " undef"
description: La direttiva \ undef rimuove la definizione corrente del nome specificato. Tutte le occorrenze successive del nome vengono elaborate senza sostituzione.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298243"
---
# <a name="undef"></a><span data-ttu-id="208db-104">\#undef</span><span class="sxs-lookup"><span data-stu-id="208db-104">\#undef</span></span>

<span data-ttu-id="208db-105">La direttiva **\# undef** rimuove la definizione corrente del nome specificato.</span><span class="sxs-lookup"><span data-stu-id="208db-105">The **\#undef** directive removes the current definition of the specified name.</span></span> <span data-ttu-id="208db-106">Tutte le occorrenze successive del nome vengono elaborate senza sostituzione.</span><span class="sxs-lookup"><span data-stu-id="208db-106">All subsequent occurrences of the name are processed without replacement.</span></span>

``` syntax
#undef name
```

<dl> <dt>

<span data-ttu-id="208db-107"><span id="name"></span><span id="NAME"></span>*nome*</span><span class="sxs-lookup"><span data-stu-id="208db-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="208db-108">Nome da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="208db-108">Name to be removed.</span></span> <span data-ttu-id="208db-109">Questo valore è costituito da qualsiasi combinazione di lettere, cifre e punteggiatura valida per il preprocessore C/C++.</span><span class="sxs-lookup"><span data-stu-id="208db-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="208db-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="208db-110">Example</span></span>

<span data-ttu-id="208db-111">In questo esempio vengono rimosse le definizioni per i nomi diversi da zero e USERCLASS:</span><span class="sxs-lookup"><span data-stu-id="208db-111">This example removes the definitions for the names nonzero and USERCLASS:</span></span>

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a><span data-ttu-id="208db-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="208db-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="208db-113">Direttive per il preprocessore</span><span class="sxs-lookup"><span data-stu-id="208db-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




