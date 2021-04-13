---
title: SystemMonitor. GetLogViewRange, metodo
description: Recupera la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Metodo GetLogViewRange SysMon
- Metodo GetLogViewRange SysMon, oggetto SystemMonitor
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
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517799"
---
# <a name="systemmonitorgetlogviewrange-method"></a>SystemMonitor. GetLogViewRange, metodo

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

*StartTime* \[ out\]
</dt> <dd>

Data di inizio utilizzata per recuperare i valori dei contatori dai file di log.

</dd> <dt>

*StopTime* \[ out\]
</dt> <dd>

Data di fine utilizzata per recuperare i valori dei contatori dai file di log.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

SYSMON recupera i valori dei contatori dai file di log che rientrano nelle date di inizio e di fine, inclusi.

L'utilizzo di questo metodo è analogo all'accesso alle proprietà [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) e [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





