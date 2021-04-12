---
title: InprocHandler
description: Specifica se un'applicazione utilizza un gestore personalizzato.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- InprocHandler chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c19089ece43496465351b44e9faa8793ba893
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396495"
---
# <a name="inprochandler"></a><span data-ttu-id="c034d-104">InprocHandler</span><span class="sxs-lookup"><span data-stu-id="c034d-104">InprocHandler</span></span>

<span data-ttu-id="c034d-105">Specifica se un'applicazione utilizza un gestore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c034d-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c034d-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c034d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="c034d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c034d-107">Remarks</span></span>

<span data-ttu-id="c034d-108">Si tratta di un valore **reg \_ SZ** che specifica il gestore personalizzato usato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c034d-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="c034d-109">Se non viene utilizzato un gestore personalizzato, la voce deve essere impostata su Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="c034d-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="c034d-110">Se un contenitore esegue una ricerca nel registro di sistema per un gestore personalizzato, la versione a 16 bit ha la priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c034d-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c034d-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c034d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c034d-112">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="c034d-112">**InprocHandler32**</span></span>](inprochandler32.md)
</dt> </dl>

 

 




