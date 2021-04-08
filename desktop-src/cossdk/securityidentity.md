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
# <a name="securityidentity-class"></a>Classe SecurityIdentity

Consente di accedere a una raccolta di informazioni di sicurezza che rappresenta l'identità di un chiamante. Utilizzando questa classe, è possibile trovare informazioni su un particolare chiamante in una catena di chiamanti che fa parte del contesto di chiamata di sicurezza. Per ulteriori informazioni sull'accesso alle informazioni sul contesto delle chiamate di sicurezza, vedere sicurezza dei componenti programmatici.

Solo le applicazioni COM+ che usano la sicurezza basata sui ruoli possono accedere alla classe **SecurityIdentity** . Per ulteriori informazioni sui ruoli, vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).

## <a name="when-to-implement"></a>Quando implementare

Questa classe è implementata da COM+.



| Requisito | Valore |
|------------|--------------------------------------------------------|
| Interfacce | [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a>Utilizzo

Usare questa classe per accedere ai metodi di [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).

## <a name="remarks"></a>Commenti

Non è possibile creare direttamente un oggetto **SecurityIdentity** . Per usare i metodi di [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), è necessario ottenere un riferimento alla relativa implementazione chiamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), specificando IID \_ ISecurityCallContext per il parametro *riid* . Successivamente, chiamare [**ISecurityCallContext:: Get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) che richiede un elemento del contesto della chiamata di sicurezza che è una raccolta di identità di sicurezza, ad esempio "DirectCaller" o "OriginalCaller". Chiamare quindi [**ISecurityIdentityColl:: Get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) per recuperare un elemento Identity di sicurezza, ad esempio "Name" o "AuthenticationService".

Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+. Non è possibile creare direttamente un oggetto SecurityIdentity. Per usare le proprietà, è necessario ottenere un Refernece per la relativa implementazione usando [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext). Ottenere quindi la proprietà Item dell'oggetto, richiedendo un elemento del contesto della chiamata di sicurezza che è una raccolta di identità di sicurezza (ad esempio "DirectCaller" o "OriginalCaller"). Usare quindi la proprietà Item dell'oggetto SecurityIdentity per recuperare un elemento Identity di sicurezza, ad esempio "Name" o "AuthenticationService".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[Sicurezza del componente a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallContext**](securitycallcontext.md)
</dt> <dt>

[**SecurityCallers**](securitycallers.md)
</dt> </dl>

 

