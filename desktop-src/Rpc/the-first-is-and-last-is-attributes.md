---
title: Attributi first_is e last_is
description: È possibile determinare il numero di elementi trasmessi specificando il primo e l'ultimo elemento.
ms.assetid: bd4dcf42-64a7-4b05-ac55-be77c381eb2e
keywords:
- first_is
- last_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16c30c2e7e6689ba2a61f7f5e694a5b29f39af5cadcf7fa2ca2f51e14e1f3457
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017141"
---
# <a name="the-first_is-and-last_is-attributes"></a>Il \[ primo è e \_ \] \[ \_ l'ultimo è \] Attributes

È possibile determinare il numero di elementi trasmessi specificando il primo e l'ultimo elemento. Usare il \[ [**primo attributo \_ è**](/windows/desktop/Midl/first-is) \] e \[ [**\_ l'ultimo è**](/windows/desktop/Midl/last-is) , come illustrato di \] seguito:

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

 

 