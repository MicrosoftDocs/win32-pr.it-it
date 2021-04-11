---
description: Nell'applicazione di esempio del Blog Ink viene illustrato come creare una classe UserControl gestita con funzionalità Inking e ospitare tale controllo in Microsoft Internet Explorer.
ms.assetid: b6c3ad92-3ab1-4311-b318-13939e1a1a5a
title: Esempio di Web Ink Blog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24f132d355a95c9cb8debebe074df3f976e3b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128435"
---
# <a name="ink-blog-web-sample"></a>Esempio di Web Ink Blog

Nell'applicazione di esempio del Blog Ink viene illustrato come creare una classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) gestita con funzionalità Inking e ospitare tale controllo in Microsoft Internet Explorer. Nell'esempio viene inoltre illustrata una tecnica per l'invio di dati Ink in una rete tramite HTTP e per l'input penna permanente in un server.

> [!Note]  
> Per eseguire questo esempio, è necessario disporre di Microsoft Internet Information Services (IIS) con ASP.NET installato. Verificare che il computer soddisfi i requisiti necessari per l'esecuzione delle applicazioni ASP.NET nel computer.

 

> [!Note]  
> Se si esegue questo esempio in un computer non Tablet PC con Microsoft Windows XP Tablet PC Edition Development Kit 1,7 installato, la funzionalità di riconoscimento del testo per il titolo dell'input penna non funzionerà. Questo problema si verifica perché in un computer non Tablet PC in cui è installato Tablet PC SDK 1,7 mancano i riconoscitori. Il resto dell'applicazione viene eseguito come descritto.

 

## <a name="overview"></a>Panoramica

L'esempio di Blog Ink crea un weblog abilitato per l'input penna. InkBlogWeb è un'applicazione ASP.NET. La voce input penna viene eseguita tramite un controllo utente a cui viene fatto riferimento da una pagina ASP.NET.

Il controllo utente rileva se i componenti della piattaforma Tablet PC sono installati nel computer client. In tal caso, il controllo utente Visualizza l'utente con due aree abilitate per l'input penna nella pagina Web: una per Inking un titolo per la voce di Blog e una per il corpo della voce. Se i componenti della piattaforma Tablet PC non sono installati, all'utente viene assegnato un controllo casella di testo standard per il titolo e il corpo della voce.

Quando l'utente completa la creazione della voce, fa clic su un pulsante, Aggiungi il Blog e il post viene inviato al server Web per l'archiviazione. Nel server, l'applicazione salva il testo del titolo e la data di pubblicazione, nonché un riferimento a un file di Graphics Interchange Format (GIF). Il file GIF, anch ' esso salvato nel server, contiene i dati di input penna del corpo in un file GIF fortificato. Per altre informazioni sul formato GIF fortificato, vedere [archiviazione dell'input penna in HTML](storing-ink-in-html.md).

Nella soluzione InkBlog sono presenti due progetti: il progetto **InkBlogControls** e il progetto **InkBlogWeb** .

## <a name="inkblogcontrols-project"></a>Progetto InkBlogControls

Il progetto **InkBlogControls** è un progetto [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) che contiene il codice per il controllo utente che Abilita Inking nella pagina Web. Il codice per questo controllo, il controllo inkarea, si trova nel file inkarea. cs.

La `InkArea` classe eredita dalla classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) . Il costruttore per il `InkArea` controllo chiama un metodo helper, `CreateInkCollectionSurface` .


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



Il `CreateInkCollectionSurface` metodo determina se i componenti di Tablet PC sono disponibili sul client tentando di creare un'istanza della classe [InkCollector](/previous-versions/ms583683(v=vs.100)) . Se la chiamata al `CreateInkCollectionSurface` metodo ha esito positivo, il metodo restituisce un oggetto [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) come controllo.


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



Se il costruttore non riesce perché i file della piattaforma Inking non vengono trovati, `InputArea` viene creata un'istanza del controllo come controllo [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) anziché come controllo [InkCollector](/previous-versions/ms583683(v=vs.100)) . Il costruttore Ridimensiona quindi il controllo alla dimensione del controllo utente padre e lo aggiunge alla raccolta di controlli padre.

La classe del controllo inkarea implementa tre proprietà pubbliche interessanti: InkData, TextData e webenabled.

La proprietà InkData è di sola lettura e fornisce l'accesso ai dati di input penna serializzati, se il client supporta Inking. Se il client non supporta Inking, la proprietà InkData ottiene una stringa vuota. La proprietà InkData chiama un metodo helper, SerializeInkData, per determinare se il client supporta Inking.


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



Nel `SerializeInkData` metodo, il cast a [InkCollector](/previous-versions/ms583683(v=vs.100)) è necessario quando si ottiene l'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) , perché `inputArea` è dichiarato come [controllo](/dotnet/api/system.windows.forms.control?view=netcore-3.1). Se l'oggetto Ink contiene tratti, i dati di input penna vengono salvati nella `inkDataBytes` matrice di byte come un gif (specificato tramite il valore di enumerazione [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) ). Il metodo converte quindi la matrice di byte in una stringa con codifica Base64 e restituisce questa stringa.

Supponendo che il client sia in grado di eseguire il riconoscimento, la `TextData` proprietà restituisce l'oggetto [RecognitionResult](/previous-versions/ms552537(v=vs.100)) dal passaggio dei dati Ink a un riconoscimento della grafia. Se il client non è compatibile con l'input penna, viene restituito il contenuto della casella di testo, come illustrato nel codice seguente.


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



La `TextData` proprietà chiama un metodo helper, `RecognizeInkData` , illustrato nel codice seguente, per eseguire il riconoscimento. Quando i motori di riconoscimento sono presenti nel sistema, il `RecognizeInkData` metodo restituisce una stringa che contiene la proprietà di [stringa](/previous-versions/ms572009(v=vs.100)) dell'oggetto [RecognitionResult](/previous-versions/ms552537(v=vs.100)) . Altrimenti restituisce una stringa vuota.


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



La `InkEnabled` proprietà è un valore booleano di sola lettura che indica se Inking è supportato nel computer client.

Un altro importante membro pubblico della `InkArea` classe Control è il `DisposeResources` metodo. Questo metodo chiama internamente il `Dispose` metodo per garantire la pulizia di tutte le risorse utilizzate dal controllo utente. Qualsiasi applicazione che utilizza il `InkArea` controllo deve chiamare il `DisposeResources` metodo al termine dell'utilizzo del controllo.

## <a name="inkblogweb-project"></a>Progetto InkBlogWeb

Il progetto InkBlogWeb è un progetto di distribuzione del programma di installazione Web che fa riferimento al `InkArea` controllo per fornire la funzionalità di Blog. Per ulteriori informazioni sui progetti di distribuzione del programma di installazione Web, vedere [distribuzione di un progetto di installazione Web](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).

Sono disponibili due file aspx che implementano l'esempio blogging: default. aspx e AddBlog. aspx. Default. aspx è la pagina predefinita per l'applicazione InkBlogWeb. Il file code-behind per questa pagina è default. aspx. cs. Questa pagina contiene un collegamento alla pagina che contiene il nuovo modulo di inserimento nel Blog e visualizza eventuali voci di Blog esistenti. Questo processo viene descritto in seguito, dopo l'esame della pagina del nuovo modulo del post del Blog, AddBlog. aspx.

AddBlog. aspx e il relativo file code-behind, AddBlog. aspx. cs, contengono la logica e il codice dell'interfaccia utente per la creazione di nuove voci di Blog. AddBlox. aspx fa riferimento a due istanze della classe del controllo inkarea creata nel progetto InkBlogControls usando l'elemento oggetto HTML, come illustrato nell'esempio seguente. Un'istanza ha un `id` attributo di inkBlogTitle e l'altra ha un attributo ID di inkBlogBody.

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

Il InkBlogControls.dll assembly deve essere presente nella stessa directory della pagina aspx a cui fa riferimento. Il progetto di distribuzione del programma di installazione Web garantisce che questo sia il caso, come evidenziato dalla presenza dell'elemento "output primario da InkBlogControls" nel progetto di distribuzione.

Il controllo del titolo è di 48 pixel di altezza per facilitare l'immissione di una singola riga di input penna per il titolo. Il controllo del corpo è di 296 pixel di altezza per fare spazio a voci di Blog più grandi di più righe o forse di disegni.

I controlli inkarea sono connessi a una funzione script sul lato client, AddBlog, mediante un gestore dell'evento OnClick dell'elemento BUTTON HTML standard.

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

Nella pagina è presente anche un form HTML che contiene tre elementi di INPUT nascosti: BlogTitleText, BlogBodyText e BlogBodyInkData. Questo modulo viene usato per pubblicare i dati di immissione nel Blog sul server. AddBlog. aspx è il gestore di postback definito per il form.

La funzione AddBlog, scritta in Microsoft JScript <entity type="reg"/> , estrae i dati del Blog dai controlli Inkarea e invia i risultati al server.


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



Quando i dati arrivano al server, il codice in AddBlog. aspx. cs controlla il gestore dell' \_ evento di caricamento della pagina per verificare se la proprietà form dell'oggetto HttpRequest contiene dati. In tal caso, crea un nome di file basato sull'ora di sistema corrente, inserisce i dati del modulo in tre variabili stringa e scrive i dati in un file HTML e un file GIF contenente i dati di input penna, se presenti, come illustrato nel codice seguente.


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

Per impostazione predefinita, Tablet PC SDK 1,7 installa l'esempio di Web Ink Blog. Per eseguire l'esempio, in Internet Explorer passare a https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx . Se si esegue Windows Server 2003, sostituire "localhost" con il nome del computer.

> [!Note]  
> Gli esempi Web compilati non vengono installati tramite l'opzione di installazione predefinita per l'SDK. È necessario completare un'installazione personalizzata e selezionare l'opzione secondaria "esempi Web precompilati" per installarli.

 

È anche possibile eseguire l'esempio aprendo e compilando il progetto in Microsoft Visual Studio <entity type="reg"/> .NET e quindi distribuendo il progetto in un computer separato che esegue IIS.

## <a name="troubleshooting-the-sample"></a>Risoluzione dei problemi relativi all'esempio

Tre aree che possono causare difficoltà durante l'esecuzione o l'hosting dell'esempio sono le autorizzazioni e il riconoscimento.

### <a name="permissions"></a>Autorizzazioni

L'esempio richiede le autorizzazioni di scrittura all'interno della cartella radice virtuale per l'account che sta tentando di creare una nuova voce di Blog. Per impostazione predefinita, la versione compilata dell'esempio disponibile in Tablet PC SDK 1,7 dispone delle autorizzazioni corrette impostate per soddisfare questo requisito.

Se si compila e si distribuisce l'esempio usando il progetto di distribuzione dell'installazione Web fornito, è necessario assegnare al gruppo% MACHINENAME% \\ Users il gruppo di accesso in scrittura alla cartella file System a cui fa riferimento la radice virtuale InkBlogWeb (ad esempio, C: \\ Inetpub \\ wwwroot \\ InkBlogWeb). Il gruppo Users include l'account anonimo usato da IIS, consentendo così all'applicazione ASP.NET di scrivere le nuove voci di Blog nel file system. In alternativa, è possibile rimuovere l'accesso anonimo alla radice virtuale e forzare l'autenticazione.

### <a name="recognition"></a>Riconoscimento

Per riconoscere l'input penna nel titolo del Blog, è necessario installare i riconoscitori della grafia. Se si accede all'applicazione InkBlog da un computer con un sistema operativo diverso da Windows XP Tablet PC Edition ma con Tablet PC SDK 1,7 installato, è possibile scrivere in input penna nei controlli inkarea, ma i motori di riconoscimento non saranno presenti e non verrà visualizzato alcun titolo per le voci di Blog. Tuttavia, il contenuto dell'input penna nel corpo viene comunque visualizzato.

### <a name="machine-configuration"></a>Configurazione computer

Se è stato installato ASP.NET e il .NET Framework in un computer e si disinstalla e si reinstalla IIS, le mappe di script si interrompono e ASP.NET non funzionerà. In tal caso, è possibile ripristinare le mappe di script ASP.NET con lo strumento di registrazione IIS ASP.NET (ASPNET \_regiis.exe-i).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[InkCollector](/previous-versions/ms583683(v=vs.100))
</dt> <dt>

[Input penna sul Web](ink-on-the-web.md)
</dt> <dt>

[Formati di dati Ink](ink-data-formats.md)
</dt> <dt>

[Classe System. Windows. Forms. UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
