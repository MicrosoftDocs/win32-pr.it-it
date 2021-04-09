---
description: Rappresenta un'associazione tra un oggetto StorageExtent CIM di livello superiore \_ e un oggetto STORAGEEXTENT CIM di livello inferiore \_ . Un \_ oggetto CIM ProtectedSpaceExtent, ad esempio, fa parte di un \_ oggetto CIM PhysicalExtent.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: Classe CIM_BasedOn (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879109"
---
# <a name="cim_basedon-class-hyper-v-management"></a>Classe CIM_BasedOn (gestione Hyper-V)

Rappresenta un'associazione tra un oggetto **\_ StorageExtent CIM** di livello superiore e un oggetto **\_ StorageExtent CIM** di livello inferiore. Un oggetto [**CIM \_ ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) , ad esempio, fa parte di un oggetto [**CIM \_ PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) .

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>Members

La classe **CIM \_ BasedOn** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ BasedOn** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ StorageExtent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Oggetto **\_ StorageExtent CIM** di livello inferiore.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ StorageExtent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Oggetto **\_ StorageExtent CIM** di livello superiore.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo che indica il punto in cui si conclude l'oggetto di archiviazione di livello inferiore, l'oggetto **\_ StorageExtent** di livello superiore. Questa proprietà è utile quando si esegue il mapping di oggetti **CIM \_ StorageExtent** non contigui in un raggruppamento di livello superiore.

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indice utilizzato per specificare l'ordine delle associazioni **CIM \_ BasedOn** in una raccolta; in caso contrario, "0" indica nessun ordine. **CIM \_** Le istanze di BasedOn con lo stesso valore dipendente devono inserire valori univoci nella proprietà **OrderIndex** . Il valore **OrderIndex** più basso specifica il primo membro della raccolta.

Un esempio di utilizzo di questa proprietà è la definizione di una matrice con striping RAID 0 di 3 dischi. La matrice RAID risultante è un extent di archiviazione che dipende dagli extent di archiviazione che descrivono ognuno dei 3 dischi. Il valore **OrderIndex** di ogni associazione **CIM \_ BasedOn** da extent del disco all'array RAID può essere specificato come 1, 2 e 3 per indicare l'ordine in cui gli extent del disco vengono usati per accedere ai dati RAID.

</dd> <dt>

**IndirizzoIniziale**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo che indica il punto in cui viene avviata l'oggetto **\_ StorageExtent** di livello più alto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> </dl>

 

