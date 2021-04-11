---
description: Associa una macchina virtuale e i relativi dispositivi a istanze di CIM \_ SettingData che rappresentano le impostazioni correnti che si applicano a tali oggetti.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Classe Msvm_SettingsDefineState
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
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232268"
---
# <a name="msvm_settingsdefinestate-class"></a>\_Classe MSVM SettingsDefineState

Associa una macchina virtuale e i relativi dispositivi a istanze di [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) che rappresentano le impostazioni correnti che si applicano a tali oggetti. In particolare, associa [**MSVM \_ ComputerSystem**](msvm-computersystem.md) alle istanze di [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)e associa **MSVM \_ \** _ derivati di [_ *CIM \_ LogicalDevice* *](/windows/desktop/CIMWin32Prov/cim-logicaldevice) con **\_ \* MSVM* _ derivati di [_ *CIM \_ ResourceAllocationSettingData*. *](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

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

La **classe \_ SettingsDefineState di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SettingsDefineState di MSVM** dispone di queste proprietà.

<dl> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento alla macchina virtuale.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Un riferimento alle impostazioni attualmente attive per la macchina virtuale.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ SettingsDefineState di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTINGSDEFINESTATE CIM**](cim-settingsdefinestate.md)
</dt> <dt>

[**\_SETTINGSDEFINESTATE CIM**](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[Classi di gestione del sistema virtuale](virtual-system-management-classes.md)
</dt> </dl>

 

