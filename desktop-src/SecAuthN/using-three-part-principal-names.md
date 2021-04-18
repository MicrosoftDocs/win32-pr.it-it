---
description: Quando si crea un pacchetto di sicurezza di Security Support Provider (SSP), è consigliabile non consentire al client aggiunto al dominio di eseguire l'autenticazione a un controller di dominio utilizzando un nome del provider di servizi (SPN) in due parti nel formato seguente.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Uso di tre nomi di entità parte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760ba740843c62c39a98e7e4683d25410a94ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306548"
---
# <a name="using-three-part-principal-names"></a><span data-ttu-id="39b73-103">Uso di tre nomi di entità parte</span><span class="sxs-lookup"><span data-stu-id="39b73-103">Using Three Part Principal Names</span></span>

<span data-ttu-id="39b73-104">Quando si crea un pacchetto di sicurezza di Security Support Provider (SSP), è consigliabile non consentire al client aggiunto al dominio di eseguire l'autenticazione a un controller di dominio utilizzando un nome del provider di servizi (SPN) in due parti nel formato seguente.</span><span class="sxs-lookup"><span data-stu-id="39b73-104">When creating a security support provider (SSP) security package, you should not allow the domain joined client to authenticate to a domain controller by using a two part service provider name (SPN) of the following form.</span></span>

-   <span data-ttu-id="39b73-105"><*protocollo* >/< di *nome host*></span><span class="sxs-lookup"><span data-stu-id="39b73-105"><*protocol*>/<*host name*></span></span>

<span data-ttu-id="39b73-106">Un client deve sempre eseguire l'autenticazione specificando il dominio.</span><span class="sxs-lookup"><span data-stu-id="39b73-106">A client should always authenticate by specifying the domain.</span></span>

-   <span data-ttu-id="39b73-107"><*protocollo* >/< di *nome host* >/< *nome di dominio*></span><span class="sxs-lookup"><span data-stu-id="39b73-107"><*protocol*>/<*host name*>/<*domain name*></span></span>

<span data-ttu-id="39b73-108">Un client aggiunto a un dominio che esegue l'accesso con un SPN a due parti potrebbe essere in grado di rappresentare il controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="39b73-108">A domain joined client that logs on with a two part SPN may be able to impersonate the domain controller.</span></span> <span data-ttu-id="39b73-109">Se si concedono due SPN della parte, è necessario creare una voce di log contenente informazioni sufficienti per consentire all'amministratore di identificare il chiamante.</span><span class="sxs-lookup"><span data-stu-id="39b73-109">If you allow two part SPNs, you should create a log entry that contains enough information to enable the administrator to identify the caller.</span></span>

 

 



