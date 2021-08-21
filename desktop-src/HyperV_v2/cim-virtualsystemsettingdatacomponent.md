---
description: Rappresenta una parte di una relazione tra un'istanza CIM VirtualSystemSettingData e un set di \_ istanze di CIM \_ ResourceAllocationSettingData.
ms.assetid: 4f167517-079e-4b5f-885a-741ac1d1dc71
title: CIM_VirtualSystemSettingDataComponent classe
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
ms.openlocfilehash: 54ceb24806b21a06a9a0e8e82cf5fbb6ca96776d645b45679edb3adfcbd46c3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150287"
---
# <a name="cim_virtualsystemsettingdatacomponent-class"></a>Classe CIM \_ VirtualSystemSettingDataComponent

Rappresenta una parte di una relazione tra [**un'istanza CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) e un set di [**istanze di CIM \_ ResourceAllocationSettingData.**](cim-resourceallocationsettingdata.md)

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

La **classe CIM \_ VirtualSystemSettingDataComponent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ VirtualSystemSettingDataComponent** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Riferimento all'oggetto [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) di primo livello della configurazione del sistema virtuale.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ResourceAllocationSettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Riferimento [**all'oggetto CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresenta una parte della configurazione del sistema virtuale.

</dd> </dl>

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

[**Componente \_ CIM**](cim-component.md)
</dt> </dl>

 

