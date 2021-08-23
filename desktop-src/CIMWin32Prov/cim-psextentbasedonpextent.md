---
description: La classe \_ CIM PSExtentBasedOnPExtent associa gli extent dello spazio protetto basati su un extent fisico.
ms.assetid: 4b89319c-022c-4ff4-91ec-70c435a5888a
ms.tgt_platform: multiple
title: CIM_PSExtentBasedOnPExtent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PSExtentBasedOnPExtent
- CIM_PSExtentBasedOnPExtent.EndingAddress
- CIM_PSExtentBasedOnPExtent.StartingAddress
- CIM_PSExtentBasedOnPExtent.Dependent
- CIM_PSExtentBasedOnPExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 788d19eb2d9d11f5515f3507431498e713b3d1f98871ec79065f616cc606dea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080325"
---
# <a name="cim_psextentbasedonpextent-class"></a>Classe \_ CIM PSExtentBasedOnPExtent

La **classe \_ CIM PSExtentBasedOnPExtent** associa gli extent dello spazio protetto basati su un extent fisico.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{451FE14C-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_PSExtentBasedOnPExtent : CIM_BasedOn
{
  uint64                       EndingAddress;
  uint64                       StartingAddress;
  CIM_ProtectedSpaceExtent REF Dependent;
  CIM_PhysicalExtent       REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe \_ CIM PSExtentBasedOnPExtent** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ PSExtentBasedOnPExtent** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalExtent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Oggetto [**CiM \_ PhysicalExtent**](cim-physicalextent.md) che descrive l'extent fisico.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ProtectedSpaceExtent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Oggetto [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) che descrive l'extent dello spazio protetto basato sull'extent fisico.

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

La **classe CIM \_ PSExtentBasedOnPExtent** è derivata da [**CIM \_ BasedOn.**](cim-basedon.md)

WMI non implementa questa classe.

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

 

