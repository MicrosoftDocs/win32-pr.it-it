---
description: Associazione usata per stabilire &0034;parte di&0034; relazioni tra un'istanza di Msvm EthernetPortAllocationSettingData e una o più istanze di \# \# \_ msvm \_ EthernetSwitchFeatureSettingData.
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Msvm_EthernetPortSettingDataComponent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 989d734d4c59d710c737c218b22591517347a8f5e434ff99e195887cbb4b6774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524841"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a>Classe Msvm \_ EthernetPortSettingDataComponent

Associazione usata per stabilire relazioni "parte di" tra un'istanza di [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) e una o più istanze di [**msvm \_ EthernetSwitchFeatureSettingData.**](msvm-ethernetswitchfeaturesettingdata.md)

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ EthernetPortSettingDataComponent** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ EthernetPortSettingDataComponent** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) che rappresenta la porta Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Chiave**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) che rappresenta le impostazioni delle funzionalità applicate alla porta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

