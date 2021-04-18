---
description: Consente di accedere al contesto di sicurezza della chiamata corrente, che contiene informazioni sui chiamanti di un oggetto.
ms.assetid: e8ac05fb-6665-4e57-b64e-82d9799d29d4
title: Classe SecurityCallContext (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallContext
api_type:
- COM
ms.openlocfilehash: bd15b7e0317a507a2340cc148bb927bb5d94a37b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321082"
---
# <a name="securitycallcontext-class"></a><span data-ttu-id="c9587-103">Classe SecurityCallContext</span><span class="sxs-lookup"><span data-stu-id="c9587-103">SecurityCallContext class</span></span>

<span data-ttu-id="c9587-104">Consente di accedere al contesto di sicurezza della chiamata corrente, che contiene informazioni sui chiamanti di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="c9587-104">Provides access to the current call's security context, which contains information about an object's callers.</span></span> <span data-ttu-id="c9587-105">Utilizzando questa classe, è anche possibile scoprire se il chiamante diretto di un oggetto è membro di un determinato ruolo e se la sicurezza è abilitata per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c9587-105">Using this class, you can also find out whether an object's direct caller is a member of a particular role and whether security is enabled for the object.</span></span>

<span data-ttu-id="c9587-106">Solo le applicazioni COM+ che usano la sicurezza basata sui ruoli possono accedere alla classe **SecurityCallContext** .</span><span class="sxs-lookup"><span data-stu-id="c9587-106">Only COM+ applications that use role-based security can access the **SecurityCallContext** class.</span></span> <span data-ttu-id="c9587-107">Per ulteriori informazioni sui ruoli, vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="c9587-107">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="c9587-108">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="c9587-108">When to implement</span></span>

<span data-ttu-id="c9587-109">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="c9587-109">This class is implemented by COM+.</span></span>



| <span data-ttu-id="c9587-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9587-110">Requirement</span></span> | <span data-ttu-id="c9587-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c9587-111">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="c9587-112">Interfacce</span><span class="sxs-lookup"><span data-stu-id="c9587-112">Interfaces</span></span> | [<span data-ttu-id="c9587-113">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="c9587-113">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="c9587-114">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="c9587-114">When to use</span></span>

<span data-ttu-id="c9587-115">Usare questa classe per accedere ai metodi di [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="c9587-115">Use this class to access the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9587-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9587-116">Remarks</span></span>

<span data-ttu-id="c9587-117">Non è possibile creare direttamente un oggetto **SecurityCallContext** .</span><span class="sxs-lookup"><span data-stu-id="c9587-117">You cannot directly create a **SecurityCallContext** object.</span></span> <span data-ttu-id="c9587-118">Per usare i metodi di [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), è necessario ottenere un riferimento alla relativa implementazione chiamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), specificando IID \_ ISecurityCallContext per il parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="c9587-118">To use the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span>

<span data-ttu-id="c9587-119">Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="c9587-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="c9587-120">Un oggetto SecurityCallContext può essere dichiarato con "COMSVCSLib. SecurityCallContext" come nome della classe; viene creato chiamando [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="c9587-120">A SecurityCallContext object can be declared using "COMSVCSLib.SecurityCallContext" as the class name; it is created by calling [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9587-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9587-121">Requirements</span></span>



| <span data-ttu-id="c9587-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9587-122">Requirement</span></span> | <span data-ttu-id="c9587-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c9587-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c9587-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9587-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c9587-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c9587-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c9587-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9587-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c9587-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c9587-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c9587-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9587-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9587-129"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9587-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9587-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9587-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9587-131">**GetSecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="c9587-131">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="c9587-132">**ISecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="c9587-132">**ISecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="c9587-133">Sicurezza del componente a livello di codice</span><span class="sxs-lookup"><span data-stu-id="c9587-133">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="c9587-134">Amministrazione della sicurezza basata sui ruoli</span><span class="sxs-lookup"><span data-stu-id="c9587-134">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="c9587-135">**SecurityCallers**</span><span class="sxs-lookup"><span data-stu-id="c9587-135">**SecurityCallers**</span></span>](securitycallers.md)
</dt> <dt>

[<span data-ttu-id="c9587-136">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="c9587-136">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

