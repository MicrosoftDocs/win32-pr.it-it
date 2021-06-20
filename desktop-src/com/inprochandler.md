---
title: InprocHandler
description: InprocHandler specifica se un'applicazione usa un gestore personalizzato nella chiave HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID del Registro di sistema.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- InprocHandler chiave del Registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404734"
---
# <a name="inprochandler"></a><span data-ttu-id="d2e3d-104">InprocHandler</span><span class="sxs-lookup"><span data-stu-id="d2e3d-104">InprocHandler</span></span>

<span data-ttu-id="d2e3d-105">Specifica se un'applicazione usa un gestore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d2e3d-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="d2e3d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="d2e3d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2e3d-107">Remarks</span></span>

<span data-ttu-id="d2e3d-108">Si tratta di **un valore \_ REG SZ** che specifica il gestore personalizzato usato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="d2e3d-109">Se non viene usato un gestore personalizzato, la voce deve essere impostata su Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="d2e3d-110">Se un contenitore cerca un gestore personalizzato nel Registro di sistema, la versione a 16 bit ha la priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2e3d-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d2e3d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2e3d-112">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="d2e3d-112">**InprocHandler32**</span></span>](inprochandler32.md)
</dt> </dl>

 

 




