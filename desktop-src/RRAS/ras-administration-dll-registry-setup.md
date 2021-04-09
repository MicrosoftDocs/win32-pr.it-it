---
title: Informazioni sulla configurazione del registro di sistema della DLL di amministrazione RAS
description: Il programma di installazione di una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo le informazioni riportate nella seguente chiave del registro di sistema.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- Amministrazione RAS RRAS, configurazione del registro di sistema DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf487f792a4add9ebf61e8f866b9f0577fb468d
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103857826"
---
# <a name="about-ras-administration-dll-registry-setup"></a><span data-ttu-id="4a407-104">Informazioni sulla configurazione del registro di sistema della DLL di amministrazione RAS</span><span class="sxs-lookup"><span data-stu-id="4a407-104">About RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="4a407-105">Il programma di installazione di una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo le informazioni riportate nella seguente chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4a407-105">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="4a407-106">Per registrare la DLL, impostare i valori seguenti in questa chiave.</span><span class="sxs-lookup"><span data-stu-id="4a407-106">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="4a407-107">Nome del valore</span><span class="sxs-lookup"><span data-stu-id="4a407-107">Value name</span></span>    | <span data-ttu-id="4a407-108">Dati del valore</span><span class="sxs-lookup"><span data-stu-id="4a407-108">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="4a407-109">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="4a407-109">*DisplayName*</span></span> | <span data-ttu-id="4a407-110">Stringa **reg \_ SZ** che contiene il nome visualizzato descrittivo della dll.</span><span class="sxs-lookup"><span data-stu-id="4a407-110">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="4a407-111">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="4a407-111">*DLLPath*</span></span>     | <span data-ttu-id="4a407-112">Stringa **reg \_ SZ** che contiene il percorso completo della dll.</span><span class="sxs-lookup"><span data-stu-id="4a407-112">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="4a407-113">Poiché RAS supporta più DLL di amministrazione RAS, il valore del registro di sistema **DllPath** può contenere un elenco delimitato da punti e virgola di percorsi.</span><span class="sxs-lookup"><span data-stu-id="4a407-113">Because RAS supports multiple RAS Administration DLLs, the registry value **DLLPath** can contain a semi-colon delimited list of paths.</span></span> <span data-ttu-id="4a407-114">Ad esempio, la voce del registro di sistema per una DLL di amministrazione RAS da una società fittizia denominata proelectro, Inc. potrebbe essere la seguente:</span><span class="sxs-lookup"><span data-stu-id="4a407-114">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc., might be the following:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="4a407-115">*DisplayName*: **reg \_ SZ** : dll amministratore RAS proelectron</span><span class="sxs-lookup"><span data-stu-id="4a407-115">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="4a407-116">*DllPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll; C: \\ NT \\ system32 \\ntwkadm2.dll</span><span class="sxs-lookup"><span data-stu-id="4a407-116">*DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll; C:\\nt\\system32\\ntwkadm2.dll</span></span>

<span data-ttu-id="4a407-117">RAS chiama le dll nell'ordine in cui sono elencate in questo valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4a407-117">RAS calls the DLLs in the order in which they are listed in this registry value.</span></span> <span data-ttu-id="4a407-118">Il valore del registro di sistema *DisplayName* contiene ancora un solo nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="4a407-118">The registry value *DisplayName* still contains only a single display name.</span></span>

<span data-ttu-id="4a407-119">Anche il programma di installazione di una DLL di amministrazione RAS deve fornire la funzionalità di rimozione e disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="4a407-119">The setup program for a RAS administration DLL must also provide remove and uninstall functionality.</span></span> <span data-ttu-id="4a407-120">Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del registro di sistema per la DLL.</span><span class="sxs-lookup"><span data-stu-id="4a407-120">If a user removes the DLL, the setup program must delete the registry entries for the DLL.</span></span>

<span data-ttu-id="4a407-121">**Windows 2000/NT:** RAS supporta solo una DLL di amministrazione RAS, quindi il valore del registro di sistema **DllPath** non può contenere un elenco delimitato da punti e virgola di percorsi.</span><span class="sxs-lookup"><span data-stu-id="4a407-121">**Windows 2000/NT:** RAS supports only one RAS Administration DLL, so the registry value **DLLPath** cannot contain a semi-colon delimited list of paths.</span></span>

 

 




