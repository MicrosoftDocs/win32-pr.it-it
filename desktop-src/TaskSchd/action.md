---
title: Oggetto Action
description: Oggetto di scripting che fornisce le proprietà comuni ereditate da tutti gli oggetti azione.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Oggetto Action Utilità di pianificazione
- Oggetto azione Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b9f41521f1af8b4601faafce9674277b172ad4cde3f364fc2ab7a84cfcc0df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739041"
---
# <a name="action-object"></a>Oggetto Action

Oggetto di scripting che fornisce le proprietà comuni ereditate da tutti gli oggetti azione. Un oggetto azione viene creato dal [**metodo ActionCollection.Create.**](actioncollection-create.md)

## <a name="members"></a>Membri

**L'oggetto** Action ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto Action** ha queste proprietà.



| Proprietà                               | Tipo di accesso           | Descrizione                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [**Id**](action-id.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore dell'azione.<br/> |
| [**Tipo**](action-type.md)<br/> | Sola lettura<br/>  | Ottiene il tipo dell'azione.<br/>               |



 

## <a name="remarks"></a>Commenti

Per informazioni sul funzionamento di azioni e attività, vedere [Azioni attività.](task-actions.md) La tabella seguente contiene gli oggetti di scripting che rappresentano le azioni che possono essere eseguite:



| API                                            | Descrizione                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**ComHandlerAction**](comhandleraction.md)   | Rappresenta un'azione che genera un gestore.                   |
| [**ExecAction**](execaction.md)               | Rappresenta un'azione che esegue un'operazione della riga di comando. |
| [**EmailAction**](emailaction.md)             | Rappresenta un'azione che invia un messaggio di posta elettronica.            |
| [**ShowMessageAction**](showmessageaction.md) | Rappresenta un'azione che mostra una finestra di messaggio.               |



 

Durante la lettura o la scrittura di codice XML, le azioni di un'attività vengono specificate [**nell'elemento Actions**](taskschedulerschema-actions-tasktype-element.md) dello schema Utilità di pianificazione dati.

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere Time [Trigger Example (Scripting) (Esempio](time-trigger-example--scripting-.md) di trigger di tempo (scripting), Event [Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))(Esempio di trigger di evento (scripting), [Daily Trigger Example (Scripting) (Esempio](daily-trigger-example--scripting-.md)di trigger giornaliero (scripting), Registration [Trigger Example (Scripting) (Esempio](registration-trigger-example--scripting-.md)di trigger di registrazione -Scripting), [Weekly Trigger Example (Scripting) (Esempio](weekly-trigger-example--scripting-.md)di trigger settimanale -Scripting), [Logon Trigger Example (Scripting) (Esempio](logon-trigger-example--scripting-.md)di trigger di accesso (scripting) ) o Boot [Trigger Example (Scripting) (Esempio](boot-trigger-example--scripting-.md)di trigger di avvio (scripting) ).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione Scripting Objects](task-scheduler-objects.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





