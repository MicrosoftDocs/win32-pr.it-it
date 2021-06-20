---
title: Informazioni sull'installazione del Registro di sistema delle DLL di amministrazione RAS
description: Comprendere i requisiti per la registrazione di una DLL di amministrazione del servizio di accesso remoto (RAS) di terze parti con RAS. RAS supporta più DLL di amministrazione RAS.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- Amministrazione RAS RRAS, configurazione del Registro di sistema DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9a7b7c48422264a890a74b1bab36e61672f11d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406664"
---
# <a name="about-ras-administration-dll-registry-setup"></a><span data-ttu-id="2be47-105">Informazioni sull'installazione del Registro di sistema delle DLL di amministrazione RAS</span><span class="sxs-lookup"><span data-stu-id="2be47-105">About RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="2be47-106">Il programma di installazione per una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo informazioni nella chiave seguente nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2be47-106">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="2be47-107">Per registrare la DLL, impostare i valori seguenti in questa chiave.</span><span class="sxs-lookup"><span data-stu-id="2be47-107">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="2be47-108">Nome del valore</span><span class="sxs-lookup"><span data-stu-id="2be47-108">Value name</span></span>    | <span data-ttu-id="2be47-109">Dati del valore</span><span class="sxs-lookup"><span data-stu-id="2be47-109">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="2be47-110">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="2be47-110">*DisplayName*</span></span> | <span data-ttu-id="2be47-111">Stringa **REG \_ SZ** che contiene il nome visualizzato descrittivo della DLL.</span><span class="sxs-lookup"><span data-stu-id="2be47-111">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="2be47-112">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="2be47-112">*DLLPath*</span></span>     | <span data-ttu-id="2be47-113">Stringa **REG \_ SZ** che contiene il percorso completo della DLL.</span><span class="sxs-lookup"><span data-stu-id="2be47-113">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="2be47-114">Poiché RAS supporta più DLL di amministrazione RAS, il valore **dllPath** del Registro di sistema può contenere un elenco di percorsi delimitato da punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="2be47-114">Because RAS supports multiple RAS Administration DLLs, the registry value **DLLPath** can contain a semi-colon delimited list of paths.</span></span> <span data-ttu-id="2be47-115">Ad esempio, la voce del Registro di sistema per una DLL di amministrazione RAS di una società fittizia denominata ProElectron, Inc., potrebbe essere la seguente:</span><span class="sxs-lookup"><span data-stu-id="2be47-115">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc., might be the following:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="2be47-116">*DisplayName*: **REG \_ SZ** : PROElectron RAS Admin DLL</span><span class="sxs-lookup"><span data-stu-id="2be47-116">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="2be47-117">*DLLPath*: **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll; C: \\ nt \\ system32 \\ntwkadm2.dll</span><span class="sxs-lookup"><span data-stu-id="2be47-117">*DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll; C:\\nt\\system32\\ntwkadm2.dll</span></span>

<span data-ttu-id="2be47-118">RAS chiama le DLL nell'ordine in cui sono elencate in questo valore del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2be47-118">RAS calls the DLLs in the order in which they are listed in this registry value.</span></span> <span data-ttu-id="2be47-119">Il valore del Registro di sistema *DisplayName* contiene ancora un solo nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="2be47-119">The registry value *DisplayName* still contains only a single display name.</span></span>

<span data-ttu-id="2be47-120">Anche il programma di installazione per una DLL di amministrazione RAS deve fornire funzionalità di rimozione e disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="2be47-120">The setup program for a RAS administration DLL must also provide remove and uninstall functionality.</span></span> <span data-ttu-id="2be47-121">Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del Registro di sistema per la DLL.</span><span class="sxs-lookup"><span data-stu-id="2be47-121">If a user removes the DLL, the setup program must delete the registry entries for the DLL.</span></span>

<span data-ttu-id="2be47-122">**Windows 2000/NT:** RAS supporta una sola DLL di amministrazione RAS, quindi il valore del Registro di sistema **DLLPath** non può contenere un elenco di percorsi delimitato da punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="2be47-122">**Windows 2000/NT:** RAS supports only one RAS Administration DLL, so the registry value **DLLPath** cannot contain a semi-colon delimited list of paths.</span></span>

 

 




