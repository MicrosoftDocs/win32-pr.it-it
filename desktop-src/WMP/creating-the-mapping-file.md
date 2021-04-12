---
title: Creazione del file di mapping
description: Creazione del file di mapping
ms.assetid: d882cd5b-1404-4dfd-8b51-a61e1505fae1
keywords:
- creazione di interfacce, mapping di file
- Interfacce di Media Player di Windows, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, mapping di immagini
- Interfacce di Media Player di Windows, mapping di immagini
- interfacce, mapping di immagini
- mapping di immagini in interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b71682f48ecdba098f76a9e27f656b27d5fe8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395339"
---
# <a name="creating-the-mapping-file"></a><span data-ttu-id="228ff-111">Creazione del file di mapping</span><span class="sxs-lookup"><span data-stu-id="228ff-111">Creating the Mapping File</span></span>

<span data-ttu-id="228ff-112">Una volta creati i componenti del file dell'immagine principale, è relativamente semplice creare un file di mapping.</span><span class="sxs-lookup"><span data-stu-id="228ff-112">Once you have created the pieces of your primary art file, it is relatively easy to create a mapping file.</span></span> <span data-ttu-id="228ff-113">Il nuovo file di mapping viene creato combinando l'arte dei livelli di due pulsanti già creati.</span><span class="sxs-lookup"><span data-stu-id="228ff-113">You will create the new mapping file by combining the art from the two button layers you already created.</span></span>

1.  <span data-ttu-id="228ff-114">Sarà necessario eseguire i due pulsanti creati per il file di immagine principale e copiarli in un nuovo livello.</span><span class="sxs-lookup"><span data-stu-id="228ff-114">You will need to take the two buttons you created for the primary art file and copy them to a new layer.</span></span> <span data-ttu-id="228ff-115">Usare i passaggi seguenti: copiare il livello del pulsante Chiudi, rimuovere gli effetti dei livelli e rinominarlo "Chiudi mappa".</span><span class="sxs-lookup"><span data-stu-id="228ff-115">Use the following steps: Copy the Close button layer, remove any Layer effects, and rename it "Close map".</span></span> <span data-ttu-id="228ff-116">L'arte dovrebbe apparire piatta senza smussature.</span><span class="sxs-lookup"><span data-stu-id="228ff-116">The art should look flat, with no bevels.</span></span>
2.  <span data-ttu-id="228ff-117">Usare la selezione colori per creare un colore di primo piano di rosso puro.</span><span class="sxs-lookup"><span data-stu-id="228ff-117">Use the Color Picker to create a foreground color of pure red.</span></span> <span data-ttu-id="228ff-118">Verificare che il valore del numero di colore sia " \# FF0000".</span><span class="sxs-lookup"><span data-stu-id="228ff-118">Be sure the color number value is "\#FF0000".</span></span> <span data-ttu-id="228ff-119">Usare quindi lo strumento Secchiello per riempire l'interno del cerchio del livello di chiusura della mappa.</span><span class="sxs-lookup"><span data-stu-id="228ff-119">Then use the Paint Bucket tool to fill the inside of the circle of the Close map layer.</span></span>
3.  <span data-ttu-id="228ff-120">Copiare il livello del pulsante Play, rimuovere gli effetti dei livelli e rinominarlo "Play map".</span><span class="sxs-lookup"><span data-stu-id="228ff-120">Copy the Play button layer, remove any Layer effects, and rename it "Play map".</span></span> <span data-ttu-id="228ff-121">Anche in questo caso, l'arte dovrebbe apparire piatta.</span><span class="sxs-lookup"><span data-stu-id="228ff-121">Again, the art should look flat.</span></span> <span data-ttu-id="228ff-122">Non si desiderano effetti nel livello di mapping poiché si definiscono solo le aree della bitmap che Windows Media Player utilizzerà per determinare il punto in cui il mouse esegue un'azione e l'operazione che si desidera eseguire.</span><span class="sxs-lookup"><span data-stu-id="228ff-122">You do not want any effects in the mapping layer because you are just defining regions of the bitmap that Windows Media Player will use to determine where the mouse performs an action and what you want to do with it.</span></span>
4.  <span data-ttu-id="228ff-123">Usare la selezione colori per creare un colore di primo piano di verde puro.</span><span class="sxs-lookup"><span data-stu-id="228ff-123">Use the Color Picker to create a foreground color of pure green.</span></span> <span data-ttu-id="228ff-124">Verificare che il valore del numero di colore sia " \# 00FF00".</span><span class="sxs-lookup"><span data-stu-id="228ff-124">Be sure the color number value is "\#00FF00".</span></span> <span data-ttu-id="228ff-125">Usare quindi lo strumento Secchiello per riempire l'interno del cerchio del livello mappa di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="228ff-125">Then use the Paint Bucket tool to fill the inside of the circle of the Play map layer.</span></span>

<span data-ttu-id="228ff-126">A questo punto è possibile creare il file di grafica di mapping.</span><span class="sxs-lookup"><span data-stu-id="228ff-126">You are now ready to create the mapping art file.</span></span> <span data-ttu-id="228ff-127">Nascondi tutti i livelli, quindi Mostra solo i livelli seguenti, in questo ordine (dall'alto verso il basso):</span><span class="sxs-lookup"><span data-stu-id="228ff-127">Hide all layers, and then show only the following layers, in this order (top to bottom):</span></span>

<span data-ttu-id="228ff-128">Esegui mapping</span><span class="sxs-lookup"><span data-stu-id="228ff-128">Play map</span></span>

<span data-ttu-id="228ff-129">Chiudi mappa</span><span class="sxs-lookup"><span data-stu-id="228ff-129">Close map</span></span>

<span data-ttu-id="228ff-130">Salvare in un nuovo file usando il comando Salva copia dal menu file.</span><span class="sxs-lookup"><span data-stu-id="228ff-130">Save to a new file using the Save a Copy command from the File menu.</span></span> <span data-ttu-id="228ff-131">Selezionare l'opzione BMP nella parte Salva come della finestra di dialogo Salva copia e digitare il nome di un file a cui si fa riferimento in un secondo momento nel file di definizione dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="228ff-131">Select the BMP option in the Save As portion of the Save a Copy dialog box and type a file name that you will refer to later in your skin definition file.</span></span> <span data-ttu-id="228ff-132">Idealmente deve trovarsi nella stessa directory del file di definizione dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="228ff-132">Ideally it should be in the same directory as your skin definition file.</span></span> <span data-ttu-id="228ff-133">Ad esempio, è possibile chiamare questo file map.bmp.</span><span class="sxs-lookup"><span data-stu-id="228ff-133">For example, you could call this file map.bmp.</span></span> <span data-ttu-id="228ff-134">Scegliere le impostazioni predefinite e salvare il file.</span><span class="sxs-lookup"><span data-stu-id="228ff-134">Choose the default settings and save the file.</span></span>

<span data-ttu-id="228ff-135">Il file di mapping dovrebbe avere un aspetto simile a quello illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="228ff-135">Your mapping file should look like the following illustration.</span></span>

![mapping file](images/g01map.png)

<span data-ttu-id="228ff-137">Come si può intuire, l'area verde verrà utilizzata per determinare quando creare Media Player Windows e l'area rossa indica che l'arresto.</span><span class="sxs-lookup"><span data-stu-id="228ff-137">As you might guess, the green area will be used to determine when to make Windows Media Player start and the red area is for telling it to stop.</span></span> <span data-ttu-id="228ff-138">È possibile utilizzare due colori qualsiasi, purché vengano utilizzati i numeri di colore quando si configura il file di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="228ff-138">Any two colors can be used, as long as you use the color numbers when you set up the skin definition file.</span></span> <span data-ttu-id="228ff-139">Assicurarsi che i colori della mappa siano colori puri per l'area che si vuole usare e che abbiano bordi distinti.</span><span class="sxs-lookup"><span data-stu-id="228ff-139">Be sure the colors in the map are pure colors for the region you want to use and have distinct edges.</span></span> <span data-ttu-id="228ff-140">Un colore puro è uno in cui ogni singolo pixel nell'area ha lo stesso valore di colore.</span><span class="sxs-lookup"><span data-stu-id="228ff-140">A pure color would be one where every single pixel in the area has the same color value.</span></span> <span data-ttu-id="228ff-141">L'uso di un effetto può offuscare o falsare il bordo, modificando leggermente i colori di alcuni pixel.</span><span class="sxs-lookup"><span data-stu-id="228ff-141">Using an effect may blur or distort the edge, thereby slightly modifying the colors of some of the pixels.</span></span> <span data-ttu-id="228ff-142">Il file di mapping viene visualizzato solo dal mouse, non da un utente, quindi non infastidirlo e rimuovere gli effetti dei livelli che potrebbero essere stati trasferiti dagli altri livelli.</span><span class="sxs-lookup"><span data-stu-id="228ff-142">The mapping file is only seen by the mouse, not a human, so do not bother decorating it, and remove any layer effects you may have carried over from other layers.</span></span>

<span data-ttu-id="228ff-143">Quando si salva il file, il nome file scelto verrà usato in un secondo momento come valore per l'attributo **mappingImage** dell'elemento **ButtonGroup** nel file di definizione dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="228ff-143">When you save your file, the file name you choose will later be used as the value for the **mappingImage** attribute of the **BUTTONGROUP** element in your skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="228ff-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="228ff-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="228ff-145">**Creazione della prima interfaccia**</span><span class="sxs-lookup"><span data-stu-id="228ff-145">**Building Your First Skin**</span></span>](building-your-first-skin.md)
</dt> </dl>

 

 




