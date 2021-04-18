---
description: Associazione generica utilizzata per stabilire parte delle relazioni tra un'istanza di CIM \_ VirtualSystemSettingData e una o più istanze di CIM \_ ResourceAllocationSettingData.
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Classe Msvm_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfff3981d6fdb9fdb0368fa887c559026fc10af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305982"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a>\_Classe MSVM VirtualSystemSettingDataComponent

Associazione generica utilizzata per stabilire relazioni ' parte di ' tra un'istanza di [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) e una o più istanze di [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe \_ VirtualSystemSettingDataComponent di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualSystemSettingDataComponent di MSVM** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **override**, **min** (1), **Max** (1)
</dt> </dl>

Elemento padre nell'associazione. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento figlio nell'associazione. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ VirtualSystemSettingDataComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

[**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**](/previous-versions//cc150674(v=vs.85))
</dt> <dt>

[Classi di sistema virtuali](virtual-system-classes.md)
</dt> </dl>

 

