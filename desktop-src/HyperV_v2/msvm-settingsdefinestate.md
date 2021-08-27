---
description: Associa una macchina virtuale e i relativi dispositivi alle istanze di \_ CiM SettingData che rappresentano le impostazioni correnti che si applicano a questi oggetti.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Msvm_SettingsDefineState classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eea8a6cce263ddb3ad00ecd6951c1d5b47c6d98d58e99763b3f28780cb3438b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950466"
---
# <a name="msvm_settingsdefinestate-class"></a>Classe Msvm \_ SettingsDefineState

Associa una macchina virtuale e i relativi dispositivi alle istanze di [**\_ CiM SettingData**](/previous-versions//cc136911(v=vs.85)) che rappresentano le impostazioni correnti che si applicano a questi oggetti. In particolare, associa [**Msvm \_ ComputerSystem**](msvm-computersystem.md) alle istanze di [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)e associa **\_ \* Msvm* _ derivati di [_ *CIM \_ LogicalDevice* *](/windows/desktop/CIMWin32Prov/cim-logicaldevice) a **Msvm \_ \** _ derivati di _ [*CIM \_ ResourceAllocationSettingData* *](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SettingsDefineState** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SettingsDefineState** ha queste proprietà.

<dl> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento alla macchina virtuale.

</dd> <dt>

**Impostazione dei dati**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento alle impostazioni attualmente attive per la macchina virtuale.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ SettingsDefineState** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                 |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni \_ CIMDefineState**](cim-settingsdefinestate.md)
</dt> <dt>

[**Impostazioni \_ CIMDefineState**](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[Classi di gestione del sistema virtuale](virtual-system-management-classes.md)
</dt> </dl>

 

