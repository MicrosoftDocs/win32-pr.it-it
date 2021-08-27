---
description: Rappresenta un'associazione tra un'istanza della classe CIM ComputerSystem che rappresenta la replica della macchina virtuale e un'istanza della classe CIM ComputerSystem che rappresenta la \_ replica della macchina virtuale di \_ test.
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Msvm_ReplicaSystemDependency classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f6bb3f4879ee0e1c7babaf8f85b8455716ee1b2e61db4e0764d6b28583efefd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130431"
---
# <a name="msvm_replicasystemdependency-class"></a>Classe Msvm \_ ReplicaSystemDependency

Rappresenta un'associazione tra un'istanza della [**classe \_ CIM ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la replica della macchina virtuale e un'istanza della **classe CIM \_ ComputerSystem** che rappresenta la replica di macchina virtuale di test.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ ReplicaSystemDependency** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ReplicaSystemDependency** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Antecedent")
</dt> </dl>

Riferimento a un'istanza della [**classe \_ CIM ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la replica della macchina virtuale. Questa proprietà viene ereditata dalla [**dipendenza CIM. \_**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Dependent")
</dt> </dl>

Riferimento a un'istanza della [**classe \_ CIM ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la replica di macchina virtuale di test creata dal [**metodo Msvm \_ ReplicationService.TestReplicaSystem.**](testreplicasystem-msvm-replicationservice.md) Questa proprietà viene ereditata dalla [**dipendenza CIM. \_**](/windows/desktop/CIMWin32Prov/cim-dependency)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

