---
title: Actions (taskType)-elemento
description: Contiene le azioni eseguite dall'attività.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Actions (taskType)-elemento Utilità di pianificazione
- Utilità di pianificazione azioni, XML
- Elemento Actions Utilità di pianificazione
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21af0f8a06faa9cdc61917dcb3b3b0672c47e0e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400407"
---
# <a name="actions-tasktype-element"></a>Actions (taskType)-elemento

Contiene le azioni eseguite dall'attività.

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

L'elemento **Actions** viene definito dal tipo complesso [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                          | Derivato da                                                 | Descrizione                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Attività**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Descrive l'attività eseguita dal servizio Utilità di pianificazione.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                    | Tipo                                                                       | Descrizione                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Comgestore**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)   | Specifica un'azione che attiva un gestore.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**execType**](taskschedulerschema-exectype-complextype.md)               | Specifica un'azione che esegue un'operazione della riga di comando.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | Specifica un'azione che invia un messaggio di posta elettronica.<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Specifica un'azione che visualizza una finestra di messaggio.<br/>               |



## <a name="attributes"></a>Attributi



| Nome    | Tipo | Descrizione                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| Context |      | Identificatore principale dell'utente che rappresenta il contesto di sicurezza per le azioni dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Gli elementi figlio elencati in precedenza (massimo 32) sono definiti dal gruppo [**actionGroup**](taskschedulerschema-actiongroup-group.md) . Questi elementi possono essere aggiunti in qualsiasi ordine.

Per lo sviluppo in C++, le azioni di un'attività sono definite nell'interfaccia [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) .

Per lo sviluppo di script, le azioni di un'attività sono definite nell'oggetto [**ActionCollection**](actioncollection.md) .

## <a name="examples"></a>Esempio

Per ulteriori informazioni e un esempio completo del codice XML per un'attività che contiene una singola azione di esecuzione, vedere l'esempio relativo al [trigger temporale (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**taskType**](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[**actionGroup**](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





