---
description: Quando si utilizza la sicurezza basata sui ruoli, è possibile utilizzare l'oggetto contesto della chiamata di sicurezza per accedere alle informazioni di sicurezza sulla chiamata corrente.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Accesso alle informazioni sul contesto delle chiamate di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225716"
---
# <a name="accessing-security-call-context-information"></a><span data-ttu-id="735d5-103">Accesso alle informazioni sul contesto delle chiamate di sicurezza</span><span class="sxs-lookup"><span data-stu-id="735d5-103">Accessing Security Call Context Information</span></span>

<span data-ttu-id="735d5-104">Quando si utilizza la sicurezza basata sui ruoli, è possibile utilizzare l'oggetto contesto della chiamata di sicurezza per accedere alle informazioni di sicurezza sulla chiamata corrente.</span><span class="sxs-lookup"><span data-stu-id="735d5-104">When role-based security is being used, the security call context object can be used to access security information about the current call.</span></span>

<span data-ttu-id="735d5-105">Dall'oggetto contesto della chiamata di sicurezza sono disponibili le seguenti raccolte di proprietà:</span><span class="sxs-lookup"><span data-stu-id="735d5-105">The following collections of properties are available from the security call context object:</span></span>

-   [<span data-ttu-id="735d5-106">Raccolta SecurityCallContext</span><span class="sxs-lookup"><span data-stu-id="735d5-106">SecurityCallContext Collection</span></span>](#securitycallcontext-collection)
-   [<span data-ttu-id="735d5-107">Raccolta SecurityCallers</span><span class="sxs-lookup"><span data-stu-id="735d5-107">SecurityCallers Collection</span></span>](#securitycallers-collection)
-   [<span data-ttu-id="735d5-108">Raccolta SecurityIdentity</span><span class="sxs-lookup"><span data-stu-id="735d5-108">SecurityIdentity Collection</span></span>](#securityidentity-collection)
-   [<span data-ttu-id="735d5-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="735d5-109">Related topics</span></span>](#related-topics)

## <a name="securitycallcontext-collection"></a><span data-ttu-id="735d5-110">Raccolta SecurityCallContext</span><span class="sxs-lookup"><span data-stu-id="735d5-110">SecurityCallContext Collection</span></span>



| <span data-ttu-id="735d5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="735d5-111">Property</span></span>                          | <span data-ttu-id="735d5-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="735d5-112">Description</span></span>                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="735d5-113">NumCallers</span><span class="sxs-lookup"><span data-stu-id="735d5-113">NumCallers</span></span><br/>             | <span data-ttu-id="735d5-114">Numero di chiamanti nella catena di chiamate.</span><span class="sxs-lookup"><span data-stu-id="735d5-114">The number of callers in the chain of calls.</span></span><br/>                                                                                |
| <span data-ttu-id="735d5-115">MinAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="735d5-115">MinAuthenticationLevel</span></span><br/> | <span data-ttu-id="735d5-116">Livello di autenticazione meno sicuro di tutti i chiamanti nella catena.</span><span class="sxs-lookup"><span data-stu-id="735d5-116">The least secure authentication level of all callers in the chain.</span></span><br/>                                                          |
| <span data-ttu-id="735d5-117">Chiamanti</span><span class="sxs-lookup"><span data-stu-id="735d5-117">Callers</span></span><br/>                | <span data-ttu-id="735d5-118">Informazioni sull'identità dei chiamanti upstream, sotto forma di raccolta [**SecurityCallers**](securitycallers.md) .</span><span class="sxs-lookup"><span data-stu-id="735d5-118">Information about the identity of upstream callers, in the form of a [**SecurityCallers**](securitycallers.md) collection.</span></span><br/> |
| <span data-ttu-id="735d5-119">DirectCaller</span><span class="sxs-lookup"><span data-stu-id="735d5-119">DirectCaller</span></span><br/>           | <span data-ttu-id="735d5-120">Il chiamante che ha chiamato direttamente l'oggetto (senza chiamanti).</span><span class="sxs-lookup"><span data-stu-id="735d5-120">The caller that called the object directly (with no intervening callers).</span></span> <br/>                                                  |
| <span data-ttu-id="735d5-121">OriginalCaller</span><span class="sxs-lookup"><span data-stu-id="735d5-121">OriginalCaller</span></span><br/>         | <span data-ttu-id="735d5-122">Il chiamante che ha originato la catena di chiamate all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="735d5-122">The caller that originated the chain of calls to the object.</span></span> <br/>                                                               |



 

<span data-ttu-id="735d5-123">Per ulteriori informazioni sull'utilizzo di questa raccolta, gli sviluppatori Microsoft Visual Basic dovrebbero vedere la classe [**SecurityCallContext**](securitycallcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="735d5-123">For more information about how to use this collection, Microsoft Visual Basic developers should see the [**SecurityCallContext**](securitycallcontext.md) class.</span></span> <span data-ttu-id="735d5-124">Gli sviluppatori C e C++ devono fare riferimento a [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="735d5-124">C and C++ developers should refer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="securitycallers-collection"></a><span data-ttu-id="735d5-125">Raccolta SecurityCallers</span><span class="sxs-lookup"><span data-stu-id="735d5-125">SecurityCallers Collection</span></span>

<span data-ttu-id="735d5-126">La raccolta [**SecurityCallers**](securitycallers.md) rappresenta i chiamanti che possono essere recuperati tramite un indice compreso tra 0 e 1 minore di NumCallers, inclusi.</span><span class="sxs-lookup"><span data-stu-id="735d5-126">The [**SecurityCallers**](securitycallers.md) collection represents callers that can be retrieved by using an index between 0 and 1 less than NumCallers, inclusive.</span></span> <span data-ttu-id="735d5-127">Ogni chiamante è rappresentato da un oggetto [**SecurityIdentity**](securityidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="735d5-127">Each caller is represented by a [**SecurityIdentity**](securityidentity.md) object.</span></span>

<span data-ttu-id="735d5-128">Per ulteriori informazioni su questa raccolta, Visual Basic gli sviluppatori dovrebbero vedere la classe [**SecurityCallers**](securitycallers.md) .</span><span class="sxs-lookup"><span data-stu-id="735d5-128">For more information about this collection, Visual Basic developers should see the [**SecurityCallers**](securitycallers.md) class.</span></span> <span data-ttu-id="735d5-129">Gli sviluppatori C e C++ devono fare riferimento a [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span><span class="sxs-lookup"><span data-stu-id="735d5-129">C and C++ developers should refer to [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="securityidentity-collection"></a><span data-ttu-id="735d5-130">Raccolta SecurityIdentity</span><span class="sxs-lookup"><span data-stu-id="735d5-130">SecurityIdentity Collection</span></span>



| <span data-ttu-id="735d5-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="735d5-131">Property</span></span>                         | <span data-ttu-id="735d5-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="735d5-132">Description</span></span>                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="735d5-133">SID</span><span class="sxs-lookup"><span data-stu-id="735d5-133">SID</span></span><br/>                   | <span data-ttu-id="735d5-134">Identificatore di sicurezza per il chiamante.</span><span class="sxs-lookup"><span data-stu-id="735d5-134">The security identifier for the caller.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="735d5-135">AccountName</span><span class="sxs-lookup"><span data-stu-id="735d5-135">AccountName</span></span><br/>           | <span data-ttu-id="735d5-136">Nome dell'account del chiamante.</span><span class="sxs-lookup"><span data-stu-id="735d5-136">The account name of the caller.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="735d5-137">AuthenticationService</span><span class="sxs-lookup"><span data-stu-id="735d5-137">AuthenticationService</span></span><br/> | <span data-ttu-id="735d5-138">Servizio di autenticazione utilizzato, ad esempio NTLMSSP, Kerberos o SSL.</span><span class="sxs-lookup"><span data-stu-id="735d5-138">The authentication service used, such as NTLMSSP, Kerberos, or SSL.</span></span><br/>                                                                                       |
| <span data-ttu-id="735d5-139">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="735d5-139">AuthenticationLevel</span></span><br/>   | <span data-ttu-id="735d5-140">Livello di autenticazione utilizzato, che rappresenta la quantità di protezione utilizzata per la comunicazione con l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="735d5-140">The authentication level used, which represents the amount of protection used when communicating with the object.</span></span><br/>                                         |
| <span data-ttu-id="735d5-141">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="735d5-141">ImpersonationLevel</span></span><br/>    | <span data-ttu-id="735d5-142">Livello di rappresentazione impostato dal client, se è stata utilizzata la rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="735d5-142">The level of impersonation set by the client, if impersonation was used.</span></span> <span data-ttu-id="735d5-143">Questo livello indica la quantità di autorità assegnata al server dal client.</span><span class="sxs-lookup"><span data-stu-id="735d5-143">This level indicates the amount of authority given to the server by the client.</span></span> <br/> |



 

<span data-ttu-id="735d5-144">Per ulteriori informazioni su questa raccolta, Visual Basic gli sviluppatori dovrebbero vedere la classe [**SecurityIdentity**](securityidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="735d5-144">For more information on this collection, Visual Basic developers should see the [**SecurityIdentity**](securityidentity.md) class.</span></span> <span data-ttu-id="735d5-145">Gli sviluppatori C e C++ devono fare riferimento a [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span><span class="sxs-lookup"><span data-stu-id="735d5-145">C and C++ developers should refer to [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="related-topics"></a><span data-ttu-id="735d5-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="735d5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="735d5-147">Verifica dell'appartenenza ai ruoli</span><span class="sxs-lookup"><span data-stu-id="735d5-147">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="735d5-148">Determinare se Role-Based sicurezza è abilitata</span><span class="sxs-lookup"><span data-stu-id="735d5-148">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="735d5-149">Sicurezza del componente a livello di codice</span><span class="sxs-lookup"><span data-stu-id="735d5-149">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 




