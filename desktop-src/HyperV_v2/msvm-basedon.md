---
description: Associazione che descrive come possono essere assemblati gli extent di archiviazione dagli extent di livello inferiore.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Classe Msvm_BasedOn
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
ms.openlocfilehash: 8262ae5e510574bf02630410b584d9df10d64ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317208"
---
# <a name="msvm_basedon-class"></a>\_Classe MSVM BasedOn

Associazione che descrive come possono essere assemblati gli extent di archiviazione dagli extent di livello inferiore. Ad esempio, ProtectedSpaceExtents sono parti di PhysicalExtents, mentre VolumeSets vengono assemblati da uno o più fisici o ProtectedSpaceExtents. Come altro esempio, CacheMemory può essere definito in modo indipendente e realizzato in un oggetto PhysicalElement oppure può essere basato su volatile o NonVolatileStorageExtents.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

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

La **classe \_ BasedOn di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ BasedOn di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Extent di archiviazione di livello inferiore. Questa proprietà viene ereditata da [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Extent di archiviazione di livello superiore. Questa proprietà viene ereditata da [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo finale in cui termina, nell'archiviazione di livello inferiore, l'extent di livello superiore. Questa proprietà è utile quando si esegue il mapping di extent non contigui in un raggruppamento di livello superiore. Questa proprietà viene ereditata da [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se è presente un ordine per l'oggetto in base alle associazioni che descrivono come viene assemblato un extent di archiviazione di livello superiore, la proprietà **OrderIndex** indica questa. Quando esiste un ordine, le istanze con lo stesso valore **dipendente** (lo stesso extent di livello superiore) devono inserire valori univoci nella proprietà **OrderIndex** . Il valore più basso implica il primo membro della raccolta di extent di livello inferiore e i valori crescenti implicano i membri successivi della raccolta. Se non è presente alcuna relazione ordinata, è necessario specificare un valore pari a zero. Un esempio di utilizzo di questa proprietà è la definizione di una matrice con striping RAID 0 di tre dischi. La matrice RAID risultante è un extent di archiviazione che dipende dagli extent di archiviazione che descrivono ognuno dei tre dischi. Per indicare l'ordine in cui vengono usati gli extent del disco per accedere ai dati RAID, è possibile specificare il **OrderIndex** di ogni associazione tra gli extent del disco e la matrice RAID come 1, 2 e 3. Questa proprietà viene ereditata da [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> <dt>

**IndirizzoIniziale**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo iniziale in cui inizia l'extent di livello superiore nell'archiviazione di livello più basso. Questa proprietà viene ereditata da [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

