---
description: L'API delle metriche di Hyper-V definisce gli elementi di programmazione seguenti.
ms.assetid: 00235614-9FCB-4161-B03D-9D557050153B
title: Informazioni di riferimento sulle API delle metriche di Hyper-V
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b833d96d26a3c48183c341ab0f1ff2bc9f5b178ca4439e1c035d82551ec3e094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532251"
---
# <a name="hyper-v-metrics-api-reference"></a>Informazioni di riferimento sulle API delle metriche di Hyper-V

L'API delle metriche di Hyper-V definisce gli elementi di programmazione seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md)<br/> | Rappresenta gli aspetti della definizione di una metrica derivata da un altro valore della metrica.<br/>                                                                                                                                                                                                                             |
| [**Msvm \_ AggregationMetricValue**](msvm-aggregationmetricvalue.md)<br/>           | Rappresenta il valore dell'istanza di una metrica definita da un'istanza della [**classe Msvm \_ AggregationMetricDefinition.**](msvm-aggregationmetricdefinition.md)<br/>                                                                                                                                                         |
| [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)<br/>               | Rappresenta gli aspetti della definizione di una metrica.<br/>                                                                                                                                                                                                                                                                       |
| [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md)<br/>                         | Rappresenta un valore della metrica definito da un'istanza della [**classe \_ BaseMetricDefinition msvm.**](msvm-basemetricdefinition.md)<br/>                                                                                                                                                                                       |
| [**Msvm \_ MetricCollectionDependency**](msvm-metriccollectiondependency.md)<br/>   | Rappresenta l'associazione tra due definizioni di metrica o due valori delle metriche.<br/>                                                                                                                                                                                                                                      |
| [**Msvm \_ MetricDefForME**](msvm-metricdefforme.md)<br/>                           | Definisce l'associazione tra [**un oggetto \_ BaseMetricDefinition msvm**](msvm-basemetricdefinition.md) e [**un elemento \_ CIM ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) per definire le metriche per quest'ultimo. La definizione delle metriche viene data al contesto da ManagedElement, motivo per cui la definizione dipende dall'elemento.<br/> |
| [**Msvm \_ MetricForME**](msvm-metricforme.md)<br/>                                 | Questa associazione collega un elemento gestito ai valori delle metriche mantenuti per tale elemento.<br/>                                                                                                                                                                                                                               |
| [**Msvm \_ MetricInstance**](msvm-metricinstance.md)<br/>                           | Rappresenta un'associazione di oggetti valore della metrica con le relative definizioni di metrica.<br/>                                                                                                                                                                                                                                    |
| [**Msvm \_ MetricService**](msvm-metricservice.md)<br/>                             | Consente di gestire le metriche.<br/>                                                                                                                                                                                                                                                                              |
| [**Msvm \_ MetricServiceCapabilities**](msvm-metricservicecapabilities.md)<br/>     | Descrive le funzionalità dell'istanza [**msvm \_ MetricService**](msvm-metricservice.md) associata.<br/>                                                                                                                                                                                                             |
| [**Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md)<br/>       | Rappresenta le impostazioni per il servizio metrica. Le proprietà per questa classe non possono essere modificate direttamente. Il client deve chiamare il [**metodo ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) per modificare una di queste proprietà.<br/>                                                              |



 

 

