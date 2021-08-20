---
title: Interfaccia INapEnforcementClientCallback (NapEnforcementClient.h)
description: I client di imposizione devono implementare per consentire a NapAgent di comunicare con essi.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- Interfaccia INapEnforcementClientCallback nap
- Interfaccia INapEnforcementClientCallback nap , descritta
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48c595918d28d912725353eb856de8f0af4541a68dabcb6f5a7cb0bb944496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134040"
---
# <a name="inapenforcementclientcallback-interface"></a>Interfaccia INapEnforcementClientCallback

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**L'interfaccia INapEnforcementClientCallback** fornisce metodi di callback che i client di imposizione devono implementare per consentire a NapAgent di comunicare con essi.

## <a name="members"></a>Membri

**L'interfaccia INapEnforcementClientCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapEnforcementClientCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **INapEnforcementClientCallback.**



| Metodo                                                                                                         | Descrizione                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientCallback::GetConnections**](inapenforcementclientcallback-getconnections-method.md)   | Usato da NapAgent per recuperare le connessioni.<br/>                         |
| [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) | Usato da NapAgent per informare il client di imposizione delle modifiche SoH.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



 

