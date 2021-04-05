---
description: Rappresenta un servizio che controlla la migrazione di sistemi virtuali tra sistemi host. Questa classe verifica anche se è probabile che una migrazione in sospeso abbia esito positivo.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: Classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6343cec0573a97656368d66426ec9b46c7255e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881217"
---
# <a name="cim_virtualsystemmigrationservice-class"></a>CIM \_ VirtualSystemMigrationService (classe)

Rappresenta un servizio che controlla la migrazione di sistemi virtuali tra sistemi host. Questa classe verifica anche se è probabile che una migrazione in sospeso abbia esito positivo.

## <a name="syntax"></a>Sintassi

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a>Members

La classe **CIM \_ VirtualSystemMigrationService** presenta questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La classe **CIM \_ VirtualSystemMigrationService** presenta questi metodi.



| Metodo                                                                                                                     | Descrizione                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | Verifica se è probabile che la migrazione di un sistema virtuale in sospeso a un host abbia esito positivo.<br/>   |
| [**CheckVirtualSystemIsMigratableToSystem**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | Verifica se una migrazione del sistema virtuale in sospeso a un sistema ha probabilmente esito positivo.<br/> |
| [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | Esegue la migrazione di un sistema virtuale a un host di destinazione.<br/>                                           |
| [**MigrateVirtualSystemToSystem**](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | Esegue la migrazione di un sistema virtuale al sistema di destinazione.<br/>                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Servizio CIM**](cim-service.md)
</dt> </dl>

 

 




