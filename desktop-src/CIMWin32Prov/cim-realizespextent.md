---
description: L'associazione CIM \_ RealizesPExtent rappresenta la relazione in cui gli extent fisici vengono realizzati su un supporto fisico. Viene inoltre specificato l'indirizzo iniziale dell'extent fisico nel supporto fisico.
ms.assetid: 9abe1a7d-8463-4d48-8cec-52bf934ad08b
ms.tgt_platform: multiple
title: CIM_RealizesPExtent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesPExtent
- CIM_RealizesPExtent.Dependent
- CIM_RealizesPExtent.Antecedent
- CIM_RealizesPExtent.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 697ca0386d03ade55895f63cab67b3144bf50b3d0ffea2928633384e4d1f502a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920841"
---
# <a name="cim_realizespextent-class"></a>Classe CIM \_ RealizesPExtent

**L'associazione CIM \_ RealizesPExtent** rappresenta la relazione in cui gli extent fisici vengono realizzati su un supporto fisico. Viene inoltre specificato l'indirizzo iniziale dell'extent fisico nel supporto fisico.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B7F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesPExtent : CIM_Realizes
{
  CIM_PhysicalExtent REF Dependent;
  CIM_PhysicalMedia  REF Antecedent;
  uint64                 StartingAddress;
};
```

## <a name="members"></a>Members

La **classe CIM \_ RealizesPExtent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ RealizesPExtent** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalMedia**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Oggetto [**CIM \_ PhysicalMedia**](cim-physicalmedia.md) che descrive i supporti fisici in cui viene realizzato l'extent.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalExtent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Oggetto [**CIM \_ PhysicalExtent**](cim-physicalextent.md) che descrive l'extent fisico che si trova nel supporto.

</dd> <dt>

**Indirizzo iniziale**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo iniziale sul supporto fisico in cui inizia l'extent fisico. L'indirizzo finale dell'extent fisico viene determinato usando le **proprietà NumberOfBlocks** e **BlockSize** dell'oggetto [**\_ PhysicalExtent CIM.**](cim-physicalextent.md)

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ RealizesPExtent** è derivata da [**CIM \_ Realizes**](cim-realizes.md).

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

[**CIM \_ Realizes**](cim-realizes.md)
</dt> </dl>

 

