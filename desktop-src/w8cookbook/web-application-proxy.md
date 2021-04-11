---
title: Proxy applicazione Web
description: Proxy applicazione Web
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220ac5f52a8f5130cdb6fb21649ff302e6693b1b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104118575"
---
# <a name="web-application-proxy"></a><span data-ttu-id="d2672-103">Proxy applicazione Web</span><span class="sxs-lookup"><span data-stu-id="d2672-103">Web Application Proxy</span></span>

## <a name="platform"></a><span data-ttu-id="d2672-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="d2672-104">Platform</span></span>

<span data-ttu-id="d2672-105">**Server-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d2672-105">**Servers -** Windows Server 2012 R2</span></span>  






## <a name="description"></a><span data-ttu-id="d2672-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2672-106">Description</span></span>

<span data-ttu-id="d2672-107">In Windows Server 2012 R2 è stato aggiunto un nuovo servizio denominato proxy applicazione Web con il ruolo accesso remoto che consente agli amministratori di pubblicare applicazioni per l'accesso esterno.</span><span class="sxs-lookup"><span data-stu-id="d2672-107">In Windows Server 2012 R2, we added a new service called the Web Application Proxy under the Remote Access role that allows administrators to publish applications for external access.</span></span> <span data-ttu-id="d2672-108">Questo servizio funge da proxy inverso e come proxy di Active Directory Federation Services (AD FS).</span><span class="sxs-lookup"><span data-stu-id="d2672-108">This service acts as a reverse proxy and as an Active Directory Federation Services (AD FS) proxy.</span></span> <span data-ttu-id="d2672-109">Questo servizio sostituisce infatti il servizio proxy AD FS come è noto in Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="d2672-109">In fact, this service replaces the AD FS proxy service as it was known in Windows Server 2012.</span></span>

<span data-ttu-id="d2672-110">Con il proxy dell'applicazione Web, un'organizzazione può rendere disponibili risorse Web locali per l'accesso esterno, gestendo allo stesso tempo il rischio di questo accesso controllando i criteri di autenticazione e autorizzazione nel AD FS.</span><span class="sxs-lookup"><span data-stu-id="d2672-110">With the Web Application Proxy, an organization can make on-premises web resources available for external access while at the same time managing the risk of this access by controlling authentication and authorization policies on the AD FS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="d2672-111">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="d2672-111">Manifestation</span></span>

<span data-ttu-id="d2672-112">Il servizio proxy AD FS non è più sotto il ruolo di Active Directory Federation Services (AD FS), ma è stato sostituito dal proxy dell'applicazione Web nel ruolo accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="d2672-112">The AD FS proxy service is no longer under the Active Directory Federation Services role (AD FS), but has been replaced by the Web Application Proxy under the Remote Access role.</span></span> <span data-ttu-id="d2672-113">Rappresenta un'espansione del servizio proxy AD FS includendo la funzionalità del proxy inverso per la pubblicazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2672-113">This represents an expansion of the AD FS proxy service by including reverse proxy functionality for application publishing.</span></span>

## <a name="solution"></a><span data-ttu-id="d2672-114">Soluzione</span><span class="sxs-lookup"><span data-stu-id="d2672-114">Solution</span></span>

<span data-ttu-id="d2672-115">Per accedere al proxy dell'applicazione Web, gli amministratori possono passare a Server Manager e aggiungere un nuovo ruolo/servizio ruolo.</span><span class="sxs-lookup"><span data-stu-id="d2672-115">To access the Web Application Proxy, administrators can go to Server Manager and add a new role/role service.</span></span> <span data-ttu-id="d2672-116">L'amministratore troverà il proxy applicazione Web nel ruolo accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="d2672-116">The administrator will find the Web Application Proxy under the Remote Access role.</span></span>

## <a name="resources"></a><span data-ttu-id="d2672-117">Risorse</span><span class="sxs-lookup"><span data-stu-id="d2672-117">Resources</span></span>

-   <span data-ttu-id="d2672-118">[Guida alla soluzione](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="d2672-118">[Solution guide](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span></span>

 

 