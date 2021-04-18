---
description: Quando si utilizza la sicurezza basata sui ruoli nell'applicazione COM+ che contiene il componente, è possibile accedere alla funzionalità di sicurezza a livello di codice dall'interno del componente.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Sicurezza del componente a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304941"
---
# <a name="programmatic-component-security"></a><span data-ttu-id="de8f1-103">Sicurezza del componente a livello di codice</span><span class="sxs-lookup"><span data-stu-id="de8f1-103">Programmatic Component Security</span></span>

<span data-ttu-id="de8f1-104">Quando si utilizza la sicurezza basata sui ruoli nell'applicazione COM+ che contiene il componente, è possibile accedere alla funzionalità di sicurezza a livello di codice dall'interno del componente.</span><span class="sxs-lookup"><span data-stu-id="de8f1-104">When you use role-based security in the COM+ application that contains your component, you have access to programmatic security functionality from within your component.</span></span> <span data-ttu-id="de8f1-105">È possibile controllare l'appartenenza ai ruoli per determinare se vengono eseguite specifiche sezioni di codice, è possibile accedere alle informazioni di sicurezza utilizzando l'oggetto contesto delle chiamate di sicurezza e determinare se la sicurezza è abilitata per la chiamata corrente.</span><span class="sxs-lookup"><span data-stu-id="de8f1-105">You can check role membership to determine whether particular sections of code are executed, you can access security information using the security call context object, and you can determine whether security is enabled for the current call.</span></span> <span data-ttu-id="de8f1-106">È possibile eseguire tutte queste attività usando un riferimento a un oggetto [**SecurityCallContext**](securitycallcontext.md) (per le applicazioni Microsoft Visual Basic) o un puntatore all'interfaccia [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) (per le applicazioni C e Microsoft Visual C++).</span><span class="sxs-lookup"><span data-stu-id="de8f1-106">You can perform all of these tasks by using a reference to a [**SecurityCallContext**](securitycallcontext.md) object (for Microsoft Visual Basic applications) or a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface (for C and Microsoft Visual C++ applications).</span></span>

<span data-ttu-id="de8f1-107">Per ulteriori informazioni sulla sicurezza basata sui ruoli a livello di codice, vedere gli argomenti seguenti in questa sezione:</span><span class="sxs-lookup"><span data-stu-id="de8f1-107">For more information regarding programmatic role-based security, see the following topics in this section:</span></span>

-   [<span data-ttu-id="de8f1-108">Verifica dell'appartenenza ai ruoli</span><span class="sxs-lookup"><span data-stu-id="de8f1-108">Checking Role Membership</span></span>](checking-role-membership.md)
-   [<span data-ttu-id="de8f1-109">Determinare se Role-Based sicurezza è abilitata</span><span class="sxs-lookup"><span data-stu-id="de8f1-109">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
-   [<span data-ttu-id="de8f1-110">Accesso alle informazioni sul contesto delle chiamate di sicurezza</span><span class="sxs-lookup"><span data-stu-id="de8f1-110">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a><span data-ttu-id="de8f1-111">Rappresentazione e funzionalità di sicurezza COM</span><span class="sxs-lookup"><span data-stu-id="de8f1-111">Impersonation and COM Security Features</span></span>

<span data-ttu-id="de8f1-112">Se il componente viene utilizzato in un'applicazione COM+ che non utilizza la protezione basata sui ruoli, non sono disponibili informazioni sul contesto di controllo dei ruoli e delle chiamate di sicurezza a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="de8f1-112">If your component is used in a COM+ application that does not use role-based security, programmatic role checking and security call context information are not available.</span></span> <span data-ttu-id="de8f1-113">Tuttavia, è possibile usare la funzionalità di sicurezza a livello di codice fornita da COM.</span><span class="sxs-lookup"><span data-stu-id="de8f1-113">However, you can use the programmatic security functionality provided by COM.</span></span> <span data-ttu-id="de8f1-114">Per ulteriori informazioni, vedere [sicurezza in com](/windows/desktop/com/security-in-com).</span><span class="sxs-lookup"><span data-stu-id="de8f1-114">For more information, see [Security in COM](/windows/desktop/com/security-in-com).</span></span>

<span data-ttu-id="de8f1-115">Sebbene sia possibile utilizzare la maggior parte delle funzionalità di sicurezza fornite da COM, non è possibile chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) da un componente che fa parte di un'applicazione com+ perché **CoInitializeSecurity** viene chiamato dal surrogato in cui viene eseguita l'applicazione com+.</span><span class="sxs-lookup"><span data-stu-id="de8f1-115">Although you can use most of the security functionality provided by COM, you cannot call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) from a component that is part of a COM+ application because **CoInitializeSecurity** is called by the surrogate that the COM+ application runs in.</span></span> <span data-ttu-id="de8f1-116">Tuttavia, è possibile chiamare altre funzioni di sicurezza, ad esempio [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), che recupera le informazioni sul client.</span><span class="sxs-lookup"><span data-stu-id="de8f1-116">However, you can call other security functions, such as [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), which retrieves information about the client.</span></span>

<span data-ttu-id="de8f1-117">In particolare, quando è necessario usare l'identità del client per accedere a una risorsa, ad esempio l'accesso a un file protetto da un descrittore di sicurezza o la propagazione dell'identità del client tramite a un database, è possibile eseguire la rappresentazione a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="de8f1-117">In particular, when you need to use the client's identity to access some resource—for example, accessing a file protected by a security descriptor, or propagating the client's identity through to a database—you can perform impersonation programmatically.</span></span> <span data-ttu-id="de8f1-118">Per informazioni dettagliate su quando e come eseguire questa operazione, vedere [rappresentazione e delega del client](client-impersonation-and-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="de8f1-118">For more detail about when and how to do this, see [Client Impersonation and Delegation](client-impersonation-and-delegation.md).</span></span>

## <a name="testing-security-functionality"></a><span data-ttu-id="de8f1-119">Test della funzionalità di sicurezza</span><span class="sxs-lookup"><span data-stu-id="de8f1-119">Testing Security Functionality</span></span>

<span data-ttu-id="de8f1-120">Se si utilizza la sicurezza a livello di codice COM+ nel componente, è necessario integrare il componente in un'applicazione COM+ quando si è pronti per testare la funzionalità di sicurezza del componente.</span><span class="sxs-lookup"><span data-stu-id="de8f1-120">If you use COM+ programmatic security in your component, you must integrate the component into a COM+ application when you are ready to test the component's security functionality.</span></span> <span data-ttu-id="de8f1-121">Se un componente che utilizza la sicurezza a livello di codice COM+ viene eseguito senza essere integrato in un'applicazione COM+, verranno generate eccezioni.</span><span class="sxs-lookup"><span data-stu-id="de8f1-121">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="de8f1-122">Pertanto, se si desidera garantire che tale componente sia anche in grado di integrarsi correttamente in un'applicazione che non fa parte dell'ambiente COM+, è necessario assicurarsi che tali eccezioni vengano gestite in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="de8f1-122">Therefore, if you want to ensure that such a component is also capable of being successfully integrated into an application that is not part of the COM+ environment, you must ensure that these exceptions are handled appropriately.</span></span>

## <a name="documenting-security-requirements"></a><span data-ttu-id="de8f1-123">Documentazione dei requisiti di sicurezza</span><span class="sxs-lookup"><span data-stu-id="de8f1-123">Documenting Security Requirements</span></span>

<span data-ttu-id="de8f1-124">Se si sta scrivendo un componente autonomo per applicazioni COM+ che utilizzano la sicurezza basata sui ruoli, è necessario documentare il componente in modo che la sicurezza possa essere configurata in modo appropriato quando il componente è integrato in un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="de8f1-124">If you are writing a stand-alone component for COM+ applications that use role-based security, you need to document the component so that security can be configured appropriately when the component is integrated into a COM+ application.</span></span> <span data-ttu-id="de8f1-125">È ad esempio necessario identificare i ruoli che devono essere aggiunti e spiegare i metodi e le interfacce a cui deve essere assegnato ogni ruolo.</span><span class="sxs-lookup"><span data-stu-id="de8f1-125">For example, you should identify the roles that must be added and explain which methods and interfaces each role should be assigned to.</span></span> <span data-ttu-id="de8f1-126">Se, inoltre, viene chiamato un metodo, ad esempio IsCallerInRole ("Teller"), è necessario descrivere la funzionalità a cui hanno accesso solo i cassieri.</span><span class="sxs-lookup"><span data-stu-id="de8f1-126">In addition, if a method such as IsCallerInRole("Teller") is called, you should describe the functionality that only Tellers have access to.</span></span> <span data-ttu-id="de8f1-127">È inoltre necessario specificare se un ruolo è necessario per consentire la protezione dell'accesso all'intero componente.</span><span class="sxs-lookup"><span data-stu-id="de8f1-127">You should also specify whether a role is required to help protect access to the entire component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de8f1-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="de8f1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de8f1-129">Autenticazione client</span><span class="sxs-lookup"><span data-stu-id="de8f1-129">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="de8f1-130">Rappresentazione e delega client</span><span class="sxs-lookup"><span data-stu-id="de8f1-130">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="de8f1-131">Sicurezza delle applicazioni di libreria</span><span class="sxs-lookup"><span data-stu-id="de8f1-131">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="de8f1-132">Sicurezza delle applicazioni a più livelli</span><span class="sxs-lookup"><span data-stu-id="de8f1-132">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="de8f1-133">Amministrazione della sicurezza basata sui ruoli</span><span class="sxs-lookup"><span data-stu-id="de8f1-133">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="de8f1-134">Uso dei criteri di restrizione software in COM+</span><span class="sxs-lookup"><span data-stu-id="de8f1-134">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
