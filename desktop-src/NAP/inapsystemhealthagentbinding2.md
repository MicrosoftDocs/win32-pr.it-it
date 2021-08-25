---
title: Interfaccia INapSystemHealthAgentBinding2 (NapSystemHealthAgent.h)
description: Gli SHA usano per comunicare con NapAgent. | Interfaccia INapSystemHealthAgentBinding2 (NapSystemHealthAgent.h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- Interfaccia INapSystemHealthAgentBinding2 nap
- Interfaccia INapSystemHealthAgentBinding2 nap , descritta
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c42db59c23826855ca6cda7529eb9dcbbadfb2a1ee2a5aa93d9bd45587c45a87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780931"
---
# <a name="inapsystemhealthagentbinding2-interface"></a>Interfaccia INapSystemHealthAgentBinding2

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapSystemHealthAgentBinding2** fornisce metodi che gli SHA usano per comunicare con NapAgent.

> [!Note]  
> Questa interfaccia eredita tutti i metodi di [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) e deve essere usata.

 

## <a name="members"></a>Membri

**L'interfaccia INapSystemHealthAgentBinding2** eredita da [**INapSystemHealthAgentBinding.**](inapsystemhealthagentbinding.md) **INapSystemHealthAgentBinding2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapSystemHealthAgentBinding2** include questi metodi.



| Metodo                                                                                                                    | Descrizione                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | Chiamato da SHAs per determinare lo stato di isolamento del sistema e lo stato di isolamento esteso.<br/> |



 

## <a name="remarks"></a>Commenti

Tutte le API in questa interfaccia restituiranno **RPC \_ E \_ DISCONNECTED** se NapAgent viene arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, dopo il riavvio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

 





