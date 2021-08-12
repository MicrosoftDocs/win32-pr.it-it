---
description: Fornisce l'accesso a una raccolta di informazioni di sicurezza che rappresentano l'identità di un chiamante. Usando questa classe, è possibile trovare informazioni su un determinato chiamante in una catena di chiamanti che fa parte del contesto della chiamata di sicurezza.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: Classe SecurityIdentity (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: d16139ccf60a22ebfb4cf609e734e0b8df3285ef9ddb1804657313900a3ea05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305477"
---
# <a name="securityidentity-class"></a>Classe SecurityIdentity

Fornisce l'accesso a una raccolta di informazioni di sicurezza che rappresentano l'identità di un chiamante. Usando questa classe, è possibile trovare informazioni su un determinato chiamante in una catena di chiamanti che fa parte del contesto della chiamata di sicurezza. Per altre informazioni sull'accesso alle informazioni sul contesto delle chiamate di sicurezza, vedere Sicurezza dei componenti a livello di codice.

Solo le applicazioni COM+ che usano la sicurezza basata sui ruoli possono accedere **alla classe SecurityIdentity.** Per altre informazioni sui ruoli, vedere [Amministrazione della sicurezza basata sui ruoli.](role-based-security-administration.md)

## <a name="when-to-implement"></a>Quando implementare

Questa classe viene implementata da COM+.



| Requisito | Valore |
|------------|--------------------------------------------------------|
| Interfacce | [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a>Utilizzo

Usare questa classe per accedere ai metodi di [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).

## <a name="remarks"></a>Commenti

Non è possibile creare direttamente **un oggetto SecurityIdentity.** Per usare i metodi di [**ISecurityIdentityColl,**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)è necessario ottenere un riferimento alla relativa implementazione chiamando [**CoGetCallContext,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)fornendo IID ISecurityCallContext per il \_ parametro *riid.* Chiamare quindi [**ISecurityCallContext::get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) richiedendo un elemento del contesto di chiamata di sicurezza che sia una raccolta di identità di sicurezza, ad esempio "DirectCaller" o "OriginalCaller". Chiamare quindi [**ISecurityIdentityColl::get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) per recuperare un elemento di identità di sicurezza, ad esempio "Name" o "AuthenticationService".

Per usare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi dei servizi COM+. Non è possibile creare direttamente un oggetto SecurityIdentity. Per usare le relative proprietà, è necessario ottenere un riferimento alla relativa implementazione usando [**GetSecurityCallContext.**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) Ottenere quindi la proprietà Item dell'oggetto , richiedendo un elemento del contesto di chiamata di sicurezza che sia una raccolta di identità di sicurezza, ad esempio "DirectCaller" o "OriginalCaller". Usare quindi la proprietà Item dell'oggetto SecurityIdentity per recuperare un elemento di identità di sicurezza, ad esempio "Name" o "AuthenticationService".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[Sicurezza dei componenti a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallContext**](securitycallcontext.md)
</dt> <dt>

[**SecurityCallers**](securitycallers.md)
</dt> </dl>

 

