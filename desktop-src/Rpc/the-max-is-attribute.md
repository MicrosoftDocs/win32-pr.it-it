---
title: Attributo max_is
description: È possibile specificare i limiti validi dei numeri di indice di una matrice usando l'attributo \ Max \_ is \.
ms.assetid: b629e3cf-544d-47ee-8f8f-b049f693897c
keywords:
- max_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8901f952a55de6b81143b0e615c878d8599fb354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104224006"
---
# <a name="the-max_is-attribute"></a><span data-ttu-id="00367-104">\[Attributo max \_ is \]</span><span class="sxs-lookup"><span data-stu-id="00367-104">The \[max\_is\] Attribute</span></span>

<span data-ttu-id="00367-105">È possibile specificare i limiti validi dei numeri di indice di una matrice usando l'attributo \[ [**Max \_ is**](/windows/desktop/Midl/max-is) \] .</span><span class="sxs-lookup"><span data-stu-id="00367-105">You can specify the valid bounds of the index numbers of an array using the \[[**max\_is**](/windows/desktop/Midl/max-is)\] attribute.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(5.0)
]
interface arraytest
{
  void fArray5([in] short sMax,
               [in, out, max_is(sMax)]  char achArray[]);
}
```

 

 