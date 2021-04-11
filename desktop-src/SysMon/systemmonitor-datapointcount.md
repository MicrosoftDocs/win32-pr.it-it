---
title: Proprietà SystemMonitor. DataPointCount
description: Recupera o imposta il numero di punti dati visualizzati in un grafico a linee.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Proprietà DataPointCount SysMon
- Proprietà DataPointCount SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, proprietà DataPointCount
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
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963991"
---
# <a name="systemmonitordatapointcount-property"></a>Proprietà SystemMonitor. DataPointCount

Recupera o imposta il numero di punti dati visualizzati in un grafico a linee.

## <a name="syntax"></a>Sintassi


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>Valore proprietà

Numero di punti dati visualizzati nella visualizzazione per un grafico a linee. Il valore predefinito è 100 punti dati. L'intervallo valido di valori è compreso tra 2 e 1.000.

## <a name="remarks"></a>Commenti

Questa proprietà viene utilizzata solo se [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è **sysmonCurrentActivity**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





