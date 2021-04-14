---
title: Oggetto TaskDefinition
description: Oggetto di scripting che definisce tutti i componenti di un'attività, ad esempio le impostazioni di attività, i trigger, le azioni e le informazioni di registrazione.
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- Utilità di pianificazione oggetto TaskDefinition
- Oggetto TaskDefinition Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518076"
---
# <a name="taskdefinition-object"></a>Oggetto TaskDefinition

Oggetto di scripting che definisce tutti i componenti di un'attività, ad esempio le impostazioni di attività, i trigger, le azioni e le informazioni di registrazione.

## <a name="members"></a>Membri

L'oggetto **TaskDefinition** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **TaskDefinition** dispone di queste proprietà.



| Proprietà                                                               | Tipo di accesso           | Descrizione                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Azioni**](taskdefinition-actions.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta una raccolta di azioni eseguite dall'attività.<br/>                                                                                                         |
| [**Data**](taskdefinition-data.md)<br/>                         | Lettura/Scrittura<br/> | Ottiene o imposta i dati associati all'attività. Questi dati vengono ignorati dal servizio Utilità di pianificazione, ma vengono utilizzati da terze parti che desiderano estendere il formato dell'attività.<br/> |
| [**Principale**](taskdefinition-principal.md)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta l'entità per l'attività che fornisce le credenziali di sicurezza per l'attività.<br/>                                                                                 |
| [**RegistrationInfo**](taskdefinition-registrationinfo.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta le informazioni di registrazione utilizzate per descrivere un'attività, ad esempio la descrizione dell'attività, l'autore dell'attività e la data di registrazione dell'attività.<br/> |
| [**Impostazioni**](taskdefinition-settings.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta le impostazioni che definiscono il modo in cui il servizio Utilità di pianificazione esegue l'attività.<br/>                                                                                      |
| [**Trigger**](taskdefinition-triggers.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta una raccolta di trigger utilizzati per avviare un'attività.<br/>                                                                                                         |
| [**XmlText**](taskdefinition-xmltext.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta la definizione in formato XML dell'attività.<br/>                                                                                                                       |



 

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificata una definizione di attività usando l'elemento [**Task**](taskschedulerschema-task-element.md) dello schema utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere esempio di [trigger di ora (script)](time-trigger-example--scripting-.md) , esempio di [trigger di evento (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))scripting), [esempio di trigger giornaliero (scripting)](daily-trigger-example--scripting-.md), [esempio di trigger di registrazione (scripting)](registration-trigger-example--scripting-.md), [esempio di trigger settimanale (scripting)](weekly-trigger-example--scripting-.md), esempio di trigger [Logon (](logon-trigger-example--scripting-.md)scripting) o [esempio di trigger di avvio (script](boot-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





