---
title: Interfaccia INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
description: SHAs usare per comunicare con NapAgent. | Interfaccia INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- NAP interfaccia INapSystemHealthAgentBinding2
- Interfaccia NAP di INapSystemHealthAgentBinding2, descrizione
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
ms.openlocfilehash: f9a7491a2e78d66399f9ca246bcee9182e4f95d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352796"
---
# <a name="inapsystemhealthagentbinding2-interface"></a>Interfaccia INapSystemHealthAgentBinding2

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapSystemHealthAgentBinding2** fornisce i metodi usati da Shas per comunicare con napagent.

> [!Note]  
> Questa interfaccia eredita tutti i metodi di [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) e deve essere usata in alternativa.

 

## <a name="members"></a>Membri

L'interfaccia **INapSystemHealthAgentBinding2** eredita da [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md). **INapSystemHealthAgentBinding2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapSystemHealthAgentBinding2** dispone di questi metodi.



| Metodo                                                                                                                    | Descrizione                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | Chiamata eseguita da SHAs per determinare lo stato di isolamento del sistema e lo stato di isolamento esteso.<br/> |



 

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

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

 





