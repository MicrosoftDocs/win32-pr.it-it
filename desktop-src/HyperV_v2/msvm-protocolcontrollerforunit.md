---
description: Questa associazione indica che una sottoclasse di un dispositivo logico, ad esempio un volume di archiviazione, è connessa tramite un controller di protocollo specifico.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Classe Msvm_ProtocolControllerForUnit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1470192fc4f10e60bdfef013146483b47cbfa7f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310010"
---
# <a name="msvm_protocolcontrollerforunit-class"></a>\_Classe MSVM ProtocolControllerForUnit

Questa associazione indica che una sottoclasse di un dispositivo logico, ad esempio un volume di archiviazione, è connessa tramite un controller di protocollo specifico. In molte situazioni, ad esempio mascheramento LUN di archiviazione, è possibile che molte di queste associazioni vengano usate per correlare oggetti diversi. Pertanto, le sottoclassi sono state definite per ottimizzare l'enumerazione delle associazioni.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a>Members

La **classe \_ ProtocolControllerForUnit di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ProtocolControllerForUnit di MSVM** dispone di queste proprietà.

<dl> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Priorità assegnata ad accessi del dispositivo tramite questo controller. Il percorso con la priorità più alta avrà il valore più basso per questo parametro. Questa classe è ereditata da **CIM \_ ProtocolControllerForDevice**.

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il controller sta attivamente eseguendo il comando o accede al dispositivo (2) o meno (3). È inoltre possibile definire il valore 0 (sconosciuto). Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller di protocollo. Questa classe è ereditata da **CIM \_ ProtocolControllerForDevice**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Attivo** (2)
</dt> <dt>

<span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inattivo** (3)
</dt> </dl>

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Controller del protocollo. Questa classe viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dispositivo controllato. Questa classe viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**DeviceAccess**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Diritti di accesso concessi al dispositivo tramite questo controller. Questa classe è ereditata da **CIM \_ ProtocolControllerForUnit**.



| Valore                                                                               | Significato                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>        | Sconosciuto<br/>         |
| <dl> <dt>2</dt> </dl>        | Lettura/Scrittura<br/>      |
| <dl> <dt>3</dt> </dl>        | Sola lettura<br/>       |
| <dl> <dt>4</dt> </dl>        | Nessun accesso.<br/>      |
| <dl> <dt>5.. 15999</dt> </dl> | DMTF riservato<br/>   |
| <dl> <dt>16000..</dt> </dl>  | Fornitore riservato<br/> |



 

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo del dispositivo associato nel contesto del controller precedente. Questa classe è ereditata da **CIM \_ ProtocolControllerForDevice**.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ ProtocolControllerForUnit di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_PROTOCOLCONTROLLERFORUNIT CIM**](cim-protocolcontrollerforunit.md)
</dt> <dt>

[**\_PROTOCOLCONTROLLERFORUNIT CIM**](/previous-versions//cc150672(v=vs.85))
</dt> <dt>

[Classi di archiviazione](storage-classes.md)
</dt> </dl>

 

