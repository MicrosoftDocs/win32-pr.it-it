---
description: 'Chiamare il metodo IAzClientContext:: AccessCheck per verificare se il client ha accesso a una o più operazioni.'
ms.assetid: cf1070fe-3737-4ae6-a8ef-f0782418a1d5
title: Verifica dell'accesso client alle risorse richieste nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6d5c3940e38d8a9a8befa00b85ac9c3cd406c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314169"
---
# <a name="verifying-client-access-to-requested-resources-in-script"></a><span data-ttu-id="1c93f-103">Verifica dell'accesso client alle risorse richieste nello script</span><span class="sxs-lookup"><span data-stu-id="1c93f-103">Verifying Client Access to Requested Resources in Script</span></span>

<span data-ttu-id="1c93f-104">Chiamare il metodo [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) di un oggetto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) per verificare se il client ha accesso a una o più operazioni.</span><span class="sxs-lookup"><span data-stu-id="1c93f-104">Call the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object to check whether the client has access to one or more operations.</span></span> <span data-ttu-id="1c93f-105">Per informazioni sulla creazione di un oggetto **IAzClientContext** , vedere [definizione di un contesto client nello script](establishing-a-client-context-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="1c93f-105">For information about creating an **IAzClientContext** object, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="1c93f-106">Un client potrebbe appartenere a più di un ruolo e un'operazione potrebbe essere assegnata a più di un'attività, in modo che Gestione autorizzazioni verifichi tutti i ruoli e le attività.</span><span class="sxs-lookup"><span data-stu-id="1c93f-106">A client might have membership in more than one role, and an operation might be assigned to more than one task, so Authorization Manager checks for all roles and tasks.</span></span> <span data-ttu-id="1c93f-107">Se un ruolo a cui appartiene il client contiene un'attività che contiene un'operazione, viene concesso l'accesso a tale operazione.</span><span class="sxs-lookup"><span data-stu-id="1c93f-107">If any role to which the client belongs contains any task that contains an operation, access to that operation is granted.</span></span>

<span data-ttu-id="1c93f-108">Per controllare l'accesso solo a un singolo ruolo a cui appartiene il client, impostare la proprietà [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) dell'oggetto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="1c93f-108">To check access for only a single role to which the client belongs, set the [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) property of the [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span>

<span data-ttu-id="1c93f-109">Quando si inizializza l'archivio dei criteri di autorizzazione per il controllo dell'accesso, è necessario passare zero come valore del parametro *è* del metodo [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) dell'oggetto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="1c93f-109">When initializing the authorization policy store for access check, you must pass zero as the value of the *lFlags* parameter of the [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span>

<span data-ttu-id="1c93f-110">È anche possibile applicare la logica di business in fase di esecuzione per qualificare l'accesso.</span><span class="sxs-lookup"><span data-stu-id="1c93f-110">It is also possible to apply business logic at run time to qualify access.</span></span> <span data-ttu-id="1c93f-111">Per informazioni sull'accesso idoneo con la logica di business, vedere la pagina relativa [all'accesso idoneo con la logica di business nello script](qualifying-access-with-business-logic-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="1c93f-111">For information about qualifying access with business logic, see [Qualifying Access with Business Logic in Script](qualifying-access-with-business-logic-in-script.md).</span></span>

<span data-ttu-id="1c93f-112">Nell'esempio seguente viene illustrato come controllare l'accesso di un client a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="1c93f-112">The following example shows how to check a client's access to an operation.</span></span> <span data-ttu-id="1c93f-113">Nell'esempio si presuppone l'esistenza di un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C e che l'archivio contenga un'applicazione denominata Expense e un'operazione denominata UseFormControl.</span><span class="sxs-lookup"><span data-stu-id="1c93f-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense and an operation named UseFormControl.</span></span>


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

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Check access.
Dim Operations(1)
Operations(0) = operationID
Dim Results

Results = _
    clientContext.AccessCheck("UseFormControl", Empty, Operations)

%>
```



 

 



