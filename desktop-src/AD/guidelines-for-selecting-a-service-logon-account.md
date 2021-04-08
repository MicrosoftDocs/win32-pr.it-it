---
title: Linee guida per la selezione di un account di accesso al servizio
description: Un servizio basato su Win32 può essere eseguito nel contesto di sicurezza di un account utente locale, di un account utente di dominio o dell'account LocalSystem.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Linee guida per la selezione di un account di accesso al servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bb8f5b4fe6a57863c09c9563454fc3ec09e75c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044110"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a><span data-ttu-id="52118-104">Linee guida per la selezione di un account di accesso al servizio</span><span class="sxs-lookup"><span data-stu-id="52118-104">Guidelines for Selecting a Service Logon Account</span></span>

<span data-ttu-id="52118-105">Un servizio basato su Win32 può essere eseguito nel contesto di sicurezza di un account utente locale, di un account utente di dominio o dell'account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="52118-105">A Win32-based service can run in the security context of a local user account, a domain user account, or the LocalSystem account.</span></span> <span data-ttu-id="52118-106">Per decidere quale account usare, un amministratore deve installare il servizio con il set minimo di autorizzazioni necessarie per eseguire le operazioni del servizio.</span><span class="sxs-lookup"><span data-stu-id="52118-106">To decide which account to use, an administrator should install the service with the minimum set of permissions required to perform the service operations.</span></span> <span data-ttu-id="52118-107">In un tipico servizio abilitato per la directory, questo significa che il programma di installazione del servizio deve creare un account utente di dominio per il servizio e concedere all'account i diritti di accesso e i privilegi specifici richiesti dal servizio in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="52118-107">In a typical directory-enabled service, this means the service installer should create a domain user account for the service and grant that account the specific access rights and privileges required by the service at run time.</span></span> <span data-ttu-id="52118-108">Un servizio deve essere eseguito solo con l'account LocalSystem se il servizio richiede privilegi amministrativi o deve agire come parte del sistema operativo nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="52118-108">A service should only run under the LocalSystem account if the service requires administrative privileges or must act as part of the operating system on the local computer.</span></span>

<span data-ttu-id="52118-109">Tenere presente che, per impostazione predefinita, il programma di installazione del servizio configura il servizio per l'esecuzione con un account utente di dominio.</span><span class="sxs-lookup"><span data-stu-id="52118-109">Be aware that the service installer should, by default, set up the service to run under a domain user account.</span></span> <span data-ttu-id="52118-110">Per eseguire il servizio con l'account LocalSystem, il programma di installazione del servizio deve eseguire una query sull'amministratore per ottenere le autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="52118-110">To run the service under the LocalSystem account, the service installer should query the administrator for permission to do so.</span></span>

<span data-ttu-id="52118-111">Per ulteriori informazioni sulle descrizioni, i vantaggi e gli svantaggi di ogni tipo di conto, vedere:</span><span class="sxs-lookup"><span data-stu-id="52118-111">For more information about descriptions, advantages, and disadvantages of each account type, see:</span></span>

-   <span data-ttu-id="52118-112">[Account utente locali](local-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="52118-112">[Local User Accounts](local-user-accounts.md).</span></span>
-   <span data-ttu-id="52118-113">[Account utente di dominio](domain-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="52118-113">[Domain User Accounts](domain-user-accounts.md).</span></span>
-   <span data-ttu-id="52118-114">[Account LocalSystem](the-localsystem-account.md).</span><span class="sxs-lookup"><span data-stu-id="52118-114">[The LocalSystem Account](the-localsystem-account.md).</span></span>

 

 




