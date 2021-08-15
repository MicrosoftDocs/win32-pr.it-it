---
description: Elenca gli handle usati dall'API SSPI.
ms.assetid: 94b622d0-7c04-4513-841f-0df9b5d49136
title: Handle SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38fadebea7ff6b32f0058106595718a24d589854a662ef7b504ce6d7e8e5bc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916970"
---
# <a name="sspi-handles"></a>Handle SSPI

SSPI usa i tipi di handle e il puntatore a questi handle seguenti:

-   **SecHandle** e **PSecHandle**
-   **CredHandle** e **PCredHandle**
-   **CtxtHandle** e **PCtxtHandle**

Questi tipi di handle e puntatori a questi tipi di handle sono definiti come segue.


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



 

 



