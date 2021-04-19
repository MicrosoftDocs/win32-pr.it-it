---
description: Associazione utilizzata per rappresentare le impostazioni della rete di migrazione del sistema virtuale del servizio di migrazione del sistema virtuale.
ms.assetid: 5704dce7-1db3-4049-8c61-58bfa9596766
title: Classe Msvm_VirtualSystemMigrationServiceSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingDataComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.GroupComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ba69ebd6cfd50b30923db2ecc87e7e5aeebcaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305987"
---
# <a name="msvm_virtualsystemmigrationservicesettingdatacomponent-class"></a>\_Classe MSVM VirtualSystemMigrationServiceSettingDataComponent

Associazione utilizzata per rappresentare le impostazioni della rete di migrazione del sistema virtuale del servizio di migrazione del sistema virtuale.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingDataComponent : CIM_Component
{
  Msvm_VirtualSystemMigrationServiceSettingData REF GroupComponent;
  Msvm_VirtualSystemMigrationNetworkSettingData REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe \_ VirtualSystemMigrationServiceSettingDataComponent di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualSystemMigrationServiceSettingDataComponent di MSVM** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ VirtualSystemMigrationServiceSettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**aggregazione**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) che rappresenta le impostazioni del servizio di migrazione.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ VirtualSystemMigrationNetworkSettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) che rappresenta le impostazioni della rete di migrazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

