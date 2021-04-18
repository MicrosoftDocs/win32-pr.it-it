---
description: Associa un sistema a un dispositivo logico che è un componente del sistema.
ms.assetid: d5a36f71-5ebe-46e2-aaa9-5d99fa075d31
title: Classe CIM_SystemDevice (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.GroupComponent
- CIM_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b02921e4be0f8aa0cddc194a2ed430e10e115eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310575"
---
# <a name="cim_systemdevice-class-hyper-v-management"></a>Classe CIM_SystemDevice (gestione Hyper-V)

Associa un sistema a un dispositivo logico che è un componente del sistema.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ SystemDevice** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ SystemDevice** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ sistema CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Riferimento [**di \_ sistema CIM**](cim-system.md) al sistema padre nell'associazione.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Un riferimento [**CIM \_ LogicalDevice**](cim-logicaldevice.md) al dispositivo logico che è un componente del sistema.

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

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> </dl>

 

