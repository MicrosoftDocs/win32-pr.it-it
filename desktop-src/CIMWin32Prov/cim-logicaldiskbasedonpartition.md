---
description: La classe CIM LogicalDiskBasedOnPartition associa un disco logico alla partizione del disco \_ in cui risiede.
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: CIM_LogicalDiskBasedOnPartition classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27e0805d4fa3a4a59d59423b30b3644e78ccc6138509b2b0f71cdecb435ffc7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679873"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a>Classe \_ CiM LogicalDiskBasedOnPartition

La **classe \_ CIM LogicalDiskBasedOnPartition** associa un disco logico alla partizione del disco in cui risiede.

Ad esempio, l'unità C di un computer può trovarsi in una partizione in un supporto fisico locale, a indicare che un disco logico non può estendersi su più di una partizione. Quando un disco logico può estendersi su più di una partizione, tuttavia, il disco logico è basato sulla configurazione RAID , ad esempio un mirror o un set di stripe. In tal caso, il disco logico è basato sul volume di archiviazione. Per impedire l'uso non corretto dell'associazione **\_ CIM LogicalDiskBasedOnPartition,** il qualificatore **Max(1)** è stato inserito nel riferimento precedente alla partizione del disco. 

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe \_ CIM LogicalDiskBasedOnPartition** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ LogicalDiskBasedOnPartition** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ DiskPartition**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Oggetto [**CIM \_ DiskPartition**](cim-diskpartition.md) che descrive la partizione del disco.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDisk**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Disco [**logico CIM \_**](cim-logicaldisk.md) che descrive il disco logico basato sulla partizione.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la fine dell'extent di alto livello nell'archiviazione di livello inferiore. Questa proprietà è utile quando si esegue il mapping di extent non contigui in un raggruppamento di livello superiore.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Questa proprietà viene ereditata da [**CIM \_ BasedOn.**](cim-basedon.md)

</dd> <dt>

**Indirizzo iniziale**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica l'inizio dell'extent di alto livello nell'archiviazione di livello inferiore.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Questa proprietà viene ereditata da [**CIM \_ BasedOn.**](cim-basedon.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ LogicalDiskBasedOnPartition** è derivata da [**CIM \_ BasedOn.**](cim-basedon.md)

WMI non implementa questa classe. Per le classi derivate **da CIM \_ LogicalDiskBasedOnPartition,** vedere [Classi Win32.](win32-provider.md)

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ BasedOn**](cim-basedon.md)
</dt> </dl>

 

