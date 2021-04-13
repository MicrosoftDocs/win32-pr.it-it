---
title: Proprietà SystemMonitor. MonitorDuplicateInstances
description: Recupera o imposta un valore che determina se è possibile monitorare più istanze di un contatore.
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- Proprietà MonitorDuplicateInstances SysMon
- Proprietà MonitorDuplicateInstances SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà MonitorDuplicateInstances
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6ae53d0a1dcf3f67a43dab7959bb42619ace6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400522"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a>Proprietà SystemMonitor. MonitorDuplicateInstances

Recupera o imposta un valore che determina se è possibile monitorare più istanze di un contatore.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a>Valore proprietà

True indica che è possibile monitorare più istanze di un contatore (il valore predefinito è true). False indica che è possibile monitorare solo un'istanza di un contatore.

## <a name="remarks"></a>Commenti

Il monitoraggio di sistema aggiunge \# n a ogni nome di istanza, eccetto il primo, se esistono più istanze. Il numero di serie, n, inizia con uno e viene incrementato di uno per ogni nuova istanza. Se ad esempio si specifica " \\ Process ( \* ) \\ % Processor Time", l'insieme di contatori deve contenere più istanze di svchost. La prima occorrenza sarà svchost, l'occorrenza successiva sarà svchost \# 1 e così via.

Le istanze duplicate vengono monitorate solo se si usa il carattere jolly ( \* ) per il nome dell'istanza. Se è stato specificato " \\ Process (SVCHOST) \\ % Processor Time", viene monitorata solo la prima istanza trovata di svchost, non tutte le istanze di svchost.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





