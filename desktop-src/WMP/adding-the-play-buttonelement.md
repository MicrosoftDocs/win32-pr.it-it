---
title: Aggiunta del pulsante di riproduzione
description: Aggiunta del pulsante di riproduzione
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- creazione di interfacce, elemento BUTTONelement
- Windows Media Player Skin, elemento BUTTONelement
- interfacce, elemento BUTTONelement
- file di definizione dell'interfaccia, elemento BUTTONelement
- BUTTONelement (elemento)
- Elements, BUTTONelement
- creazione di interfacce, pulsanti di riproduzione
- Interfacce di Media Player di Windows, pulsanti di riproduzione
- interfacce, pulsanti di riproduzione
- file di definizione dell'interfaccia, pulsanti di riproduzione
- Pulsanti di riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515787"
---
# <a name="adding-the-play-buttonelement"></a><span data-ttu-id="22762-114">Aggiunta del pulsante di riproduzione</span><span class="sxs-lookup"><span data-stu-id="22762-114">Adding the Play BUTTONELEMENT</span></span>

<span data-ttu-id="22762-115">Infine, è possibile aggiungere gli elementi **ButtonElement** che connettono i pulsanti visivi sullo schermo alle azioni di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="22762-115">Finally, you can add the **BUTTONELEMENT** elements that connect the visual buttons on the screen to Windows Media Player actions.</span></span> <span data-ttu-id="22762-116">Questo è il nucleo della pelle ed è possibile considerarlo come un cablaggio della superficie dell'interfaccia alla macchina interna di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="22762-116">This is the core of your skin and you can think of it as wiring the surface of the skin to the inner machinery of Windows Media Player.</span></span>

<span data-ttu-id="22762-117">I **pulsanti** sono contenuti all'interno di un **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="22762-117">**BUTTONELEMENT** s are contained within a **BUTTONGROUP**.</span></span> <span data-ttu-id="22762-118">È necessario disporre sempre di almeno un **pulsanteelement** all'interno di ogni **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="22762-118">You must always have at least one **BUTTONELEMENT** inside each **BUTTONGROUP**.</span></span>

<span data-ttu-id="22762-119">Inserire il codice del **pulsante** di riproduzione dopo la parentesi angolare di chiusura di **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="22762-119">Put the Play **BUTTONELEMENT** code after the closing angle bracket of **BUTTONGROUP**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



<span data-ttu-id="22762-120">Gli attributi seguenti vengono usati per definire il **pulsante ButtonElement** per il pulsante Play:</span><span class="sxs-lookup"><span data-stu-id="22762-120">The following attributes are used to define the **BUTTONELEMENT** for the Play button:</span></span>

<span data-ttu-id="22762-121">**mappingColor**</span><span class="sxs-lookup"><span data-stu-id="22762-121">**mappingColor**</span></span>

<span data-ttu-id="22762-122">Si tratta del valore del colore di un'area nel file di grafica di mapping creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="22762-122">This is the color value of a region in the mapping art file you created before.</span></span> <span data-ttu-id="22762-123">In questo caso si tratta del colore verde tinta unita.</span><span class="sxs-lookup"><span data-stu-id="22762-123">In this case it is the solid green color.</span></span> <span data-ttu-id="22762-124">Questo attributo è obbligatorio per qualsiasi **pulsanteelement**.</span><span class="sxs-lookup"><span data-stu-id="22762-124">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="22762-125">Definendo questo colore, si indica a Windows Media Player di associare questa area dei colori al codice XML di questo pulsante.</span><span class="sxs-lookup"><span data-stu-id="22762-125">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="22762-126">**Descrizione comando**</span><span class="sxs-lookup"><span data-stu-id="22762-126">**upToolTip**</span></span>

<span data-ttu-id="22762-127">Definisce il testo che verrà visualizzato se l'utente posiziona il puntatore del mouse sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="22762-127">This defines the text that will be displayed if the user hovers the mouse over the button.</span></span> <span data-ttu-id="22762-128">Non confondere questo oggetto con l'Art hover che verrà visualizzato.</span><span class="sxs-lookup"><span data-stu-id="22762-128">Do not confuse this with the hover art that will be displayed.</span></span> <span data-ttu-id="22762-129">Una descrizione comando è una piccola didascalia a fumetti che richiede un istante per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="22762-129">A ToolTip is a small balloon caption that takes a moment to appear.</span></span> <span data-ttu-id="22762-130">L'immagine del passaggio del mouse, tuttavia, verrà visualizzata immediatamente in base al colore e alla forma scelti.</span><span class="sxs-lookup"><span data-stu-id="22762-130">The hover art image, however, will appear instantly in whatever color and shape you choose.</span></span>

<span data-ttu-id="22762-131">**onClick**</span><span class="sxs-lookup"><span data-stu-id="22762-131">**onClick**</span></span>

<span data-ttu-id="22762-132">Definisce l'evento che si verifica quando si fa clic con il mouse sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="22762-132">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="22762-133">Il valore di questo attributo evento è denominato gestore eventi e sarà una riga di codice Microsoft JScript o una funzione JScript in un file di testo esterno caricato dall'attributo **loadScript** di una **vista**.</span><span class="sxs-lookup"><span data-stu-id="22762-133">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="22762-134">In questo caso, il codice JScript chiama il metodo **URL** di Windows Media Player, che carica e avvia la riproduzione di un file denominato "Laure. WMA".</span><span class="sxs-lookup"><span data-stu-id="22762-134">In this case, the JScript code calls the **URL** method of Windows Media Player, which loads and starts playing a file named "laure.wma".</span></span> <span data-ttu-id="22762-135">Si noti che la riga termina con un punto e virgola all'interno delle virgolette, che è un'ottima pratica del codice JScript.</span><span class="sxs-lookup"><span data-stu-id="22762-135">Note that the line ends with a semicolon inside the quotes, which is good JScript coding practice.</span></span> <span data-ttu-id="22762-136">Si noti anche l'uso delle virgolette singole all'interno delle virgolette doppie per impostare il nome del file.</span><span class="sxs-lookup"><span data-stu-id="22762-136">Note also the use of single quotes inside the double quotes to set off the file name.</span></span> <span data-ttu-id="22762-137">Per ulteriori informazioni su JScript, vedere [utilizzo di JScript](using-jscript.md) nella sezione about Skins di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="22762-137">For more information about JScript, see [Using JScript](using-jscript.md) in the About Skins section of this SDK.</span></span>

<span data-ttu-id="22762-138">Si noti che non è presente alcun tag **ButtonElement** finale.</span><span class="sxs-lookup"><span data-stu-id="22762-138">Notice that there is no ending **BUTTONELEMENT** tag.</span></span> <span data-ttu-id="22762-139">Se un elemento non racchiude un altro elemento, è possibile chiuderlo con la barra immediatamente prima della parentesi angolare di chiusura.</span><span class="sxs-lookup"><span data-stu-id="22762-139">If an element does not enclose another element, you can close it off with the forward slash just before the closing angle bracket.</span></span> <span data-ttu-id="22762-140">Ciò indica a XML che l'elemento è terminato.</span><span class="sxs-lookup"><span data-stu-id="22762-140">This tells XML that you are finished with that element.</span></span> <span data-ttu-id="22762-141">Ad esempio,</span><span class="sxs-lookup"><span data-stu-id="22762-141">For example,</span></span>


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



<span data-ttu-id="22762-142">e</span><span class="sxs-lookup"><span data-stu-id="22762-142">and</span></span>


```C++
<BUTTONELEMENT/>
```



<span data-ttu-id="22762-143">fornire le stesse informazioni in XML.</span><span class="sxs-lookup"><span data-stu-id="22762-143">convey the same information in XML.</span></span>

<span data-ttu-id="22762-144">La potenza delle interfacce deriva dall'uso dei gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="22762-144">The power of skins comes from using event handlers.</span></span> <span data-ttu-id="22762-145">Se l'utente esegue un'operazione con il mouse, è possibile gestire l'evento con JScript.</span><span class="sxs-lookup"><span data-stu-id="22762-145">If the user does something with a mouse, you can handle that event with JScript.</span></span> <span data-ttu-id="22762-146">Il codice può essere costituito da una singola riga che consente a Windows Media Player di eseguire operazioni semplici come la riproduzione o un'applicazione completa scritta in JScript.</span><span class="sxs-lookup"><span data-stu-id="22762-146">Your code can be a single line that makes Windows Media Player do something simple like play, or it can be a complete application written in JScript.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22762-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22762-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22762-148">**Creazione del file di definizione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="22762-148">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




