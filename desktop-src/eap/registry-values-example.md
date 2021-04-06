---
title: Esempio di valori del registro di sistema
description: Nell'esempio seguente vengono mostrati i dati possibili per alcuni valori del registro di sistema del protocollo di autenticazione.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104046152"
---
# <a name="registry-values-example"></a><span data-ttu-id="d8c37-103">Esempio di valori del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="d8c37-103">Registry Values Example</span></span>

<span data-ttu-id="d8c37-104">Nell'esempio seguente vengono mostrati i dati possibili per alcuni valori del registro di sistema del protocollo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d8c37-104">The following example shows possible data for some of the authentication protocol registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| <span data-ttu-id="d8c37-105">Nome chiave</span><span class="sxs-lookup"><span data-stu-id="d8c37-105">Key Name</span></span>            | <span data-ttu-id="d8c37-106">Datatype</span><span class="sxs-lookup"><span data-stu-id="d8c37-106">Datatype</span></span>        | <span data-ttu-id="d8c37-107">Valore</span><span class="sxs-lookup"><span data-stu-id="d8c37-107">Value</span></span>                                  |
|---------------------|-----------------|----------------------------------------|
| <span data-ttu-id="d8c37-108">Percorso</span><span class="sxs-lookup"><span data-stu-id="d8c37-108">Path</span></span>                | <span data-ttu-id="d8c37-109">REG \_ Espandi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d8c37-109">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="d8c37-110">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="d8c37-110">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="d8c37-111">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d8c37-111">FriendlyName</span></span>        | <span data-ttu-id="d8c37-112">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d8c37-112">REG\_SZ</span></span>         | <span data-ttu-id="d8c37-113">Protocollo EAP di esempio</span><span class="sxs-lookup"><span data-stu-id="d8c37-113">Sample EAP Protocol</span></span>                    |
| <span data-ttu-id="d8c37-114">ConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="d8c37-114">ConfigUIPath</span></span>        | <span data-ttu-id="d8c37-115">REG \_ Espandi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d8c37-115">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="d8c37-116">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="d8c37-116">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="d8c37-117">IdentityPath</span><span class="sxs-lookup"><span data-stu-id="d8c37-117">IdentityPath</span></span>        | <span data-ttu-id="d8c37-118">REG \_ Espandi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d8c37-118">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="d8c37-119">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="d8c37-119">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="d8c37-120">InteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="d8c37-120">InteractiveUIPath</span></span>   | <span data-ttu-id="d8c37-121">REG \_ Espandi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d8c37-121">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="d8c37-122">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="d8c37-122">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="d8c37-123">RequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="d8c37-123">RequireConfigUI</span></span>     | <span data-ttu-id="d8c37-124">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="d8c37-124">REG\_DWORD</span></span>      | <span data-ttu-id="d8c37-125">1</span><span class="sxs-lookup"><span data-stu-id="d8c37-125">1</span></span>                                      |
| <span data-ttu-id="d8c37-126">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="d8c37-126">ConfigCLSID</span></span>         | <span data-ttu-id="d8c37-127">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d8c37-127">REG\_SZ</span></span>         | <span data-ttu-id="d8c37-128">{0000031A-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="d8c37-128">{0000031A-0000-0000-C000-000000000046}</span></span> |
| <span data-ttu-id="d8c37-129">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="d8c37-129">StandaloneSupported</span></span> | <span data-ttu-id="d8c37-130">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="d8c37-130">REG\_DWORD</span></span>      | <span data-ttu-id="d8c37-131">1</span><span class="sxs-lookup"><span data-stu-id="d8c37-131">1</span></span>                                      |



 

 

 




