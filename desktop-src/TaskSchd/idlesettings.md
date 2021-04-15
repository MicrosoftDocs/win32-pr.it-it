---
title: Oggetto IdleSettings
description: Oggetto di scripting che specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in una condizione di inattività.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Utilità di pianificazione oggetto IdleSettings
- Oggetto IdleSettings Utilità di pianificazione, descritto
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
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400478"
---
# <a name="idlesettings-object"></a>Oggetto IdleSettings

Oggetto di scripting che specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in una condizione di inattività. Per informazioni sulle condizioni di inattività, vedere [condizioni](task-idle-conditions.md)di inattività.

## <a name="members"></a>Membri

L'oggetto **IdleSettings** dispone di questi tipi di membri:

- [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **IdleSettings** dispone di queste proprietà.

> [!NOTE]
> Le impostazioni *IdleDuration* e *WaitTimeout* sono deprecate. Sono ancora presenti nel Utilità di pianificazione interfaccia utente e i relativi metodi di interfaccia possono comunque restituire valori validi, ma non vengono più usati.

| Proprietà                                                       | Tipo di accesso           | Descrizione                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](idlesettings-restartonidle.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica se l'attività viene riavviata quando il computer scorre in una condizione di inattività più di una volta.<br/>            |
| [**StopOnIdleEnd**](idlesettings-stoponidleend.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica che il Utilità di pianificazione terminerà l'attività se la condizione di inattività termina prima del completamento dell'attività.<br/> |
| **Deprecato**: [ **IdleDuration**](idlesettings-idleduration.md)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica la quantità di tempo in cui il computer deve essere in uno stato inattivo prima dell'esecuzione dell'attività.<br/>                            |
| **Deprecato**: [ **WaitTimeout**](idlesettings-waittimeout.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica l'intervallo di tempo durante il quale il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.<br/>                             |

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) dello schema utilità di pianificazione.

Se un'attività viene attivata da un trigger inattivo, la proprietà [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) viene ignorata.

> [!NOTE]
> *IdleSettings. IdleDuration* e *IdleSettings. WaitTimeout* sono deprecati.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[Oggetti Utilità di pianificazione](task-scheduler-objects.md)

[Utilità di pianificazione](task-scheduler-start-page.md)
