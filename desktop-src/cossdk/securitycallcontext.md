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
# <a name="securitycallcontext-class"></a>Classe SecurityCallContext

Consente di accedere al contesto di sicurezza della chiamata corrente, che contiene informazioni sui chiamanti di un oggetto. Utilizzando questa classe, è anche possibile scoprire se il chiamante diretto di un oggetto è membro di un determinato ruolo e se la sicurezza è abilitata per l'oggetto.

Solo le applicazioni COM+ che usano la sicurezza basata sui ruoli possono accedere alla classe **SecurityCallContext** . Per ulteriori informazioni sui ruoli, vedere [amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md).

## <a name="when-to-implement"></a>Quando implementare

Questa classe è implementata da COM+.



| Requisito | Valore |
|------------|------------------------------------------------------|
| Interfacce | [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a>Utilizzo

Usare questa classe per accedere ai metodi di [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).

## <a name="remarks"></a>Commenti

Non è possibile creare direttamente un oggetto **SecurityCallContext** . Per usare i metodi di [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), è necessario ottenere un riferimento alla relativa implementazione chiamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), specificando IID \_ ISecurityCallContext per il parametro *riid* .

Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+. Un oggetto SecurityCallContext può essere dichiarato con "COMSVCSLib. SecurityCallContext" come nome della classe; viene creato chiamando [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).

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

[**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)
</dt> <dt>

[Sicurezza del componente a livello di codice](programmatic-component-security.md)
</dt> <dt>

[Amministrazione della sicurezza basata sui ruoli](role-based-security-administration.md)
</dt> <dt>

[**SecurityCallers**](securitycallers.md)
</dt> <dt>

[**SecurityIdentity**](securityidentity.md)
</dt> </dl>

 

