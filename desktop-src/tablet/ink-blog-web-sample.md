---
description: L'applicazione di esempio Ink Blog illustra come creare una classe UserControl gestita con funzionalità di input penna e che ospita tale controllo in Microsoft Internet Explorer.
ms.assetid: b6c3ad92-3ab1-4311-b318-13939e1a1a5a
title: Esempio Web di blog ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8796a05861d278015205b5ba0d3775e2e47af6a57ce1fee426c5c0c5011dacd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032359"
---
# <a name="ink-blog-web-sample"></a>Esempio Web di blog ink

L'applicazione di esempio Ink Blog illustra come creare una classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) gestita con funzionalità di input penna e che ospita tale controllo in Microsoft Internet Explorer. L'esempio illustra anche una tecnica per l'invio di dati input penna attraverso una rete tramite HTTP e per rendere persistente l'input penna in un server.

> [!Note]  
> Per eseguire questo esempio è Microsoft Internet Information Services (IIS) con ASP.NET installato. Assicurarsi che il computer soddisfi i requisiti necessari per ASP.NET applicazioni da eseguire nel computer.

 

> [!Note]  
> Se si esegue questo esempio in un computer non Tablet PC con Microsoft Windows XP Tablet PC Edition Development Kit 1.7 installato, la funzionalità di riconoscimento del testo per il titolo dell'input penna non funzionerà. Ciò si verifica perché un computer non Tablet PC in cui è installato Tablet PC SDK 1.7 non dispone di riconoscitori. Il resto dell'applicazione viene eseguito come descritto.

 

## <a name="overview"></a>Panoramica

L'esempio Ink Blog crea un Weblog abilitato per l'input penna. InkBlogWeb è un'ASP.NET applicazione. L'immissione dell'input penna viene eseguita tramite un controllo utente a cui viene fatto riferimento da ASP.NET pagina.

Il controllo utente rileva se i componenti della piattaforma Tablet PC sono installati nel computer client. In tal caso, il controllo utente presenta all'utente due aree abilitate per l'input penna nella pagina Web: una per l'input penna di un titolo per la voce del blog e una per il corpo della voce. Se i componenti della piattaforma Tablet PC non sono installati, all'utente viene assegnato un controllo casella di testo standard per il titolo e il corpo della voce.

Al termine della creazione della voce, l'utente fa clic su un pulsante Aggiungi blog e il post viene inviato al server Web per l'archiviazione. Nel server, l'applicazione salva il testo del titolo e la data di pubblicazione, nonché un riferimento a un file Graphics Interchange Format (GIF). Il file GIF, salvato anche nel server, contiene i dati dell'input penna del corpo in un file GIF arricchito. Per altre informazioni sul formato GIF arricchito, vedere [Archiviazione dell'input penna in HTML.](storing-ink-in-html.md)

Esistono due progetti nella soluzione InkBlog: il **progetto InkBlogControls** e il **progetto InkBlogWeb.**

## <a name="inkblogcontrols-project"></a>Controllo InkBlogControls Project

Il **progetto InkBlogControls** è un [progetto UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) che contiene il codice per il controllo utente che abilita l'input penna nella pagina Web. Il codice per questo controllo, il controllo InkArea, si trova nel file InkArea.cs.

La `InkArea` classe eredita dalla classe [UserControl.](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) Il costruttore per il `InkArea` controllo chiama un metodo helper, `CreateInkCollectionSurface` .


```C++
public InkArea()
{
    // Standard template code

    try
    {
        inputArea = CreateInkCollectionSurface();
    }
    catch (FileNotFoundException)
    { 
        inputArea = new TextBox();
        ((TextBox)inputArea).Multiline = true;
    }

    inputArea.Size = this.Size;

    // Add the control used for collecting blog input
    this.Controls.Add(inputArea);
}
```



Il metodo determina se i componenti input penna di Tablet PC sono disponibili nel client provando a creare un'istanza `CreateInkCollectionSurface` della [classe InkCollector.](/previous-versions/ms583683(v=vs.100)) Se la chiamata al `CreateInkCollectionSurface` metodo ha esito positivo, il metodo restituisce un [oggetto Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) come controllo.


```C++
protected Control CreateInkCollectionSurface()
{
    try
    {
        Panel inkPanel = new Panel();
        inkPanel.BorderStyle = BorderStyle.Fixed3D;
        inkCollector = new InkCollector(inkPanel);
        ((InkCollector)inkCollector).Enabled = true;
        return inkPanel;
    }
    catch
    {
        throw;
    }
}
```



Se il costruttore ha esito negativo perché i file della piattaforma di input penna non vengono trovati, viene creata un'istanza del controllo come controllo TextBox anziché come `InputArea` [controllo InkCollector.](/previous-versions/ms583683(v=vs.100)) [](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) Il costruttore ridimensiona quindi il controllo in base alle dimensioni del controllo utente padre e lo aggiunge alla raccolta Controls dell'elemento padre.

La classe del controllo InkArea implementa tre interessanti proprietà pubbliche: InkData, TextData e WebEnabled.

La proprietà InkData è di sola lettura e fornisce l'accesso ai dati dell'input penna serializzati, se il client supporta l'input penna. Se il client non supporta l'input penna, la proprietà InkData ottiene una stringa vuota. La proprietà InkData chiama un metodo helper, SerializeInkData, per determinare se il client supporta l'input penna.


```C++
protected String SerializeInkData()
{
    Debug.Assert(InkEnabled, null, "Client must be ink-enabled");

    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    // Serialize the ink
    if (ink.Strokes.Count > 0) 
    {
        byte[] inkDataBytes = ink.Save(PersistenceFormat.Gif);
        return Convert.ToBase64String(inkDataBytes);
    }

    // Default to returning the empty string.
    return String.Empty;
}
```



Nel metodo `SerializeInkData` il cast a [InkCollector](/previous-versions/ms583683(v=vs.100)) è necessario quando si ottiene l'oggetto [Ink,](/previous-versions/ms583670(v=vs.100)) perché `inputArea` è dichiarato come [control.](/dotnet/api/system.windows.forms.control?view=netcore-3.1) Se l'oggetto Ink contiene tratti, i dati dell'input penna vengono salvati nella matrice di byte come GIF (specificata usando il valore di `inkDataBytes` [enumerazione PersistenceFormat).](/previous-versions/ms552503(v=vs.100)) Il metodo converte quindi la matrice di byte in una stringa con codifica Base64 e restituisce questa stringa.

Supponendo che il client possa eseguire il riconoscimento, la proprietà restituisce l'oggetto RecognitionResult passando i dati dell'input penna a un sistema di riconoscimento `TextData` della grafia. [](/previous-versions/ms552537(v=vs.100)) Se il client non è in grado di riconoscere l'input penna, viene restituito il contenuto della casella di testo, come illustrato nel codice seguente.


```C++
public string TextData
{
    get
    {
        if (this.WebEnabled) 
        {
            return RecognizeInkData();
        }
        else
        {
            return ((TextBox)inputArea).Text;
        }
    }
}
```



La `TextData` proprietà chiama un metodo `RecognizeInkData` helper, , illustrato nel codice seguente, per eseguire il riconoscimento. Quando i motori di riconoscimento sono presenti nel sistema, il metodo restituisce una stringa contenente `RecognizeInkData` la proprietà [TopString dell'oggetto](/previous-versions/ms572009(v=vs.100)) [RecognitionResult.](/previous-versions/ms552537(v=vs.100)) Altrimenti restituisce una stringa vuota.


```C++
protected String RecognizeInkData()
{
    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    if (ink.Strokes.Count > 0) 
    {

        // Attempt to create a recognition context and use it to
        // retrieve the top alternate.
        try 
        {
            RecognizerContext recognizerContext = new RecognizerContext();
            RecognitionStatus recognitionStatus;
            recognizerContext.Strokes = ink.Strokes;
            RecognitionResult recognitionResult = recognizerContext.Recognize(out recognitionStatus);
            if (recognitionStatus == RecognitionStatus.NoError) && ( null != recognitionResult) )
            {
                return recognitionResult.TopString;
            }
        }
        catch (Exception)
        {
            // An exception will occur if the client does not have
            // any handwriting recognizers installed on their system.
            // In this case, we default to returning an empty string. 
        }
    }

    return String.Empty;
}
```



La `InkEnabled` proprietà è un valore booleano di sola lettura che indica se l'input penna è supportato nel computer client.

Un altro membro pubblico importante della `InkArea` classe del controllo è il metodo `DisposeResources` . Questo metodo chiama internamente il metodo per garantire che tutte le risorse `Dispose` sfruttate dal controllo utente siano pulite. Qualsiasi applicazione che usa `InkArea` il controllo deve chiamare il metodo al termine `DisposeResources` dell'utilizzo del controllo.

## <a name="inkblogweb-project"></a>InkBlogWeb Project

Il progetto InkBlogWeb è un progetto di distribuzione di installazione Web che fa riferimento al `InkArea` controllo per fornire la funzionalità di blog. Per altre informazioni sui progetti di distribuzione di Installazione Web, vedere [Distribuzione di un'installazione Web Project](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).

Sono disponibili due file aspx che implementano l'esempio di blog: Default.aspx e AddBlog.aspx. Default.aspx è la pagina predefinita per l'applicazione InkBlogWeb. Il file code-behind per questa pagina è Default.aspx.cs. Questa pagina fornisce un collegamento alla pagina contenente il nuovo modulo di immissione del blog e visualizza eventuali voci di blog esistenti. Questo processo viene descritto più avanti, dopo l'esame seguente della nuova pagina del modulo di immissione nel blog, AddBlog.aspx.

AddBlog.aspx e il relativo file code-behind, AddBlog.aspx.cs, contengono la logica e il codice dell'interfaccia utente per la creazione di nuove voci del blog. AddBlox.aspx fa riferimento a due istanze della classe del controllo InkArea creata nel progetto InkBlogControls usando l'elemento OBJECT HTML, come illustrato nell'esempio seguente. Un'istanza ha `id` un attributo inkBlogTitle e l'altra ha un attributo id inkBlogBody.

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

LInkBlogControls.dll assembly deve essere presente nella stessa directory della pagina aspx che vi fa riferimento. Il progetto di distribuzione installazione Web garantisce che questo sia il caso, come dimostra la presenza dell'elemento "Primary output from InkBlogControls" (Output primario da InkBlogControls) in Deployment Project.

Il controllo titolo è alto solo 48 pixel per facilitare l'immissione di una singola riga di input penna per il titolo. Il controllo del corpo è alto 296 pixel per fare spazio a voci di blog più grandi di più linee o forse disegni.

I controlli InkArea sono connessi a una funzione script sul lato client, AddBlog, tramite il gestore eventi onclick di un elemento HTML BUTTON standard.

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

Nella pagina è presente anche un modulo HTML che contiene tre elementi INPUT nascosti: BlogTitleText, BlogBodyText e BlogBodyInkData. Questo modulo viene usato per pubblicare i dati dell'inserimento nel blog nel server. AddBlog.aspx è il gestore di post-backup definito per il form.

La funzione AddBlog scritta in Microsoft JScript - estrae i dati del blog dai controlli InkArea e invia <entity type="reg"/> i risultati al server.


```C++
function AddBlog() 
{
    // Extract the blog's title data as ink and text
    form.BlogTitleText.value  = inkBlogTitle.TextData;
    
    // Extract the blog's body data as ink and text
    form.BlogBodyText.value = inkBlogBody.TextData;
    form.BlogBodyInkData.value = inkBlogBody.InkData;   

    form.submit();
}
```



Quando i dati arrivano al server, il codice in AddBlog.aspx.cs controlla il gestore dell'evento Page Load per verificare se la proprietà \_ Form dell'oggetto HttpRequest contiene dati. In questo caso, crea un nome file basato sull'ora di sistema corrente, inserisce i dati del modulo in tre variabili stringa e scrive i dati in un file HTML e in un file GIF contenente i dati dell'input penna, se presenti, come illustrato nel codice seguente.


```C++
if ( (String.Empty != inkBody) )
{           
    // Use helper method to create a GIF image file from ink data 
    CreateGif(imagePath, fileName, inkBody);
    
    // Create an HTML fragment to reference the image file
    content = "<img src=\"Blogs/Images/" + fileName + ".gif\"></img>";
}                
else 
{
    // If no ink data is available create an HTML fragment that contains
    // the blog's text directly.
    content = "<P>" + textBody + "</P>";
}

// Use helper method to create the blog web page on the server
CreateHtm(blogPath, fileName, blogTitle, content);
```



Per altri dettagli sui metodi helper, vedere il codice sorgente di esempio.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Tablet PC SDK 1.7 installa l'esempio Web Ink Blog per impostazione predefinita. Per eseguire l'esempio, in Internet Explorer passare a https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx . Se si esegue Windows Server 2003, sostituire il nome del computer con "localhost".

> [!Note]  
> Gli esempi Web compilati non vengono installati dall'opzione di installazione predefinita per l'SDK. È necessario completare un'installazione personalizzata e selezionare l'opzione secondaria "Pre-compiled Web Samples" (Esempi Web precompilato) per installarli.

 

È anche possibile eseguire l'esempio aprendo e compilando il progetto in Microsoft Visual Studio .NET e quindi distribuerlo <entity type="reg"/> in un computer separato che esegue IIS.

## <a name="troubleshooting-the-sample"></a>Risoluzione dei problemi relativi all'esempio

Tre aree che possono causare difficoltà durante l'esecuzione o l'hosting dell'esempio sono le autorizzazioni e il riconoscimento.

### <a name="permissions"></a>Autorizzazioni

L'esempio richiede autorizzazioni di scrittura all'interno della cartella radice virtuale per l'account che sta tentando di creare una nuova voce del blog. Per impostazione predefinita, la versione compilata dell'esempio fornito in Tablet PC SDK 1.7 ha le autorizzazioni corrette impostate per soddisfare questo requisito.

Se si compila e si distribuisce l'esempio usando il progetto di distribuzione dell'installazione Web fornito, è necessario concedere al gruppo %MACHINENAME% Users l'accesso in scrittura alla cartella file system a cui punta la radice virtuale \\ InkBlogWeb (ad esempio, C: \\ InetPub \\ WWWRoot \\ InkBlogWeb). Il gruppo Utenti include l'account anonimo usato da IIS, consentendo così all'applicazione ASP.NET di scrivere le nuove voci di blog nel file system. Un'alternativa consiste nel rimuovere l'accesso anonimo alla radice virtuale e forzare l'autenticazione.

### <a name="recognition"></a>Riconoscimento

I riconoscitori della grafia devono essere installati per riconoscere l'input penna nel titolo del blog. Se si accede all'applicazione InkBlog da un computer con un sistema operativo diverso da Windows XP Tablet PC Edition ma con Tablet PC SDK 1.7 installato, è possibile scrivere a penna nei controlli InkArea, ma i motori di riconoscimento non saranno presenti e non verrà visualizzato alcun titolo per le voci del blog. Il contenuto dell'input penna nel corpo viene comunque visualizzato.

### <a name="machine-configuration"></a>Configurazione del computer

Se è stato installato ASP.NET e il .NET Framework in un computer e quindi si disinstalla e reinstalla IIS, le mappe di script si interromperanno e ASP.NET non funzioneranno. In questo caso, è possibile ripristinare le mappe ASP.NET script con lo strumento ASP.NET registrazione IIS (Aspnet \_regiis.exe -i).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Inkcollector](/previous-versions/ms583683(v=vs.100))
</dt> <dt>

[Input penna sul Web](ink-on-the-web.md)
</dt> <dt>

[Formati di dati input penna](ink-data-formats.md)
</dt> <dt>

[Sistema. Windows. Classe Forms.UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
