---
description: Un'associazione tra un'istanza di MSVM \_ VssComponent e un'istanza di MSVM \_ VssService che rappresenta un servizio per l'esecuzione di operazioni sul componente VSS.
ms.assetid: 19fdf2e3-48c4-452b-89d0-ec0b8681fca2
title: Classe Msvm_ServiceOfVssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceOfVssComponent
- Msvm_ServiceOfVssComponent.Antecedent
- Msvm_ServiceOfVssComponent.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5787dcdd4d8ce1aeefdc1fbafb2c156aec4d467a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314328"
---
# <a name="msvm_serviceofvsscomponent-class"></a>\_Classe MSVM ServiceOfVssComponent

Un'associazione tra un'istanza di [**MSVM \_ VssComponent**](msvm-vsscomponent.md) e un'istanza di [**MSVM \_ VssService**](msvm-vssservice.md) che rappresenta un servizio per l'esecuzione di operazioni sul componente VSS.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceOfVssComponent : CIM_Dependency
{
  Msvm_VssComponent REF Antecedent;
  Msvm_VssService   REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ ServiceOfVssComponent di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ServiceOfVssComponent di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ VssComponent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Antecedent")
</dt> </dl>

, [**MSVM \_ VssComponent**](msvm-vsscomponent.md) che rappresenta il componente VSS.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ VssService**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. dependent")
</dt> </dl>

Un [**\_ VssService MSVM**](msvm-vssservice.md) che rappresenta il servizio IC VSS.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> </dl>

 

