---
title: Evento SystemMonitor. OnCounterDeleted
description: Notifica all'utente prima dell'eliminazione di un contatore dalla raccolta dei contatori.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- Evento OnCounterDeleted SysMon
- Evento OnCounterDeleted SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, evento OnCounterDeleted
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
ms.openlocfilehash: ceafcc73f38e5413e312d00bf8aa8eba4eaf2c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964273"
---
# <a name="systemmonitoroncounterdeleted-event"></a>Evento SystemMonitor. OnCounterDeleted

Notifica all'utente prima dell'eliminazione di un contatore dalla raccolta dei [**contatori**](counters.md) .

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

Indice del contatore da eliminare dall'oggetto raccolta dei [**contatori**](counters.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor. OnCounterAdded**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**SystemMonitor. OnCounterSelected**](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





