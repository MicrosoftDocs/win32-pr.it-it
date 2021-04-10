---
description: La \_ classe CIM BasedOn rappresenta un'associazione che descrive come possono essere assemblati gli extent di archiviazione da extent di livello inferiore.
ms.assetid: 82132012-5851-4be8-82db-edbdb50b70e5
ms.tgt_platform: multiple
title: Classe CIM_BasedOn (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Dependent
- CIM_BasedOn.Antecedent
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e25cd9a5f194df8c5cbc0c7dc24a4777cee3417
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225724"
---
# <a name="cim_basedon-class-cimwin32-wmi-providers"></a>Classe CIM_BasedOn (provider WMI CIMWin32)

La classe **CIM \_ BasedOn** rappresenta un'associazione che descrive come possono essere assemblati gli extent di archiviazione da extent di livello inferiore. Ad esempio, gli extent fisici includono extent dello spazio protetto. I set di volumi vengono quindi assemblati da uno o più extent di spazio fisico o protetto. La memoria cache può essere definita in modo indipendente e realizzata in un elemento fisico oppure può essere basata su extent di archiviazione volatili o non volatili.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{8502C53E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Dependent;
  CIM_StorageExtent REF Antecedent;
  uint64                EndingAddress;
  uint64                StartingAddress;
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

Un [**\_ StorageExtent CIM**](cim-storageextent.md) che descrive l'extent di archiviazione di livello inferiore.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ StorageExtent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Un [**\_ StorageExtent CIM**](cim-storageextent.md) che descrive l'extent di archiviazione di livello superiore.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la fine dell'extent di alto livello nell'archiviazione di livello inferiore. Questa proprietà è utile quando si esegue il mapping di extent non contigui in un raggruppamento di livello superiore.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**IndirizzoIniziale**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica l'inizio dell'extent di alto livello nell'archiviazione di livello inferiore.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ BasedOn** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> </dl>

 

