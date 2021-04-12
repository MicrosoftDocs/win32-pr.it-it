---
title: Utilizzo di Dynamic Data Exchange
description: In questo argomento vengono forniti esempi di codice relativi a Dynamic Data Exchange.
ms.assetid: 6d94403b-64b4-4763-868a-3b94431dab79
keywords:
- Dynamic Data Exchange (DDE), conversazioni
- DDE (Dynamic Data Exchange), conversazioni
- scambio di dati, Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), esempi
- DDE (Dynamic Data Exchange), esempi
- Dynamic Data Exchange (DDE), comandi nelle applicazioni server
- DDE (Dynamic Data Exchange), comandi nelle applicazioni server
- Dynamic Data Exchange (DDE), collegamenti dati
- DDE (Dynamic Data Exchange), collegamenti dati
- Dynamic Data Exchange (DDE), elementi
- DDE (Dynamic Data Exchange), elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe20c4dedc38303fe9bcb9c4b0fae42d03ee536
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337911"
---
# <a name="using-dynamic-data-exchange"></a><span data-ttu-id="edd55-114">Utilizzo di Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="edd55-114">Using Dynamic Data Exchange</span></span>

<span data-ttu-id="edd55-115">Questa sezione contiene esempi di codice sulle attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="edd55-115">This section has code samples on the following tasks:</span></span>

-   [<span data-ttu-id="edd55-116">Avvio di una conversazione</span><span class="sxs-lookup"><span data-stu-id="edd55-116">Initiating a Conversation</span></span>](#initiating-a-conversation)
-   [<span data-ttu-id="edd55-117">Trasferimento di un singolo elemento</span><span class="sxs-lookup"><span data-stu-id="edd55-117">Transferring a Single Item</span></span>](#transferring-a-single-item)
    -   [<span data-ttu-id="edd55-118">Recupero di un elemento dal server</span><span class="sxs-lookup"><span data-stu-id="edd55-118">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
    -   [<span data-ttu-id="edd55-119">Invio di un elemento al server</span><span class="sxs-lookup"><span data-stu-id="edd55-119">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)
-   [<span data-ttu-id="edd55-120">Creazione di un collegamento dati permanente</span><span class="sxs-lookup"><span data-stu-id="edd55-120">Establishing a Permanent Data Link</span></span>](#establishing-a-permanent-data-link)
    -   [<span data-ttu-id="edd55-121">Avvio di un collegamento dati</span><span class="sxs-lookup"><span data-stu-id="edd55-121">Initiating a Data Link</span></span>](#initiating-a-data-link)
    -   [<span data-ttu-id="edd55-122">Avvio di un collegamento dati con il comando Incolla collegamento</span><span class="sxs-lookup"><span data-stu-id="edd55-122">Initiating a Data Link with the Paste Link Command</span></span>](#initiating-a-data-link-with-the-paste-link-command)
    -   [<span data-ttu-id="edd55-123">Notifica al client che i dati sono stati modificati</span><span class="sxs-lookup"><span data-stu-id="edd55-123">Notifying the Client that Data Has Changed</span></span>](#notifying-the-client-that-data-has-changed)
    -   [<span data-ttu-id="edd55-124">Terminazione di un collegamento dati</span><span class="sxs-lookup"><span data-stu-id="edd55-124">Terminating a Data Link</span></span>](#terminating-a-data-link)
-   [<span data-ttu-id="edd55-125">Esecuzione di comandi in un'applicazione server</span><span class="sxs-lookup"><span data-stu-id="edd55-125">Carrying Out Commands in a Server Application</span></span>](#carrying-out-commands-in-a-server-application)
-   [<span data-ttu-id="edd55-126">Terminazione di una conversazione</span><span class="sxs-lookup"><span data-stu-id="edd55-126">Terminating a Conversation</span></span>](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a><span data-ttu-id="edd55-127">Avvio di una conversazione</span><span class="sxs-lookup"><span data-stu-id="edd55-127">Initiating a Conversation</span></span>

<span data-ttu-id="edd55-128">Per avviare una conversazione di Dynamic Data Exchange (DDE), il client invia un messaggio di [**\_ \_ inizializzazione di WM DDE**](wm-dde-initiate.md) .</span><span class="sxs-lookup"><span data-stu-id="edd55-128">To initiate a Dynamic Data Exchange (DDE) conversation, the client sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message.</span></span> <span data-ttu-id="edd55-129">In genere, il client trasmette questo messaggio chiamando [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), con-1 come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="edd55-129">Usually, the client broadcasts this message by calling [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), with –1 as the first parameter.</span></span> <span data-ttu-id="edd55-130">Se l'applicazione dispone già dell'handle di finestra per l'applicazione server, il messaggio può essere inviato direttamente a tale finestra.</span><span class="sxs-lookup"><span data-stu-id="edd55-130">If the application already has the window handle to the server application, it can send the message directly to that window.</span></span> <span data-ttu-id="edd55-131">Il client prepara gli atomi per il nome dell'applicazione e il nome dell'argomento chiamando [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma).</span><span class="sxs-lookup"><span data-stu-id="edd55-131">The client prepares atoms for the application name and topic name by calling [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma).</span></span> <span data-ttu-id="edd55-132">Il client può richiedere conversazioni con qualsiasi applicazione server potenziale e per qualsiasi potenziale argomento fornendo atomi **null** (carattere jolly) per l'applicazione e l'argomento.</span><span class="sxs-lookup"><span data-stu-id="edd55-132">The client can request conversations with any potential server application and for any potential topic by supplying **NULL** (wildcard) atoms for the application and topic.</span></span>

<span data-ttu-id="edd55-133">Nell'esempio seguente viene illustrata la modalità di avvio di una conversazione da parte del client, in cui vengono specificati sia l'applicazione che l'argomento.</span><span class="sxs-lookup"><span data-stu-id="edd55-133">The following example illustrates how the client initiates a conversation, where both the application and topic are specified.</span></span>


```
    static BOOL fInInitiate = FALSE; 
    char *szApplication; 
    char *szTopic; 
    atomApplication = *szApplication == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szApplication); 
    atomTopic = *szTopic == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szTopic); 
 
    fInInitiate = TRUE; 
    SendMessage((HWND) HWND_BROADCAST, // broadcasts message 
        WM_DDE_INITIATE,               // initiates conversation 
        (WPARAM) hwndClientDDE,        // handle to client DDE window 
        MAKELONG(atomApplication,      // application-name atom 
            atomTopic));               // topic-name atom 
    fInInitiate = FALSE; 
    if (atomApplication != NULL) 
        GlobalDeleteAtom(atomApplication); 
    if (atomTopic != NULL) 
        GlobalDeleteAtom(atomTopic);
```



> [!Note]  
> <span data-ttu-id="edd55-134">Se l'applicazione usa atomi **null** , non è necessario usare le funzioni [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) e [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) .</span><span class="sxs-lookup"><span data-stu-id="edd55-134">If your application uses **NULL** atoms, you need not use the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) and [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) functions.</span></span> <span data-ttu-id="edd55-135">In questo esempio, l'applicazione client crea due atomi globali che contengono rispettivamente il nome del server e il nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="edd55-135">In this example, the client application creates two global atoms containing the name of the server and the name of the topic, respectively.</span></span>

 

<span data-ttu-id="edd55-136">L'applicazione client invia un messaggio di [**\_ \_ inizializzazione del DDE WM**](wm-dde-initiate.md) con questi due atomi nel parametro *lParam* del messaggio.</span><span class="sxs-lookup"><span data-stu-id="edd55-136">The client application sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message with these two atoms in the *lParam* parameter of the message.</span></span> <span data-ttu-id="edd55-137">Nella chiamata alla funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , l'handle di finestra speciale – 1 indica al sistema di inviare il messaggio a tutte le altre applicazioni attive.</span><span class="sxs-lookup"><span data-stu-id="edd55-137">In the call to the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, the special window handle –1 directs the system to send this message to all other active applications.</span></span> <span data-ttu-id="edd55-138">**SendMessage** non torna all'applicazione client fino a quando tutte le applicazioni che ricevono il messaggio non hanno a sua volta restituito il controllo al sistema.</span><span class="sxs-lookup"><span data-stu-id="edd55-138">**SendMessage** does not return to the client application until all applications that receive the message have, in turn, returned control to the system.</span></span> <span data-ttu-id="edd55-139">Ciò significa che tutti i messaggi di [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) inviati in risposta dalle applicazioni server vengono elaborati dal client nel momento in cui la chiamata **SendMessage** ha restituito.</span><span class="sxs-lookup"><span data-stu-id="edd55-139">This means that all [**WM\_DDE\_ACK**](wm-dde-ack.md) messages sent in reply by the server applications are guaranteed to have been processed by the client by the time the **SendMessage** call has returned.</span></span>

<span data-ttu-id="edd55-140">Dopo la restituzione di [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , l'applicazione client elimina gli atomi globali.</span><span class="sxs-lookup"><span data-stu-id="edd55-140">After [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application deletes the global atoms.</span></span>

<span data-ttu-id="edd55-141">Le applicazioni server rispondono secondo la logica illustrata nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="edd55-141">Server applications respond according to the logic illustrated in the following diagram.</span></span>

![logica di risposta dell'applicazione server](images/csdde-01.png)

<span data-ttu-id="edd55-143">Per confermare uno o più argomenti, il server deve creare atomi per ogni conversazione (richiedendo atomi di nome applicazione duplicati se sono presenti più argomenti) e inviare un messaggio di [**\_ \_ ACK DDE WM**](wm-dde-ack.md) per ogni conversazione, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="edd55-143">To acknowledge one or more topics, the server must create atoms for each conversation (requiring duplicate application-name atoms if there are multiple topics) and send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each conversation, as illustrated in the following example.</span></span>


```
if ((atomApplication = GlobalAddAtom("Server")) != 0) 
{ 
    if ((atomTopic = GlobalAddAtom(szTopic)) != 0) 
    { 
        SendMessage(hwndClientDDE, 
            WM_DDE_ACK, 
            (WPARAM) hwndServerDDE, 
            MAKELONG(atomApplication, atomTopic)); 
        GlobalDeleteAtom(atomApplication); 
    } 
 
    GlobalDeleteAtom(atomTopic); 
} 
 
if ((atomApplication == 0) || (atomTopic == 0)) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="edd55-144">Quando un server risponde con un messaggio [**\_ \_ ACK DDE WM**](wm-dde-ack.md) , l'applicazione client deve salvare un handle per la finestra del server.</span><span class="sxs-lookup"><span data-stu-id="edd55-144">When a server responds with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client application should save a handle to the server window.</span></span> <span data-ttu-id="edd55-145">Il client che riceve l'handle come parametro *wParam* del messaggio **\_ \_ ACK DDE WM** invia quindi tutti i messaggi DDE successivi alla finestra del server identificata da questo handle.</span><span class="sxs-lookup"><span data-stu-id="edd55-145">The client receiving the handle as the *wParam* parameter of the **WM\_DDE\_ACK** message then sends all subsequent DDE messages to the server window this handle identifies.</span></span>

<span data-ttu-id="edd55-146">Se l'applicazione client utilizza un Atom **null** per il nome dell'applicazione o dell'argomento, si prevede che l'applicazione riceva i riconoscimenti da più di un'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="edd55-146">If your client application uses a **NULL** atom for the application name or topic name, expect the application to receive acknowledgments from more than one server application.</span></span> <span data-ttu-id="edd55-147">Più riconoscimenti possono provenire da più istanze di un server DDE, anche se l'applicazione client non **utilizza gli** atomi.</span><span class="sxs-lookup"><span data-stu-id="edd55-147">Multiple acknowledgements can also come from multiple instances of a DDE server, even if your client application does not **NULL** use atoms.</span></span> <span data-ttu-id="edd55-148">Un server deve sempre usare una finestra univoca per ogni conversazione.</span><span class="sxs-lookup"><span data-stu-id="edd55-148">A server should always use a unique window for each conversation.</span></span> <span data-ttu-id="edd55-149">La routine della finestra nell'applicazione client può utilizzare un handle per la finestra del server (fornito come parametro *lParam* dell' [**\_ \_ avvio di WM DDE**](wm-dde-initiate.md)) per tenere traccia di più conversazioni.</span><span class="sxs-lookup"><span data-stu-id="edd55-149">The window procedure in the client application can use a handle to the server window (provided as the *lParam* parameter of [**WM\_DDE\_INITIATE**](wm-dde-initiate.md)) to track multiple conversations.</span></span> <span data-ttu-id="edd55-150">Ciò consente a una singola finestra client di elaborare diverse conversazioni senza dover terminare e riconnettersi a una nuova finestra del client per ogni conversazione.</span><span class="sxs-lookup"><span data-stu-id="edd55-150">This allows a single client window to process several conversations without needing to terminate and reconnect with a new client window for each conversation.</span></span>

## <a name="transferring-a-single-item"></a><span data-ttu-id="edd55-151">Trasferimento di un singolo elemento</span><span class="sxs-lookup"><span data-stu-id="edd55-151">Transferring a Single Item</span></span>

<span data-ttu-id="edd55-152">Una volta stabilita una conversazione DDE, il client può recuperare il valore di un elemento di dati dal server inviando il messaggio di [**\_ \_ richiesta DDE di WM**](wm-dde-request.md) oppure inviare un valore dell'elemento di dati al server eseguendo il [**\_ \_ poke DDE di WM**](wm-dde-poke.md).</span><span class="sxs-lookup"><span data-stu-id="edd55-152">Once a DDE conversation has been established, the client can either retrieve the value of a data item from the server by issuing the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or submit a data-item value to the server by issuing [**WM\_DDE\_POKE**](wm-dde-poke.md).</span></span>

-   [<span data-ttu-id="edd55-153">Recupero di un elemento dal server</span><span class="sxs-lookup"><span data-stu-id="edd55-153">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
-   [<span data-ttu-id="edd55-154">Invio di un elemento al server</span><span class="sxs-lookup"><span data-stu-id="edd55-154">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a><span data-ttu-id="edd55-155">Recupero di un elemento dal server</span><span class="sxs-lookup"><span data-stu-id="edd55-155">Retrieving an Item from the Server</span></span>

<span data-ttu-id="edd55-156">Per recuperare un elemento dal server, il client invia al server un messaggio [**di \_ \_ richiesta DDE WM**](wm-dde-request.md) che specifica l'elemento e il formato da recuperare, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="edd55-156">To retrieve an item from the server, the client sends the server a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message specifying the item and format to retrieve, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_REQUEST, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_REQUEST, CF_TEXT, atomItem))) 
    {
        GlobalDeleteAtom(atomItem); 
    }
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="edd55-157">In questo esempio, il client specifica il formato degli Appunti del **\_ testo CF** come formato preferito per l'elemento di dati richiesto.</span><span class="sxs-lookup"><span data-stu-id="edd55-157">In this example, the client specifies the clipboard format **CF\_TEXT** as the preferred format for the requested data item.</span></span>

<span data-ttu-id="edd55-158">Il ricevitore (Server) del messaggio [**di \_ \_ richiesta DDE di WM**](wm-dde-request.md) deve in genere eliminare il Atom dell'elemento, ma se la chiamata al [**messaggio**](/windows/desktop/api/winuser/nf-winuser-postmessagea) non riesce, il client deve eliminare il formato Atom.</span><span class="sxs-lookup"><span data-stu-id="edd55-158">The receiver (server) of the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message typically must delete the item atom, but if the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) call fails, the client must delete the atom.</span></span>

<span data-ttu-id="edd55-159">Se il server ha accesso all'elemento richiesto ed è in grado di eseguirne il rendering nel formato richiesto, il server copia il valore dell'elemento come oggetto Shared Memory e invia al client un messaggio di [**\_ \_ dati DDE di WM**](wm-dde-data.md) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="edd55-159">If the server has access to the requested item and can render it in the requested format, the server copies the item value as a shared memory object and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as illustrated in the following example.</span></span>


```
// Allocate the size of the DDE data header, plus the data: a 
// string,<CR><LF><NULL>. The byte for the string's terminating 
// null character is counted by DDEDATA.Value[1].

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEDATA) + *pcch + 2)))  
{
    return; 
}
 
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData)))  
{
    GlobalFree(hData); 
    return; 
} 
 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpData->Value, *pcch +1, (LPCSTR) szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
} 
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItemName)) != 0) 
{ 
    lParam = PackDDElParam(WM_DDE_ACK, (UINT) hData, atomItem); 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            lParam)) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_ACK, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors.  
}
```



<span data-ttu-id="edd55-160">In questo esempio, l'applicazione server alloca un oggetto memoria per contenere l'elemento dati.</span><span class="sxs-lookup"><span data-stu-id="edd55-160">In this example, the server application allocates a memory object to contain the data item.</span></span> <span data-ttu-id="edd55-161">L'oggetto dati viene inizializzato come struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) .</span><span class="sxs-lookup"><span data-stu-id="edd55-161">The data object is initialized as a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span>

<span data-ttu-id="edd55-162">L'applicazione server imposta quindi il membro **cfFormat** della struttura su testo CF \_ per informare l'applicazione client che i dati sono in formato testo.</span><span class="sxs-lookup"><span data-stu-id="edd55-162">The server application then sets the **cfFormat** member of the structure to CF\_TEXT to inform the client application that the data is in text format.</span></span> <span data-ttu-id="edd55-163">Il client risponde copiando il valore dei dati richiesti nel membro del **valore** della struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) .</span><span class="sxs-lookup"><span data-stu-id="edd55-163">The client responds by copying the value of the requested data into the **Value** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span> <span data-ttu-id="edd55-164">Dopo che il server ha riempito l'oggetto dati, il server Sblocca i dati e crea un Atom globale contenente il nome dell'elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="edd55-164">After the server has filled the data object, the server unlocks the data and creates a global atom containing the name of the data item.</span></span>

<span data-ttu-id="edd55-165">Infine, il server emette il messaggio di [**\_ \_ dati DDE di WM**](wm-dde-data.md) chiamando [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea).</span><span class="sxs-lookup"><span data-stu-id="edd55-165">Finally, the server issues the [**WM\_DDE\_DATA**](wm-dde-data.md) message by calling [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea).</span></span> <span data-ttu-id="edd55-166">L'handle per l'oggetto dati e il formato Atom contenente il nome dell'elemento vengono compressi nel parametro *lParam* del messaggio tramite la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) .</span><span class="sxs-lookup"><span data-stu-id="edd55-166">The handle to the data object and the atom containing the item name are packed into the *lParam* parameter of the message by the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function.</span></span>

<span data-ttu-id="edd55-167">Se [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) ha esito negativo, il server deve usare la funzione [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) per liberare il parametro *lParam* compresso.</span><span class="sxs-lookup"><span data-stu-id="edd55-167">If [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) fails, the server must use the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function to free the packed *lParam* parameter.</span></span> <span data-ttu-id="edd55-168">Il server deve inoltre liberare il parametro *lParam* compresso per il messaggio di [**\_ \_ richiesta DDE WM**](wm-dde-request.md) ricevuto.</span><span class="sxs-lookup"><span data-stu-id="edd55-168">The server must also free the packed *lParam* parameter for the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message it received.</span></span>

<span data-ttu-id="edd55-169">Se il server non è in grado di soddisfare la richiesta, invia un messaggio [**\_ \_ ACK DDE**](wm-dde-ack.md) negativo al client, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="edd55-169">If the server cannot satisfy the request, it sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the client, as shown in the following example.</span></span>


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



<span data-ttu-id="edd55-170">Al momento della ricezione di un messaggio di [**\_ \_ dati DDE di WM**](wm-dde-data.md) , il client elabora il valore dell'elemento di dati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="edd55-170">Upon receiving a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the client processes the data-item value as appropriate.</span></span> <span data-ttu-id="edd55-171">Se quindi il membro **fAckReq** a cui puntava il messaggio di **\_ \_ dati DDE di WM** è 1, il client deve inviare al server un messaggio [**\_ \_ ACK DDE positivo WM**](wm-dde-ack.md) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="edd55-171">Then, if the **fAckReq** member pointed to in the **WM\_DDE\_DATA** message is 1, the client must send the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message, as shown in the following example.</span></span>


```
UnpackDDElParam(WM_DDE_DATA, lParam, (PUINT) &hData, 
    (PUINT) &atomItem); 
if (!(lpDDEData = (DDEDATA FAR*) GlobalLock(hData)) 
        || (lpDDEData->cfFormat != CF_TEXT)) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // Negative ACK. 
} 
 
// Copy data from lpDDEData here. 
 
if (lpDDEData->fAckReq) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0x8000, 
            atomItem)); // Positive ACK 
} 
 
bRelease = lpDDEData->fRelease; 
GlobalUnlock(hData); 
if (bRelease) 
    GlobalFree(hData);
```



<span data-ttu-id="edd55-172">In questo esempio, il client esamina il formato dei dati.</span><span class="sxs-lookup"><span data-stu-id="edd55-172">In this example, the client examines the format of the data.</span></span> <span data-ttu-id="edd55-173">Se il formato non è **un \_ testo CF** (o se il client non è in grado di bloccare la memoria per i dati), il client invia un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) negativo per indicare che non è in grado di elaborare i dati.</span><span class="sxs-lookup"><span data-stu-id="edd55-173">If the format is not **CF\_TEXT** (or if the client cannot lock the memory for the data), the client sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to indicate that it cannot process the data.</span></span> <span data-ttu-id="edd55-174">Se il client non è in grado di bloccare un handle di dati perché l'handle contiene il membro **fAckReq** , il client non deve inviare un messaggio **\_ \_ ACK DDE di WM** negativo.</span><span class="sxs-lookup"><span data-stu-id="edd55-174">If the client cannot lock a data handle because the handle contains the **fAckReq** member, the client should not send a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="edd55-175">Al contrario, il client deve terminare la conversazione.</span><span class="sxs-lookup"><span data-stu-id="edd55-175">Instead, the client should terminate the conversation.</span></span>

<span data-ttu-id="edd55-176">Se un client invia un riconoscimento negativo in risposta a un messaggio [**di \_ \_ dati DDE di WM**](wm-dde-data.md) , il server è responsabile della liberazione della memoria (ma non del parametro *lParam* ) a cui fa riferimento il messaggio di **\_ \_ dati DDE di WM** associato al riconoscimento negativo.</span><span class="sxs-lookup"><span data-stu-id="edd55-176">If a client sends a negative acknowledgment in response to a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the server is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_DATA** message associated with the negative acknowledgment.</span></span>

<span data-ttu-id="edd55-177">Se è in grado di elaborare i dati, il client esamina il membro **fAckReq** della struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) per determinare se il server ha richiesto di essere informato che il client ha ricevuto ed elaborato correttamente i dati.</span><span class="sxs-lookup"><span data-stu-id="edd55-177">If it can process the data, the client examines the **fAckReq** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to determine whether the server requested that it be informed that the client received and processed the data successfully.</span></span> <span data-ttu-id="edd55-178">Se il server ha richiesto queste informazioni, il client invia al server un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) positivo.</span><span class="sxs-lookup"><span data-stu-id="edd55-178">If the server did request this information, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="edd55-179">Poiché lo sblocco dei dati invalida il puntatore ai dati, il client salva il valore del membro **fRelease** prima di sbloccare l'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="edd55-179">Because unlocking data invalidates the pointer to the data, the client saves the value of the **fRelease** member before unlocking the data object.</span></span> <span data-ttu-id="edd55-180">Dopo aver salvato il valore, il client lo esamina per determinare se l'applicazione server ha richiesto al client di liberare la memoria contenente i dati. il client agisce di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="edd55-180">After saving the value, the client then examines it to determine whether the server application requested the client to free the memory containing the data; the client acts accordingly.</span></span>

<span data-ttu-id="edd55-181">Al momento della ricezione di un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) negativo, il client può richiedere di nuovo lo stesso valore dell'elemento, specificando un formato degli Appunti diverso.</span><span class="sxs-lookup"><span data-stu-id="edd55-181">Upon receiving a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client can ask for the same item value again, specifying a different clipboard format.</span></span> <span data-ttu-id="edd55-182">In genere, un client richiederà per prima cosa il formato più complesso che può supportare, quindi eseguire un'istruzione per difetto con formati progressivamente più semplici fino a quando non ne troverà uno che il server è in grado di fornire.</span><span class="sxs-lookup"><span data-stu-id="edd55-182">Typically, a client will first ask for the most complex format it can support, then step down if necessary through progressively simpler formats until it finds one the server can provide.</span></span>

<span data-ttu-id="edd55-183">Se il server supporta l'elemento formats dell'argomento System, il client può determinare una volta il formato degli appunti supportato dal server, anziché determinarli ogni volta che il client richiede un elemento.</span><span class="sxs-lookup"><span data-stu-id="edd55-183">If the server supports the Formats item of the system topic, the client can determine once what clipboard formats the server supports, instead of determining them each time the client requests an item.</span></span>

### <a name="submitting-an-item-to-the-server"></a><span data-ttu-id="edd55-184">Invio di un elemento al server</span><span class="sxs-lookup"><span data-stu-id="edd55-184">Submitting an Item to the Server</span></span>

<span data-ttu-id="edd55-185">Il client può inviare un valore dell'elemento al server tramite il messaggio [**di \_ \_ poke DDE di WM**](wm-dde-poke.md) .</span><span class="sxs-lookup"><span data-stu-id="edd55-185">The client may send an item value to the server by using the [**WM\_DDE\_POKE**](wm-dde-poke.md) message.</span></span> <span data-ttu-id="edd55-186">Il client esegue il rendering dell'elemento da inviare e invia il messaggio di **\_ \_ poke DDE di WM** , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="edd55-186">The client renders the item to be sent and sends the **WM\_DDE\_POKE** message, as illustrated in the following example.</span></span>


```
size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hPokeData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEPOKE) + *pcch + 2))) 
{
    return; 
}
 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData))) 
{ 
    GlobalFree(hPokeData); 
    return; 
} 
 
lpPokeData->fRelease = TRUE; 
lpPokeData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpPokeData->Value, *pcch +1, (LPCSTR) szValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpPokeData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hPokeData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItem)) != 0) 
{ 
 
        if (!PostMessage(hwndServerDDE, 
                WM_DDE_POKE, 
                (WPARAM) hwndClientDDE, 
                PackDDElParam(WM_DDE_POKE, (UINT) hPokeData, 
                    atomItem))) 
        { 
            GlobalDeleteAtom(atomItem); 
            GlobalFree(hPokeData); 
        } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
} 
```



> [!Note]  
> <span data-ttu-id="edd55-187">L'invio di dati tramite un messaggio [**\_ \_ poke DDE di WM**](wm-dde-poke.md) è essenzialmente analogo all'invio tramite [**\_ \_ dati DDE**](wm-dde-data.md)di WM, ad eccezione del fatto che **WM \_ DDE \_ poke** viene inviato dal client al server.</span><span class="sxs-lookup"><span data-stu-id="edd55-187">Sending data by using a [**WM\_DDE\_POKE**](wm-dde-poke.md) message is essentially the same as sending it by using [**WM\_DDE\_DATA**](wm-dde-data.md), except that **WM\_DDE\_POKE** is sent from the client to the server.</span></span>

 

<span data-ttu-id="edd55-188">Se il server è in grado di accettare il valore dell'elemento di dati nel formato di cui è stato eseguito il rendering dal client, il server elabora il valore dell'elemento in base alle esigenze e invia al client un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) positivo.</span><span class="sxs-lookup"><span data-stu-id="edd55-188">If the server is able to accept the data-item value in the format rendered by the client, the server processes the item value as appropriate and sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="edd55-189">Se non è in grado di elaborare il valore dell'elemento, a causa del formato o per altri motivi, il server invia al client un messaggio **\_ \_ ACK DDE di WM** negativo.</span><span class="sxs-lookup"><span data-stu-id="edd55-189">If it is unable to process the item value, because of its format or for other reasons, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>


```
UnpackDDElParam(WM_DDE_POKE, lParam, (PUINT) &hPokeData, 
    (PUINT) &atomItem); 
GlobalGetAtomName(atomItem, szItemName, ITEM_NAME_MAX_SIZE); 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData)) 
        || lpPokeData->cfFormat != CF_TEXT 
        || !IsItemSupportedByServer(szItemName)) 
{ 
    PostMessage(hwndClientDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndServerDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // negative ACK  
}
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
} 
hResult = StringCchCopy(szItemValue, *pcch +1, lpPokeData->Value); // copies value 
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
bRelease = lpPokeData->fRelease; 
GlobalUnlock(hPokeData); 
if (bRelease) 
{ 
    GlobalFree(hPokeData); 
} 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 
         0x8000, atomItem));    // positive ACK.
```



<span data-ttu-id="edd55-190">In questo esempio, il server chiama [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) per recuperare il nome dell'elemento inviato dal client.</span><span class="sxs-lookup"><span data-stu-id="edd55-190">In this example, the server calls [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) to retrieve the name of the item the client sent.</span></span> <span data-ttu-id="edd55-191">Il server determina quindi se supporta l'elemento e se viene eseguito il rendering dell'elemento nel formato corretto (ovvero il testo CF \_ ).</span><span class="sxs-lookup"><span data-stu-id="edd55-191">The server then determines whether it supports the item and whether the item is rendered in the correct format (that is, CF\_TEXT).</span></span> <span data-ttu-id="edd55-192">Se l'elemento non è supportato e non viene sottoposto a rendering nel formato corretto o se il server non è in grado di bloccare la memoria per i dati, il server invia un riconoscimento negativo all'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="edd55-192">If the item is not supported and not rendered in the correct format, or if the server cannot lock the memory for the data, the server sends a negative acknowledgment back to the client application.</span></span> <span data-ttu-id="edd55-193">Si noti che in questo caso, l'invio di un riconoscimento negativo è corretto perché per i messaggi [**\_ \_ poke DDE di WM**](wm-dde-poke.md) si presuppone sempre che sia impostato il membro **fAckReq** .</span><span class="sxs-lookup"><span data-stu-id="edd55-193">Note that in this case, sending a negative acknowledgment is correct because [**WM\_DDE\_POKE**](wm-dde-poke.md) messages are always assumed to have the **fAckReq** member set.</span></span> <span data-ttu-id="edd55-194">Il server deve ignorare il membro.</span><span class="sxs-lookup"><span data-stu-id="edd55-194">The server should ignore the member.</span></span>

<span data-ttu-id="edd55-195">Se un server invia un riconoscimento negativo in risposta a un messaggio [**\_ \_ poke DDE WM**](wm-dde-poke.md) , il client è responsabile della liberazione della memoria (ma non del parametro *lParam* ) a cui fa riferimento il messaggio **di \_ \_ poke DDE di WM** associato al riconoscimento negativo.</span><span class="sxs-lookup"><span data-stu-id="edd55-195">If a server sends a negative acknowledgment in response to a [**WM\_DDE\_POKE**](wm-dde-poke.md) message, the client is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_POKE** message associated with the negative acknowledgment.</span></span>

## <a name="establishing-a-permanent-data-link"></a><span data-ttu-id="edd55-196">Creazione di un collegamento dati permanente</span><span class="sxs-lookup"><span data-stu-id="edd55-196">Establishing a Permanent Data Link</span></span>

<span data-ttu-id="edd55-197">Un'applicazione client può utilizzare DDE per stabilire un collegamento a un elemento in un'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="edd55-197">A client application can use DDE to establish a link to an item in a server application.</span></span> <span data-ttu-id="edd55-198">Dopo aver stabilito un collegamento di questo tipo, il server invia aggiornamenti periodici dell'elemento collegato al client, in genere ogni volta che viene modificato il valore dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="edd55-198">After such a link is established, the server sends periodic updates of the linked item to the client, typically, whenever the value of the item changes.</span></span> <span data-ttu-id="edd55-199">Viene pertanto stabilito un flusso di dati permanente tra le due applicazioni; Questo flusso di dati rimane attivo fino a quando non viene disconnesso in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="edd55-199">Thus, a permanent data stream is established between the two applications; this data stream remains in place until it is explicitly disconnected.</span></span>

### <a name="initiating-a-data-link"></a><span data-ttu-id="edd55-200">Avvio di un collegamento dati</span><span class="sxs-lookup"><span data-stu-id="edd55-200">Initiating a Data Link</span></span>

<span data-ttu-id="edd55-201">Il client avvia un collegamento dati pubblicando un messaggio [**di \_ \_ notifica DDE di WM**](wm-dde-advise.md) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="edd55-201">The client initiates a data link by posting a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, as shown in the following example.</span></span>


```
if (!(hOptions = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(DDEADVISE)))) 
    return; 
if (!(lpOptions = (DDEADVISE FAR*) GlobalLock(hOptions))) 
{ 
    GlobalFree(hOptions); 
    return; 
} 
 
lpOptions->cfFormat = CF_TEXT; 
lpOptions->fAckReq = TRUE; 
lpOptions->fDeferUpd = FALSE; 
GlobalUnlock(hOptions); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!(PostMessage(hwndServerDDE, 
            WM_DDE_ADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_ADVISE, (UINT) hOptions, 
                atomItem)))) 
    { 
        GlobalDeleteAtom(atomItem); 
        GlobalFree(hOptions); 
        FreeDDElParam(WM_DDE_ADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors 
 
}
```



<span data-ttu-id="edd55-202">In questo esempio, l'applicazione client imposta il flag **FDeferUpd** del messaggio [**di \_ \_ avviso DDE di WM**](wm-dde-advise.md) su **false**.</span><span class="sxs-lookup"><span data-stu-id="edd55-202">In this example, the client application sets the **fDeferUpd** flag of the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to **FALSE**.</span></span> <span data-ttu-id="edd55-203">In questo modo l'applicazione server invia i dati al client ogni volta che i dati vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="edd55-203">This directs the server application to send the data to the client whenever the data changes.</span></span>

<span data-ttu-id="edd55-204">Se il server non è in grado di servire la richiesta di [**\_ \_ notifica DDE di WM**](wm-dde-advise.md) , invia al client un messaggio di [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) negativo.</span><span class="sxs-lookup"><span data-stu-id="edd55-204">If the server is unable to service the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) request, it sends the client a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="edd55-205">Tuttavia, se il server ha accesso all'elemento e può eseguirne il rendering nel formato richiesto, il server annota il nuovo collegamento, chiamando i flag specificati nel parametro *hOptions* , e invia al client un messaggio **\_ \_ ACK DDE** positivo.</span><span class="sxs-lookup"><span data-stu-id="edd55-205">But if the server has access to the item and can render it in the requested format, the server notes the new link (recalling the flags specified in the *hOptions* parameter) and sends the client a positive **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="edd55-206">Da quel momento in poi, fino a quando il client non emette un messaggio di avviso [**\_ \_ DDE di WM**](wm-dde-unadvise.md) corrispondente, il server invia i nuovi dati al client ogni volta che il valore dell'elemento viene modificato nel server.</span><span class="sxs-lookup"><span data-stu-id="edd55-206">From then on, until the client issues a matching [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, the server sends the new data to the client every time the value of the item changes in the server.</span></span>

<span data-ttu-id="edd55-207">Il messaggio di [**\_ \_ notifica DDE di WM**](wm-dde-advise.md) stabilisce il formato dei dati da scambiare durante il collegamento.</span><span class="sxs-lookup"><span data-stu-id="edd55-207">The [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message establishes the format of the data to be exchanged during the link.</span></span> <span data-ttu-id="edd55-208">Se il client tenta di stabilire un altro collegamento con lo stesso elemento, ma usa un formato dati diverso, il server può scegliere di rifiutare il secondo formato dati o tentare di supportarlo.</span><span class="sxs-lookup"><span data-stu-id="edd55-208">If the client attempts to establish another link with the same item but is using a different data format, the server can choose to reject the second data format or attempt to support it.</span></span> <span data-ttu-id="edd55-209">Se è stato stabilito un collegamento a caldo per qualsiasi elemento di dati, il server può supportare un solo formato dati alla volta.</span><span class="sxs-lookup"><span data-stu-id="edd55-209">If a warm link has been established for any data item, the server can support only one data format at a time.</span></span> <span data-ttu-id="edd55-210">Questo è dovuto al fatto che il messaggio di [**\_ \_ dati DDE di WM**](wm-dde-data.md) per un collegamento a caldo ha un handle di dati **null** , che altrimenti contiene le informazioni sul formato.</span><span class="sxs-lookup"><span data-stu-id="edd55-210">This is because the [**WM\_DDE\_DATA**](wm-dde-data.md) message for a warm link has a **NULL** data handle, which otherwise contains the format information.</span></span> <span data-ttu-id="edd55-211">Pertanto, un server deve rifiutare tutti i collegamenti caldi per un elemento già collegato e deve rifiutare tutti i collegamenti per un elemento con collegamenti caldi.</span><span class="sxs-lookup"><span data-stu-id="edd55-211">Thus, a server must reject all warm links for an item already linked, and must reject all links for an item that has warm links.</span></span> <span data-ttu-id="edd55-212">Un'altra interpretazione potrebbe essere che il server modifica il formato e lo stato attivo o caldo di un collegamento quando viene richiesto un secondo collegamento per lo stesso elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="edd55-212">Another interpretation may be that the server changes the format and the hot or warm state of a link when a second link is requested for the same data item.</span></span>

<span data-ttu-id="edd55-213">In generale, le applicazioni client non devono tentare di stabilire più di un collegamento alla volta per un elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="edd55-213">In general, client applications should not attempt to establish more than one link at a time for a data item.</span></span>

### <a name="initiating-a-data-link-with-the-paste-link-command"></a><span data-ttu-id="edd55-214">Avvio di un collegamento dati con il comando Incolla collegamento</span><span class="sxs-lookup"><span data-stu-id="edd55-214">Initiating a Data Link with the Paste Link Command</span></span>

<span data-ttu-id="edd55-215">Le applicazioni che supportano i collegamenti dati ad accesso frequente o caldo in genere supportano un formato degli Appunti registrato denominato collegamento.</span><span class="sxs-lookup"><span data-stu-id="edd55-215">Applications that support hot or warm data links typically support a registered clipboard format named Link.</span></span> <span data-ttu-id="edd55-216">Quando è associato ai comandi copia e Incolla collegamento dell'applicazione, questo formato degli Appunti consente all'utente di stabilire conversazioni DDE tra le applicazioni semplicemente copiando un elemento di dati nell'applicazione server e incollarlo nell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="edd55-216">When associated with the application's Copy and Paste Link commands, this clipboard format enables the user to establish DDE conversations between applications simply by copying a data item in the server application and pasting it into the client application.</span></span>

<span data-ttu-id="edd55-217">Un'applicazione server supporta il formato degli Appunti di collegamento inserendo negli Appunti una stringa contenente i nomi dell'applicazione, dell'argomento e dell'elemento quando l'utente sceglie il comando **Copy** dal menu **modifica** .</span><span class="sxs-lookup"><span data-stu-id="edd55-217">A server application supports the Link clipboard format by placing in the clipboard a string containing the application, topic, and item names when the user chooses the **Copy** command from the **Edit** menu.</span></span> <span data-ttu-id="edd55-218">Di seguito è riportato il formato di collegamento standard:</span><span class="sxs-lookup"><span data-stu-id="edd55-218">Following is the standard Link format:</span></span>

<span data-ttu-id="edd55-219">*applicazione ***\\ 0*** argomento ***\\ 0*** elemento \* \* \\ 0 0 \\*\*</span><span class="sxs-lookup"><span data-stu-id="edd55-219">*application ***\\0*** topic ***\\0*** item\*\*\*\\0\\0*\*</span></span>

<span data-ttu-id="edd55-220">Un singolo carattere null separa i nomi e due caratteri null terminano l'intera stringa.</span><span class="sxs-lookup"><span data-stu-id="edd55-220">A single null character separates the names, and two null characters terminate the entire string.</span></span>

<span data-ttu-id="edd55-221">Le applicazioni client e server devono registrare il formato degli Appunti di collegamento, come illustrato:</span><span class="sxs-lookup"><span data-stu-id="edd55-221">Both the client and server applications must register the Link clipboard format, as shown:</span></span>


```
cfLink = RegisterClipboardFormat("Link");
```



<span data-ttu-id="edd55-222">Un'applicazione client supporta il formato degli Appunti di collegamento per mezzo di un comando Incolla collegamento nel menu Modifica.</span><span class="sxs-lookup"><span data-stu-id="edd55-222">A client application supports the Link clipboard format by means of a Paste Link command on its Edit menu.</span></span> <span data-ttu-id="edd55-223">Quando l'utente sceglie questo comando, l'applicazione client analizza i nomi dell'applicazione, dell'argomento e degli elementi dai dati degli Appunti in formato di collegamento.</span><span class="sxs-lookup"><span data-stu-id="edd55-223">When the user chooses this command, the client application parses the application, topic, and item names from the Link-format clipboard data.</span></span> <span data-ttu-id="edd55-224">Usando questi nomi, l'applicazione client avvia una conversazione per l'applicazione e l'argomento, se tale conversazione non esiste già.</span><span class="sxs-lookup"><span data-stu-id="edd55-224">Using these names, the client application initiates a conversation for the application and topic, if such a conversation does not already exist.</span></span> <span data-ttu-id="edd55-225">L'applicazione client invia quindi un messaggio di [**\_ \_ notifica DDE di WM**](wm-dde-advise.md) all'applicazione server, specificando il nome dell'elemento contenuto nei dati degli Appunti in formato collegamento.</span><span class="sxs-lookup"><span data-stu-id="edd55-225">The client application then sends a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server application, specifying the item name contained in the Link-format clipboard data.</span></span>

<span data-ttu-id="edd55-226">Di seguito è riportato un esempio di risposta di un'applicazione client quando l'utente sceglie il comando Incolla collegamento.</span><span class="sxs-lookup"><span data-stu-id="edd55-226">Following is an example of a client application's response when the user chooses the Paste Link command.</span></span>


```
void DoPasteLink(hwndClientDDE) 
HWND hwndClientDDE; 
{ 
    HANDLE hData; 
    LPSTR lpData; 
    HWND hwndServerDDE; 
    CHAR szApplication[APP_MAX_SIZE + 1]; 
    CHAR szTopic[TOPIC_MAX_SIZE + 1]; 
    CHAR szItem[ITEM_MAX_SIZE + 1]; 
    size_t * nBufLen; 
 HRESULT hResult;
 
    if (OpenClipboard(hwndClientDDE)) 
    { 
        if (!(hData = GetClipboardData(cfLink)) || 
                !(lpData = GlobalLock(hData))) 
        { 
            CloseClipboard(); 
            return; 
        } 
 
        // Parse the clipboard data.
  hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
// TODO: Write error handler.
  return;
 }
 if (*nBufLen >= APP_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szApplication, APP_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
// TODO: Write error handler.
  return;
 }
        lpData += (*nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= TOPIC_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szTopic, TOPIC_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 }
        lpData += (nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= ITEM_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }

 hResult = StringCchCopy(szItem, ITEM_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 } 
        GlobalUnlock(hData); 
        CloseClipboard(); 
 
        if (hwndServerDDE = 
                FindServerGivenAppTopic(szApplication, szTopic)) 
        { 
            // App/topic conversation is already started. 
 
            if (DoesAdviseAlreadyExist(hwndServerDDE, szItem)) 
            {
                MessageBox(hwndMain, 
                    "Advisory already established", 
                    "Client", MB_ICONEXCLAMATION | MB_OK); 
            }
            else SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
        } 
        else 
        { 
            // Client must initiate a new conversation first. 
            SendInitiate(szApplication, szTopic); 
            if (hwndServerDDE = 
                    FindServerGivenAppTopic(szApplication, 
                        szTopic)) 
            {
                SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
            }
        } 
    } 
    return; 
}
```



<span data-ttu-id="edd55-227">In questo esempio, l'applicazione client apre gli appunti e determina se contiene dati nel formato di collegamento (ovvero cfLink) precedentemente registrato.</span><span class="sxs-lookup"><span data-stu-id="edd55-227">In this example, the client application opens the clipboard and determines whether it contains data in the Link format (that is, cfLink) it had previously registered.</span></span> <span data-ttu-id="edd55-228">In caso contrario, o se non è in grado di bloccare i dati negli Appunti, il client restituisce.</span><span class="sxs-lookup"><span data-stu-id="edd55-228">If not, or if it cannot lock the data in the clipboard, the client returns.</span></span>

<span data-ttu-id="edd55-229">Quando l'applicazione client recupera un puntatore ai dati degli Appunti, analizza i dati per estrarre i nomi dell'applicazione, dell'argomento e dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="edd55-229">After the client application retrieves a pointer to the clipboard data, it parses the data to extract the application, topic, and item names.</span></span>

<span data-ttu-id="edd55-230">L'applicazione client determina se una conversazione nell'argomento esiste già tra l'applicazione e l'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="edd55-230">The client application determines whether a conversation on the topic already exists between it and the server application.</span></span> <span data-ttu-id="edd55-231">Se esiste una conversazione, il client verifica se esiste già un collegamento per l'elemento dati.</span><span class="sxs-lookup"><span data-stu-id="edd55-231">If a conversation does exist, the client checks whether a link already exists for the data item.</span></span> <span data-ttu-id="edd55-232">Se esiste un collegamento di questo tipo, il client visualizza una finestra di messaggio all'utente; in caso contrario, chiama la propria funzione *SendAdvise* per inviare un messaggio di [**\_ \_ notifica DDE di WM**](wm-dde-advise.md) al server per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="edd55-232">If such a link exists, the client displays a message box to the user; otherwise, it calls its own *SendAdvise* function to send a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server for the item.</span></span>

<span data-ttu-id="edd55-233">Se una conversazione nell'argomento non esiste già tra il client e il server, il client chiama prima la propria funzione *SendInitiate* per trasmettere il messaggio di [**\_ \_ inizializzazione di WM DDE**](wm-dde-initiate.md) per richiedere una conversazione e, in secondo luogo, chiama la propria funzione *FindServerGivenAppTopic* per stabilire la conversazione con la finestra che risponde per conto dell'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="edd55-233">If a conversation on the topic does not already exist between the client and the server, the client first calls its own *SendInitiate* function to broadcast the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message to request a conversation and, second, calls its own *FindServerGivenAppTopic* function to establish the conversation with the window that responds on behalf of the server application.</span></span> <span data-ttu-id="edd55-234">Una volta iniziata la conversazione, l'applicazione client chiama *SendAdvise* per richiedere il collegamento.</span><span class="sxs-lookup"><span data-stu-id="edd55-234">After the conversation has begun, the client application calls *SendAdvise* to request the link.</span></span>

### <a name="notifying-the-client-that-data-has-changed"></a><span data-ttu-id="edd55-235">Notifica al client che i dati sono stati modificati</span><span class="sxs-lookup"><span data-stu-id="edd55-235">Notifying the Client that Data Has Changed</span></span>

<span data-ttu-id="edd55-236">Quando il client stabilisce un collegamento usando il messaggio [**di \_ \_ notifica DDE di WM**](wm-dde-advise.md) , con il membro **FDeferUpd** non impostato (ovvero uguale a zero) nella struttura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) , il client ha richiesto al server di inviare l'elemento dati ogni volta che il valore dell'elemento cambia.</span><span class="sxs-lookup"><span data-stu-id="edd55-236">When the client establishes a link by using the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, with the **fDeferUpd** member not set (that is, equal to zero) in the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure, the client has requested the server send the data item each time the item's value changes.</span></span> <span data-ttu-id="edd55-237">In questi casi, il server esegue il rendering del nuovo valore dell'elemento di dati nel formato specificato in precedenza e invia al client un messaggio di [**\_ \_ dati DDE WM**](wm-dde-data.md) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="edd55-237">In such cases, the server renders the new value of the data item in the previously specified format and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as shown in the following example.</span></span>


```
// Allocate the size of a DDE data header, plus data (a string), 
// plus a <CR><LF><NULL> 

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  sizeof(DDEDATA) + *pcch + 3))) 
{
    return; 
}
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData))) 
{ 
    GlobalFree(hData); 
    return; 
} 
lpData->fAckReq = bAckRequest;       // as in original WM_DDE_ADVISE 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy(lpData->Value, *pcch +1, szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
// add CR/LF for CF_TEXT format
hResult = StringCchCat(lpData->Value, *pcch + 3, "\r\n");
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            PackDDElParam(WM_DDE_DATA, (UINT) hData, atomItem))) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_DATA, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
 
}
```



<span data-ttu-id="edd55-238">In questo esempio, il client elabora il valore dell'elemento in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="edd55-238">In this example, the client processes the item value as appropriate.</span></span> <span data-ttu-id="edd55-239">Se viene impostato il flag **fAckReq** per l'elemento, il client invia al server un messaggio [**\_ \_ ACK DDE positivo WM**](wm-dde-ack.md) .</span><span class="sxs-lookup"><span data-stu-id="edd55-239">If the **fAckReq** flag for the item is set, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="edd55-240">Quando il client stabilisce il collegamento con il set di membri **FDeferUpd** (ovvero, uguale a 1), il client ha richiesto che solo una notifica, non i dati stessi, venga inviata ogni volta che i dati cambiano.</span><span class="sxs-lookup"><span data-stu-id="edd55-240">When the client establishes the link, with the **fDeferUpd** member set (that is, equal to 1), the client has requested that only a notification, not the data itself, be sent each time the data changes.</span></span> <span data-ttu-id="edd55-241">In questi casi, quando il valore dell'elemento viene modificato, il server non esegue il rendering del valore ma invia semplicemente al client un messaggio di [**\_ \_ dati DDE WM**](wm-dde-data.md) con un handle di dati null, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="edd55-241">In such cases, when the item value changes, the server does not render the value but simply sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message with a null data handle, as illustrated in the following example.</span></span>


```
if (bDeferUpd)      // check whether flag was set in WM_DDE_ADVISE
{
    if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
    { 
        if (!PostMessage(hwndClientDDE, 
                WM_DDE_DATA, 
                (WPARAM) hwndServerDDE, 
                PackDDElParam(WM_DDE_DATA, 0, 
                    atomItem)))                  // NULL data
        {
            GlobalDeleteAtom(atomItem); 
            FreeDDElParam(WM_DDE_DATA, lParam); 
        } 
    } 
} 
 
if (atomItem == 0) 
{ 
     // Handle errors. 
} 
```



<span data-ttu-id="edd55-242">Se necessario, il client può richiedere il valore più recente dell'elemento di dati emettendo un normale messaggio [**di \_ \_ richiesta DDE di WM**](wm-dde-request.md) oppure ignorare semplicemente l'avviso dal server in cui sono stati modificati i dati.</span><span class="sxs-lookup"><span data-stu-id="edd55-242">As necessary, the client can request the latest value of the data item by issuing a normal [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or it can simply ignore the notice from the server that the data has changed.</span></span> <span data-ttu-id="edd55-243">In entrambi i casi, se **fAckReq** è uguale a 1, il client deve inviare al server un messaggio di [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) positivo.</span><span class="sxs-lookup"><span data-stu-id="edd55-243">In either case, if **fAckReq** is equal to 1, the client is expected to send a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the server.</span></span>

### <a name="terminating-a-data-link"></a><span data-ttu-id="edd55-244">Terminazione di un collegamento dati</span><span class="sxs-lookup"><span data-stu-id="edd55-244">Terminating a Data Link</span></span>

<span data-ttu-id="edd55-245">Se il client richiede la terminazione di un collegamento dati specifico, il client invia al server un messaggio di [**\_ \_ Unadvise DDE di WM**](wm-dde-unadvise.md) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="edd55-245">If the client requests that a specific data link be terminated, the client sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_UNADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_UNADVISE, 0, atomItem))) 
    { 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_UNADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="edd55-246">Il server verifica se il client dispone attualmente di un collegamento all'elemento specifico di questa conversazione.</span><span class="sxs-lookup"><span data-stu-id="edd55-246">The server checks whether the client currently has a link to the specific item in this conversation.</span></span> <span data-ttu-id="edd55-247">Se esiste un collegamento, il server invia al client un messaggio [**\_ \_ ACK DDE**](wm-dde-ack.md) positivo. il server non è più necessario per inviare aggiornamenti sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="edd55-247">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server is then no longer required to send updates about the item.</span></span> <span data-ttu-id="edd55-248">Se non esiste alcun collegamento, il server invia al client un **messaggio \_ \_ ACK DDE di WM** negativo.</span><span class="sxs-lookup"><span data-stu-id="edd55-248">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

<span data-ttu-id="edd55-249">Il messaggio di [**\_ \_ Unadvise DDE WM**](wm-dde-unadvise.md) specifica un formato dati.</span><span class="sxs-lookup"><span data-stu-id="edd55-249">The [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message specifies a data format.</span></span> <span data-ttu-id="edd55-250">Il formato zero indica al server di arrestare tutti i collegamenti per l'elemento specificato, anche se vengono stabiliti diversi collegamenti sensibili e ognuno usa un formato diverso.</span><span class="sxs-lookup"><span data-stu-id="edd55-250">A format of zero informs the server to stop all links for the specified item, even if several hot links are established and each uses a different format.</span></span>

<span data-ttu-id="edd55-251">Per terminare tutti i collegamenti per una conversazione, l'applicazione client invia al server un messaggio di annullamento dell' [**\_ \_ avviso DDE di WM**](wm-dde-unadvise.md) con un Atom elemento null.</span><span class="sxs-lookup"><span data-stu-id="edd55-251">To terminate all links for a conversation, the client application sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message with a null item atom.</span></span> <span data-ttu-id="edd55-252">Il server determina se per la conversazione è attualmente stabilito almeno un collegamento.</span><span class="sxs-lookup"><span data-stu-id="edd55-252">The server determines whether the conversation has at least one link currently established.</span></span> <span data-ttu-id="edd55-253">Se esiste un collegamento, il server invia al client un messaggio [**\_ \_ ACK DDE**](wm-dde-ack.md) positivo. il server non deve più inviare aggiornamenti nella conversazione.</span><span class="sxs-lookup"><span data-stu-id="edd55-253">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server then no longer has to send any updates in the conversation.</span></span> <span data-ttu-id="edd55-254">Se non esiste alcun collegamento, il server invia al client un **messaggio \_ \_ ACK DDE di WM** negativo.</span><span class="sxs-lookup"><span data-stu-id="edd55-254">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

## <a name="carrying-out-commands-in-a-server-application"></a><span data-ttu-id="edd55-255">Esecuzione di comandi in un'applicazione server</span><span class="sxs-lookup"><span data-stu-id="edd55-255">Carrying Out Commands in a Server Application</span></span>

<span data-ttu-id="edd55-256">Le applicazioni possono utilizzare il messaggio di [**\_ \_ esecuzione DDE di WM**](wm-dde-execute.md) per fare in modo che venga eseguito un determinato comando o una serie di comandi in un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="edd55-256">Applications can use the [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message to cause a certain command or series of commands to be carried out in another application.</span></span> <span data-ttu-id="edd55-257">A tale scopo, il client invia al server un messaggio di **\_ \_ esecuzione DDE WM** contenente un handle a una stringa di comando, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="edd55-257">To do this, the client sends the server a **WM\_DDE\_EXECUTE** message containing a handle to a command string, as shown in the following example.</span></span>


```
HRESULT hResult;
  
if (!(hCommand = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(szCommandString) + 1))) 
{
    return; 
}
if (!(lpCommand = GlobalLock(hCommand))) 
{ 
    GlobalFree(hCommand); 
    return; 
} 

hResult = StringCbCopy(lpCommand, sizeof(szCommandString), szCommandString);
if (hResult != S_OK)
{
// TODO: Write error handler.
 return;
}
 
GlobalUnlock(hCommand); 
if (!PostMessage(hwndServerDDE, 
        WM_DDE_EXECUTE, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_EXECUTE, 0, (UINT) hCommand))) 
{ 
    GlobalFree(hCommand); 
    FreeDDElParam(WM_DDE_EXECUTE, lParam); 
}
```



<span data-ttu-id="edd55-258">In questo esempio, il server tenta di eseguire la stringa di comando specificata.</span><span class="sxs-lookup"><span data-stu-id="edd55-258">In this example, the server attempts to carry out the specified command string.</span></span> <span data-ttu-id="edd55-259">Se ha esito positivo, il server invia al client un [**messaggio \_ \_ ACK DDE**](wm-dde-ack.md) positivo. in caso contrario, invia un messaggio di **\_ \_ ACK DDE WM** negativo.</span><span class="sxs-lookup"><span data-stu-id="edd55-259">If it succeeds, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; otherwise, it sends a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="edd55-260">Questo messaggio di **\_ \_ ACK DDE WM** riutilizza l'handle *hCommand* passato nel messaggio [**\_ \_ Execute DDE**](wm-dde-execute.md) originale di WM.</span><span class="sxs-lookup"><span data-stu-id="edd55-260">This **WM\_DDE\_ACK** message reuses the *hCommand* handle passed in the original [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message.</span></span>

<span data-ttu-id="edd55-261">Se la stringa di esecuzione dei comandi del client richiede che il server termini, il server deve rispondere inviando un messaggio [**\_ \_ ACK DDE positivo WM**](wm-dde-ack.md) e quindi inviare un messaggio di [**\_ \_ terminazione DDE WM**](wm-dde-terminate.md) prima di terminare.</span><span class="sxs-lookup"><span data-stu-id="edd55-261">If the client's command execution string requests that the server terminate, the server should respond by sending a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message and then post a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message before terminating.</span></span> <span data-ttu-id="edd55-262">Tutti gli altri comandi inviati con un messaggio di [**\_ \_ esecuzione DDE di WM**](wm-dde-execute.md) devono essere eseguiti in modo sincrono, ovvero il server deve inviare un messaggio **\_ \_ ACK DDE WM** solo dopo aver completato correttamente il comando.</span><span class="sxs-lookup"><span data-stu-id="edd55-262">All other commands sent with a [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message should be executed synchronously; that is, the server should send a **WM\_DDE\_ACK** message only after successfully completing the command.</span></span>

## <a name="terminating-a-conversation"></a><span data-ttu-id="edd55-263">Terminazione di una conversazione</span><span class="sxs-lookup"><span data-stu-id="edd55-263">Terminating a Conversation</span></span>

<span data-ttu-id="edd55-264">Il client o il server può emettere un messaggio [**di \_ \_ terminazione DDE di WM**](wm-dde-terminate.md) per terminare una conversazione in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="edd55-264">Either the client or the server can issue a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to terminate a conversation at any time.</span></span> <span data-ttu-id="edd55-265">Analogamente, entrambe le applicazioni client e server devono essere preparate a ricevere questo messaggio in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="edd55-265">Similarly, both the client and server applications should be prepared to receive this message at any time.</span></span> <span data-ttu-id="edd55-266">Un'applicazione deve terminare tutte le conversazioni prima di arrestarsi.</span><span class="sxs-lookup"><span data-stu-id="edd55-266">An application must terminate all of its conversations before shutting down.</span></span>

<span data-ttu-id="edd55-267">Nell'esempio seguente, l'applicazione che termina la conversazione invia un messaggio [**di \_ \_ terminazione DDE di WM**](wm-dde-terminate.md) .</span><span class="sxs-lookup"><span data-stu-id="edd55-267">In the following example, the application terminating the conversation posts a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span>


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



<span data-ttu-id="edd55-268">In questo modo si informa l'altra applicazione che l'applicazione mittente non invierà altri messaggi e il destinatario potrà chiudere la finestra.</span><span class="sxs-lookup"><span data-stu-id="edd55-268">This informs the other application that the sending application will send no further messages and the recipient can close its window.</span></span> <span data-ttu-id="edd55-269">Il destinatario è previsto in tutti i casi per rispondere tempestivamente inviando un messaggio di [**\_ \_ terminazione del DDE WM**](wm-dde-terminate.md) .</span><span class="sxs-lookup"><span data-stu-id="edd55-269">The recipient is expected in all cases to respond promptly by sending a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span> <span data-ttu-id="edd55-270">Il destinatario non deve inviare un messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) negativo, occupato o positivo.</span><span class="sxs-lookup"><span data-stu-id="edd55-270">The recipient must not send a negative, busy, or positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="edd55-271">Dopo che un'applicazione ha inviato il messaggio di [**\_ \_ terminazione del DDE WM**](wm-dde-terminate.md) al partner in una conversazione DDE, non deve rispondere ai messaggi provenienti da tale partner, perché il partner potrebbe avere eliminato definitivamente la finestra a cui verrebbe inviata la risposta.</span><span class="sxs-lookup"><span data-stu-id="edd55-271">After an application has sent the [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to the partner in a DDE conversation, it must not respond to messages from that partner, since the partner might have destroyed the window to which the response would be sent.</span></span>

<span data-ttu-id="edd55-272">Se un'applicazione riceve un messaggio DDE diverso da [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) dopo la pubblicazione **di \_ WM DDE \_ Terminate**, deve liberare tutti gli oggetti associati ai messaggi ricevuti, ad eccezione degli handle di dati per i [**\_ \_ dati DDE WM**](wm-dde-data.md) o i messaggi [**\_ \_ poke DDE di WM**](wm-dde-poke.md) per i quali **non** è impostato il membro **fRelease** .</span><span class="sxs-lookup"><span data-stu-id="edd55-272">If an application receives a DDE message other than [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) after it has posted **WM\_DDE\_TERMINATE**, it should free all objects associated with the received messages except the data handles for [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_POKE**](wm-dde-poke.md) messages that do **not** have the **fRelease** member set.</span></span>

<span data-ttu-id="edd55-273">Quando un'applicazione sta per terminare, deve terminare tutte le conversazioni DDE attive prima di completare l'elaborazione del messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="edd55-273">When an application is about to terminate, it should end all active DDE conversations before completing processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="edd55-274">Tuttavia, se un'applicazione non termina le conversazioni DDE attive, il sistema interromperà tutte le conversazioni DDE associate a una finestra quando la finestra viene distrutta.</span><span class="sxs-lookup"><span data-stu-id="edd55-274">However, if an application does not end its active DDE conversations, the system will terminate any DDE conversations associated with a window when the window is destroyed.</span></span> <span data-ttu-id="edd55-275">Nell'esempio seguente viene illustrato il modo in cui un'applicazione server termina tutte le conversazioni DDE.</span><span class="sxs-lookup"><span data-stu-id="edd55-275">The following example shows how a server application terminates all DDE conversations.</span></span>


```
void TerminateConversations(hwndServerDDE) 
HWND hwndServerDDE; 
{ 
    HWND hwndClientDDE; 
 
    // Terminate each active conversation. 
 
    while (hwndClientDDE = GetNextLink(hwndClientDDE)) 
    { 
        SendTerminate(hwndServerDDE, hwndClientDDE); 
    } 
    return; 
} 
 
BOOL AtLeastOneLinkActive(VOID) 
{ 
    return TRUE; 
} 
 
HWND GetNextLink(hwndDummy) 
    HWND hwndDummy; 
{ 
    return (HWND) 1; 
} 
 
VOID SendTerminate(HWND hwndServerDDE, HWND hwndClientDDE) 
{ 
    return; 
}
```



 

 