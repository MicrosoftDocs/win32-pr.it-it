---
title: Creazione del file di immagine principale
description: Creazione del file di immagine principale
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- creazione di interfacce, file di immagine principali
- Interfacce di Media Player di Windows, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, immagini primarie
- Windows Media Player Skin, immagini primarie
- interfacce, immagini primarie
- immagini primarie nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104557334"
---
# <a name="creating-the-primary-art-file"></a><span data-ttu-id="0ca36-111">Creazione del file di immagine principale</span><span class="sxs-lookup"><span data-stu-id="0ca36-111">Creating the Primary Art File</span></span>

<span data-ttu-id="0ca36-112">Il file di immagine principale conterrà l'immagine che l'utente dell'interfaccia vede per primo.</span><span class="sxs-lookup"><span data-stu-id="0ca36-112">The primary art file will contain the art that the user of your skin first sees.</span></span> <span data-ttu-id="0ca36-113">In questo caso, verranno create immagini in diversi livelli del programma Art.</span><span class="sxs-lookup"><span data-stu-id="0ca36-113">In this case, you will be creating images in different layers of your art program.</span></span> <span data-ttu-id="0ca36-114">Il motivo per l'uso dei livelli è che i livelli specifici vengono copiati in un secondo momento per creare file di mapping e file di grafica alternativi.</span><span class="sxs-lookup"><span data-stu-id="0ca36-114">The reason for using layers is that you will copy specific layers later to create map files and alternate art files.</span></span>

<span data-ttu-id="0ca36-115">Per creare il file di immagine principale, si creeranno i livelli seguenti nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="0ca36-115">To create the primary art file, you will create the following layers in the following order:</span></span>

<span data-ttu-id="0ca36-116">Livello sfondo interfaccia</span><span class="sxs-lookup"><span data-stu-id="0ca36-116">Skin background layer</span></span>

<span data-ttu-id="0ca36-117">Si tratta del colore che sarà trasparente quando verrà visualizzata l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0ca36-117">This is the color that will be transparent when the skin is displayed.</span></span> <span data-ttu-id="0ca36-118">Per prima cosa, creare un livello, ma scegliere il colore finale del livello dopo aver scelto un colore per il livello contenitore dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0ca36-118">Create a layer for this first, but choose the final color of this layer after you chose a color for the skin container layer.</span></span> <span data-ttu-id="0ca36-119">Questo colore deve essere simile a, ma non allo stesso modo del livello contenitore dell'interfaccia, per nascondere eventuali effetti anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="0ca36-119">This color should be similar to, but not the same as, the skin container layer, to hide any anti-aliasing effects.</span></span>

<span data-ttu-id="0ca36-120">Livello contenitore interfaccia</span><span class="sxs-lookup"><span data-stu-id="0ca36-120">Skin container layer</span></span>

<span data-ttu-id="0ca36-121">Si tratta dell'immagine che formerà il contorno dell'interfaccia e sarà ciò che viene visualizzato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="0ca36-121">This is the image that will form the outline of your skin and will be what the user sees.</span></span> <span data-ttu-id="0ca36-122">In questo esempio sarà anche il contenitore per i due pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0ca36-122">It also will be the container for the two buttons in this example.</span></span> <span data-ttu-id="0ca36-123">Si pensi alla propria interfaccia come a un contenitore per i controlli dell'interfaccia utente, ad esempio pulsanti, dispositivi di scorrimento e così via.</span><span class="sxs-lookup"><span data-stu-id="0ca36-123">Think of your skin as a container for user interface controls such as buttons, sliders, and so on.</span></span> <span data-ttu-id="0ca36-124">In questo esempio, il contenitore è un ovale giallo.</span><span class="sxs-lookup"><span data-stu-id="0ca36-124">In this example, the container is a yellow oval.</span></span>

<span data-ttu-id="0ca36-125">Livelli pulsante Riproduci e Chiudi</span><span class="sxs-lookup"><span data-stu-id="0ca36-125">Play and Close button layers</span></span>

<span data-ttu-id="0ca36-126">Questi sono i due controlli dell'interfaccia utente usati in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="0ca36-126">These are the two user interface controls that this example uses.</span></span> <span data-ttu-id="0ca36-127">Si inseriranno in livelli distinti per poterli modificare facilmente o copiarli in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="0ca36-127">You will put them in separate layers so that you can easily adjust them or copy them later.</span></span>

<span data-ttu-id="0ca36-128">Prima di creare i livelli, è necessario creare il file che conterrà i livelli.</span><span class="sxs-lookup"><span data-stu-id="0ca36-128">Before you create your layers, you must create the file that will hold your layers.</span></span> <span data-ttu-id="0ca36-129">Avviare Photoshop e creare un nuovo file con dimensioni massime di 100 pixel e 200 pixel di larghezza.</span><span class="sxs-lookup"><span data-stu-id="0ca36-129">Start up Photoshop and create a new file that is 100 pixels high and 200 pixels wide.</span></span> <span data-ttu-id="0ca36-130">Il file utilizzato per creare l'immagine per questo esempio è denominato tiny.psd ed è incluso nell'SDK.</span><span class="sxs-lookup"><span data-stu-id="0ca36-130">The file used to create the art for this sample is called tiny.psd and is included with the SDK.</span></span>

<span data-ttu-id="0ca36-131">Tutte le istruzioni sono fornite in termini di Photoshop, ma è possibile usare qualsiasi altro programma artistico per creare interfacce, purché sia possibile salvare in uno dei formati di file supportati da Windows Media Player (BMP, GIF, JPG e PNG).</span><span class="sxs-lookup"><span data-stu-id="0ca36-131">All instructions are given in terms of Photoshop, but any other art program can be used to create skins as long as you can save to one of the file formats supported by the Windows Media Player (BMP, GIF, JPG, and PNG).</span></span> <span data-ttu-id="0ca36-132">La creazione di Skin è più semplice se si usa un programma artistico con livelli, ad esempio Adobe Photoshop, Jasc Paint Shop Pro o la viscosità di Jedor.</span><span class="sxs-lookup"><span data-stu-id="0ca36-132">You will find skin creation easier if you use an art program that has layers, such as Adobe Photoshop, Jasc Paint Shop Pro, or Jedor Viscosity.</span></span> <span data-ttu-id="0ca36-133">I livelli sono estremamente utili perché le immagini devono essere allineate correttamente per il mapping delle immagini e la visualizzazione di immagini alternative.</span><span class="sxs-lookup"><span data-stu-id="0ca36-133">Layers are extremely useful because images must be properly aligned for image mapping and display of alternative images.</span></span>

## <a name="skin-background-layer"></a><span data-ttu-id="0ca36-134">Livello sfondo interfaccia</span><span class="sxs-lookup"><span data-stu-id="0ca36-134">Skin Background Layer</span></span>

<span data-ttu-id="0ca36-135">Creare un nuovo livello e denominarlo "sfondo interfaccia".</span><span class="sxs-lookup"><span data-stu-id="0ca36-135">Create a new layer and name it "Skin background".</span></span> <span data-ttu-id="0ca36-136">Questo diventerà il colore di trasparenza che verrà definito nel file di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0ca36-136">This will become the transparency color you will define in the skin definition file.</span></span> <span data-ttu-id="0ca36-137">Attendere che il colore per il contenitore di Skin venga scelto prima di riempire il livello di sfondo dell'interfaccia con un colore specifico.</span><span class="sxs-lookup"><span data-stu-id="0ca36-137">Wait until the color for the skin container is chosen before filling the skin background layer with a specific color.</span></span>

## <a name="skin-container-layer"></a><span data-ttu-id="0ca36-138">Livello contenitore interfaccia</span><span class="sxs-lookup"><span data-stu-id="0ca36-138">Skin Container Layer</span></span>

<span data-ttu-id="0ca36-139">Successivamente, creare un nuovo livello e chiamarlo "contenitore di skin".</span><span class="sxs-lookup"><span data-stu-id="0ca36-139">Next create a new layer and call it "Skin container".</span></span> <span data-ttu-id="0ca36-140">Verranno definiti i bordi dell'interfaccia e sarà il contenitore per i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0ca36-140">This will define the edges of your skin and will be the container for the buttons.</span></span>

<span data-ttu-id="0ca36-141">Scegliere un colore di primo piano per la forma utilizzando i dispositivi di scorrimento dei colori Web.</span><span class="sxs-lookup"><span data-stu-id="0ca36-141">Choose a foreground color for the shape, using the Web color sliders.</span></span> <span data-ttu-id="0ca36-142">In questo esempio \# è stato scelto il colore "DBDD11".</span><span class="sxs-lookup"><span data-stu-id="0ca36-142">In this example, the color "\#DBDD11" was chosen.</span></span>

<span data-ttu-id="0ca36-143">Successivamente, creare una forma ovale.</span><span class="sxs-lookup"><span data-stu-id="0ca36-143">Next create an oval shape.</span></span> <span data-ttu-id="0ca36-144">Il modo più semplice consiste nell'usare lo strumento ellittica Marquee e creare una selezione ovale.</span><span class="sxs-lookup"><span data-stu-id="0ca36-144">The easiest way is to use the Eliptical Marquee tool and create an oval selection.</span></span> <span data-ttu-id="0ca36-145">Quando è stata creata una selezione ovale che rappresenta le dimensioni e la forma desiderate, riempire la selezione con il colore di primo piano e annullare la selezione.</span><span class="sxs-lookup"><span data-stu-id="0ca36-145">When you have created an oval selection that is the size and shape you want, fill the selection with the foreground color and cancel the selection.</span></span>

<span data-ttu-id="0ca36-146">Infine, per rendere questo aspetto leggermente più interessante, applicare l'effetto del livello di smussatura e rilievo con i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0ca36-146">Finally, to make this look a bit more interesting, apply the layer effect of Bevel and Emboss with the default values.</span></span>

<span data-ttu-id="0ca36-147">Il livello del contenitore dell'interfaccia utente dovrebbe essere simile a quello illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="0ca36-147">Your skin container layer should look like the following illustration.</span></span>

![livello contenitore interfaccia](images/g01cont.png)

## <a name="background-skin-color"></a><span data-ttu-id="0ca36-149">Colore della pelle di sfondo</span><span class="sxs-lookup"><span data-stu-id="0ca36-149">Background Skin Color</span></span>

<span data-ttu-id="0ca36-150">Ora che è stato scelto un colore di primo piano per la forma del contenitore di skin, è possibile scegliere un colore simile per il livello di sfondo della pelle.</span><span class="sxs-lookup"><span data-stu-id="0ca36-150">Now that you have chosen a foreground color for your skin container shape, you can choose a similar color for your skin background layer.</span></span> <span data-ttu-id="0ca36-151">Non si vuole esattamente lo stesso colore o il contenitore Skin sarà anche trasparente.</span><span class="sxs-lookup"><span data-stu-id="0ca36-151">You do not want the exact same color, or your skin container will be transparent also.</span></span> <span data-ttu-id="0ca36-152">In realtà, assicurarsi di non usare questo colore esatto in qualsiasi altra parte dell'interfaccia, neanche nelle fotografie, perché ogni volta che viene visualizzato questo colore, viene visualizzata l'immagine del desktop.</span><span class="sxs-lookup"><span data-stu-id="0ca36-152">In fact, be sure you do not use this exact color anywhere else in your skin, even in photographs, because wherever this color appears, the desktop image will appear instead.</span></span>

<span data-ttu-id="0ca36-153">Si desidera un colore vicino al colore del contenitore dell'interfaccia per evitare effetti anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="0ca36-153">You want a color close to the skin container color to avoid anti-aliasing effects.</span></span> <span data-ttu-id="0ca36-154">Se, ad esempio, si dispone di uno sfondo nero, alcuni bit del nero possono apparire intorno al bordo della pelle.</span><span class="sxs-lookup"><span data-stu-id="0ca36-154">For example, if you have a black background, some bits of black may show up around the edge of your skin.</span></span> <span data-ttu-id="0ca36-155">Scegliendo un colore vicino al colore del contenitore dell'interfaccia, eventuali pixel randagi visualizzati nel processo di anti-aliasing non verranno rilevati.</span><span class="sxs-lookup"><span data-stu-id="0ca36-155">By choosing a color close to the color of the skin container, any stray pixels that show up in the anti-aliasing process will be unnoticed.</span></span>

<span data-ttu-id="0ca36-156">L'anti-aliasing è il processo di smussatura dei bordi delle forme inclinate o curve.</span><span class="sxs-lookup"><span data-stu-id="0ca36-156">Anti-aliasing is the process of smoothing the edges of slanted or curved shapes.</span></span> <span data-ttu-id="0ca36-157">L'anti-aliasing crea nuovi colori, per pixel lungo i bordi di una forma, ovvero una combinazione del colore di primo piano e del colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="0ca36-157">Anti-aliasing creates new colors, for pixels along the edges of a shape, that are a blend of the foreground color and the background color.</span></span> <span data-ttu-id="0ca36-158">Alcuni di questi colori possono causare la mancata presenza di pixel quando il colore di sfondo viene reso trasparente.</span><span class="sxs-lookup"><span data-stu-id="0ca36-158">Some of these in-between colors can cause pixels to be missed when the background color is made transparent.</span></span>

<span data-ttu-id="0ca36-159">Il livello dello sfondo dell'interfaccia utente dovrebbe essere simile a quello illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="0ca36-159">Your skin background layer should look like the following illustration.</span></span>

![livello interfaccia di sfondo](images/g01backg.png)

## <a name="play-and-close-button-layers"></a><span data-ttu-id="0ca36-161">Livelli pulsante Riproduci e Chiudi</span><span class="sxs-lookup"><span data-stu-id="0ca36-161">Play and Close Button Layers</span></span>

<span data-ttu-id="0ca36-162">Creare un nuovo livello e denominarlo "Chiudi pulsante".</span><span class="sxs-lookup"><span data-stu-id="0ca36-162">Create a new layer and name it "Close button".</span></span> <span data-ttu-id="0ca36-163">Utilizzando di nuovo lo strumento ellittica Marquee Selection, creare un cerchio e posizionarlo sul lato sinistro dell'immagine complessiva.</span><span class="sxs-lookup"><span data-stu-id="0ca36-163">Using the Eliptical Marquee selection tool again, create a circle and position it on the left side of the overall image.</span></span> <span data-ttu-id="0ca36-164">Attivare la visibilità del file contenitore dell'interfaccia per facilitare la selezione.</span><span class="sxs-lookup"><span data-stu-id="0ca36-164">Turn on the visibility of the skin container file to help place the selection.</span></span>

<span data-ttu-id="0ca36-165">Quando si è soddisfatti della posizione, riempire la selezione con qualsiasi colore, ad eccezione del colore del contenitore o dello sfondo dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0ca36-165">When you are satisfied with the placement, fill the selection with any color (except the color of the skin container or the skin background).</span></span> <span data-ttu-id="0ca36-166">In questo esempio è stato scelto un colore viola.</span><span class="sxs-lookup"><span data-stu-id="0ca36-166">In this example, a purple color was chosen.</span></span> <span data-ttu-id="0ca36-167">Non è necessario ricordare il numero di colore.</span><span class="sxs-lookup"><span data-stu-id="0ca36-167">You do not need to remember the number of the color.</span></span> <span data-ttu-id="0ca36-168">Annullare quindi la selezione e applicare un altro effetto del livello di rilievo e smussatura predefinito.</span><span class="sxs-lookup"><span data-stu-id="0ca36-168">Then cancel the selection and apply another default Bevel and Emboss layer effect.</span></span> <span data-ttu-id="0ca36-169">Se si desidera applicare effetti non di livello al pulsante, creare una copia dell'originale per utilizzarlo in un secondo momento nel mapping.</span><span class="sxs-lookup"><span data-stu-id="0ca36-169">If you want to apply non-layer effects to your button, make a copy of the original for later use in mapping.</span></span>

<span data-ttu-id="0ca36-170">Il pulsante Chiudi avrà un aspetto simile a quello illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="0ca36-170">Your Close button should look like the following illustration.</span></span>

![pulsante di chiusura](images/g01qbut.png)

<span data-ttu-id="0ca36-172">Creare un nuovo livello e denominarlo "pulsante Riproduci".</span><span class="sxs-lookup"><span data-stu-id="0ca36-172">Create a new layer and name it "Play button".</span></span> <span data-ttu-id="0ca36-173">Utilizzare le stesse tecniche effettuate per il pulsante Chiudi, ma assegnare un colore diverso.</span><span class="sxs-lookup"><span data-stu-id="0ca36-173">Use the same techniques you did for the Close button, but give it a different color.</span></span> <span data-ttu-id="0ca36-174">In questo caso, è stato scelto il colore di un pulsante rosa, ma è possibile usare qualsiasi colore, purché non sia lo stesso colore del contenitore di Skin (perché si mescolerà nel contenitore) o il colore di sfondo dell'interfaccia (perché diventerebbe trasparente).</span><span class="sxs-lookup"><span data-stu-id="0ca36-174">In this case, a pink button color was chosen, but any color can be used as long as it is not the same color as the skin container (because it would blend into the container) or the skin background color (because it would become transparent).</span></span>

<span data-ttu-id="0ca36-175">Il pulsante Riproduci avrà un aspetto simile a quello illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="0ca36-175">Your Play button should look like the following illustration.</span></span>

![pulsante Riproduci](images/g01pbut.png)

## <a name="combine-layers-and-save"></a><span data-ttu-id="0ca36-177">Combinare i livelli e salvare</span><span class="sxs-lookup"><span data-stu-id="0ca36-177">Combine Layers and Save</span></span>

<span data-ttu-id="0ca36-178">A questo punto è possibile creare il file di immagine principale.</span><span class="sxs-lookup"><span data-stu-id="0ca36-178">You are now ready to create the primary art file.</span></span> <span data-ttu-id="0ca36-179">Nascondi tutti i livelli e Mostra solo i livelli seguenti, in questo ordine (dall'alto verso il basso):</span><span class="sxs-lookup"><span data-stu-id="0ca36-179">Hide all layers and then show only the following layers, in this order (top to bottom):</span></span>

<span data-ttu-id="0ca36-180">Pulsante Riproduci</span><span class="sxs-lookup"><span data-stu-id="0ca36-180">Play button</span></span>

<span data-ttu-id="0ca36-181">Pulsante Chiudi</span><span class="sxs-lookup"><span data-stu-id="0ca36-181">Close button</span></span>

<span data-ttu-id="0ca36-182">Contenitore Skin</span><span class="sxs-lookup"><span data-stu-id="0ca36-182">Skin container</span></span>

<span data-ttu-id="0ca36-183">Sfondo interfaccia</span><span class="sxs-lookup"><span data-stu-id="0ca36-183">Skin background</span></span>

<span data-ttu-id="0ca36-184">Salvare in un nuovo file usando il comando Salva copia dal menu file.</span><span class="sxs-lookup"><span data-stu-id="0ca36-184">Save to a new file using the Save a Copy command from the File menu.</span></span> <span data-ttu-id="0ca36-185">Selezionare l'opzione BMP nella parte Salva come della finestra di dialogo Salva copia e digitare il nome di un file a cui si fa riferimento in un secondo momento nel file di definizione dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0ca36-185">Select the BMP option in the Save As portion of the Save a Copy dialog box and type a file name that you will refer to later in your skin definition file.</span></span> <span data-ttu-id="0ca36-186">Idealmente, è consigliabile salvarlo nella stessa directory del file di definizione dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0ca36-186">Ideally you should save this in the same directory as your skin definition file.</span></span> <span data-ttu-id="0ca36-187">Ad esempio, è possibile chiamare questo background.bmp.</span><span class="sxs-lookup"><span data-stu-id="0ca36-187">For example, you could call this background.bmp.</span></span> <span data-ttu-id="0ca36-188">Scegliere le impostazioni predefinite e salvare il file.</span><span class="sxs-lookup"><span data-stu-id="0ca36-188">Choose the default settings and save the file.</span></span>

<span data-ttu-id="0ca36-189">Il file di immagine principale dovrebbe essere simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="0ca36-189">Your primary art file should look like this:</span></span>

![file di immagine principale](images/g01prime.png)

<span data-ttu-id="0ca36-191">Questo nome file verrà usato come valore per l'attributo **BackgroundImage** dell'elemento **View** nel file di definizione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0ca36-191">You will use this file name as the value for the **backgroundImage** attribute of the **VIEW** element in your skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ca36-192">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ca36-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ca36-193">**Creazione della prima interfaccia**</span><span class="sxs-lookup"><span data-stu-id="0ca36-193">**Building Your First Skin**</span></span>](building-your-first-skin.md)
</dt> </dl>

 

 




