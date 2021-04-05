---
title: Configurazione del registro di sistema della DLL di amministrazione RAS
description: Il programma di installazione di una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo le informazioni riportate nella seguente chiave del registro di sistema.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aed28fc41334c161a11ce5575b6395c4bb5da5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516024"
---
# <a name="ras-administration-dll-registry-setup"></a><span data-ttu-id="60611-103">Configurazione del registro di sistema della DLL di amministrazione RAS</span><span class="sxs-lookup"><span data-stu-id="60611-103">RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="60611-104">Il programma di installazione di una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo le informazioni riportate nella seguente chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="60611-104">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="60611-105">Per registrare la DLL, impostare i valori seguenti in questa chiave.</span><span class="sxs-lookup"><span data-stu-id="60611-105">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="60611-106">Nome del valore</span><span class="sxs-lookup"><span data-stu-id="60611-106">Value name</span></span>    | <span data-ttu-id="60611-107">Dati del valore</span><span class="sxs-lookup"><span data-stu-id="60611-107">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="60611-108">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="60611-108">*DisplayName*</span></span> | <span data-ttu-id="60611-109">Stringa **reg \_ SZ** che contiene il nome visualizzato descrittivo della dll.</span><span class="sxs-lookup"><span data-stu-id="60611-109">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="60611-110">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="60611-110">*DLLPath*</span></span>     | <span data-ttu-id="60611-111">Stringa **reg \_ SZ** che contiene il percorso completo della dll.</span><span class="sxs-lookup"><span data-stu-id="60611-111">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="60611-112">Ad esempio, la voce del registro di sistema per una DLL di amministrazione RAS da una società fittizia denominata proelectro, Inc. potrebbe essere:</span><span class="sxs-lookup"><span data-stu-id="60611-112">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="60611-113">*DisplayName* : **reg \_ SZ** : dll amministratore RAS proelectron</span><span class="sxs-lookup"><span data-stu-id="60611-113">*DisplayName* : **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="60611-114">*DllPath* : **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="60611-114">*DLLPath* : **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="60611-115">Anche il programma di installazione di una DLL di amministrazione RAS deve fornire la funzionalità di rimozione/disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="60611-115">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="60611-116">Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del registro di sistema della DLL.</span><span class="sxs-lookup"><span data-stu-id="60611-116">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 




