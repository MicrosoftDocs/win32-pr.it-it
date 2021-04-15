---
title: Creazione di un'applicazione Ribbon
description: Il Framework della barra multifunzione di Windows è costituito da due piattaforme di sviluppo distinte, ma dipendenti, un linguaggio di markup basato su Extensible Application Markup Language (XAML) per dichiarare controlli e il relativo layout visivo e un set di interfacce basato su C++ Component Object Model (COM) per definire la funzionalità del comando e gli hook dell'applicazione. Questa divisione del lavoro all'interno dell'architettura del Framework della barra multifunzione richiede che uno sviluppatore che desidera sfruttare le funzionalità dell'interfaccia utente avanzate offerte dal Framework debba progettare e descrivere l'interfaccia utente nel markup, quindi utilizzare le interfacce COM del Framework della barra multifunzione per connettere il Framework all'applicazione host.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Barra multifunzione di Windows, creazione di applicazioni
- Barra multifunzione, creazione di applicazioni
- Barra multifunzione di Windows, roadmap
- Barra multifunzione, roadmap
- Barra multifunzione di Windows, markup
- Barra multifunzione, markup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399448"
---
# <a name="creating-a-ribbon-application"></a><span data-ttu-id="2a74a-110">Creazione di un'applicazione Ribbon</span><span class="sxs-lookup"><span data-stu-id="2a74a-110">Creating a Ribbon Application</span></span>

<span data-ttu-id="2a74a-111">Il Framework della barra multifunzione di Windows è costituito da due piattaforme di sviluppo distinte e dipendenti, ovvero un linguaggio di markup basato su Extensible Application Markup Language (XAML) per dichiarare controlli e il relativo layout visivo e un set di interfacce basato su C++ Component Object Model (COM) per definire le funzionalità dei comandi e gli hook dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-111">The Windows Ribbon framework is composed of two distinct, yet dependent, development platforms: a markup language based on Extensible Application Markup Language (XAML) to declare controls and their visual layout, and a C++ Component Object Model (COM)-based set of interfaces to define command functionality and application hooks.</span></span> <span data-ttu-id="2a74a-112">Questa divisione del lavoro all'interno dell'architettura del Framework della barra multifunzione richiede che uno sviluppatore che desidera sfruttare le funzionalità dell'interfaccia utente avanzate offerte dal Framework debba progettare e descrivere l'interfaccia utente nel markup, quindi utilizzare le interfacce COM del Framework della barra multifunzione per connettere il Framework all'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="2a74a-112">This division of labor within the Ribbon framework architecture requires that a developer who wants to take advantage of the rich UI capabilities offered by the framework must design and describe the UI in markup, and then use the Ribbon framework COM interfaces to connect the framework to the host application.</span></span>

-   [<span data-ttu-id="2a74a-113">Roadmap della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="2a74a-113">Ribbon Roadmap</span></span>](#ribbon-roadmap)
-   [<span data-ttu-id="2a74a-114">Scrivere il markup</span><span class="sxs-lookup"><span data-stu-id="2a74a-114">Write the Markup</span></span>](#write-the-markup)
    -   [<span data-ttu-id="2a74a-115">Compilare il markup</span><span class="sxs-lookup"><span data-stu-id="2a74a-115">Compile the Markup</span></span>](#compile-the-markup)
-   [<span data-ttu-id="2a74a-116">Compilare l'applicazione</span><span class="sxs-lookup"><span data-stu-id="2a74a-116">Build the Application</span></span>](#build-the-application)
    -   [<span data-ttu-id="2a74a-117">Inizializza la barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="2a74a-117">Initialize the Ribbon</span></span>](#initialize-the-ribbon)
    -   [<span data-ttu-id="2a74a-118">Collegare il markup all'applicazione</span><span class="sxs-lookup"><span data-stu-id="2a74a-118">Link the Markup to the Application</span></span>](#link-the-markup-to-the-application)
    -   [<span data-ttu-id="2a74a-119">Compilare l'applicazione</span><span class="sxs-lookup"><span data-stu-id="2a74a-119">Compile the Application</span></span>](#link-the-markup-to-the-application)
-   [<span data-ttu-id="2a74a-120">Aggiornamenti ed esecuzioni in fase di esecuzione</span><span class="sxs-lookup"><span data-stu-id="2a74a-120">Run Time Updates and Executions</span></span>](#run-time-updates-and-executions)
-   [<span data-ttu-id="2a74a-121">Supporto OLE</span><span class="sxs-lookup"><span data-stu-id="2a74a-121">OLE Support</span></span>](#ole-support)
-   [<span data-ttu-id="2a74a-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a74a-122">Related topics</span></span>](#related-topics)

## <a name="ribbon-roadmap"></a><span data-ttu-id="2a74a-123">Roadmap della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="2a74a-123">Ribbon Roadmap</span></span>

<span data-ttu-id="2a74a-124">Gli aspetti visivi di un'applicazione Ribbon, ad esempio i controlli visualizzati e la posizione in cui vengono inseriti, vengono dichiarati nel markup (vedere [dichiarazione di comandi e controlli con markup della barra multifunzione](windowsribbon-schema.md)).</span><span class="sxs-lookup"><span data-stu-id="2a74a-124">The visual aspects of a Ribbon application, such as what controls are displayed and where they are placed, are declared in markup (see [Declaring Commands and Controls with Ribbon Markup](windowsribbon-schema.md)).</span></span> <span data-ttu-id="2a74a-125">La logica del comando dell'applicazione, ad esempio cosa accade quando viene premuto un pulsante, viene implementata nel codice.</span><span class="sxs-lookup"><span data-stu-id="2a74a-125">The application command logic, such as what happens when a button is pressed, is implemented in code.</span></span>

<span data-ttu-id="2a74a-126">Il processo di implementazione di una barra multifunzione e di incorporarlo in un'applicazione Windows richiede quattro attività di base: scrivere il markup, compilare il markup, scrivere il codice e compilare e collegare l'intera applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-126">The process of implementing a Ribbon and incorporating it into a Windows application requires four basic tasks: write the markup, compile the markup, write the code, and compile and link the entire application.</span></span>

<span data-ttu-id="2a74a-127">Il diagramma seguente illustra il flusso di lavoro per una tipica implementazione della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-127">The following diagram illustrates the workflow for a typical Ribbon implementation.</span></span>

![diagramma che illustra il flusso di lavoro per una tipica implementazione della barra multifunzione.](images/overviews/ribbonroadmap.png)

<span data-ttu-id="2a74a-129">Le sezioni seguenti descrivono questo processo in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="2a74a-129">The following sections describe this process in more detail.</span></span>

## <a name="write-the-markup"></a><span data-ttu-id="2a74a-130">Scrivere il markup</span><span class="sxs-lookup"><span data-stu-id="2a74a-130">Write the Markup</span></span>

<span data-ttu-id="2a74a-131">Una volta progettata l'interfaccia utente della barra multifunzione, la prima attività per uno sviluppatore di applicazioni consiste nel descrivere l'interfaccia utente con il markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-131">After the Ribbon UI has been designed, the first task for an application developer is to describe the UI with Ribbon markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a74a-132">Il file dello schema di markup del Framework della barra multifunzione, UICC. xsd, viene installato con Microsoft Windows Software Development Kit (SDK) per Windows 7 e .NET Framework 4,0.</span><span class="sxs-lookup"><span data-stu-id="2a74a-132">The Ribbon framework markup schema file, UICC.xsd, is installed with the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0.</span></span> <span data-ttu-id="2a74a-133">Utilizzando il percorso di installazione standard, il file si trova nella cartella% ProgramFiles% \\ Microsoft \\ SDK \\ \[ numero versione Windows \] \\ bin a cui è possibile fare riferimento da molti editor XML per fornire suggerimenti e completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="2a74a-133">Using the standard installation path, the file is located in the %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Bin folder where it can be referenced by many XML editors to provide hinting and auto-completion.</span></span>

 

<span data-ttu-id="2a74a-134">Controlli della barra multifunzione, comandi della barra multifunzione (elementi indipendenti dal controllo che forniscono la funzionalità di base per i controlli della barra multifunzione) e tutti i layout di controllo e le relazioni visive sono dichiarati nel</span><span class="sxs-lookup"><span data-stu-id="2a74a-134">Ribbon controls, Ribbon Commands (the control-independent elements that provide the base functionality for Ribbon controls), and all control layout and visual relationships are declared in markup.</span></span> <span data-ttu-id="2a74a-135">La struttura del markup della barra multifunzione enfatizza la distinzione tra i controlli della barra multifunzione e i comandi attraverso due gerarchie di nodi primari: un albero di [comandi e risorse](windowsribbon-reference-elements-command.md) e una struttura di [visualizzazioni](windowsribbon-reference-elements-view.md) .</span><span class="sxs-lookup"><span data-stu-id="2a74a-135">The structure of the Ribbon markup emphasizes the distinction between Ribbon controls and Commands through two primary node hierarchies: a [Commands and Resources](windowsribbon-reference-elements-command.md) tree and a [Views](windowsribbon-reference-elements-view.md) tree.</span></span>

<span data-ttu-id="2a74a-136">Tutti i contenitori e le azioni esposti dalla barra multifunzione sono dichiarati nell'albero [comandi e risorse](windowsribbon-reference-elements-command.md) .</span><span class="sxs-lookup"><span data-stu-id="2a74a-136">All containers and actions that are exposed by the Ribbon are declared in the [Commands and Resources](windowsribbon-reference-elements-command.md) tree.</span></span> <span data-ttu-id="2a74a-137">Ogni elemento Command è associato a un set di risorse, come richiesto dalla progettazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="2a74a-137">Each Command element is associated with a set of resources, as required by the UI design.</span></span>

<span data-ttu-id="2a74a-138">Dopo aver creato i comandi per un'applicazione, è necessario dichiarare i controlli nell'albero delle [visualizzazioni](windowsribbon-reference-elements-view.md) e associare ogni controllo a un comando per esporre la funzionalità del comando.</span><span class="sxs-lookup"><span data-stu-id="2a74a-138">After you create the Commands for an application, you declare controls in the [Views](windowsribbon-reference-elements-view.md) tree and bind each control to a Command to expose the Command functionality.</span></span> <span data-ttu-id="2a74a-139">Il Framework della barra multifunzione determina il posizionamento effettivo dei controlli in base alla gerarchia dei controlli dichiarata qui.</span><span class="sxs-lookup"><span data-stu-id="2a74a-139">The Ribbon framework determines the actual positioning of the controls based on the Control hierarchy declared here.</span></span>

<span data-ttu-id="2a74a-140">Nell'esempio di codice riportato di seguito viene illustrato come dichiarare un controllo Button, con etichetta Exit Application e come associarlo a un comando Exit.</span><span class="sxs-lookup"><span data-stu-id="2a74a-140">The following code example illustrates how to declare a Button control, labeled Exit application, and associate it with an Exit Command.</span></span>


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> <span data-ttu-id="2a74a-141">Sebbene sia possibile utilizzare qualsiasi estensione di file per il file di markup della barra multifunzione, XML è l'estensione consigliata utilizzata nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-141">While it is possible to use any file name extension for the Ribbon markup file, .xml is the recommended extension that is used throughout the documentation.</span></span>

 

### <a name="compile-the-markup"></a><span data-ttu-id="2a74a-142">Compilare il markup</span><span class="sxs-lookup"><span data-stu-id="2a74a-142">Compile the Markup</span></span>

<span data-ttu-id="2a74a-143">Dopo aver creato il file di markup della barra multifunzione, è necessario compilarlo in un formato binario tramite il compilatore di markup della barra multifunzione, il compilatore di comandi dell'interfaccia utente (UICC), incluso in Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="2a74a-143">After the Ribbon markup file is created, it must be compiled into a binary format by the Ribbon markup compiler, UI Command Compiler (UICC), that is included with the Windows software development kit (SDK).</span></span> <span data-ttu-id="2a74a-144">Un riferimento a questo file binario viene passato al metodo [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) durante l'inizializzazione del Framework della barra multifunzione dall'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="2a74a-144">A reference to this binary file is passed to the [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) method during initialization of the Ribbon framework by the host application.</span></span>

<span data-ttu-id="2a74a-145">UICC può essere eseguito direttamente da una finestra della riga di comando o aggiunto come "passaggio di compilazione personalizzato" in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2a74a-145">UICC can be executed directly from a command-line window or added as a "Custom Build Step" in Visual Studio.</span></span>

<span data-ttu-id="2a74a-146">La figura seguente mostra il compilatore di markup UICC nella finestra della shell CMD di Windows 7 SDK.</span><span class="sxs-lookup"><span data-stu-id="2a74a-146">The following image shows the UICC markup compiler in the Windows 7 SDK CMD Shell window.</span></span>

![screenshot che mostra uicc.exe in una finestra della riga di comando.](images/overviews/screenshot-intentcl-commandline.png)

<span data-ttu-id="2a74a-148">La figura seguente mostra UICC aggiunto come un'istruzione di compilazione personalizzata in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2a74a-148">The following image shows UICC added as a Custom Build Step in Visual Studio.</span></span>

![screenshot che mostra uicc.exe aggiunto come istruzione di compilazione personalizzata in Visual Studio.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

<span data-ttu-id="2a74a-150">UICC genera tre file: una versione binaria del markup (. BML), un'intestazione di definizione ID (file h) per esporre gli elementi di markup all'applicazione host della barra multifunzione e uno [script di definizione delle risorse](../menurc/about-resource-files.md) (file RC) per collegare le risorse di tipo stringa e immagine della barra multifunzione all'applicazione host in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-150">The UICC generates three files: a binary version of the markup (.bml), an ID definition header (.h file) to expose markup elements to the Ribbon host application, and a [resource-definition script](../menurc/about-resource-files.md) (.rc file) to link Ribbon image and string resources to the host application at compile time.</span></span>

<span data-ttu-id="2a74a-151">Per informazioni più dettagliate sulla compilazione del markup del Framework della barra multifunzione, vedere [compilazione del markup della barra](windowsribbon-intentcl.md)multifunzione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-151">For more detail on compiling Ribbon framework markup, see [Compiling Ribbon Markup](windowsribbon-intentcl.md).</span></span>

## <a name="build-the-application"></a><span data-ttu-id="2a74a-152">Compilare l'applicazione</span><span class="sxs-lookup"><span data-stu-id="2a74a-152">Build the Application</span></span>

<span data-ttu-id="2a74a-153">Una volta che l'interfaccia utente preliminare per un'applicazione Ribbon è stata progettata e implementata nel markup, è necessario scrivere il codice dell'applicazione che inizializza il Framework, usa il markup e associa i comandi dichiarati nel markup ai gestori di comandi appropriati nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-153">Once the preliminary UI for a Ribbon application has been designed and implemented in markup, application code must be written that initializes the framework, consumes the markup, and binds the Commands declared in the markup to the appropriate Command handlers in the application.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="2a74a-154">Poiché il Framework della barra multifunzione è basato su COM, è consigliabile che i progetti Ribbon usino l' \_ \_ operatore uuidof () per fare riferimento ai GUID per le interfacce del Framework della barra multifunzione (IID).</span><span class="sxs-lookup"><span data-stu-id="2a74a-154">Since the Ribbon framework is COM-based, it is recommended that Ribbon projects use the \_\_uuidof() operator to reference the GUIDs for Ribbon framework interfaces (IIDs).</span></span> <span data-ttu-id="2a74a-155">Nei casi in cui non è possibile usare l' \_ \_ operatore uuidof (), ad esempio quando viene usato un compilatore non Microsoft o l'applicazione host è basata su C, il IID deve essere definito dall'applicazione perché non è contenuto in UUID. lib.</span><span class="sxs-lookup"><span data-stu-id="2a74a-155">In those cases where it is not possible to use the \_\_uuidof() operator, such as when a non-Microsoft compiler is used or the host application is C-based, the IIDs must be defined by the application since they are not contained in uuid.lib.</span></span>
>
> <span data-ttu-id="2a74a-156">Se i IID sono definiti dall'applicazione, è necessario usare i GUID specificati in UIRibbon. idl.</span><span class="sxs-lookup"><span data-stu-id="2a74a-156">If the IIDs are defined by the application then the GUIDs specified in UIRibbon.idl must be used.</span></span>
>
> <span data-ttu-id="2a74a-157">UIRibbon. idl viene fornito come parte di [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) e si trova nel percorso di installazione standard di% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ include.</span><span class="sxs-lookup"><span data-stu-id="2a74a-157">UIRibbon.idl ships as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and can be found at the standard installation path of %ProgramFiles%\\Microsoft SDKs\\Windows\\v7.0\\Include.</span></span>

 

### <a name="initialize-the-ribbon"></a><span data-ttu-id="2a74a-158">Inizializza la barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="2a74a-158">Initialize the Ribbon</span></span>

<span data-ttu-id="2a74a-159">Il diagramma seguente illustra i passaggi necessari per implementare una semplice applicazione della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-159">The following diagram illustrates the steps required to implement a simple Ribbon application.</span></span>

![diagramma che illustra i passaggi necessari per implementare una semplice implementazione della barra multifunzione.](images/overviews/initializationsteps.png)

<span data-ttu-id="2a74a-161">I passaggi seguenti descrivono in dettaglio come implementare una semplice applicazione della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-161">The following steps describe in detail how to implement a simple Ribbon application.</span></span>

1.  <span data-ttu-id="2a74a-162">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="2a74a-162">CoCreateInstance</span></span>

    <span data-ttu-id="2a74a-163">L'applicazione chiama la funzione standard COM CoCreateInstance con l'ID classe del Framework della barra multifunzione per ottenere un puntatore al Framework.</span><span class="sxs-lookup"><span data-stu-id="2a74a-163">The application calls the standard COM CoCreateInstance function with the Ribbon framework class ID to obtain a pointer to the framework.</span></span>

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  <span data-ttu-id="2a74a-164">Initialize (HWND, IUIApplication \* )</span><span class="sxs-lookup"><span data-stu-id="2a74a-164">Initialize(hwnd, IUIApplication\*)</span></span>

    <span data-ttu-id="2a74a-165">L'applicazione chiama [**IUIFramework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), passando due parametri: l'handle per la finestra di primo livello che conterrà la barra multifunzione e un puntatore all'implementazione di [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) che consente al Framework di eseguire i callback all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-165">The application calls [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), passing in two parameters: the handle to the top-level window that will contain the Ribbon and a pointer to the [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) implementation that allows the framework to make callbacks to the application.</span></span>

    > <span data-ttu-id="2a74a-166">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="2a74a-166">\[!Important\]</span></span>  
    > <span data-ttu-id="2a74a-167">Il Framework della barra multifunzione viene inizializzato come un Apartment a thread singolo (STA).</span><span class="sxs-lookup"><span data-stu-id="2a74a-167">The Ribbon framework is initialized as a single-threaded apartment (STA).</span></span>

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  <span data-ttu-id="2a74a-168">LoadUI (istanza, resourceName)</span><span class="sxs-lookup"><span data-stu-id="2a74a-168">LoadUI(instance, resourceName)</span></span>

    <span data-ttu-id="2a74a-169">L'applicazione chiama [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) per associare la risorsa di markup.</span><span class="sxs-lookup"><span data-stu-id="2a74a-169">The application calls [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to bind the markup resource.</span></span> <span data-ttu-id="2a74a-170">Il primo parametro di questa funzione è un handle per l'istanza dell'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="2a74a-170">The first parameter of this function is a handle to the Ribbon application instance.</span></span> <span data-ttu-id="2a74a-171">Il secondo parametro è il nome della risorsa di markup binario che è stata compilata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="2a74a-171">The second parameter is the name of the binary markup resource that was compiled previously.</span></span> <span data-ttu-id="2a74a-172">Passando il markup binario al framework della barra multifunzione, l'applicazione segnala la struttura della barra multifunzione e il modo in cui devono essere disposti i controlli.</span><span class="sxs-lookup"><span data-stu-id="2a74a-172">By passing the binary markup to the Ribbon framework, the application signals what the Ribbon structure should be and how controls should be arranged.</span></span> <span data-ttu-id="2a74a-173">Fornisce inoltre al Framework un manifesto di comandi da esporre, ad esempio incolla, taglia, trova, che vengono utilizzati dal framework quando vengono eseguiti callback correlati al comando in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-173">It also provides the framework with a manifest of commands to expose (such as Paste, Cut, Find), which are used by the framework when it makes Command-related callbacks at run time.</span></span>

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  <span data-ttu-id="2a74a-174">Callback [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)</span><span class="sxs-lookup"><span data-stu-id="2a74a-174">[**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) callbacks</span></span>

    <span data-ttu-id="2a74a-175">Una volta completati i passaggi da 1 a 3, il Framework della barra multifunzione sa quali comandi esporre nella barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-175">After steps 1 through 3 are completed, the Ribbon framework knows which Commands to expose in the Ribbon.</span></span> <span data-ttu-id="2a74a-176">Tuttavia, il Framework necessita ancora di due elementi prima che la barra multifunzione sia completamente funzionante: un modo per indicare all'applicazione quando vengono eseguiti i comandi e un modo per ottenere le risorse o le proprietà del comando in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-176">However, the framework still needs two things before the Ribbon is fully functional: a way to tell the application when Commands are executed and a way to get Command resources, or properties, at run time.</span></span> <span data-ttu-id="2a74a-177">Se, ad esempio, una casella combinata viene visualizzata nell'interfaccia utente, il Framework deve richiedere gli elementi con cui popolare la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="2a74a-177">For example, if a combo box is to appear in the UI, then the framework needs to ask for the items with which to populate the combo box.</span></span>

    <span data-ttu-id="2a74a-178">Queste due parti di funzionalità vengono gestite tramite l'interfaccia [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .</span><span class="sxs-lookup"><span data-stu-id="2a74a-178">These two pieces of functionality are handled through the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span> <span data-ttu-id="2a74a-179">In particolare, per ogni comando dichiarato nel markup binario (vedere il passaggio 3 precedente), il Framework chiama [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) per chiedere all'applicazione un oggetto **IUICommandHandler** per tale comando</span><span class="sxs-lookup"><span data-stu-id="2a74a-179">Specifically, for each command declared in the binary markup (see Step 3 above), the framework calls [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) to ask the application for an **IUICommandHandler** object for that command</span></span>

    > [!Note]  
    > <span data-ttu-id="2a74a-180">L'interfaccia [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) consente di associare un gestore di comando a uno o più comandi.</span><span class="sxs-lookup"><span data-stu-id="2a74a-180">The [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface allows a Command handler to be bound to one or more Commands.</span></span>

     

<span data-ttu-id="2a74a-181">Come minimo, l'applicazione deve implementare gli stub dei metodi [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) che restituiscono E \_ NOTIMPL, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="2a74a-181">At a minimum, the application is required to implement [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) methods stubs that return E\_NOTIMPL as shown in the following example.</span></span>


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a><span data-ttu-id="2a74a-182">Collegare il markup all'applicazione</span><span class="sxs-lookup"><span data-stu-id="2a74a-182">Link the Markup to the Application</span></span>

<span data-ttu-id="2a74a-183">A questo punto, i file di risorse di markup devono essere collegati all'applicazione host includendo un riferimento al file di definizione delle risorse di markup, che contiene un riferimento al file di intestazione di markup, nel file di risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-183">At this point, the markup resource files must be linked to the host application by including a reference to the markup resource-definition file (which contains a reference to the markup header file) in the application resource file.</span></span> <span data-ttu-id="2a74a-184">Ad esempio, un'applicazione denominata RibbonApp con un file di risorse denominato ribbonUI. RC richiede la riga seguente nel file RibbonApp. RC.</span><span class="sxs-lookup"><span data-stu-id="2a74a-184">For example, an application called RibbonApp with a resource file called ribbonUI.rc requires the following line in the RibbonApp.rc file.</span></span>


```C++
#include "ribbonUI.rc"
```



<span data-ttu-id="2a74a-185">A seconda del compilatore e del linker utilizzati, è possibile che anche lo script di definizione della risorsa richieda la compilazione prima che l'applicazione Ribbon possa essere compilata.</span><span class="sxs-lookup"><span data-stu-id="2a74a-185">Depending on the compiler and linker being used, the resource-definition script may also require compiling before the Ribbon application can be compiled.</span></span> <span data-ttu-id="2a74a-186">Lo strumento da riga di comando del [compilatore di risorse (RC)](../menurc/using-rc-the-rc-command-line-.md) fornito con Microsoft Visual Studio e il Windows SDK può essere utilizzato per questa attività.</span><span class="sxs-lookup"><span data-stu-id="2a74a-186">The [resource compiler (RC)](../menurc/using-rc-the-rc-command-line-.md) command line tool that ships with Microsoft Visual Studio and the Windows SDK can be used for this task.</span></span>

### <a name="compile-the-application"></a><span data-ttu-id="2a74a-187">Compilare l'applicazione</span><span class="sxs-lookup"><span data-stu-id="2a74a-187">Compile the Application</span></span>

<span data-ttu-id="2a74a-188">Una volta compilata l'applicazione Ribbon, è possibile eseguirla e testare l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="2a74a-188">Once the Ribbon application is compiled, it can be run and the UI tested.</span></span> <span data-ttu-id="2a74a-189">Se l'interfaccia utente richiede la modifica e non vi sono modifiche ai gestori di comandi associati nel codice dell'applicazione principale, modificare il file di origine di markup, ricompilare il markup con UICC.exe e collegare i nuovi file di risorse di markup.</span><span class="sxs-lookup"><span data-stu-id="2a74a-189">If the UI requires tweaking and there are no changes to any associated Command handlers in the core application code, revise the markup source file, recompile the markup with UICC.exe, and link the new markup resource files.</span></span> <span data-ttu-id="2a74a-190">Quando l'applicazione viene riavviata, viene visualizzata l'interfaccia utente modificata.</span><span class="sxs-lookup"><span data-stu-id="2a74a-190">When the application is restarted, the modified UI is displayed.</span></span>

<span data-ttu-id="2a74a-191">Tutto questo è possibile senza modificare il codice dell'applicazione principale, ovvero un miglioramento significativo dello sviluppo e della distribuzione di applicazioni standard.</span><span class="sxs-lookup"><span data-stu-id="2a74a-191">All this is possible without touching the core application code—a significant improvement over standard application development and distribution.</span></span>

## <a name="run-time-updates-and-executions"></a><span data-ttu-id="2a74a-192">Aggiornamenti ed esecuzioni in fase di esecuzione</span><span class="sxs-lookup"><span data-stu-id="2a74a-192">Run Time Updates and Executions</span></span>

<span data-ttu-id="2a74a-193">La struttura di comunicazione in fase di esecuzione del Framework della barra multifunzione è basata su un modello di push e pull o di un chiamante bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="2a74a-193">The run-time communication structure of the Ribbon framework is based on a push and pull, or two-way caller, model.</span></span>

<span data-ttu-id="2a74a-194">Questo modello consente al Framework di informare l'applicazione quando viene eseguito un comando e consente al Framework e all'applicazione di eseguire query, aggiornare e invalidare i valori delle proprietà e le risorse della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-194">This model allows the framework to inform the application when a Command is executed and allows both the framework and the application to query, update, and invalidate property values and Ribbon resources.</span></span> <span data-ttu-id="2a74a-195">Questa funzionalità viene fornita tramite una serie di interfacce e metodi.</span><span class="sxs-lookup"><span data-stu-id="2a74a-195">This functionality is provided through a number of interfaces and methods.</span></span>

<span data-ttu-id="2a74a-196">Il Framework esegue il pull delle informazioni aggiornate sulla proprietà dall'applicazione Ribbon tramite il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="2a74a-196">The framework pulls updated property information from the Ribbon application through the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span> <span data-ttu-id="2a74a-197">Un ID di comando e una chiave di proprietà, che identifica la proprietà del comando da aggiornare, vengono passati al metodo che quindi restituisce, o effettua il push, un valore per la chiave della proprietà nel Framework.</span><span class="sxs-lookup"><span data-stu-id="2a74a-197">A Command ID and a property key, which identifies the Command property to update, are passed to the method which then returns, or pushes, a value for that property key to the framework.</span></span>

<span data-ttu-id="2a74a-198">Il Framework chiama [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando viene eseguito un comando, identificando sia l'ID del comando sia il tipo di esecuzione che si è verificata ([**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)).</span><span class="sxs-lookup"><span data-stu-id="2a74a-198">The framework calls [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) when a Command is executed, identifying both the Command ID and the type of execution that occurred ([**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)).</span></span> <span data-ttu-id="2a74a-199">Questo è il punto in cui l'applicazione specifica la logica di esecuzione per un comando.</span><span class="sxs-lookup"><span data-stu-id="2a74a-199">This is where the application specifies the execution logic for a command.</span></span>

<span data-ttu-id="2a74a-200">Il diagramma seguente illustra la comunicazione di run-time per l'esecuzione dei comandi tra il Framework e l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-200">The following diagram illustrates the run-time communication for Command execution between the framework and the application.</span></span>

![diagramma che mostra un esempio della comunicazione di run-time tra il Framework della barra multifunzione e un'applicazione host.](images/overviews/updatesandexecutions.png)

> [!Note]  
> <span data-ttu-id="2a74a-202">L'implementazione delle funzioni [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) e [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) non è necessaria per visualizzare inizialmente una barra multifunzione in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2a74a-202">Implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) and [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) functions is not necessary to initially display a Ribbon in an application.</span></span> <span data-ttu-id="2a74a-203">Tuttavia, questi metodi sono necessari per garantire che l'applicazione funzioni correttamente quando i comandi vengono eseguiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2a74a-203">However, these methods are necessary to ensure that the application functions correctly when commands are executed by the user.</span></span>

 

## <a name="ole-support"></a><span data-ttu-id="2a74a-204">Supporto OLE</span><span class="sxs-lookup"><span data-stu-id="2a74a-204">OLE Support</span></span>

<span data-ttu-id="2a74a-205">Un'applicazione Ribbon può essere configurata come server OLE per supportare l'attivazione OLE fuori sede.</span><span class="sxs-lookup"><span data-stu-id="2a74a-205">A Ribbon application can be configured as an OLE server to support out-of-place OLE activation.</span></span>

<span data-ttu-id="2a74a-206">Gli oggetti creati in un'applicazione server OLE mantengono l'associazione con l'applicazione server quando vengono inseriti (incollati o posizionati) in un'applicazione client OLE (o contenitore).</span><span class="sxs-lookup"><span data-stu-id="2a74a-206">Objects created in an OLE server application maintain their association with the server application when inserted (either pasted or placed) into an OLE client application (or container).</span></span> <span data-ttu-id="2a74a-207">Nell'attivazione OLE fuori sede, facendo doppio clic sull'oggetto nell'applicazione client viene aperta un'istanza dedicata dell'applicazione server e viene caricato l'oggetto per la modifica.</span><span class="sxs-lookup"><span data-stu-id="2a74a-207">In out-of-place OLE activation, double clicking the object in the client application opens a dedicated instance of the server application and loads the object for editing.</span></span> <span data-ttu-id="2a74a-208">Quando l'applicazione server viene chiusa, tutte le modifiche apportate all'oggetto vengono riflesse nell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="2a74a-208">When the server application is closed, all changes made to the object are reflected in the client application.</span></span>

> [!Note]  
> <span data-ttu-id="2a74a-209">Il Framework della barra multifunzione non supporta l'attivazione OLE sul posto.</span><span class="sxs-lookup"><span data-stu-id="2a74a-209">The Ribbon framework does not support in-place OLE activation.</span></span> <span data-ttu-id="2a74a-210">Impossibile modificare gli oggetti creati in un server OLE basato su barra multifunzione dall'interno dell'applicazione client OLE.</span><span class="sxs-lookup"><span data-stu-id="2a74a-210">Objects created in a Ribbon-based OLE server cannot be edited from within the OLE client application.</span></span> <span data-ttu-id="2a74a-211">È necessaria un'istanza esterna dedicata dell'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="2a74a-211">An external dedicated instance of the server application is required.</span></span>


## <a name="related-topics"></a><span data-ttu-id="2a74a-212">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a74a-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a74a-213">Dichiarazione di comandi e controlli con markup della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="2a74a-213">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="2a74a-214">Linee guida sull'esperienza utente della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="2a74a-214">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="2a74a-215">Processo di progettazione della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="2a74a-215">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




