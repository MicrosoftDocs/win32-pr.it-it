---
description: Rappresenta una parte di una relazione tra un' \_ istanza CIM VirtualSystemSettingData e un set di \_ istanze ResourceAllocationSettingData CIM.
ms.assetid: 4f167517-079e-4b5f-885a-741ac1d1dc71
title: Classe CIM_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingDataComponent
- CIM_VirtualSystemSettingDataComponent.GroupComponent
- CIM_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afbd7ab192c65e99f4479e5380e57dc78c8a0a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131999"
---
# <a name="cim_virtualsystemsettingdatacomponent-class"></a>CIM \_ VirtualSystemSettingDataComponent (classe)

Rappresenta una parte di una relazione tra un'istanza [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) e un set di [**istanze \_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) .

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingDataComponent : CIM_Component
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ VirtualSystemSettingDataComponent** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ VirtualSystemSettingDataComponent** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Riferimento all'oggetto [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) di primo livello della configurazione del sistema virtuale.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ResourceAllocationSettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Un riferimento all' [**oggetto \_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) che rappresenta una parte della configurazione del sistema virtuale.

</dd> </dl>

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

[**\_Componente CIM**](cim-component.md)
</dt> </dl>

 

