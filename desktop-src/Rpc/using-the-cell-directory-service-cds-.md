---
title: Uso del servizio directory delle celle (CDS)
description: Se si dispone di CDS, è possibile usarlo anziché Microsoft Locator.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- RPC (Remote Procedure Call), attività, uso del servizio directory delle celle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0029bf78308d6963d615daa04eaf87f3617ebbb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710582"
---
# <a name="using-the-cell-directory-service-cds"></a><span data-ttu-id="0e047-104">Uso del servizio directory delle celle (CDS)</span><span class="sxs-lookup"><span data-stu-id="0e047-104">Using the Cell Directory Service (CDS)</span></span>

<span data-ttu-id="0e047-105">Se si dispone di CDS, è possibile usarlo anziché Microsoft Locator.</span><span class="sxs-lookup"><span data-stu-id="0e047-105">If you have CDS, you can use it instead of Microsoft Locator.</span></span> <span data-ttu-id="0e047-106">Modificare le voci del registro di sistema come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="0e047-106">Change the registry entries as shown:</span></span>

``` syntax
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    NetworkAddress
 
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    Endpoint
```

<span data-ttu-id="0e047-107">La modifica di queste voci punterà a un computer gateway che esegue NSID.</span><span class="sxs-lookup"><span data-stu-id="0e047-107">Changing these entries will point to a gateway computer that is running the NSID.</span></span> <span data-ttu-id="0e047-108">Verrà usato come localizzatore master.</span><span class="sxs-lookup"><span data-stu-id="0e047-108">This will be used as the master locator.</span></span> <span data-ttu-id="0e047-109">In caso di arresto anomalo, non verrà cercata alcuna sostituzione.</span><span class="sxs-lookup"><span data-stu-id="0e047-109">In the event of a crash, there will be no search for a replacement.</span></span>

 

 




