---
title: Evento SystemMonitor. OnCounterSelected
description: Notifica all'utente la selezione di un contatore.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- Evento OnCounterSelected SysMon
- Evento OnCounterSelected SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, evento OnCounterSelected
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0174ab2f896a27e44df592ec28b7cb12a03198f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301697"
---
# <a name="systemmonitoroncounterselected-event"></a>Evento SystemMonitor. OnCounterSelected

Notifica all'utente la selezione di un contatore.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

Indice del contatore selezionato nell'oggetto raccolta dei [**contatori**](counters.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

È possibile ricevere questo evento quando

-   Impostare [**CounterItem. Selected**](counteritem-selected.md) su true
-   L'utente seleziona un contatore nella legenda
-   L'utente fa doppio clic su un contatore nella legenda

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

[**SystemMonitor. OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





