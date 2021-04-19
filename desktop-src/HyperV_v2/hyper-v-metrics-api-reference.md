---
description: L'API della metrica Hyper-V definisce gli elementi di programmazione seguenti.
ms.assetid: 00235614-9FCB-4161-B03D-9D557050153B
title: Informazioni di riferimento sull'API per le metriche Hyper-V
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdd4945bd390d995378c290f846335371fead753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310533"
---
# <a name="hyper-v-metrics-api-reference"></a>Informazioni di riferimento sull'API per le metriche Hyper-V

L'API della metrica Hyper-V definisce gli elementi di programmazione seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AggregationMetricDefinition MSVM**](msvm-aggregationmetricdefinition.md)<br/> | Rappresenta gli aspetti della definizione di una metrica derivata da un altro valore della metrica.<br/>                                                                                                                                                                                                                             |
| [**\_AggregationMetricValue MSVM**](msvm-aggregationmetricvalue.md)<br/>           | Rappresenta il valore dell'istanza di una metrica definita da un'istanza della classe [**MSVM \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) .<br/>                                                                                                                                                         |
| [**\_BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md)<br/>               | Rappresenta gli aspetti della definizione di una metrica.<br/>                                                                                                                                                                                                                                                                       |
| [**\_BaseMetricValue MSVM**](msvm-basemetricvalue.md)<br/>                         | Rappresenta un valore della metrica definito da un'istanza della classe [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) .<br/>                                                                                                                                                                                       |
| [**\_MetricCollectionDependency MSVM**](msvm-metriccollectiondependency.md)<br/>   | Rappresenta l'associazione tra due definizioni delle metriche o due valori di metrica.<br/>                                                                                                                                                                                                                                      |
| [**\_MetricDefForME MSVM**](msvm-metricdefforme.md)<br/>                           | Definisce l'associazione tra un [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) e un [**oggetto \_ gestito CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) per definire le metriche per quest'ultimo. La definizione delle metriche viene configurata in base al contesto da Managed, motivo per cui la definizione dipende dall'elemento.<br/> |
| [**\_MetricForME MSVM**](msvm-metricforme.md)<br/>                                 | Questa associazione collega un elemento gestito ai valori della metrica gestiti.<br/>                                                                                                                                                                                                                               |
| [**\_MetricInstance MSVM**](msvm-metricinstance.md)<br/>                           | Rappresenta un'associazione di oggetti valore della metrica con le rispettive definizioni di metrica.<br/>                                                                                                                                                                                                                                    |
| [**\_MetricService MSVM**](msvm-metricservice.md)<br/>                             | Offre la possibilità di gestire le metriche.<br/>                                                                                                                                                                                                                                                                              |
| [**\_MetricServiceCapabilities MSVM**](msvm-metricservicecapabilities.md)<br/>     | Descrive le funzionalità dell'istanza [**\_ MetricService di MSVM**](msvm-metricservice.md) associata.<br/>                                                                                                                                                                                                             |
| [**\_MetricServiceSettingData MSVM**](msvm-metricservicesettingdata.md)<br/>       | Rappresenta le impostazioni per il servizio metrico. Non è possibile modificare direttamente le proprietà di questa classe. Il client deve chiamare il metodo [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) per modificare una di queste proprietà.<br/>                                                              |



 

 

