---
description: Consente di accedere alle informazioni sui singoli chiamanti in una raccolta di chiamanti. La raccolta rappresenta la catena di chiamate che terminano con la chiamata corrente e ogni chiamante della raccolta rappresenta l'identità di un chiamante.
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: Classe SecurityCallers (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: c757b11bba6a30e8951915e1eace0811b6b6f732
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342191"
---
# <a name="securitycallers-class"></a><span data-ttu-id="21419-104">Classe SecurityCallers</span><span class="sxs-lookup"><span data-stu-id="21419-104">SecurityCallers class</span></span>

<span data-ttu-id="21419-105">Consente di accedere alle informazioni sui singoli chiamanti in una raccolta di chiamanti.</span><span class="sxs-lookup"><span data-stu-id="21419-105">Provides access to information about individual callers in a collection of callers.</span></span> <span data-ttu-id="21419-106">La raccolta rappresenta la catena di chiamate che terminano con la chiamata corrente e ogni chiamante della raccolta rappresenta l'identità di un chiamante.</span><span class="sxs-lookup"><span data-stu-id="21419-106">The collection represents the chain of calls ending with the current call, and each caller in the collection represents the identity of one caller.</span></span> <span data-ttu-id="21419-107">Nella catena di chiamanti vengono inclusi solo i chiamanti che superano un limite in cui è selezionata la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="21419-107">Only callers who cross a boundary where security is checked are included in the chain of callers.</span></span> <span data-ttu-id="21419-108">Nell'ambiente COM+, la sicurezza viene controllata ai limiti dell'applicazione. L'accesso alle informazioni relative all'identità di un determinato chiamante viene fornito tramite la classe [**SecurityIdentity**](securityidentity.md) , una raccolta di identità.</span><span class="sxs-lookup"><span data-stu-id="21419-108">(In the COM+ environment, security is checked at application boundaries.) Access to information about a particular caller's identity is provided through the [**SecurityIdentity**](securityidentity.md) class, an identity collection.</span></span>

<span data-ttu-id="21419-109">Solo le applicazioni COM+ che usano la sicurezza basata sui ruoli possono accedere alla classe **SecurityCallers** .</span><span class="sxs-lookup"><span data-stu-id="21419-109">Only COM+ applications that use role-based security can access the **SecurityCallers** class.</span></span> <span data-ttu-id="21419-110">Per ulteriori informazioni sui ruoli, vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="21419-110">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="21419-111">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="21419-111">When to implement</span></span>

<span data-ttu-id="21419-112">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="21419-112">This class is implemented by COM+.</span></span>



| <span data-ttu-id="21419-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="21419-113">Requirement</span></span> | <span data-ttu-id="21419-114">Valore</span><span class="sxs-lookup"><span data-stu-id="21419-114">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="21419-115">Interfacce</span><span class="sxs-lookup"><span data-stu-id="21419-115">Interfaces</span></span> | [<span data-ttu-id="21419-116">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="21419-116">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="21419-117">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="21419-117">When to use</span></span>

<span data-ttu-id="21419-118">Usare questa classe per accedere ai metodi di [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span><span class="sxs-lookup"><span data-stu-id="21419-118">Use this class to access the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="21419-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="21419-119">Remarks</span></span>

<span data-ttu-id="21419-120">Non è possibile creare direttamente un oggetto **SecurityCallers** .</span><span class="sxs-lookup"><span data-stu-id="21419-120">You cannot directly create a **SecurityCallers** object.</span></span> <span data-ttu-id="21419-121">Per usare i metodi di [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), è necessario ottenere un riferimento alla relativa implementazione chiamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), specificando IID \_ ISecurityCallContext per il parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="21419-121">To use the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="21419-122">Successivamente, chiamare [**ISecurityCallContext:: Get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) che richiede un elemento del contesto della chiamata di sicurezza che è una raccolta di identità di sicurezza, ad esempio "DirectCaller" o "OriginalCaller".</span><span class="sxs-lookup"><span data-stu-id="21419-122">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

<span data-ttu-id="21419-123">Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="21419-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="21419-124">Non è possibile creare direttamente un oggetto SecurityCallers.</span><span class="sxs-lookup"><span data-stu-id="21419-124">You cannot directly create a SecurityCallers object.</span></span> <span data-ttu-id="21419-125">Per usare le proprietà, è necessario ottenere un Refernece per la relativa implementazione usando [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="21419-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="21419-126">Ottenere quindi la proprietà Item dell'oggetto, richiedendo un elemento del contesto della chiamata di sicurezza che è una raccolta di identità di sicurezza (ad esempio "DirectCaller" o "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="21419-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

## <a name="requirements"></a><span data-ttu-id="21419-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21419-127">Requirements</span></span>



| <span data-ttu-id="21419-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="21419-128">Requirement</span></span> | <span data-ttu-id="21419-129">Valore</span><span class="sxs-lookup"><span data-stu-id="21419-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="21419-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21419-130">Minimum supported client</span></span><br/> | <span data-ttu-id="21419-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="21419-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="21419-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21419-132">Minimum supported server</span></span><br/> | <span data-ttu-id="21419-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="21419-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="21419-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21419-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="21419-135"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="21419-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21419-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21419-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21419-137">**GetSecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="21419-137">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="21419-138">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="21419-138">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="21419-139">Sicurezza del componente a livello di codice</span><span class="sxs-lookup"><span data-stu-id="21419-139">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="21419-140">Amministrazione della sicurezza basata sui ruoli</span><span class="sxs-lookup"><span data-stu-id="21419-140">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="21419-141">**SecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="21419-141">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="21419-142">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="21419-142">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

