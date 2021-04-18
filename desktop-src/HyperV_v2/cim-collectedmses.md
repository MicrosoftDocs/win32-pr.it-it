---
description: Rappresenta un'associazione generica tra una raccolta di elementi di sistema gestiti e i membri della raccolta.
ms.assetid: c9e2bbca-67be-41f2-a94c-cf4eaf5f4694
title: Classe CIM_CollectedMSEs (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdf5c5d682f1b6e1b47b64100b3e00f5f79cebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315524"
---
# <a name="cim_collectedmses-class-hyper-v-management"></a>Classe CIM_CollectedMSEs (gestione Hyper-V)

Rappresenta un'associazione generica tra una raccolta di elementi di sistema gestiti e i membri della raccolta.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectedMSEs : CIM_MemberOfCollection
{
  CIM_CollectionOfMSEs     REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a>Members

La classe **CIM \_ CollectedMSEs** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ CollectedMSEs** dispone di queste proprietà.

<dl> <dt>

**Raccolta**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Raccolta.

</dd> <dt>

**Membro**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")
</dt> </dl>

Membri della raccolta.

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

[**\_MEMBEROFCOLLECTION CIM**](cim-memberofcollection.md)
</dt> </dl>

 

