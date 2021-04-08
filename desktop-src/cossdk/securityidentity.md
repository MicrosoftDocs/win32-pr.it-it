---
description: Consente di accedere a una raccolta di informazioni di sicurezza che rappresenta l'identità di un chiamante. Utilizzando questa classe, è possibile trovare informazioni su un particolare chiamante in una catena di chiamanti che fa parte del contesto di chiamata di sicurezza.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: Classe SecurityIdentity (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: 6775c06bc25bfb32a1c2c247868fd2a9fbc9aade
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103761555"
---
# <a name="securityidentity-class"></a><span data-ttu-id="5ed31-104">Classe SecurityIdentity</span><span class="sxs-lookup"><span data-stu-id="5ed31-104">SecurityIdentity class</span></span>

<span data-ttu-id="5ed31-105">Consente di accedere a una raccolta di informazioni di sicurezza che rappresenta l'identità di un chiamante.</span><span class="sxs-lookup"><span data-stu-id="5ed31-105">Provides access to a collection of security information representing a caller's identity.</span></span> <span data-ttu-id="5ed31-106">Utilizzando questa classe, è possibile trovare informazioni su un particolare chiamante in una catena di chiamanti che fa parte del contesto di chiamata di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="5ed31-106">Using this class, you can find out about a particular caller in a chain of callers that is part of the security call context.</span></span> <span data-ttu-id="5ed31-107">Per ulteriori informazioni sull'accesso alle informazioni sul contesto delle chiamate di sicurezza, vedere sicurezza dei componenti programmatici.</span><span class="sxs-lookup"><span data-stu-id="5ed31-107">For more information about how security call context information is accessed, see Programmatic Component Security.</span></span>

<span data-ttu-id="5ed31-108">Solo le applicazioni COM+ che usano la sicurezza basata sui ruoli possono accedere alla classe **SecurityIdentity** .</span><span class="sxs-lookup"><span data-stu-id="5ed31-108">Only COM+ applications that use role-based security can access the **SecurityIdentity** class.</span></span> <span data-ttu-id="5ed31-109">Per ulteriori informazioni sui ruoli, vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="5ed31-109">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="5ed31-110">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="5ed31-110">When to implement</span></span>

<span data-ttu-id="5ed31-111">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="5ed31-111">This class is implemented by COM+.</span></span>



| <span data-ttu-id="5ed31-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ed31-112">Requirement</span></span> | <span data-ttu-id="5ed31-113">Valore</span><span class="sxs-lookup"><span data-stu-id="5ed31-113">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="5ed31-114">Interfacce</span><span class="sxs-lookup"><span data-stu-id="5ed31-114">Interfaces</span></span> | [<span data-ttu-id="5ed31-115">**ISecurityIdentityColl**</span><span class="sxs-lookup"><span data-stu-id="5ed31-115">**ISecurityIdentityColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="5ed31-116">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="5ed31-116">When to use</span></span>

<span data-ttu-id="5ed31-117">Usare questa classe per accedere ai metodi di [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span><span class="sxs-lookup"><span data-stu-id="5ed31-117">Use this class to access the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="5ed31-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ed31-118">Remarks</span></span>

<span data-ttu-id="5ed31-119">Non è possibile creare direttamente un oggetto **SecurityIdentity** .</span><span class="sxs-lookup"><span data-stu-id="5ed31-119">You cannot directly create a **SecurityIdentity** object.</span></span> <span data-ttu-id="5ed31-120">Per usare i metodi di [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), è necessario ottenere un riferimento alla relativa implementazione chiamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), specificando IID \_ ISecurityCallContext per il parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="5ed31-120">To use the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="5ed31-121">Successivamente, chiamare [**ISecurityCallContext:: Get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) che richiede un elemento del contesto della chiamata di sicurezza che è una raccolta di identità di sicurezza, ad esempio "DirectCaller" o "OriginalCaller".</span><span class="sxs-lookup"><span data-stu-id="5ed31-121">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="5ed31-122">Chiamare quindi [**ISecurityIdentityColl:: Get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) per recuperare un elemento Identity di sicurezza, ad esempio "Name" o "AuthenticationService".</span><span class="sxs-lookup"><span data-stu-id="5ed31-122">Then call [**ISecurityIdentityColl::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

<span data-ttu-id="5ed31-123">Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="5ed31-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="5ed31-124">Non è possibile creare direttamente un oggetto SecurityIdentity.</span><span class="sxs-lookup"><span data-stu-id="5ed31-124">You cannot directly create a SecurityIdentity object.</span></span> <span data-ttu-id="5ed31-125">Per usare le proprietà, è necessario ottenere un Refernece per la relativa implementazione usando [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="5ed31-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="5ed31-126">Ottenere quindi la proprietà Item dell'oggetto, richiedendo un elemento del contesto della chiamata di sicurezza che è una raccolta di identità di sicurezza (ad esempio "DirectCaller" o "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="5ed31-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="5ed31-127">Usare quindi la proprietà Item dell'oggetto SecurityIdentity per recuperare un elemento Identity di sicurezza, ad esempio "Name" o "AuthenticationService".</span><span class="sxs-lookup"><span data-stu-id="5ed31-127">Then, use the Item property of the SecurityIdentity object to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed31-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ed31-128">Requirements</span></span>



| <span data-ttu-id="5ed31-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ed31-129">Requirement</span></span> | <span data-ttu-id="5ed31-130">Valore</span><span class="sxs-lookup"><span data-stu-id="5ed31-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed31-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ed31-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed31-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5ed31-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5ed31-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ed31-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed31-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5ed31-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5ed31-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ed31-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ed31-136"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ed31-136"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ed31-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ed31-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed31-138">**GetSecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="5ed31-138">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="5ed31-139">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="5ed31-139">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="5ed31-140">Sicurezza del componente a livello di codice</span><span class="sxs-lookup"><span data-stu-id="5ed31-140">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="5ed31-141">Amministrazione della sicurezza basata sui ruoli</span><span class="sxs-lookup"><span data-stu-id="5ed31-141">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="5ed31-142">**SecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="5ed31-142">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="5ed31-143">**SecurityCallers**</span><span class="sxs-lookup"><span data-stu-id="5ed31-143">**SecurityCallers**</span></span>](securitycallers.md)
</dt> </dl>

 

