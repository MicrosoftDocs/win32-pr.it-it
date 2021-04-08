---
description: Verifica dell'appartenenza ai ruoli
ms.assetid: 690cab3f-4476-4fce-b842-d63a4d0d5c6f
title: Verifica dell'appartenenza ai ruoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 777d47b36d2eea79d8b16e7025839b696c38ff87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748671"
---
# <a name="checking-role-membership"></a><span data-ttu-id="6f321-103">Verifica dell'appartenenza ai ruoli</span><span class="sxs-lookup"><span data-stu-id="6f321-103">Checking Role Membership</span></span>

<span data-ttu-id="6f321-104">È possibile chiamare il metodo [**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) per determinare se il chiamante diretto di un oggetto è un membro di un ruolo specifico.</span><span class="sxs-lookup"><span data-stu-id="6f321-104">You can call the [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) method to determine whether an object's direct caller is a member of a particular role.</span></span> <span data-ttu-id="6f321-105">Questa funzionalità è utile quando si desidera garantire che non venga eseguito un determinato blocco di codice, a meno che il chiamante non sia membro di un ruolo specifico.</span><span class="sxs-lookup"><span data-stu-id="6f321-105">This functionality is useful when you want to ensure that a certain block of code is not executed unless the caller is a member of a particular role.</span></span>

<span data-ttu-id="6f321-106">Ad esempio, è possibile usare [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) per garantire che le transazioni in un importo specificato, ad esempio $1000, vengano eseguite solo dai membri di un ruolo managers.</span><span class="sxs-lookup"><span data-stu-id="6f321-106">For example, you could use [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) to ensure that transactions over a specified amount, such as $1000, are performed only by members of a Managers role.</span></span> <span data-ttu-id="6f321-107">Se il chiamante non è un gestore e la transazione è superiore a $1000, la transazione non viene eseguita e viene visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="6f321-107">If the caller is not a Manager and the transaction is over $1000, the transaction is not performed and an error message is displayed.</span></span>

<span data-ttu-id="6f321-108">Il modo migliore per accedere a [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) è tramite l'oggetto contesto di chiamata di sicurezza perché è possibile utilizzare lo stesso riferimento all'oggetto contesto della chiamata di sicurezza per ottenere le proprietà di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6f321-108">The preferred way to access [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) is through the security call context object because you can use the same reference to the security call context object to obtain security properties.</span></span> <span data-ttu-id="6f321-109">Tuttavia, è anche possibile accedere al metodo **IsCallerInRole** dall'oggetto **ObjectContext** .</span><span class="sxs-lookup"><span data-stu-id="6f321-109">However, you can also access the **IsCallerInRole** method from the **ObjectContext** object.</span></span> <span data-ttu-id="6f321-110">Per ulteriori informazioni, vedere [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) o [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .</span><span class="sxs-lookup"><span data-stu-id="6f321-110">(See [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) or [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) for more information.)</span></span>

<span data-ttu-id="6f321-111">Se si sviluppano componenti per un'applicazione Visual Basic Microsoft, chiamare la funzione [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) e quindi usare il contesto della chiamata di sicurezza per chiamare [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="6f321-111">If you are developing components for a Microsoft Visual Basic application, you call the [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) function and then use the security call context to call [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), as shown in the following example:</span></span>


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



<span data-ttu-id="6f321-112">Se si sta sviluppando un'applicazione C o C++, usare [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) per recuperare un puntatore all'interfaccia [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) .</span><span class="sxs-lookup"><span data-stu-id="6f321-112">If you are developing a C or C++ application, use [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to retrieve a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface.</span></span> <span data-ttu-id="6f321-113">Quindi si chiama [**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="6f321-113">Then you call [**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), as shown in the following example:</span></span>


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsInRole;

HRESULT hr = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr)) throw(hr);
if (NULL == pSecCtx) { 
    // No security call context is available.
    // Display an error message and return.
    return E_FAIL;
}
hr = pSecCtx->IsCallerInRole(myRole, &bIsInRole);
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="6f321-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f321-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f321-115">Accesso alle informazioni sul contesto delle chiamate di sicurezza</span><span class="sxs-lookup"><span data-stu-id="6f321-115">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="6f321-116">Determinare se Role-Based sicurezza è abilitata</span><span class="sxs-lookup"><span data-stu-id="6f321-116">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="6f321-117">Sicurezza del componente a livello di codice</span><span class="sxs-lookup"><span data-stu-id="6f321-117">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 
