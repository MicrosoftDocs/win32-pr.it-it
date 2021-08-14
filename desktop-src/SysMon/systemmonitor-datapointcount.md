---
title: SystemMonitor.DataPointCount - proprietà
description: Recupera o imposta il numero di punti dati visualizzati in un grafico a linee.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Proprietà DataPointCount SysMon
- Proprietà DataPointCount SysMon , oggetto SystemMonitor
- Oggetto SystemMonitor SysMon , proprietà DataPointCount
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d7d1212f3f1467c0fb505e84dffdd9cc6bb381c19d8ccc34ad38ee46562ec6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882626"
---
# <a name="systemmonitordatapointcount-property"></a>SystemMonitor.DataPointCount - proprietà

Recupera o imposta il numero di punti dati visualizzati in un grafico a linee.

## <a name="syntax"></a>Sintassi


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>Valore proprietà

Numero di punti dati visualizzati nella visualizzazione per un grafico a linee. Il valore predefinito è 100 punti dati. L'intervallo valido di valori è compreso tra 2 e 1.000.

## <a name="remarks"></a>Commenti

Questa proprietà viene usata solo se [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) è **sysmonCurrentActivity.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





