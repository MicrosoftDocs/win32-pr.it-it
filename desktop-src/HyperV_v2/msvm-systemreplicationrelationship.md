---
description: Rappresenta un'associazione tra un'istanza di Msvm ComputerSystem che rappresenta la macchina virtuale e un'istanza di \_ Msvm ReplicationRelationship che rappresenta una relazione di replica \_ della macchina virtuale.
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Msvm_SystemReplicationRelationship classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86040e6dc5676f6cd40b223f0a3cbd31864965722de957fda6ff1d140ad94b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810609"
---
# <a name="msvm_systemreplicationrelationship-class"></a>Classe \_ Msvm SystemReplicationRelationship

Rappresenta un'associazione tra un'istanza di [**Msvm \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale e un'istanza di [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) che rappresenta una relazione di replica della macchina virtuale. Questa classe deriva dalla [**classe \_ Dependency CIM.**](/windows/desktop/CIMWin32Prov/cim-dependency)

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SystemReplicationRelationship** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SystemReplicationRelationship** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Msvm \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Antecedent")
</dt> </dl>

Riferimento all'istanza della [**classe \_ ComputerSystem Msvm**](msvm-computersystem.md) che rappresenta la macchina virtuale.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Msvm \_ ReplicationRelationship**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Dependent")
</dt> </dl>

Riferimento all'istanza della [**classe Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) che rappresenta la relazione di replica di un sistema virtuale.

</dd> </dl>

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

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> <dt>

[**Dipendenza \_ CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

