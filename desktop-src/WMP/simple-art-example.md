---
title: Esempio di arte semplice
description: Esempio di arte semplice
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Interfacce di Media Player di Windows, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, esempi
- Windows Media Player Skin, esempi
- interfacce, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab7b25dc33da70a627f8b0e126d6797b1bcdd9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710009"
---
# <a name="simple-art-example"></a><span data-ttu-id="080ff-109">Esempio di arte semplice</span><span class="sxs-lookup"><span data-stu-id="080ff-109">Simple Art Example</span></span>

<span data-ttu-id="080ff-110">Sono necessari tre file di immagine per creare un'interfaccia semplice con due pulsanti.</span><span class="sxs-lookup"><span data-stu-id="080ff-110">Three art files are needed to create a simple skin with two buttons.</span></span> <span data-ttu-id="080ff-111">Sono necessarie un'immagine primaria e un'immagine di mapping e un'immagine alternativa fornisce un segnale visivo all'utente che è possibile fare clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="080ff-111">A primary image and a mapping image are required, and an alternate image provides a visual cue to the user that a button is clickable.</span></span>

<span data-ttu-id="080ff-112">Questi file di immagine sono stati creati in un programma artistico che usa i livelli.</span><span class="sxs-lookup"><span data-stu-id="080ff-112">These art files were created in an art program that uses layers.</span></span> <span data-ttu-id="080ff-113">L'uso dei livelli semplifica la verifica dell'uniformità delle dimensioni delle immagini primarie, di mapping e alternative.</span><span class="sxs-lookup"><span data-stu-id="080ff-113">Using layers makes it easier to make sure that your primary, mapping, and alternate images are all the same size and line up with each other.</span></span>

<span data-ttu-id="080ff-114">Le istruzioni dettagliate sulla creazione dell'arte sono disponibili nella [Guida alla creazione dell'interfaccia](skin-creation-guide.md).</span><span class="sxs-lookup"><span data-stu-id="080ff-114">The detailed instructions on creating the art are in the [Skin Creation Guide](skin-creation-guide.md).</span></span>

## <a name="primary-image"></a><span data-ttu-id="080ff-115">Immagine primaria</span><span class="sxs-lookup"><span data-stu-id="080ff-115">Primary Image</span></span>

<span data-ttu-id="080ff-116">L'immagine principale è un semplice ovale giallo con due pulsanti, uno rosa per avviare Windows Media Player e il pulsante viola per arrestarlo.</span><span class="sxs-lookup"><span data-stu-id="080ff-116">The primary image is a simple yellow oval with two buttons, a pink one to start Windows Media Player and purple button to stop it.</span></span> <span data-ttu-id="080ff-117">Lo sfondo è un colore giallo leggermente più scuro rispetto all'ovale.</span><span class="sxs-lookup"><span data-stu-id="080ff-117">The background is a slightly darker yellow than the oval.</span></span> <span data-ttu-id="080ff-118">Questa immagine è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="080ff-118">This image is shown in the following illustration.</span></span>

![immagine primaria](images/absam01b.png)

<span data-ttu-id="080ff-120">L'immagine principale è stata dalle immagini seguenti, ognuna in un livello separato.</span><span class="sxs-lookup"><span data-stu-id="080ff-120">The primary image was from the following images, each in a separate layer.</span></span> <span data-ttu-id="080ff-121">Prima di tutto è stato creato un Oval con un effetto smussato e rilievo livello.</span><span class="sxs-lookup"><span data-stu-id="080ff-121">First an oval was created with a layer bevel and emboss effect.</span></span> <span data-ttu-id="080ff-122">Questa immagine è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="080ff-122">This image is shown in the following illustration.</span></span>

![immagine ovale](images/absam01s.png)

<span data-ttu-id="080ff-124">Sono stati creati i due pulsanti, anche con effetti smussato e rilievo del livello.</span><span class="sxs-lookup"><span data-stu-id="080ff-124">Then the two buttons were created, also with layer bevel and emboss effects.</span></span> <span data-ttu-id="080ff-125">Questo aspetto è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="080ff-125">This is shown in the following illustration.</span></span>

![due pulsanti](images/absam01p.png)

<span data-ttu-id="080ff-127">Successivamente è stato creato lo sfondo dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="080ff-127">Next the image background was created.</span></span> <span data-ttu-id="080ff-128">È stato scelto un giallo leggermente più scuro in modo che non venga notato alcun anti-aliasing tra l'ovale e lo sfondo.</span><span class="sxs-lookup"><span data-stu-id="080ff-128">A slightly darker yellow was chosen so that any anti-aliasing between the oval and the background will not be noticed.</span></span> <span data-ttu-id="080ff-129">Il valore del colore è \# CCCC00.</span><span class="sxs-lookup"><span data-stu-id="080ff-129">The color value is \#CCCC00.</span></span> <span data-ttu-id="080ff-130">Questa immagine è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="080ff-130">This image is shown in the following illustration.</span></span>

![immagine di sfondo](images/absam01y.png)

<span data-ttu-id="080ff-132">I livelli che contenevano queste immagini erano resi visibili e salvati come copia in formato bitmap, creando l'immagine principale.</span><span class="sxs-lookup"><span data-stu-id="080ff-132">The layers that contained these images were made visible and saved as a copy in bitmap format, creating the primary image.</span></span> <span data-ttu-id="080ff-133">L'immagine composita primaria verrà utilizzata dall'attributo **BackgroundImage** dell'elemento **View** .</span><span class="sxs-lookup"><span data-stu-id="080ff-133">The primary composite image will be used by the **backgroundImage** attribute of the **VIEW** element.</span></span>

## <a name="mapping-image"></a><span data-ttu-id="080ff-134">Immagine di mapping</span><span class="sxs-lookup"><span data-stu-id="080ff-134">Mapping Image</span></span>

<span data-ttu-id="080ff-135">È necessaria un'immagine di mapping per specificare quando e dove viene fatto clic su un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="080ff-135">A mapping image is needed to specify when and where a skin is clicked.</span></span> <span data-ttu-id="080ff-136">È stata creata un'immagine di mapping con un'area rossa e un'area verde.</span><span class="sxs-lookup"><span data-stu-id="080ff-136">A mapping image was created with a red area and a green area.</span></span> <span data-ttu-id="080ff-137">Questa immagine è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="080ff-137">This image is shown in the following illustration.</span></span>

![immagine di mapping](images/absam01m.png)

<span data-ttu-id="080ff-139">L'area verde verrà usata per identificare l'area nell'interfaccia che avvierà Windows Media Player e l'area rossa verrà usata per arrestarla.</span><span class="sxs-lookup"><span data-stu-id="080ff-139">The green area will be used to identify the area on the skin that will start Windows Media Player and the red area will be used to stop it.</span></span> <span data-ttu-id="080ff-140">L'immagine di mapping ha le stesse dimensioni dell'immagine principale.</span><span class="sxs-lookup"><span data-stu-id="080ff-140">The mapping image is the same size as the primary image.</span></span>

<span data-ttu-id="080ff-141">L'immagine di mapping è stata creata copiando il livello del pulsante in un nuovo livello e disattivando l'effetto smussatura e rilievo.</span><span class="sxs-lookup"><span data-stu-id="080ff-141">The mapping image was created by copying the button layer to a new layer and turning off the bevel and emboss effect.</span></span> <span data-ttu-id="080ff-142">Per il mapping sono necessarie immagini flat perché Windows Media Player cercherà i valori a colore singolo in ogni area.</span><span class="sxs-lookup"><span data-stu-id="080ff-142">Flat images are needed for mapping because Windows Media Player will be looking for single color values in each area.</span></span> <span data-ttu-id="080ff-143">Può solo cercare un colore definito, ad esempio rosso ( \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="080ff-143">It can only search for a color you define, such as red (\#FF0000).</span></span> <span data-ttu-id="080ff-144">Se l'immagine ha una smussatura o un altro effetto, non tutto sarà il rosso esatto necessario.</span><span class="sxs-lookup"><span data-stu-id="080ff-144">If your image has a bevel or other effect, not all of it will be the exact red you need.</span></span>

<span data-ttu-id="080ff-145">Per fare in modo che i pulsanti di mapping siano un colore semplice da ricordare, le immagini sono state riempite con il rosso puro e puro verde, ma è possibile usare qualsiasi colore.</span><span class="sxs-lookup"><span data-stu-id="080ff-145">To make the mapping buttons an easy color to remember, the images were filled with pure red and pure green, but any color can be used.</span></span> <span data-ttu-id="080ff-146">È necessario ricordare i numeri di colore nella mappa in modo che possano essere immessi nel file di definizione dell'interfaccia XML.</span><span class="sxs-lookup"><span data-stu-id="080ff-146">You will need to remember the color numbers in your map so that they can be entered in the XML skin definition file.</span></span> <span data-ttu-id="080ff-147">In questo caso, il colore rosso è \# ff0000 e verde è \# 00FF00.</span><span class="sxs-lookup"><span data-stu-id="080ff-147">In this case, red is \#FF0000 and green is \#00FF00.</span></span>

<span data-ttu-id="080ff-148">Quindi, solo con il nuovo livello visibile, l'immagine è stata salvata come copia in un file BMP.</span><span class="sxs-lookup"><span data-stu-id="080ff-148">Then, with only the new layer visible, the image was saved as a copy to a BMP file.</span></span> <span data-ttu-id="080ff-149">Verrà chiamato dall'attributo **mappingImage** dell'elemento **ButtonGroup** .</span><span class="sxs-lookup"><span data-stu-id="080ff-149">It will be called by the **mappingImage** attribute of the **BUTTONGROUP** element.</span></span>

## <a name="alternate-image"></a><span data-ttu-id="080ff-150">Immagine alternativa</span><span class="sxs-lookup"><span data-stu-id="080ff-150">Alternate Image</span></span>

<span data-ttu-id="080ff-151">Le immagini alternative non sono necessarie, ma sono molto utili per fornire segnali visivi all'utente.</span><span class="sxs-lookup"><span data-stu-id="080ff-151">Alternate images are not required but are very useful to give visual cues to the user.</span></span> <span data-ttu-id="080ff-152">In questo caso, è consigliabile usare un'immagine del passaggio del mouse in modo che l'utente sappia quali aree possono essere selezionate.</span><span class="sxs-lookup"><span data-stu-id="080ff-152">In this case, a hover image is recommended so that the user knows what areas can be clicked on.</span></span>

<span data-ttu-id="080ff-153">È stata creata un'immagine alternativa con due pulsanti gialli.</span><span class="sxs-lookup"><span data-stu-id="080ff-153">An alternate image was created with two yellow buttons.</span></span> <span data-ttu-id="080ff-154">Questo aspetto è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="080ff-154">This is shown in the following illustration.</span></span>

![immagine del passaggio del mouse](images/absam01h.png)

<span data-ttu-id="080ff-156">L'immagine alternativa è stata creata copiando il livello del pulsante originale in un nuovo livello e quindi cambiando il colore di riempimento in giallo.</span><span class="sxs-lookup"><span data-stu-id="080ff-156">The alternate image was created by copying the original button layer to a new layer and then changing the fill color to yellow.</span></span> <span data-ttu-id="080ff-157">L'effetto smussatura e rilievo è stato mantenuto.</span><span class="sxs-lookup"><span data-stu-id="080ff-157">The bevel and emboss effect was kept.</span></span> <span data-ttu-id="080ff-158">È stato creato un nuovo livello e sono state aggiunte le immagini: la freccia indica "Play" e il quadrato indica "Stop".</span><span class="sxs-lookup"><span data-stu-id="080ff-158">Then a new layer was created and images were added: the arrow indicates "play" and the square indicates "stop".</span></span> <span data-ttu-id="080ff-159">Quindi, con il nuovo pulsante giallo e i livelli di tipo visibili, l'immagine è stata salvata come copia in un file bitmap.</span><span class="sxs-lookup"><span data-stu-id="080ff-159">Then, with only the new yellow button and type layers visible, the image was saved as a copy to a bitmap file.</span></span>

<span data-ttu-id="080ff-160">Il risultato è che quando il mouse viene spostato su un'area definita dall'immagine di mapping, viene visualizzata l'immagine del passaggio del mouse, che avvisa il lettore che se fa clic su tale punto, può riprodurre o arrestare Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="080ff-160">The result is that when the mouse hovers over an area defined by the mapping image, the hover image will be displayed, alerting the reader that if they click on that spot, they can play or stop Windows Media Player.</span></span>

## <a name="final-image"></a><span data-ttu-id="080ff-161">Immagine finale</span><span class="sxs-lookup"><span data-stu-id="080ff-161">Final Image</span></span>

<span data-ttu-id="080ff-162">Di seguito è illustrata l'immagine finale dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="080ff-162">Here is the final image of the skin.</span></span>

![immagine finale](images/absam01f.png)

<span data-ttu-id="080ff-164">Si tratta dell'immagine che verrà visualizzata se si passa il mouse sul pulsante rosa a destra.</span><span class="sxs-lookup"><span data-stu-id="080ff-164">And this is the image you will see if you hover over the pink button on the right.</span></span>

![pulsante con il pulsante destro del mouse](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a><span data-ttu-id="080ff-166">Codice XML per l'esempio di arte</span><span class="sxs-lookup"><span data-stu-id="080ff-166">XML Code for the Art Example</span></span>

<span data-ttu-id="080ff-167">Di seguito sono riportati i dettagli relativi alla scrittura di codice XML nella [Guida alla creazione dell'interfaccia](skin-creation-guide.md), ma per mostrare la quantità di codice necessaria per creare un'interfaccia di lavoro, ecco il codice per l'artwork in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="080ff-167">The details of how to write XML code are given in the [Skin Creation Guide](skin-creation-guide.md), but to show how little code is needed to create a working skin, here is the code for the artwork in this example.</span></span>

<span data-ttu-id="080ff-168">I pulsanti predefiniti vengono usati per le funzioni play e stop.</span><span class="sxs-lookup"><span data-stu-id="080ff-168">Predefined buttons are used for the play and stop functions.</span></span> <span data-ttu-id="080ff-169">È necessario caricare un file o una playlist dal Windows Media Anchor.</span><span class="sxs-lookup"><span data-stu-id="080ff-169">You must load a file or playlist from the Windows Media anchor.</span></span> <span data-ttu-id="080ff-170">Quando Windows Media Player passa alla modalità Skin, viene visualizzata una piccola casella nell'angolo inferiore destro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="080ff-170">When Windows Media Player changes to skin mode, a small box appears in the lower-right corner of the screen.</span></span> <span data-ttu-id="080ff-171">Questa casella è denominata "ancoraggio".</span><span class="sxs-lookup"><span data-stu-id="080ff-171">This box is called the "anchor".</span></span> <span data-ttu-id="080ff-172">Facendo clic sull'ancoraggio si ottiene la funzionalità minima necessaria, nel caso in cui un'interfaccia non fornisca un modo per tornare alla modalità completa di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="080ff-172">Clicking the anchor gives you the minimum functionality needed, in case a skin does not provide a way to return to the full mode of Windows Media Player.</span></span> <span data-ttu-id="080ff-173">L'utente può passare da una modalità all'altra tramite il menu **Visualizza** se è in modalità completa oppure facendo clic sull'ancoraggio se in modalità interfaccia.</span><span class="sxs-lookup"><span data-stu-id="080ff-173">The user can switch between modes by using the **View** menu if in full mode, or by clicking the anchor if in skin mode.</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a><span data-ttu-id="080ff-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="080ff-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="080ff-175">**File di immagine**</span><span class="sxs-lookup"><span data-stu-id="080ff-175">**Art Files**</span></span>](art-files.md)
</dt> </dl>

 

 




