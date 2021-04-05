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
# <a name="customizing-a-folders-web-view"></a>Personalizzazione della visualizzazione Web di una cartella

\[Questa funzionalità è supportata solo in Windows XP o versioni precedenti. \]

Una visualizzazione Web è un modo potente e flessibile per utilizzare Esplora risorse per visualizzare informazioni sul contenuto di una cartella della shell.

-   [Introduzione](#introduction)
-   [Uso del modello di visualizzazione Web](#using-the-web-view-template)
    -   [Corpo del modello](#the-template-body)
    -   [Intestazione del modello](#the-template-head)
-   [Summary](#summary)

## <a name="introduction"></a>Introduzione

Windows offre agli utenti due modi principali per visualizzare ed esplorare lo spazio dei nomi della shell. Il più familiare di questi, lo stile classico, è simile al noto gestore di file di Windows. Il riquadro destro elenca il contenuto della cartella attualmente selezionata in uno dei cinque formati seguenti: icona grande, icona piccola, elenco, dettagli e anteprima. La differenza principale rispetto a gestione file di Windows è il riquadro sinistro, che ha un aspetto molto simile alla barra di Explorer di Windows Internet Explorer. Può essere ridimensionato o rimosso e può visualizzare diversi riquadri oltre al familiare albero file system, ad esempio un riquadro di ricerca.

> [!Note]  
> Le informazioni contenute in questo documento non si applicano a Windows XP, le tecniche illustrate si applicano solo alle versioni precedenti di Windows.

 

Nella figura seguente viene illustrata la cartella stampanti nello stile classico.

![stile classico della cartella stampanti.](images/webview1.png)

Lo stile classico funziona ragionevolmente bene per le normali cartelle e file di file system. Tuttavia, con l'introduzione di Windows 95, il file system si è evoluto nello spazio dei nomi. Lo spazio dei nomi consente la creazione di *cartelle virtuali*, ad esempio stampanti o quartiere di rete, che possono rappresentare tipi di informazioni molto diversi rispetto a una normale cartella di file System.

Lo stile Web, noto anche come visualizzazione Web, offre un metodo più flessibile e potente per presentare informazioni rispetto allo stile classico. In una visualizzazione Web, l'utente fondamentalmente Visualizza e sposta lo spazio dei nomi utilizzando Internet Explorer. Il layout di base di una visualizzazione Web è simile allo stile classico. La barra di Explorer è invariata. Tuttavia, l'area occupata dall'elenco di file diventa un'area di visualizzazione di uso generico che è effettivamente una pagina Web. Una visualizzazione Web viene comunque utilizzata per visualizzare informazioni sul contenuto di una cartella, ma sono presenti pochi vincoli sulle informazioni visualizzate o su come. Ogni cartella può avere una propria visualizzazione Web, personalizzata in base alle specifiche funzionalità.

Nella figura seguente è illustrata una visualizzazione Web della cartella stampanti (illustrata in precedenza in stile classico).

![visualizzazione Web predefinita della cartella stampanti.](images/webview2.png)

Analogamente alle pagine Web convenzionali, le visualizzazioni Web sono controllate da un modello basato su HTML. La creazione di un modello di visualizzazione Web è quasi identica alla creazione di una pagina Web e fornisce lo stesso livello di flessibilità nel contenuto e nel layout delle informazioni. I modelli di visualizzazione Web possono usare DHTML (Dynamic HTML) e scripting per rispondere agli eventi, ad esempio un utente che fa clic su un elemento. Possono inoltre ospitare oggetti che consentono loro di ottenere e visualizzare informazioni dalla cartella o dal contenuto.

L'utente può scegliere una visualizzazione Web avviando Esplora risorse, facendo clic su **Opzioni cartella** dal menu **Visualizza** e selezionando questa opzione: **Abilita contenuto Web nelle cartelle**. Tuttavia, l'utente può anche avviare Internet Explorer e puntare il browser all'file system facendo clic sul menu **Visualizza** , puntando alla **barra di Explorer** e facendo clic su **cartelle**. In una visualizzazione Web non esiste praticamente alcuna differenza tra Internet Explorer e Esplora risorse.

Sul lato sinistro del riquadro destro, nella visualizzazione Web stampanti viene visualizzato un banner con il nome e l'icona della cartella, seguito da un blocco di informazioni sulla cartella. Il consueto elenco di file occupa il lato destro della pagina.

Quando un utente fa clic su un elemento, vengono visualizzate informazioni dettagliate sull'elemento nel blocco Information. La visualizzazione Web stampanti Visualizza effettivamente le stesse informazioni disponibili nello stile classico, ma in un formato più utilizzabile. Tuttavia, una visualizzazione Web non è semplicemente un modo diverso per visualizzare le informazioni di stile classiche. Ad esempio, un collegamento a un sito web utile può essere visualizzato sotto il blocco informazioni, una funzionalità non disponibile in stile classico. Se l'utente fa clic sul collegamento, verrà visualizzato il sito.

La visualizzazione Web stampanti illustrata nell'illustrazione precedente è simile allo stile classico, perché il modello di visualizzazione Web sottostante, ovvero un file con estensione HTT, è stato scritto in questo modo. L'elenco di file, ad esempio, non viene generato direttamente dal modello di visualizzazione Web. Viene creato e visualizzato da un oggetto [**WebViewFolderContents**](webviewfoldercontents.md) ospitato dal modello di visualizzazione Web. I metodi e le proprietà dell'oggetto consentono alla visualizzazione Web di controllare il layout e ottenere informazioni su determinati elementi. Il contenuto e il layout del banner e del blocco di informazioni vengono specificati nel modello di visualizzazione Web.

Poiché una visualizzazione Web supporta DHTML, il modello può essere usato anche per gestire l'interazione dell'utente. Ad esempio, quando un utente fa clic su una delle icone della stampante, l'oggetto **WebViewFolderIcon** genera un evento [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) . Il modello usa un gestore eventi DHTML scritto nello script per recuperare le informazioni richieste e visualizzarle nel blocco Information.

Questo semplice esempio per la cartella stampanti è l'unico modo per utilizzare una visualizzazione Web. Scrivendo un modello personalizzato e, se necessario, gli oggetti, è possibile usare una visualizzazione Web per visualizzare le informazioni e interagire con l'utente nel modo più efficace possibile. Si noti che, attualmente, i modelli di visualizzazione Web visualizzano solo le cartelle virtuali definite dal sistema. Sebbene gli sviluppatori possano creare una cartella virtuale implementando un'estensione dello spazio dei nomi, è necessario utilizzare le tecniche descritte nelle [estensioni dello spazio dei nomi](/windows/desktop/shell/nse-works) per visualizzarla.

## <a name="using-the-web-view-template"></a>Uso del modello di visualizzazione Web

Il modo in cui i dati vengono visualizzati in una visualizzazione Web può essere personalizzato in modo limitato modificando il file di Desktop.ini di una cartella. Per informazioni dettagliate, vedere [personalizzazione delle cartelle con Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) . Un modo molto più flessibile e potente per personalizzare una visualizzazione Web consiste nel creare un modello di visualizzazione Web personalizzato.

Il modello di visualizzazione Web controlla gli elementi visualizzati in una visualizzazione Web e in che modo. Usa le tecniche standard HTML, DHTML e di scripting per ottenere e visualizzare informazioni e interagire con l'utente. In questa sezione viene illustrato come creare una visualizzazione Web esaminando un modello semplice, Generic. htt.


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



Un modo semplice per creare un modello di visualizzazione Web personalizzato consiste nel prendere Generic. htt e modificarlo. Poiché è piuttosto limitato, è consigliabile esaminare anche altri esempi più complessi per altre idee. È possibile trovarli cercando il sistema per l'estensione htt usato da tutti i modelli di visualizzazione Web. Se si desidera creare un modello personalizzato per una cartella, è consigliabile iniziare con il modello Folder. htt predefinito, che in genere è archiviato in C: \\ WinNT \\ Web o c: \\ Windows \\ Web. Si noti che questi file sono definiti come nascosti, quindi potrebbe essere necessario modificare le impostazioni di Esplora risorse per visualizzarli. Una volta creato, un file con estensione htt dovrebbe essere contrassegnato come di sola lettura e nascosto.

I modelli di visualizzazione Web usano l'estensione htt perché si differenziano leggermente dai documenti convenzionali. htm. La differenza principale è rappresentata da diverse variabili speciali nei file con estensione htt sostituiti dal sistema con i valori dello spazio dei nomi correnti. Le variabili% THISDIR% e% THISDIRPATH% rappresentano il nome e il percorso della cartella attualmente selezionata. La variabile% TEMPLATEDIR% rappresenta la cartella in cui sono archiviati i fogli di stile della visualizzazione Web.

Come la maggior parte dei modelli HTML, i file con estensione htt hanno due parti di base: un corpo e un Head. Il corpo del modello controlla il layout di base della visualizzazione Web e carica gli oggetti utilizzati per comunicare con lo spazio dei nomi e visualizzare le informazioni. L'intestazione contiene gli script e le funzioni che eseguono attività quali la gestione del ridimensionamento e l'ottenimento di informazioni dalla cartella. La maggior parte dei modelli, incluso Generic. htt, include anche un foglio di stile. In generale, è preferibile includere le informazioni sul foglio di stile nel modello. I fogli di stile separati potrebbero non funzionare correttamente quando una visualizzazione Web viene utilizzata con gli spazi dei nomi remoti.

### <a name="the-template-body"></a>Corpo del modello

Il corpo del modello specifica gli elementi che verranno presentati da una visualizzazione Web. Si tratta anche della posizione in cui vengono caricati gli oggetti utilizzati per visualizzare le informazioni e comunicare con le cartelle dello spazio dei nomi. Il layout definito da Generic. htt è simile a quello illustrato nell'illustrazione della sezione precedente. Sono disponibili tre aree di visualizzazione: il banner e il blocco informazioni sul lato sinistro della visualizzazione e l'elenco dei file a destra.

Le aree sono tutti identificatori assegnati che devono essere usati dal foglio di stile e da DHTML. Come descritto nella sezione successiva, è possibile usare due banner, con identificatori di "banner" e "MiniBanner". L'identificatore dell'area del blocco informazioni è "info". L'identificatore dell'oggetto elenco file è "filelist". I dettagli del [layout](#controlling-the-web-view-layout) dell'area sono gestiti dal foglio di stile e da una funzione Microsoft JScript, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), che viene discussa più avanti nel capitolo.

### <a name="the-banner-region"></a>Area banner

Il banner si trova nella parte superiore dello schermo, nell'angolo superiore sinistro della visualizzazione Web. Il banner normale Visualizza il nome e l'icona della cartella il cui contenuto viene visualizzato nell'elenco dei file a destra. Tuttavia, se la finestra diventa troppo corta, potrebbe non esserci spazio sotto l'icona per visualizzare le informazioni. Per questo motivo, Generic. htt definisce anche un Minibanner che visualizza solo il nome della cartella. Entrambi i banner sono inizialmente definiti come nascosti. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) sceglie quello da visualizzare e lo imposta su "Visible".

Il banner normale per Generic. htt è definito da:


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



Nella prima parte della sezione banner viene visualizzato il titolo con una regola orizzontale sottostante. I tag table vengono usati per controllare la posizione. L'attributo nowrap è impostato per il <TD> Tag per impedire il ritorno a capo automatico. Il sistema sostituirà% THISDIRNAME% con il nome della cartella corrente. Un oggetto **WebViewFolderIcon** , con l'identificatore "Icon" per semplicità, viene quindi caricato per estrarre e visualizzare l'icona della cartella.

La sezione Minibanner è simile al banner normale. Il formato del titolo viene inserito leggermente più in alto e non ha una regola. Poiché non è presente alcuna icona, l'oggetto **WebViewFolderIcon** non viene caricato.


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a>Area informazioni

La parte della visualizzazione Web sotto il banner viene utilizzata per presentare informazioni dettagliate relative all'elemento selezionato. Se non è selezionato alcun elemento, viene visualizzato un messaggio predefinito. Poiché Generic. htt Visualizza solo un singolo blocco di testo, questa sezione è piuttosto semplice.


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



La maggior parte delle operazioni di raccolta delle informazioni viene gestita da uno [script di informazioni sulle cartelle](#retrieving-and-displaying-folder-information) illustrato più avanti nel capitolo. Le informazioni vengono visualizzate assegnando il testo a [TextBlock. InnerHtml](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).

È possibile personalizzare facilmente la visualizzazione delle informazioni modificando questi elementi o includendo quelli aggiuntivi. È possibile usare qualsiasi elemento che può essere inserito in una pagina Web. Per visualizzare, ad esempio, un collegamento al sito Web, è possibile aggiungere un elemento Anchor dopo il blocco di testo in Generic. htt.


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



### <a name="the-filelist-region"></a>Area filefile

Infine, Generic. htt carica un oggetto [**WebViewFolderContents**](webviewfoldercontents.md) per l'area di file. Poiché il relativo identificatore è impostato su "fileid", verrà indicato come oggetto filebase da ora in poi.


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



L'oggetto filefile si trova nella maggior parte delle visualizzazioni Web e svolge diversi scopi. Filelist Visualizza l'elenco di elementi contenuti nella cartella selezionata con le stesse opzioni e aspetto dell'elenco di file in stile classico. Quando viene selezionato un elemento, fileEvent invia una notifica alla visualizzazione Web mediante la generazione di un evento [SelectionChanged](#retrieving-and-displaying-folder-information) . Fileitem espone inoltre metodi e proprietà che possono essere utilizzati per recuperare informazioni sui singoli elementi e controllare la posizione e le dimensioni dell'area di visualizzazione.

Anche se l'oggetto filefile è molto utile, restituisce solo informazioni file system standard, ad esempio le dimensioni del file o gli attributi. Per recuperare altri tipi di informazioni da una cartella della shell, sarà necessario caricare e gestire oggetti aggiuntivi. Qualsiasi oggetto che può essere ospitato da una pagina Web può essere utilizzato con una visualizzazione Web.

### <a name="the-template-head"></a>Intestazione del modello

L'intestazione del modello di visualizzazione Web contiene gli script e le funzioni che eseguono la maggior parte del lavoro effettivo. È necessario gestire due attività essenziali. Uno è il layout della visualizzazione Web, che deve essere regolato in modo da adattarsi a diverse aree di visualizzazione. L'altro è il recupero e la visualizzazione delle informazioni dalla cartella quando viene selezionato un elemento. Come per i fogli di stile, è preferibile includere tutti gli script e le funzioni del modello anziché farvi riferimento come file distinti.

### <a name="controlling-the-web-view-layout"></a>Controllo del layout della visualizzazione Web

L'area disponibile per una visualizzazione Web dipende dalle dimensioni della finestra visualizzazione Web e dalla quantità di risorse occupate dalla barra di Esplora risorse. Quest'area verrà modificata ogni volta che la finestra o la barra di Esplora risorse viene ridimensionata. Pertanto, il layout deve corrispondere all'area disponibile quando viene caricata una visualizzazione Web e viene modificata in modo appropriato quando viene ridimensionata. Gran parte del layout viene specificato nel foglio di stile. L'area info, ad esempio, viene definita in modo da occupare il 30% più a sinistra della visualizzazione Web.


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



Quando una visualizzazione Web viene ridimensionata, la larghezza dell'area info cambierà in modo da mantenere la percentuale. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) gestisce i problemi di layout che non possono essere gestiti da un foglio di stile.

### <a name="loading-and-initializing-the-web-view"></a>Caricamento e inizializzazione della visualizzazione Web

Quando viene caricata una visualizzazione Web, è necessario modificare il layout per adattarlo all'area di visualizzazione disponibile. Poiché non è ancora stato selezionato alcun elemento, le visualizzazioni Web in genere visualizzano alcune informazioni predefinite valide per l'intera cartella. Per gestire l'inizializzazione, il <BODY> Tag per Generic. htt rileva l'evento [OnLoad](/previous-versions//ms531409(v=vs.85)) e chiama la funzione **init** .


```
<body scroll=no onload="Init">
                    
```



**Init** è una semplice funzione JScript.


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



**Init** associa [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) all'evento [Window. OnResize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) in modo che venga chiamato ogni volta che viene modificata l'area di visualizzazione della visualizzazione Web. Esegue quindi FixSize per impostare il layout iniziale e assegna il \_ testo introduttivo \_ all'area info. L \_ testo introduttivo \_ è un blocco di testo introduttivo definito nella sezione foglio di stile.


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a>Regolazione del layout tramite la funzione FixSize

La funzione [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) viene usata per specificare diversi aspetti del layout che non possono essere gestiti dal foglio di stile.

Sono disponibili due banner che è possibile usare, a seconda dell'altezza della visualizzazione Web.


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



Generic. htt usa un'altezza di 200 pixel come linea di divisione tra Normal e minibanners. Imposta lo stile del banner selezionato su Visible e l'altro su Hidden. Vengono inoltre impostate diverse proprietà di layout per le aree Info e filesets in modo da adattarle correttamente al banner selezionato.

Se una visualizzazione Web diventa troppo stretta, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) utilizza la larghezza intera dell'area di visualizzazione per la visualizzazione di file.


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



Generic. htt utilizza 400 pixel come linea di divisione tra le visualizzazioni narrow e Wide. Se la visualizzazione Web è troppo stretta, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) nasconde l'area info e modifica la proprietà [filepixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) in modo da riempire l'intera area sotto il banner.

Le ultime righe di [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) regolano diverse proprietà di layout in base ai risultati del codice precedente. La larghezza dell'area di visualizzazione di file è regolata in modo da riempire esattamente la parte della visualizzazione Web non occupata dall'area info. L'altezza dell'area info è dimensionata in modo da adattarsi al banner e alla parte inferiore della visualizzazione Web.


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a>Recupero e visualizzazione delle informazioni sulle cartelle

Quando un utente seleziona un elemento, l'oggetto fileitem genera un evento [SelectionChanged](#retrieving-and-displaying-folder-information) . Questo evento viene gestito da uno script JScript. Per semplicità, lo script trovato in Generic. htt presuppone che sia possibile selezionare un solo elemento alla volta.


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



Per ottenere informazioni sull'elemento, nello script vengono utilizzate due proprietà fileitem, [**fileFocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)e [**filefile. Folder**](/windows/desktop/shell/shellfolderview-folder) . **FileFocusedItem** identifica l'elemento selezionato, con il nome dell'elemento specificato da **FileList.FocusedItem.Name**. **Filefile. Folder** è effettivamente un puntatore a un oggetto [**Folder**](../shell/folder.md) . Il metodo [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) dell'oggetto Folder viene usato per recuperare le informazioni rimanenti sull'elemento.

Tutte le informazioni sono concatenate in una singola stringa di testo, separate da <BR> Tag per migliorare la leggibilità. Il testo viene quindi visualizzato assegnando il testo a [TextBlock. InnerHtml](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).

## <a name="summary"></a>Riepilogo

In questo capitolo vengono descritte alcune tecniche che è possibile utilizzare per personalizzare il modo in cui Esplora risorse Visualizza le informazioni sulle cartelle della shell. La creazione di un file di Desktop.ini consente di eseguire alcune semplici operazioni di personalizzazione, ad esempio la visualizzazione di un'icona personalizzata al posto dell'icona della cartella standard. Quando una cartella viene visualizzata in una visualizzazione Web, il layout e la visualizzazione sono controllati da un modello basato su HTML che determina quali informazioni vengono visualizzate e come. È possibile esercitare un elevato livello di controllo sulla visualizzazione Web di una cartella utilizzando le tecniche standard HTML, DHTML e di scripting per creare un modello personalizzato.

 

 