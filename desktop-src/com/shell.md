---
title: Shell (COM)
description: Fornisce informazioni sulla stampa della shell di Windows 3,1 e sui file aperti.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- Chiave del registro di sistema shell COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739346"
---
# <a name="shell-com"></a><span data-ttu-id="c618c-104">Shell (COM)</span><span class="sxs-lookup"><span data-stu-id="c618c-104">Shell (COM)</span></span>

<span data-ttu-id="c618c-105">Fornisce informazioni sulla stampa della shell di Windows 3,1 e sui **file aperti** .</span><span class="sxs-lookup"><span data-stu-id="c618c-105">Provides Windows 3.1 shell printing and **File Open** information.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c618c-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c618c-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Shell
         Open
            command = path %1
         Print
            command = path %1
```

## <a name="remarks"></a><span data-ttu-id="c618c-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c618c-107">Remarks</span></span>

<span data-ttu-id="c618c-108">Queste voci devono fornire il percorso e il nome file dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c618c-108">These entries should provide the path and file name of the application.</span></span>

 

 




