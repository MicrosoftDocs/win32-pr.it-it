---
title: Azioni attività
description: Gli elementi di lavoro eseguiti da un'attività sono detti azioni. Un'attività può avere una singola azione o un massimo di 32 azioni. Tenere presente che quando vengono specificate più azioni, vengono eseguite in sequenza.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- azioni Utilità di pianificazione
- azioni Utilità di pianificazione , descritto
- azioni Utilità di pianificazione, eseguire azione
- azioni Utilità di pianificazione, azione del gestore COM
- Eseguire l'azione Utilità di pianificazione
- Azione del gestore COM Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a7cc4a0e3ecbd4d55e4731379287f2cf4fd660
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470496"
---
# <a name="task-actions"></a>Azioni attività

Gli elementi di lavoro eseguiti da un'attività sono detti azioni. Un'attività può avere una singola azione o un massimo di 32 azioni. Tenere presente che quando vengono specificate più azioni, vengono eseguite in sequenza.

## <a name="types-of-actions"></a>Tipi di azioni

La tabella di azioni seguente descrive il tipo di lavoro o azioni che possono essere eseguite da un'attività.

| Tipo di azione      | Descrizione                                                             |
|---------------------|-------------------------------------------------------------------------|
| Azione ComHandler   | Questa azione genera un gestore COM.                                        |
| Azione Exec         | Questa azione esegue un'operazione della riga di comando, ad esempio l'avvio Blocco note. |
| Azione tramite posta elettronica       | Questa azione invia un messaggio di posta elettronica quando viene attivata un'attività.                    |
| Mostra azione messaggio | Questa azione mostra una finestra di messaggio con un messaggio e un titolo specificati.     |



 

## <a name="specifying-actions"></a>Specifica delle azioni

Le azioni di un'attività vengono specificate quando l'attività viene definita e archiviata in una raccolta di azioni usate dal Utilità di pianificazione servizio. Nella tabella seguente sono elencati i collegamenti agli argomenti di riferimento per le API e gli elementi XML associati alle azioni.

Per altre informazioni ed esempi su come usare le interfacce Utilità di pianificazione, gli oggetti di scripting e XML, vedere [Using the Utilità di pianificazione](using-the-task-scheduler.md).

### <a name="interface-apis-for-c-development"></a>API di interfaccia per lo sviluppo C++



| API                                                                    | Descrizione                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Proprietà Actions di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | Ottiene o imposta le azioni eseguite dall'attività.              |
| [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | Contiene le azioni eseguite dall'attività.                  |
| [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | Rappresenta un'azione che genera un gestore.                   |
| [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | Rappresenta un'azione che esegue un'operazione della riga di comando. |
| [**IEmailAction**](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | Rappresenta un'azione che invia un messaggio di posta elettronica.            |
| [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | Rappresenta un'azione che mostra una finestra di messaggio.               |



 

### <a name="scripting-object-apis-for-scripting-development"></a>API degli oggetti di scripting per lo sviluppo di script



| API                                                      | Descrizione                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**TaskDefinition.Actions**](taskdefinition-actions.md) | Ottiene o imposta le azioni eseguite dall'attività.              |
| [**Actioncollection**](actioncollection.md)             | Contiene le azioni eseguite dall'attività.                  |
| [**ComHandlerAction**](comhandleraction.md)             | Rappresenta un'azione che genera un gestore.                   |
| [**ExecAction**](execaction.md)                         | Rappresenta un'azione che esegue un'operazione della riga di comando. |
| [**EmailAction**](emailaction.md)                       | Rappresenta un'azione che invia un messaggio di posta elettronica.            |
| [**ShowMessageAction**](showmessageaction.md)           | Rappresenta un'azione che mostra una finestra di messaggio.               |



 

### <a name="xml-elements"></a>Elementi XML



| Elemento                                                                    | Descrizione                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Azioni**](taskschedulerschema-actions-tasktype-element.md)            | Definisce le azioni eseguite dall'attività.                   |
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | Rappresenta un'azione che genera un gestore.                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | Rappresenta un'azione che esegue un'operazione della riga di comando. |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | Rappresenta un'azione che invia un messaggio di posta elettronica.            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | Rappresenta un'azione che mostra una finestra di messaggio.               |



 

## <a name="using-variables-in-action-properties"></a>Uso di variabili nelle proprietà delle azioni

Alcune proprietà dell'azione di tipo **BSTR** possono contenere variabili $(Arg0), $(Arg1), ..., $(Arg32) nei valori stringa. Queste variabili vengono sostituite con i valori specificati nel parametro *params* dei metodi [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) e [**IRegisteredTask::RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) o contenuti nel trigger di evento per l'attività. Nella tabella seguente sono elencate le proprietà dell'azione che possono usare le variabili nei relativi valori stringa.


| Azione | Proprietà | 
|--------|------------|
| Azione del gestore COM | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>Proprietà ClassId di IComHandlerAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Proprietà Data di IComHandlerAction</strong></a></li></ul><br /> Scripting:<ul><li><a href="comhandleraction-classid.md"><strong>ComHandlerAction.ClassId</strong></a></li><li><a href="comhandleraction-data.md"><strong>ComHandlerAction.Data</strong></a></li></ul><br /> | 
| Azione di posta elettronica | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Proprietà Body di IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Proprietà Server di IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Proprietà Subject di IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>Proprietà To di IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Proprietà Cc di IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Proprietà Bcc di IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>Proprietà ReplyTo di IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>Dalla proprietà di IEmailAction</strong></a></li></ul><br /> Scripting:<ul><li><a href="emailaction-body.md"><strong>EmailAction.Body</strong></a></li><li><a href="emailaction-server.md"><strong>EmailAction.Server</strong></a></li><li><a href="emailaction-subject.md"><strong>EmailAction.Subject</strong></a></li><li><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></li><li><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></li><li><a href="emailaction-bcc.md"><strong>EmailAction.Bcc</strong></a></li><li><a href="emailaction-replyto.md"><strong>EmailAction.ReplyTo</strong></a></li><li><a href="emailaction-from.md"><strong>EmailAction.From</strong></a></li></ul><br /> | 
| Azione Exec | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Proprietà Arguments di IExecAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>Proprietà WorkingDirectory di IExecAction</strong></a></li></ul><br /> Scripting:<ul><li><a href="execaction-arguments.md"><strong>ExecAction.Arguments</strong></a></li><li><a href="execaction-workingdirectory.md"><strong>ExecAction.WorkingDirectory</strong></a></li></ul><br /> | 
| Mostra azione messaggio | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Proprietà Title di IShowMessageAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>Proprietà MessageBody di IShowMessageAction</strong></a></li></ul><br /> Scripting:<ul><li><a href="showmessageaction-title.md"><strong>ShowMessageAction.Title</strong></a></li><li><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction.MessageBody</strong></a></li></ul><br /> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md)
</dt> </dl>

 

 





