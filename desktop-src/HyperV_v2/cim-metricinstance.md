---
description: Rappresenta un'associazione tra un'istanza di un valore di metrica e una definizione di metrica.
ms.assetid: 4c620a7a-8b15-49ad-ae84-246e2fca175d
title: CIM_MetricInstance classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricInstance
- CIM_MetricInstance.Antecedent
- CIM_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3ff08757b8043e51d43079be6011b69731bdc761f22da27ff85272b95d4795c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695061"
---
# <a name="cim_metricinstance-class"></a>Classe CIM \_ MetricInstance

Rappresenta un'associazione tra un'istanza di un valore di metrica e una definizione di metrica.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricInstance : CIM_Dependency
{
  CIM_BaseMetricDefinition REF Antecedent;
  CIM_BaseMetricValue      REF Dependent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ MetricInstance** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ MetricInstance** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ BaseMetricDefinition**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Definizione del valore della metrica.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ BaseMetricValue**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Valore della metrica associato alla definizione della metrica.

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

 

