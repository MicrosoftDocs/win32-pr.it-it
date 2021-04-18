---
title: Gestione delle conversazioni
description: In questo argomento vengono illustrate le conversazioni tra un client e un server.
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- Interfaccia utente di Windows, Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), conversazioni
- DDE (Dynamic Data Exchange), conversazioni
- scambio di dati, Dynamic Data Exchange (DDE)
- Interfaccia utente di Windows, libreria di gestione Dynamic Data Exchange (DDEML)
- Libreria di gestione Dynamic Data Exchange (DDEML), conversazioni
- DDEML (libreria di gestione Dynamic Data Exchange), conversazioni
- scambio di dati, libreria di gestione Dynamic Data Exchange (DDEML)
- Dynamic Data Exchange (DDE), più conversazioni
- DDE (Dynamic Data Exchange), più conversazioni
- Libreria di gestione Dynamic Data Exchange (DDEML), più conversazioni
- DDEML (libreria di gestione Dynamic Data Exchange), più conversazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca1a0a8e02bceb6b2f69051d89df289871fdd42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298925"
---
# <a name="conversation-management"></a><span data-ttu-id="1c7c0-115">Gestione delle conversazioni</span><span class="sxs-lookup"><span data-stu-id="1c7c0-115">Conversation Management</span></span>

<span data-ttu-id="1c7c0-116">Una conversazione tra un client e un server viene sempre stabilita in corrispondenza della richiesta del client.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-116">A conversation between a client and a server is always established at the request of the client.</span></span> <span data-ttu-id="1c7c0-117">Quando viene stabilita una conversazione, ogni partner riceve un handle che identifica la conversazione.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-117">When a conversation is established, each partner receives a handle that identifies the conversation.</span></span> <span data-ttu-id="1c7c0-118">I partner utilizzano questo handle in altre funzioni DDEML (Dynamic Data Exchange Management Library) per inviare le transazioni e gestire la conversazione.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-118">The partners use this handle in other Dynamic Data Exchange Management Library (DDEML) functions to send transactions and manage the conversation.</span></span> <span data-ttu-id="1c7c0-119">Un client può richiedere una conversazione con un solo server oppure può richiedere più conversazioni con uno o più server.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-119">A client can request a conversation with a single server, or it can request multiple conversations with one or more servers.</span></span>

<span data-ttu-id="1c7c0-120">Negli argomenti seguenti viene descritto il modo in cui un'applicazione stabilisce nuove conversazioni e ottiene informazioni sulle conversazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-120">The following topics describe how an application establishes new conversations and gets information about existing conversations.</span></span>

-   [<span data-ttu-id="1c7c0-121">Conversazioni singole</span><span class="sxs-lookup"><span data-stu-id="1c7c0-121">Single Conversations</span></span>](#single-conversations)
-   [<span data-ttu-id="1c7c0-122">Più conversazioni</span><span class="sxs-lookup"><span data-stu-id="1c7c0-122">Multiple Conversations</span></span>](#multiple-conversations)

## <a name="single-conversations"></a><span data-ttu-id="1c7c0-123">Conversazioni singole</span><span class="sxs-lookup"><span data-stu-id="1c7c0-123">Single Conversations</span></span>

<span data-ttu-id="1c7c0-124">Un'applicazione client richiede una singola conversazione con un server chiamando la funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e specificando handle di stringa che identificano le stringhe che contengono il nome del servizio dell'applicazione server e il nome dell'argomento per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-124">A client application requests a single conversation with a server by calling the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function and specifying string handles that identify the strings containing the service name of the server application and the topic name for the conversation.</span></span> <span data-ttu-id="1c7c0-125">DDEML risponde inviando la transazione di [**\_ connessione XTYP**](xtyp-connect.md) alla funzione di callback di Dynamic Data Exchange (DDE) di ogni applicazione server che ha registrato un nome di servizio che corrisponde a quello specificato in **DdeConnect** o ha disattivato il filtro del nome del servizio chiamando [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span><span class="sxs-lookup"><span data-stu-id="1c7c0-125">The DDEML responds by sending the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the Dynamic Data Exchange (DDE) callback function of each server application that either has registered a service name that matches the one specified in **DdeConnect** or has turned service name filtering off by calling [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span></span> <span data-ttu-id="1c7c0-126">Un server può anche filtrare le transazioni di **\_ connessione XTYP** specificando il \_ flag di filtro CBF Fail \_ Connections nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="1c7c0-126">A server can also filter **XTYP\_CONNECT** transactions by specifying the CBF\_FAIL\_CONNECTIONS filter flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="1c7c0-127">Durante la transazione di **\_ connessione XTYP** , il DDEML passa il nome del servizio e il nome dell'argomento al server.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-127">During the **XTYP\_CONNECT** transaction, the DDEML passes the service name and the topic name to the server.</span></span> <span data-ttu-id="1c7c0-128">Il server deve esaminare i nomi e restituire **true** se supporta il nome del servizio e la coppia di nomi di argomento oppure **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-128">The server must examine the names and return **TRUE** if it supports the service name and topic name pair or **FALSE** if it does not.</span></span>

<span data-ttu-id="1c7c0-129">Se nessun server risponde in modo positivo alla richiesta di connessione del client, il client riceve **null** da [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e non viene stabilita alcuna conversazione.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-129">If no server responds positively to the client's request to connect, the client receives **NULL** from [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) and no conversation is established.</span></span> <span data-ttu-id="1c7c0-130">Se un server restituisce **true**, viene stabilita una conversazione e il client riceve un handle di conversazione, ovvero un valore **DWORD** che identifica la conversazione.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-130">If a server returns **TRUE**, a conversation is established and the client receives a conversation handle — a **DWORD** value that identifies the conversation.</span></span> <span data-ttu-id="1c7c0-131">Il client usa l'handle nelle successive chiamate DDEML per ottenere i dati dal server.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-131">The client uses the handle in subsequent DDEML calls to obtain data from the server.</span></span> <span data-ttu-id="1c7c0-132">Il server riceve la transazione di [**\_ \_ conferma XTYP Connect**](xtyp-connect-confirm.md) , a meno che il server non abbia specificato il flag di filtro di CBF \_ Skip \_ Connect \_ confirms.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-132">The server receives the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction (unless the server specified the CBF\_SKIP\_CONNECT\_CONFIRMS filter flag).</span></span> <span data-ttu-id="1c7c0-133">Questa transazione passa l'handle di conversazione al server.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-133">This transaction passes the conversation handle to the server.</span></span>

<span data-ttu-id="1c7c0-134">Nell'esempio seguente viene richiesta una conversazione nell'argomento di sistema con un server che riconosce il nome del servizio MyServer.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-134">The following example requests a conversation on the System topic with a server that recognizes the service name MyServer.</span></span> <span data-ttu-id="1c7c0-135">I parametri *hszServName* e *hszSysTopic* sono stati creati in precedenza come handle di stringa.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-135">The *hszServName* and *hszSysTopic* parameters are previously created string handles.</span></span>


```
HCONV hConv;         // conversation handle 
HWND hwndParent;     // parent window handle 
HSZ hszServName;     // service name string handle 
HSZ hszSysTopic;     // System topic string handle 
 
hConv = DdeConnect( 
    idInst,               // instance identifier 
    hszServName,          // service name string handle 
    hszSysTopic,          // System topic string handle 
    (PCONVCONTEXT) NULL); // use default context 
 
if (hConv == NULL) 
{ 
    MessageBox(hwndParent, "MyServer is unavailable.", 
        (LPSTR) NULL, MB_OK); 
    return FALSE; 
} 
```



<span data-ttu-id="1c7c0-136">Nell'esempio precedente, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) fa sì che la funzione di callback DDE dell'applicazione MyServer riceva una transazione [**di \_ connessione XTYP**](xtyp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="1c7c0-136">In the preceding example, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) causes the DDE callback function of the MyServer application to receive an [**XTYP\_CONNECT**](xtyp-connect.md) transaction.</span></span>

<span data-ttu-id="1c7c0-137">Nell'esempio seguente, il server risponde alla transazione [**XTYP \_ Connect**](xtyp-connect.md) confrontando la stringa del nome dell'argomento handle DDEML passato al server con ogni elemento nella matrice di nome argomento stringa Handles the server supports.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-137">In the following example, the server responds to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction by comparing the topic name string handle the DDEML passed to the server with each element in the array of topic name string handles the server supports.</span></span> <span data-ttu-id="1c7c0-138">Se il server individua una corrispondenza, stabilisce la conversazione.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-138">If the server finds a match, it establishes the conversation.</span></span>


```
#define CTOPICS 5 
 
HSZ hsz1;                  // string handle passed by DDEML 
HSZ ahszTopics[CTOPICS];   // array of supported topics 
int i;                     // loop counter 
 
// Use a switch statement to examine transaction types. 
// Here is the connect case.
 
    case XTYP_CONNECT: 
        for (i = 0; i < CTOPICS; i++) 
        { 
            if (hsz1 == ahszTopics[i]) 
                return TRUE;   // establish a conversation 
        } 
 
        return FALSE; // Topic not supported; deny conversation.  
 
// Process other transaction types. 
```



<span data-ttu-id="1c7c0-139">Se il server restituisce **true** in risposta alla transazione [**di \_ connessione XTYP**](xtyp-connect.md) , DDEML invia una transazione [**di \_ \_ Conferma connessione XTYP**](xtyp-connect-confirm.md) alla funzione di callback DDE del server.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-139">If the server returns **TRUE** in response to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction, the DDEML sends an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's DDE callback function.</span></span> <span data-ttu-id="1c7c0-140">Il server può ottenere l'handle per la conversazione elaborando la transazione.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-140">The server can obtain the handle to the conversation by processing this transaction.</span></span>

<span data-ttu-id="1c7c0-141">Un client può stabilire una conversazione con caratteri jolly specificando **null** per l'handle di stringa del nome del servizio, l'handle di stringa del nome dell'argomento o entrambi in una chiamata a [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect).</span><span class="sxs-lookup"><span data-stu-id="1c7c0-141">A client can establish a wildcard conversation by specifying **NULL** for the service name string handle, the topic name string handle, or both in a call to [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect).</span></span> <span data-ttu-id="1c7c0-142">Se almeno uno degli handle di stringa è **null**, DDEML invia la transazione [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) alle funzioni di callback di tutte le applicazioni DDE (ad eccezione di quelle che filtrano la transazione **XTYP \_ WILDCONNECT** ).</span><span class="sxs-lookup"><span data-stu-id="1c7c0-142">If at least one of the string handles is **NULL**, the DDEML sends the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the callback functions of all DDE applications (except those that filter the **XTYP\_WILDCONNECT** transaction).</span></span> <span data-ttu-id="1c7c0-143">Ogni applicazione server deve rispondere restituendo un handle di dati che identifica una matrice con terminazione null di strutture [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) .</span><span class="sxs-lookup"><span data-stu-id="1c7c0-143">Each server application should respond by returning a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="1c7c0-144">Se l'applicazione server non ha chiamato [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per registrare i nomi di servizio e se il filtro è on, il server non riceverà le transazioni **XTYP \_ WILDCONNECT** .</span><span class="sxs-lookup"><span data-stu-id="1c7c0-144">If the server application has not called [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to register its service names and if filtering is on, the server does not receive **XTYP\_WILDCONNECT** transactions.</span></span> <span data-ttu-id="1c7c0-145">Per ulteriori informazioni sugli handle di dati, vedere [Gestione dati](data-management.md).</span><span class="sxs-lookup"><span data-stu-id="1c7c0-145">For more information about data handles, see [Data Management](data-management.md).</span></span>

<span data-ttu-id="1c7c0-146">La matrice deve contenere una struttura per ogni coppia nome servizio e nome argomento che corrisponde alla coppia specificata dal client.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-146">The array must contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="1c7c0-147">DDEML seleziona una delle coppie per stabilire una conversazione e restituisce al client un handle che identifica la conversazione.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-147">The DDEML selects one of the pairs to establish a conversation and returns to the client a handle that identifies the conversation.</span></span> <span data-ttu-id="1c7c0-148">DDEML invia la transazione [**di \_ \_ Conferma connessione XTYP**](xtyp-connect-confirm.md) al server (a meno che il server non filtri questa transazione).</span><span class="sxs-lookup"><span data-stu-id="1c7c0-148">The DDEML sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server (unless the server filters this transaction).</span></span> <span data-ttu-id="1c7c0-149">Nell'esempio seguente viene illustrata una tipica risposta server alla transazione [**\_ WILDCONNECT di XTYP**](xtyp-wildconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="1c7c0-149">The following example shows a typical server response to the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```
#define CTOPICS 2 
 
UINT uType; 
HSZPAIR ahszp[(CTOPICS + 1)]; 
HSZ ahszTopicList[CTOPICS]; 
HSZ hszServ, hszTopic; 
WORD i, j; 
 
if (uType == XTYP_WILDCONNECT) 
{ 
    // Scan the topic list and create an array of HSZPAIR structures. 
 
    j = 0; 
    for (i = 0; i < CTOPICS; i++) 
    { 
        if (hszTopic == (HSZ) NULL || 
                hszTopic == ahszTopicList[i]) 
        { 
            ahszp[j].hszSvc = hszServ; 
            ahszp[j++].hszTopic = ahszTopicList[i]; 
        } 
    } 
 
    // End the list with an HSZPAIR structure that contains NULL 
    // string handles as its members. 
 
    ahszp[j].hszSvc = NULL; 
    ahszp[j++].hszTopic = NULL; 
 
    // Return a handle to a global memory object containing the 
    // HSZPAIR structures. 
 
    return DdeCreateDataHandle( 
        idInst,          // instance identifier 
        (LPBYTE) &ahszp, // pointer to HSZPAIR array 
        sizeof(HSZ) * j, // length of the array 
        0,               // start at the beginning 
        (HSZ) NULL,      // no item name string 
        0,               // return the same format 
        0);              // let the system own it 
} 
```



<span data-ttu-id="1c7c0-150">Il client o il server possono terminare una conversazione in qualsiasi momento chiamando la funzione [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) .</span><span class="sxs-lookup"><span data-stu-id="1c7c0-150">Either the client or the server can terminate a conversation at any time by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="1c7c0-151">Questa funzione fa in modo che la funzione di callback del partner nella conversazione riceva la transazione di [**\_ disconnessione XTYP**](xtyp-disconnect.md) , a meno che il partner non abbia specificato il \_ flag di filtro di \_ disconnessione CBF Skip.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-151">This function causes the callback function of the partner in the conversation to receive the [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction (unless the partner specified the CBF\_SKIP\_DISCONNECTS filter flag).</span></span> <span data-ttu-id="1c7c0-152">In genere, un'applicazione risponde alla transazione **di \_ disconnessione XTYP** utilizzando la funzione [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) per ottenere informazioni sulla conversazione terminata.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-152">Typically, an application responds to the **XTYP\_DISCONNECT** transaction by using the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function to obtain information about the conversation that terminated.</span></span> <span data-ttu-id="1c7c0-153">Quando la funzione di callback restituisce l'elaborazione della transazione di **\_ disconnessione XTYP** , l'handle di conversazione non è più valido.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-153">After the callback function returns from processing the **XTYP\_DISCONNECT** transaction, the conversation handle is no longer valid.</span></span>

<span data-ttu-id="1c7c0-154">Un'applicazione client che riceve una transazione di [**\_ disconnessione XTYP**](xtyp-disconnect.md) nella relativa funzione di callback DDE può tentare di ristabilire la conversazione chiamando la funzione [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) .</span><span class="sxs-lookup"><span data-stu-id="1c7c0-154">A client application that receives an [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction in its DDE callback function can attempt to reestablish the conversation by calling the [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) function.</span></span> <span data-ttu-id="1c7c0-155">Il client deve chiamare **DdeReconnect** dall'interno della relativa funzione di callback DDE.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-155">The client must call **DdeReconnect** from within its DDE callback function.</span></span>

## <a name="multiple-conversations"></a><span data-ttu-id="1c7c0-156">Più conversazioni</span><span class="sxs-lookup"><span data-stu-id="1c7c0-156">Multiple Conversations</span></span>

<span data-ttu-id="1c7c0-157">Un'applicazione client può utilizzare la funzione [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) per determinare se tutti i server di interesse sono disponibili nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-157">A client application can use the [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function to determine whether any servers of interest are available in the system.</span></span> <span data-ttu-id="1c7c0-158">Un client specifica un nome di servizio e un nome di argomento quando chiama **DdeConnectList**, facendo in modo che DDEML trasmetta la transazione [**\_ WILDCONNECT XTYP**](xtyp-wildconnect.md) alle funzioni di callback DDE di tutti i server che corrispondono al nome del servizio (ad eccezione di quelli che filtrano la transazione).</span><span class="sxs-lookup"><span data-stu-id="1c7c0-158">A client specifies a service name and topic name when it calls **DdeConnectList**, causing the DDEML to broadcast the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the DDE callback functions of all servers that match the service name (except those that filter the transaction).</span></span> <span data-ttu-id="1c7c0-159">La funzione di callback di un server deve restituire un handle di dati che identifichi una matrice con terminazione null di strutture [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) .</span><span class="sxs-lookup"><span data-stu-id="1c7c0-159">A server's callback function should return a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="1c7c0-160">La matrice deve contenere una struttura per ogni coppia nome servizio e nome argomento che corrisponde alla coppia specificata dal client.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-160">The array should contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="1c7c0-161">DDEML stabilisce una conversazione per ogni struttura **HSZPAIR** riempita dal server e restituisce un handle dell'elenco di conversazioni al client.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-161">The DDEML establishes a conversation for each **HSZPAIR** structure filled by the server and returns a conversation list handle to the client.</span></span> <span data-ttu-id="1c7c0-162">Il server riceve l'handle di conversazione tramite la transazione [**di \_ connessione XTYP**](xtyp-connect.md) (a meno che il server non filtri questa transazione).</span><span class="sxs-lookup"><span data-stu-id="1c7c0-162">The server receives the conversation handle by way of the [**XTYP\_CONNECT**](xtyp-connect.md) transaction (unless the server filters this transaction).</span></span>

<span data-ttu-id="1c7c0-163">Un client può specificare **null** per il nome del servizio, il nome dell'argomento o entrambi quando chiama [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="1c7c0-163">A client can specify **NULL** for the service name, topic name, or both when it calls [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="1c7c0-164">Se il nome del servizio è **null**, tutti i server del sistema che supportano il nome dell'argomento specificato rispondono.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-164">If the service name is **NULL**, all servers in the system that support the specified topic name respond.</span></span> <span data-ttu-id="1c7c0-165">Viene stabilita una conversazione con ogni server che risponde, incluse più istanze dello stesso server.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-165">A conversation is established with each responding server, including multiple instances of the same server.</span></span> <span data-ttu-id="1c7c0-166">Se il nome dell'argomento è **null**, viene stabilita una conversazione per ogni argomento riconosciuto da ogni server che corrisponde al nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-166">If the topic name is **NULL**, a conversation is established on each topic recognized by each server that matches the service name.</span></span>

<span data-ttu-id="1c7c0-167">Un client può utilizzare le funzioni [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) e [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) per identificare i server che rispondono a [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="1c7c0-167">A client can use the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to identify the servers that respond to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="1c7c0-168">**DdeQueryNextServer** restituisce l'handle di conversazione successivo in un elenco di conversazioni e **DdeQueryConvInfo** riempie una struttura [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) con le informazioni sulla conversazione.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-168">**DdeQueryNextServer** returns the next conversation handle in a conversation list, and **DdeQueryConvInfo** fills a [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) structure with information about the conversation.</span></span> <span data-ttu-id="1c7c0-169">Il client può gestire gli handle di conversazione necessari ed eliminare il resto dall'elenco delle conversazioni.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-169">The client can keep the conversation handles that it needs and discard the rest from the conversation list.</span></span>

<span data-ttu-id="1c7c0-170">Nell'esempio seguente viene utilizzato [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) per stabilire conversazioni con tutti i server che supportano l'argomento di sistema, quindi vengono utilizzate le funzioni [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) e [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) per ottenere gli handle di stringa del nome di servizio dei server e archiviarli in un buffer.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-170">The following example uses [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) to establish conversations with all servers that support the System topic and then uses the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to obtain the servers' service name string handles and store them in a buffer.</span></span>


```
HCONVLIST hconvList; // conversation list 
DWORD idInst;        // instance identifier 
HSZ hszSystem;       // System topic 
HCONV hconv = NULL;  // conversation handle 
CONVINFO ci;         // holds conversation data 
UINT cConv = 0;      // count of conv. handles 
HSZ *pHsz, *aHsz;    // point to string handles 
 
// Connect to all servers that support the System topic. 
 
hconvList = DdeConnectList(idInst, NULL, hszSystem, NULL, NULL); 
 
// Count the number of handles in the conversation list. 
 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
    cConv++; 
 
// Allocate a buffer for the string handles. 
 
hconv = NULL; 
aHsz = (HSZ *) LocalAlloc(LMEM_FIXED, cConv * sizeof(HSZ)); 
 
// Copy the string handles to the buffer. 
 
pHsz = aHsz; 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
{ 
    DdeQueryConvInfo(hconv, QID_SYNC, (PCONVINFO) &ci); 
    DdeKeepStringHandle(idInst, ci.hszSvcPartner); 
    *pHsz++ = ci.hszSvcPartner; 
} 
 
// Use the handles; converse with the servers. 
 
// Free the memory and terminate the conversations. 
 
LocalFree((HANDLE) aHsz); 
DdeDisconnectList(hconvList); 
```



<span data-ttu-id="1c7c0-171">Un'applicazione può terminare una singola conversazione in un elenco di conversazioni chiamando la funzione [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) .</span><span class="sxs-lookup"><span data-stu-id="1c7c0-171">An application can terminate an individual conversation in a conversation list by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="1c7c0-172">Un'applicazione può terminare tutte le conversazioni in un elenco di conversazioni chiamando la funzione [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) .</span><span class="sxs-lookup"><span data-stu-id="1c7c0-172">An application can terminate all conversations in a conversation list by calling the [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) function.</span></span> <span data-ttu-id="1c7c0-173">Entrambe le funzioni fanno sì che DDEML invii XTYP transazioni di [**\_ disconnessione**](xtyp-disconnect.md) alla funzione di callback DDE di ogni partner.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-173">Both functions cause the DDEML to send [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transactions to each partner's DDE callback function.</span></span> <span data-ttu-id="1c7c0-174">**DdeDisconnectList** invia una transazione di **\_ disconnessione XTYP** per ogni handle di conversazione presente nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-174">**DdeDisconnectList** sends an **XTYP\_DISCONNECT** transaction for each conversation handle in the list.</span></span>

<span data-ttu-id="1c7c0-175">Un client può recuperare un elenco di handle di conversazione in un elenco di conversazioni passando un handle dell'elenco di conversazioni esistente a [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="1c7c0-175">A client can retrieve a list of the conversation handles in a conversation list by passing an existing conversation list handle to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="1c7c0-176">Il processo di enumerazione rimuove gli handle delle conversazioni interrotte dall'elenco e le conversazioni non duplicate che soddisfano il nome del servizio e il nome dell'argomento specificati vengono aggiunti.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-176">The enumeration process removes the handles of terminated conversations from the list, and nonduplicate conversations that fit the specified service name and topic name are added.</span></span>

<span data-ttu-id="1c7c0-177">Se [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) specifica un handle dell'elenco di conversazioni esistente, la funzione crea un nuovo elenco di conversazioni che contiene gli handle delle nuove conversazioni e degli handle dall'elenco esistente.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-177">If [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) specifies an existing conversation list handle, the function creates a new conversation list that contains the handles of any new conversations and the handles from the existing list.</span></span>

<span data-ttu-id="1c7c0-178">Se esistono conversazioni duplicate, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) tenta di impedire handle di conversazione duplicati nell'elenco delle conversazioni.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-178">If duplicate conversations exist, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) attempts to prevent duplicate conversation handles in the conversation list.</span></span> <span data-ttu-id="1c7c0-179">Una conversazione duplicata è una seconda conversazione con lo stesso server con lo stesso nome di servizio e nome di argomento.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-179">A duplicate conversation is a second conversation with the same server on the same service name and topic name.</span></span> <span data-ttu-id="1c7c0-180">Due conversazioni di questo tipo hanno handle diversi, ma identificano la stessa conversazione.</span><span class="sxs-lookup"><span data-stu-id="1c7c0-180">Two such conversations would have different handles, yet they would identify the same conversation.</span></span>

 

 




