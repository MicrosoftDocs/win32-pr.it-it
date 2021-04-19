---
description: Associa il \_ BootSourceSettingData MSVM al VirtualSystemSettingData globale MSVM \_ .
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Classe Msvm_BootSourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dfe86fa7882b1b20e5b5abbbdaa9d4f37f231f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308342"
---
# <a name="msvm_bootsourcecomponent-class"></a>\_Classe MSVM BootSourceComponent

Associa il [**\_ BootSourceSettingData MSVM**](msvm-bootsourcesettingdata.md) al VirtualSystemSettingData globale [**MSVM \_**](msvm-virtualsystemsettingdata.md). Questa classe deriva dal [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe \_ BootSourceComponent di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ BootSourceComponent di MSVM** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'elemento padre nell'associazione. Questa proprietà viene ereditata [**dal \_ componente CIM**](cim-component.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'elemento figlio nell'associazione. Questa proprietà viene ereditata [**dal \_ componente CIM**](cim-component.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Componente CIM**](cim-component.md)
</dt> <dt>

[**\_Componente CIM**](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[**\_BootSourceSettingData MSVM**](msvm-bootsourcesettingdata.md)
</dt> <dt>

[**\_VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 

