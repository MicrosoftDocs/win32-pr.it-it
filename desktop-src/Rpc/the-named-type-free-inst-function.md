---
title: Funzione named_type_free_inst
description: Gli stub chiamano la \_ \_ funzione Inst gratuita del tipo denominato \_ per liberare la memoria associata al tipo trasmesso.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d3b5103572eb58e4311c65b0e1cff02e91f66f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709091"
---
# <a name="the-named_type_free_inst-function"></a><span data-ttu-id="1bfbc-104">\_ \_ Funzione Inst disponibile del tipo denominato \_</span><span class="sxs-lookup"><span data-stu-id="1bfbc-104">The named\_type\_free\_inst Function</span></span>

<span data-ttu-id="1bfbc-105">Gli stub chiamano la **funzione \_ \_ \_ inst gratuita del tipo denominato** per liberare la memoria associata al tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="1bfbc-105">The stubs call the **named\_type\_free\_inst** function to free memory associated with the transmitted type.</span></span> <span data-ttu-id="1bfbc-106">La funzione è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="1bfbc-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

<span data-ttu-id="1bfbc-107">Il parametro punta all'istanza del tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="1bfbc-107">The parameter points to the instance of the transmitted type.</span></span> <span data-ttu-id="1bfbc-108">Questo oggetto non deve essere liberato.</span><span class="sxs-lookup"><span data-stu-id="1bfbc-108">This object should not be freed.</span></span> <span data-ttu-id="1bfbc-109">Per una discussione su quando chiamare la funzione, vedere [l'argomento rappresentare \_ come attributo](the-represent-as-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="1bfbc-109">For a discussion on when to call the function, see [The represent\_as Attribute](the-represent-as-attribute.md).</span></span>

 

 




