---
title: Interfaccia INapClientManagement (NapManagement.h)
description: Fornisce metodi per la gestione client di Protezione accesso alla rete. | Interfaccia INapClientManagement (NapManagement.h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- Interfaccia INapClientManagement nap
- Interfaccia INapClientManagement NAP , descritta
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a9d338cdaad8ed46fd3c3c730ca3ae4c2065cda9803c283ae262addd939713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622117"
---
# <a name="inapclientmanagement-interface"></a>Interfaccia INapClientManagement

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**L'interfaccia INapClientManagement** fornisce metodi per la gestione client di Protezione accesso alla rete.

> [!Note]  
> [**INapClientManagement2**](inapclientmanagement2.md) eredita tutti i metodi di questa interfaccia e deve essere usato.

 

## <a name="members"></a>Membri

**L'interfaccia INapClientManagement** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapClientManagement** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapClientManagement** include questi metodi.



| Metodo                                                                                                                | Descrizione                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**INapClientManagement::GetNapClientInfo**](inapclientmanagement-getnapclientinfo.md)                               | Recupera informazioni su un client di Protezione accesso alla rete.<br/>                          |
| [**INapClientManagement::GetRegisteredEnforcementClients**](inapclientmanagement-getregisteredenforcementclients.md) | Recupera informazioni sui client di imposizione registrati.<br/>    |
| [**INapClientManagement::GetRegisteredSystemHealthAgents**](inapclientmanagement-getregisteredsystemhealthagents.md) | Recuperare informazioni su un'applicazione SHA registrata.<br/>                       |
| [**INapClientManagement::GetSystemIsolationInfo**](inapclientmanagement-getsystemisolationinfo.md)                   | Recupera informazioni sullo stato di isolamento del client Nap.<br/> |
| [**INapClientManagement::RegisterEnforcementClient**](inapclientmanagement-registerenforcementclient.md)             | Registra un client di imposizione con il sistema di Protezione accesso alla rete.<br/>               |
| [**INapClientManagement::RegisterSystemHealthAgent**](inapclientmanagement-registersystemhealthagent.md)             | Registra un'sha con il sistema di Protezione accesso alla rete.<br/>                              |
| [**INapClientManagement::UnregisterEnforcementClient**](inapclientmanagement-unregisterenforcementclient.md)         | Annulla la registrazione di un client di imposizione con il sistema di Protezione accesso alla rete.<br/>             |
| [**INapClientManagement::UnregisterSystemHealthAgent**](inapclientmanagement-unregistersystemhealthagent.md)         | Annulla la registrazione di un'sha con il sistema di Protezione accesso alla rete.<br/>                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

