---
title: Aggiunta dell'attributo ContentDistributor
description: Aggiunta dell'attributo ContentDistributor
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Windows Media Player Online Stores, aggiunta dell'attributo ContentDistributor
- archivi online, aggiunta dell'attributo ContentDistributor
- digitare 1 Store online, aggiunta dell'attributo ContentDistributor
- digitare 2 archivi online, aggiunta dell'attributo ContentDistributor
- Windows Media Player Online Stores, attributo ContentDistributor
- archivi online, attributo ContentDistributor
- digitare 1 Store online, attributo ContentDistributor
- digitare 2 archivi online, attributo ContentDistributor
- Aggiunta dell'attributo ContentDistributor
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330100"
---
# <a name="adding-the-contentdistributor-attribute"></a><span data-ttu-id="c8249-113">Aggiunta dell'attributo ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="c8249-113">Adding the ContentDistributor Attribute</span></span>

<span data-ttu-id="c8249-114">Quando l'utente tenta di riprodurre il contenuto di uno Store online o di copiare il contenuto in un CD o un dispositivo, Windows Media Player chiama determinati metodi nell'oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="c8249-114">When the user attempts to play online store content or to copy the content to a CD or device, Windows Media Player calls certain methods in your COM object.</span></span> <span data-ttu-id="c8249-115">A tale scopo, il lettore necessita di un modo per distinguere il contenuto da quello degli altri provider del negozio online.</span><span class="sxs-lookup"><span data-stu-id="c8249-115">To do this, the Player needs a way to differentiate your content from that of other online store providers.</span></span> <span data-ttu-id="c8249-116">Aggiungendo il nome della chiave del negozio online come valore per **contentdistributor** (un alias per l'attributo Windows Media Format SDK denominato **WM/contentdistributor**) al contenuto basato su Windows Media, si garantisce che il lettore possa identificare il contenuto associato al servizio.</span><span class="sxs-lookup"><span data-stu-id="c8249-116">By adding your online store key name as the value for the **ContentDistributor** (which is an alias for the Windows Media Format SDK attribute named **WM/ContentDistributor**) attribute to your Windows Media-based content, you ensure that the Player can identify the content associated with your service.</span></span>

<span data-ttu-id="c8249-117">L'aggiunta di un valore per **contentdistributor** garantisce inoltre che Windows Media Player creerà un nodo nella libreria per il contenuto fornito.</span><span class="sxs-lookup"><span data-stu-id="c8249-117">Adding a value for **ContentDistributor** also ensures that Windows Media Player will create a node in the library for content you provide.</span></span> <span data-ttu-id="c8249-118">Vedere [integrazione della libreria](library-integration.md).</span><span class="sxs-lookup"><span data-stu-id="c8249-118">See [Library Integration](library-integration.md).</span></span>

<span data-ttu-id="c8249-119">Questo valore può essere specificato in due modi:</span><span class="sxs-lookup"><span data-stu-id="c8249-119">You can specify this value two ways:</span></span>

-   <span data-ttu-id="c8249-120">Usare il modello a oggetti di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c8249-120">Use the Windows Media Player object model.</span></span> <span data-ttu-id="c8249-121">Quando si esegue questa operazione, Windows Media Player aggiunge il valore specificato al database di libreria.</span><span class="sxs-lookup"><span data-stu-id="c8249-121">When you do this, Windows Media Player adds the value you specify to the library database.</span></span> <span data-ttu-id="c8249-122">Infine, il lettore scriverà anche il valore dell'attributo nel file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="c8249-122">Eventually, the Player will also write the attribute value to the digital media file.</span></span>
-   <span data-ttu-id="c8249-123">Usare Windows Media Format SDK per aggiungere l'attributo **WM/contentdistributor** a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="c8249-123">Use the Windows Media Format SDK to programmatically add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="c8249-124">Quando si esegue questa operazione, Windows Media Player legge il valore dell'attributo e lo aggiunge al database quando il file multimediale digitale viene aggiunto alla libreria.</span><span class="sxs-lookup"><span data-stu-id="c8249-124">When you do this, Windows Media Player reads the attribute value and adds it to the database when the digital media file is added to the library.</span></span>

<span data-ttu-id="c8249-125">Quando si crea l'oggetto COM di archivio online, il valore dell'attributo file impostato per **contentdistributor** e il valore assegnato alla costante KszContentDistributorID in progettoutente. h devono corrispondere esattamente.</span><span class="sxs-lookup"><span data-stu-id="c8249-125">When creating your online store COM object, the file attribute value you set for **ContentDistributor** and the value assigned to the constant kszContentDistributorID in YourProject.h must match exactly.</span></span> <span data-ttu-id="c8249-126">Ricordare che è stato specificato questo valore costante per l'oggetto COM quando è stato creato il progetto tramite la creazione guidata progetto.</span><span class="sxs-lookup"><span data-stu-id="c8249-126">Recall that you specified this constant value for your COM object when you created the project by using the project wizard.</span></span> <span data-ttu-id="c8249-127">Questo valore può essere modificato manualmente.</span><span class="sxs-lookup"><span data-stu-id="c8249-127">You can change this value manually.</span></span> <span data-ttu-id="c8249-128">Assicurarsi di usare una stringa che identifichi in modo univoco il servizio.</span><span class="sxs-lookup"><span data-stu-id="c8249-128">Just be sure to use a string that uniquely identifies your service.</span></span>

## <a name="using-the-windows-media-player-object-model"></a><span data-ttu-id="c8249-129">Uso del modello a oggetti di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="c8249-129">Using the Windows Media Player Object Model</span></span>

<span data-ttu-id="c8249-130">Per specificare un valore per **contentdistributor** usando il modello a oggetti di Windows Media Player, usare il metodo [Media. setItemInfo](media-setiteminfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c8249-130">To specify a value for **ContentDistributor** using the Windows Media Player object model, use the [Media.setItemInfo](media-setiteminfo.md) method.</span></span> <span data-ttu-id="c8249-131">Il codice di esempio seguente specifica il valore "Proseware" per **contentdistributor** per l'elemento multimediale attualmente in riproduzione:</span><span class="sxs-lookup"><span data-stu-id="c8249-131">The following example code specifies the value "Proseware" for **ContentDistributor** for the currently playing media item:</span></span>


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a><span data-ttu-id="c8249-132">Uso di Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="c8249-132">Using the Windows Media Format SDK</span></span>

<span data-ttu-id="c8249-133">Windows Media Player SDK include un file C++ di esempio, denominato SetContentDistributor. cpp, che illustra come usare Windows Media Format 9 Series SDK per aggiungere l'attributo **WM/contentdistributor** .</span><span class="sxs-lookup"><span data-stu-id="c8249-133">The Windows Media Player SDK includes a sample C++ file, named SetContentDistributor.cpp, which demonstrates how to use the Windows Media Format 9 Series SDK to add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="c8249-134">È possibile individuare questo file di esempio nella cartella denominata Metadata in cui è stato installato l'SDK.</span><span class="sxs-lookup"><span data-stu-id="c8249-134">You can locate this sample file in the folder named Metadata where you installed the SDK.</span></span> <span data-ttu-id="c8249-135">Per usare questo codice è necessario attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="c8249-135">To use this code you must follow these steps:</span></span>

1.  <span data-ttu-id="c8249-136">Installare Windows Media Format 9 Series SDK e configurare il runtime come descritto nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="c8249-136">Install the Windows Media Format 9 Series SDK and configure the runtime as described in the documentation.</span></span>
2.  <span data-ttu-id="c8249-137">Creare un nuovo progetto C++ vuoto in Visual Studio e aggiungere al progetto il file di esempio denominato SetContentDistributor. cpp.</span><span class="sxs-lookup"><span data-stu-id="c8249-137">Create a new empty C++ project in Visual Studio and add the sample file named SetContentDistributor.cpp to the project.</span></span>
3.  <span data-ttu-id="c8249-138">Aggiungere il percorso delle cartelle lib di Windows Media Format 9 Series SDK all'elenco dei percorsi di file.</span><span class="sxs-lookup"><span data-stu-id="c8249-138">Add the path to the Windows Media Format 9 Series SDK Lib folders to your list of file paths.</span></span> <span data-ttu-id="c8249-139">Scegliere **Opzioni** dal menu **Strumenti**.</span><span class="sxs-lookup"><span data-stu-id="c8249-139">From the **Tools** menu, choose **Options**.</span></span>
4.  <span data-ttu-id="c8249-140">Nella finestra di dialogo **Opzioni** fare clic su **progetti**, quindi fare clic su **directory di VC + +**.</span><span class="sxs-lookup"><span data-stu-id="c8249-140">In the **Options** dialog box, click **Projects**, and then click **VC++ Directories**.</span></span>
5.  <span data-ttu-id="c8249-141">Nella casella di riepilogo **Visualizza directory per** fare clic su file di **libreria**.</span><span class="sxs-lookup"><span data-stu-id="c8249-141">In the **Show Directories for** drop-down list box, click **Library files**.</span></span>
6.  <span data-ttu-id="c8249-142">Utilizzare i pulsanti per aggiungere i percorsi alle caselle di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="c8249-142">Use the buttons to add the paths to the list boxes.</span></span>
7.  <span data-ttu-id="c8249-143">Aprire la finestra di dialogo Pagine delle proprietà per il progetto.</span><span class="sxs-lookup"><span data-stu-id="c8249-143">Open the property pages dialog box for your project.</span></span> <span data-ttu-id="c8249-144">Scegliere **proprietà di configurazione**, quindi **linker**, quindi **input**.</span><span class="sxs-lookup"><span data-stu-id="c8249-144">Choose **Configuration Properties**, then **Linker**, and then **Input**.</span></span> <span data-ttu-id="c8249-145">Digitare "Wmvcore. lib" nella casella di testo **dipendenze aggiuntive** .</span><span class="sxs-lookup"><span data-stu-id="c8249-145">Type "wmvcore.lib" in the **Additional Dependencies** text box.</span></span>

<span data-ttu-id="c8249-146">Il codice di esempio crea un programma da riga di comando.</span><span class="sxs-lookup"><span data-stu-id="c8249-146">The sample code creates a command-line program.</span></span> <span data-ttu-id="c8249-147">Gli argomenti forniti durante l'esecuzione del programma specificano il percorso del file multimediale digitale da modificare e una stringa per il valore dell'attributo **contentdistributor** .</span><span class="sxs-lookup"><span data-stu-id="c8249-147">The arguments you provide when running the program specify the path to the digital media file to modify and a string for the **ContentDistributor** attribute value.</span></span> <span data-ttu-id="c8249-148">Il codice usa **IWMHeaderInfo:: SetAttribute** per aggiungere l'attributo al file specificato.</span><span class="sxs-lookup"><span data-stu-id="c8249-148">The code uses **IWMHeaderInfo::SetAttribute** to add the attribute to the file you specified.</span></span> <span data-ttu-id="c8249-149">È possibile utilizzare questo esempio così com'è o utilizzarlo come punto di partenza per il programma.</span><span class="sxs-lookup"><span data-stu-id="c8249-149">You can use this sample as is or use it as a starting point for your own program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8249-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8249-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8249-151">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="c8249-151">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




