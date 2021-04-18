---
title: Interfaccia INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: SHAs usare per comunicare con NapAgent. | Interfaccia INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- NAP interfaccia INapSystemHealthAgentBinding
- Interfaccia NAP di INapSystemHealthAgentBinding, descrizione
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
ms.openlocfilehash: d38d1331996e34c6879fc2e98ce566ce6802527a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321961"
---
# <a name="inapsystemhealthagentbinding-interface"></a>Interfaccia INapSystemHealthAgentBinding

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapSystemHealthAgentBinding** fornisce i metodi usati da Shas per comunicare con napagent.

> [!Note]  
> [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) eredita tutti i metodi di questa interfaccia e deve essere usato in alternativa.

 

## <a name="members"></a>Membri

L'interfaccia **INapSystemHealthAgentBinding** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthAgentBinding** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapSystemHealthAgentBinding** dispone di questi metodi.



| Metodo                                                                                                                     | Descrizione                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding:: FlushCache**](inapsystemhealthagentbinding-flushcache-method.md)                         | Chiamato da un SHA per scaricare la cache del rapporto di integrità.<br/>                                                |
| [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | Chiamato da SHAs per determinare lo stato di isolamento del sistema.<br/>                                 |
| [**INapSystemHealthAgentBinding:: Initialize**](inapsystemhealthagentbinding-initialize-method.md)                         | Inizializza l'SHA e associa l'SHA al servizio NapAgent. <br/>                         |
| [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md)               | Chiamato da SHAs quando cambia il rapporto di integrità.<br/>                                                  |
| [**INapSystemHealthAgentBinding:: Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md)                     | Chiamato da SHAs per fare in modo che NapAgent rilasci tutti i relativi riferimenti ai puntatori SHA COM.<br/> |



 

## <a name="remarks"></a>Commenti

Tutte le API in questa interfaccia restituiranno **RPC \_ E \_ disconnesse** se il NapAgent è stato arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

