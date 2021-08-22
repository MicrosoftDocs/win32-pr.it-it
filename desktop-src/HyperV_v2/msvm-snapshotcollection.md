---
description: Rappresenta una raccolta di snapshot del sistema virtuale.
ms.assetid: c9b64421-232c-4f32-a088-6b98602ca3f4
title: Msvm_SnapshotCollection classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotCollection
- Msvm_SnapshotCollection.CollectionID
- Msvm_SnapshotCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fc83a12fc67192f686ddd75d6bc9626d9403244b2cbc8490270d236741174cdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950290"
---
# <a name="msvm_snapshotcollection-class"></a>Classe Msvm \_ SnapshotCollection

Rappresenta una raccolta di snapshot del sistema virtuale.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotCollection : CIM_Collection
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SnapshotCollection** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SnapshotCollection** ha queste proprietà.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificazione univoca dell'oggetto raccolta.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Nome definito dall'utente per la raccolta. Si noti che non è garantito che sia univoco.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Raccolta \_ CIM**](cim-collection.md)
</dt> </dl>

 

