---
title: Oggetto azione
description: Oggetto di scripting che fornisce le proprietà comuni ereditate da tutti gli oggetti azione.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Utilità di pianificazione oggetto azione
- Utilità di pianificazione oggetto azione, descritto
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
ms.openlocfilehash: 236b26cc4cfcd10f1e6e6094e4b69928343a9ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518238"
---
# <a name="action-object"></a>Oggetto azione

Oggetto di scripting che fornisce le proprietà comuni ereditate da tutti gli oggetti azione. Un oggetto azione viene creato dal metodo [**ActionCollection. Create**](actioncollection-create.md) .

## <a name="members"></a>Membri

L'oggetto **azione** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **azione** dispone di queste proprietà.



| Proprietà                               | Tipo di accesso           | Descrizione                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [**ID**](action-id.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore dell'azione.<br/> |
| [**Tipo**](action-type.md)<br/> | Sola lettura<br/>  | Ottiene il tipo dell'azione.<br/>               |



 

## <a name="remarks"></a>Commenti

Per informazioni sul funzionamento combinato di azioni e attività, vedere [azioni attività](task-actions.md). Nella tabella seguente sono inclusi gli oggetti di scripting che rappresentano le azioni che è possibile eseguire:



| API                                            | Descrizione                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**ComHandlerAction**](comhandleraction.md)   | Rappresenta un'azione che attiva un gestore.                   |
| [**ExecAction**](execaction.md)               | Rappresenta un'azione che esegue un'operazione della riga di comando. |
| [**EmailAction**](emailaction.md)             | Rappresenta un'azione che invia un messaggio di posta elettronica.            |
| [**ShowMessageAction**](showmessageaction.md) | Rappresenta un'azione che visualizza una finestra di messaggio.               |



 

Durante la lettura o la scrittura di codice XML, le azioni di un'attività vengono specificate nell'elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) dello schema utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere esempio di [trigger di ora (script)](time-trigger-example--scripting-.md) , esempio di [trigger di evento (](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))scripting), [esempio di trigger giornaliero (scripting)](daily-trigger-example--scripting-.md), [esempio di trigger di registrazione (scripting)](registration-trigger-example--scripting-.md), [esempio di trigger settimanale (scripting)](weekly-trigger-example--scripting-.md), esempio di trigger [Logon (](logon-trigger-example--scripting-.md)scripting) o [esempio di trigger di avvio (script](boot-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti di scripting Utilità di pianificazione](task-scheduler-objects.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





