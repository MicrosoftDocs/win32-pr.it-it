---
title: IdleSettings.RestartOnIdle - proprietà
description: Per la creazione di script, ottiene o imposta un valore booleano che indica se l'attività viene riavviata quando il computer scorre più volte in una condizione di inattività.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- Proprietà RestartOnIdle Utilità di pianificazione
- Proprietà RestartOnIdle Utilità di pianificazione , oggetto IdleSettings
- Oggetto IdleSettings Utilità di pianificazione proprietà , RestartOnIdle
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa405ce4090a080106ec030acbe0ca7211b1c6f94e5874729226ce6adfafa652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760078"
---
# <a name="idlesettingsrestartonidle-property"></a>IdleSettings.RestartOnIdle - proprietà

Per la creazione di script, ottiene o imposta un valore booleano che indica se l'attività viene riavviata quando il computer scorre più volte in una condizione di inattività.

## <a name="syntax"></a>Sintassi


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a>Valore proprietà

Valore booleano che indica se l'attività deve essere riavviata quando il computer va in una condizione di inattività più volte. Il valore predefinito è False.

## <a name="remarks"></a>Commenti

Questa proprietà viene usata solo se la [**proprietà IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md) è impostata su True.

Quando si legge o si scrive codice XML per un'attività, questa impostazione viene specificata nell'elemento [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) dello schema Utilità di pianificazione dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





