---
title: Evento SystemMonitor.OnCounterDeleted
description: Notifica all'utente prima che un contatore venga eliminato dalla raccolta Counters.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- SysMon dell'evento OnCounterDeleted
- Evento OnCounterDeleted SysMon , classe SystemMonitor
- Classe SystemMonitor SysMon , evento OnCounterDeleted
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44c178cb0b9c19fde0814f15729ffd49a0a0dbea65023bde06673cd843aeb668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884003"
---
# <a name="systemmonitoroncounterdeleted-event"></a>Evento SystemMonitor.OnCounterDeleted

Notifica all'utente prima che un contatore venga eliminato dalla [**raccolta Counters.**](counters.md)

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

Indice del contatore da eliminare [**dall'oggetto raccolta Counters.**](counters.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor.OnCounterAdded**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**SystemMonitor.OnCounterSelected**](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





