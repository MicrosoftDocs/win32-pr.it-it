---
description: Rappresenta un'associazione in cui vengono raccolti i valori delle metriche per un elemento gestito.
ms.assetid: 00752751-bc27-463b-a4ac-4db8e5040077
title: Classe CIM_MetricForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricForME
- CIM_MetricForME.Antecedent
- CIM_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89c119ad622b778d0402100a64ff15befe623685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314358"
---
# <a name="cim_metricforme-class"></a>CIM \_ MetricForME (classe)

Rappresenta un'associazione in cui vengono raccolti i valori delle metriche per un elemento gestito.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricForME : CIM_Dependency
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ MetricForME** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ MetricForME** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ Managed**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Elemento gestito nell'associazione.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ BaseMetricValue**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Valore della metrica nell'associazione.

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

 

