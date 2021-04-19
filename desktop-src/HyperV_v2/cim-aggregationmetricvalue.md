---
description: Rappresenta il valore dell'istanza di una metrica definita da un'istanza di CIM \_ AggregationMetricDefinition.
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: Classe CIM_AggregationMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0af264b66838e7c039ef3f99a4f365ebab55c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310587"
---
# <a name="cim_aggregationmetricvalue-class"></a>CIM \_ AggregationMetricValue (classe)

Rappresenta il valore dell'istanza di una metrica definita da un'istanza di **CIM \_ AggregationMetricDefinition**.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>Members

La classe **CIM \_ AggregationMetricValue** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ AggregationMetricValue** dispone di queste proprietà.

<dl> <dt>

**AggregationDuration**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**AggregationTimeStamp**")
</dt> </dl>

Rappresenta la durata dell'intervallo di tempo in cui è stata calcolata l'aggregazione. L'inizio di un intervallo di monitoraggio sul quale viene applicata la funzione di aggregazione viene determinato sottraendo il valore **AggregationDuration** dal valore di **AggregationTimestamp** .

</dd> <dt>

**AggregationTimeStamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**Durata**")
</dt> </dl>

Ora di applicazione della funzione di aggregazione per determinare il valore dell'istanza della metrica. Questa operazione è diversa dal momento in cui viene creata l'istanza. Il valore **AggregationTimeStamp** cambia ogni volta che viene applicata la funzione di aggregazione per calcolare il valore.

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

[**\_BASEMETRICVALUE CIM**](cim-basemetricvalue.md)
</dt> </dl>

 

