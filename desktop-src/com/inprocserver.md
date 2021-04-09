---
title: InprocServer
description: Specifica il percorso della DLL del server in-process.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- InprocServer chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955457"
---
# <a name="inprocserver"></a><span data-ttu-id="03973-104">InprocServer</span><span class="sxs-lookup"><span data-stu-id="03973-104">InprocServer</span></span>

<span data-ttu-id="03973-105">Specifica il percorso della DLL del server in-process.</span><span class="sxs-lookup"><span data-stu-id="03973-105">Specifies the path to the in-process server DLL.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="03973-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="03973-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a><span data-ttu-id="03973-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="03973-107">Remarks</span></span>

<span data-ttu-id="03973-108">La voce **InprocServer** è relativamente rara per le classi inseribili.</span><span class="sxs-lookup"><span data-stu-id="03973-108">The **InprocServer** entry is relatively rare for insertable classes.</span></span>

<span data-ttu-id="03973-109">I server in-process sono attualmente registrati usando la voce del registro di sistema **InprocServer** .</span><span class="sxs-lookup"><span data-stu-id="03973-109">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="03973-110">I server in-process a 32 e 64 bit devono usare la voce [**InprocServer32**](inprocserver32.md) .</span><span class="sxs-lookup"><span data-stu-id="03973-110">The 32-bit and 64-bit in-process servers should use the [**InprocServer32**](inprocserver32.md) entry.</span></span> <span data-ttu-id="03973-111">Se un contenitore esegue una ricerca nel registro di sistema per un server in-process, la versione a 16 bit ha la priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="03973-111">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03973-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03973-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03973-113">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="03973-113">**InprocServer32**</span></span>](inprocserver32.md)
</dt> </dl>

 

 




