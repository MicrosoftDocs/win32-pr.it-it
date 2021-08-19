---
description: Associa un dispositivo di archiviazione al controller di archiviazione proprietario del dispositivo.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Msvm_ControlledBy classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b08cf97c54363009e839ea78fe139c6c8a1bdd81cac07182d019d3d00857dee4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130601"
---
# <a name="msvm_controlledby-class"></a>Classe Msvm \_ ControlledBy

Associa un dispositivo di archiviazione al controller di archiviazione proprietario del dispositivo. Questa associazione viene usata con i controller IDE e floppy.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ ControlledBy** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ControlledBy** ha queste proprietà.

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Accessibilità del dispositivo tramite il controller precedente. Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)e viene sempre impostata su 2 (lettura/scrittura).

</dd> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Priorità data agli accessi del dispositivo tramite questo controller. Il percorso con priorità più alta avrà il valore più basso. Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)e viene sempre impostata su 0.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il controller sta attivando o accedendo al dispositivo. Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)e viene sempre impostata su 1 (attiva).

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Controller CIM \_**](/windows/desktop/CIMWin32Prov/cim-controller)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al controller. Questa proprietà viene ereditata da [**CIM \_ ControlledBy.**](/windows/desktop/CIMWin32Prov/cim-controlledby)

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al dispositivo controllato. Questa proprietà viene ereditata da [**CIM \_ ControlledBy.**](/windows/desktop/CIMWin32Prov/cim-controlledby)

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo del dispositivo associato nel contesto del controller precedente. Questa proprietà viene ereditata da [**CIM \_ ControlledBy.**](/windows/desktop/CIMWin32Prov/cim-controlledby)

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)e viene sempre impostata su 0.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)e viene sempre impostata su 0.

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ControlledBy,**](/windows/desktop/CIMWin32Prov/cim-controlledby)ma non viene usata.

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ControlledBy,**](/windows/desktop/CIMWin32Prov/cim-controlledby)ma non viene usata.

</dd> <dt>

**TimeOfDeviceReset**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ControlledBy,**](/windows/desktop/CIMWin32Prov/cim-controlledby)ma non viene usata.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ ControlledBy** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[Archiviazione Classi](storage-classes.md)
</dt> </dl>

 

