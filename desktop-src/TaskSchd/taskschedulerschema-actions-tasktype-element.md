---
title: Elemento Actions (taskType)
description: Contiene le azioni eseguite dall'attività.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Elemento Actions (taskType) Utilità di pianificazione
- azioni Utilità di pianificazione , XML
- Elementi Actions Utilità di pianificazione
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79fb5fe36b6fcff3622e0d12f0571e7f06c5f00d1ae930abc2bca805315f7dd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357099"
---
# <a name="actions-tasktype-element"></a>Elemento Actions (taskType)

Contiene le azioni eseguite dall'attività.

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

**L'elemento** Actions è definito dal [**tipo complesso taskType.**](taskschedulerschema-tasktype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                          | Derivato da                                                 | Descrizione                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Attività**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Descrive l'attività eseguita dal servizio Utilità di pianificazione.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                    | Tipo                                                                       | Descrizione                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)   | Specifica un'azione che genera un gestore.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**execType**](taskschedulerschema-exectype-complextype.md)               | Specifica un'azione che esegue un'operazione della riga di comando.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | Specifica un'azione che invia un messaggio di posta elettronica.<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Specifica un'azione che mostra una finestra di messaggio.<br/>               |



## <a name="attributes"></a>Attributi



| Nome    | Tipo | Descrizione                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| Context |      | Identificatore dell'entità dell'utente che rappresenta il contesto di sicurezza per le azioni dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Gli elementi figlio elencati in precedenza (massimo 32) sono definiti dal [**gruppo actionGroup.**](taskschedulerschema-actiongroup-group.md) Questi elementi possono essere aggiunti in qualsiasi ordine.

Per lo sviluppo C++, le azioni di un'attività sono definite [**nell'interfaccia IActionCollection.**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)

Per lo sviluppo di script, le azioni di un'attività vengono definite [**nell'oggetto ActionCollection.**](actioncollection.md)

## <a name="examples"></a>Esempio

Per altre informazioni e un esempio completo del codice XML per un'attività che contiene una singola azione di esecuzione, vedere [Time Trigger Example (XML) .](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**taskType**](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[**Actiongroup**](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





