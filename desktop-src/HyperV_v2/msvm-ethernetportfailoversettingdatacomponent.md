---
description: Associazione utilizzata per stabilire relazioni tra un'istanza di Msvm EmulatedEthernetPortSettingData e una o più istanze di \_ msvm \_ EthernetSwitchFeatureSettingData.
ms.assetid: A2929D81-ED86-4C5A-9280-276204EDE89B
title: Msvm_EthernetPortFailoverSettingDataComponent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortFailoverSettingDataComponent
- Msvm_EthernetPortFailoverSettingDataComponent.GroupComponent
- Msvm_EthernetPortFailoverSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00653b19cffabeb658e7727332b7e6fe1b2e23be7ff0c4eba298ef198404234c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531521"
---
# <a name="msvm_ethernetportfailoversettingdatacomponent-class"></a>Classe Msvm \_ EthernetPortFailoverSettingDataComponent

Associazione utilizzata per stabilire relazioni tra un'istanza di [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) e una o più istanze di [**msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortFailoverSettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData      REF GroupComponent;
  Msvm_FailoverNetworkAdapterSettingData REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ EthernetPortFailoverSettingDataComponent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ EthernetPortFailoverSettingDataComponent** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) o [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) che rappresenta la porta Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) che rappresenta la configurazione della scheda di rete guest.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

