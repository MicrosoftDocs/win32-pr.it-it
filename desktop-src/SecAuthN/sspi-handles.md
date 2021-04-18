---
description: Elenca gli handle utilizzati dall'API SSPI.
ms.assetid: 94b622d0-7c04-4513-841f-0df9b5d49136
title: Handle SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e388633cfee0d0f0470e519bac124a0bd1c70fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316214"
---
# <a name="sspi-handles"></a>Handle SSPI

SSPI usa i tipi di handle e il puntatore seguenti a questi handle:

-   **SecHandle** e **PSecHandle**
-   **CredHandle** e **PCredHandle**
-   **CtxtHandle** e **PCtxtHandle**

I tipi di handle e i puntatori a questi tipi di handle sono definiti nel modo seguente.


```C++
typedef struct _SecHandle {
  ULONG_PTR       dwLower;
  ULONG_PTR       dwUpper;
} SecHandle, * PSecHandle;

typedef SecHandle    CredHandle;
typedef PSecHandle   PCredHandle;

typedef SecHandle    CtxtHandle;
typedef PSecHandle   PCtxtHandle;
```



 

 



