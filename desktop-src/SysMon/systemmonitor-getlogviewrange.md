---
title: Metodo SystemMonitor.GetLogViewRange
description: Recupera la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Metodo GetLogViewRange SysMon
- Metodo GetLogViewRange SysMon , oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, metodo GetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3233dd57327734669631fc57b31bfb85578621991f34c1b1c414a69697b82048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882427"
---
# <a name="systemmonitorgetlogviewrange-method"></a>Metodo SystemMonitor.GetLogViewRange

Recupera la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartTime* \[ Cambio\]
</dt> <dd>

Data di inizio utilizzata per recuperare i valori dei contatori dai file di log.

</dd> <dt>

*StopTime* \[ Cambio\]
</dt> <dd>

Data di fine utilizzata per recuperare i valori dei contatori dai file di log.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

SYSMON recupera i valori dei contatori dai file di log che rientrano nelle date di inizio e di arresto, in modo inclusivo.

L'uso di questo metodo è identico all'accesso [**alle proprietà SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) [**e SystemMonitor.LogViewStop.**](systemmonitor-logviewstop.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





