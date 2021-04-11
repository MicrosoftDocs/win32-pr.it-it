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
# <a name="determining-whether-role-based-security-is-enabled"></a>Determinare se Role-Based sicurezza è abilitata

Utilizzando il metodo [**ISecurityCallContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) disponibile nell'oggetto contesto della chiamata di sicurezza, è possibile determinare se la sicurezza è abilitata per l'oggetto corrente. È necessario chiamare **IsSecurityEnabled** prima di usare ISecurityCallContext::[**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) per controllare l'appartenenza al ruolo perché **IsCallerInRole** restituisce true se la sicurezza non è abilitata.

Gli sviluppatori Microsoft Visual Basic chiamano [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) per ottenere un riferimento a un oggetto [**SecurityCallContext**](securitycallcontext.md) e quindi chiamano [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled), come illustrato nell'esempio seguente:


```VB
Dim objSecCallCtx As SecurityCallContext
Dim boolSecEn As Boolean
Set objSecCallCtx = GetSecurityCallContext()
boolSecEn = objSecCallCtx.IsSecurityEnabled()
 
```



Microsoft Visual C++ gli sviluppatori possono chiamare [**ISecurityCallContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) chiamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) per ottenere un puntatore a [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) e quindi chiamare **IsSecurityEnabled**. Un breve esempio segue:


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



Sebbene il modo migliore per chiamare [**IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled) consiste nell'usare l'oggetto contesto di chiamata di sicurezza, è anche possibile chiamare **IsSecurityEnabled** tramite il contesto dell'oggetto. Per ulteriori informazioni, vedere [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) o [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alle informazioni sul contesto delle chiamate di sicurezza](accessing-security-call-context-information.md)
</dt> <dt>

[Verifica dell'appartenenza ai ruoli](checking-role-membership.md)
</dt> <dt>

[Sicurezza del componente a livello di codice](programmatic-component-security.md)
</dt> </dl>

 

 
