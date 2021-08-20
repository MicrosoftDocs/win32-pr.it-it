---
description: Rappresenta un servizio che controlla la migrazione di sistemi virtuali tra sistemi host. Questa classe verifica anche se è probabile che una migrazione in sospeso riesca.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: CIM_VirtualSystemMigrationService classe
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
ms.openlocfilehash: 44b034c5b91eb024bdbcde0b0d835ba12f0367bedc6dbd9c5c2d52dca1029f87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068541"
---
# <a name="cim_virtualsystemmigrationservice-class"></a>Classe CIM \_ VirtualSystemMigrationService

Rappresenta un servizio che controlla la migrazione di sistemi virtuali tra sistemi host. Questa classe verifica anche se è probabile che una migrazione in sospeso riesca.

## <a name="syntax"></a>Sintassi

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a>Members

La **classe CIM \_ VirtualSystemMigrationService** include questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe CIM \_ VirtualSystemMigrationService** include questi metodi.



| Metodo                                                                                                                     | Descrizione                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | Verifica se è probabile che una migrazione del sistema virtuale in sospeso a un host riesca.<br/>   |
| [**CheckVirtualSystemIsMigratableToSystem**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | Verifica se è probabile che una migrazione del sistema virtuale in sospeso a un sistema riesca.<br/> |
| [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | Esegue la migrazione di un sistema virtuale a un host di destinazione.<br/>                                           |
| [**MigrateVirtualSystemToSystem**](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | Esegue la migrazione di un sistema virtuale al sistema di destinazione.<br/>                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Servizio \_ CIM**](cim-service.md)
</dt> </dl>

 

 




