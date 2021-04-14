---
title: Spostamento tra i riquadri attività del servizio
description: Spostamento tra i riquadri attività del servizio
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player Online Stores, spostamento
- negozi online, esplorazione
- digitare 2 archivi online, spostamento
- Windows Media Player Online Stores, riquadri attività servizio
- archivi online, riquadri attività del servizio
- digitare 2 archivi online, riquadri attività servizio
- Windows Media Player Online Stores, riquadri attività
- archivi online, riquadri attività
- digitare 2 archivi online, riquadri attività
- spostamento nei negozi online di tipo 2
- Media Player di Windows, riquadri attività servizio
- Media Player di Windows, riquadri attività
- riquadri attività servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035215f822c67bb40c528f141422977efc8653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329980"
---
# <a name="navigating-between-service-task-panes"></a><span data-ttu-id="d7908-116">Spostamento tra i riquadri attività del servizio</span><span class="sxs-lookup"><span data-stu-id="d7908-116">Navigating between Service Task Panes</span></span>

<span data-ttu-id="d7908-117">Per spostarsi tra i riquadri attività del servizio in Windows Media Player, utilizzare il metodo **NavigateTaskPaneURL** , disponibile tramite l'oggetto **Window. External** .</span><span class="sxs-lookup"><span data-stu-id="d7908-117">To navigate between service task panes in Windows Media Player, you use the **NavigateTaskPaneURL** method, which is available by using the **window.external** object.</span></span> <span data-ttu-id="d7908-118">Quando si usa questo metodo, si specificano i valori per tre parametri:</span><span class="sxs-lookup"><span data-stu-id="d7908-118">When you use this method, you specify values for three parameters:</span></span>

-   <span data-ttu-id="d7908-119">*bstrKeyName*.</span><span class="sxs-lookup"><span data-stu-id="d7908-119">*bstrKeyName*.</span></span> <span data-ttu-id="d7908-120">Si tratta del nome della chiave dell'archivio online.</span><span class="sxs-lookup"><span data-stu-id="d7908-120">This is the key name of the online store.</span></span> <span data-ttu-id="d7908-121">Quando si esegue la navigazione all'interno di un archivio online, usare il nome della chiave dell'archivio corrente.</span><span class="sxs-lookup"><span data-stu-id="d7908-121">When navigating within an online store, use the key name of the current store.</span></span>
-   <span data-ttu-id="d7908-122">*bstrTaskPane*.</span><span class="sxs-lookup"><span data-stu-id="d7908-122">*bstrTaskPane*.</span></span> <span data-ttu-id="d7908-123">Questa stringa contiene il nome del riquadro attività del servizio in cui si desidera spostarsi.</span><span class="sxs-lookup"><span data-stu-id="d7908-123">This string contains the name of the service task pane to which you want to navigate.</span></span>
-   <span data-ttu-id="d7908-124">*bstrParams*.</span><span class="sxs-lookup"><span data-stu-id="d7908-124">*bstrParams*.</span></span> <span data-ttu-id="d7908-125">Questa stringa contiene i parametri della stringa di query che si desidera aggiungere all'URL per la pagina Web ospitata dal riquadro attività del servizio in cui si desidera spostarsi.</span><span class="sxs-lookup"><span data-stu-id="d7908-125">This string contains the query string parameters you want to append to the URL for the webpage hosted by the service task pane to which you want to navigate.</span></span>

<span data-ttu-id="d7908-126">La navigazione viene gestita da una pagina Web creata, denominata pagina Navigate.</span><span class="sxs-lookup"><span data-stu-id="d7908-126">Navigation is managed by a webpage you create, called the navigate page.</span></span> <span data-ttu-id="d7908-127">L'URL della pagina Navigate viene specificato dall'elemento **Navigate** nel documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="d7908-127">The URL for the navigate page is specified by the **Navigate** element in the ServiceInfo document.</span></span> <span data-ttu-id="d7908-128">Quando si chiama **NavigateTaskPaneURL**, Windows Media Player apre la pagina Navigate, non la pagina Web specificata dagli elementi **ServiceTask1**, **ServiceTask2** o **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="d7908-128">When you call **NavigateTaskPaneURL**, Windows Media Player opens the navigate page, not the webpage specified by the **ServiceTask1**, **ServiceTask2**, or **ServiceTask3** elements.</span></span> <span data-ttu-id="d7908-129">Si tratta della pagina Navigate che riceve la stringa di query specificata da *bstrParams*.</span><span class="sxs-lookup"><span data-stu-id="d7908-129">It is the navigate page that receives the query string specified by *bstrParams*.</span></span> <span data-ttu-id="d7908-130">La pagina Navigate deve contenere le regole che determinano quale contenuto viene visualizzato in un riquadro attività del servizio dopo lo spostamento.</span><span class="sxs-lookup"><span data-stu-id="d7908-130">The navigate page should contain the rules that determine which content displays in a service task pane after navigation.</span></span>

<span data-ttu-id="d7908-131">Si supponga, ad esempio, di voler fare in modo che gli utenti clicchino su un collegamento per passare da **ServiceTask1** a **ServiceTask2**.</span><span class="sxs-lookup"><span data-stu-id="d7908-131">For example, suppose you want users to click a link to navigate from **ServiceTask1** to **ServiceTask2**.</span></span> <span data-ttu-id="d7908-132">Per creare il collegamento, è possibile usare il codice HTML seguente:</span><span class="sxs-lookup"><span data-stu-id="d7908-132">You could use the following HTML to create the link:</span></span>


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



<span data-ttu-id="d7908-133">Quando l'utente fa clic sul collegamento video, Windows Media Player passa a **ServiceTask2** e apre la pagina Navigate, aggiungendo la stringa di query seguente al relativo URL.</span><span class="sxs-lookup"><span data-stu-id="d7908-133">When the user clicks the Video link, Windows Media Player switches to **ServiceTask2** and opens the navigate page, appending the following query string to its URL.</span></span>


```C++
?From=Music&To=2

```



<span data-ttu-id="d7908-134">Il parametro from identifica la pagina dalla quale l'utente ha fatto clic sul collegamento e il parametro to identifica il numero del riquadro attività del servizio a cui vuole spostarsi.</span><span class="sxs-lookup"><span data-stu-id="d7908-134">The From parameter identifies the page from which the user clicked the link and the To parameter identifies the number of the service task pane to which he or she wants to navigate.</span></span> <span data-ttu-id="d7908-135">Si noti che non c'è niente di speciale su questi parametri.</span><span class="sxs-lookup"><span data-stu-id="d7908-135">(Note that there is nothing special about these parameters.</span></span> <span data-ttu-id="d7908-136">È possibile usare tutti i parametri desiderati per qualsiasi scopo.</span><span class="sxs-lookup"><span data-stu-id="d7908-136">You can use any parameters you like for any purpose you choose.)</span></span>

<span data-ttu-id="d7908-137">Ad esempio, il codice di esempio seguente mostra l'elemento **Navigate** in un documento ServiceInfo:</span><span class="sxs-lookup"><span data-stu-id="d7908-137">For instance, the following example code shows the **Navigate** element in a ServiceInfo document:</span></span>


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



<span data-ttu-id="d7908-138">L'URL risultante, completo con la stringa di query, è illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="d7908-138">The resulting URL, complete with query string, is shown in the following example:</span></span>


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



<span data-ttu-id="d7908-139">Il codice di esempio seguente mostra la pagina Navigate:</span><span class="sxs-lookup"><span data-stu-id="d7908-139">The following example code shows the navigate page:</span></span>


```C++
<%
    Dim sURL
    Dim sQS
    Dim sTo

    sURL = ""
    sQS = Request.ServerVariables("QUERY_STRING")
    sTo = "" & Request.QueryString("To")
 
    Select Case sTo
       Case "1" sURL = sURL & "Music_Music.asp"
       Case "2" sURL = sURL & "Music_Video.asp"
       Case "3" sURL = sURL & "Music_Radio.asp"
       Case Else sURL = sURL & "Music_Music.asp"
    End Select
     
    sURL = sURL & "?" & sQS

    Response.Redirect(sURL)    
%>

```



<span data-ttu-id="d7908-140">Il codice precedente crea semplicemente un URL e ne reindirizza il browser.</span><span class="sxs-lookup"><span data-stu-id="d7908-140">The preceding code simply creates a URL and redirects the browser to it.</span></span> <span data-ttu-id="d7908-141">In primo luogo, il codice recupera i valori dalla stringa di query dell'URL e dalla stringa di query stessa.</span><span class="sxs-lookup"><span data-stu-id="d7908-141">First, the code retrieves To values from the URL query string and the query string itself.</span></span> <span data-ttu-id="d7908-142">Usa il valore del parametro to per determinare la pagina da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="d7908-142">It uses the value of the To parameter to determine which page to display.</span></span> <span data-ttu-id="d7908-143">Viene quindi aggiunta la stringa di query originale all'URL.</span><span class="sxs-lookup"><span data-stu-id="d7908-143">It then appends the original query string to the URL.</span></span> <span data-ttu-id="d7908-144">Infine, Esplora il browser usando un URL simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="d7908-144">Finally, it navigates the browser using a URL similar to the following:</span></span>


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



<span data-ttu-id="d7908-145">Quando si esegue la navigazione in questo modo, assicurarsi di specificare [External. SelectedTaskPane](external-selectedtaskpane.md) per assicurarsi che il pulsante attività corretto sia evidenziato.</span><span class="sxs-lookup"><span data-stu-id="d7908-145">Whenever you perform navigation in this manner, be sure to specify [External.SelectedTaskPane](external-selectedtaskpane.md) to ensure that the correct task button is highlighted.</span></span>

-   <span data-ttu-id="d7908-146">**Avviso** di Prestare attenzione all'uso dei parametri della stringa di query per la navigazione.</span><span class="sxs-lookup"><span data-stu-id="d7908-146">**Warning** Be careful how you use query string parameters for navigation.</span></span>

<span data-ttu-id="d7908-147">Le pagine Web di HTMLView possono essere fornite da chiunque crei una playlist ASX.</span><span class="sxs-lookup"><span data-stu-id="d7908-147">HTMLView webpages can be provided by anyone who creates an ASX playlist.</span></span> <span data-ttu-id="d7908-148">Ciò significa che i siti Web dannosi possono passare i valori della stringa di query allo Store online usando **NavigateTaskPaneURL**.</span><span class="sxs-lookup"><span data-stu-id="d7908-148">This means that malicious websites can pass query string values to your online store using **NavigateTaskPaneURL**.</span></span> <span data-ttu-id="d7908-149">È necessario pianificare questa possibilità per garantire la protezione del proprio negozio online.</span><span class="sxs-lookup"><span data-stu-id="d7908-149">You must plan for this possibility to keep your online store secure.</span></span> <span data-ttu-id="d7908-150">Ad esempio, se l'archivio online Visualizza semplicemente un valore della stringa di query per l'utente, un sito Web dannoso potrebbe visualizzare un testo imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d7908-150">For example, if your online store simply displays a query string value to the user, a malicious website could display unexpected text.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7908-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7908-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7908-152">**Visualizzazione di pagine Web in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="d7908-152">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="d7908-153">**Navigate-elemento**</span><span class="sxs-lookup"><span data-stu-id="d7908-153">**Navigate Element**</span></span>](navigate-element.md)
</dt> <dt>

[<span data-ttu-id="d7908-154">**Navigazione per i negozi di tipo 2 online**</span><span class="sxs-lookup"><span data-stu-id="d7908-154">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




