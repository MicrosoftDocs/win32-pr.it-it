---
title: Configurazione del Registro di sistema della DLL di amministrazione RAS
description: Comprendere i requisiti per la registrazione di una DLL di amministrazione del servizio di accesso remoto (RAS) di terze parti con RAS.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0af8e4b189de69f254429c18beb4756e01ad56
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406714"
---
# <a name="ras-administration-dll-registry-setup"></a><span data-ttu-id="d0985-103">Configurazione del Registro di sistema della DLL di amministrazione RAS</span><span class="sxs-lookup"><span data-stu-id="d0985-103">RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="d0985-104">Il programma di installazione per una DLL di amministrazione RAS di terze parti deve registrare la DLL con RAS fornendo informazioni nella chiave seguente nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d0985-104">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="d0985-105">Per registrare la DLL, impostare i valori seguenti in questa chiave.</span><span class="sxs-lookup"><span data-stu-id="d0985-105">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="d0985-106">Nome del valore</span><span class="sxs-lookup"><span data-stu-id="d0985-106">Value name</span></span>    | <span data-ttu-id="d0985-107">Dati del valore</span><span class="sxs-lookup"><span data-stu-id="d0985-107">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="d0985-108">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="d0985-108">*DisplayName*</span></span> | <span data-ttu-id="d0985-109">Stringa **REG \_ SZ** che contiene il nome visualizzato descrittivo della DLL.</span><span class="sxs-lookup"><span data-stu-id="d0985-109">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="d0985-110">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="d0985-110">*DLLPath*</span></span>     | <span data-ttu-id="d0985-111">Stringa **REG \_ SZ** che contiene il percorso completo della DLL.</span><span class="sxs-lookup"><span data-stu-id="d0985-111">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="d0985-112">Ad esempio, la voce del Registro di sistema per una DLL di amministrazione RAS di una società fittizia denominata ProElectron, Inc. potrebbe essere:</span><span class="sxs-lookup"><span data-stu-id="d0985-112">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="d0985-113">*DisplayName* : **REG \_ SZ** : PROElectron RAS Admin DLL</span><span class="sxs-lookup"><span data-stu-id="d0985-113">*DisplayName* : **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="d0985-114">*DLLPath* : **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="d0985-114">*DLLPath* : **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="d0985-115">Anche il programma di installazione per una DLL di amministrazione RAS deve fornire funzionalità di rimozione/disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="d0985-115">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="d0985-116">Se un utente rimuove la DLL, il programma di installazione deve eliminare le voci del Registro di sistema della DLL.</span><span class="sxs-lookup"><span data-stu-id="d0985-116">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 




