---
description: Windows carica ed esegue la DLL standard di Microsoft GINA (MSGina.dll). Per caricare un'altra GINA, è necessario modificare un valore della chiave del registro di sistema.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Caricamento ed esecuzione di una DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6242ac0124d85d280d951cbc0bfbdbe748fde0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313288"
---
# <a name="loading-and-running-a-gina-dll"></a><span data-ttu-id="5f22f-104">Caricamento ed esecuzione di una DLL GINA</span><span class="sxs-lookup"><span data-stu-id="5f22f-104">Loading and Running a GINA DLL</span></span>

<span data-ttu-id="5f22f-105">Windows carica ed esegue la DLL standard di Microsoft GINA (MSGina.dll).</span><span class="sxs-lookup"><span data-stu-id="5f22f-105">Windows loads and executes the standard Microsoft GINA DLL (MSGina.dll).</span></span> <span data-ttu-id="5f22f-106">Per caricare un'altra [*Gina*](../secgloss/g-gly.md), è necessario modificare il valore della chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="5f22f-106">To load a different [*GINA*](../secgloss/g-gly.md), you must alter the following registry key value:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

<span data-ttu-id="5f22f-107">Se il valore della chiave GinaDLL è presente, deve contenere il nome di una DLL GINA, che verrà caricata e utilizzata da [*Winlogon*](../secgloss/w-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5f22f-107">If the GinaDLL key value is present, it must contain the name of a GINA DLL, which [*Winlogon*](../secgloss/w-gly.md) will load and use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f22f-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f22f-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f22f-109">Compilazione e test di una DLL GINA</span><span class="sxs-lookup"><span data-stu-id="5f22f-109">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="5f22f-110">Funzioni di esportazione GINA</span><span class="sxs-lookup"><span data-stu-id="5f22f-110">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="5f22f-111">Strutture GINA</span><span class="sxs-lookup"><span data-stu-id="5f22f-111">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="5f22f-112">Funzioni di Servizi terminal GINA</span><span class="sxs-lookup"><span data-stu-id="5f22f-112">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
