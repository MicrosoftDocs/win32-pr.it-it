---
title: InprocHandler32
description: InprocHandler32 specifica se un'applicazione usa un gestore personalizzato nella chiave HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID registro di sistema.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- Chiave del Registro di sistema COM InprocHandler32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73a8b2577a554b0bb8b5ba5a851e630edbf90a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406004"
---
# <a name="inprochandler32"></a><span data-ttu-id="8d5db-104">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="8d5db-104">InprocHandler32</span></span>

<span data-ttu-id="8d5db-105">Specifica se un'applicazione usa un gestore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="8d5db-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="8d5db-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="8d5db-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="8d5db-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d5db-107">Remarks</span></span>

<span data-ttu-id="8d5db-108">Si tratta di **un \_ valore REG SZ** che specifica il gestore personalizzato usato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8d5db-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="8d5db-109">Se non viene usato un gestore personalizzato, la voce deve essere impostata su Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="8d5db-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="8d5db-110">Se un contenitore cerca nel Registro di sistema un gestore personalizzato, la versione a 16 bit ha la priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8d5db-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d5db-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d5db-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d5db-112">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="8d5db-112">**InprocHandler**</span></span>](inprochandler.md)
</dt> </dl>

 

 




