---
title: Oggetto IdleSettings
description: Oggetto di scripting che specifica il modo in Utilità di pianificazione le attività quando il computer si trova in una condizione di inattività.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Oggetti IdleSettings Utilità di pianificazione
- Oggetto IdleSettings Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7597f2232d95d6ddd5f8001be8cf88178ccf5dacd3694c2a8e179d371e54c898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659601"
---
# <a name="idlesettings-object"></a>Oggetto IdleSettings

Oggetto di scripting che specifica il modo in cui il Utilità di pianificazione esegue attività quando il computer si trova in una condizione di inattività. Per informazioni sulle condizioni di inattività, vedere [Condizioni di inattività delle attività](task-idle-conditions.md).

## <a name="members"></a>Membri

**L'oggetto IdleSettings** ha questi tipi di membri:

- [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto IdleSettings** ha queste proprietà.

> [!NOTE]
> Le *impostazioni IdleDuration* *e WaitTimeout* sono deprecate. Sono ancora presenti nell'interfaccia Utilità di pianificazione utente e i relativi metodi di interfaccia possono comunque restituire valori validi, ma non vengono più usati.

| Proprietà                                                       | Tipo di accesso           | Descrizione                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](idlesettings-restartonidle.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica se l'attività viene riavviata quando il computer scorre più volte in una condizione di inattività.<br/>            |
| [**StopOnIdleEnd**](idlesettings-stoponidleend.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che il Utilità di pianificazione terminerà l'attività se la condizione di inattività termina prima del completamento dell'attività.<br/> |
| **Deprecato:** [ **IdleDuration**](idlesettings-idleduration.md)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica la quantità di tempo in cui il computer deve essere inattivo prima dell'esecuzione dell'attività.<br/>                            |
| **Deprecato:** [ **WaitTimeout**](idlesettings-waittimeout.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica la quantità di tempo in cui il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.<br/>                             |

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML per un'attività, questa impostazione viene specificata nell'elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) dello schema Utilità di pianificazione dati.

Se un'attività viene attivata da un trigger inattivo, la proprietà [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) viene ignorata.

> [!NOTE]
> *IdleSettings.IdleDuration e* *IdleSettings.WaitTimeout* sono deprecati.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[Utilità di pianificazione oggetti](task-scheduler-objects.md)

[Utilità di pianificazione](task-scheduler-start-page.md)
