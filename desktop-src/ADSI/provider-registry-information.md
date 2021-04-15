---
title: Informazioni del registro di sistema del provider
description: In questo argomento vengono illustrate le chiavi e i valori che è necessario impostare quando si aggiunge un provider ADSI.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790a80964bdcc6111a4c167056a0b85bda23e147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395278"
---
# <a name="provider-registry-information"></a><span data-ttu-id="8aa78-103">Informazioni del registro di sistema del provider</span><span class="sxs-lookup"><span data-stu-id="8aa78-103">Provider Registry Information</span></span>

<span data-ttu-id="8aa78-104">Il provider viene registrato con ADSI con le chiavi e i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8aa78-104">The provider is registered with ADSI with the following keys and values:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

<span data-ttu-id="8aa78-105">Il provider viene registrato con Windows con le chiavi e i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8aa78-105">The provider is registered with Windows with the following keys and values:</span></span>

```
HKEY_CLASSES_ROOT
   provider
      Clsid
         (Default) = <provider CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider DLL filename>
            ThreadingModel = Both
         ProgID = <provider object name>
         TypeLib = <provider TypeLib CLSID>
         Version = <provider version number>
```

<span data-ttu-id="8aa78-106">Lo spazio dei nomi del provider viene registrato con Windows con le chiavi e i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8aa78-106">The provider namespace is registered with Windows with the following keys and values:</span></span>

```
HKEY_CLASSES_ROOT
   provider namespace
      Clsid
         (Default) = <provider namespace CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider namespace CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider namespace DLL filename>
            ThreadingModel = Both
         ProgID = <provider namespace object name>
         TypeLib = <provider namespace TypeLib CLSID>
         Version = <provider namespace version number>
```

<span data-ttu-id="8aa78-107">Nei paragrafi precedenti, il *provider* è l'identificatore dell'oggetto di primo livello del provider.</span><span class="sxs-lookup"><span data-stu-id="8aa78-107">In the previous paragraphs, the *provider* is the identifier of the provider's top-level object.</span></span> <span data-ttu-id="8aa78-108">Lo *spazio dei nomi del provider* è l'identificatore dell'oggetto che implementa lo spazio dei nomi del provider.</span><span class="sxs-lookup"><span data-stu-id="8aa78-108">The *provider namespace* is the identifier of the object which implements the provider's namespace.</span></span>

<span data-ttu-id="8aa78-109">Per un esempio specifico, vedere [installazione del componente provider di esempio](installing-the-example-provider-component.md).</span><span class="sxs-lookup"><span data-stu-id="8aa78-109">For a specific example, see [Installing the Example Provider Component](installing-the-example-provider-component.md).</span></span>

 

 




