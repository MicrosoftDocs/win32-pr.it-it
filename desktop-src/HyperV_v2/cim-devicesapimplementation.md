---
description: Rappresenta un'associazione tra un punto di accesso al servizio (SAP) e un dispositivo logico che lo implementa.
ms.assetid: 40c8111a-d439-4c0f-805e-9c10d7182eb4
title: Classe CIM_DeviceSAPImplementation (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Antecedent
- CIM_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e32676077cccd5c7e17fa551e904079f457b8d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308356"
---
# <a name="cim_devicesapimplementation-class-hyper-v-management"></a>Classe CIM_DeviceSAPImplementation (gestione Hyper-V)

Rappresenta un'associazione tra un punto di accesso al servizio (SAP) e un dispositivo logico che lo implementa.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ DeviceSAPImplementation** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ DeviceSAPImplementation** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Il dispositivo logico.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ serviceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

SAP implementato dal dispositivo logico.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> </dl>

 

