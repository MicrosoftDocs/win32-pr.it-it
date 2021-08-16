---
description: Fornisce l'accesso alle informazioni sui singoli chiamanti in una raccolta di chiamanti. La raccolta rappresenta la catena di chiamate che termina con la chiamata corrente e ogni chiamante nella raccolta rappresenta l'identità di un chiamante.
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: Classe SecurityCallers (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: a494e1421e443d2a6c3663bd7fa7c15eda898079477592e8df9958a2d5b87990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915895"
---
# <a name="securitycallers-class"></a>Classe SecurityCallers

Fornisce l'accesso alle informazioni sui singoli chiamanti in una raccolta di chiamanti. La raccolta rappresenta la catena di chiamate che termina con la chiamata corrente e ogni chiamante nella raccolta rappresenta l'identità di un chiamante. Nella catena di chiamanti vengono inclusi solo i chiamanti che superano un limite in cui viene verificata la sicurezza. Nell'ambiente COM+ la sicurezza viene controllata ai limiti dell'applicazione. L'accesso alle informazioni sull'identità di un determinato chiamante viene fornito tramite la [**classe SecurityIdentity,**](securityidentity.md) una raccolta di identità.

Solo le applicazioni COM+ che usano la sicurezza basata sui ruoli possono accedere alla **classe SecurityCallers.** Per altre informazioni sui ruoli, vedere [Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).

## <a name="when-to-implement"></a>Quando implementare

Questa classe viene implementata da COM+.



| Requisito | Valore |
|------------|------------------------------------------------------|
| Interfacce | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>Utilizzo

Usare questa classe per accedere ai metodi di [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).

## <a name="remarks"></a>Commenti

Non è possibile creare direttamente un **oggetto SecurityCallers.** Per usare i metodi di [**ISecurityCallersColl,**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)è necessario ottenere un riferimento alla relativa implementazione chiamando [**CoGetCallContext,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext)fornendo IID ISecurityCallContext per il \_ parametro *riid.* Chiamare quindi [**ISecurityCallContext::get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) per richiedere un elemento del contesto di chiamata di sicurezza che sia una raccolta di identità di sicurezza, ad esempio "DirectCaller" o "OriginalCaller".

Per usare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi dei servizi COM+. Non è possibile creare direttamente un oggetto SecurityCallers. Per usare le relative proprietà, è necessario ottenere un riferimento alla relativa implementazione usando [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext). Ottenere quindi la proprietà Item dell'oggetto, richiedendo un elemento del contesto di chiamata di sicurezza che sia una raccolta di identità di sicurezza, ad esempio "DirectCaller" o "OriginalCaller".

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

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 

