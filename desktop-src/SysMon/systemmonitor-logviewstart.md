---
title: SystemMonitor.LogViewStart - proprietà
description: Recupera o imposta la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- Proprietà LogViewStart SysMon
- Proprietà LogViewStart SysMon , classe SystemMonitor
- Classe SystemMonitor SysMon , proprietà LogViewStart
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc1c7c4a46ac746582d62ee7ce08980b078eb8d972cb6b4d3ed787b49f2285f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955404"
---
# <a name="systemmonitorlogviewstart-property"></a>SystemMonitor.LogViewStart - proprietà

Recupera o imposta la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a>Valore proprietà

Data di inizio utilizzata per recuperare i valori dei contatori dai file di log.

## <a name="remarks"></a>Commenti

SYSMON recupera i valori dei contatori dai file di log che rientrano nelle date start e [**SystemMonitor.LogViewStop,**](systemmonitor-logviewstop.md) in modo inclusivo.

Se non si specifica una data di inizio o se si imposta questa proprietà su un valore di data non compreso nell'intervallo di valori di data presenti nei file di log, SYSMON modifica il valore sul valore di data meno recente trovato nei file di log.

Se questa proprietà è impostata su un valore di data maggiore di [**LogViewStop**](systemmonitor-logviewstop.md), SYSMON modifica il valore di nel valore di **LogViewStop**.

Se si specifica una data di inizio e di arresto, è necessario specificare le date prima di [**impostare SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).

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

[**SystemMonitor.LogFiles**](systemmonitor-logfiles.md)
</dt> <dt>

[**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor.LogSourceStartTime**](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





