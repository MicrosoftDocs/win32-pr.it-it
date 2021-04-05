---
title: Azioni attività
description: Gli elementi di lavoro eseguiti da un'attività vengono chiamati azioni. Un'attività può avere una sola azione o un massimo di 32 azioni. Tenere presente che, quando si specificano più azioni, vengono eseguite in modo sequenziale.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- azioni Utilità di pianificazione
- azioni Utilità di pianificazione, descritte
- azioni Utilità di pianificazione, Esegui azione
- azioni Utilità di pianificazione, azione gestore COM
- Esegui azione Utilità di pianificazione
- Utilità di pianificazione azione gestore COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71003e2cea5febfab61617451f3b6ebef4a244a3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "103722057"
---
# <a name="task-actions"></a>Azioni attività

Gli elementi di lavoro eseguiti da un'attività vengono chiamati azioni. Un'attività può avere una sola azione o un massimo di 32 azioni. Tenere presente che, quando si specificano più azioni, vengono eseguite in modo sequenziale.

## <a name="types-of-actions"></a>Tipi di azioni

Nella seguente tabella di azioni viene descritto il tipo di lavoro o le azioni che possono essere eseguite da un'attività.

| Tipo di azione      | Descrizione                                                             |
|---------------------|-------------------------------------------------------------------------|
| Azione del comgestore   | Questa azione attiva un gestore COM.                                        |
| Azione exec         | Questa azione esegue un'operazione della riga di comando, ad esempio l'avvio del blocco note. |
| Azione di posta elettronica       | Questa azione Invia un messaggio di posta elettronica quando viene attivata un'attività.                    |
| Mostra azione messaggio | Questa azione Visualizza una finestra di messaggio con un messaggio e un titolo specificati.     |



 

## <a name="specifying-actions"></a>Specifica di azioni

Le azioni di un'attività vengono specificate quando l'attività viene definita e archiviata in una raccolta di azioni usate dal servizio Utilità di pianificazione. La tabella seguente elenca i collegamenti agli argomenti di riferimento per le API e gli elementi XML associati alle azioni.

Per ulteriori informazioni ed esempi su come utilizzare le interfacce Utilità di pianificazione, gli oggetti di script e il codice XML, vedere [utilizzo del utilità di pianificazione](using-the-task-scheduler.md).

### <a name="interface-apis-for-c-development"></a>API di interfaccia per lo sviluppo in C++



| API                                                                    | Descrizione                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Proprietà Actions di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | Ottiene o imposta le azioni eseguite dall'attività.              |
| [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | Contiene le azioni eseguite dall'attività.                  |
| [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | Rappresenta un'azione che attiva un gestore.                   |
| [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | Rappresenta un'azione che esegue un'operazione della riga di comando. |
| [**IEmailAction**](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | Rappresenta un'azione che invia un messaggio di posta elettronica.            |
| [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | Rappresenta un'azione che visualizza una finestra di messaggio.               |



 

### <a name="scripting-object-apis-for-scripting-development"></a>API di oggetti di scripting per lo sviluppo di script



| API                                                      | Descrizione                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**TaskDefinition. Actions**](taskdefinition-actions.md) | Ottiene o imposta le azioni eseguite dall'attività.              |
| [**ActionCollection**](actioncollection.md)             | Contiene le azioni eseguite dall'attività.                  |
| [**ComHandlerAction**](comhandleraction.md)             | Rappresenta un'azione che attiva un gestore.                   |
| [**ExecAction**](execaction.md)                         | Rappresenta un'azione che esegue un'operazione della riga di comando. |
| [**EmailAction**](emailaction.md)                       | Rappresenta un'azione che invia un messaggio di posta elettronica.            |
| [**ShowMessageAction**](showmessageaction.md)           | Rappresenta un'azione che visualizza una finestra di messaggio.               |



 

### <a name="xml-elements"></a>Elementi XML



| Elemento                                                                    | Descrizione                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Azioni**](taskschedulerschema-actions-tasktype-element.md)            | Definisce le azioni eseguite dall'attività.                   |
| [**Comgestore**](taskschedulerschema-comhandler-actiongroup-element.md)   | Rappresenta un'azione che attiva un gestore.                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | Rappresenta un'azione che esegue un'operazione della riga di comando. |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | Rappresenta un'azione che invia un messaggio di posta elettronica.            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | Rappresenta un'azione che visualizza una finestra di messaggio.               |



 

## <a name="using-variables-in-action-properties"></a>Utilizzo di variabili nelle proprietà dell'azione

Alcune proprietà di azione di tipo **BSTR** possono contenere variabili $ (Arg0), $ (arg1),..., $ (Arg32) nei relativi valori di stringa. Queste variabili vengono sostituite con i valori specificati nel parametro *params* dei metodi [**IRegisteredTask:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) e [**IRegisteredTask:: RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) oppure sono contenuti nel trigger di evento per l'attività. Nella tabella seguente sono elencate le proprietà dell'azione che possono usare variabili nei valori stringa.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Azione</th>
<th>Proprietà</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Azione gestore COM</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>Proprietà ClassID di IComHandlerAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Proprietà Data di IComHandlerAction</strong></a></li>
</ul>
<br/> Scripting:
<ul>
<li><a href="comhandleraction-classid.md"><strong>ComHandlerAction. ClassID</strong></a></li>
<li><a href="comhandleraction-data.md"><strong>ComHandlerAction. Data</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Azione di posta elettronica</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Proprietà Body di IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Proprietà server di IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Proprietà Subject di IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>Alla proprietà di IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Proprietà CC di IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Proprietà Ccn di IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>Proprietà ReplyTo di IEmailAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>Proprietà from di IEmailAction</strong></a></li>
</ul>
<br/> Scripting:
<ul>
<li><a href="emailaction-body.md"><strong>EmailAction. Body</strong></a></li>
<li><a href="emailaction-server.md"><strong>EmailAction. Server</strong></a></li>
<li><a href="emailaction-subject.md"><strong>EmailAction. Subject</strong></a></li>
<li><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></li>
<li><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></li>
<li><a href="emailaction-bcc.md"><strong>EmailAction. Ccn</strong></a></li>
<li><a href="emailaction-replyto.md"><strong>EmailAction. ReplyTo</strong></a></li>
<li><a href="emailaction-from.md"><strong>EmailAction. from</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Azione exec</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Proprietà Arguments di IExecAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>Proprietà WorkingDirectory di IExecAction</strong></a></li>
</ul>
<br/> Scripting:
<ul>
<li><a href="execaction-arguments.md"><strong>ExecAction. Arguments</strong></a></li>
<li><a href="execaction-workingdirectory.md"><strong>ExecAction. WorkingDirectory</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Mostra azione messaggio</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Proprietà title di IShowMessageAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>Proprietà MessageBody di IShowMessageAction</strong></a></li>
</ul>
<br/> Scripting:
<ul>
<li><a href="showmessageaction-title.md"><strong>ShowMessageAction. title</strong></a></li>
<li><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction. MessageBody</strong></a></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md)
</dt> </dl>

 

 





