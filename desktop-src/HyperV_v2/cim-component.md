---
description: Rappresenta un'associazione generica tra un elemento gestito padre e un elemento gestito figlio in cui l'elemento figlio rappresenta un componente o parte dell'elemento padre.
ms.assetid: b5cef452-2d00-483c-8e70-f804f1e3536b
title: Classe CIM_Component (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56ff83a4da51ba18205a8d8ab5e6e57ea1a7794b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313383"
---
# <a name="cim_component-class-hyper-v-management"></a>Classe CIM_Component (gestione Hyper-V)

Rappresenta un'associazione generica tra un elemento gestito padre e un elemento gestito figlio in cui l'elemento figlio rappresenta un componente o parte dell'elemento padre.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Aggregation, Version("2.7.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a>Members

La classe del **\_ componente CIM** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe del **\_ componente CIM** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ Managed**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**aggregazione**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Elemento padre nell'associazione.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ Managed**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Elemento figlio nell'associazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

