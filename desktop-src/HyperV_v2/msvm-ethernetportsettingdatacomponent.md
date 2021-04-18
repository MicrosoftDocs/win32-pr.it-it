---
description: Associazione utilizzata per stabilire &\# 0034; parte di&\# 0034; relazioni tra un'istanza di un EthernetPortAllocationSettingData MSVM \_ e una o più istanze di un EthernetSwitchFeatureSettingData MSVM \_ .
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Classe Msvm_EthernetPortSettingDataComponent
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
ms.openlocfilehash: 1c00c056bd5095d945af12fde3556d92b9a2d7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312912"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a>\_Classe MSVM EthernetPortSettingDataComponent

Associazione utilizzata per stabilire relazioni "parte di" tra un'istanza di un [**\_ EthernetPortAllocationSettingData MSVM**](msvm-ethernetportallocationsettingdata.md) e una o più istanze di un [**\_ EthernetSwitchFeatureSettingData MSVM**](msvm-ethernetswitchfeaturesettingdata.md).

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

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

La **classe \_ EthernetPortSettingDataComponent di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ EthernetPortSettingDataComponent di MSVM** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**aggregazione**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) che rappresenta la porta Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) che rappresenta le impostazioni della funzionalità applicate alla porta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

