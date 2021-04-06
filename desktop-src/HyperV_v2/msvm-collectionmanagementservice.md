---
description: Gestisce le raccolte nell'host Hyper-V.
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760496"
---
# <a name="msvm_collectionmanagementservice-class"></a>\_Classe MSVM CollectionManagementService

Gestisce le raccolte nell'host Hyper-V.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a>Members

La **classe \_ CollectionManagementService di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe \_ CollectionManagementService di MSVM** dispone di questi metodi.



| Metodo                                                                          | Descrizione                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddMember**](msvm-collectionmanagementservice-addmember.md)                 | Aggiunge il Managementelement specificato come membro dell'oggetto [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) specificato.<br/>                                                                                           |
| [**Definecollection**](msvm-collectionmanagementservice-definecollection.md)   | Crea un nuovo [**oggetto \_ CollectionOfMSEs CIM**](cim-collectionofmses.md) .<br/>                                                                                                                                        |
| [**Distruttore**](msvm-collectionmanagementservice-destroycollection.md) | Elimina l'oggetto [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) specificato.<br/>                                                                                                                                    |
| [**RemoveMember**](msvm-collectionmanagementservice-removemember.md)           | Rimuove il Managementelement specificato come membro dell'oggetto [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) specificato.<br/>                                                                                        |
| [**RemoveMemberById**](msvm-collectionmanagementservice-removememberbyid.md)   | Rimuove l'oggetto gestito specificato come membro del [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) con l'identificatore specificato. Questa operazione avrà esito positivo anche se l'oggetto con tale identificatore non è presente.<br/> |
| [**Rinominacollection**](msvm-collectionmanagementservice-renamecollection.md)   | Aggiorna l'elemento ElementName dell' [**oggetto \_ CollectionOfMSEs CIM**](cim-collectionofmses.md) specificato.<br/>                                                                                                                    |
| [**StartService**](msvm-collectionmanagementservice-startservice.md)           | avvia il servizio.<br/>                                                                                                                                                                                                |
| [**StopService**](msvm-collectionmanagementservice-stopservice.md)             | arresta il servizio.<br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Servizio CIM**](cim-service.md)
</dt> </dl>

 

 




