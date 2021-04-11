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
# <a name="ink-blog-web-sample"></a><span data-ttu-id="db0be-103">Esempio di Web Ink Blog</span><span class="sxs-lookup"><span data-stu-id="db0be-103">Ink Blog Web Sample</span></span>

<span data-ttu-id="db0be-104">Nell'applicazione di esempio del Blog Ink viene illustrato come creare una classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) gestita con funzionalità Inking e ospitare tale controllo in Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="db0be-104">The Ink Blog sample application demonstrates how to create a managed [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class that has inking capability and host that control in Microsoft Internet Explorer.</span></span> <span data-ttu-id="db0be-105">Nell'esempio viene inoltre illustrata una tecnica per l'invio di dati Ink in una rete tramite HTTP e per l'input penna permanente in un server.</span><span class="sxs-lookup"><span data-stu-id="db0be-105">The sample also demonstrates one technique for sending ink data across a network by using HTTP and for persisting ink on a server.</span></span>

> [!Note]  
> <span data-ttu-id="db0be-106">Per eseguire questo esempio, è necessario disporre di Microsoft Internet Information Services (IIS) con ASP.NET installato.</span><span class="sxs-lookup"><span data-stu-id="db0be-106">You must have Microsoft Internet Information Services (IIS) with ASP.NET installed to run this sample.</span></span> <span data-ttu-id="db0be-107">Verificare che il computer soddisfi i requisiti necessari per l'esecuzione delle applicazioni ASP.NET nel computer.</span><span class="sxs-lookup"><span data-stu-id="db0be-107">Make sure that your computer meets the requirements necessary for ASP.NET applications to run on your computer.</span></span>

 

> [!Note]  
> <span data-ttu-id="db0be-108">Se si esegue questo esempio in un computer non Tablet PC con Microsoft Windows XP Tablet PC Edition Development Kit 1,7 installato, la funzionalità di riconoscimento del testo per il titolo dell'input penna non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="db0be-108">If you run this sample on a non-Tablet PC computer with the Microsoft Windows XP Tablet PC Edition Development Kit 1.7 installed the text recognition feature for the ink title will not function.</span></span> <span data-ttu-id="db0be-109">Questo problema si verifica perché in un computer non Tablet PC in cui è installato Tablet PC SDK 1,7 mancano i riconoscitori.</span><span class="sxs-lookup"><span data-stu-id="db0be-109">This occurs because a non-Tablet PC computer with the Tablet PC SDK 1.7 installed lacks recognizers.</span></span> <span data-ttu-id="db0be-110">Il resto dell'applicazione viene eseguito come descritto.</span><span class="sxs-lookup"><span data-stu-id="db0be-110">The rest of the application performs as described.</span></span>

 

## <a name="overview"></a><span data-ttu-id="db0be-111">Panoramica</span><span class="sxs-lookup"><span data-stu-id="db0be-111">Overview</span></span>

<span data-ttu-id="db0be-112">L'esempio di Blog Ink crea un weblog abilitato per l'input penna.</span><span class="sxs-lookup"><span data-stu-id="db0be-112">The Ink Blog sample creates an ink-enabled Weblog.</span></span> <span data-ttu-id="db0be-113">InkBlogWeb è un'applicazione ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="db0be-113">InkBlogWeb is an ASP.NET application.</span></span> <span data-ttu-id="db0be-114">La voce input penna viene eseguita tramite un controllo utente a cui viene fatto riferimento da una pagina ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="db0be-114">Ink entry is accomplished by means of a user control that is referenced from an ASP.NET page.</span></span>

<span data-ttu-id="db0be-115">Il controllo utente rileva se i componenti della piattaforma Tablet PC sono installati nel computer client.</span><span class="sxs-lookup"><span data-stu-id="db0be-115">The user control detects whether the Tablet PC platform components are installed on the client computer.</span></span> <span data-ttu-id="db0be-116">In tal caso, il controllo utente Visualizza l'utente con due aree abilitate per l'input penna nella pagina Web: una per Inking un titolo per la voce di Blog e una per il corpo della voce.</span><span class="sxs-lookup"><span data-stu-id="db0be-116">If so, the user control presents the user with two ink-enabled areas on the Web page: one for inking a title for the blog entry and one for the body of the entry.</span></span> <span data-ttu-id="db0be-117">Se i componenti della piattaforma Tablet PC non sono installati, all'utente viene assegnato un controllo casella di testo standard per il titolo e il corpo della voce.</span><span class="sxs-lookup"><span data-stu-id="db0be-117">If the Tablet PC Platform components are not installed, then the user is given a standard text box control for the title and body of the entry.</span></span>

<span data-ttu-id="db0be-118">Quando l'utente completa la creazione della voce, fa clic su un pulsante, Aggiungi il Blog e il post viene inviato al server Web per l'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="db0be-118">When the user finishes creating the entry, she clicks a button, Add Blog, and the post is sent to the Web server for storage.</span></span> <span data-ttu-id="db0be-119">Nel server, l'applicazione salva il testo del titolo e la data di pubblicazione, nonché un riferimento a un file di Graphics Interchange Format (GIF).</span><span class="sxs-lookup"><span data-stu-id="db0be-119">On the server, the application saves the title text and posting date, as well as a reference to a Graphics Interchange Format (GIF) file.</span></span> <span data-ttu-id="db0be-120">Il file GIF, anch ' esso salvato nel server, contiene i dati di input penna del corpo in un file GIF fortificato.</span><span class="sxs-lookup"><span data-stu-id="db0be-120">The GIF file, also saved to the server, contains the ink data from the body in a fortified GIF file.</span></span> <span data-ttu-id="db0be-121">Per altre informazioni sul formato GIF fortificato, vedere [archiviazione dell'input penna in HTML](storing-ink-in-html.md).</span><span class="sxs-lookup"><span data-stu-id="db0be-121">For more information about the fortified GIF format, see [Storing Ink in HTML](storing-ink-in-html.md).</span></span>

<span data-ttu-id="db0be-122">Nella soluzione InkBlog sono presenti due progetti: il progetto **InkBlogControls** e il progetto **InkBlogWeb** .</span><span class="sxs-lookup"><span data-stu-id="db0be-122">There are two projects in the InkBlog solution: the **InkBlogControls** project and the **InkBlogWeb** project.</span></span>

## <a name="inkblogcontrols-project"></a><span data-ttu-id="db0be-123">Progetto InkBlogControls</span><span class="sxs-lookup"><span data-stu-id="db0be-123">InkBlogControls Project</span></span>

<span data-ttu-id="db0be-124">Il progetto **InkBlogControls** è un progetto [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) che contiene il codice per il controllo utente che Abilita Inking nella pagina Web.</span><span class="sxs-lookup"><span data-stu-id="db0be-124">The **InkBlogControls** project is a [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) project that contains the code for the user control that enables inking on the Web page.</span></span> <span data-ttu-id="db0be-125">Il codice per questo controllo, il controllo inkarea, si trova nel file inkarea. cs.</span><span class="sxs-lookup"><span data-stu-id="db0be-125">The code for this control, the InkArea control, is in the InkArea.cs file.</span></span>

<span data-ttu-id="db0be-126">La `InkArea` classe eredita dalla classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="db0be-126">The `InkArea` Class inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class.</span></span> <span data-ttu-id="db0be-127">Il costruttore per il `InkArea` controllo chiama un metodo helper, `CreateInkCollectionSurface` .</span><span class="sxs-lookup"><span data-stu-id="db0be-127">The constructor for the `InkArea` control calls a helper method, `CreateInkCollectionSurface`.</span></span>


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



<span data-ttu-id="db0be-128">Il `CreateInkCollectionSurface` metodo determina se i componenti di Tablet PC sono disponibili sul client tentando di creare un'istanza della classe [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="db0be-128">The `CreateInkCollectionSurface` method determines whether the Tablet PC inking components are available on the client by attempting to create an instance of the [InkCollector](/previous-versions/ms583683(v=vs.100)) class.</span></span> <span data-ttu-id="db0be-129">Se la chiamata al `CreateInkCollectionSurface` metodo ha esito positivo, il metodo restituisce un oggetto [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) come controllo.</span><span class="sxs-lookup"><span data-stu-id="db0be-129">If the call to the `CreateInkCollectionSurface` method succeeds, the method returns a [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) object as the control.</span></span>


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



<span data-ttu-id="db0be-130">Se il costruttore non riesce perché i file della piattaforma Inking non vengono trovati, `InputArea` viene creata un'istanza del controllo come controllo [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) anziché come controllo [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="db0be-130">If the constructor fails because the inking platform files are not found, then the `InputArea` control is instantiated as a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control rather than a [InkCollector](/previous-versions/ms583683(v=vs.100)) control.</span></span> <span data-ttu-id="db0be-131">Il costruttore Ridimensiona quindi il controllo alla dimensione del controllo utente padre e lo aggiunge alla raccolta di controlli padre.</span><span class="sxs-lookup"><span data-stu-id="db0be-131">The constructor then sizes the control to the size of the parent user control and adds it to the parent's Controls collection.</span></span>

<span data-ttu-id="db0be-132">La classe del controllo inkarea implementa tre proprietà pubbliche interessanti: InkData, TextData e webenabled.</span><span class="sxs-lookup"><span data-stu-id="db0be-132">The InkArea control class implements three interesting public properties: InkData, TextData, and WebEnabled.</span></span>

<span data-ttu-id="db0be-133">La proprietà InkData è di sola lettura e fornisce l'accesso ai dati di input penna serializzati, se il client supporta Inking.</span><span class="sxs-lookup"><span data-stu-id="db0be-133">The InkData property is read-only and provides access to the serialized ink data, if the client supports inking.</span></span> <span data-ttu-id="db0be-134">Se il client non supporta Inking, la proprietà InkData ottiene una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="db0be-134">If the client does not support inking, the InkData property gets an empty string.</span></span> <span data-ttu-id="db0be-135">La proprietà InkData chiama un metodo helper, SerializeInkData, per determinare se il client supporta Inking.</span><span class="sxs-lookup"><span data-stu-id="db0be-135">The InkData property calls a helper method, SerializeInkData, to determine if the client supports inking.</span></span>


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



<span data-ttu-id="db0be-136">Nel `SerializeInkData` metodo, il cast a [InkCollector](/previous-versions/ms583683(v=vs.100)) è necessario quando si ottiene l'oggetto [Ink](/previous-versions/ms583670(v=vs.100)) , perché `inputArea` è dichiarato come [controllo](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="db0be-136">In the `SerializeInkData` method, the cast to [InkCollector](/previous-versions/ms583683(v=vs.100)) is necessary when obtaining the [Ink](/previous-versions/ms583670(v=vs.100)) object, because `inputArea` is declared as a [Control](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="db0be-137">Se l'oggetto Ink contiene tratti, i dati di input penna vengono salvati nella `inkDataBytes` matrice di byte come un gif (specificato tramite il valore di enumerazione [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) ).</span><span class="sxs-lookup"><span data-stu-id="db0be-137">If the Ink object contains any strokes, the ink data is saved into the `inkDataBytes` byte array as a GIF (specified by using the [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) enumeration value).</span></span> <span data-ttu-id="db0be-138">Il metodo converte quindi la matrice di byte in una stringa con codifica Base64 e restituisce questa stringa.</span><span class="sxs-lookup"><span data-stu-id="db0be-138">The method then converts the byte array to a Base64-encoded string and returns this string.</span></span>

<span data-ttu-id="db0be-139">Supponendo che il client sia in grado di eseguire il riconoscimento, la `TextData` proprietà restituisce l'oggetto [RecognitionResult](/previous-versions/ms552537(v=vs.100)) dal passaggio dei dati Ink a un riconoscimento della grafia.</span><span class="sxs-lookup"><span data-stu-id="db0be-139">Assuming that the client can perform recognition, the `TextData` property returns the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object from passing the ink data to a handwriting recognizer.</span></span> <span data-ttu-id="db0be-140">Se il client non è compatibile con l'input penna, viene restituito il contenuto della casella di testo, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="db0be-140">If the client is not ink-aware, the text box contents are returned, as shown in the following code.</span></span>


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



<span data-ttu-id="db0be-141">La `TextData` proprietà chiama un metodo helper, `RecognizeInkData` , illustrato nel codice seguente, per eseguire il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="db0be-141">The `TextData` property calls a helper method, `RecognizeInkData`, shown in the following code, to carry out the recognition.</span></span> <span data-ttu-id="db0be-142">Quando i motori di riconoscimento sono presenti nel sistema, il `RecognizeInkData` metodo restituisce una stringa che contiene la proprietà di [stringa](/previous-versions/ms572009(v=vs.100)) dell'oggetto [RecognitionResult](/previous-versions/ms552537(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="db0be-142">When recognition engines are present on the system, the `RecognizeInkData` method returns a string containing the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object's [TopString](/previous-versions/ms572009(v=vs.100)) property.</span></span> <span data-ttu-id="db0be-143">Altrimenti restituisce una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="db0be-143">Otherwise, it returns an empty string.</span></span>


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



<span data-ttu-id="db0be-144">La `InkEnabled` proprietà è un valore booleano di sola lettura che indica se Inking è supportato nel computer client.</span><span class="sxs-lookup"><span data-stu-id="db0be-144">The `InkEnabled` property is a read-only Boolean value that indicates whether inking is supported on the client machine.</span></span>

<span data-ttu-id="db0be-145">Un altro importante membro pubblico della `InkArea` classe Control è il `DisposeResources` metodo.</span><span class="sxs-lookup"><span data-stu-id="db0be-145">Another important public member of the `InkArea` control class is the `DisposeResources` method.</span></span> <span data-ttu-id="db0be-146">Questo metodo chiama internamente il `Dispose` metodo per garantire la pulizia di tutte le risorse utilizzate dal controllo utente.</span><span class="sxs-lookup"><span data-stu-id="db0be-146">This method internally calls the `Dispose` method to ensure that all resources leveraged by the user control are cleaned up.</span></span> <span data-ttu-id="db0be-147">Qualsiasi applicazione che utilizza il `InkArea` controllo deve chiamare il `DisposeResources` metodo al termine dell'utilizzo del controllo.</span><span class="sxs-lookup"><span data-stu-id="db0be-147">Any application that uses the `InkArea` control must call the `DisposeResources` method when it is finished using the control.</span></span>

## <a name="inkblogweb-project"></a><span data-ttu-id="db0be-148">Progetto InkBlogWeb</span><span class="sxs-lookup"><span data-stu-id="db0be-148">InkBlogWeb Project</span></span>

<span data-ttu-id="db0be-149">Il progetto InkBlogWeb è un progetto di distribuzione del programma di installazione Web che fa riferimento al `InkArea` controllo per fornire la funzionalità di Blog.</span><span class="sxs-lookup"><span data-stu-id="db0be-149">The InkBlogWeb project is a Web Setup deployment project that references the `InkArea` control to provide the blogging functionality.</span></span> <span data-ttu-id="db0be-150">Per ulteriori informazioni sui progetti di distribuzione del programma di installazione Web, vedere [distribuzione di un progetto di installazione Web](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="db0be-150">For more information about Web Setup deployment projects, see [Deployment of a Web Setup Project](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span></span>

<span data-ttu-id="db0be-151">Sono disponibili due file aspx che implementano l'esempio blogging: default. aspx e AddBlog. aspx.</span><span class="sxs-lookup"><span data-stu-id="db0be-151">There are two .aspx files that implement the blogging sample: Default.aspx and AddBlog.aspx.</span></span> <span data-ttu-id="db0be-152">Default. aspx è la pagina predefinita per l'applicazione InkBlogWeb.</span><span class="sxs-lookup"><span data-stu-id="db0be-152">Default.aspx is the default page for the InkBlogWeb application.</span></span> <span data-ttu-id="db0be-153">Il file code-behind per questa pagina è default. aspx. cs.</span><span class="sxs-lookup"><span data-stu-id="db0be-153">The code behind file for this page is Default.aspx.cs.</span></span> <span data-ttu-id="db0be-154">Questa pagina contiene un collegamento alla pagina che contiene il nuovo modulo di inserimento nel Blog e visualizza eventuali voci di Blog esistenti.</span><span class="sxs-lookup"><span data-stu-id="db0be-154">This page provides a link to the page containing the new blog entry form and displays any existing blog entries.</span></span> <span data-ttu-id="db0be-155">Questo processo viene descritto in seguito, dopo l'esame della pagina del nuovo modulo del post del Blog, AddBlog. aspx.</span><span class="sxs-lookup"><span data-stu-id="db0be-155">This process is described later, after the following examination of the new blog entry form page, AddBlog.aspx.</span></span>

<span data-ttu-id="db0be-156">AddBlog. aspx e il relativo file code-behind, AddBlog. aspx. cs, contengono la logica e il codice dell'interfaccia utente per la creazione di nuove voci di Blog.</span><span class="sxs-lookup"><span data-stu-id="db0be-156">AddBlog.aspx and its code-behind file, AddBlog.aspx.cs, contain the logic and user interface code for creating new blog entries.</span></span> <span data-ttu-id="db0be-157">AddBlox. aspx fa riferimento a due istanze della classe del controllo inkarea creata nel progetto InkBlogControls usando l'elemento oggetto HTML, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="db0be-157">AddBlox.aspx references two instances of the InkArea control class created in the InkBlogControls project by using the HTML OBJECT element as shown in the following example.</span></span> <span data-ttu-id="db0be-158">Un'istanza ha un `id` attributo di inkBlogTitle e l'altra ha un attributo ID di inkBlogBody.</span><span class="sxs-lookup"><span data-stu-id="db0be-158">One instance has an `id` attribute of inkBlogTitle and the other has an id attribute of inkBlogBody.</span></span>

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

<span data-ttu-id="db0be-159">Il InkBlogControls.dll assembly deve essere presente nella stessa directory della pagina aspx a cui fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="db0be-159">The InkBlogControls.dll assembly must be present in the same directory as the .aspx page that is referencing it.</span></span> <span data-ttu-id="db0be-160">Il progetto di distribuzione del programma di installazione Web garantisce che questo sia il caso, come evidenziato dalla presenza dell'elemento "output primario da InkBlogControls" nel progetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="db0be-160">The Web Setup deployment project ensures that this is the case, as evidenced by the presence of the "Primary output from InkBlogControls" item in the Deployment Project.</span></span>

<span data-ttu-id="db0be-161">Il controllo del titolo è di 48 pixel di altezza per facilitare l'immissione di una singola riga di input penna per il titolo.</span><span class="sxs-lookup"><span data-stu-id="db0be-161">The title control is only 48 pixels high to facilitate the entry of a single line of ink for the title.</span></span> <span data-ttu-id="db0be-162">Il controllo del corpo è di 296 pixel di altezza per fare spazio a voci di Blog più grandi di più righe o forse di disegni.</span><span class="sxs-lookup"><span data-stu-id="db0be-162">The body control is 296 pixels high to make room for larger blog entries of multiple lines or perhaps drawings.</span></span>

<span data-ttu-id="db0be-163">I controlli inkarea sono connessi a una funzione script sul lato client, AddBlog, mediante un gestore dell'evento OnClick dell'elemento BUTTON HTML standard.</span><span class="sxs-lookup"><span data-stu-id="db0be-163">The InkArea controls are connected to a client-side script function, AddBlog, by means of a standard HTML BUTTON element's onclick event handler.</span></span>

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

<span data-ttu-id="db0be-164">Nella pagina è presente anche un form HTML che contiene tre elementi di INPUT nascosti: BlogTitleText, BlogBodyText e BlogBodyInkData.</span><span class="sxs-lookup"><span data-stu-id="db0be-164">There is also an HTML form on the page that contains three hidden INPUT elements: BlogTitleText, BlogBodyText, and BlogBodyInkData.</span></span> <span data-ttu-id="db0be-165">Questo modulo viene usato per pubblicare i dati di immissione nel Blog sul server.</span><span class="sxs-lookup"><span data-stu-id="db0be-165">This form is used to post the blog entry data back to the server.</span></span> <span data-ttu-id="db0be-166">AddBlog. aspx è il gestore di postback definito per il form.</span><span class="sxs-lookup"><span data-stu-id="db0be-166">AddBlog.aspx is the post-back handler defined for the form.</span></span>

<span data-ttu-id="db0be-167">La funzione AddBlog, scritta in Microsoft JScript <entity type="reg"/> , estrae i dati del Blog dai controlli Inkarea e invia i risultati al server.</span><span class="sxs-lookup"><span data-stu-id="db0be-167">The AddBlog function-written in Microsoft JScript<entity type="reg"/>-extracts the blog data from the InkArea controls and posts the results to the server.</span></span>


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



<span data-ttu-id="db0be-168">Quando i dati arrivano al server, il codice in AddBlog. aspx. cs controlla il gestore dell' \_ evento di caricamento della pagina per verificare se la proprietà form dell'oggetto HttpRequest contiene dati.</span><span class="sxs-lookup"><span data-stu-id="db0be-168">When the data arrives at the server, the code in AddBlog.aspx.cs checks the Page\_Load event handler to see if the HttpRequest object's Form property contains any data.</span></span> <span data-ttu-id="db0be-169">In tal caso, crea un nome di file basato sull'ora di sistema corrente, inserisce i dati del modulo in tre variabili stringa e scrive i dati in un file HTML e un file GIF contenente i dati di input penna, se presenti, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="db0be-169">If so, it creates a file name based on the current system time, puts the form data into three string variables and writes the data out to an HTML file and a GIF file containing the ink data, if present, as shown in the following code.</span></span>


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



<span data-ttu-id="db0be-170">Per altri dettagli sui metodi helper, vedere il codice sorgente di esempio.</span><span class="sxs-lookup"><span data-stu-id="db0be-170">For more details about the helper methods, refer to the sample source code.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="db0be-171">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="db0be-171">Running the Sample</span></span>

<span data-ttu-id="db0be-172">Per impostazione predefinita, Tablet PC SDK 1,7 installa l'esempio di Web Ink Blog.</span><span class="sxs-lookup"><span data-stu-id="db0be-172">The Tablet PC SDK 1.7 installs the Ink Blog Web sample by default.</span></span> <span data-ttu-id="db0be-173">Per eseguire l'esempio, in Internet Explorer passare a https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx .</span><span class="sxs-lookup"><span data-stu-id="db0be-173">To run the sample, in Internet Explorer, navigate to https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx.</span></span> <span data-ttu-id="db0be-174">Se si esegue Windows Server 2003, sostituire "localhost" con il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="db0be-174">If you are running Windows Server 2003, substitute your computer name for "localhost".</span></span>

> [!Note]  
> <span data-ttu-id="db0be-175">Gli esempi Web compilati non vengono installati tramite l'opzione di installazione predefinita per l'SDK.</span><span class="sxs-lookup"><span data-stu-id="db0be-175">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="db0be-176">È necessario completare un'installazione personalizzata e selezionare l'opzione secondaria "esempi Web precompilati" per installarli.</span><span class="sxs-lookup"><span data-stu-id="db0be-176">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="db0be-177">È anche possibile eseguire l'esempio aprendo e compilando il progetto in Microsoft Visual Studio <entity type="reg"/> .NET e quindi distribuendo il progetto in un computer separato che esegue IIS.</span><span class="sxs-lookup"><span data-stu-id="db0be-177">You can also run the sample by opening and building the project in Microsoft Visual Studio<entity type="reg"/> .NET and then deploying it to a separate computer running IIS.</span></span>

## <a name="troubleshooting-the-sample"></a><span data-ttu-id="db0be-178">Risoluzione dei problemi relativi all'esempio</span><span class="sxs-lookup"><span data-stu-id="db0be-178">Troubleshooting the Sample</span></span>

<span data-ttu-id="db0be-179">Tre aree che possono causare difficoltà durante l'esecuzione o l'hosting dell'esempio sono le autorizzazioni e il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="db0be-179">Three areas that may cause difficulty when running or hosting the sample are permissions and recognition.</span></span>

### <a name="permissions"></a><span data-ttu-id="db0be-180">Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="db0be-180">Permissions</span></span>

<span data-ttu-id="db0be-181">L'esempio richiede le autorizzazioni di scrittura all'interno della cartella radice virtuale per l'account che sta tentando di creare una nuova voce di Blog.</span><span class="sxs-lookup"><span data-stu-id="db0be-181">The sample requires write permissions within the virtual root folder for the account that is attempting to create a new blog entry.</span></span> <span data-ttu-id="db0be-182">Per impostazione predefinita, la versione compilata dell'esempio disponibile in Tablet PC SDK 1,7 dispone delle autorizzazioni corrette impostate per soddisfare questo requisito.</span><span class="sxs-lookup"><span data-stu-id="db0be-182">By default, the compiled version of the sample provided in the Tablet PC SDK 1.7 has the correct permissions set to meet this requirement.</span></span>

<span data-ttu-id="db0be-183">Se si compila e si distribuisce l'esempio usando il progetto di distribuzione dell'installazione Web fornito, è necessario assegnare al gruppo% MACHINENAME% \\ Users il gruppo di accesso in scrittura alla cartella file System a cui fa riferimento la radice virtuale InkBlogWeb (ad esempio, C: \\ Inetpub \\ wwwroot \\ InkBlogWeb).</span><span class="sxs-lookup"><span data-stu-id="db0be-183">If you build and deploy the sample by using the provided Web Setup deployment project, you must give the %MACHINENAME%\\Users group write-access to the file system folder pointed to by the InkBlogWeb virtual root (for example, C:\\InetPub\\WWWRoot\\InkBlogWeb).</span></span> <span data-ttu-id="db0be-184">Il gruppo Users include l'account anonimo usato da IIS, consentendo così all'applicazione ASP.NET di scrivere le nuove voci di Blog nel file system.</span><span class="sxs-lookup"><span data-stu-id="db0be-184">The Users group includes the Anonymous account used by IIS, thus allowing the ASP.NET application to write the new blog entries to the file system.</span></span> <span data-ttu-id="db0be-185">In alternativa, è possibile rimuovere l'accesso anonimo alla radice virtuale e forzare l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="db0be-185">An alternative is to remove anonymous access to the virtual root and force authentication.</span></span>

### <a name="recognition"></a><span data-ttu-id="db0be-186">Riconoscimento</span><span class="sxs-lookup"><span data-stu-id="db0be-186">Recognition</span></span>

<span data-ttu-id="db0be-187">Per riconoscere l'input penna nel titolo del Blog, è necessario installare i riconoscitori della grafia.</span><span class="sxs-lookup"><span data-stu-id="db0be-187">The handwriting recognizers must be installed in order to recognize the ink in the title of the blog.</span></span> <span data-ttu-id="db0be-188">Se si accede all'applicazione InkBlog da un computer con un sistema operativo diverso da Windows XP Tablet PC Edition ma con Tablet PC SDK 1,7 installato, è possibile scrivere in input penna nei controlli inkarea, ma i motori di riconoscimento non saranno presenti e non verrà visualizzato alcun titolo per le voci di Blog.</span><span class="sxs-lookup"><span data-stu-id="db0be-188">If you access the InkBlog application from a computer with an operating system other than Windows XP Tablet PC Edition but with the Tablet PC SDK 1.7 installed, you can write in ink in the InkArea controls, but the recognition engines will not be present and no titles will appear for your blog entries.</span></span> <span data-ttu-id="db0be-189">Tuttavia, il contenuto dell'input penna nel corpo viene comunque visualizzato.</span><span class="sxs-lookup"><span data-stu-id="db0be-189">The ink content in the body still appears, though.</span></span>

### <a name="machine-configuration"></a><span data-ttu-id="db0be-190">Configurazione computer</span><span class="sxs-lookup"><span data-stu-id="db0be-190">Machine Configuration</span></span>

<span data-ttu-id="db0be-191">Se è stato installato ASP.NET e il .NET Framework in un computer e si disinstalla e si reinstalla IIS, le mappe di script si interrompono e ASP.NET non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="db0be-191">If you have installed ASP.NET and the .NET Framework on a computer and you then uninstall and reinstall IIS, the script maps will break and ASP.NET will not work.</span></span> <span data-ttu-id="db0be-192">In tal caso, è possibile ripristinare le mappe di script ASP.NET con lo strumento di registrazione IIS ASP.NET (ASPNET \_regiis.exe-i).</span><span class="sxs-lookup"><span data-stu-id="db0be-192">If this happens, you can repair the ASP.NET script maps with the ASP.NET IIS Registration tool (Aspnet\_regiis.exe -i).</span></span>

## <a name="related-topics"></a><span data-ttu-id="db0be-193">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db0be-193">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="db0be-194">[InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="db0be-194">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="db0be-195">Input penna sul Web</span><span class="sxs-lookup"><span data-stu-id="db0be-195">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> <dt>

[<span data-ttu-id="db0be-196">Formati di dati Ink</span><span class="sxs-lookup"><span data-stu-id="db0be-196">Ink Data Formats</span></span>](ink-data-formats.md)
</dt> <dt>

[<span data-ttu-id="db0be-197">Classe System. Windows. Forms. UserControl</span><span class="sxs-lookup"><span data-stu-id="db0be-197">System.Windows.Forms.UserControl Class</span></span>](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
