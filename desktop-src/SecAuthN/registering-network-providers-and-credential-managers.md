---
description: Dopo aver creato il provider di rete o Gestione credenziali, è necessario registrarlo nel sistema.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Registrazione di provider di rete e gestori di credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de34c97b61f685c3e779bd487fbc2c5b21fa7af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231841"
---
# <a name="registering-network-providers-and-credential-managers"></a><span data-ttu-id="42248-103">Registrazione di provider di rete e gestori di credenziali</span><span class="sxs-lookup"><span data-stu-id="42248-103">Registering Network Providers and Credential Managers</span></span>

<span data-ttu-id="42248-104">Dopo aver creato il provider di rete o Gestione credenziali, è necessario registrarlo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="42248-104">After you have created your network provider or credential manager, you must register it with the system.</span></span> <span data-ttu-id="42248-105">Questa operazione è necessaria per consentire a MPR di sapere quali provider di rete sono installati.</span><span class="sxs-lookup"><span data-stu-id="42248-105">This is necessary so the MPR will know what network providers are installed.</span></span> <span data-ttu-id="42248-106">All'avvio di MPR, viene verificato il registro di sistema e vengono caricati i provider di rete o i gestori di credenziali trovati.</span><span class="sxs-lookup"><span data-stu-id="42248-106">When the MPR starts, it checks the registry and loads any network providers or credential managers it finds.</span></span>

<span data-ttu-id="42248-107">Poiché i provider di rete e i gestori di credenziali sono correlati, vengono registrati nelle stesse sottochiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="42248-107">Because network providers and credential managers are related, they are registered in the same subkeys of the registry.</span></span> <span data-ttu-id="42248-108">Di fatto, le dll del provider di rete possono anche essere gestori di credenziali.</span><span class="sxs-lookup"><span data-stu-id="42248-108">In fact, network provider DLLs can also be credential managers.</span></span>

<span data-ttu-id="42248-109">Per informazioni dettagliate sulle chiavi del registro di sistema che è necessario creare per il provider di rete o Gestione credenziali, vedere [autenticazione delle chiavi del registro](authentication-registry-keys.md)di sistema.</span><span class="sxs-lookup"><span data-stu-id="42248-109">For detailed information about the registry keys you should create for your network provider or credential manager, see [Authentication Registry Keys](authentication-registry-keys.md).</span></span>

 

 



