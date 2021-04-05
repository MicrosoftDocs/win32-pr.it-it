---
title: Registrazione di una DLL di sicurezza RAS
description: Il programma di installazione di una DLL di sicurezza RAS deve registrare la DLL con il server RAS Windows NT/Windows 2000.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae856b33b2233ae114a281d96447719d9b2832
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709859"
---
# <a name="registering-a-ras-security-dll"></a><span data-ttu-id="92a2c-103">Registrazione di una DLL di sicurezza RAS</span><span class="sxs-lookup"><span data-stu-id="92a2c-103">Registering a RAS Security DLL</span></span>

<span data-ttu-id="92a2c-104">Il programma di installazione di una DLL di sicurezza RAS deve registrare la DLL con il server RAS Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="92a2c-104">The setup program for a RAS security DLL must register the DLL with the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="92a2c-105">È possibile registrare solo una DLL di sicurezza RAS perché non è disponibile il supporto per più DLL di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="92a2c-105">Only one RAS security DLL can be registered as support for multiple security DLLs is not provided.</span></span> <span data-ttu-id="92a2c-106">Per registrare una DLL di sicurezza RAS, impostare il valore *DllPath* nella chiave seguente del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="92a2c-106">To register a RAS security DLL, set the *DLLPath* value under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| <span data-ttu-id="92a2c-107">Nome del valore</span><span class="sxs-lookup"><span data-stu-id="92a2c-107">Value name</span></span> | <span data-ttu-id="92a2c-108">Dati del valore</span><span class="sxs-lookup"><span data-stu-id="92a2c-108">Value data</span></span>                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92a2c-109">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="92a2c-109">*DLLPath*</span></span>  | <span data-ttu-id="92a2c-110">Stringa **reg \_ SZ** che contiene il percorso della dll.</span><span class="sxs-lookup"><span data-stu-id="92a2c-110">A **REG\_SZ** string that contains the path of the DLL.</span></span> <span data-ttu-id="92a2c-111">Questa stringa deve specificare il percorso completo, a meno che la DLL non si trovi in una directory elencata nel percorso di sistema.</span><span class="sxs-lookup"><span data-stu-id="92a2c-111">This string should specify the full path unless the DLL is in a directory listed in the system path.</span></span> |



 

<span data-ttu-id="92a2c-112">Anche il programma di installazione di una DLL di sicurezza RAS deve fornire la funzionalità di rimozione/disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="92a2c-112">The setup program for a RAS security DLL must also provide remove/uninstall functionality.</span></span> <span data-ttu-id="92a2c-113">Se un utente rimuove la DLL, il programma di installazione deve eliminare il valore *DllPath* dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="92a2c-113">If a user removes the DLL, the setup program must delete the *DLLPath* value from the registry.</span></span> <span data-ttu-id="92a2c-114">Il servizio RAS non viene avviato se il valore *DllPath* specifica una dll non trovata.</span><span class="sxs-lookup"><span data-stu-id="92a2c-114">The RAS service does not start if the *DLLPath* value specifies a DLL that cannot be found.</span></span>

<span data-ttu-id="92a2c-115">Una DLL di sicurezza RAS deve esportare le funzioni [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) e [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) .</span><span class="sxs-lookup"><span data-stu-id="92a2c-115">A RAS security DLL must export the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) and [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) functions.</span></span>

 

 




