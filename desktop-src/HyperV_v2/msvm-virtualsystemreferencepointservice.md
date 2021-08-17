---
description: Descrive un servizio punto di riferimento del sistema virtuale.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Msvm_VirtualSystemReferencePointService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f33ac35e9848b913978ef6fab91f60823e5c40e9a2bb652236b2ab902e4ea435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340161"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a>Classe Msvm \_ VirtualSystemReferencePointService

Descrive un servizio punto di riferimento del sistema virtuale.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a>Members

La **classe Msvm \_ VirtualSystemReferencePointService** include questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe Msvm \_ VirtualSystemReferencePointService** include questi metodi.



| Metodo                                                                                                       | Descrizione                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | Crea un punto di riferimento di un sistema virtuale.<br/>            |
| [**DestroyReferencePoint**](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | Elimina il punto di riferimento specificato.<br/>                    |
| [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | Esporta il punto di riferimento del sistema virtuale.<br/>        |
| [**ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | Importa i metadati del punto di riferimento del sistema virtuale.<br/>   |
| [**RemoveAssociatedData**](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | Rimuove il log di dati associato al punto di riferimento.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Servizio \_ CIM**](cim-service.md)
</dt> </dl>

 

 




