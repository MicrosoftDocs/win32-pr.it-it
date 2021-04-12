---
title: Attributi first_is e last_is
description: È possibile determinare il numero di elementi trasmessi specificando il primo e l'ultimo elemento.
ms.assetid: bd4dcf42-64a7-4b05-ac55-be77c381eb2e
keywords:
- first_is
- last_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159a2696db8e175f921b797176baaa8f3aa0263c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339047"
---
# <a name="the-first_is-and-last_is-attributes"></a>Il \[ primo \_ è \] e l' \[ ultimo \_ è \] Attributes

È possibile determinare il numero di elementi trasmessi specificando il primo e l'ultimo elemento. Usare la \[ [**prima \_**](/windows/desktop/Midl/first-is) \] e l' \[ [**Ultima \_**](/windows/desktop/Midl/last-is) è \] attribuite agli attributi, come illustrato:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(4.0)
]
interface arraytest
{

  void fArray4([in]               short sSize,
               [in]               short sLast,
               [in]               short sFirst,
               [in, 
                out,
                size_is(sSize),
                first_is(sFirst),
                last_is(sLast)]   char achArray[]) ;
}
```

 

 