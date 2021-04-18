---
description: Utilizzo di script delle regole business nello script per fornire la logica di run-time per il controllo dell'accesso.
ms.assetid: 10c28ecb-3f36-45a8-b037-7038e8927b6b
title: Qualificazione dell'accesso con la logica di business nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 65ee69e0572c0f480cded2930ea81ac6da710b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308146"
---
# <a name="qualifying-access-with-business-logic-in-script"></a>Qualificazione dell'accesso con la logica di business nello script

Usare gli script delle regole business per fornire la logica di run-time per il controllo dell'accesso. Per ulteriori informazioni sulle regole business, vedere [regole business](business-rules.md).

Per assegnare una regola business a un'attività, impostare innanzitutto la proprietà [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) dell'oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) che rappresenta l'attività. Lo script deve essere scritto utilizzando il linguaggio di programmazione di Visual Basic Scripting Edition (VBScript) o il software di sviluppo JScript. Dopo aver specificato il linguaggio di script, impostare la proprietà [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) dell'oggetto **IAzTask** con una rappresentazione di stringa dello script.

Quando si verifica l'accesso per un'operazione contenuta da un'attività a cui è associata una regola business, l'applicazione deve creare due matrici con le stesse dimensioni da passare come parametri *varParameterNames* e *VarParameterValues* del metodo [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) di un oggetto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) . Per informazioni sulla creazione di un contesto client, vedere [definizione di un contesto client nello script](establishing-a-client-context-in-script.md).

Il metodo [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) crea un oggetto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) passato allo script della regola business. Lo script imposta quindi la proprietà [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) dell'oggetto **AzBizRuleContext** . Il valore **true** indica che è stato concesso l'accesso e il valore **false** indica che l'accesso è stato negato.

Non è possibile assegnare uno script della regola business a un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) contenuto in un oggetto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) delegato.

Nell'esempio seguente viene illustrato come utilizzare uno script della regola business per controllare l'accesso di un client a un'operazione. Nell'esempio si presuppone che esista un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C e che l'archivio contenga un'applicazione denominata Expense, un'attività denominata Submit Expense e un'operazione denominata UseFormControl.


```VB
<%@ Language=VBScript %>
<%
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 0, "msxml://C:\MyStore.xml"

'  Open the application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a client context.
Dim clientName
clientName = Request.ServerVariables("LOGON_USER")
Dim clientContext
Set clientContext = _
    expenseApp.InitializeClientContextFromName(clientName)

'  Create a business rule for the Submit Expense task.

'  Open the Submit Expense task.
Dim submitTask
Set submitTask = expenseApp.OpenTask("Submit Expense")

'  Set the business rule language to VBScript.
submitTask.BizRuleLanguage = "VBScript"

'  Create a string with the business rule code.
Dim newline
newline = chr(13)
Dim bizRuleString
bizRuleString = "Dim Amount" + newline _
         +"AzBizRuleContext.BusinessRuleResult = FALSE" + newline _
         +"Amount = AzBizRuleContext.GetParameter(""ExpAmount"")" _
   +newline _
   +"if Amount < 500 then AzBizRuleContext.BusinessRuleResult = TRUE"

'  Assign the business rule to the Submit Expense task.
submitTask.BizRule = bizRuleString
                
'  Save the task information to the store.
submitTask.Submit

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Set up arrays for operations and results.
Dim Operations(1)
Operations(0) = operationID
Dim Results

'  Set up business rule parameters.
Dim bizNames(1)
Dim bizValues(1)
bizNames(0) = "ExpAmount"
bizValues(0) = 100

'  Check access.
Results = clientContext.AccessCheck _
    ("UseFormControl", Empty, Operations, bizNames, bizValues)
 
%>
```



 

 



