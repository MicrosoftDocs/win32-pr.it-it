---
description: Associa una porta seriale a un controller seriale.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Msvm_SerialPortOnSerialController classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ddc5a5c006b92945178f89cf5f4df585f96ed3eaef692b04326878cb0d16520
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107441"
---
# <a name="msvm_serialportonserialcontroller-class"></a>Classe Msvm \_ SerialPortOnSerialController

Associa una porta seriale a un controller seriale.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SerialPortOnSerialController** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SerialPortOnSerialController** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Controller seriale a cui è connessa la porta. Questa proprietà viene ereditata da [**CIM \_ PortOnDevice.**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Porta del controller seriale. Questa proprietà viene ereditata da [**CIM \_ PortOnDevice.**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ SerialPortOnSerialController** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Porta \_ CIMDisposizionale**](cim-portondevice.md)
</dt> <dt>

[**Porta \_ CIMDisposizionale**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[Classi di dispositivi seriali](serial-devices-classes.md)
</dt> </dl>

 

