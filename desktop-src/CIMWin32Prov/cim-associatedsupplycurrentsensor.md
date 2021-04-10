---
description: La \_ classe CIM AssociatedSupplyCurrentSensor associa un alimentatore a un sensore corrente (amperaggio) che monitora la frequenza di input.
ms.assetid: bed4714f-ecf4-4c53-b231-c8fac673371f
ms.tgt_platform: multiple
title: Classe CIM_AssociatedSupplyCurrentSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyCurrentSensor
- CIM_AssociatedSupplyCurrentSensor.Dependent
- CIM_AssociatedSupplyCurrentSensor.Antecedent
- CIM_AssociatedSupplyCurrentSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70a88d87c68b36db5bd44413e3c68940db44f29b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225725"
---
# <a name="cim_associatedsupplycurrentsensor-class"></a>CIM \_ AssociatedSupplyCurrentSensor (classe)

La classe **CIM \_ AssociatedSupplyCurrentSensor** associa un alimentatore a un sensore corrente (amperaggio) che monitora la frequenza di input.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{29B273F2-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyCurrentSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_CurrentSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a>Members

La classe **CIM \_ AssociatedSupplyCurrentSensor** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ AssociatedSupplyCurrentSensor** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ CurrentSensor**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

[**\_ CurrentSensor CIM**](cim-currentsensor.md) che descrive il sensore corrente.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ alimentatore**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

[**\_ Alimentatore CIM**](cim-powersupply.md) che descrive l'alimentatore associato al sensore corrente.

</dd> <dt>

**MonitoringRange**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica l'intervallo di frequenza di input dell'alimentatore misurato dal sensore associato.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Intervallo 1** (2)


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Intervallo 2** (3)


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Entrambi i valori sono compresi tra 1 e 2** (4)


</dt> <dd>

Intervallo 1 e 2

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ AssociatedSupplyCurrentSensor** è derivata da [**CIM \_ AssociatedSensor**](cim-associatedsensor.md).

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

[**\_ASSOCIATEDSENSOR CIM**](cim-associatedsensor.md)
</dt> </dl>

 

