---
description: Definisce i profili registrati a cui è conforme il sistema autonomo a cui si fa riferimento.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Classe Msvm_StandaloneV2ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c492ad5bdd0e50bbbe86fd220000099269501ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967028"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a>\_Classe MSVM StandaloneV2ElementConformsToProfile

Definisce i profili registrati a cui è conforme il sistema autonomo a cui si fa riferimento.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Members

La **classe \_ StandaloneV2ElementConformsToProfile di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ StandaloneV2ElementConformsToProfile di MSVM** dispone di queste proprietà.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ RegisteredProfile**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Profilo registrato a cui è conforme il sistema autonomo.

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT \_ targetNamespace** ("root \\ \\ Virtualization \\ \\ v2")
</dt> </dl>

Sistema autonomo conforme al profilo registrato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Interoperabilità radice<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ElementConformsToProfile MSVM**](msvm-elementconformstoprofile.md)
</dt> </dl>

 

