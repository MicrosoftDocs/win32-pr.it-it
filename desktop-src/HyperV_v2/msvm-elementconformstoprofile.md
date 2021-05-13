---
description: Definisce i profili registrati a cui è conforme il sistema di riferimento.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Msvm_ElementConformsToProfile classe
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
ms.openlocfilehash: e9b4e257c2ebc0584a8291461439f75238599d35
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843282"
---
# <a name="msvm_elementconformstoprofile-class"></a>Classe Msvm \_ ElementConformsToProfile

Definisce i profili registrati a cui è conforme il sistema di riferimento. Questa associazione può essere applicata a qualsiasi elemento gestito. L'utilizzo tipico lo applicherà a un'istanza di livello superiore, ad esempio un sistema, uno spazio dei nomi o un servizio. Quando viene applicato a un'istanza di livello superiore, tutte le parti costituenti devono comportarsi in modo appropriato per supportare la conformità dell'elemento gestito al profilo registrato denominato.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ ElementConformsToProfile** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ElementConformsToProfile** ha queste proprietà.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ RegisteredProfile**](msvm-registeredprofile.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ RegisteredProfile**](msvm-registeredprofile.md) che rappresenta il profilo registrato a cui il sistema è conforme.

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) che rappresenta il sistema conforme al profilo registrato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 solo \[ app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

