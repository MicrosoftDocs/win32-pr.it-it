---
title: Interfaccia INapEnforcementClientBinding (NapEnforcementClient. h)
description: I client di imposizione utilizzano per comunicare con NapAgent.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- NAP interfaccia INapEnforcementClientBinding
- Interfaccia NAP di INapEnforcementClientBinding, descrizione
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
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874585"
---
# <a name="inapenforcementclientbinding-interface"></a>Interfaccia INapEnforcementClientBinding

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapEnforcementClientBinding** fornisce metodi che i client di imposizione utilizzano per comunicare con napagent.

## <a name="members"></a>Membri

L'interfaccia **INapEnforcementClientBinding** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapEnforcementClientBinding** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapEnforcementClientBinding** dispone di questi metodi.



| Metodo                                                                                                                           | Descrizione                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientBinding:: CreateConnection**](inapenforcementclientbinding-createconnection-method.md)                   | Utilizzato dalle forze di esecuzione per creare oggetti connessione.<br/>                                                                                                                                                            |
| [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)                         | Usato dal client di imposizione quando necessita di una richiesta di rapporto di integrità per una determinata connessione.<br/>                                                                                                                   |
| [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md)                               | Avvia il servizio NapAgent. Il client di imposizione deve chiamare questo metodo prima di chiamare qualsiasi altro metodo di questa interfaccia.<br/>                                                                            |
| [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | Utilizzato per indicare al NapAgent che una connessione a un client di imposizione è diminuita.<br/>                                                                                                                      |
| [**INapEnforcementClientBinding::NotifySoHChangeFailure**](inapenforcementclientbinding-notifysohchangefailure-method.md)       | Utilizzato dal client di imposizione per informare NapAgent che non è stato possibile elaborare un [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)precedente.<br/> |
| [**INapEnforcementClientBinding::P rocessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md)               | Usato dai client di imposizione ogni volta che ricevono un BLOB di dati SoH-Response dal server di imposizione.<br/>                                                                                                       |
| [**INapEnforcementClientBinding:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md)                           | Conclude il servizio NapAgent per la connessione client.<br/>                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

Tutte le API in questa interfaccia restituiranno RPC \_ E \_ disconnesse se il NapAgent è stato arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

