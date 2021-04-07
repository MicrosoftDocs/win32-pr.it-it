---
title: Proprietà SystemMonitor. LogViewStop
description: Recupera o imposta la data di fine utilizzata per recuperare i valori dei contatori dai file di log.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Proprietà LogViewStop SysMon
- Proprietà LogViewStop SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, proprietà LogViewStop
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
ms.openlocfilehash: 4b725ee2efba22453d44f1e15fb9ce231b07cdb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964180"
---
# <a name="systemmonitorlogviewstop-property"></a>Proprietà SystemMonitor. LogViewStop

Recupera o imposta la data di fine utilizzata per recuperare i valori dei contatori dai file di log.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a>Valore proprietà

Data di fine utilizzata per recuperare i valori dei contatori dai file di log.

## <a name="remarks"></a>Commenti

SYSMON recupera i valori dei contatori dai file di log che rientrano in [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) e le date di arresto, inclusi.

Se non si specifica un valore di interruzione o si imposta questa proprietà su un valore di data successivo all'ultima data contenuta nel file di log, SYSMON modifica il valore con il valore di data più recente trovato nei file di log.

Se questa proprietà è impostata su un valore di data minore di [**LogViewStart**](systemmonitor-logviewstart.md), Sysmon modifica il valore nel valore di **LogViewStart**.

Prima di impostare la data di arresto, è necessario impostare la data di inizio. in caso contrario, entrambi i valori vengono impostati su date. MinValue e se si impostano le date dopo l'impostazione di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md), solo il primo valore del contatore viene recuperato dal file di log.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> <dt>

[**SystemMonitor. LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor. SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





