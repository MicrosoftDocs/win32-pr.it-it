---
description: Chiamare il metodo IAzClientContext::AccessCheck per verificare se il client ha accesso a una o più operazioni.
ms.assetid: cf1070fe-3737-4ae6-a8ef-f0782418a1d5
title: Verifica dell'accesso client alle risorse richieste nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7393001c63f0a5b605870a8498e76231f0bf620a8c7e819a8c624eace565499a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906701"
---
# <a name="verifying-client-access-to-requested-resources-in-script"></a>Verifica dell'accesso client alle risorse richieste nello script

Chiamare il [**metodo AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) di un [**oggetto IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) per verificare se il client ha accesso a una o più operazioni. Per informazioni sulla creazione di **un oggetto IAzClientContext,** vedere [Definizione di un contesto client nello script.](establishing-a-client-context-in-script.md)

Un client potrebbe essere membro di più di un ruolo e un'operazione potrebbe essere assegnata a più di un'attività, quindi Gestione autorizzazioni controlla tutti i ruoli e le attività. Se un ruolo a cui appartiene il client contiene un'attività che contiene un'operazione, viene concesso l'accesso a tale operazione.

Per controllare l'accesso per un solo ruolo a cui appartiene il client, impostare la [**proprietà RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) [**dell'oggetto IAzClientContext.**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext)

Quando si inizializza l'archivio dei criteri di autorizzazione per il controllo di accesso, è necessario passare zero come valore del parametro *lFlags* del metodo [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) dell'oggetto [**AzAuthorizationStore.**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore)

È anche possibile applicare la logica di business in fase di esecuzione per qualificare l'accesso. Per informazioni sulla qualifica dell'accesso con la logica di business, vedere [Qualifying Access with Business Logic in Script](qualifying-access-with-business-logic-in-script.md).

Nell'esempio seguente viene illustrato come controllare l'accesso di un client a un'operazione. Nell'esempio si presuppone che sia presente un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C e che questo archivio contenga un'applicazione denominata Expense e un'operazione denominata UseFormControl.


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



 

 



