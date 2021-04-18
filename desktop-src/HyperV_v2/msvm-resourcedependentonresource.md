---
description: Stabilisce che un' \_ istanza di RESOURCEALLOCATIONSETTINGDATA CIM che rappresenta un'allocazione di risorse dipende da un'altra allocazione di risorse.
ms.assetid: 567ee36a-d47b-444d-8d2f-425873f95bef
title: Classe Msvm_ResourceDependentOnResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceDependentOnResource
- Msvm_ResourceDependentOnResource.Antecedent
- Msvm_ResourceDependentOnResource.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 29cf3b607449c6a9145568e3ee858248af3c4248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313846"
---
# <a name="msvm_resourcedependentonresource-class"></a>\_Classe MSVM ResourceDependentOnResource

Stabilisce che un'istanza di [**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) che rappresenta un'allocazione di risorse dipende da un'altra allocazione di risorse.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceDependentOnResource : CIM_Dependency
{
  CIM_ResourceAllocationSettingData REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ ResourceDependentOnResource di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ResourceDependentOnResource di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ResourceAllocationSettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

[**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) che rappresenta la risorsa indipendente in questa associazione.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ResourceAllocationSettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Un [**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) che rappresenta la risorsa dipendente dall'attività precedente.

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

 

