---
description: Poiché un'applicazione libreria COM+ è ospitata da un altro processo, che può avere le proprie impostazioni di sicurezza, la sicurezza per le applicazioni di libreria richiede una particolare attenzione.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Sicurezza delle applicazioni di libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2885173f3798d33ed26a5b447fde4429b9bf96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523418"
---
# <a name="library-application-security"></a><span data-ttu-id="b9647-103">Sicurezza delle applicazioni di libreria</span><span class="sxs-lookup"><span data-stu-id="b9647-103">Library Application Security</span></span>

<span data-ttu-id="b9647-104">Poiché un'applicazione libreria COM+ è ospitata da un altro processo, che può avere le proprie impostazioni di sicurezza, la sicurezza per le applicazioni di libreria richiede una particolare attenzione.</span><span class="sxs-lookup"><span data-stu-id="b9647-104">Because a COM+ library application is hosted by another process, which may have its own security settings, security for library applications requires special consideration.</span></span>

<span data-ttu-id="b9647-105">I vincoli seguenti si applicano alla sicurezza dell'applicazione della libreria:</span><span class="sxs-lookup"><span data-stu-id="b9647-105">The following constraints apply to library application security:</span></span>

-   <span data-ttu-id="b9647-106">Le applicazioni di libreria vengono eseguite con il token di sicurezza del processo client anziché con la propria identità utente.</span><span class="sxs-lookup"><span data-stu-id="b9647-106">Library applications run under the client process security token rather than under their own user identity.</span></span> <span data-ttu-id="b9647-107">Hanno solo il privilegio del client.</span><span class="sxs-lookup"><span data-stu-id="b9647-107">They have only as much privilege as the client has.</span></span>
-   <span data-ttu-id="b9647-108">Le applicazioni di libreria non controllano la sicurezza a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="b9647-108">Library applications do not control process-level security.</span></span> <span data-ttu-id="b9647-109">Nessun utente nei ruoli verrà aggiunto al descrittore di sicurezza per il processo.</span><span class="sxs-lookup"><span data-stu-id="b9647-109">No users in roles will be added to the security descriptor for the process.</span></span> <span data-ttu-id="b9647-110">L'unico modo per eseguire controlli di accesso a un'applicazione libreria consiste nell'usare la sicurezza a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="b9647-110">The only way for a library application to perform its own access checks is to use component-level security.</span></span> <span data-ttu-id="b9647-111">Vedere i [limiti di sicurezza](security-boundaries.md).</span><span class="sxs-lookup"><span data-stu-id="b9647-111">(See [Security Boundaries](security-boundaries.md).)</span></span>
-   <span data-ttu-id="b9647-112">Le applicazioni di libreria possono essere configurate per partecipare o non partecipare all'autenticazione del processo host, abilitando o disabilitando l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b9647-112">Library applications can be configured to either participate or not participate in host process authentication, by enabling or disabling authentication.</span></span> <span data-ttu-id="b9647-113">Vedere [Abilitazione dell'autenticazione per un'applicazione di libreria](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="b9647-113">(See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).)</span></span>
-   <span data-ttu-id="b9647-114">Le applicazioni di libreria non possono impostare un livello di rappresentazione. usano quello del processo host.</span><span class="sxs-lookup"><span data-stu-id="b9647-114">Library applications cannot set an impersonation level; they use that of the host process.</span></span>

## <a name="using-library-applications-to-limit-application-privilege"></a><span data-ttu-id="b9647-115">Uso delle applicazioni di libreria per limitare i privilegi dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b9647-115">Using Library Applications to Limit Application Privilege</span></span>

<span data-ttu-id="b9647-116">In alcuni casi, può essere necessario configurare un'applicazione in modo specifico come applicazione di libreria in modo che venga eseguita con l'identità del processo di hosting.</span><span class="sxs-lookup"><span data-stu-id="b9647-116">In some cases, you may want to configure an application specifically as a library application so that it runs under the identity of the hosting process.</span></span> <span data-ttu-id="b9647-117">Questa operazione limita fondamentalmente l'applicazione in modo che possa accedere solo alle risorse accessibili dal client, ovvero dal processo host.</span><span class="sxs-lookup"><span data-stu-id="b9647-117">Doing so fundamentally limits the application so that it can access only those resources that its client, the host process, can access.</span></span> <span data-ttu-id="b9647-118">I thread sui quali vengono eseguiti i componenti dell'applicazione della libreria utilizzeranno il token di processo per impostazione predefinita e, pertanto, quando effettuano chiamate all'esterno dell'applicazione o accedono alle risorse, ad esempio i file sorvegliati con un descrittore di sicurezza, verranno visualizzati come client.</span><span class="sxs-lookup"><span data-stu-id="b9647-118">The threads that the library application components run on will use the process token by default, and therefore when they make calls outside of the application or access resources such as files guarded with a security descriptor, they will appear to be the client.</span></span> <span data-ttu-id="b9647-119">Per le applicazioni che eseguono operazioni riservate, questo può essere un modo semplice per controllare l'ambito delle proprie azioni.</span><span class="sxs-lookup"><span data-stu-id="b9647-119">For applications that perform sensitive work, this may be an easy way to control the scope of their actions.</span></span>

## <a name="effectively-securing-library-applications"></a><span data-ttu-id="b9647-120">Protezione efficace delle applicazioni di libreria</span><span class="sxs-lookup"><span data-stu-id="b9647-120">Effectively Securing Library Applications</span></span>

<span data-ttu-id="b9647-121">Per la configurazione della sicurezza basata sui ruoli e dell'autenticazione per le applicazioni di libreria è necessario tenere presenti alcune considerazioni speciali, in modo che vengano eseguite come previsto.</span><span class="sxs-lookup"><span data-stu-id="b9647-121">There are special considerations in configuring role-based security and authentication for library applications so that they perform as expected.</span></span> <span data-ttu-id="b9647-122">Per informazioni dettagliate, vedere [configurazione della protezione per le applicazioni di libreria](configuring-security-for-library-applications.md).</span><span class="sxs-lookup"><span data-stu-id="b9647-122">For details, see [Configuring Security for Library Applications](configuring-security-for-library-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9647-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9647-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9647-124">Autenticazione client</span><span class="sxs-lookup"><span data-stu-id="b9647-124">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="b9647-125">Rappresentazione e delega client</span><span class="sxs-lookup"><span data-stu-id="b9647-125">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="b9647-126">Sicurezza delle applicazioni a più livelli</span><span class="sxs-lookup"><span data-stu-id="b9647-126">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="b9647-127">Sicurezza del componente a livello di codice</span><span class="sxs-lookup"><span data-stu-id="b9647-127">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="b9647-128">Amministrazione della sicurezza basata sui ruoli</span><span class="sxs-lookup"><span data-stu-id="b9647-128">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="b9647-129">Uso dei criteri di restrizione software in COM+</span><span class="sxs-lookup"><span data-stu-id="b9647-129">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



