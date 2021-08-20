---
title: Interfaccia INapEnforcementClientBinding (NapEnforcementClient.h)
description: I client di imposizione usano per comunicare con NapAgent.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- Interfaccia INapEnforcementClientBinding NAP
- Interfaccia INapEnforcementClientBinding NAP, descritta
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdad90e7f96a981a28e4c44351d5a2a4f55c75184826154e0e2effba54157049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134067"
---
# <a name="inapenforcementclientbinding-interface"></a>Interfaccia INapEnforcementClientBinding

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapEnforcementClientBinding fornisce** metodi che i client di imposizione usano per comunicare con NapAgent.

## <a name="members"></a>Membri

**L'interfaccia INapEnforcementClientBinding** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapEnforcementClientBinding** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapEnforcementClientBinding** include questi metodi.



| Metodo                                                                                                                           | Descrizione                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientBinding::CreateConnection**](inapenforcementclientbinding-createconnection-method.md)                   | Utilizzato dagli imponitori per creare oggetti connessione.<br/>                                                                                                                                                            |
| [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)                         | Usato dal client di imposizione quando necessita di una richiesta SoH per una connessione specifica.<br/>                                                                                                                   |
| [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md)                               | Avvia il servizio NapAgent. Il client di imposizione deve chiamare questo metodo prima di chiamare qualsiasi altro metodo di questa interfaccia.<br/>                                                                            |
| [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | Usato per informare NapAgent che una connessione a un client di imposizione è stata erta.<br/>                                                                                                                      |
| [**INapEnforcementClientBinding::NotifySoHChangeFailure**](inapenforcementclientbinding-notifysohchangefailure-method.md)       | Usato dal client di imposizione per informare NapAgent che non è stato possibile elaborare un [**oggetto INapEnforcementClientCallback::NotifySoHChange precedente.**](inapenforcementclientcallback-notifysohchange-method.md)<br/> |
| [**INapEnforcementClientBinding::P rocessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md)               | Usato dai client di imposizione ogni volta che ottengono SoH-Response BLOB di dati dal server di imposizione.<br/>                                                                                                       |
| [**INapEnforcementClientBinding::Uninitialize**](inapenforcementclientbinding-uninitialize-method.md)                           | Conclude il servizio NapAgent per questa connessione client.<br/>                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

Tutte le API in questa interfaccia restituiranno RPC \_ E \_ DISCONNECTED se NapAgent viene arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, dopo il riavvio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

