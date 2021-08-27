---
title: SystemMonitor.LogViewStop - proprietà
description: Recupera o imposta la data di fine utilizzata per recuperare i valori dei contatori dai file di log.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Proprietà LogViewStop SysMon
- Proprietà LogViewStop SysMon , oggetto SystemMonitor
- Oggetto SystemMonitor SysMon , proprietà LogViewStop
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8c30305f99e0d9bf66dd0f00dccc7674073e0f7058bca4284411c9d24426b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882075"
---
# <a name="systemmonitorlogviewstop-property"></a>SystemMonitor.LogViewStop - proprietà

Recupera o imposta la data di fine utilizzata per recuperare i valori dei contatori dai file di log.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a>Valore proprietà

Data di fine utilizzata per recuperare i valori dei contatori dai file di log.

## <a name="remarks"></a>Commenti

SYSMON recupera i valori dei contatori dai file di log inclusi in [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) e le date di arresto, in modo inclusivo.

Se non si specifica un valore di arresto o si imposta questa proprietà su un valore di data successivo all'ultima data contenuta nel file di log, SYSMON modifica il valore sul valore di data più recente trovato nei file di log.

Se questa proprietà è impostata su un valore di data minore di [**LogViewStart,**](systemmonitor-logviewstart.md)SYSMON modifica il valore di nel valore **di LogViewStart**.

È necessario impostare la data di inizio prima di impostare la data di arresto. In caso contrario, entrambi i valori vengono impostati su Date.MinValue e se si impostano le date dopo l'impostazione di [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md), dal file di log viene recuperato solo il primo valore del contatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> <dt>

[**SystemMonitor.LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





