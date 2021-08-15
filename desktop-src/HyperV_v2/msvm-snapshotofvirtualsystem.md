---
description: Associa un sistema virtuale a uno snapshot acquisito dal sistema virtuale.
ms.assetid: CF1C1C04-02BC-4AC3-8327-FEE54ECE8541
title: Msvm_SnapshotOfVirtualSystem classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystem
- Msvm_SnapshotOfVirtualSystem.Antecedent
- Msvm_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc1971c1123ab30fb88da9278b1d4f142e35785a393a75e1bf8a3ec69771f98a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950300"
---
# <a name="msvm_snapshotofvirtualsystem-class"></a>Classe Msvm \_ SnapshotOfVirtualSystem

Associa un sistema virtuale a uno snapshot acquisito dal sistema virtuale.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystem : CIM_SnapshotOfVirtualSystem
{
  Msvm_ComputerSystem           REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SnapshotOfVirtualSystem** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SnapshotOfVirtualSystem** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) che rappresenta il sistema virtuale. Questa proprietà è derivata dalla [**dipendenza CIM \_**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta lo snapshot. Questa proprietà è derivata dalla [**dipendenza CIM \_**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> </dl>

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

[**CIM \_ SnapshotOfVirtualSystem**](cim-snapshotofvirtualsystem.md)
</dt> <dt>

[**CreateSnapshot**](createsnapshot-msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

