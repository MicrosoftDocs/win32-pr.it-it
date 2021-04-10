---
description: Per stabilire un contesto client nello script, un'applicazione può creare un contesto client con un handle per un token, un dominio e un nome utente o una rappresentazione di stringa dell'ID di sicurezza del client.
ms.assetid: 94fb79e4-7e9f-4fef-8ca5-b2000a92efab
title: Creazione di un contesto client nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 63c0381834a42d10a03b02ee949f8fe4bf7560bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883866"
---
# <a name="establishing-a-client-context-in-script"></a><span data-ttu-id="04fcf-103">Creazione di un contesto client nello script</span><span class="sxs-lookup"><span data-stu-id="04fcf-103">Establishing a Client Context in Script</span></span>

<span data-ttu-id="04fcf-104">In Gestione autorizzazioni, un'applicazione determina se a un client viene concesso l'accesso a un'operazione chiamando il metodo [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) di un oggetto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) , che rappresenta un contesto client.</span><span class="sxs-lookup"><span data-stu-id="04fcf-104">In Authorization Manager, an application determines whether a client is given access to an operation by calling the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object, which represents a client context.</span></span>

<span data-ttu-id="04fcf-105">Un'applicazione può creare un contesto client con un handle per un token, un dominio e un nome utente o una rappresentazione di stringa dell' [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) del client.</span><span class="sxs-lookup"><span data-stu-id="04fcf-105">An application can create a client context with a handle to a token, a domain and user name, or a string representation of the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the client.</span></span>

<span data-ttu-id="04fcf-106">Usare i metodi [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)e [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) di un oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) per creare un contesto client.</span><span class="sxs-lookup"><span data-stu-id="04fcf-106">Use the [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname), and [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) methods of an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object to create a client context.</span></span>

<span data-ttu-id="04fcf-107">Nell'esempio seguente viene illustrato come creare un oggetto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) da un nome client.</span><span class="sxs-lookup"><span data-stu-id="04fcf-107">The following example shows how to create an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object from a client name.</span></span> <span data-ttu-id="04fcf-108">Nell'esempio si presuppone l'esistenza di un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C e che l'archivio contenga un'applicazione denominata Expense.</span><span class="sxs-lookup"><span data-stu-id="04fcf-108">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense.</span></span>


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



 

 
