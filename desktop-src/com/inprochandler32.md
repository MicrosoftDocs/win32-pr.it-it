---
title: InprocHandler32
description: Specifica se un'applicazione utilizza un gestore personalizzato.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- InprocHandler32 chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c918669aa3de1c8cf2622e3caf4acc9ae18f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395531"
---
# <a name="inprochandler32"></a><span data-ttu-id="28492-104">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="28492-104">InprocHandler32</span></span>

<span data-ttu-id="28492-105">Specifica se un'applicazione utilizza un gestore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="28492-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="28492-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="28492-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="28492-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="28492-107">Remarks</span></span>

<span data-ttu-id="28492-108">Si tratta di un valore **reg \_ SZ** che specifica il gestore personalizzato usato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="28492-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="28492-109">Se non viene utilizzato un gestore personalizzato, la voce deve essere impostata su Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="28492-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="28492-110">Se un contenitore esegue una ricerca nel registro di sistema per un gestore personalizzato, la versione a 16 bit ha la priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="28492-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28492-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28492-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28492-112">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="28492-112">**InprocHandler**</span></span>](inprochandler.md)
</dt> </dl>

 

 




