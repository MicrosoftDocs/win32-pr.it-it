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
# <a name="sspi-handles"></a><span data-ttu-id="22caa-103">Handle SSPI</span><span class="sxs-lookup"><span data-stu-id="22caa-103">SSPI Handles</span></span>

<span data-ttu-id="22caa-104">SSPI usa i tipi di handle e il puntatore seguenti a questi handle:</span><span class="sxs-lookup"><span data-stu-id="22caa-104">SSPI uses the following handle types and pointer to these handles:</span></span>

-   <span data-ttu-id="22caa-105">**SecHandle** e **PSecHandle**</span><span class="sxs-lookup"><span data-stu-id="22caa-105">**SecHandle** and **PSecHandle**</span></span>
-   <span data-ttu-id="22caa-106">**CredHandle** e **PCredHandle**</span><span class="sxs-lookup"><span data-stu-id="22caa-106">**CredHandle** and **PCredHandle**</span></span>
-   <span data-ttu-id="22caa-107">**CtxtHandle** e **PCtxtHandle**</span><span class="sxs-lookup"><span data-stu-id="22caa-107">**CtxtHandle** and **PCtxtHandle**</span></span>

<span data-ttu-id="22caa-108">I tipi di handle e i puntatori a questi tipi di handle sono definiti nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="22caa-108">These handle types and pointers to these handle types are defined as follows.</span></span>


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



 

 



