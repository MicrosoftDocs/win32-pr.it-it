---
description: Associazione che descrive come assemblare gli extent di archiviazione da extent di livello inferiore.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Msvm_BasedOn classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f3f8138fcc06d5e2d100f38b0333dcbfc5e76c61366da686b313a70d40ffa120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790251"
---
# <a name="msvm_basedon-class"></a>Classe Msvm \_ BasedOn

Associazione che descrive come assemblare gli extent di archiviazione da extent di livello inferiore. Ad esempio, ProtectedSpaceExtents è una parte di PhysicalExtents, mentre i VolumeSet vengono assemblati da uno o più oggetti Physical o ProtectedSpaceExtents. Come altro esempio, CacheMemory può essere definito in modo indipendente e realizzato in un elemento PhysicalElement o può essere basato su Volatile o NonVolatileStorageExtents.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ BasedOn** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ BasedOn** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Extent di archiviazione di livello inferiore. Questa proprietà viene ereditata da [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Extent di archiviazione di livello superiore. Questa proprietà viene ereditata da [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo finale in cui, nell'archiviazione di livello inferiore, termina l'extent di livello superiore. Questa proprietà è utile quando si esegue il mapping di extent non contigui in un raggruppamento di livello superiore. Questa proprietà viene ereditata da [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se è presente un ordine per l'oggetto in base alle associazioni che descrivono come viene assemblato un extent di archiviazione di livello superiore, la **proprietà OrderIndex** lo indica. Quando esiste un ordine, le istanze con lo stesso **valore Dependent** (lo stesso extent di livello superiore) devono inserire valori univoci nella **proprietà OrderIndex.** Il valore più basso implica il primo membro della raccolta di extent di livello inferiore e i valori crescenti implicano membri successivi della raccolta. Se non esiste alcuna relazione ordinata, è necessario che sia specificato un valore pari a zero. Un esempio dell'uso di questa proprietà è la definizione di una matrice con striped RAID-0 di tre dischi. L'array RAID risultante è un extent di archiviazione che dipende da extent di archiviazione che descrivono ognuno dei tre dischi. **L'elemento OrderIndex** di ogni associazione dagli extent del disco alla matrice RAID può essere specificato come 1, 2 e 3 per indicare l'ordine in cui gli extent del disco vengono usati per accedere ai dati RAID. Questa proprietà viene ereditata da [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**Indirizzo iniziale**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo iniziale in cui, nell'archiviazione di livello inferiore, inizia l'extent di livello superiore. Questa proprietà viene ereditata da [**CIM \_ BasedOn.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

