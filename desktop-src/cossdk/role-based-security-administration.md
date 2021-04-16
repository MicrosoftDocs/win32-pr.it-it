---
description: Amministrazione della sicurezza Role-Based
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Amministrazione della sicurezza Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524041"
---
# <a name="role-based-security-administration"></a><span data-ttu-id="fb7af-103">Amministrazione della sicurezza Role-Based</span><span class="sxs-lookup"><span data-stu-id="fb7af-103">Role-Based Security Administration</span></span>

<span data-ttu-id="fb7af-104">La protezione basata sui ruoli è un servizio automatico fornito da COM+ che consente di costruire e applicare in modo amministrativo un criterio di controllo di accesso per l'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="fb7af-104">Role-based security is an automatic service provided by COM+ that enables you to administratively construct and enforce an access control policy for your COM+ application.</span></span> <span data-ttu-id="fb7af-105">Con un modello di configurazione della sicurezza flessibile ed estendibile, la protezione basata sui ruoli offre un notevole vantaggio rispetto all'applicazione di tutta la sicurezza all'interno dei componenti e offre i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="fb7af-105">With a flexible and extensible security configuration model, role-based security offers a considerable advantage over enforcing all security within your components and provides the following benefits:</span></span>

-   <span data-ttu-id="fb7af-106">È possibile configurare la sicurezza in modo amministrativo, usando lo strumento di amministrazione Servizi componenti o le funzioni amministrative.</span><span class="sxs-lookup"><span data-stu-id="fb7af-106">You can configure security administratively, using either the Component Services administrative tool or the Administrative functions.</span></span>
-   <span data-ttu-id="fb7af-107">Non è necessario scrivere logica correlata alla sicurezza nei componenti quando la protezione dei ruoli a livello di metodo offre un controllo di accesso sufficientemente preciso.</span><span class="sxs-lookup"><span data-stu-id="fb7af-107">You don't have to write security-related logic into your components when role protection at the method level provides you with fine enough access control.</span></span>
-   <span data-ttu-id="fb7af-108">Non è necessario eseguire il factoring della sicurezza nella progettazione di interfacce o componenti.</span><span class="sxs-lookup"><span data-stu-id="fb7af-108">You don't have to factor security into interface or component design.</span></span> <span data-ttu-id="fb7af-109">È invece possibile impostare la sicurezza in base al metodo.</span><span class="sxs-lookup"><span data-stu-id="fb7af-109">Instead, you can set security on a method-by-method basis.</span></span>
-   <span data-ttu-id="fb7af-110">È possibile concentrarsi sulla struttura dei criteri di sicurezza che si desidera applicare e, tramite i ruoli, che i criteri possono essere chiaramente espressi agli amministratori che distribuiscono l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb7af-110">You can focus on the structure of the security policy you want to enforce, and through roles, that policy can be clearly expressed to the administrators deploying your application.</span></span>
-   <span data-ttu-id="fb7af-111">È possibile modificare facilmente i criteri di sicurezza per adattarsi ai requisiti di sicurezza in evoluzione per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb7af-111">You can easily modify a security policy to adapt to evolving security requirements for an application.</span></span>
-   <span data-ttu-id="fb7af-112">È possibile creare criteri di sicurezza più granulari a livello di codice, se necessario, usando la protezione basata sui ruoli come piattaforma di supporto.</span><span class="sxs-lookup"><span data-stu-id="fb7af-112">You can build more granular security policies programmatically if you need to, using role-based security as a supporting platform.</span></span>
-   <span data-ttu-id="fb7af-113">È possibile sfruttare la protezione basata sui ruoli per eseguire controlli dettagliati, perché è possibile ottenere informazioni sulla sicurezza del chiamante per un'intera catena di chiamate upstream.</span><span class="sxs-lookup"><span data-stu-id="fb7af-113">You can leverage role-based security to do detailed auditing, because you can obtain caller security information for an entire chain of upstream calls.</span></span>

> [!Note]  
> <span data-ttu-id="fb7af-114">Gli utenti con ruolo di amministratore per l'applicazione di sistema devono essere membri del gruppo Administrators locale.</span><span class="sxs-lookup"><span data-stu-id="fb7af-114">Users in the Administrator role for the System Application must be members of the local administrators group.</span></span> <span data-ttu-id="fb7af-115">Inoltre, a partire da Windows Server 2003, la funzionalità di autenticazione per l'applicazione di sistema COM+ include il valore EOAC \_ Disable \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="fb7af-115">Also, as of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="fb7af-116">Questo valore, che disabilita le attivazioni di Activate-As-Activator (AAA), viene usato nella chiamata [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) quando viene avviata l'applicazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="fb7af-116">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="fb7af-117">Impostando la funzionalità di autenticazione su EOAC \_ Disable AAA è possibile consentire a \_ un'applicazione in esecuzione con un account con privilegi, ad esempio LocalSystem, di impedire l'utilizzo dell'identità per l'avvio di componenti non attendibili.</span><span class="sxs-lookup"><span data-stu-id="fb7af-117">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

 

<span data-ttu-id="fb7af-118">Vedere gli argomenti seguenti in questa sezione per informazioni sul funzionamento della sicurezza basata sui ruoli e sui problemi da considerare quando si usa per creare criteri di sicurezza per un'applicazione:</span><span class="sxs-lookup"><span data-stu-id="fb7af-118">See the following topics in this section for information about how role-based security works and issues to consider when using it to construct a security policy for an application:</span></span>

-   [<span data-ttu-id="fb7af-119">Utilizzo dei ruoli per l'autorizzazione client</span><span class="sxs-lookup"><span data-stu-id="fb7af-119">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
-   [<span data-ttu-id="fb7af-120">Progettazione efficace dei ruoli</span><span class="sxs-lookup"><span data-stu-id="fb7af-120">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
-   [<span data-ttu-id="fb7af-121">Limiti di sicurezza</span><span class="sxs-lookup"><span data-stu-id="fb7af-121">Security Boundaries</span></span>](security-boundaries.md)
-   [<span data-ttu-id="fb7af-122">Informazioni sul contesto delle chiamate di sicurezza</span><span class="sxs-lookup"><span data-stu-id="fb7af-122">Security Call Context Information</span></span>](security-call-context-information.md)
-   [<span data-ttu-id="fb7af-123">Proprietà del contesto di sicurezza</span><span class="sxs-lookup"><span data-stu-id="fb7af-123">Security Context Property</span></span>](security-context-property.md)

<span data-ttu-id="fb7af-124">Per una descrizione dettagliata dei passaggi necessari per la configurazione della sicurezza basata sui ruoli per un'applicazione, vedere [configurazione Role-Based sicurezza](configuring-role-based-security.md).</span><span class="sxs-lookup"><span data-stu-id="fb7af-124">For detailed how-to descriptions of the steps involved in configuring role-based security for an application, see [Configuring Role-Based Security](configuring-role-based-security.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb7af-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fb7af-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb7af-126">Autenticazione client</span><span class="sxs-lookup"><span data-stu-id="fb7af-126">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="fb7af-127">Rappresentazione e delega client</span><span class="sxs-lookup"><span data-stu-id="fb7af-127">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="fb7af-128">Sicurezza delle applicazioni di libreria</span><span class="sxs-lookup"><span data-stu-id="fb7af-128">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="fb7af-129">Sicurezza delle applicazioni a più livelli</span><span class="sxs-lookup"><span data-stu-id="fb7af-129">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="fb7af-130">Sicurezza del componente a livello di codice</span><span class="sxs-lookup"><span data-stu-id="fb7af-130">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="fb7af-131">Uso dei criteri di restrizione software in COM+</span><span class="sxs-lookup"><span data-stu-id="fb7af-131">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
