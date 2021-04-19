---
description: Sicurezza delle applicazioni a più livelli
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Sicurezza delle applicazioni a più livelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150f7894c7d11e832786e31ab028f9dbac35f6e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304817"
---
# <a name="multi-tier-application-security"></a><span data-ttu-id="7ec01-103">Sicurezza delle applicazioni a più livelli</span><span class="sxs-lookup"><span data-stu-id="7ec01-103">Multi-Tier Application Security</span></span>

<span data-ttu-id="7ec01-104">È possibile affrontare scelte difficili nel decidere esattamente dove applicare la protezione in un'applicazione multilivello basata su componenti: nel database?</span><span class="sxs-lookup"><span data-stu-id="7ec01-104">You can face difficult choices in deciding precisely where to enforce security in a multi-tier, component-based application: At the database?</span></span> <span data-ttu-id="7ec01-105">Al livello intermedio?</span><span class="sxs-lookup"><span data-stu-id="7ec01-105">At the middle tier?</span></span> <span data-ttu-id="7ec01-106">Nei componenti?</span><span class="sxs-lookup"><span data-stu-id="7ec01-106">In the components?</span></span> <span data-ttu-id="7ec01-107">Altrove?</span><span class="sxs-lookup"><span data-stu-id="7ec01-107">Somewhere else?</span></span> <span data-ttu-id="7ec01-108">Ovunque?</span><span class="sxs-lookup"><span data-stu-id="7ec01-108">Everywhere?</span></span> <span data-ttu-id="7ec01-109">Con l'aumentare del numero e della complessità dei meccanismi di sicurezza, il calo delle prestazioni e il comportamento dell'applicazione diventano meno prevedibili.</span><span class="sxs-lookup"><span data-stu-id="7ec01-109">As security mechanisms increase in number and complexity, performance declines and application behavior becomes less predictable.</span></span> <span data-ttu-id="7ec01-110">Tuttavia, è necessario assicurarsi che i dati siano protetti, che vengano seguite le regole business e che venga registrata un'attività significativa e che l'applicazione funzioni per i client come previsto.</span><span class="sxs-lookup"><span data-stu-id="7ec01-110">Nevertheless, you must ensure that data is protected, business rules are followed, and significant activity is logged, and still have your application work for clients as intended.</span></span> <span data-ttu-id="7ec01-111">È necessario essere certi che ogni percorso client nell'applicazione sia corretto e che i checkpoint di sicurezza disponibili siano sufficienti.</span><span class="sxs-lookup"><span data-stu-id="7ec01-111">You must be certain that every client path through your application is correct and that the security checkpoints you have in place will suffice.</span></span>

<span data-ttu-id="7ec01-112">La decisione più complessa è spesso la possibilità di applicare la protezione al database.</span><span class="sxs-lookup"><span data-stu-id="7ec01-112">The hardest decision is often whether to enforce security at the database.</span></span> <span data-ttu-id="7ec01-113">Storicamente, questo è il punto in cui la sicurezza è più stretta perché viene percepita come un Regno che deve essere effettivamente sicuro e gli amministratori di database sono molto riluttanti a fidarsi di un altro utente per applicare la protezione.</span><span class="sxs-lookup"><span data-stu-id="7ec01-113">Historically, this is where security is tightest because it is perceived as the one kingdom that needs to be truly secure, and database administrators are very reluctant to trust someone else to enforce security for them.</span></span> <span data-ttu-id="7ec01-114">Tuttavia, l'applicazione della sicurezza nel database può essere piuttosto costosa e difficile da scalare, che è esattamente il punto di scrittura di applicazioni multilivello in primo luogo.</span><span class="sxs-lookup"><span data-stu-id="7ec01-114">But enforcing security at the database can be quite expensive and difficult to scale, which is precisely the point of writing multi-tier applications in the first place.</span></span>

<span data-ttu-id="7ec01-115">La regola generale da seguire con le applicazioni multilivello scalabili mediante COM+ è che, laddove possibile, è necessario applicare una sicurezza dettagliata nell'applicazione COM+ a livello intermedio.</span><span class="sxs-lookup"><span data-stu-id="7ec01-115">The general rule to follow with scalable multi-tier applications using COM+ is that, whenever possible, you should enforce detailed security in the COM+ application at the middle tier.</span></span> <span data-ttu-id="7ec01-116">Questa operazione consente di sfruttare appieno i servizi scalabili forniti da COM+.</span><span class="sxs-lookup"><span data-stu-id="7ec01-116">Doing so enables you to fully leverage the scalable services provided by COM+.</span></span> <span data-ttu-id="7ec01-117">Eseguire l'autenticazione nel database solo quando è assolutamente necessario e valutare completamente le implicazioni delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="7ec01-117">Authenticate at the database only when you absolutely need to, and fully weigh the performance implications of doing so.</span></span>

<span data-ttu-id="7ec01-118">Per informazioni sui problemi da prendere in considerazione per decidere dove eseguire i controlli di sicurezza, vedere [decidere dove applicare la sicurezza](deciding-where-to-enforce-security.md).</span><span class="sxs-lookup"><span data-stu-id="7ec01-118">For a discussion of issues to consider in deciding where to perform security checks, see [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

<span data-ttu-id="7ec01-119">Per informazioni su alcuni scenari di base per la protezione di applicazioni multilivello, vedere [scenari di base per la protezione dei dati nelle applicazioni multilivello](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span><span class="sxs-lookup"><span data-stu-id="7ec01-119">For a discussion of some basic scenarios in securing multi-tier applications, see [Basic Scenarios for Securing Data in Multi-Tier Applications](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ec01-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ec01-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ec01-121">Autenticazione client</span><span class="sxs-lookup"><span data-stu-id="7ec01-121">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="7ec01-122">Rappresentazione e delega client</span><span class="sxs-lookup"><span data-stu-id="7ec01-122">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="7ec01-123">Sicurezza delle applicazioni di libreria</span><span class="sxs-lookup"><span data-stu-id="7ec01-123">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="7ec01-124">Sicurezza del componente a livello di codice</span><span class="sxs-lookup"><span data-stu-id="7ec01-124">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="7ec01-125">Amministrazione della sicurezza basata sui ruoli</span><span class="sxs-lookup"><span data-stu-id="7ec01-125">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="7ec01-126">Uso dei criteri di restrizione software in COM+</span><span class="sxs-lookup"><span data-stu-id="7ec01-126">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



