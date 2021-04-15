---
description: Uso di GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Uso di GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78118253d86a88231456b72dc8c42ed2a674f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529521"
---
# <a name="using-graphedit"></a><span data-ttu-id="ddf45-103">Uso di GraphEdit</span><span class="sxs-lookup"><span data-stu-id="ddf45-103">Using GraphEdit</span></span>

<span data-ttu-id="ddf45-104">GraphEdit è disponibile nel Software Development Kit (SDK) di Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).</span><span class="sxs-lookup"><span data-stu-id="ddf45-104">GraphEdit is available in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span>

<span data-ttu-id="ddf45-105">Il nome dell'applicazione GraphEdit è "graphedt.exe".</span><span class="sxs-lookup"><span data-stu-id="ddf45-105">The name of the GraphEdit application is "graphedt.exe".</span></span> <span data-ttu-id="ddf45-106">Dopo aver installato l'SDK, "graphedt.exe" si trova nella directory seguente: \[ programmi \] \\ Microsoft SDK \\ Windows \\ \[ versione \] \\ bin \\ .</span><span class="sxs-lookup"><span data-stu-id="ddf45-106">After you install the SDK, "graphedt.exe" is located in the following directory: \[Program Files\]\\Microsoft SDKs\\Windows\\\[version\]\\Bin\\.</span></span>

<span data-ttu-id="ddf45-107">Prima di eseguire GraphEdit, usare l'utilità regsvr32 per registrare le seguenti DLL, che si trovano nella stessa directory:</span><span class="sxs-lookup"><span data-stu-id="ddf45-107">Before running GraphEdit, use the regsvr32 utility to register the following DLLs, which are located in the same directory:</span></span>

-   <span data-ttu-id="ddf45-108">proppage.dll</span><span class="sxs-lookup"><span data-stu-id="ddf45-108">proppage.dll</span></span>
-   <span data-ttu-id="ddf45-109">evrprop.dll</span><span class="sxs-lookup"><span data-stu-id="ddf45-109">evrprop.dll</span></span>

<span data-ttu-id="ddf45-110">Queste DLL consentono a GraphEdit di visualizzare le pagine delle proprietà per alcuni dei filtri DirectShow incorporati.</span><span class="sxs-lookup"><span data-stu-id="ddf45-110">These DLLs enable GraphEdit to display property pages for some of the built-in DirectShow filters.</span></span>

## <a name="build-a-file-playback-graph"></a><span data-ttu-id="ddf45-111">Creazione di un grafico per la riproduzione di file</span><span class="sxs-lookup"><span data-stu-id="ddf45-111">Build a File Playback Graph</span></span>

<span data-ttu-id="ddf45-112">GraphEdit è in grado di creare un grafico di filtro per la riproduzione di file.</span><span class="sxs-lookup"><span data-stu-id="ddf45-112">GraphEdit can build a filter graph for file playback.</span></span> <span data-ttu-id="ddf45-113">Questa funzionalità equivale a chiamare il metodo [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ddf45-113">This feature is equivalent to calling the [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method in an application.</span></span> <span data-ttu-id="ddf45-114">Scegliere **rendering file multimediale** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="ddf45-114">From the **File** menu, click **Render Media File**.</span></span> <span data-ttu-id="ddf45-115">GraphEdit Visualizza una finestra di dialogo **Apri file** .</span><span class="sxs-lookup"><span data-stu-id="ddf45-115">GraphEdit displays an **Open File** dialog box.</span></span> <span data-ttu-id="ddf45-116">Selezionare un file multimediale e fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="ddf45-116">Select a multimedia file and click **Open**.</span></span> <span data-ttu-id="ddf45-117">GraphEdit compila un grafico di filtro per riprodurre il file selezionato.</span><span class="sxs-lookup"><span data-stu-id="ddf45-117">GraphEdit builds a filter graph to play the file you've selected.</span></span>

<span data-ttu-id="ddf45-118">È anche possibile eseguire il rendering di un file multimediale che si trova in un URL.</span><span class="sxs-lookup"><span data-stu-id="ddf45-118">You can also render a media file located at a URL.</span></span> <span data-ttu-id="ddf45-119">Scegliere **Render URL** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="ddf45-119">From the **File** menu, click **Render URL**.</span></span> <span data-ttu-id="ddf45-120">GraphEdit Visualizza una finestra di dialogo in cui digitare l'URL.</span><span class="sxs-lookup"><span data-stu-id="ddf45-120">GraphEdit displays a dialog box in which to type the URL.</span></span>

## <a name="build-a-filter-graph"></a><span data-ttu-id="ddf45-121">Creare un grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="ddf45-121">Build a Filter Graph</span></span>

<span data-ttu-id="ddf45-122">GraphEdit è in grado di creare un grafico di filtro personalizzato, usando uno dei filtri registrati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ddf45-122">GraphEdit can build a custom filter graph, using any of the filters registered on your system.</span></span> <span data-ttu-id="ddf45-123">Scegliere **Inserisci filtri** dal menu **grafo** .</span><span class="sxs-lookup"><span data-stu-id="ddf45-123">From the **Graph** menu, click **Insert Filters**.</span></span> <span data-ttu-id="ddf45-124">Viene visualizzata una finestra di dialogo con un elenco dei filtri presenti nel sistema, organizzati in base alla categoria filtro.</span><span class="sxs-lookup"><span data-stu-id="ddf45-124">A dialog box appears with a list of the filters on your system, organized by filter category.</span></span> <span data-ttu-id="ddf45-125">GraphEdit compila questo elenco dalle informazioni contenute nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ddf45-125">GraphEdit builds this list from information in the registry.</span></span> <span data-ttu-id="ddf45-126">Nella figura seguente viene illustrata la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ddf45-126">The following illustration shows the dialog box.</span></span>

![quali filtri si desidera inserire?](images/gedit12.png)

<span data-ttu-id="ddf45-128">Per aggiungere un filtro al grafico, selezionare il nome del filtro e fare clic sul pulsante **Inserisci filtri** oppure fare doppio clic sul nome del filtro.</span><span class="sxs-lookup"><span data-stu-id="ddf45-128">To add a filter to the graph, select the name of the filter and click the **Insert Filters** button, or double-click the filter name.</span></span> <span data-ttu-id="ddf45-129">Dopo aver aggiunto i filtri, è possibile connettere due filtri trascinando il mouse dal pin di output di un filtro al pin di input di un altro filtro.</span><span class="sxs-lookup"><span data-stu-id="ddf45-129">After you have added the filters, you can connect two filters by dragging the mouse from one filter's output pin to another filter's input pin.</span></span> <span data-ttu-id="ddf45-130">Se i pin accettano la connessione, GraphEdit disegna una freccia per connetterli.</span><span class="sxs-lookup"><span data-stu-id="ddf45-130">If the pins accept the connection, GraphEdit draws an arrow connecting them.</span></span>

![connessione di due filtri](images/gedit-connect.png)

## <a name="run-the-graph"></a><span data-ttu-id="ddf45-132">Eseguire il grafo</span><span class="sxs-lookup"><span data-stu-id="ddf45-132">Run the Graph</span></span>

<span data-ttu-id="ddf45-133">Una volta creato un grafico di filtro nella modifica del grafo, è possibile eseguire il grafo per verificare se funziona come previsto.</span><span class="sxs-lookup"><span data-stu-id="ddf45-133">Once you have built a filter graph in Graph Edit, you can run the graph to see whether it works as you expect.</span></span> <span data-ttu-id="ddf45-134">Il menu **grafico** contiene i comandi di menu **Riproduci**, **Sospendi** e **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="ddf45-134">The **Graph** menu contains the menu commands **Play**, **Pause**, and **Stop**.</span></span> <span data-ttu-id="ddf45-135">Questi comandi richiamano i metodi [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) , rispettivamente, [**vengono eseguiti**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**sospesi**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)e [**arrestati**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span><span class="sxs-lookup"><span data-stu-id="ddf45-135">These commands invoke to the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods [**Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause), and [**Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), respectively.</span></span> <span data-ttu-id="ddf45-136">La barra degli strumenti di GraphEdit include anche pulsanti per questi comandi:</span><span class="sxs-lookup"><span data-stu-id="ddf45-136">The GraphEdit toolbar has buttons for these commands, as well:</span></span>

![pulsanti Sospendi, Riproduci e arresta](images/gedit-toolbar.png)

> [!Note]  
> <span data-ttu-id="ddf45-138">Il comando GraphEdit **Stop** consente innanzitutto di sospendere il grafico e di cercare il tempo zero (presupponendo che il grafico sia ricercabile).</span><span class="sxs-lookup"><span data-stu-id="ddf45-138">The GraphEdit **Stop** command first pauses the graph and seeks to time zero (assuming the graph is seekable).</span></span> <span data-ttu-id="ddf45-139">Per la riproduzione di file, questa azione Reimposta la finestra video sul primo fotogramma.</span><span class="sxs-lookup"><span data-stu-id="ddf45-139">For file playback, this action resets the video window to the first frame.</span></span> <span data-ttu-id="ddf45-140">Quindi GraphEdit chiama [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span><span class="sxs-lookup"><span data-stu-id="ddf45-140">Then GraphEdit calls [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>

 

<span data-ttu-id="ddf45-141">Se il grafico è ricercabile, è possibile cercarlo trascinando la barra del dispositivo di scorrimento visualizzata sotto la barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="ddf45-141">If the graph is seekable, you can seek it by dragging the slider bar that appears below the toolbar.</span></span> <span data-ttu-id="ddf45-142">Il trascinamento della barra del dispositivo di scorrimento richiama il metodo [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="ddf45-142">Dragging the slider bar invokes the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="view-property-pages"></a><span data-ttu-id="ddf45-143">Visualizzare le pagine delle proprietà</span><span class="sxs-lookup"><span data-stu-id="ddf45-143">View Property Pages</span></span>

<span data-ttu-id="ddf45-144">Alcuni filtri supportano le pagine delle proprietà personalizzate, che forniscono un'interfaccia utente per l'impostazione delle proprietà nel filtro.</span><span class="sxs-lookup"><span data-stu-id="ddf45-144">Some filters support custom property pages, which provide a user interface for setting properties on the filter.</span></span> <span data-ttu-id="ddf45-145">Per visualizzare la pagina delle proprietà di un filtro in GraphEdit, fare clic con il pulsante destro del mouse sul filtro e scegliere **Proprietà** dalla finestra popup.</span><span class="sxs-lookup"><span data-stu-id="ddf45-145">To view a filter's property page in GraphEdit, right-click the filter and select **Properties** from the pop-up window.</span></span> <span data-ttu-id="ddf45-146">GraphEdit Visualizza una pagina delle proprietà che contiene le finestre delle proprietà definite dal filtro (se presente).</span><span class="sxs-lookup"><span data-stu-id="ddf45-146">GraphEdit displays a property page that contains the property sheets defined by the filter (if any).</span></span> <span data-ttu-id="ddf45-147">Inoltre, GraphEdit include una finestra delle proprietà per ogni pin nel filtro.</span><span class="sxs-lookup"><span data-stu-id="ddf45-147">In addition, GraphEdit includes a property sheet for each pin on the filter.</span></span> <span data-ttu-id="ddf45-148">Le finestre delle proprietà del pin sono definite da GraphEdit, non dal filtro.</span><span class="sxs-lookup"><span data-stu-id="ddf45-148">The pin property sheets are defined by GraphEdit, not by the filter.</span></span> <span data-ttu-id="ddf45-149">Se il PIN è connesso, nella finestra delle proprietà Aggiungi viene visualizzato il tipo di supporto per la connessione.</span><span class="sxs-lookup"><span data-stu-id="ddf45-149">If the pin is connected, the pin property sheet displays the media type for the connection.</span></span> <span data-ttu-id="ddf45-150">In caso contrario, elenca i tipi di supporto preferiti del PIN.</span><span class="sxs-lookup"><span data-stu-id="ddf45-150">Otherwise, it lists the pin's preferred media types.</span></span>

> [!Note]  
> <span data-ttu-id="ddf45-151">Per usare le pagine delle proprietà predefinite di GraphEdit, è necessario registrare proppage.dll.</span><span class="sxs-lookup"><span data-stu-id="ddf45-151">To use GraphEdit's built-in property pages, you must register proppage.dll.</span></span> <span data-ttu-id="ddf45-152">Questa DLL è disponibile nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ddf45-152">This DLL is available in the Windows SDK.</span></span> <span data-ttu-id="ddf45-153">La DLL contiene anche pagine di proprietà aggiuntive per alcuni filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ddf45-153">The DLL also contains additional property pages for some DirectShow filters.</span></span> <span data-ttu-id="ddf45-154">Queste pagine delle proprietà vengono fornite solo a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="ddf45-154">These property pages are provided for debugging purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ddf45-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ddf45-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddf45-156">Simulazione della creazione di grafici con GraphEdit</span><span class="sxs-lookup"><span data-stu-id="ddf45-156">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



