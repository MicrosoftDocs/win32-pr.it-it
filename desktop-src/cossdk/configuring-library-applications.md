---
description: Configurazione di applicazioni di libreria
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Configurazione di applicazioni di libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51e00626d42044797881ccb86553ddfda38a089
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049139"
---
# <a name="configuring-library-applications"></a><span data-ttu-id="c2046-103">Configurazione di applicazioni di libreria</span><span class="sxs-lookup"><span data-stu-id="c2046-103">Configuring Library Applications</span></span>

<span data-ttu-id="c2046-104">Poiché le applicazioni di libreria COM+ vengono eseguite nel processo del client, gli elementi configurabili per le applicazioni di libreria sono notevolmente diversi rispetto alle applicazioni server.</span><span class="sxs-lookup"><span data-stu-id="c2046-104">Because COM+ library applications run in the client's process, the configurable elements for library applications are considerably different than for server applications.</span></span> <span data-ttu-id="c2046-105">Non è possibile configurare alcun aspetto dell'applicazione determinato dal processo di hosting.</span><span class="sxs-lookup"><span data-stu-id="c2046-105">You cannot configure any aspect of the application that is determined by the hosting process.</span></span>

<span data-ttu-id="c2046-106">A livello di applicazione, diverse impostazioni sono limitate o non disponibili per le applicazioni di libreria.</span><span class="sxs-lookup"><span data-stu-id="c2046-106">At the application level, several settings are either limited or unavailable for library applications.</span></span> <span data-ttu-id="c2046-107">Questi vincoli sono descritti nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="c2046-107">These constraints are described in the following table:</span></span>



| <span data-ttu-id="c2046-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="c2046-108">Attribute</span></span>                                       | <span data-ttu-id="c2046-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2046-109">Description</span></span>                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2046-110">Livello di sicurezza</span><span class="sxs-lookup"><span data-stu-id="c2046-110">Security level</span></span><br/>                       | <span data-ttu-id="c2046-111">È necessario scegliere i controlli di accesso a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="c2046-111">You must choose component-level access checks.</span></span> <span data-ttu-id="c2046-112">L'applicazione di libreria non può influenzare i controlli di accesso a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="c2046-112">The library application cannot influence process-level access checks.</span></span> <span data-ttu-id="c2046-113">Vedere [impostazione di un livello di sicurezza per i controlli di accesso](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="c2046-113">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span><br/>             |
| <span data-ttu-id="c2046-114">Abilitazione o disabilitazione dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="c2046-114">Enabling or disabling authentication</span></span><br/> | <span data-ttu-id="c2046-115">È possibile indicare se l'applicazione della libreria parteciperà all'autenticazione eseguita dal processo host.</span><span class="sxs-lookup"><span data-stu-id="c2046-115">You can indicate whether the library application will participate in authentication performed by the host process.</span></span> <span data-ttu-id="c2046-116">Vedere [Abilitazione dell'autenticazione per un'applicazione di libreria](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="c2046-116">See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).</span></span><br/> |
| <span data-ttu-id="c2046-117">Livello di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="c2046-117">Impersonation level</span></span><br/>                  | <span data-ttu-id="c2046-118">Disponibile.</span><span class="sxs-lookup"><span data-stu-id="c2046-118">Unavailable.</span></span> <span data-ttu-id="c2046-119">Viene utilizzata l'impostazione del processo host.</span><span class="sxs-lookup"><span data-stu-id="c2046-119">The setting of the host process is used.</span></span> <br/>                                                                                                                                                                             |
| <span data-ttu-id="c2046-120">Identità di sicurezza</span><span class="sxs-lookup"><span data-stu-id="c2046-120">Security identity</span></span><br/>                    | <span data-ttu-id="c2046-121">Disponibile.</span><span class="sxs-lookup"><span data-stu-id="c2046-121">Unavailable.</span></span> <span data-ttu-id="c2046-122">L'applicazione viene eseguita con l'identità del processo host.</span><span class="sxs-lookup"><span data-stu-id="c2046-122">The application runs under the identity of the host process.</span></span><br/>                                                                                                                                                          |
| <span data-ttu-id="c2046-123">Arresto del processo server</span><span class="sxs-lookup"><span data-stu-id="c2046-123">Server process shutdown</span></span><br/>              | <span data-ttu-id="c2046-124">Disponibile.</span><span class="sxs-lookup"><span data-stu-id="c2046-124">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="c2046-125">Abilita supporto da 3 GB</span><span class="sxs-lookup"><span data-stu-id="c2046-125">Enable 3-GB support</span></span><br/>                  | <span data-ttu-id="c2046-126">Disponibile.</span><span class="sxs-lookup"><span data-stu-id="c2046-126">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="c2046-127">Avvia nel debugger</span><span class="sxs-lookup"><span data-stu-id="c2046-127">Launch in debugger</span></span><br/>                   | <span data-ttu-id="c2046-128">Disponibile.</span><span class="sxs-lookup"><span data-stu-id="c2046-128">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="c2046-129">Abilita CRM</span><span class="sxs-lookup"><span data-stu-id="c2046-129">Enable CRM</span></span><br/>                           | <span data-ttu-id="c2046-130">Disponibile.</span><span class="sxs-lookup"><span data-stu-id="c2046-130">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="c2046-131">Accodamento</span><span class="sxs-lookup"><span data-stu-id="c2046-131">Queuing</span></span><br/>                              | <span data-ttu-id="c2046-132">Disponibile.</span><span class="sxs-lookup"><span data-stu-id="c2046-132">Unavailable.</span></span><br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="c2046-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2046-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2046-134">Panoramica dell'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="c2046-134">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> </dl>

 

 




