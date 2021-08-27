---
description: Per stabilire un contesto client in Script, un'applicazione può creare un contesto client con un handle per un token, un dominio e un nome utente o una rappresentazione di stringa dell'identificatore di sicurezza del client.
ms.assetid: 94fb79e4-7e9f-4fef-8ca5-b2000a92efab
title: Definizione di un contesto client nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05a8ea51efa427c83e78c35806175712b3c6d0d66e0987909f98e23a081415e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913737"
---
# <a name="establishing-a-client-context-in-script"></a>Definizione di un contesto client nello script

In Gestione autorizzazioni un'applicazione determina se a un client viene assegnato l'accesso a un'operazione chiamando il metodo [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) di un [**oggetto IAzClientContext,**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) che rappresenta un contesto client.

Un'applicazione può creare un contesto client con un handle per un token, un dominio e un nome utente o una rappresentazione di stringa dell'identificatore [*di*](/windows/desktop/SecGloss/s-gly) sicurezza (SID) del client.

Usare i [**metodi InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)e [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) di un [**oggetto IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) per creare un contesto client.

L'esempio seguente illustra come creare un [**oggetto IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) da un nome client. Nell'esempio si presuppone che sia presente un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C e che questo archivio contenga un'applicazione denominata Expense.


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

%>
```



 

 
