---
title: Gestione delle informazioni sulla sessione
description: Gestione delle informazioni sulla sessione
ms.assetid: 2ab862dc-62e1-44d6-ac81-7d3c574a779f
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player Online Stores, gestione delle informazioni sulla sessione
- archivi online, gestione delle informazioni sulla sessione
- digitare 2 archivi online, gestione delle informazioni sulla sessione
- Windows Media Player Online Stores, informazioni sulla sessione
- archivi online, informazioni sulla sessione
- digitare 2 archivi online, informazioni sulla sessione
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
- gestione delle informazioni sulla sessione
- informazioni sulla sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786892afebb26f64a97b300bd1a4bd7c46d44883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332679"
---
# <a name="maintaining-session-information"></a><span data-ttu-id="e6e54-117">Gestione delle informazioni sulla sessione</span><span class="sxs-lookup"><span data-stu-id="e6e54-117">Maintaining Session Information</span></span>

## <a name="how-the-sample-stores-information"></a><span data-ttu-id="e6e54-118">Come archiviare le informazioni nell'esempio</span><span class="sxs-lookup"><span data-stu-id="e6e54-118">How the Sample Stores Information</span></span>

<span data-ttu-id="e6e54-119">La pagina Web di esempio gestisce i dati tramite cookie.</span><span class="sxs-lookup"><span data-stu-id="e6e54-119">The sample webpage maintains data by using cookies.</span></span> <span data-ttu-id="e6e54-120">I cookie sono semplicemente coppie nome/valore permanenti che possono essere archiviate dal Web browser.</span><span class="sxs-lookup"><span data-stu-id="e6e54-120">Cookies are simply persistent name/value pairs that the Web browser can store for you.</span></span>

<span data-ttu-id="e6e54-121">Quando la pagina Web si chiude, viene eseguita la funzione **Shutdown** .</span><span class="sxs-lookup"><span data-stu-id="e6e54-121">When the webpage closes, the **Shutdown** function runs.</span></span> <span data-ttu-id="e6e54-122">**Shutdown** chiama la funzione **SetPendingCookies**.</span><span class="sxs-lookup"><span data-stu-id="e6e54-122">**Shutdown** calls the function **SetPendingCookies**.</span></span> <span data-ttu-id="e6e54-123">Questa funzione esegue il ciclo dell'elenco di raccolta di download, archiviato nella casella di riepilogo a discesa denominata selDLC.</span><span class="sxs-lookup"><span data-stu-id="e6e54-123">This function loops through the download collection list, stored in the drop-down list box named selDLC.</span></span> <span data-ttu-id="e6e54-124">Se una raccolta di download contiene elementi incompleti, la funzione chiama il metodo **Secookie**, passando un nome e un valore.</span><span class="sxs-lookup"><span data-stu-id="e6e54-124">If a download collection contains incomplete items, the function calls the method **SetCookie**, passing a name and a value.</span></span> <span data-ttu-id="e6e54-125">La stringa del nome viene determinata aggiungendo un valore integer a un valore costante, **WMPDLC**, archiviato nella variabile denominata g \_ sPreCookie.</span><span class="sxs-lookup"><span data-stu-id="e6e54-125">The name string is determined by appending an integer value to a constant value, **WMPDLC**, which is stored in the variable named g\_sPreCookie.</span></span> <span data-ttu-id="e6e54-126">Per la terza raccolta di download in sospeso, ad esempio, il nome del cookie sarà "WMPDLC2", perché il meccanismo di conteggio è in base zero.</span><span class="sxs-lookup"><span data-stu-id="e6e54-126">For instance, for the third pending download collection, the cookie name would be "WMPDLC2", because the counting mechanism is zero-based.</span></span> <span data-ttu-id="e6e54-127">Quando ogni cookie viene creato, la funzione incrementa la variabile globale g \_ in sospeso per contenere un conteggio dei download in sospeso.</span><span class="sxs-lookup"><span data-stu-id="e6e54-127">As each cookie is created, the function increments the global variable g\_Pending to keep a count of pending downloads.</span></span> <span data-ttu-id="e6e54-128">Il codice viene riprodotto qui per praticità:</span><span class="sxs-lookup"><span data-stu-id="e6e54-128">The code is reproduced here for your convenience:</span></span>


```C++
// Write cookies for pending downloads.
function SetPendingCookies()
{
    g_Pending = 0; // Init the pending count.
    
    for(var i = 0; i < selDLC.length; i++)
    {
        var sCookieName = g_sPreCookie + i.toString(10);
        var sCookieVal = selDLC.options[i].text;
    
        // Write a cookie for each pending download.    
        if(IsDLCComplete(sCookieVal.valueOf()) == false)
        {      
            SetCookie(sCookieName, sCookieVal);
            g_Pending++;
        }        
    }
}

```



<span data-ttu-id="e6e54-129">**IsDLCComplete** è una funzione di supporto che esegue semplicemente il ciclo di ogni elemento di download nella raccolta di download per determinare se un elemento è in sospeso.</span><span class="sxs-lookup"><span data-stu-id="e6e54-129">**IsDLCComplete** is a helper function that simply loops through each download item in the download collection to determine whether any item is pending.</span></span> <span data-ttu-id="e6e54-130">Se è presente un elemento in sospeso, la funzione restituisce false.</span><span class="sxs-lookup"><span data-stu-id="e6e54-130">If there is a pending item, the function returns false.</span></span>

<span data-ttu-id="e6e54-131">**Secookie** è la funzione che crea il cookie.</span><span class="sxs-lookup"><span data-stu-id="e6e54-131">**SetCookie** is the function that creates the cookie.</span></span>

<span data-ttu-id="e6e54-132">Quando **SetPendingCookies** restituisce, **Shutdown** crea il cookie di conteggio, che archivia il valore dalla variabile g \_ in sospeso.</span><span class="sxs-lookup"><span data-stu-id="e6e54-132">When **SetPendingCookies** returns, **Shutdown** creates the count cookie, which stores the value from the variable g\_Pending.</span></span> <span data-ttu-id="e6e54-133">Questo valore è importante perché la pagina Web richiede un modo per determinare il numero di cookie da recuperare quando viene ricaricato.</span><span class="sxs-lookup"><span data-stu-id="e6e54-133">This value is important because the webpage needs a way to determine how many cookies to retrieve when it reloads.</span></span> <span data-ttu-id="e6e54-134">Il nome del cookie di conteggio viene archiviato nella variabile denominata g \_ sCountCookie.</span><span class="sxs-lookup"><span data-stu-id="e6e54-134">The count cookie name is stored in the variable named g\_sCountCookie.</span></span>

## <a name="how-the-sample-retrieves-information"></a><span data-ttu-id="e6e54-135">Come vengono recuperate le informazioni nell'esempio</span><span class="sxs-lookup"><span data-stu-id="e6e54-135">How the Sample Retrieves Information</span></span>

<span data-ttu-id="e6e54-136">Quando viene caricata la pagina Web, viene eseguita la funzione **init** .</span><span class="sxs-lookup"><span data-stu-id="e6e54-136">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="e6e54-137">Per prima cosa, la funzione chiama **GetPendingDlCount** per recuperare il cookie di conteggio.</span><span class="sxs-lookup"><span data-stu-id="e6e54-137">First, the function calls **GetPendingDlCount** to retrieve the count cookie.</span></span> <span data-ttu-id="e6e54-138">Quindi Archivia questo valore nella variabile denominata g \_ in sospeso.</span><span class="sxs-lookup"><span data-stu-id="e6e54-138">Next, it stores this value in the variable named g\_Pending.</span></span> <span data-ttu-id="e6e54-139">Chiama quindi la funzione **PopulateDLList** per recuperare ogni cookie della sessione di download e aggiungere il relativo identificatore alla casella di riepilogo a discesa.</span><span class="sxs-lookup"><span data-stu-id="e6e54-139">Then it calls the **PopulateDLList** function to retrieve each download session cookie and add its identifier to the drop-down list box.</span></span> <span data-ttu-id="e6e54-140">Ecco il codice per la funzione:</span><span class="sxs-lookup"><span data-stu-id="e6e54-140">Here is the code for that function:</span></span>


```C++
// Fill the drop-down list with pending download collection IDs.
function PopulateDlList(iCount)
{
    ClearList(selDLC);
     
    // For each cookie, add the value to the SELECT element.
    // The value represents a download collection ID.  
    for (var j = 0; j < iCount; j++)
    {
        var sCookieName = g_sPreCookie + j.toString(10);        
        var sCookieVal = GetCookie(sCookieName);
        DelCookie(sCookieName); // Don't leave the cookies lying around. 
  
        if(sCookieVal != null)
        {      
            var oOption = document.createElement("OPTION");
            oOption.text = sCookieVal;
            oOption.value = j;
            selDLC.add(oOption); 
        }          
    }
}

```



<span data-ttu-id="e6e54-141">La funzione **Clear** list rimuove tutti gli elementi dalla casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e6e54-141">The function **ClearList** removes all items from the list box.</span></span>

<span data-ttu-id="e6e54-142">La funzione immette quindi un ciclo.</span><span class="sxs-lookup"><span data-stu-id="e6e54-142">The function then enters a loop.</span></span> <span data-ttu-id="e6e54-143">Ogni nome di cookie viene compilato come stringa e quindi il cookie viene recuperato chiamando la funzione helper **GetCookie**.</span><span class="sxs-lookup"><span data-stu-id="e6e54-143">Each cookie name is built as a string, and then the cookie is retrieved by calling the helper function **GetCookie**.</span></span> <span data-ttu-id="e6e54-144">Una volta recuperato, il cookie viene eliminato chiamando **DelCookie**.</span><span class="sxs-lookup"><span data-stu-id="e6e54-144">Once retrieved, the cookie is deleted by calling **DelCookie**.</span></span> <span data-ttu-id="e6e54-145">Se il cookie ha un valore, il valore viene aggiunto alla casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e6e54-145">If the cookie has a value, the value is added to the list box.</span></span> <span data-ttu-id="e6e54-146">Questa azione avvia l'evento **OnChange** per l'elenco selDLC, che a sua volta chiama la funzione di gestione denominata **OnSelectDLC**.</span><span class="sxs-lookup"><span data-stu-id="e6e54-146">This action initiates the **onChange** event for the selDLC list, which in turn calls the handler function named **OnSelectDLC**.</span></span> <span data-ttu-id="e6e54-147">Si tratta della stessa funzione che viene eseguita quando l'utente seleziona una raccolta di download; si tratta del codice che compila la casella di riepilogo Scarica elemento.</span><span class="sxs-lookup"><span data-stu-id="e6e54-147">This is the same function that executes when the user selects a download collection; it is the code that fills the download item list box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6e54-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6e54-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6e54-149">**Uso di Download Manager**</span><span class="sxs-lookup"><span data-stu-id="e6e54-149">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




