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
# <a name="securitycallers-class"></a>Classe SecurityCallers

Consente di accedere alle informazioni sui singoli chiamanti in una raccolta di chiamanti. La raccolta rappresenta la catena di chiamate che terminano con la chiamata corrente e ogni chiamante della raccolta rappresenta l'identità di un chiamante. Nella catena di chiamanti vengono inclusi solo i chiamanti che superano un limite in cui è selezionata la sicurezza. Nell'ambiente COM+, la sicurezza viene controllata ai limiti dell'applicazione. L'accesso alle informazioni relative all'identità di un determinato chiamante viene fornito tramite la classe [**SecurityIdentity**](securityidentity.md) , una raccolta di identità.

Solo le applicazioni COM+ che usano la sicurezza basata sui ruoli possono accedere alla classe **SecurityCallers** . Per ulteriori informazioni sui ruoli, vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).

## <a name="when-to-implement"></a>Quando implementare

Questa classe è implementata da COM+.



| Requisito | Valore |
|------------|------------------------------------------------------|
| Interfacce | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>Utilizzo

Usare questa classe per accedere ai metodi di [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).

## <a name="remarks"></a>Commenti

Non è possibile creare direttamente un oggetto **SecurityCallers** . Per usare i metodi di [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), è necessario ottenere un riferimento alla relativa implementazione chiamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), specificando IID \_ ISecurityCallContext per il parametro *riid* . Successivamente, chiamare [**ISecurityCallContext:: Get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) che richiede un elemento del contesto della chiamata di sicurezza che è una raccolta di identità di sicurezza, ad esempio "DirectCaller" o "OriginalCaller".

Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+. Non è possibile creare direttamente un oggetto SecurityCallers. Per usare le proprietà, è necessario ottenere un Refernece per la relativa implementazione usando [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext). Ottenere quindi la proprietà Item dell'oggetto, richiedendo un elemento del contesto della chiamata di sicurezza che è una raccolta di identità di sicurezza (ad esempio "DirectCaller" o "OriginalCaller").

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

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 

