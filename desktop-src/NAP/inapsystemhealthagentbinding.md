---
title: Interfaccia INapSystemHealthAgentBinding (NapSystemHealthAgent.h)
description: Gli SHA usano per comunicare con NapAgent. | Interfaccia INapSystemHealthAgentBinding (NapSystemHealthAgent.h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- Interfaccia INapSystemHealthAgentBinding NAP
- Interfaccia INapSystemHealthAgentBinding NAP, descritta
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38fe66a5cd6883114ff46da3e98174d299f1813e670ed5ce67ee3843dc210d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799186"
---
# <a name="inapsystemhealthagentbinding-interface"></a>Interfaccia INapSystemHealthAgentBinding

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapSystemHealthAgentBinding** fornisce metodi che gli SHA usano per comunicare con NapAgent.

> [!Note]  
> [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) eredita tutti i metodi di questa interfaccia e deve essere usato.

 

## <a name="members"></a>Membri

**L'interfaccia INapSystemHealthAgentBinding** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthAgentBinding** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapSystemHealthAgentBinding** include questi metodi.



| Metodo                                                                                                                     | Descrizione                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding::FlushCache**](inapsystemhealthagentbinding-flushcache-method.md)                         | Chiamato da un sha per scaricare la cache SoH.<br/>                                                |
| [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | Chiamato dagli sha per determinare lo stato di isolamento del sistema.<br/>                                 |
| [**INapSystemHealthAgentBinding::Initialize**](inapsystemhealthagentbinding-initialize-method.md)                         | Inizializza l'sha e lo associa al servizio NapAgent. <br/>                         |
| [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md)               | Chiamato dagli sha quando il relativo soH cambia.<br/>                                                  |
| [**INapSystemHealthAgentBinding::Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md)                     | Chiamato da SHAs per fare in modo che NapAgent rilasci tutti i relativi riferimenti ai puntatori SHA COM.<br/> |



 

## <a name="remarks"></a>Commenti

Tutte le API in questa interfaccia restituiranno **RPC \_ E \_ DISCONNECTED** se NapAgent viene arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, dopo il riavvio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

