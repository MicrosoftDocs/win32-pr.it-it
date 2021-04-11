---
description: Determinare se Role-Based sicurezza è abilitata
ms.assetid: b5e6ab7e-5a77-4c6f-9bec-02942bba389d
title: Determinare se Role-Based sicurezza è abilitata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ccf6f95b9c8776a45c071f6d4ea3326eda035c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127551"
---
# <a name="determining-whether-role-based-security-is-enabled"></a><span data-ttu-id="5d61e-103">Determinare se Role-Based sicurezza è abilitata</span><span class="sxs-lookup"><span data-stu-id="5d61e-103">Determining Whether Role-Based Security Is Enabled</span></span>

<span data-ttu-id="5d61e-104">Utilizzando il metodo [**ISecurityCallContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) disponibile nell'oggetto contesto della chiamata di sicurezza, è possibile determinare se la sicurezza è abilitata per l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="5d61e-104">By using the [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) method available from the security call context object, you can determine whether security is enabled for the current object.</span></span> <span data-ttu-id="5d61e-105">È necessario chiamare **IsSecurityEnabled** prima di usare ISecurityCallContext::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) per controllare l'appartenenza al ruolo perché **IsCallerInRole** restituisce true se la sicurezza non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="5d61e-105">You should call **IsSecurityEnabled** before you use ISecurityCallContext::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) to check role membership because **IsCallerInRole** returns True if security is not enabled.</span></span>

<span data-ttu-id="5d61e-106">Gli sviluppatori Microsoft Visual Basic chiamano [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) per ottenere un riferimento a un oggetto [**SecurityCallContext**](securitycallcontext.md) e quindi chiamano [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="5d61e-106">Microsoft Visual Basic developers call [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) to obtain a reference to a [**SecurityCallContext**](securitycallcontext.md) object and then call [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), as shown in the following example:</span></span>


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



<span data-ttu-id="5d61e-107">Microsoft Visual C++ gli sviluppatori possono chiamare [**ISecurityCallContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) chiamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) per ottenere un puntatore a [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) e quindi chiamare **IsSecurityEnabled**.</span><span class="sxs-lookup"><span data-stu-id="5d61e-107">Microsoft Visual C++ developers can call [**ISecurityCallContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) and then calling **IsSecurityEnabled**.</span></span> <span data-ttu-id="5d61e-108">Un breve esempio segue:</span><span class="sxs-lookup"><span data-stu-id="5d61e-108">A brief example follows:</span></span>


```C++
ISecurityCallContext* pSecCtx;
VARIANT_BOOL bIsEnabled;

HRESULT hr1 = CoGetCallContext(IID_ISecurityCallContext, (void**)&pSecCtx);
if (FAILED(hr1)) throw(hr1);
if (NULL == pSecCtx) {
    // Display error message.
    return E_FAIL;
}

HRESULT hr2 = pSecCtx->IsSecurityEnabled(&bIsEnabled);
return hr2;
```



<span data-ttu-id="5d61e-109">Sebbene il modo migliore per chiamare [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) consiste nell'usare l'oggetto contesto di chiamata di sicurezza, è anche possibile chiamare **IsSecurityEnabled** tramite il contesto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5d61e-109">Although the preferred way to call [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) is by using the security call context object, you can also call **IsSecurityEnabled** through the object context.</span></span> <span data-ttu-id="5d61e-110">Per ulteriori informazioni, vedere [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) o [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .</span><span class="sxs-lookup"><span data-stu-id="5d61e-110">(See [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) or [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) for more information.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d61e-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d61e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d61e-112">Accesso alle informazioni sul contesto delle chiamate di sicurezza</span><span class="sxs-lookup"><span data-stu-id="5d61e-112">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="5d61e-113">Verifica dell'appartenenza ai ruoli</span><span class="sxs-lookup"><span data-stu-id="5d61e-113">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="5d61e-114">Sicurezza del componente a livello di codice</span><span class="sxs-lookup"><span data-stu-id="5d61e-114">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 
