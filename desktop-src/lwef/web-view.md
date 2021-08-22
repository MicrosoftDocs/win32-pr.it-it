---
title: Personalizzazione della visualizzazione Web di una cartella
description: Una visualizzazione Web è un modo potente e flessibile per usare Windows Explorer per visualizzare informazioni sul contenuto di una cartella shell.
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Visualizzazioni Web
- Stile classico
- Stile Web
- intestazioni
- Area FileList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ebe106bdada4da55eef8891a3c93ee82aba3cc4da9194e1fcd4c7e71bcd4e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745688"
---
# <a name="customizing-a-folders-web-view"></a>Personalizzazione della visualizzazione Web di una cartella

\[Questa funzionalità è supportata solo in Windows XP o versioni precedenti. \]

Una visualizzazione Web è un modo potente e flessibile per usare Windows Explorer per visualizzare informazioni sul contenuto di una cartella shell.

-   [Introduzione](#introduction)
-   [Uso del modello di visualizzazione Web](#using-the-web-view-template)
    -   [Corpo del modello](#the-template-body)
    -   [Testa del modello](#the-template-head)
-   [Summary](#summary)

## <a name="introduction"></a>Introduzione

Windows offre agli utenti due modi principali per visualizzare ed esplorare lo spazio dei nomi shell. L'interfaccia più familiare, lo stile classico, è simile a quella Windows File Manager. Il riquadro destro elenca i contenuti della cartella attualmente selezionata in uno dei cinque formati seguenti: Icona grande, Icona piccola, Elenco, Dettagli e Anteprima. La differenza principale rispetto Windows File Manager è il riquadro sinistro, che ha un aspetto molto simile alla barra esplora risorse Windows Internet Explorer. Può essere ridimensionata o rimossa e può visualizzare diversi riquadri oltre al noto albero file system, ad esempio un riquadro di ricerca.

> [!Note]  
> Le informazioni contenute in questo documento non si applicano Windows XP, le tecniche illustrate si applicano solo alle versioni precedenti di Windows.

 

La figura seguente mostra la cartella Stampanti in stile classico.

![stile classico della cartella printers.](images/webview1.png)

Lo stile classico funziona ragionevolmente bene per le file system e i file normali. Tuttavia, con l'introduzione di Windows 95, il file system si è evoluto nello spazio dei nomi . Lo spazio dei nomi consente la creazione di cartelle *virtuali,* ad esempio Stampanti o Network Neighborhood, che possono rappresentare tipi di informazioni molto diversi rispetto a una normale file system cartella.

Lo stile Web, noto anche come visualizzazione Web, offre un modo più flessibile e potente per presentare informazioni rispetto allo stile classico. In una visualizzazione Web, l'utente essenzialmente visualizza e esplora lo spazio dei nomi usando Internet Explorer. Il layout di base di una visualizzazione Web è simile allo stile classico. La barra di Explorer rimane invariata. Tuttavia, l'area occupata dall'elenco di file diventa un'area di visualizzazione per utilizzo generico che è effettivamente una pagina Web. Una visualizzazione Web viene comunque utilizzata per visualizzare informazioni sul contenuto di una cartella, ma esistono alcuni vincoli sulle informazioni visualizzate o su come. Ogni cartella può avere una propria visualizzazione Web, personalizzata in base alle specifiche funzionalità.

La figura seguente mostra una visualizzazione Web della cartella Stampanti (illustrata in precedenza in stile classico).

![visualizzazione Web predefinita della cartella printers.](images/webview2.png)

Analogamente alle pagine Web convenzionali, le visualizzazioni Web sono controllate da un modello basato su HTML. La creazione di un modello di visualizzazione Web è quasi identica alla creazione di una pagina Web e offre lo stesso livello di flessibilità nel contenuto e nel layout delle informazioni. I modelli di visualizzazione Web possono usare html dinamico (DHTML) e script per rispondere a eventi, ad esempio un utente che fa clic su un elemento. Possono anche ospitare oggetti che consentono di ottenere e visualizzare informazioni dalla cartella o dal relativo contenuto.

L'utente può scegliere una visualizzazione Web avviando  Windows Explorer, scegliendo Opzioni cartella dal **menu** Visualizza e selezionando questa opzione: Abilita contenuto Web **nelle cartelle**. Tuttavia, l'utente può anche avviare Internet Explorer e puntare il browser al file system facendo clic sul **menu** Visualizza, scegliendo Barra di Explorer **e** facendo clic su **Cartelle.** In una visualizzazione Web non c'è praticamente alcuna differenza tra Internet Explorer e Windows Explorer.

Sul lato sinistro del riquadro destro la visualizzazione Web Stampanti visualizza un banner con il nome e l'icona della cartella, seguito da un blocco di informazioni sulla cartella. Il consueto elenco di file occupa il lato destro della pagina.

Quando un utente fa clic su un elemento, nel blocco di informazioni vengono visualizzate informazioni dettagliate sull'elemento. La visualizzazione Web Stampanti visualizza effettivamente molte delle stesse informazioni disponibili in stile classico, ma lo fa in un formato più utilizzabile. Tuttavia, una visualizzazione Web non è semplicemente un modo diverso per visualizzare le informazioni sullo stile classico. Ad esempio, un collegamento a un sito Web utile può essere visualizzato sotto il blocco di informazioni, una funzionalità che non è disponibile in stile classico. Se l'utente fa clic sul collegamento, verrà visualizzato il sito.

La visualizzazione Web Stampanti illustrata nella figura precedente è simile allo stile Classico, perché il modello di visualizzazione Web sottostante (un file con estensione htt) è stato scritto in questo modo. L'elenco di file, ad esempio, non viene generato direttamente dal modello di visualizzazione Web. Viene creato e visualizzato da un [**oggetto WebViewFolderContents**](webviewfoldercontents.md) ospitato dal modello di visualizzazione Web. I metodi e le proprietà dell'oggetto consentono alla visualizzazione Web di controllare il layout e ottenere informazioni su elementi specifici. Il contenuto e il layout del banner e del blocco di informazioni sono specificati nel modello di visualizzazione Web.

Poiché una visualizzazione Web supporta DHTML, il modello può essere usato anche per gestire l'interazione dell'utente. Ad esempio, quando un utente fa clic su una delle icone della stampante, l'oggetto **WebViewFolderIcon** genera un [**evento SelectionChanged.**](/windows/desktop/shell/application-support-bumper) Il modello usa un gestore eventi DHTML scritto nello script per recuperare le informazioni richieste e visualizzarle nel blocco di informazioni.

Questo semplice esempio per la cartella Stampanti non è affatto l'unico modo per usare una visualizzazione Web. Scrivendo un modello personalizzato e, se necessario, oggetti , è possibile usare una visualizzazione Web per visualizzare le informazioni e interagire con l'utente nel modo più efficace possibile. Si noti che, al momento, i modelli di visualizzazione Web visualizzano solo cartelle virtuali definite dal sistema. Anche se gli sviluppatori possono creare una cartella virtuale implementando un'estensione dello spazio dei nomi, devono usare le tecniche descritte [in](/windows/desktop/shell/nse-works) Estensioni dello spazio dei nomi per visualizzarla.

## <a name="using-the-web-view-template"></a>Uso del modello di visualizzazione Web

La modalità di visualizzazione dei dati in una visualizzazione Web può essere personalizzata in modo limitato modificando il file Desktop.ini cartella. Per [informazioni dettagliate, vedere Personalizzazione Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) cartelle con il servizio. Un modo molto più flessibile e potente per personalizzare una visualizzazione Web è creare un modello di visualizzazione Web personalizzato.

Il modello di visualizzazione Web controlla ciò che viene visualizzato in una visualizzazione Web e come. Usa tecniche standard html, DHTML e di scripting per ottenere e visualizzare informazioni e interagire con l'utente. Questa sezione illustra come creare una visualizzazione Web esaminando un modello semplice, Generic.htt.


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



Un modo semplice per creare un modello di visualizzazione Web personalizzato è prendere Generic.htt e modificarlo. Poiché è piuttosto limitato, è consigliabile esaminare anche altri esempi più complessi per idee aggiuntive. È possibile trovarli cercando nel sistema l'estensione htt usata da tutti i modelli di visualizzazione Web. Se si vuole creare un modello personalizzato per una cartella, iniziare con il modello Folder.htt predefinito, in genere archiviato in C: Winnt Web o \\ \\ C: \\ Windows \\ Web. Si noti che questi file sono definiti come nascosti, quindi potrebbe essere necessario modificare le impostazioni Windows Explorer per visualizzarli. Una volta creato, un file con estensione htt deve essere contrassegnato come di sola lettura e nascosto.

I modelli di visualizzazione Web usano l'estensione htt perché differiscono leggermente dai documenti .htm convenzionali. La differenza principale è data da diverse variabili speciali nei file con estensione htt che il sistema sostituisce con i valori dello spazio dei nomi corrente. Le variabili %THISDIR% e %THISDIRPATH% rappresentano il nome e il percorso della cartella attualmente selezionata. La variabile %TEMPLATEDIR% rappresenta la cartella in cui sono archiviati i fogli di stile della visualizzazione Web.

Come la maggior parte dei modelli HTML, i file con estensione htt hanno due parti di base: un corpo e una testa. Il corpo del modello controlla il layout di base della visualizzazione Web e carica gli oggetti utilizzati per comunicare con lo spazio dei nomi e visualizzare le informazioni. L'elemento head contiene script e funzioni che eseguiti attività quali la gestione del ridimensionamento e il recupero di informazioni dalla cartella. La maggior parte dei modelli, incluso Generic.htt, include anche un foglio di stile. In generale, è meglio includere le informazioni del foglio di stile nel modello. Fogli di stile separati potrebbero non funzionare correttamente quando si usa una visualizzazione Web con spazi dei nomi remoti.

### <a name="the-template-body"></a>Corpo del modello

Il corpo del modello specifica ciò che verrà presentato da una visualizzazione Web. È anche la posizione in cui vengono caricati gli oggetti utilizzati per visualizzare le informazioni e comunicare con le cartelle dello spazio dei nomi. Il layout definito da Generic.htt è simile a quello illustrato nella figura nella sezione precedente. Sono disponibili tre aree di visualizzazione: il banner e il blocco di informazioni sul lato sinistro della visualizzazione e l'elenco di file a destra.

Le aree sono tutti identificatori assegnati che devono essere usati dal foglio di stile e da DHTML. Come illustrato nella sezione successiva, sono disponibili due banner possibili, con identificatori "Banner" e "MiniBanner". L'identificatore dell'area del blocco di informazioni è "Info". L'identificatore dell'oggetto elenco di file è "FileList". I dettagli del [layout](#controlling-the-web-view-layout) dell'area vengono gestiti dal foglio di stile e da una funzione di Microsoft JScript, [FixSize,](#adjusting-the-layout-by-using-the-fixsize-function)descritta più avanti nel capitolo.

### <a name="the-banner-region"></a>Area banner

Il banner si trova nella parte superiore dello schermo, nell'angolo superiore sinistro della visualizzazione Web. Il banner normale visualizza il nome e l'icona della cartella il cui contenuto viene visualizzato nell'elenco di file a destra. Tuttavia, se la finestra diventa troppo breve, potrebbe non esserci spazio sotto l'icona per visualizzare le informazioni. Per questo motivo, Generic.htt definisce anche un minibanner che visualizza solo il nome della cartella. Entrambi i banner sono inizialmente definiti come nascosti. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) sceglie quale visualizzare e lo imposta su "visible".

Il banner normale per Generic.htt è definito da:


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



La prima parte della sezione banner visualizza il titolo con una regola orizzontale sotto di essa. I tag di tabella vengono usati per controllarne la posizione. L'attributo nowrap è impostato per <TD> tag per impedire il ritorno a capo automatico. Il sistema sostituirà %THISDIRNAME% con il nome della cartella corrente. Un **oggetto WebViewFolderIcon,** con l'identificatore "Icon" per semplicità, viene quindi caricato per estrarre e visualizzare l'icona della cartella.

La sezione minibanner è simile al banner normale. Il formato del titolo è leggermente superiore e non ha una regola. Poiché non è presente alcuna icona, **l'oggetto WebViewFolderIcon** non viene caricato.


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a>Area informazioni

La parte della visualizzazione Web sotto il banner viene usata per presentare informazioni dettagliate sull'elemento selezionato. Se non è selezionato alcun elemento, viene visualizzato un messaggio predefinito. Poiché Generic.htt visualizza solo un singolo blocco di testo, questa sezione è piuttosto semplice.


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



La maggior parte delle operazioni di raccolta delle informazioni viene gestita da uno [script di](#retrieving-and-displaying-folder-information) informazioni sulle cartelle descritto più avanti nel capitolo. Visualizza le informazioni assegnando il testo a [TextBlock.innerHTML.](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)

È possibile personalizzare facilmente la visualizzazione delle informazioni modificando questi elementi o includendo altri elementi. È possibile usare qualsiasi elemento che è possibile inserire in una pagina Web. Ad esempio, per visualizzare un collegamento al sito Web, è possibile aggiungere un elemento di ancoraggio dopo il blocco di testo in Generic.htt.


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



### <a name="the-filelist-region"></a>Area FileList

Generic.htt carica infine un [**oggetto WebViewFolderContents**](webviewfoldercontents.md) per l'area FileList. Poiché il relativo identificatore è impostato su "FileList", d'ora in poi verrà definito oggetto FileList.


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



L'oggetto FileList si trova nella maggior parte delle visualizzazioni Web e ha diversi scopi. FileList visualizza l'elenco di elementi contenuti nella cartella selezionata con le stesse opzioni e lo stesso aspetto dell'elenco di file nello stile classico. Quando viene selezionato un elemento, FileList invia una notifica alla visualizzazione Web generando un [evento SelectionChanged.](#retrieving-and-displaying-folder-information) FileList espone anche metodi e proprietà che possono essere usati per recuperare informazioni sui singoli elementi e controllare la posizione e le dimensioni dell'area di visualizzazione.

Anche se l'oggetto FileList è molto utile, restituisce solo informazioni standard file system, ad esempio le dimensioni del file o gli attributi. Per recuperare altri tipi di informazioni da una cartella Shell, è necessario caricare e gestire oggetti aggiuntivi. Qualsiasi oggetto che può essere ospitato da una pagina Web può essere usato con una visualizzazione Web.

### <a name="the-template-head"></a>Testa del modello

L'elemento head del modello di visualizzazione Web contiene gli script e le funzioni che eseranno la maggior parte del lavoro effettivo. È necessario gestire due attività essenziali. Uno è il layout della visualizzazione Web, che deve essere regolato in base alle diverse aree di visualizzazione. L'altro è il recupero e la visualizzazione di informazioni dalla cartella quando viene selezionato un elemento. Come per i fogli di stile, è meglio includere tutti gli script e le funzioni nel modello anziché fare riferimento a essi come file separati.

### <a name="controlling-the-web-view-layout"></a>Controllo del layout della visualizzazione Web

L'area disponibile per una visualizzazione Web dipende dalle dimensioni della finestra di visualizzazione Web e dalla quantità di dati che viene prelevata dalla barra Windows Explorer. Quest'area verrà cambiata ogni volta che la finestra o Windows barra di Explorer viene ridimensionata. È quindi necessario associare il layout all'area disponibile quando viene caricata una visualizzazione Web e modificarla in modo appropriato quando viene ridimensionata. Gran parte del layout viene specificato nel foglio di stile. L'area Informazioni, ad esempio, viene definita in modo da occupare il 30% più a sinistra della visualizzazione Web.


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



Quando una visualizzazione Web viene ridimensionata, la larghezza dell'area Informazioni cambia per mantenere tale percentuale. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) gestisce i problemi di layout che non possono essere gestiti da un foglio di stile.

### <a name="loading-and-initializing-the-web-view"></a>Caricamento e inizializzazione della visualizzazione Web

Quando viene caricata una visualizzazione Web, il layout deve essere adattato all'area di visualizzazione disponibile. Poiché non è stato ancora selezionato alcun elemento, le visualizzazioni Web visualizzano in genere alcune informazioni predefinite che si applicano all'intera cartella. Per gestire l'inizializzazione, <BODY> il tag per Generic.htt rileva [l'evento onload](/previous-versions//ms531409(v=vs.85)) e chiama la **funzione Init.**


```
<body scroll=no onload="Init">
                    
```



**Init** è una funzione JScript semplice.


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



**Init** associa [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) all'evento [window.onresize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) in modo che sia chiamato ogni volta che l'area di visualizzazione della visualizzazione Web cambia. Esegue quindi FixSize per impostare il layout iniziale e assegna L \_ Intro \_ Text all'area Info. L \_ Intro Text è un blocco di testo \_ introduttivo definito nella sezione del foglio di stile.


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a>Regolazione del layout tramite la funzione FixSize

La [funzione FixSize](#adjusting-the-layout-by-using-the-fixsize-function) viene usata per specificare diversi aspetti del layout che non possono essere gestiti dal foglio di stile.

È possibile usare due banner, a seconda dell'altezza della visualizzazione Web.


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



Generic.htt usa un'altezza di 200 pixel come linea di divisione tra normali e minibanner. Imposta lo stile del banner selezionato su visibile e l'altro su nascosto. Imposta anche diverse proprietà di layout per le aree Info e FileList in modo che si adattino correttamente al banner selezionato.

Se una visualizzazione Web diventa troppo stretta, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) usa l'intera larghezza dell'area di visualizzazione per la visualizzazione FileList.


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



Generic.htt usa 400 pixel come linea di divisione tra schermi narrow e wide. Se la visualizzazione Web è troppo stretta, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) nasconde l'area informazioni e modifica la proprietà [PixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) di FileList in modo che riempia l'intera area sotto il banner.

Le ultime righe di [FixSize regolano](#adjusting-the-layout-by-using-the-fixsize-function) diverse proprietà di layout in base ai risultati del codice precedente. La larghezza dell'area FileList viene regolata in modo che riempia esattamente la parte della visualizzazione Web non occupata dall'area Informazioni. L'altezza dell'area Informazioni viene ridimensionata in modo da adattarsi tra il banner e la parte inferiore della visualizzazione Web.


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a>Recupero e visualizzazione di informazioni sulle cartelle

Quando un utente seleziona un elemento, l'oggetto FileList genera un [evento SelectionChanged.](#retrieving-and-displaying-folder-information) Questo evento viene gestito da uno script JScript. Per semplicità, lo script disponibile in Generic.htt presuppone che sia possibile selezionare un solo elemento alla volta.


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



Lo script usa due proprietà FileList, [**FileList.FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)e [**FileList.Folder,**](/windows/desktop/shell/shellfolderview-folder) per ottenere informazioni sull'elemento. **FileList.FocusedItem** identifica l'elemento selezionato, con il nome dell'elemento specificato **da FileList.FocusedItem.Name**. **FileList.Folder è** in realtà un puntatore a un [**oggetto**](../shell/folder.md) Folder. Il metodo [**GetDetailsOf dell'oggetto Folder**](/windows/desktop/shell/folder-getdetailsof) viene usato per recuperare le informazioni rimanenti sull'elemento.

Tutte le informazioni vengono concatenate in un'unica stringa di testo, separata da <BR> tag per una leggibilità. Il testo viene quindi visualizzato assegnandolo a [TextBlock.innerHTML.](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)

## <a name="summary"></a>Riepilogo

Questo capitolo illustra alcune delle tecniche che è possibile usare per personalizzare il modo in cui Windows Explorer visualizza le informazioni sulle cartelle della shell. La creazione Desktop.ini file consente di eseguire alcune semplici personalizzazioni, ad esempio la visualizzazione di un'icona personalizzata al posto dell'icona della cartella standard. Quando una cartella viene visualizzata in una visualizzazione Web, il layout e la visualizzazione vengono controllati da un modello basato su HTML che determina quali informazioni vengono visualizzate e come. È possibile esercitare un elevato livello di controllo sulla visualizzazione Web di una cartella usando tecniche standard html, DHTML e di scripting per creare un modello personalizzato.

 

 