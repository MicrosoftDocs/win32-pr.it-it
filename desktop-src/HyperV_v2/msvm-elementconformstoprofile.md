---
description: Definisce i profili registrati a cui è conforme il sistema a cui si fa riferimento.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Classe Msvm_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b0afdc7dd9d55a036de0695f9a88a95d2b01308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314831"
---
# <a name="msvm_elementconformstoprofile-class"></a>\_Classe MSVM ElementConformsToProfile

Definisce i profili registrati a cui è conforme il sistema a cui si fa riferimento. Questa associazione può essere applicata a qualsiasi elemento gestito. L'utilizzo tipico lo applicherà a un'istanza di livello superiore, ad esempio un sistema, uno spazio dei nomi o un servizio. Quando viene applicato a un'istanza di livello superiore, tutte le parti costituenti devono comportarsi in modo appropriato per supportare la conformità dell'elemento gestito al profilo registrato denominato.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Members

La **classe \_ ElementConformsToProfile di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ElementConformsToProfile di MSVM** dispone di queste proprietà.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ RegisteredProfile**](msvm-registeredprofile.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ RegisteredProfile**](msvm-registeredprofile.md) che rappresenta il profilo registrato a cui è conforme il sistema.

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta il sistema conforme al profilo registrato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

