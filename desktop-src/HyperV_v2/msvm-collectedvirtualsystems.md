---
description: Associa il \_ VirtualSystemCollection MSVM agli oggetti contenuti MSVM \_ ComputerSystem.
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Classe Msvm_CollectedVirtualSystems
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedVirtualSystems
- Msvm_CollectedVirtualSystems.Collection
- Msvm_CollectedVirtualSystems.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0803eda14ffbaf21ee2bf4491bd835123b7191e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317205"
---
# <a name="msvm_collectedvirtualsystems-class"></a>\_Classe MSVM CollectedVirtualSystems

Associa il [**\_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) agli oggetti contenuti [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a>Members

La **classe \_ CollectedVirtualSystems di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CollectedVirtualSystems di MSVM** dispone di queste proprietà.

<dl> <dt>

**Raccolta**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ VirtualSystemCollection**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Oggetto di raggruppamento o ' contenitore ' di [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) che rappresenta la raccolta.

</dd> <dt>

**Membro**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")
</dt> </dl>

Oggetto [**MSVM \_ ComputerSystem**](msvm-computersystem.md) contenente i membri della raccolta.

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

[**\_COLLECTEDMSES CIM**](cim-collectedmses.md)
</dt> </dl>

 

