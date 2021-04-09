---
title: Inizia con tema e visualizzazione
description: Inizia con tema e visualizzazione
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- creazione di interfacce, elemento THEME
- Windows Media Player Skin, elemento THEME
- Skin, elemento THEME
- file di definizione dell'interfaccia, elemento del tema
- Elemento THEME
- creazione di interfacce, visualizzazione di elementi
- Interfacce Media Player di Windows, elemento di visualizzazione
- Skin, elemento VIEW
- file di definizione dell'interfaccia, elemento di visualizzazione
- Elemento VIEW
- elementi, visualizzazione
- elementi, tema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499444ee2093e743f58174797794a50fbf74555a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856826"
---
# <a name="start-with-theme-and-view"></a><span data-ttu-id="fb43c-115">Inizia con tema e visualizzazione</span><span class="sxs-lookup"><span data-stu-id="fb43c-115">Start with THEME and VIEW</span></span>

<span data-ttu-id="fb43c-116">Ogni interfaccia deve avere esattamente un elemento del **tema** e almeno un elemento di **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="fb43c-116">Every skin must have exactly one **THEME** element and at least one **VIEW** element.</span></span>

<span data-ttu-id="fb43c-117">Usando l'editor di testo, creare il testo seguente:</span><span class="sxs-lookup"><span data-stu-id="fb43c-117">Using your text editor, create the following text:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



<span data-ttu-id="fb43c-118">Lasciare alcune righe vuote prima del tag della **visualizzazione** di chiusura perché verrà aggiunto altro codice in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="fb43c-118">Leave some blank lines before the closing **VIEW** tag because you'll be adding more code here later.</span></span>

<span data-ttu-id="fb43c-119">Salvare il file con un nome di file desiderato, ma assicurarsi che l'estensione sia. WMS.</span><span class="sxs-lookup"><span data-stu-id="fb43c-119">Save your file with any file name you wish, but be sure that the extension is .wms.</span></span> <span data-ttu-id="fb43c-120">Ad esempio, un nome di file tipico potrebbe essere skinone. WMS.</span><span class="sxs-lookup"><span data-stu-id="fb43c-120">For example, a typical file name might be skinone.wms.</span></span>

<span data-ttu-id="fb43c-121">Ogni interfaccia deve iniziare con <THEME> e terminare con </THEME>.</span><span class="sxs-lookup"><span data-stu-id="fb43c-121">Every skin must start with <THEME> and end with </THEME>.</span></span> <span data-ttu-id="fb43c-122">È possibile avere un solo elemento del **tema** nell'interfaccia, ma è necessario disporre di uno.</span><span class="sxs-lookup"><span data-stu-id="fb43c-122">You can only have one **THEME** element in your skin, but you must have one.</span></span>

<span data-ttu-id="fb43c-123">È inoltre necessario disporre di almeno un elemento di **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="fb43c-123">You must also have at least one **VIEW** element.</span></span> <span data-ttu-id="fb43c-124">È possibile avere più di una **vista**, ma in questo esempio ne è presente solo una.</span><span class="sxs-lookup"><span data-stu-id="fb43c-124">You can have more than one **VIEW**, but this example only has one.</span></span> <span data-ttu-id="fb43c-125">È necessario avere un'apertura <VIEW> e una chiusura <VIEW>. Si noti che il </VIEW> tag di apertura non chiude immediatamente il tag, ma include diversi attributi prima della parentesi angolare di chiusura (>).</span><span class="sxs-lookup"><span data-stu-id="fb43c-125">You must have an opening <VIEW> and a closing <VIEW>. Notice that the opening </VIEW> tag does not close the tag right away, but includes several attributes before the closing angle bracket (>).</span></span> <span data-ttu-id="fb43c-126">Gli attributi seguenti vengono usati nell'elemento **Theme** in questo esempio:</span><span class="sxs-lookup"><span data-stu-id="fb43c-126">The following attributes are used in the **THEME** element in this example:</span></span>

<span data-ttu-id="fb43c-127">**clippingColor**</span><span class="sxs-lookup"><span data-stu-id="fb43c-127">**clippingColor**</span></span>

<span data-ttu-id="fb43c-128">L'attributo **clippingColor** non sarà sempre necessario se i bordi dell'interfaccia sono rettangolari.</span><span class="sxs-lookup"><span data-stu-id="fb43c-128">You will not always need the **clippingColor** attribute if the edges of your skin are rectangular.</span></span> <span data-ttu-id="fb43c-129">L'interfaccia in questo esempio è a forma ovale, quindi è necessario un colore di ritaglio per le parti dell'interfaccia da visualizzare sul desktop; essenzialmente tutte le parti al di fuori dell'Oval.</span><span class="sxs-lookup"><span data-stu-id="fb43c-129">The skin in this example is oval-shaped, so you need a clipping color for the parts of the skin that you want to see the desktop through; essentially all parts outside the oval.</span></span> <span data-ttu-id="fb43c-130">In questo esempio di interfaccia, verrà usato un colore giallo scuro, specificato come " \# CCCC00" nel formato Web.</span><span class="sxs-lookup"><span data-stu-id="fb43c-130">In this example skin, we will use a dark yellow, specified as "\#CCCC00" in Web format.</span></span> <span data-ttu-id="fb43c-131">I motivi di questa scelta sono forniti nella [creazione del file](creating-the-primary-art-file.md)di immagine principale.</span><span class="sxs-lookup"><span data-stu-id="fb43c-131">The reasons for this choice are given in [Creating the Primary Art File](creating-the-primary-art-file.md).</span></span> <span data-ttu-id="fb43c-132">In sostanza, questo valore sarà sempre un numero ottenuto dal programma di grafica.</span><span class="sxs-lookup"><span data-stu-id="fb43c-132">Essentially, this value will always be a number that you get from your art program.</span></span>

<span data-ttu-id="fb43c-133">**backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="fb43c-133">**backgroundImage**</span></span>

<span data-ttu-id="fb43c-134">Si tratta del nome del file di immagine principale.</span><span class="sxs-lookup"><span data-stu-id="fb43c-134">This is the name of the primary art file.</span></span> <span data-ttu-id="fb43c-135">Deve corrispondere esattamente al nome file e al percorso del file di immagine principale.</span><span class="sxs-lookup"><span data-stu-id="fb43c-135">It should be the exact file name and path of your primary art file.</span></span> <span data-ttu-id="fb43c-136">Sono supportati solo i file BMP, JPG, GIF e PNG ed è consigliabile usare BMP.</span><span class="sxs-lookup"><span data-stu-id="fb43c-136">Only BMP, JPG, GIF, and PNG files are supported, and BMP is recommended.</span></span>

<span data-ttu-id="fb43c-137">**titleBar**</span><span class="sxs-lookup"><span data-stu-id="fb43c-137">**titleBar**</span></span>

<span data-ttu-id="fb43c-138">Questa interfaccia non ha una **barra** del titolo, quindi il valore sarà "false".</span><span class="sxs-lookup"><span data-stu-id="fb43c-138">This skin does not have a **titleBar**, so the value will be "false".</span></span> <span data-ttu-id="fb43c-139">Si vuole una barra del titolo solo se si vuole che l'interfaccia abbia un colore di sfondo e sia rettangolare.</span><span class="sxs-lookup"><span data-stu-id="fb43c-139">You will only want a title bar if you want your skin to have a background color and be rectangular.</span></span>

<span data-ttu-id="fb43c-140">Assicurarsi di inserire la parentesi angolare di chiusura (>) dopo il valore della **barra** del titolo per indicare che è stata terminata la definizione della **visualizzazione**.</span><span class="sxs-lookup"><span data-stu-id="fb43c-140">Be sure that you put the closing angle bracket (>) after the **titleBar** value to indicate that you are finished defining the **VIEW**.</span></span> <span data-ttu-id="fb43c-141">Lasciare alcune righe vuote prima della **visualizzazione** di chiusura e dei tag del **tema** .</span><span class="sxs-lookup"><span data-stu-id="fb43c-141">Leave a few blank lines before the closing **VIEW** and **THEME** tags.</span></span> <span data-ttu-id="fb43c-142">Sono necessarie le righe per il codice che si aggiungerà in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="fb43c-142">You will need the lines for code that you will add later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb43c-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fb43c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb43c-144">**Creazione del file di definizione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="fb43c-144">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




