---
title: Evento SystemMonitor. OnCounterAdded
description: Notifica all'utente l'aggiunta di un contatore alla raccolta dei contatori.
ms.assetid: f798443f-e2f1-4d25-b142-d88d6e4fe12c
keywords:
- Evento OnCounterAdded SysMon
- Evento OnCounterAdded SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, evento OnCounterAdded
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterAdded
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f150709114ae25da89b107c7de85e3c5eca2551f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301575"
---
# <a name="systemmonitoroncounteradded-event"></a>Evento SystemMonitor. OnCounterAdded

Notifica all'utente l'aggiunta di un contatore alla raccolta dei [**contatori**](counters.md) .

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.OnCounterAdded( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

Indice del contatore aggiunto all'oggetto raccolta dei [**contatori**](counters.md) .

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

[**SystemMonitor. OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
</dt> <dt>

[**SystemMonitor. OnCounterSelected**](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





