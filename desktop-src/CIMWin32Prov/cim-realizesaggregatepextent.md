---
description: L'associazione CIM RealizesAggregatePExtent rappresenta la relazione in cui viene realizzata la classe \_ CIM \_ AggregatePExtent su un supporto fisico.
ms.assetid: 420dde1d-daa8-4cd3-b3fd-c2aefdc1e217
ms.tgt_platform: multiple
title: CIM_RealizesAggregatePExtent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesAggregatePExtent
- CIM_RealizesAggregatePExtent.Dependent
- CIM_RealizesAggregatePExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c5eaf7e53fc7972795d0502c156e753bae60c777987e7304ef27a3a3fde54e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920941"
---
# <a name="cim_realizesaggregatepextent-class"></a>Classe CIM \_ RealizesAggregatePExtent

**L'associazione CIM \_ RealizesAggregatePExtent** rappresenta la relazione in cui viene realizzata la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) su un supporto fisico.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B81-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesAggregatePExtent : CIM_Realizes
{
  CIM_AggregatePExtent REF Dependent;
  CIM_PhysicalMedia    REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ RealizesAggregatePExtent** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ RealizesAggregatePExtent** ha queste proprietà.

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

Tipo di dati: **CIM \_ AggregatePExtent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

[**CiM \_ AggregatePExtent**](cim-aggregatepextent.md) che si trova nel supporto.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ RealizesAggregatePExtent** è derivata da [**CIM \_ Realizes.**](cim-realizes.md)

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

 

