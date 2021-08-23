---
description: Definisce i profili registrati a cui è conforme il sistema autonomo a cui si fa riferimento.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Msvm_StandaloneV2ElementConformsToProfile classe
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
ms.openlocfilehash: 5506119f0e8938a29b94b298460a1f164dab97359d13d956bfa5ca74e97a081b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950240"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a>Classe Msvm \_ StandaloneV2ElementConformsToProfile

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

La **classe Msvm \_ StandaloneV2ElementConformsToProfile** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ StandaloneV2ElementConformsToProfile** ha queste proprietà.

<dl> <dt>

**Standard conforme**
</dt> <dd> <dl> <dt>

Tipo di dati: **Msvm \_ RegisteredProfile**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Profilo registrato a cui è conforme il sistema autonomo.

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **Msvm \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**esegue l'override**](/windows/desktop/WmiSdk/standard-qualifiers)di **, MSFT \_ TargetNamespace** ("root \\ \\ virtualization \\ \\ v2")
</dt> </dl>

Sistema autonomo conforme al profilo registrato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Interoperabilità \\ radice<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento \_ MsvmConformsToProfile**](msvm-elementconformstoprofile.md)
</dt> </dl>

 

