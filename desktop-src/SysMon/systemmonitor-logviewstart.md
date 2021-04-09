---
title: Proprietà SystemMonitor. LogViewStart
description: Recupera o imposta la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- Proprietà LogViewStart SysMon
- Proprietà LogViewStart SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà LogViewStart
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
ms.openlocfilehash: 967c44940b195c4d8ddd3028e1d4f307827bbbfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964088"
---
# <a name="systemmonitorlogviewstart-property"></a>Proprietà SystemMonitor. LogViewStart

Recupera o imposta la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a>Valore proprietà

Data di inizio utilizzata per recuperare i valori dei contatori dai file di log.

## <a name="remarks"></a>Commenti

SYSMON recupera i valori dei contatori dai file di log che rientrano tra le date Start e [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) , inclusi.

Se non si specifica una data di inizio o si imposta questa proprietà su un valore di data non compreso nell'intervallo dei valori di data presenti nei file di log, SYSMON modifica il valore in un valore di data meno recente trovato nei file di log.

Se questa proprietà è impostata su un valore di data maggiore di [**LogViewStop**](systemmonitor-logviewstop.md), Sysmon modifica il valore nel valore di **LogViewStop**.

Se si specifica una data di inizio e di fine, è necessario specificare le date prima di impostare [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md).

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

[**SystemMonitor. LogFiles**](systemmonitor-logfiles.md)
</dt> <dt>

[**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor. LogSourceStartTime**](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[**SystemMonitor. SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





