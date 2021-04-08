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
# <a name="checking-role-membership"></a>Verifica dell'appartenenza ai ruoli

È possibile chiamare il metodo [**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) per determinare se il chiamante diretto di un oggetto è un membro di un ruolo specifico. Questa funzionalità è utile quando si desidera garantire che non venga eseguito un determinato blocco di codice, a meno che il chiamante non sia membro di un ruolo specifico.

Ad esempio, è possibile usare [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) per garantire che le transazioni in un importo specificato, ad esempio $1000, vengano eseguite solo dai membri di un ruolo managers. Se il chiamante non è un gestore e la transazione è superiore a $1000, la transazione non viene eseguita e viene visualizzato un messaggio di errore.

Il modo migliore per accedere a [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole) è tramite l'oggetto contesto di chiamata di sicurezza perché è possibile utilizzare lo stesso riferimento all'oggetto contesto della chiamata di sicurezza per ottenere le proprietà di sicurezza. Tuttavia, è anche possibile accedere al metodo **IsCallerInRole** dall'oggetto **ObjectContext** . Per ulteriori informazioni, vedere [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) o [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) .

Se si sviluppano componenti per un'applicazione Visual Basic Microsoft, chiamare la funzione [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) e quindi usare il contesto della chiamata di sicurezza per chiamare [**IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), come illustrato nell'esempio seguente:


```VB
If (GetSecurityCallContext.IsCallerInRole("Manager")) Then
   ' Go ahead and perform the transaction.
Else
   ' Display an error message.
End If
```



Se si sta sviluppando un'applicazione C o C++, usare [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) per recuperare un puntatore all'interfaccia [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) . Quindi si chiama [**ISecurityCallContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole), come illustrato nell'esempio seguente:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alle informazioni sul contesto delle chiamate di sicurezza](accessing-security-call-context-information.md)
</dt> <dt>

[Determinare se Role-Based sicurezza è abilitata](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[Sicurezza del componente a livello di codice](programmatic-component-security.md)
</dt> </dl>

 

 
