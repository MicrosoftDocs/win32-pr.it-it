---
title: Interfaccia INapClientManagement (NapManagement. h)
description: Fornisce metodi per la gestione client di protezione accesso alla rete. | Interfaccia INapClientManagement (NapManagement. h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- NAP interfaccia INapClientManagement
- Interfaccia NAP di INapClientManagement, descrizione
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
ms.openlocfilehash: fe90158d6f1e9a864f7d19448a412d70890133d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969198"
---
# <a name="inapclientmanagement-interface"></a>Interfaccia INapClientManagement

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'interfaccia **INapClientManagement** fornisce metodi per la gestione client di protezione accesso alla rete.

> [!Note]  
> [**INapClientManagement2**](inapclientmanagement2.md) eredita tutti i metodi di questa interfaccia e deve essere usato in alternativa.

 

## <a name="members"></a>Membri

L'interfaccia **INapClientManagement** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapClientManagement** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapClientManagement** dispone di questi metodi.



| Metodo                                                                                                                | Descrizione                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**INapClientManagement::GetNapClientInfo**](inapclientmanagement-getnapclientinfo.md)                               | Recupera le informazioni su un client di protezione accesso alla rete.<br/>                          |
| [**INapClientManagement::GetRegisteredEnforcementClients**](inapclientmanagement-getregisteredenforcementclients.md) | Recupera le informazioni sui client di imposizione registrati.<br/>    |
| [**INapClientManagement::GetRegisteredSystemHealthAgents**](inapclientmanagement-getregisteredsystemhealthagents.md) | Recuperare informazioni su un SHA registrato.<br/>                       |
| [**INapClientManagement::GetSystemIsolationInfo**](inapclientmanagement-getsystemisolationinfo.md)                   | Recupera le informazioni sullo stato di isolamento del client di protezione accesso alla rete.<br/> |
| [**INapClientManagement::RegisterEnforcementClient**](inapclientmanagement-registerenforcementclient.md)             | Registra un client di imposizione con il sistema NAP.<br/>               |
| [**INapClientManagement::RegisterSystemHealthAgent**](inapclientmanagement-registersystemhealthagent.md)             | Registra un SHA con il sistema NAP.<br/>                              |
| [**INapClientManagement::UnregisterEnforcementClient**](inapclientmanagement-unregisterenforcementclient.md)         | Annulla la registrazione di un client di imposizione con il sistema NAP.<br/>             |
| [**INapClientManagement::UnregisterSystemHealthAgent**](inapclientmanagement-unregistersystemhealthagent.md)         | Annulla la registrazione di un SHA con il sistema NAP.<br/>                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

