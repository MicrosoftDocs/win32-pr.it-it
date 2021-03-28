---
description: A partire da Windows Vista, la visualizzazione delle categorie del pannello di controllo fornisce collegamenti alle attività sotto ogni icona dell'elemento del pannello di controllo, come illustrato qui.
ms.assetid: 54a03536-6fe6-4304-a555-58e5bca128b9
title: Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4e98e8a6e07f84e8012b58cefe8e0d249fc069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878770"
---
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a><span data-ttu-id="5bc3c-103">Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="5bc3c-103">Creating Searchable Task Links for a Control Panel Item</span></span>

<span data-ttu-id="5bc3c-104">A partire da Windows Vista, la visualizzazione delle categorie del pannello di controllo fornisce collegamenti alle attività sotto ogni icona dell'elemento del pannello di controllo, come illustrato qui.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-104">As of Windows Vista, the Control Panel category view provides task links beneath each Control Panel item's icon as shown here.</span></span>

![collegamenti alle attività nella pagina della categoria sistema e manutenzione](images/controlpaneltasklinks.png)

<span data-ttu-id="5bc3c-106">Quando un utente immette testo nella casella di **ricerca** nella parte superiore destra della finestra, i risultati della ricerca includono i collegamenti delle attività indicati di seguito per una ricerca nella parola "display".</span><span class="sxs-lookup"><span data-stu-id="5bc3c-106">When a user enters text in the **Search** box in the upper right of the window, the search results include these task links as shown here for a search on the word "display".</span></span>

![collegamenti alle attività nei risultati della ricerca del pannello di controllo](images/controlpanelsearchresults.png)

<span data-ttu-id="5bc3c-108">In questo argomento vengono trattati i seguenti temi:</span><span class="sxs-lookup"><span data-stu-id="5bc3c-108">This topic discusses the following:</span></span>

-   [<span data-ttu-id="5bc3c-109">Procedure consigliate per il collegamento alle attività</span><span class="sxs-lookup"><span data-stu-id="5bc3c-109">Task Link Best Practices</span></span>](#task-link-best-practices)
-   [<span data-ttu-id="5bc3c-110">Creazione di un file XML di attività</span><span class="sxs-lookup"><span data-stu-id="5bc3c-110">Creating a Task XML File</span></span>](#creating-a-task-xml-file)
-   [<span data-ttu-id="5bc3c-111">Localizzazione di collegamenti alle attività</span><span class="sxs-lookup"><span data-stu-id="5bc3c-111">Localizing Task Links</span></span>](#localizing-task-links)
-   [<span data-ttu-id="5bc3c-112">Parole chiave e ricerca</span><span class="sxs-lookup"><span data-stu-id="5bc3c-112">Keywords and Searching</span></span>](#keywords-and-searching)
-   [<span data-ttu-id="5bc3c-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5bc3c-113">Related topics</span></span>](#related-topics)

## <a name="task-link-best-practices"></a><span data-ttu-id="5bc3c-114">Procedure consigliate per il collegamento alle attività</span><span class="sxs-lookup"><span data-stu-id="5bc3c-114">Task Link Best Practices</span></span>

<span data-ttu-id="5bc3c-115">È consigliabile fornire collegamenti alle attività per gli elementi del pannello di controllo come supporto per gli utenti che cercano funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-115">It is recommended that you provide task links for your Control Panel items as an aid to users searching for functionality.</span></span> <span data-ttu-id="5bc3c-116">È anche possibile aggiungere parole chiave ai collegamenti alle attività in modo che un utente possa trovarle anche senza conoscere il titolo o la terminologia di un'attività.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-116">It is also possible to add keywords to the task links so that a user can find them even without knowing a task's title or terminology.</span></span>

<span data-ttu-id="5bc3c-117">I collegamenti alle attività migliori servono tre scopi:</span><span class="sxs-lookup"><span data-stu-id="5bc3c-117">The best task links serve three purposes:</span></span>

1.  <span data-ttu-id="5bc3c-118">Consente di specificare un collegamento alla funzionalità dell'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-118">Provide a shortcut to the functionality of the Control Panel item.</span></span>
2.  <span data-ttu-id="5bc3c-119">Fornire parole chiave in modo che gli utenti possano eseguire ricerche usando la propria lingua.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-119">Provide keywords so that users can search using their own language.</span></span> <span data-ttu-id="5bc3c-120">Un utente potrebbe voler digitare "compattazione" perché conosce il termine tecnico.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-120">A user may want to type "compaction" because he or she knows the technical term.</span></span> <span data-ttu-id="5bc3c-121">Un utente può digitare "DB troppo grande" o "database Filesize".</span><span class="sxs-lookup"><span data-stu-id="5bc3c-121">A user may type "DB too big", or "database filesize".</span></span> <span data-ttu-id="5bc3c-122">L'aggiunta di parole chiave appropriate all'attività significa che gli utenti possono trovare l'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-122">Adding suitable keywords to the task means that users can find your Control Panel item.</span></span>
3.  <span data-ttu-id="5bc3c-123">Fornire suggerimenti sull'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-123">Provide hints about what the Control Panel item does.</span></span> <span data-ttu-id="5bc3c-124">Quando un utente Visualizza i collegamenti sotto l'icona di un elemento del pannello di controllo, può ottenere ulteriori informazioni sull'elemento utilizzato dal pannello di controllo, oltre al nome e all'icona che possono essere forniti da soli.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-124">When a user sees the links beneath a Control Panel item's icon, they can get more information about what the Control Panel item is used for than the name and icon alone can provide.</span></span>

<span data-ttu-id="5bc3c-125">I collegamenti alle attività devono essere mirati all'utente finale, non alla tecnologia o alla funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-125">Task links should be end-user focused, not technology- or feature-focused.</span></span> <span data-ttu-id="5bc3c-126">Ad esempio, la "Abilitazione della compattazione del database" potrebbe non essere una formulazione valida perché si tratta di un gergo tecnico non noto alla maggior parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-126">For example, "Enable database compaction" would be bad wording because it is technical jargon unfamiliar to the majority of users.</span></span> <span data-ttu-id="5bc3c-127">"Rendere il file di database più piccolo" è preferibile perché menziona l'obiettivo finale effettivo dell'utente anziché il meccanismo per ottenerlo.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-127">"Make my database file smaller" is better because it mentions the user's actual end goal rather than the mechanism to get there.</span></span> <span data-ttu-id="5bc3c-128">L'obiettivo non è quello di semplificare eccessivamente, ma piuttosto di formulare l'attività in termini di ciò che l'utente desidera eseguire.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-128">The goal is not to oversimplify, but rather to phrase the task in terms of what the user wants to accomplish.</span></span>

## <a name="creating-a-task-xml-file"></a><span data-ttu-id="5bc3c-129">Creazione di un file XML di attività</span><span class="sxs-lookup"><span data-stu-id="5bc3c-129">Creating a Task XML File</span></span>

<span data-ttu-id="5bc3c-130">I collegamenti alle attività sono definiti in un file XML.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-130">Task links are defined in an XML file.</span></span> <span data-ttu-id="5bc3c-131">In questa sezione vengono forniti i dettagli di un file XML di esempio che definisce tre collegamenti alle attività per un elemento del pannello di controllo denominato **blocco note**.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-131">This section provides the details of an example .xml file that defines three task links for a Control Panel item called **Notepad**.</span></span> <span data-ttu-id="5bc3c-132">Definisce i titoli, le parole chiave e le righe di comando per i collegamenti alle attività.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-132">It defines titles, keywords, and the command lines for the task links.</span></span> <span data-ttu-id="5bc3c-133">Viene inoltre illustrato come specificare quali collegamenti alle attività vengono visualizzati nella categoria.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-133">It also illustrates how to specify which task links appear under which category.</span></span> <span data-ttu-id="5bc3c-134">Un elemento del pannello di controllo registrato per essere visualizzato in più di una categoria consente di visualizzare collegamenti diversi a seconda della categoria.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-134">A Control Panel item that is registered to appear in more than one category has the option of showing different links depending on the category.</span></span> <span data-ttu-id="5bc3c-135">Le spiegazioni dei vari elementi e delle informazioni fornite vengono fornite come commenti nel codice XML stesso.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-135">Explanations of the various elements and information provided are given as comments in the XML itself.</span></span>


```
<?xml version="1.0" ?>
<applications xmlns="http://schemas.microsoft.com/windows/cpltasks/v1" 
              xmlns:sh="http://schemas.microsoft.com/windows/tasks/v1">
    
    <!-- Notepad -->
    <application id="{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}"> 
    <!-- This GUID must match the GUID you created for your Control Panel item,
         and registered in namespace -->
    
        <!-- Solitaire -->
        <sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
            <!-- This is a generated GUID, specific to this task link -->
            <sh:name>Play solitaire</sh:name>
            <sh:keywords>solitare;game;cards;ace;diamond;heart;club;single</sh:keywords>
            <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
        </sh:task>

        <!-- Task Manager -->
        <sh:task id="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}" needsElevation="true"> 
            <!-- This is a generated GUID, specific to this task link -->
            <!-- The needsElevation="true" attribute means that the task 
                 appears with a shield icon next to it. Adding this attribute 
                 does not cause the .exe to require elevation - it just adds an 
                 icon to tell users that the command already requires it -->
            <sh:name>See running processes</sh:name>
            <sh:keywords>taskmgr;taskman;running processes;threads;cpu;</sh:keywords>
            <sh:command>taskmgr.exe</sh:command>
        </sh:task>

        <!-- IE -->
        <sh:task id="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}">
            <sh:name>Open Internet Explorer</sh:name>
            <sh:keywords>IE;web;browser;net;Internet;ActiveX;plug-in;plugin</sh:keywords>
            <sh:command>iexplore.exe</sh:command>
        </sh:task>
        
        <!-- Category assignments -->

        <!-- Appearance and Personalization -->
        <category id="1"> 
        <!-- These idref attributes refer to the GUIDs of the tasks defined above. A maximum of five tasks are shown per category. -->
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"/>   
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
        </category>
        
        <!-- Programs -->
        <category id="8"> 
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}">
                <sh:name>Click here to play</sh:name>
                <!-- This overrides the defined text. When the Notepad Control 
                     Panel item appears in the Programs category, it uses the 
                     "Click here to play" text for this Solitaire link, instead 
                     of "Play solitaire". -->
            </sh:task>
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
       </category>
   </application>
</applications>
```



> [!Note]  
> <span data-ttu-id="5bc3c-136">A partire da Windows 7, un elemento del pannello di controllo può essere identificato dal relativo nome canonico anziché dal nome eseguibile: è possibile usare l'elemento **<SH: controlpanel>** al posto di **<sh: Command>**.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-136">As of Windows 7, a Control Panel item can be identified by its canonical name rather than its executable name: the **<sh:controlpanel>** element can be used in place of **<sh:command>**.</span></span> <span data-ttu-id="5bc3c-137">L'elemento **<SH: controlpanel>** fornisce anche un attributo per specificare la pagina dell'elemento a cui deve essere aperto.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-137">The **<sh:controlpanel>** element also provides an attribute to specify the page of the item to which it should open.</span></span> <span data-ttu-id="5bc3c-138">Di seguito viene illustrato un esempio dell'elemento **<SH: controlpanel>** :</span><span class="sxs-lookup"><span data-stu-id="5bc3c-138">The following shows an example of the **<sh:controlpanel>** element:</span></span>

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a><span data-ttu-id="5bc3c-139">Localizzazione di collegamenti alle attività</span><span class="sxs-lookup"><span data-stu-id="5bc3c-139">Localizing Task Links</span></span>

<span data-ttu-id="5bc3c-140">Il testo per i titoli e le parole chiave dei collegamenti alle attività può essere archiviato in una tabella di stringhe nel modulo dell'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-140">The text for the task links' titles and keywords can be stored in a string table in the Control Panel item's module.</span></span> <span data-ttu-id="5bc3c-141">In tal caso, il formato utilizzato nel file XML diventa:</span><span class="sxs-lookup"><span data-stu-id="5bc3c-141">In that case, the format used in the XML file becomes:</span></span>


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



<span data-ttu-id="5bc3c-142">In questo esempio, il testo per il nome dell'attività viene visualizzato nell'ID risorsa stringa 100 in myTextResources.dll e il testo per le parole chiave viene visualizzato in stringa ID 101.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-142">In this example, the text for the task's name appears in string resource ID 100 in myTextResources.dll, and the text for the keywords appears in string resource ID 101.</span></span>

## <a name="keywords-and-searching"></a><span data-ttu-id="5bc3c-143">Parole chiave e ricerca</span><span class="sxs-lookup"><span data-stu-id="5bc3c-143">Keywords and Searching</span></span>

<span data-ttu-id="5bc3c-144">La ricerca nel pannello di controllo consente di trovare i collegamenti alle attività in base al nome e anche alle parole chiave corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-144">The Control Panel search finds task links based on their name and also on their keywords.</span></span> <span data-ttu-id="5bc3c-145">Corrisponde a ogni parola nella ricerca con il prefisso delle parole nel nome e nelle parole chiave.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-145">It matches each word in the search with the prefix of words in the name and keywords.</span></span> <span data-ttu-id="5bc3c-146">Ad esempio, la stringa di query "CPU" corrisponderà all'attività "vedere processi in esecuzione" nell'esempio precedente perché "CPU" si trova nell'elenco di parole chiave.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-146">For example, the query string "cpu" would match the task "See running processes" in the earlier example because "cpu" is in the keyword list.</span></span> <span data-ttu-id="5bc3c-147">La stringa di query "Pro" troverà anche il risultato perché la parola "processes" del titolo inizia con tale stringa.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-147">The query string "pro" would also find that result because the title word "processes" begins with that string.</span></span> <span data-ttu-id="5bc3c-148">Si noti che la query corrisponde solo ai prefissi.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-148">Note that the query only matches prefixes.</span></span> <span data-ttu-id="5bc3c-149">La stringa di query "rocess" non corrisponde a un risultato perché tale stringa, mentre parte della parola del titolo "Process", non inizia la parola.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-149">The query string "rocess" would not match a result because that string, while part of the title word "process", does not begin that word.</span></span>

<span data-ttu-id="5bc3c-150">Quando una query di ricerca contiene più token, per un risultato tutti i token devono corrispondere al prefisso di una parola chiave o di una parte del titolo dell'attività.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-150">When a search query contains multiple tokens, all the tokens must match the prefix of some keyword or part of the task title for a result.</span></span> <span data-ttu-id="5bc3c-151">La query "livello CPU" non corrisponde, perché "Level" non è presente nella parola chiave impostata.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-151">The query "cpu level" would not match, because "level" is not in the keyword set.</span></span> <span data-ttu-id="5bc3c-152">La query "esecuzione CPU" darebbe un risultato, perché "CPU" corrisponde a una parola chiave e "Run" è il prefisso della parola "Running" nel titolo dell'attività.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-152">The query "cpu run" would give a result, because "cpu" matches a keyword, and "run" is the prefix of the word "running" in the task's title.</span></span>

<span data-ttu-id="5bc3c-153">Il pannello di controllo non fornisce automaticamente la correzione ortografica o le variazioni, ad esempio plurali o sillabazione.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-153">Control Panel does not automatically provide spelling correction or variations such as plurals or hyphenation.</span></span> <span data-ttu-id="5bc3c-154">Anche le corrispondenze non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-154">Matches are also case-insensitive.</span></span> <span data-ttu-id="5bc3c-155">Per garantire un elenco di parole chiave con esito positivo, è consigliabile fornire le variazioni manualmente, ad esempio per questo collegamento di attività che include screen saver: "Screensavers; Screen saver; screen saver;"</span><span class="sxs-lookup"><span data-stu-id="5bc3c-155">To ensure a successful keyword list, it is recommended to provide variations yourself, such as for this task link that involves screen savers: "screensavers;screen-savers;screen savers;"</span></span>

<span data-ttu-id="5bc3c-156">Non è necessario aggiungere il "salvaschermo" singolare, perché una query che trova "salvaschermi" troverà anche "salvaschermo" a causa della corrispondenza del prefisso.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-156">There is no need to add the singular "screensaver", because a query that finds "screensavers" will also find "screensaver" due to the prefix match.</span></span> <span data-ttu-id="5bc3c-157">Un utente che digita anche parte della parola, ad esempio "schermate", visualizzerà comunque una corrispondenza in un collegamento a un'attività con "salvaschermi" come parola chiave.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-157">A user typing even part of the word, like "screensa" will still see a match on a task link that has "screensavers" as a keyword.</span></span> <span data-ttu-id="5bc3c-158">Per le lingue in cui i form plurali cambiano la parola, è necessario inserire tutti i form che un utente potrebbe ragionevolmente prevedere di digitare nelle parole chiave.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-158">For languages where plural forms change the word, it is necessary to put all the forms a user could reasonably be expected to type into the keywords.</span></span>

<span data-ttu-id="5bc3c-159">Come convenzione, Microsoft ha omesso le piccole parole come "How do I" o "voglio" dal set di parole chiave.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-159">As a convention, Microsoft has omitted small words like "how do I" or "I want to" from the set of keywords.</span></span> <span data-ttu-id="5bc3c-160">Si prevede che la maggior parte degli utenti digitano semplicemente le parole più importanti, ad esempio "mouse", "contrasto elevato" o "driver video" per ottenere risultati.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-160">The expectation is that most users will simply type the most important words such as "mouse", "high contrast", or "video driver" to get results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bc3c-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5bc3c-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bc3c-162">Elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="5bc3c-162">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="5bc3c-163">Linee guida sull'esperienza utente</span><span class="sxs-lookup"><span data-stu-id="5bc3c-163">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="5bc3c-164">Registrazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="5bc3c-164">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="5bc3c-165">Uso di CPLApplet</span><span class="sxs-lookup"><span data-stu-id="5bc3c-165">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="5bc3c-166">Elaborazione del messaggio del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="5bc3c-166">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="5bc3c-167">Esecuzione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="5bc3c-167">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="5bc3c-168">Estensione degli elementi del pannello di controllo di sistema</span><span class="sxs-lookup"><span data-stu-id="5bc3c-168">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="5bc3c-169">Assegnazione delle categorie del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="5bc3c-169">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="5bc3c-170">Accesso al pannello di controllo in modalità provvisoria in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5bc3c-170">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



