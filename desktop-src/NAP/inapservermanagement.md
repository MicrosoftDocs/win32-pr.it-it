---
title: Interfaccia INapServerManagement (NapServerManagement. h)
description: Consentono di gestire il server di protezione accesso alla rete.
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- NAP interfaccia INapServerManagement
- Interfaccia NAP di INapServerManagement, descrizione
topic_type:
- apiref
api_name:
- INapServerManagement
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5eed03f535653a3b9244ff1aa74fe499c1bf2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120082"
---
# <a name="inapservermanagement-interface"></a>Interfaccia INapServerManagement

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapServerManagement** fornisce i metodi utilizzati per gestire il server di protezione accesso alla rete.

## <a name="members"></a>Membri

L'interfaccia **INapServerManagement** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapServerManagement** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapServerManagement** dispone di questi metodi.



| Metodo                                                                                                                       | Descrizione                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**INapServerManagement::RegisterSystemHealthValidator**](inapservermanagement-registersystemhealthvalidator-method.md)     | Registra un servizio di convalida dell'integrità.<br/>                         |
| [**INapServerManagement::SetFailureCategoryMappings**](inapservermanagement-setfailurecategorymappings-method.md)           | Imposta i mapping delle categorie di errori di convalida.<br/> |
| [**INapServerManagement::UnregisterSystemHealthValidator**](inapservermanagement-unregistersystemhealthvalidator-method.md) | Annulla la registrazione di un servizio di convalida integrità dal server protezione accesso alla rete.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

