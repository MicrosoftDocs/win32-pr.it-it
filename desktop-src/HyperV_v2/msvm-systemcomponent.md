---
description: Stabilisce un &\# 0034; parte della&\# 0034; relazione tra un sistema e qualsiasi elemento di sistema gestito di cui è composto.
ms.assetid: 6BF72E36-9B6C-4853-A553-DDAF65991C86
title: Classe Msvm_SystemComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemComponent
- Msvm_SystemComponent.GroupComponent
- Msvm_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee150793143b549c90d280eef287ee6a5afb66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401612"
---
# <a name="msvm_systemcomponent-class"></a>\_Classe MSVM SystemComponent

Stabilisce una relazione "parte di" tra un sistema e qualsiasi elemento di sistema gestito di cui è composto.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), Association, Aggregation]
class Msvm_SystemComponent : CIM_SystemComponent
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe \_ SystemComponent di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SystemComponent di MSVM** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento padre nell'associazione. Questa proprietà viene ereditata da [**CIM \_ SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento figlio nell'associazione. Questa proprietà viene ereditata da [**CIM \_ SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

