---
description: Associa un dispositivo di archiviazione al controller di archiviazione proprietario del dispositivo.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Classe Msvm_ControlledBy
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
ms.openlocfilehash: 7986ffb842f7a1a104a0a8d846c1b6ee47a21523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317194"
---
# <a name="msvm_controlledby-class"></a>\_Classe MSVM ControlledBy

Associa un dispositivo di archiviazione al controller di archiviazione proprietario del dispositivo. Questa associazione viene utilizzata con i controller IDE e floppy.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

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

La **classe \_ ControlledBy di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ControlledBy di MSVM** dispone di queste proprietà.

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Accessibilità del dispositivo tramite il controller precedente. Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)ed è sempre impostata su 2 (lettura/scrittura).

</dd> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Priorità assegnata ad accessi del dispositivo tramite questo controller. Il percorso con la priorità più alta avrà il valore più basso. Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)ed è sempre impostata su 0.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il controller sta attivando o accedendo attivamente al dispositivo. Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)ed è sempre impostata su 1 (attivo).

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al controller. Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al dispositivo controllato. Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo del dispositivo associato nel contesto del controller precedente. Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)ed è sempre impostata su 0.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)ed è sempre impostata su 0.

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), ma non viene utilizzata.

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), ma non viene utilizzata.

</dd> <dt>

**TimeOfDeviceReset (ora**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), ma non viene utilizzata.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ ControlledBy di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dt>

[**\_CONTROLLEDBY CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[Classi di archiviazione](storage-classes.md)
</dt> </dl>

 

