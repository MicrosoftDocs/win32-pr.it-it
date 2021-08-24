---
description: Gestisce le metriche per gli elementi gestiti.
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: CIM_MetricService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5fd976abf5bce91ffbc5581e73f93c2a8422fcdcbe69fd70745511362e504d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694941"
---
# <a name="cim_metricservice-class"></a>Classe CIM \_ MetricService

Gestisce le metriche per gli elementi gestiti.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a>Members

La **classe CIM \_ MetricService** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe CIM \_ MetricService** include questi metodi.



| Metodo                                                                   | Descrizione                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Metrica di controllo**](cim-metricservice-controlmetrics.md)               | Abilita e disabilita la raccolta di metriche.<br/>                                                                                                                          |
| [**ControlMetricsByClass**](cim-metricservice-controlmetricsbyclass.md) | Abilita e disabilita la raccolta di metriche per una classe.<br/>                                                                                                              |
| [**ControlSampleTimes**](cim-metricservice-controlsampletimes.md)       | Specifica quando vengono raccolte le metriche.<br/>                                                                                                                                     |
| [**GetMetricValues**](cim-metricservice-getmetricvalues.md)             | Recupera un elenco filtrato di valori delle metriche.<br/>                                                                                                                              |
| [**ShowMetrics**](cim-metricservice-showmetrics.md)                     | Indica se la raccolta di metriche è abilitata per gli elementi gestiti specificati e indica le metriche disponibili per la raccolta per ogni elemento gestito.<br/> |
| [**ShowMetricsByClass**](cim-metricservice-showmetricsbyclass.md)       | Indica le metriche disponibili per la raccolta per tutte le istanze di una classe CIM.<br/>                                                                                   |



 

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

[**Servizio \_ CIM**](cim-service.md)
</dt> </dl>

 

 




