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
# <a name="qualifying-access-with-business-logic-in-script"></a><span data-ttu-id="42dbe-103">Qualificazione dell'accesso con la logica di business nello script</span><span class="sxs-lookup"><span data-stu-id="42dbe-103">Qualifying Access with Business Logic in Script</span></span>

<span data-ttu-id="42dbe-104">Usare gli script delle regole business per fornire la logica di run-time per il controllo dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="42dbe-104">Use business rule scripts to provide run-time logic for checking access.</span></span> <span data-ttu-id="42dbe-105">Per ulteriori informazioni sulle regole business, vedere [regole business](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="42dbe-105">For more information about business rules, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="42dbe-106">Per assegnare una regola business a un'attività, impostare innanzitutto la proprietà [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) dell'oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) che rappresenta l'attività.</span><span class="sxs-lookup"><span data-stu-id="42dbe-106">To assign a business rule to a task, first set the [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) property of the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents the task.</span></span> <span data-ttu-id="42dbe-107">Lo script deve essere scritto utilizzando il linguaggio di programmazione di Visual Basic Scripting Edition (VBScript) o il software di sviluppo JScript.</span><span class="sxs-lookup"><span data-stu-id="42dbe-107">The script must be written using the Visual Basic Scripting Edition (VBScript) programming language or JScript development software.</span></span> <span data-ttu-id="42dbe-108">Dopo aver specificato il linguaggio di script, impostare la proprietà [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) dell'oggetto **IAzTask** con una rappresentazione di stringa dello script.</span><span class="sxs-lookup"><span data-stu-id="42dbe-108">After you specify the script language, set the [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) property of the **IAzTask** object with a string representation of the script.</span></span>

<span data-ttu-id="42dbe-109">Quando si verifica l'accesso per un'operazione contenuta da un'attività a cui è associata una regola business, l'applicazione deve creare due matrici con le stesse dimensioni da passare come parametri *varParameterNames* e *VarParameterValues* del metodo [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) di un oggetto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="42dbe-109">When checking access for an operation contained by a task that has an associated business rule, the application must create two arrays of the same size to be passed as the *varParameterNames* and *varParameterValues* parameters of the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span> <span data-ttu-id="42dbe-110">Per informazioni sulla creazione di un contesto client, vedere [definizione di un contesto client nello script](establishing-a-client-context-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="42dbe-110">For information about creating a client context, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="42dbe-111">Il metodo [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) crea un oggetto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) passato allo script della regola business.</span><span class="sxs-lookup"><span data-stu-id="42dbe-111">The [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method creates an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is passed to the business rule script.</span></span> <span data-ttu-id="42dbe-112">Lo script imposta quindi la proprietà [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) dell'oggetto **AzBizRuleContext** .</span><span class="sxs-lookup"><span data-stu-id="42dbe-112">The script then sets the [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) property of the **AzBizRuleContext** object.</span></span> <span data-ttu-id="42dbe-113">Il valore **true** indica che è stato concesso l'accesso e il valore **false** indica che l'accesso è stato negato.</span><span class="sxs-lookup"><span data-stu-id="42dbe-113">A value of **True** indicates that access is granted, and a value of **False** indicates that access is denied.</span></span>

<span data-ttu-id="42dbe-114">Non è possibile assegnare uno script della regola business a un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) contenuto in un oggetto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) delegato.</span><span class="sxs-lookup"><span data-stu-id="42dbe-114">A business rule script cannot be assigned to an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object contained by a delegated [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

<span data-ttu-id="42dbe-115">Nell'esempio seguente viene illustrato come utilizzare uno script della regola business per controllare l'accesso di un client a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="42dbe-115">The following example shows how to use a business rule script to check a client's access to an operation.</span></span> <span data-ttu-id="42dbe-116">Nell'esempio si presuppone che esista un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C e che l'archivio contenga un'applicazione denominata Expense, un'attività denominata Submit Expense e un'operazione denominata UseFormControl.</span><span class="sxs-lookup"><span data-stu-id="42dbe-116">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense, a task named Submit Expense, and an operation named UseFormControl.</span></span>


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



 

 



