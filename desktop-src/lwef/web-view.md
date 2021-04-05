---
title: Personalizzazione della visualizzazione Web di una cartella
description: Una visualizzazione Web è un modo potente e flessibile per utilizzare Esplora risorse per visualizzare informazioni sul contenuto di una cartella della shell.
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Visualizzazioni Web
- Stile classico
- Stile Web
- intestazioni
- Area filefile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e364551d461eff6ae17a780bafc0b69182a1f16f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724695"
---
# <a name="customizing-a-folders-web-view"></a><span data-ttu-id="fff49-108">Personalizzazione della visualizzazione Web di una cartella</span><span class="sxs-lookup"><span data-stu-id="fff49-108">Customizing a Folder's Web View</span></span>

<span data-ttu-id="fff49-109">\[Questa funzionalità è supportata solo in Windows XP o versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="fff49-109">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="fff49-110">\]</span><span class="sxs-lookup"><span data-stu-id="fff49-110">\]</span></span>

<span data-ttu-id="fff49-111">Una visualizzazione Web è un modo potente e flessibile per utilizzare Esplora risorse per visualizzare informazioni sul contenuto di una cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="fff49-111">A Web view is a powerful and flexible way to use the Windows Explorer to display information about the contents of a Shell folder.</span></span>

-   [<span data-ttu-id="fff49-112">Introduzione</span><span class="sxs-lookup"><span data-stu-id="fff49-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="fff49-113">Uso del modello di visualizzazione Web</span><span class="sxs-lookup"><span data-stu-id="fff49-113">Using the Web View Template</span></span>](#using-the-web-view-template)
    -   [<span data-ttu-id="fff49-114">Corpo del modello</span><span class="sxs-lookup"><span data-stu-id="fff49-114">The Template Body</span></span>](#the-template-body)
    -   [<span data-ttu-id="fff49-115">Intestazione del modello</span><span class="sxs-lookup"><span data-stu-id="fff49-115">The Template Head</span></span>](#the-template-head)
-   [<span data-ttu-id="fff49-116">Summary</span><span class="sxs-lookup"><span data-stu-id="fff49-116">Summary</span></span>](#summary)

## <a name="introduction"></a><span data-ttu-id="fff49-117">Introduzione</span><span class="sxs-lookup"><span data-stu-id="fff49-117">Introduction</span></span>

<span data-ttu-id="fff49-118">Windows offre agli utenti due modi principali per visualizzare ed esplorare lo spazio dei nomi della shell.</span><span class="sxs-lookup"><span data-stu-id="fff49-118">Windows offers users two primary ways to view and navigate the Shell namespace.</span></span> <span data-ttu-id="fff49-119">Il più familiare di questi, lo stile classico, è simile al noto gestore di file di Windows.</span><span class="sxs-lookup"><span data-stu-id="fff49-119">The most familiar of these, the Classic style, is similar to the familiar Windows File Manager.</span></span> <span data-ttu-id="fff49-120">Il riquadro destro elenca il contenuto della cartella attualmente selezionata in uno dei cinque formati seguenti: icona grande, icona piccola, elenco, dettagli e anteprima.</span><span class="sxs-lookup"><span data-stu-id="fff49-120">The right pane lists the contents of the currently selected folder in one of five formats: Large Icon, Small Icon, List, Details, and Thumbnail.</span></span> <span data-ttu-id="fff49-121">La differenza principale rispetto a gestione file di Windows è il riquadro sinistro, che ha un aspetto molto simile alla barra di Explorer di Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="fff49-121">The major difference from Windows File Manager is the left pane, which looks very similar to the Explorer bar of Windows Internet Explorer.</span></span> <span data-ttu-id="fff49-122">Può essere ridimensionato o rimosso e può visualizzare diversi riquadri oltre al familiare albero file system, ad esempio un riquadro di ricerca.</span><span class="sxs-lookup"><span data-stu-id="fff49-122">It can be resized or removed, and it can display several panes in addition to the familiar file system tree, such as a search pane.</span></span>

> [!Note]  
> <span data-ttu-id="fff49-123">Le informazioni contenute in questo documento non si applicano a Windows XP, le tecniche illustrate si applicano solo alle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="fff49-123">The information in this document does not apply to Windows XP, the techniques discussed apply only to earlier versions of Windows.</span></span>

 

<span data-ttu-id="fff49-124">Nella figura seguente viene illustrata la cartella stampanti nello stile classico.</span><span class="sxs-lookup"><span data-stu-id="fff49-124">The following illustration shows the Printers folder in Classic style.</span></span>

![stile classico della cartella stampanti.](images/webview1.png)

<span data-ttu-id="fff49-126">Lo stile classico funziona ragionevolmente bene per le normali cartelle e file di file system.</span><span class="sxs-lookup"><span data-stu-id="fff49-126">The Classic style works reasonably well for normal file system folders and files.</span></span> <span data-ttu-id="fff49-127">Tuttavia, con l'introduzione di Windows 95, il file system si è evoluto nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fff49-127">However, with the introduction of Windows 95, the file system has evolved into the namespace.</span></span> <span data-ttu-id="fff49-128">Lo spazio dei nomi consente la creazione di *cartelle virtuali*, ad esempio stampanti o quartiere di rete, che possono rappresentare tipi di informazioni molto diversi rispetto a una normale cartella di file System.</span><span class="sxs-lookup"><span data-stu-id="fff49-128">The namespace allows the creation of *virtual folders*, such as Printers or Network Neighborhood, that can represent very different types of information than a normal file system folder.</span></span>

<span data-ttu-id="fff49-129">Lo stile Web, noto anche come visualizzazione Web, offre un metodo più flessibile e potente per presentare informazioni rispetto allo stile classico.</span><span class="sxs-lookup"><span data-stu-id="fff49-129">The Web style, also known as a Web view, offers a more flexible and powerful way of presenting information than Classic style.</span></span> <span data-ttu-id="fff49-130">In una visualizzazione Web, l'utente fondamentalmente Visualizza e sposta lo spazio dei nomi utilizzando Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="fff49-130">In a Web view, the user basically views and navigates the namespace using Internet Explorer.</span></span> <span data-ttu-id="fff49-131">Il layout di base di una visualizzazione Web è simile allo stile classico.</span><span class="sxs-lookup"><span data-stu-id="fff49-131">The basic layout of a Web view is similar to Classic style.</span></span> <span data-ttu-id="fff49-132">La barra di Explorer è invariata.</span><span class="sxs-lookup"><span data-stu-id="fff49-132">The Explorer bar is unchanged.</span></span> <span data-ttu-id="fff49-133">Tuttavia, l'area occupata dall'elenco di file diventa un'area di visualizzazione di uso generico che è effettivamente una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-133">However, the region that was occupied by the file list becomes a general-purpose display area that is effectively a webpage.</span></span> <span data-ttu-id="fff49-134">Una visualizzazione Web viene comunque utilizzata per visualizzare informazioni sul contenuto di una cartella, ma sono presenti pochi vincoli sulle informazioni visualizzate o su come.</span><span class="sxs-lookup"><span data-stu-id="fff49-134">A Web view is still used to display information about the contents of a folder, but there are few constraints on what information is displayed, or how.</span></span> <span data-ttu-id="fff49-135">Ogni cartella può avere una propria visualizzazione Web, personalizzata in base alle specifiche funzionalità.</span><span class="sxs-lookup"><span data-stu-id="fff49-135">Each folder can have its own Web view, customized to suit its particular features.</span></span>

<span data-ttu-id="fff49-136">Nella figura seguente è illustrata una visualizzazione Web della cartella stampanti (illustrata in precedenza in stile classico).</span><span class="sxs-lookup"><span data-stu-id="fff49-136">The following illustration shows a Web view of the Printers folder (shown previously in Classic style).</span></span>

![visualizzazione Web predefinita della cartella stampanti.](images/webview2.png)

<span data-ttu-id="fff49-138">Analogamente alle pagine Web convenzionali, le visualizzazioni Web sono controllate da un modello basato su HTML.</span><span class="sxs-lookup"><span data-stu-id="fff49-138">Much like conventional webpages, Web views are controlled by an HTML-based template.</span></span> <span data-ttu-id="fff49-139">La creazione di un modello di visualizzazione Web è quasi identica alla creazione di una pagina Web e fornisce lo stesso livello di flessibilità nel contenuto e nel layout delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="fff49-139">Authoring a Web view template is nearly identical to authoring a webpage and provides the same degree of flexibility in content and layout of information.</span></span> <span data-ttu-id="fff49-140">I modelli di visualizzazione Web possono usare DHTML (Dynamic HTML) e scripting per rispondere agli eventi, ad esempio un utente che fa clic su un elemento.</span><span class="sxs-lookup"><span data-stu-id="fff49-140">Web view templates can use Dynamic HTML (DHTML) and scripting to respond to events, such as a user clicking an item.</span></span> <span data-ttu-id="fff49-141">Possono inoltre ospitare oggetti che consentono loro di ottenere e visualizzare informazioni dalla cartella o dal contenuto.</span><span class="sxs-lookup"><span data-stu-id="fff49-141">They can also host objects that allow them to obtain and display information from the folder or its contents.</span></span>

<span data-ttu-id="fff49-142">L'utente può scegliere una visualizzazione Web avviando Esplora risorse, facendo clic su **Opzioni cartella** dal menu **Visualizza** e selezionando questa opzione: **Abilita contenuto Web nelle cartelle**.</span><span class="sxs-lookup"><span data-stu-id="fff49-142">The user can choose a Web view by starting Windows Explorer, clicking **Folder Options** on the **View** menu, and selecting this option: **Enable Web content in folders**.</span></span> <span data-ttu-id="fff49-143">Tuttavia, l'utente può anche avviare Internet Explorer e puntare il browser all'file system facendo clic sul menu **Visualizza** , puntando alla **barra di Explorer** e facendo clic su **cartelle**.</span><span class="sxs-lookup"><span data-stu-id="fff49-143">However, the user can also start Internet Explorer and point the browser at the file system by clicking the **View** menu, pointing to **Explorer Bar**, and clicking **Folders**.</span></span> <span data-ttu-id="fff49-144">In una visualizzazione Web non esiste praticamente alcuna differenza tra Internet Explorer e Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="fff49-144">In a Web view, there is virtually no difference between Internet Explorer and Windows Explorer.</span></span>

<span data-ttu-id="fff49-145">Sul lato sinistro del riquadro destro, nella visualizzazione Web stampanti viene visualizzato un banner con il nome e l'icona della cartella, seguito da un blocco di informazioni sulla cartella.</span><span class="sxs-lookup"><span data-stu-id="fff49-145">On the left side of the right pane, the Printers Web view displays a banner with the folder's name and icon, followed by a block of information about the folder.</span></span> <span data-ttu-id="fff49-146">Il consueto elenco di file occupa il lato destro della pagina.</span><span class="sxs-lookup"><span data-stu-id="fff49-146">The usual file list occupies the right side of the page.</span></span>

<span data-ttu-id="fff49-147">Quando un utente fa clic su un elemento, vengono visualizzate informazioni dettagliate sull'elemento nel blocco Information.</span><span class="sxs-lookup"><span data-stu-id="fff49-147">When a user clicks an item, detailed information about the item appears in the information block.</span></span> <span data-ttu-id="fff49-148">La visualizzazione Web stampanti Visualizza effettivamente le stesse informazioni disponibili nello stile classico, ma in un formato più utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="fff49-148">The Printers Web view actually displays much the same information that is available in Classic style, but it does so in a more usable format.</span></span> <span data-ttu-id="fff49-149">Tuttavia, una visualizzazione Web non è semplicemente un modo diverso per visualizzare le informazioni di stile classiche.</span><span class="sxs-lookup"><span data-stu-id="fff49-149">However, a Web view is not simply a different way to display Classic style information.</span></span> <span data-ttu-id="fff49-150">Ad esempio, un collegamento a un sito web utile può essere visualizzato sotto il blocco informazioni, una funzionalità non disponibile in stile classico.</span><span class="sxs-lookup"><span data-stu-id="fff49-150">For example, a link to a useful website can be displayed below the information block, a feature that is not available in Classic style.</span></span> <span data-ttu-id="fff49-151">Se l'utente fa clic sul collegamento, verrà visualizzato il sito.</span><span class="sxs-lookup"><span data-stu-id="fff49-151">If the user clicks the link, the site will be displayed.</span></span>

<span data-ttu-id="fff49-152">La visualizzazione Web stampanti illustrata nell'illustrazione precedente è simile allo stile classico, perché il modello di visualizzazione Web sottostante, ovvero un file con estensione HTT, è stato scritto in questo modo.</span><span class="sxs-lookup"><span data-stu-id="fff49-152">The Printers Web view shown in the preceding illustration is similar to the Classic style, because the underlying Web view template (an .htt file) was written that way.</span></span> <span data-ttu-id="fff49-153">L'elenco di file, ad esempio, non viene generato direttamente dal modello di visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-153">The list of files, for instance, is not generated by the Web view template directly.</span></span> <span data-ttu-id="fff49-154">Viene creato e visualizzato da un oggetto [**WebViewFolderContents**](webviewfoldercontents.md) ospitato dal modello di visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-154">It is created and displayed by a [**WebViewFolderContents**](webviewfoldercontents.md) object hosted by the Web view template.</span></span> <span data-ttu-id="fff49-155">I metodi e le proprietà dell'oggetto consentono alla visualizzazione Web di controllare il layout e ottenere informazioni su determinati elementi.</span><span class="sxs-lookup"><span data-stu-id="fff49-155">The object's methods and properties allow the Web view to control its layout and obtain information about particular items.</span></span> <span data-ttu-id="fff49-156">Il contenuto e il layout del banner e del blocco di informazioni vengono specificati nel modello di visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-156">The content and layout of the banner and information block is specified in the Web view template.</span></span>

<span data-ttu-id="fff49-157">Poiché una visualizzazione Web supporta DHTML, il modello può essere usato anche per gestire l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fff49-157">Because a Web view supports DHTML, the template can also be used to handle user interaction.</span></span> <span data-ttu-id="fff49-158">Ad esempio, quando un utente fa clic su una delle icone della stampante, l'oggetto **WebViewFolderIcon** genera un evento [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) .</span><span class="sxs-lookup"><span data-stu-id="fff49-158">For instance, when a user clicks one of the printer icons, the **WebViewFolderIcon** object fires a [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) event.</span></span> <span data-ttu-id="fff49-159">Il modello usa un gestore eventi DHTML scritto nello script per recuperare le informazioni richieste e visualizzarle nel blocco Information.</span><span class="sxs-lookup"><span data-stu-id="fff49-159">The template uses a DHTML event handler written in script to retrieve the requested information and display it in the information block.</span></span>

<span data-ttu-id="fff49-160">Questo semplice esempio per la cartella stampanti è l'unico modo per utilizzare una visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-160">This simple example for the Printers folder is by no means the only way to use a Web view.</span></span> <span data-ttu-id="fff49-161">Scrivendo un modello personalizzato e, se necessario, gli oggetti, è possibile usare una visualizzazione Web per visualizzare le informazioni e interagire con l'utente nel modo più efficace possibile.</span><span class="sxs-lookup"><span data-stu-id="fff49-161">By writing your own template and, if necessary, objects, you can use a Web view to display information and interact with the user in whatever way you find most effective.</span></span> <span data-ttu-id="fff49-162">Si noti che, attualmente, i modelli di visualizzazione Web visualizzano solo le cartelle virtuali definite dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fff49-162">Note that, at present, Web view templates only display system-defined virtual folders.</span></span> <span data-ttu-id="fff49-163">Sebbene gli sviluppatori possano creare una cartella virtuale implementando un'estensione dello spazio dei nomi, è necessario utilizzare le tecniche descritte nelle [estensioni dello spazio dei nomi](/windows/desktop/shell/nse-works) per visualizzarla.</span><span class="sxs-lookup"><span data-stu-id="fff49-163">Although developers can create a virtual folder by implementing a namespace extension, they must use the techniques described in [Namespace Extensions](/windows/desktop/shell/nse-works) to display it.</span></span>

## <a name="using-the-web-view-template"></a><span data-ttu-id="fff49-164">Uso del modello di visualizzazione Web</span><span class="sxs-lookup"><span data-stu-id="fff49-164">Using the Web View Template</span></span>

<span data-ttu-id="fff49-165">Il modo in cui i dati vengono visualizzati in una visualizzazione Web può essere personalizzato in modo limitato modificando il file di Desktop.ini di una cartella.</span><span class="sxs-lookup"><span data-stu-id="fff49-165">The way data is displayed in a Web view can be customized in a limited way by modifying a folder's Desktop.ini file.</span></span> <span data-ttu-id="fff49-166">Per informazioni dettagliate, vedere [personalizzazione delle cartelle con Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) .</span><span class="sxs-lookup"><span data-stu-id="fff49-166">See [Customizing Folders with Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) for details.</span></span> <span data-ttu-id="fff49-167">Un modo molto più flessibile e potente per personalizzare una visualizzazione Web consiste nel creare un modello di visualizzazione Web personalizzato.</span><span class="sxs-lookup"><span data-stu-id="fff49-167">A much more flexible and powerful way to customize a Web view is to create a custom Web view template.</span></span>

<span data-ttu-id="fff49-168">Il modello di visualizzazione Web controlla gli elementi visualizzati in una visualizzazione Web e in che modo.</span><span class="sxs-lookup"><span data-stu-id="fff49-168">The Web view template controls what is displayed in a Web view and how.</span></span> <span data-ttu-id="fff49-169">Usa le tecniche standard HTML, DHTML e di scripting per ottenere e visualizzare informazioni e interagire con l'utente.</span><span class="sxs-lookup"><span data-stu-id="fff49-169">It uses standard HTML, DHTML, and scripting techniques to obtain and display information and interact with the user.</span></span> <span data-ttu-id="fff49-170">In questa sezione viene illustrato come creare una visualizzazione Web esaminando un modello semplice, Generic. htt.</span><span class="sxs-lookup"><span data-stu-id="fff49-170">This section discusses how to create a Web view by examining a simple template—Generic.htt.</span></span>


```
<html>
    <style>
    <!-- This section defines a variety of styles that can be used
     when displaying the document -->
        body        {font: 8pt/10pt verdana; margin: 0}
        #Banner     {position: absolute; width: 100%; height: 88px; background: URL(res://webvw.dll/folder.gif) no-repeat top left}
        #MiniBanner {position: absolute; width: 100%; height: 32px; background: window}
        #Icon       {position: absolute; left: 11px; top: 12px; width: 64px; height: 64px}
        #FileList   {position: absolute; left: 30%; top: 88px; width: 1px; height: 1px}
        #Info       {position: absolute; top: 88px; width: 30%; background: window; overflow: auto}
        p       {margin-left: 20px; margin-right: 8px}
        p.Title     {font: 16pt/16pt verdana; font-weight: bold; color: #0099FF}
        a:link      {color: #FF6633}
        a:visited   {color: #0099FF}
        a:active    {color: black}
    </style>

    <head>
        <!-- allow references to any resources you might add to the
         folder -->
        <base href="%THISDIRPATH%\">

        <script language="JavaScript">
        
        <!-- This section defines a number of JavaScript utilities -->
            var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br><br>To get information about any of them, click the items icon.<br><br>";
            var L_Multiple_Text = " objects selected.";

            function FixSize() {
            // this function handles layout issues not covered by the style sheet

                var hideTop = 200;
                var hideLeft    = 400;
                var miniHeight  = 32;

                if (200 > document.body.clientHeight) {
                //A short window. Use the minibanner
                    document.all.Banner.style.visibility = "hidden";
                    document.all.MiniBanner.style.visibility = "visible";
                    document.all.FileList.style.top = 32;
                    document.all.Info.style.top = 32;
                }

                else {
                //A normal window. Use the normal banner
                    document.all.Banner.style.visibility = "visible";
                    document.all.MiniBanner.style.visibility = "hidden";
                    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
                    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
                    document.all.Rule.style.width = (document.body.clientWidth > 84 ? document.body.clientWidth - 84 : 0) + "px";     
                }
                if (400 > document.body.clientWidth) {
                //A narrow window. Hide the Info region and expand the file list region
                    document.all.Info.style.visibility = "hidden";
                    document.all.FileList.style.pixelLeft = 0;
                    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
                }

                else {
                //Normal width
                    document.all.Info.style.visibility = "visible";
                    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
                }
                document.all.FileList.style.pixelWidth = document.body.clientWidth - document.all.FileList.style.pixelLeft;
                document.all.FileList.style.pixelHeight = document.body.clientHeight - document.all.FileList.style.pixelTop;
                document.all.Info.style.pixelHeight = document.body.clientHeight - document.all.Info.style.pixelTop;
            }

            function Init() {
                /* Set the initial layout and have FixSize() called whenever the window is resized*/
                window.onresize = FixSize;
                FixSize();
                TextBlock.innerHTML = L_Intro_Text;
            }
        </script>

        <script language="JavaScript" for="FileList" event="SelectionChanged">
            // Updates the TextBlock region when an item is selected
            var data;
            var text;

            // name
            text = "<b>" + FileList.FocusedItem.Name + "</b>";

            // comment
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
            if (data)
                text += "<br>" + data;

            // documents
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
            if (data)
                text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

            // status
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
            if (data)
                text += "<br><br><b><font color=red>" + data + "</font></b>";

            // tip?
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
            if (data != "" && data != FileList.FocusedItem.Name)
                text += "<br><br>" + data;

            TextBlock.innerHTML = text;
        </script>
    </head>
<!-- The body of the document controls the actual data display.
 It uses several scripting objects to communicate with the
 namespace folder, and calls on the JavaScript objects defined
 in the header to handle much of the processing -->
    <body scroll=no onload="Init()">

        <!-- The normal banner. This banner displays the folder
         name and icon at the top of the WebView pane. This banner
         is used if the WebView pane is sufficiently large to
         display the icon and still have room for some information -->
        <div id="Banner" style="visibility: hidden">
            <!-- Display the folder name using a table with nowrap
             to prevent word wrapping. Explorer will replace
              %THISDIRNAME% with the current folder name -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 104px; margin-top: 16px">
                %THISDIRNAME% 
            </td></tr></table>
            <!-- this is more efficient than a long graphic, but it has to be adjusted in FixSize() -->
            <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
            <!-- Load the WebViewFolderIcon object, which extracts the folder's icon -->
            <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
                <param name="scale" value=200>
            </object>
        </div>

        <!-- The mini banner. This banner is used when the
         WebView pane is too short to display the icon. Instead,
          it displays only the folder name -->
        <div id="MiniBanner" style="visibility: hidden">
            <!-- use a table with nowrap to prevent word wrapping -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 16px; margin-top: 4px">
                %THISDIRNAME%
            </td></tr></table>
        </div>

        <!-- The Info region. This displays the information
         associated with a folder or file. Javascript in the header
         is used to generate the regions contents by by assigning
         a text block to TextBlock.innerHTML -->
        <div id="Info">
            <p style="margin-top: 16px");
            <span id="TextBlock">
            </span>
        </div>
        <!-- end left info panel -->

        <!-- Load the WebViewFolderContents object. This object
         returns information on the contents of the folder that
          can be used in the information display.  -->
        <object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>

    </body>
</html>
            
```



<span data-ttu-id="fff49-171">Un modo semplice per creare un modello di visualizzazione Web personalizzato consiste nel prendere Generic. htt e modificarlo.</span><span class="sxs-lookup"><span data-stu-id="fff49-171">A simple way to create your own Web view template is to take Generic.htt and modify it.</span></span> <span data-ttu-id="fff49-172">Poiché è piuttosto limitato, è consigliabile esaminare anche altri esempi più complessi per altre idee.</span><span class="sxs-lookup"><span data-stu-id="fff49-172">Because it is rather limited, you should also look at other, more complex examples for additional ideas.</span></span> <span data-ttu-id="fff49-173">È possibile trovarli cercando il sistema per l'estensione htt usato da tutti i modelli di visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-173">You can find them by searching your system for the .htt extension used by all Web view templates.</span></span> <span data-ttu-id="fff49-174">Se si desidera creare un modello personalizzato per una cartella, è consigliabile iniziare con il modello Folder. htt predefinito, che in genere è archiviato in C: \\ WinNT \\ Web o c: \\ Windows \\ Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-174">If you want to create a custom template for a folder, you should start with the default Folder.htt template, which is usually stored in either C:\\Winnt\\Web or C:\\Windows\\Web.</span></span> <span data-ttu-id="fff49-175">Si noti che questi file sono definiti come nascosti, quindi potrebbe essere necessario modificare le impostazioni di Esplora risorse per visualizzarli.</span><span class="sxs-lookup"><span data-stu-id="fff49-175">Note that these files are defined as hidden, so you may need to modify your Windows Explorer settings to view them.</span></span> <span data-ttu-id="fff49-176">Una volta creato, un file con estensione htt dovrebbe essere contrassegnato come di sola lettura e nascosto.</span><span class="sxs-lookup"><span data-stu-id="fff49-176">Once an .htt file is created, it should be marked as read-only and hidden.</span></span>

<span data-ttu-id="fff49-177">I modelli di visualizzazione Web usano l'estensione htt perché si differenziano leggermente dai documenti convenzionali. htm.</span><span class="sxs-lookup"><span data-stu-id="fff49-177">Web view templates use the .htt extension because they differ slightly from conventional .htm documents.</span></span> <span data-ttu-id="fff49-178">La differenza principale è rappresentata da diverse variabili speciali nei file con estensione htt sostituiti dal sistema con i valori dello spazio dei nomi correnti.</span><span class="sxs-lookup"><span data-stu-id="fff49-178">The main difference is several special variables in .htt files that the system replaces with the current namespace values.</span></span> <span data-ttu-id="fff49-179">Le variabili% THISDIR% e% THISDIRPATH% rappresentano il nome e il percorso della cartella attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="fff49-179">The %THISDIR% and %THISDIRPATH% variables represent the name and path of the currently selected folder.</span></span> <span data-ttu-id="fff49-180">La variabile% TEMPLATEDIR% rappresenta la cartella in cui sono archiviati i fogli di stile della visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-180">The %TEMPLATEDIR% variable represents the folder where the Web view style sheets are stored.</span></span>

<span data-ttu-id="fff49-181">Come la maggior parte dei modelli HTML, i file con estensione htt hanno due parti di base: un corpo e un Head.</span><span class="sxs-lookup"><span data-stu-id="fff49-181">Like most HTML templates, .htt files have two basic parts: a body and a head.</span></span> <span data-ttu-id="fff49-182">Il corpo del modello controlla il layout di base della visualizzazione Web e carica gli oggetti utilizzati per comunicare con lo spazio dei nomi e visualizzare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="fff49-182">The template body controls the basic layout of the Web view and loads the objects used to communicate with the namespace and display information.</span></span> <span data-ttu-id="fff49-183">L'intestazione contiene gli script e le funzioni che eseguono attività quali la gestione del ridimensionamento e l'ottenimento di informazioni dalla cartella.</span><span class="sxs-lookup"><span data-stu-id="fff49-183">The head contains scripts and functions that do tasks such as handling resizing and obtaining information from the folder.</span></span> <span data-ttu-id="fff49-184">La maggior parte dei modelli, incluso Generic. htt, include anche un foglio di stile.</span><span class="sxs-lookup"><span data-stu-id="fff49-184">Most templates, including Generic.htt, also include a style sheet.</span></span> <span data-ttu-id="fff49-185">In generale, è preferibile includere le informazioni sul foglio di stile nel modello.</span><span class="sxs-lookup"><span data-stu-id="fff49-185">In general, it is better to include the style sheet information in your template.</span></span> <span data-ttu-id="fff49-186">I fogli di stile separati potrebbero non funzionare correttamente quando una visualizzazione Web viene utilizzata con gli spazi dei nomi remoti.</span><span class="sxs-lookup"><span data-stu-id="fff49-186">Separate style sheets may not work properly when a Web view is used with remote namespaces.</span></span>

### <a name="the-template-body"></a><span data-ttu-id="fff49-187">Corpo del modello</span><span class="sxs-lookup"><span data-stu-id="fff49-187">The Template Body</span></span>

<span data-ttu-id="fff49-188">Il corpo del modello specifica gli elementi che verranno presentati da una visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-188">The body of the template specifies what will be presented by a Web view.</span></span> <span data-ttu-id="fff49-189">Si tratta anche della posizione in cui vengono caricati gli oggetti utilizzati per visualizzare le informazioni e comunicare con le cartelle dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fff49-189">It is also where the objects used to display information and communicate with namespace folders are loaded.</span></span> <span data-ttu-id="fff49-190">Il layout definito da Generic. htt è simile a quello illustrato nell'illustrazione della sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="fff49-190">The layout defined by Generic.htt is similar to that shown in the illustration in the previous section.</span></span> <span data-ttu-id="fff49-191">Sono disponibili tre aree di visualizzazione: il banner e il blocco informazioni sul lato sinistro della visualizzazione e l'elenco dei file a destra.</span><span class="sxs-lookup"><span data-stu-id="fff49-191">There are three display regions: the banner and information block on the left side of the view, and the file list on the right.</span></span>

<span data-ttu-id="fff49-192">Le aree sono tutti identificatori assegnati che devono essere usati dal foglio di stile e da DHTML.</span><span class="sxs-lookup"><span data-stu-id="fff49-192">The regions are all assigned identifiers to be used by the style sheet and DHTML.</span></span> <span data-ttu-id="fff49-193">Come descritto nella sezione successiva, è possibile usare due banner, con identificatori di "banner" e "MiniBanner".</span><span class="sxs-lookup"><span data-stu-id="fff49-193">As discussed in the next section, there are two possible banners, with identifiers of "Banner" and "MiniBanner".</span></span> <span data-ttu-id="fff49-194">L'identificatore dell'area del blocco informazioni è "info".</span><span class="sxs-lookup"><span data-stu-id="fff49-194">The identifier of the information block's region is "Info".</span></span> <span data-ttu-id="fff49-195">L'identificatore dell'oggetto elenco file è "filelist".</span><span class="sxs-lookup"><span data-stu-id="fff49-195">The file list object's identifier is "FileList".</span></span> <span data-ttu-id="fff49-196">I dettagli del [layout](#controlling-the-web-view-layout) dell'area sono gestiti dal foglio di stile e da una funzione Microsoft JScript, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), che viene discussa più avanti nel capitolo.</span><span class="sxs-lookup"><span data-stu-id="fff49-196">The details of the region's [layout](#controlling-the-web-view-layout) are handled by the style sheet and a Microsoft JScript function, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), which is discussed later in the chapter.</span></span>

### <a name="the-banner-region"></a><span data-ttu-id="fff49-197">Area banner</span><span class="sxs-lookup"><span data-stu-id="fff49-197">The Banner Region</span></span>

<span data-ttu-id="fff49-198">Il banner si trova nella parte superiore dello schermo, nell'angolo superiore sinistro della visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-198">The banner is located at the top of the display, in the upper-left corner of the Web view.</span></span> <span data-ttu-id="fff49-199">Il banner normale Visualizza il nome e l'icona della cartella il cui contenuto viene visualizzato nell'elenco dei file a destra.</span><span class="sxs-lookup"><span data-stu-id="fff49-199">The normal banner displays the name and icon of the folder whose contents are displayed in the file list on the right.</span></span> <span data-ttu-id="fff49-200">Tuttavia, se la finestra diventa troppo corta, potrebbe non esserci spazio sotto l'icona per visualizzare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="fff49-200">However, if the window becomes too short, there may be no room below the icon to display information.</span></span> <span data-ttu-id="fff49-201">Per questo motivo, Generic. htt definisce anche un Minibanner che visualizza solo il nome della cartella.</span><span class="sxs-lookup"><span data-stu-id="fff49-201">For this reason, Generic.htt also defines a minibanner that only displays the folder name.</span></span> <span data-ttu-id="fff49-202">Entrambi i banner sono inizialmente definiti come nascosti.</span><span class="sxs-lookup"><span data-stu-id="fff49-202">Both banners are initially defined as hidden.</span></span> <span data-ttu-id="fff49-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) sceglie quello da visualizzare e lo imposta su "Visible".</span><span class="sxs-lookup"><span data-stu-id="fff49-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) chooses which one to display and sets it to "visible".</span></span>

<span data-ttu-id="fff49-204">Il banner normale per Generic. htt è definito da:</span><span class="sxs-lookup"><span data-stu-id="fff49-204">The normal banner for Generic.htt is defined by:</span></span>


```
<div id="Banner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
    <p class=Title style="margin-left: 104px; margin-top: 16px">
        %THISDIRNAME% 
    </td></tr></table>
    <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
    <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
        <param name="scale" value=200>
    </object>
</div>
                    
```



<span data-ttu-id="fff49-205">Nella prima parte della sezione banner viene visualizzato il titolo con una regola orizzontale sottostante.</span><span class="sxs-lookup"><span data-stu-id="fff49-205">The first part of the banner section displays the title with a horizontal rule underneath it.</span></span> <span data-ttu-id="fff49-206">I tag table vengono usati per controllare la posizione.</span><span class="sxs-lookup"><span data-stu-id="fff49-206">Table tags are used to control its position.</span></span> <span data-ttu-id="fff49-207">L'attributo nowrap è impostato per il</span><span class="sxs-lookup"><span data-stu-id="fff49-207">The nowrap attribute is set for the</span></span> <TD> <span data-ttu-id="fff49-208">Tag per impedire il ritorno a capo automatico.</span><span class="sxs-lookup"><span data-stu-id="fff49-208">tag to prevent word wrapping.</span></span> <span data-ttu-id="fff49-209">Il sistema sostituirà% THISDIRNAME% con il nome della cartella corrente.</span><span class="sxs-lookup"><span data-stu-id="fff49-209">The system will replace %THISDIRNAME% with the name of the current folder.</span></span> <span data-ttu-id="fff49-210">Un oggetto **WebViewFolderIcon** , con l'identificatore "Icon" per semplicità, viene quindi caricato per estrarre e visualizzare l'icona della cartella.</span><span class="sxs-lookup"><span data-stu-id="fff49-210">A **WebViewFolderIcon** object, with an identifier of "Icon" for simplicity, is then loaded to extract and display the folder's icon.</span></span>

<span data-ttu-id="fff49-211">La sezione Minibanner è simile al banner normale.</span><span class="sxs-lookup"><span data-stu-id="fff49-211">The minibanner section is similar to the normal banner.</span></span> <span data-ttu-id="fff49-212">Il formato del titolo viene inserito leggermente più in alto e non ha una regola.</span><span class="sxs-lookup"><span data-stu-id="fff49-212">The format of the title is placed slightly higher and does not have a rule.</span></span> <span data-ttu-id="fff49-213">Poiché non è presente alcuna icona, l'oggetto **WebViewFolderIcon** non viene caricato.</span><span class="sxs-lookup"><span data-stu-id="fff49-213">Because there is no icon, the **WebViewFolderIcon** object is not loaded.</span></span>


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a><span data-ttu-id="fff49-214">Area informazioni</span><span class="sxs-lookup"><span data-stu-id="fff49-214">The Info Region</span></span>

<span data-ttu-id="fff49-215">La parte della visualizzazione Web sotto il banner viene utilizzata per presentare informazioni dettagliate relative all'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="fff49-215">The portion of the Web view below the banner is used to present detailed information about the selected item.</span></span> <span data-ttu-id="fff49-216">Se non è selezionato alcun elemento, viene visualizzato un messaggio predefinito.</span><span class="sxs-lookup"><span data-stu-id="fff49-216">If no item is selected, a default message is shown.</span></span> <span data-ttu-id="fff49-217">Poiché Generic. htt Visualizza solo un singolo blocco di testo, questa sezione è piuttosto semplice.</span><span class="sxs-lookup"><span data-stu-id="fff49-217">Because Generic.htt only displays a single block of text, this section is quite simple.</span></span>


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



<span data-ttu-id="fff49-218">La maggior parte delle operazioni di raccolta delle informazioni viene gestita da uno [script di informazioni sulle cartelle](#retrieving-and-displaying-folder-information) illustrato più avanti nel capitolo.</span><span class="sxs-lookup"><span data-stu-id="fff49-218">Most of the work of collecting the information is handled by a [folder information script](#retrieving-and-displaying-folder-information) that is discussed later in the chapter.</span></span> <span data-ttu-id="fff49-219">Le informazioni vengono visualizzate assegnando il testo a [TextBlock. InnerHtml](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="fff49-219">It displays the information by assigning the text to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

<span data-ttu-id="fff49-220">È possibile personalizzare facilmente la visualizzazione delle informazioni modificando questi elementi o includendo quelli aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="fff49-220">You can easily customize the information display by modifying these elements or including additional ones.</span></span> <span data-ttu-id="fff49-221">È possibile usare qualsiasi elemento che può essere inserito in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-221">Anything that you can put on a webpage can be used.</span></span> <span data-ttu-id="fff49-222">Per visualizzare, ad esempio, un collegamento al sito Web, è possibile aggiungere un elemento Anchor dopo il blocco di testo in Generic. htt.</span><span class="sxs-lookup"><span data-stu-id="fff49-222">For example, to display a link to your website, you can add an anchor element after the text block in Generic.htt.</span></span>


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
        <span>
        <p> Click on <a href="https://your.address"></a>
        </span>
</div>
                    
```



### <a name="the-filelist-region"></a><span data-ttu-id="fff49-223">Area filefile</span><span class="sxs-lookup"><span data-stu-id="fff49-223">The FileList Region</span></span>

<span data-ttu-id="fff49-224">Infine, Generic. htt carica un oggetto [**WebViewFolderContents**](webviewfoldercontents.md) per l'area di file.</span><span class="sxs-lookup"><span data-stu-id="fff49-224">Finally, Generic.htt loads a [**WebViewFolderContents**](webviewfoldercontents.md) object for the FileList region.</span></span> <span data-ttu-id="fff49-225">Poiché il relativo identificatore è impostato su "fileid", verrà indicato come oggetto filebase da ora in poi.</span><span class="sxs-lookup"><span data-stu-id="fff49-225">Because its identifier is set to "FileList", it will be referred to as the FileList object from now on.</span></span>


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



<span data-ttu-id="fff49-226">L'oggetto filefile si trova nella maggior parte delle visualizzazioni Web e svolge diversi scopi.</span><span class="sxs-lookup"><span data-stu-id="fff49-226">The FileList object is found in most Web views and serves several purposes.</span></span> <span data-ttu-id="fff49-227">Filelist Visualizza l'elenco di elementi contenuti nella cartella selezionata con le stesse opzioni e aspetto dell'elenco di file in stile classico.</span><span class="sxs-lookup"><span data-stu-id="fff49-227">FileList displays the list of items contained by the selected folder with the same options and appearance as the file list in Classic style.</span></span> <span data-ttu-id="fff49-228">Quando viene selezionato un elemento, fileEvent invia una notifica alla visualizzazione Web mediante la generazione di un evento [SelectionChanged](#retrieving-and-displaying-folder-information) .</span><span class="sxs-lookup"><span data-stu-id="fff49-228">When an item is selected, FileList notifies the Web view by firing a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="fff49-229">Fileitem espone inoltre metodi e proprietà che possono essere utilizzati per recuperare informazioni sui singoli elementi e controllare la posizione e le dimensioni dell'area di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="fff49-229">FileList also exposes methods and properties that can be used to retrieve information about individual items and control the position and size of its display area.</span></span>

<span data-ttu-id="fff49-230">Anche se l'oggetto filefile è molto utile, restituisce solo informazioni file system standard, ad esempio le dimensioni del file o gli attributi.</span><span class="sxs-lookup"><span data-stu-id="fff49-230">Although the FileList object is very useful, it only returns standard file system information, such as file size or attributes.</span></span> <span data-ttu-id="fff49-231">Per recuperare altri tipi di informazioni da una cartella della shell, sarà necessario caricare e gestire oggetti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="fff49-231">To retrieve other kinds of information from a Shell folder, you will have to load and handle additional objects.</span></span> <span data-ttu-id="fff49-232">Qualsiasi oggetto che può essere ospitato da una pagina Web può essere utilizzato con una visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-232">Any object that can be hosted by a webpage can be used with a Web view.</span></span>

### <a name="the-template-head"></a><span data-ttu-id="fff49-233">Intestazione del modello</span><span class="sxs-lookup"><span data-stu-id="fff49-233">The Template Head</span></span>

<span data-ttu-id="fff49-234">L'intestazione del modello di visualizzazione Web contiene gli script e le funzioni che eseguono la maggior parte del lavoro effettivo.</span><span class="sxs-lookup"><span data-stu-id="fff49-234">The head of the Web view template contains the scripts and functions that do most of the actual work.</span></span> <span data-ttu-id="fff49-235">È necessario gestire due attività essenziali.</span><span class="sxs-lookup"><span data-stu-id="fff49-235">There are two essential tasks that need to be handled.</span></span> <span data-ttu-id="fff49-236">Uno è il layout della visualizzazione Web, che deve essere regolato in modo da adattarsi a diverse aree di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="fff49-236">One is the layout of the Web view display, which needs to be adjusted to accommodate different display regions.</span></span> <span data-ttu-id="fff49-237">L'altro è il recupero e la visualizzazione delle informazioni dalla cartella quando viene selezionato un elemento.</span><span class="sxs-lookup"><span data-stu-id="fff49-237">The other is retrieving and displaying information from the folder when an item is selected.</span></span> <span data-ttu-id="fff49-238">Come per i fogli di stile, è preferibile includere tutti gli script e le funzioni del modello anziché farvi riferimento come file distinti.</span><span class="sxs-lookup"><span data-stu-id="fff49-238">As with style sheets, it is better to include all scripts and functions in the template instead of referencing them as separate files.</span></span>

### <a name="controlling-the-web-view-layout"></a><span data-ttu-id="fff49-239">Controllo del layout della visualizzazione Web</span><span class="sxs-lookup"><span data-stu-id="fff49-239">Controlling the Web View Layout</span></span>

<span data-ttu-id="fff49-240">L'area disponibile per una visualizzazione Web dipende dalle dimensioni della finestra visualizzazione Web e dalla quantità di risorse occupate dalla barra di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="fff49-240">The area available for a Web view depends on the size of the Web view window and how much of it is taken up by the Windows Explorer bar.</span></span> <span data-ttu-id="fff49-241">Quest'area verrà modificata ogni volta che la finestra o la barra di Esplora risorse viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="fff49-241">This area will change anytime the window or Windows Explorer bar is resized.</span></span> <span data-ttu-id="fff49-242">Pertanto, il layout deve corrispondere all'area disponibile quando viene caricata una visualizzazione Web e viene modificata in modo appropriato quando viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="fff49-242">So the layout needs to be matched to the available area when a Web view is loaded and change appropriately when it is resized.</span></span> <span data-ttu-id="fff49-243">Gran parte del layout viene specificato nel foglio di stile.</span><span class="sxs-lookup"><span data-stu-id="fff49-243">Much of the layout is specified in the style sheet.</span></span> <span data-ttu-id="fff49-244">L'area info, ad esempio, viene definita in modo da occupare il 30% più a sinistra della visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-244">The Info region, for example, is defined to occupy the leftmost 30 percent of the Web view.</span></span>


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



<span data-ttu-id="fff49-245">Quando una visualizzazione Web viene ridimensionata, la larghezza dell'area info cambierà in modo da mantenere la percentuale.</span><span class="sxs-lookup"><span data-stu-id="fff49-245">As a Web view is resized, the width of the Info region will change to maintain that percentage.</span></span> <span data-ttu-id="fff49-246">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) gestisce i problemi di layout che non possono essere gestiti da un foglio di stile.</span><span class="sxs-lookup"><span data-stu-id="fff49-246">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) manages the layout issues that can't be handled by a style sheet.</span></span>

### <a name="loading-and-initializing-the-web-view"></a><span data-ttu-id="fff49-247">Caricamento e inizializzazione della visualizzazione Web</span><span class="sxs-lookup"><span data-stu-id="fff49-247">Loading and Initializing the Web View</span></span>

<span data-ttu-id="fff49-248">Quando viene caricata una visualizzazione Web, è necessario modificare il layout per adattarlo all'area di visualizzazione disponibile.</span><span class="sxs-lookup"><span data-stu-id="fff49-248">When a Web view is loaded, the layout needs to be adjusted to fit the available display area.</span></span> <span data-ttu-id="fff49-249">Poiché non è ancora stato selezionato alcun elemento, le visualizzazioni Web in genere visualizzano alcune informazioni predefinite valide per l'intera cartella.</span><span class="sxs-lookup"><span data-stu-id="fff49-249">Because no item has been selected yet, Web views normally display some default information that applies to the whole folder.</span></span> <span data-ttu-id="fff49-250">Per gestire l'inizializzazione, il</span><span class="sxs-lookup"><span data-stu-id="fff49-250">To handle initialization, the</span></span> <BODY> <span data-ttu-id="fff49-251">Tag per Generic. htt rileva l'evento [OnLoad](/previous-versions//ms531409(v=vs.85)) e chiama la funzione **init** .</span><span class="sxs-lookup"><span data-stu-id="fff49-251">tag for Generic.htt detects the [onload](/previous-versions//ms531409(v=vs.85)) event and calls the **Init** function.</span></span>


```
<body scroll=no onload="Init">
                    
```



<span data-ttu-id="fff49-252">**Init** è una semplice funzione JScript.</span><span class="sxs-lookup"><span data-stu-id="fff49-252">**Init** is a simple JScript function.</span></span>


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



<span data-ttu-id="fff49-253">**Init** associa [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) all'evento [Window. OnResize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) in modo che venga chiamato ogni volta che viene modificata l'area di visualizzazione della visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-253">**Init** binds [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) to the [window.onresize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) event so that it will be called whenever the Web view display area changes.</span></span> <span data-ttu-id="fff49-254">Esegue quindi FixSize per impostare il layout iniziale e assegna il \_ testo introduttivo \_ all'area info.</span><span class="sxs-lookup"><span data-stu-id="fff49-254">It then runs FixSize to set the initial layout and assigns L\_Intro\_Text to the Info region.</span></span> <span data-ttu-id="fff49-255">L \_ testo introduttivo \_ è un blocco di testo introduttivo definito nella sezione foglio di stile.</span><span class="sxs-lookup"><span data-stu-id="fff49-255">L\_Intro\_Text is a block of introductory text that is defined in the style sheet section.</span></span>


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a><span data-ttu-id="fff49-256">Regolazione del layout tramite la funzione FixSize</span><span class="sxs-lookup"><span data-stu-id="fff49-256">Adjusting the Layout by using the FixSize function</span></span>

<span data-ttu-id="fff49-257">La funzione [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) viene usata per specificare diversi aspetti del layout che non possono essere gestiti dal foglio di stile.</span><span class="sxs-lookup"><span data-stu-id="fff49-257">The [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) function is used to specify several aspects of the layout that can't be handled by the style sheet.</span></span>

<span data-ttu-id="fff49-258">Sono disponibili due banner che è possibile usare, a seconda dell'altezza della visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-258">There are two possible banners that can be used, depending on the height of the Web view.</span></span>


```
if (200 > document.body.clientHeight) {
    //A short window. Use the minibanner.
    document.all.Banner.style.visibility = "hidden";
    document.all.MiniBanner.style.visibility = "visible";
    document.all.FileList.style.top = 32;
    document.all.Info.style.top = 32;
}
else {
    //A normal window. Use the normal banner.
    document.all.Banner.style.visibility = "visible";
    document.all.MiniBanner.style.visibility = "hidden";
    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
    document.all.Rule.style.width = (document.body.clientWidth > 84 ?                                    document.body.clientWidth - 84 : 0) + "px";      
}
                    
```



<span data-ttu-id="fff49-259">Generic. htt usa un'altezza di 200 pixel come linea di divisione tra Normal e minibanners.</span><span class="sxs-lookup"><span data-stu-id="fff49-259">Generic.htt uses a height of 200 pixels as the dividing line between normal and minibanners.</span></span> <span data-ttu-id="fff49-260">Imposta lo stile del banner selezionato su Visible e l'altro su Hidden.</span><span class="sxs-lookup"><span data-stu-id="fff49-260">It sets the style of the selected banner to visible and the other to hidden.</span></span> <span data-ttu-id="fff49-261">Vengono inoltre impostate diverse proprietà di layout per le aree Info e filesets in modo da adattarle correttamente al banner selezionato.</span><span class="sxs-lookup"><span data-stu-id="fff49-261">It also sets several layout properties for the Info and FileList regions so that they fit properly with the selected banner.</span></span>

<span data-ttu-id="fff49-262">Se una visualizzazione Web diventa troppo stretta, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) utilizza la larghezza intera dell'area di visualizzazione per la visualizzazione di file.</span><span class="sxs-lookup"><span data-stu-id="fff49-262">If a Web view becomes too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) uses the full width of the display area for the FileList display.</span></span>


```
if (400 > document.body.clientWidth) {
    //A narrow window. Hide the Info region, and expand the file list region.
    document.all.Info.style.visibility = "hidden";
    document.all.FileList.style.pixelLeft = 0;
    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
}

else {
    //Normal width.
    document.all.Info.style.visibility = "visible";
    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
}
                    
```



<span data-ttu-id="fff49-263">Generic. htt utilizza 400 pixel come linea di divisione tra le visualizzazioni narrow e Wide.</span><span class="sxs-lookup"><span data-stu-id="fff49-263">Generic.htt uses 400 pixels as the dividing line between narrow and wide displays.</span></span> <span data-ttu-id="fff49-264">Se la visualizzazione Web è troppo stretta, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) nasconde l'area info e modifica la proprietà [filepixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) in modo da riempire l'intera area sotto il banner.</span><span class="sxs-lookup"><span data-stu-id="fff49-264">If the Web view is too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) hides the Info region and modifies the FileList [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) property so that it fills the entire region below the banner.</span></span>

<span data-ttu-id="fff49-265">Le ultime righe di [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) regolano diverse proprietà di layout in base ai risultati del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="fff49-265">The final few lines of [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) adjust several layout properties based on the results of the preceding code.</span></span> <span data-ttu-id="fff49-266">La larghezza dell'area di visualizzazione di file è regolata in modo da riempire esattamente la parte della visualizzazione Web non occupata dall'area info.</span><span class="sxs-lookup"><span data-stu-id="fff49-266">The width of the FileList region is adjusted so that it exactly fills the portion of the Web view not occupied by the Info region.</span></span> <span data-ttu-id="fff49-267">L'altezza dell'area info è dimensionata in modo da adattarsi al banner e alla parte inferiore della visualizzazione Web.</span><span class="sxs-lookup"><span data-stu-id="fff49-267">The height of the Info region is sized to fit between the banner and the bottom of the Web view.</span></span>


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a><span data-ttu-id="fff49-268">Recupero e visualizzazione delle informazioni sulle cartelle</span><span class="sxs-lookup"><span data-stu-id="fff49-268">Retrieving and Displaying Folder Information</span></span>

<span data-ttu-id="fff49-269">Quando un utente seleziona un elemento, l'oggetto fileitem genera un evento [SelectionChanged](#retrieving-and-displaying-folder-information) .</span><span class="sxs-lookup"><span data-stu-id="fff49-269">When a user selects an item, the FileList object fires a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="fff49-270">Questo evento viene gestito da uno script JScript.</span><span class="sxs-lookup"><span data-stu-id="fff49-270">This event is handled by a JScript script.</span></span> <span data-ttu-id="fff49-271">Per semplicità, lo script trovato in Generic. htt presuppone che sia possibile selezionare un solo elemento alla volta.</span><span class="sxs-lookup"><span data-stu-id="fff49-271">For simplicity, the script found in Generic.htt assumes that only one item can be selected at a time.</span></span>


```
<script language="JavaScript" for="FileList" event="SelectionChanged">
    // Updates the TextBlock region when an item is selected.
    var data;
    var text;

    // Name
    text = "<b>" + FileList.FocusedItem.Name + "</b>";

    // Comment
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
    if (data)
        text += "<br>" + data;

    // Documents
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
    if (data)
        text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

    // Status
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
    if (data)
        text += "<br><br><b><font color=red>" + data + "</font></b>";

    // Tip 
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
    if (data != "" && data != FileList.FocusedItem.Name)
        text += "<br><br>" + data;

    TextBlock.innerHTML = text;
</script>
                    
```



<span data-ttu-id="fff49-272">Per ottenere informazioni sull'elemento, nello script vengono utilizzate due proprietà fileitem, [**fileFocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)e [**filefile. Folder**](/windows/desktop/shell/shellfolderview-folder) .</span><span class="sxs-lookup"><span data-stu-id="fff49-272">The script uses two FileList properties, [**FileList.FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)and [**FileList.Folder**](/windows/desktop/shell/shellfolderview-folder) to obtain information about the item.</span></span> <span data-ttu-id="fff49-273">**FileFocusedItem** identifica l'elemento selezionato, con il nome dell'elemento specificato da **FileList.FocusedItem.Name**.</span><span class="sxs-lookup"><span data-stu-id="fff49-273">**FileList.FocusedItem** identifies the selected item, with the item's name given by **FileList.FocusedItem.Name**.</span></span> <span data-ttu-id="fff49-274">**Filefile. Folder** è effettivamente un puntatore a un oggetto [**Folder**](../shell/folder.md) .</span><span class="sxs-lookup"><span data-stu-id="fff49-274">**FileList.Folder** is actually a pointer to a [**Folder**](../shell/folder.md) object.</span></span> <span data-ttu-id="fff49-275">Il metodo [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) dell'oggetto Folder viene usato per recuperare le informazioni rimanenti sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="fff49-275">The Folder object's [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) method is used to retrieve the remaining information about the item.</span></span>

<span data-ttu-id="fff49-276">Tutte le informazioni sono concatenate in una singola stringa di testo, separate da</span><span class="sxs-lookup"><span data-stu-id="fff49-276">All the information is concatenated into a single text string, separated by</span></span> <BR> <span data-ttu-id="fff49-277">Tag per migliorare la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="fff49-277">tags for readability.</span></span> <span data-ttu-id="fff49-278">Il testo viene quindi visualizzato assegnando il testo a [TextBlock. InnerHtml](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="fff49-278">The text is then displayed by assigning it to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="fff49-279">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="fff49-279">Summary</span></span>

<span data-ttu-id="fff49-280">In questo capitolo vengono descritte alcune tecniche che è possibile utilizzare per personalizzare il modo in cui Esplora risorse Visualizza le informazioni sulle cartelle della shell.</span><span class="sxs-lookup"><span data-stu-id="fff49-280">This chapter outlines some of the techniques you can use to customize the way the Windows Explorer displays information about Shell folders.</span></span> <span data-ttu-id="fff49-281">La creazione di un file di Desktop.ini consente di eseguire alcune semplici operazioni di personalizzazione, ad esempio la visualizzazione di un'icona personalizzata al posto dell'icona della cartella standard.</span><span class="sxs-lookup"><span data-stu-id="fff49-281">Creating a Desktop.ini file allows you to do some simple customization, such as displaying a custom icon in place of the standard folder icon.</span></span> <span data-ttu-id="fff49-282">Quando una cartella viene visualizzata in una visualizzazione Web, il layout e la visualizzazione sono controllati da un modello basato su HTML che determina quali informazioni vengono visualizzate e come.</span><span class="sxs-lookup"><span data-stu-id="fff49-282">When a folder appears in a Web view, its layout and display are controlled by an HTML-based template that determines what information is displayed and how.</span></span> <span data-ttu-id="fff49-283">È possibile esercitare un elevato livello di controllo sulla visualizzazione Web di una cartella utilizzando le tecniche standard HTML, DHTML e di scripting per creare un modello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="fff49-283">You can exercise a high degree of control over a folder's Web view by using standard HTML, DHTML, and scripting techniques to create a custom template.</span></span>

 

 