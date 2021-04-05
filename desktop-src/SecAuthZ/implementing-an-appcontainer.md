---
description: Un AppContainer viene implementato mediante l'aggiunta di nuove informazioni al token del processo, modificando SeAccessCheck () in modo che tutti gli oggetti legacy, non modificati (ACL) di controllo di accesso blocchino le richieste di accesso dai processi AppContainer per impostazione predefinita e gli oggetti ACL che devono essere disponibili per AppContainers.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implementazione di un AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884454"
---
# <a name="implementing-an-appcontainer"></a><span data-ttu-id="65ebc-103">Implementazione di un AppContainer</span><span class="sxs-lookup"><span data-stu-id="65ebc-103">Implementing an AppContainer</span></span>

<span data-ttu-id="65ebc-104">Un AppContainer viene implementato mediante l'aggiunta di nuove informazioni al token del processo, modificando [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) in modo che tutti gli oggetti legacy, non modificati (ACL) di controllo di accesso blocchino le richieste di accesso dai processi appcontainer per impostazione predefinita e gli oggetti ACL che devono essere disponibili per AppContainers.</span><span class="sxs-lookup"><span data-stu-id="65ebc-104">An AppContainer is implemented by adding new information to the process token, changing [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so that all legacy, unmodified access control list (ACL) objects block access requests from AppContainer processes by default, and re-ACL objects that should be available to AppContainers.</span></span>

## <a name="the-process"></a><span data-ttu-id="65ebc-105">Il processo</span><span class="sxs-lookup"><span data-stu-id="65ebc-105">The process</span></span>

<span data-ttu-id="65ebc-106">Per iniziare, aggiungere nuove informazioni per il token di processo.</span><span class="sxs-lookup"><span data-stu-id="65ebc-106">Begin by adding new information for the process token.</span></span> <span data-ttu-id="65ebc-107">Modificare quindi **SeAccessCheck ()** in modo che tutti gli ACL legacy e non modificati blocchino le richieste di accesso dai processi appcontainer per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="65ebc-107">Then change **SeAccessCheck()** so that all legacy, unmodified ACLs will block access requests from AppContainer processes by default.</span></span> <span data-ttu-id="65ebc-108">Infine, riacl risorse che devono essere disponibili per AppContainers</span><span class="sxs-lookup"><span data-stu-id="65ebc-108">Finally, re-ACL resources that should be available to AppContainers</span></span>

<span data-ttu-id="65ebc-109">Il SID AppContainer è un identificatore univoco permanente per il appcontainer.</span><span class="sxs-lookup"><span data-stu-id="65ebc-109">The AppContainer SID is a persistent unique identifier for the appcontainer.</span></span> <span data-ttu-id="65ebc-110">I SID della funzionalità concedono l'accesso ai gruppi di risorse ai gruppi di AppContainers.</span><span class="sxs-lookup"><span data-stu-id="65ebc-110">Capability SIDs grant access to groups of resources to groups of AppContainers.</span></span> <span data-ttu-id="65ebc-111">Un AppContainerNumber è un **valore DWORD** temporaneo usato per distinguere tra AppContainers.</span><span class="sxs-lookup"><span data-stu-id="65ebc-111">An AppContainerNumber is a transient **DWORD** used to distinguish between AppContainers.</span></span> <span data-ttu-id="65ebc-112">Tuttavia, non deve essere usato come identità per AppContainer.</span><span class="sxs-lookup"><span data-stu-id="65ebc-112">However, it should not be used as an identity for the AppContainer.</span></span>

<span data-ttu-id="65ebc-113">Per consentire a un singolo AppContainer di accedere a una risorsa, aggiungere il relativo AppContainerSID all'ACL per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="65ebc-113">To allow a single AppContainer to access a resource, add its AppContainerSID to the ACL for that resource.</span></span>

<span data-ttu-id="65ebc-114">Per consentire a più AppContainers specifiche di accedere a una risorsa, aggiungere tutti i AppContainerSIDs all'ACL per tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="65ebc-114">To allow several specific AppContainers to access a resource, add all of their AppContainerSIDs to the ACL for that resource.</span></span>

<span data-ttu-id="65ebc-115">Per gestire i gruppi di autorizzazioni, creare un SID della funzionalità (un GUID) e inserire tale SID per tutte le risorse da concedere.</span><span class="sxs-lookup"><span data-stu-id="65ebc-115">To manage groups of permissions, create a Capability SID (a GUID) and put that Capability SID on all of the resources to be granted.</span></span> <span data-ttu-id="65ebc-116">Aggiungere quindi il SID funzionalità al token di processo.</span><span class="sxs-lookup"><span data-stu-id="65ebc-116">Then add the Capability SID to your process token.</span></span>

<span data-ttu-id="65ebc-117">Per consentire a tutti AppContainers di accedere a una risorsa, aggiungere il SID **tutti i pacchetti dell'applicazione** all'ACL per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="65ebc-117">To allow all AppContainers to access a resource, add the **ALL APPLICATION PACKAGES** SID to the ACL for that resource.</span></span> <span data-ttu-id="65ebc-118">Questo comportamento è simile a un carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="65ebc-118">This acts like a wildcard.</span></span>

<span data-ttu-id="65ebc-119">Sia AppContainerSID che CapabilitySID supportano le maschere di accesso nelle voci di controllo di accesso (ACE).</span><span class="sxs-lookup"><span data-stu-id="65ebc-119">Both AppContainerSID and CapabilitySID support access masks in Access Control Entries (ACE).</span></span> <span data-ttu-id="65ebc-120">Imposta come appropriato.</span><span class="sxs-lookup"><span data-stu-id="65ebc-120">Set as appropriate.</span></span>

 

 
