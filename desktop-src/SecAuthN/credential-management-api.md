---
description: API di gestione delle credenziali
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: API di gestione delle credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cae5054d0a32f42616f2845dcf18ab71ad0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757289"
---
# <a name="credential-management-api"></a><span data-ttu-id="7e14a-103">API di gestione delle credenziali</span><span class="sxs-lookup"><span data-stu-id="7e14a-103">Credential Management API</span></span>

<span data-ttu-id="7e14a-104">Le funzioni di gestione delle credenziali costituiscono il set di funzioni che devono essere implementate da Gestione credenziali.</span><span class="sxs-lookup"><span data-stu-id="7e14a-104">The credential management functions constitute the set of functions that a credential manager must implement.</span></span> <span data-ttu-id="7e14a-105">Si tratta di:</span><span class="sxs-lookup"><span data-stu-id="7e14a-105">These are:</span></span>

-   <span data-ttu-id="7e14a-106">[**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), una funzione del gestore eventi chiamata da MPR quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="7e14a-106">[**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), an event-handler function that the MPR calls when a user logs on.</span></span>
-   <span data-ttu-id="7e14a-107">[**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), una funzione del gestore eventi chiamata da MPR quando viene modificata la password di un account.</span><span class="sxs-lookup"><span data-stu-id="7e14a-107">[**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), an event-handler function the MPR calls when an account password is changed.</span></span>

<span data-ttu-id="7e14a-108">Le funzioni di gestione delle credenziali vengono sempre chiamate nel contesto di sistema (LocalSystem), anziché nel contesto utente.</span><span class="sxs-lookup"><span data-stu-id="7e14a-108">The credential management functions are always called in the system context (LocalSystem) rather than the user context.</span></span>

<span data-ttu-id="7e14a-109">Per ulteriori informazioni su come creare e registrare un'applicazione Gestione credenziali, vedere [Implementing a Credential Manager](implementing-a-credential-manager.md) e [Registering Network providers and Credential](registering-network-providers-and-credential-managers.md)managers.</span><span class="sxs-lookup"><span data-stu-id="7e14a-109">For more information about how to create and register a credential manager application, see [Implementing a Credential Manager](implementing-a-credential-manager.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

 



