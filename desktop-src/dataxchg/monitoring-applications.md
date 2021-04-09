---
title: Monitoraggio di applicazioni
description: In questo argomento viene illustrato come è possibile utilizzare gli elementi della libreria di gestione Dynamic Data Exchange per creare un'applicazione che monitora l'attività di scambio di dati dinamici nel sistema.
ms.assetid: 6705dc8e-d1e9-4057-9fa2-42cd5cf818af
keywords:
- Interfaccia utente di Windows, Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), monitoraggio delle applicazioni
- DDE (Dynamic Data Exchange), monitoraggio delle applicazioni
- scambio di dati, Dynamic Data Exchange (DDE)
- Interfaccia utente di Windows, libreria di gestione Dynamic Data Exchange (DDEML)
- Libreria di gestione Dynamic Data Exchange (DDEML), monitoraggio delle applicazioni
- DDEML (libreria di gestione Dynamic Data Exchange), monitoraggio delle applicazioni
- scambio di dati, libreria di gestione Dynamic Data Exchange (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f75685d4caa15e519485b2d8b37983faa35366
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044457"
---
# <a name="monitoring-applications"></a><span data-ttu-id="5075d-111">Monitoraggio di applicazioni</span><span class="sxs-lookup"><span data-stu-id="5075d-111">Monitoring Applications</span></span>

<span data-ttu-id="5075d-112">Gli elementi API della libreria di gestione Dynamic Data Exchange (DDEML) possono essere usati per creare un'applicazione che monitora l'attività di Dynamic Data Exchange (DDE) nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5075d-112">The API elements of the Dynamic Data Exchange Management Library (DDEML) can be used to create an application that monitors Dynamic Data Exchange (DDE) activity in the system.</span></span> <span data-ttu-id="5075d-113">Come qualsiasi applicazione DDEML, un'applicazione di monitoraggio DDE contiene una funzione di callback DDE.</span><span class="sxs-lookup"><span data-stu-id="5075d-113">Like any DDEML application, a DDE monitoring application contains a DDE callback function.</span></span> <span data-ttu-id="5075d-114">DDEML notifica a una funzione di callback DDE di un'applicazione di monitoraggio ogni volta che si verifica un evento DDE, passando le informazioni sull'evento alla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="5075d-114">The DDEML notifies a monitoring application's DDE callback function whenever a DDE event occurs, passing information about the event to the callback function.</span></span> <span data-ttu-id="5075d-115">L'applicazione in genere Visualizza le informazioni in una finestra o le scrive in un file.</span><span class="sxs-lookup"><span data-stu-id="5075d-115">The application typically displays the information in a window or writes it to a file.</span></span>

<span data-ttu-id="5075d-116">Per ricevere notifiche da DDEML, un'applicazione deve essere registrata come monitoraggio DDE specificando il \_ flag di monitoraggio APPCLASS in una chiamata alla funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="5075d-116">To receive notifications from the DDEML, an application must have registered as a DDE monitor by specifying the APPCLASS\_MONITOR flag in a call to the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="5075d-117">In questa stessa chiamata, l'applicazione può specificare uno o più flag di monitoraggio per indicare i tipi di eventi per i quali DDEML invia una notifica alla funzione di callback dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5075d-117">In this same call, the application can specify one or more monitor flags to indicate the types of events for which the DDEML is to notify the application's callback function.</span></span> <span data-ttu-id="5075d-118">I flag di monitoraggio seguenti possono essere specificati da un'applicazione:</span><span class="sxs-lookup"><span data-stu-id="5075d-118">The following monitor flags can be specified by an application:</span></span>



| <span data-ttu-id="5075d-119">Flag</span><span class="sxs-lookup"><span data-stu-id="5075d-119">Flag</span></span>          | <span data-ttu-id="5075d-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5075d-120">Description</span></span>                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5075d-121">\_callback MF</span><span class="sxs-lookup"><span data-stu-id="5075d-121">MF\_CALLBACKS</span></span> | <span data-ttu-id="5075d-122">Notifica alla funzione di callback ogni volta che una transazione viene inviata a qualsiasi funzione di callback DDE nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5075d-122">Notifies the callback function whenever a transaction is sent to any DDE callback function in the system.</span></span>                                                                                                                                           |
| <span data-ttu-id="5075d-123">MF \_ conv</span><span class="sxs-lookup"><span data-stu-id="5075d-123">MF\_CONV</span></span>      | <span data-ttu-id="5075d-124">Notifica alla funzione di callback ogni volta che una conversazione viene stabilita o terminata.</span><span class="sxs-lookup"><span data-stu-id="5075d-124">Notifies the callback function whenever a conversation is established or terminated.</span></span>                                                                                                                                                                |
| <span data-ttu-id="5075d-125">\_errori MF</span><span class="sxs-lookup"><span data-stu-id="5075d-125">MF\_ERRORS</span></span>    | <span data-ttu-id="5075d-126">Notifica alla funzione di callback ogni volta che si verifica un errore DDEML.</span><span class="sxs-lookup"><span data-stu-id="5075d-126">Notifies the callback function whenever a DDEML error occurs.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="5075d-127">\_info MF HSZ \_</span><span class="sxs-lookup"><span data-stu-id="5075d-127">MF\_HSZ\_INFO</span></span> | <span data-ttu-id="5075d-128">Notifica la funzione di callback ogni volta che un'applicazione DDEML crea, libera o incrementa il conteggio di utilizzo di un handle di stringa o ogni volta che un handle di stringa viene liberato in seguito a una chiamata alla funzione [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="5075d-128">Notifies the callback function whenever a DDEML application creates, frees, or increments the usage count of a string handle or whenever a string handle is freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> |
| <span data-ttu-id="5075d-129">\_collegamenti MF</span><span class="sxs-lookup"><span data-stu-id="5075d-129">MF\_LINKS</span></span>     | <span data-ttu-id="5075d-130">Notifica alla funzione di callback ogni volta che viene avviato o terminato un ciclo di notifica.</span><span class="sxs-lookup"><span data-stu-id="5075d-130">Notifies the callback function whenever an advise loop is started or ended.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="5075d-131">MF \_ POSTMSGS</span><span class="sxs-lookup"><span data-stu-id="5075d-131">MF\_POSTMSGS</span></span>  | <span data-ttu-id="5075d-132">Notifica alla funzione di callback ogni volta che il sistema o un'applicazione invia un messaggio DDE.</span><span class="sxs-lookup"><span data-stu-id="5075d-132">Notifies the callback function whenever the system or an application posts a DDE message.</span></span>                                                                                                                                                           |
| <span data-ttu-id="5075d-133">MF \_ SENDMSGS</span><span class="sxs-lookup"><span data-stu-id="5075d-133">MF\_SENDMSGS</span></span>  | <span data-ttu-id="5075d-134">Notifica la funzione di callback ogni volta che il sistema o un'applicazione invia un messaggio DDE.</span><span class="sxs-lookup"><span data-stu-id="5075d-134">Notifies the callback function whenever the system or an application sends a DDE message.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="5075d-135">Nell'esempio seguente viene illustrato come registrare un'applicazione di monitoraggio DDE in modo che la funzione di callback DDE riceva le notifiche di tutti gli eventi DDE.</span><span class="sxs-lookup"><span data-stu-id="5075d-135">The following example shows how to register a DDE monitoring application so that its DDE callback function receives notifications of all DDE events.</span></span>


```
DWORD idInst; 
PFNCALLBACK lpDdeProc; 
hInst = hInstance; 
 
if (DdeInitialize( 
        (LPDWORD) &idInst,  // instance identifier 
        DDECallback,        // pointer to callback function 
        APPCLASS_MONITOR |  // this is a monitoring application 
        MF_CALLBACKS     |  // monitor callback functions 
        MF_CONV          |  // monitor conversation data 
        MF_ERRORS        |  // monitor DDEML errors 
        MF_HSZ_INFO      |  // monitor data handle activity 
        MF_LINKS         |  // monitor advise loops 
        MF_POSTMSGS      |  // monitor posted DDE messages 
        MF_SENDMSGS,        // monitor sent DDE messages 
        0))                 // reserved 
{
    return FALSE; 
}
```



<span data-ttu-id="5075d-136">DDEML informa un'applicazione di monitoraggio di un evento DDE inviando una transazione di [**monitoraggio \_ XTYP**](xtyp-monitor.md) alla funzione di callback DDE dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5075d-136">The DDEML informs a monitoring application of a DDE event by sending an [**XTYP\_MONITOR**](xtyp-monitor.md) transaction to the application's DDE callback function.</span></span> <span data-ttu-id="5075d-137">Durante questa transazione, DDEML passa un flag di monitoraggio che specifica il tipo di evento DDE che si è verificato e un handle a un oggetto DDE che contiene informazioni dettagliate sull'evento.</span><span class="sxs-lookup"><span data-stu-id="5075d-137">During this transaction, the DDEML passes a monitor flag that specifies the type of DDE event that has occurred and a handle to a DDE object that contains detailed information about the event.</span></span> <span data-ttu-id="5075d-138">DDEML fornisce un set di strutture che possono essere utilizzate dall'applicazione per estrarre le informazioni dall'oggetto DDE.</span><span class="sxs-lookup"><span data-stu-id="5075d-138">The DDEML provides a set of structures that the application can use to extract the information from the DDE object.</span></span> <span data-ttu-id="5075d-139">Esiste una struttura corrispondente per ogni tipo di evento DDE.</span><span class="sxs-lookup"><span data-stu-id="5075d-139">There is a corresponding structure for each type of DDE event.</span></span>



| <span data-ttu-id="5075d-140">Struttura</span><span class="sxs-lookup"><span data-stu-id="5075d-140">Structure</span></span>                                  | <span data-ttu-id="5075d-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5075d-141">Description</span></span>                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="5075d-142">**MONCBSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="5075d-142">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | <span data-ttu-id="5075d-143">Contiene informazioni su una transazione.</span><span class="sxs-lookup"><span data-stu-id="5075d-143">Contains information about a transaction.</span></span>                         |
| [<span data-ttu-id="5075d-144">**MONCONVSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="5075d-144">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | <span data-ttu-id="5075d-145">Contiene informazioni su una conversazione.</span><span class="sxs-lookup"><span data-stu-id="5075d-145">Contains information about a conversation.</span></span>                        |
| [<span data-ttu-id="5075d-146">**MONERRSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="5075d-146">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | <span data-ttu-id="5075d-147">Contiene informazioni sull'errore DDE più recente.</span><span class="sxs-lookup"><span data-stu-id="5075d-147">Contains information about the latest DDE error.</span></span>                  |
| [<span data-ttu-id="5075d-148">**MONLINKSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="5075d-148">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | <span data-ttu-id="5075d-149">Contiene informazioni su un ciclo di notifica.</span><span class="sxs-lookup"><span data-stu-id="5075d-149">Contains information about an advise loop.</span></span>                        |
| [<span data-ttu-id="5075d-150">**MONHSZSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="5075d-150">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | <span data-ttu-id="5075d-151">Contiene informazioni su un handle di stringa.</span><span class="sxs-lookup"><span data-stu-id="5075d-151">Contains information about a string handle.</span></span>                       |
| [<span data-ttu-id="5075d-152">**MONMSGSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="5075d-152">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | <span data-ttu-id="5075d-153">Contiene informazioni su un messaggio DDE inviato o inviato.</span><span class="sxs-lookup"><span data-stu-id="5075d-153">Contains information about a DDE message that was sent or posted.</span></span> |



 

<span data-ttu-id="5075d-154">Nell'esempio seguente viene illustrata la funzione di callback DDE di un'applicazione di monitoraggio DDE che formatta le informazioni relative a ogni evento di handle di stringa e quindi Visualizza le informazioni in una finestra.</span><span class="sxs-lookup"><span data-stu-id="5075d-154">The following example shows the DDE callback function of a DDE monitoring application that formats information about each string handle event and then displays the information in a window.</span></span> <span data-ttu-id="5075d-155">La funzione utilizza la struttura [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) per estrarre le informazioni dall'oggetto DDE.</span><span class="sxs-lookup"><span data-stu-id="5075d-155">The function uses the [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure to extract the information from the DDE object.</span></span>


```
HDDEDATA CALLBACK DDECallback(uType, uFmt, hconv, hsz1, hsz2, 
    hdata, dwData1, dwData2) 
UINT uType; 
UINT uFmt; 
HCONV hconv; 
HSZ hsz1; 
HSZ hsz2; 
HDDEDATA hdata; 
DWORD dwData1; 
DWORD dwData2; 
{ 
    LPVOID lpData; 
    CHAR *szAction; 
    CHAR szBuf[256]; 
    DWORD cb;
    HRESULT hResult; 
 
    switch (uType) 
    { 
        case XTYP_MONITOR: 
            // Obtain a pointer to the global memory object. 
 
            if (lpData = DdeAccessData(hdata, &cb)) 
            { 
                // Examine the monitor flag. 
 
                switch (dwData2) 
                { 
                    case MF_HSZ_INFO: 
 
#define PHSZS ((MONHSZSTRUCT *)lpData) 
 
                        // The global memory object contains 
                        // string handle data. Use the MONHSZSTRUCT 
                        // structure to access the data. 
 
                        switch (PHSZS->fsAction) 
                        { 
                            // Examine the action flags to determine
                            // the action performed on the handle.
 
                            case MH_CREATE: 
                                szAction = "Created"; 
                                break; 
 
                            case MH_KEEP: 
                                szAction = "Incremented"; 
                                break; 
 
                            case MH_DELETE: 
                                szAction = "Deleted"; 
                                break; 
 
                            case MH_CLEANUP: 
                                szAction = "Cleaned up"; 
                                break; 
 
                            default: 
                                DdeUnaccessData(hdata); 
                                return (HDDEDATA) 0; 
                        } 
 
                        // Write formatted output to a buffer. 
                        hResult = StringCchPrintf(szBuf, 256/sizeof(TCHAR),
                            "Handle %s, Task: %x, Hsz: %lx(%s)", 
                            (LPSTR) szAction, PHSZS->hTask, 
                            PHSZS->hsz, (LPSTR) PHSZS->str);
                        if (FAILED(hResult))
                        {
                        // TO DO: Write error handler.
                            return;
                        } 
                        // Display text or write to a file. 
 
                        break; 
 
#undef PHSZS 
 
                    // Process other MF_* flags. 
 
                    default: 
                        break; 
                } 
            } 
 
            // Free the global memory object. 
 
            DdeUnaccessData(hdata); 
            break; 
 
        default: 
            break; 
    } 
    return (HDDEDATA) 0; 
} 
```



 

 




