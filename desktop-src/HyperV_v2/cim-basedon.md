---
description: Rappresenta un'associazione tra un oggetto CIM StorageExtent di livello superiore \_ e un oggetto CIM \_ StorageExtent di livello inferiore. Ad esempio, un oggetto CIM \_ ProtectedSpaceExtent fa parte di un oggetto CIM \_ PhysicalExtent.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: CIM_BasedOn classe (gestione Hyper-V)
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
ms.openlocfilehash: bd07a329388d1c4883674bc86f9cadf648746487ea44769141d91e90548722c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995767"
---
# <a name="cim_basedon-class-hyper-v-management"></a>CIM_BasedOn classe (gestione Hyper-V)

Rappresenta un'associazione tra un oggetto **CIM \_ StorageExtent** di livello superiore e un oggetto **CIM \_ StorageExtent di** livello inferiore. Ad esempio, [**un oggetto CIM \_ ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) fa parte di un [**oggetto CIM \_ PhysicalExtent.**](/windows/desktop/CIMWin32Prov/cim-physicalextent)

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

La **classe CIM \_ BasedOn** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ BasedOn** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ StorageExtent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Oggetto **CIM \_ StorageExtent di livello** inferiore.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ StorageExtent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Oggetto **CIM \_ StorageExtent di livello** superiore.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo che indica dove termina l'oggetto **CIM \_ StorageExtent** di livello superiore nell'archiviazione di livello inferiore. Questa proprietà è utile quando si esegue il mapping di oggetti **CIM \_ StorageExtent** non contigui in un raggruppamento di livello superiore.

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indice utilizzato per specificare l'ordine delle associazioni **CIM \_ BasedOn** in una raccolta. In caso contrario, "0" non indica alcun ordine. **CIM \_ Le istanze di BasedOn** con lo stesso valore dipendente devono inserire valori univoci nella **proprietà OrderIndex.** Il valore **OrderIndex più** basso specifica il primo membro della raccolta.

Un esempio dell'uso di questa proprietà è la definizione di una matrice con striped RAID-0 di 3 dischi. L'array RAID risultante è un extent di archiviazione dipendente da extent di archiviazione che descrivono ognuno dei 3 dischi. Il **valore OrderIndex** di ogni associazione **CIM \_ BasedOn** dagli extent del disco alla matrice RAID può essere specificato come 1, 2 e 3 per indicare l'ordine in cui gli extent del disco vengono usati per accedere ai dati RAID.

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo che indica dove inizia l'oggetto **CIM \_ StorageExtent** di livello superiore nell'archiviazione di livello inferiore.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> </dl>

 

