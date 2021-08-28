---
description: Questa associazione indica che una sottoclasse di un dispositivo logico , ad esempio un volume di archiviazione, è connessa tramite un controller di protocollo specifico.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Msvm_ProtocolControllerForUnit classe
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
ms.openlocfilehash: 73b8478e561d53212e0439219622595751ad954e13d0d086fabdbf57a483039d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086631"
---
# <a name="msvm_protocolcontrollerforunit-class"></a>Classe Msvm \_ ProtocolControllerForUnit

Questa associazione indica che una sottoclasse di un dispositivo logico , ad esempio un volume di archiviazione, è connessa tramite un controller di protocollo specifico. In molte situazioni (ad esempio la maschera lun di archiviazione), molte di queste associazioni possono essere usate per correlarsi a oggetti diversi. Di conseguenza, sono state definite sottoclassi per ottimizzare l'enumerazione delle associazioni.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe Msvm \_ ProtocolControllerForUnit** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ProtocolControllerForUnit** ha queste proprietà.

<dl> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Priorità data agli accessi del dispositivo tramite questo controller. Il percorso con priorità più alta avrà il valore più basso per questo parametro. Questa classe viene ereditata da **CIM \_ ProtocolControllerForDevice.**

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il controller sta attivando o accedendo al dispositivo (2) o meno (3). È anche possibile definire il valore 0 (Sconosciuto). Queste informazioni sono necessarie quando un dispositivo logico può essere eseguito o accessibile tramite più controller di protocollo. Questa classe viene ereditata da **CIM \_ ProtocolControllerForDevice.**

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Attivo** (2)
</dt> <dt>

<span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inattivo** (3 )
</dt> </dl>

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Controller del protocollo. Questa classe viene ereditata dalla [**dipendenza CIM. \_**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dispositivo controllato. Questa classe viene ereditata dalla [**dipendenza CIM. \_**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> <dt>

**DeviceAccess**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Diritti di accesso concessi al dispositivo tramite questo controller. Questa classe viene ereditata da **CIM \_ ProtocolControllerForUnit.**



| Valore                                                                               | Significato                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>        | Sconosciuto<br/>         |
| <dl> <dt>2</dt> </dl>        | Lettura/Scrittura<br/>      |
| <dl> <dt>3</dt> </dl>        | Sola lettura<br/>       |
| <dl> <dt>4</dt> </dl>        | Nessun accesso.<br/>      |
| <dl> <dt>5..15999</dt> </dl> | DmTF riservato<br/>   |
| <dl> <dt>16000..</dt> </dl>  | Fornitore riservato<br/> |



 

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo del dispositivo associato nel contesto del controller precedente. Questa classe viene ereditata da **CIM \_ ProtocolControllerForDevice.**

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ ProtocolControllerForUnit** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ ProtocolControllerForUnit**](cim-protocolcontrollerforunit.md)
</dt> <dt>

[**CIM \_ ProtocolControllerForUnit**](/previous-versions//cc150672(v=vs.85))
</dt> <dt>

[Archiviazione Classi](storage-classes.md)
</dt> </dl>

 

