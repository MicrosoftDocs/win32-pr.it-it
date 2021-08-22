---
description: Stabilire una relazione tra un'istanza della classe Msvm \_ EmulatedEthernetPortSettingData o Msvm SyntheticEthernetPortSettingData con un'istanza della \_ classe Msvm \_ GuestNetworkAdapterConfiguration.
ms.assetid: 82262e67-1e72-4bad-974e-f18d00a94c3d
title: Msvm_SettingDataComponent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingDataComponent
- Msvm_SettingDataComponent.GroupComponent
- Msvm_SettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c96ad2d24291226934e50b338f2a0a4d77e9d966d2a821b73ad38d671b50fa04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950480"
---
# <a name="msvm_settingdatacomponent-class"></a>Classe Msvm \_ SettingDataComponent

Stabilire una relazione tra un'istanza della classe [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) o [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) con un'istanza della [**classe Msvm \_ GuestNetworkAdapterConfiguration.**](msvm-guestnetworkadapterconfiguration.md)

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData     REF GroupComponent;
  Msvm_GuestNetworkAdapterConfiguration REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SettingDataComponent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SettingDataComponent** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) o [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) che rappresenta una porta Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Chiave**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Riferimento a un'istanza della classe [**Msvm \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) che rappresenta la configurazione di una scheda di rete guest.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

