---
description: Associa una porta seriale a un controller seriale.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Classe Msvm_SerialPortOnSerialController
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
ms.openlocfilehash: 357192bfb3dc4e901dd40a0cb6d7884152c3afc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879694"
---
# <a name="msvm_serialportonserialcontroller-class"></a>\_Classe MSVM SerialPortOnSerialController

Associa una porta seriale a un controller seriale.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

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

La **classe \_ SerialPortOnSerialController di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SerialPortOnSerialController di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Controller seriale a cui è connessa la porta. Questa proprietà viene ereditata da [**CIM \_ PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Porta del controller seriale. Questa proprietà viene ereditata da [**CIM \_ PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ SerialPortOnSerialController di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_PORTONDEVICE CIM**](cim-portondevice.md)
</dt> <dt>

[**\_PORTONDEVICE CIM**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[Classi di dispositivi seriali](serial-devices-classes.md)
</dt> </dl>

 

