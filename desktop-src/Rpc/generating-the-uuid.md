---
title: Generazione dell'UUID
description: Il primo passaggio per la definizione dell'interfaccia consiste nell'usare l'utilità uuidgen per generare un identificatore univoco universale (UUID).
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- RPC (Remote Procedure Call), attività, generazione dell'UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e263bfe21c4a564106c0d6328c0de891c18bca1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856066"
---
# <a name="generating-the-uuid"></a><span data-ttu-id="7d17d-104">Generazione dell'UUID</span><span class="sxs-lookup"><span data-stu-id="7d17d-104">Generating the UUID</span></span>

<span data-ttu-id="7d17d-105">Il primo passaggio per la definizione dell'interfaccia consiste nell'usare l'utilità **uuidgen** per generare un identificatore univoco universale (UUID).</span><span class="sxs-lookup"><span data-stu-id="7d17d-105">The first step in defining the interface is to use the **uuidgen** utility to generate a universally unique identifier (UUID).</span></span> <span data-ttu-id="7d17d-106">Un UUID consente alle applicazioni client e server di identificarsi reciprocamente.</span><span class="sxs-lookup"><span data-stu-id="7d17d-106">A UUID enables the client and server applications identify each other.</span></span> <span data-ttu-id="7d17d-107">L'utilità **uuidgen** (Uuidgen.exe) viene installata automaticamente quando si installa Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="7d17d-107">The **uuidgen** utility (Uuidgen.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="7d17d-108">Il comando che segue genera un UUID e crea un file di modello denominato Hello. idl.</span><span class="sxs-lookup"><span data-stu-id="7d17d-108">The following command generates a UUID and creates a template file called Hello.idl.</span></span>

<span data-ttu-id="7d17d-109">**uuidgen/i/ohello.idl**</span><span class="sxs-lookup"><span data-stu-id="7d17d-109">**uuidgen /i /ohello.idl**</span></span>

<span data-ttu-id="7d17d-110">Il modello Hello. idl sarà simile al seguente (con un UUID diverso, ovviamente).</span><span class="sxs-lookup"><span data-stu-id="7d17d-110">Your hello.idl template will look like this (with a different UUID, of course).</span></span>

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




