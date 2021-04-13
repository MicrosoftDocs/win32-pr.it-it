---
title: Controlli di selezione
description: Con un controllo di selezione, gli utenti possono fare clic sui pulsanti freccia per modificare il valore in modo incrementale all'interno della casella di testo numerica associata.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 54ce622983e52d65fa58ef05aca783ff67ebce66
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351101"
---
# <a name="spin-controls"></a><span data-ttu-id="f23d1-103">Controlli di selezione</span><span class="sxs-lookup"><span data-stu-id="f23d1-103">Spin Controls</span></span>

> [!NOTE]
> <span data-ttu-id="f23d1-104">Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="f23d1-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="f23d1-105">Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="f23d1-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="f23d1-106">Con un controllo di selezione, gli utenti possono fare clic sui pulsanti freccia per modificare il valore in modo incrementale all'interno della [casella di testo numerica](ctrl-text-boxes.md)associata.</span><span class="sxs-lookup"><span data-stu-id="f23d1-106">With a spin control, users can click arrow buttons to change incrementally the value within its associated [numeric text box](ctrl-text-boxes.md).</span></span> <span data-ttu-id="f23d1-107">Il termine casella di selezione si riferisce alla combinazione di una casella di testo e del controllo di selezione associato.</span><span class="sxs-lookup"><span data-stu-id="f23d1-107">The term spin box refers to the combination of a text box and its associated spin control.</span></span>

![<span data-ttu-id="f23d1-108">screenshot del controllo di selezione e della casella di testo</span><span class="sxs-lookup"><span data-stu-id="f23d1-108">screen shot of spin control and text box</span></span> ](images/ctrl-spin-controls-image1.png)

<span data-ttu-id="f23d1-109">Casella di selezione tipica.</span><span class="sxs-lookup"><span data-stu-id="f23d1-109">A typical spin box.</span></span>

<span data-ttu-id="f23d1-110">Spesso gli utenti preferiscono i controlli spin, perché possono apportare modifiche senza trasferire le mani dal mouse.</span><span class="sxs-lookup"><span data-stu-id="f23d1-110">Users often prefer spin controls because they can make changes without moving their hands from the mouse.</span></span> <span data-ttu-id="f23d1-111">Quando il controllo di selezione è associato a una casella di testo, gli utenti possono digitare o incollare input direttamente nella casella di testo, in modo che l'uso del controllo di selezione sia facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f23d1-111">When the spin control is paired with a text box, users can type or paste input directly in the text box, so use of the spin control is optional.</span></span>

<span data-ttu-id="f23d1-112">Mentre i controlli di selezione vengono usati per l'input numerico, l'input non deve essere un numero intero puro.</span><span class="sxs-lookup"><span data-stu-id="f23d1-112">While spin controls are used for numeric input, the input doesn't have to be a pure whole number.</span></span> <span data-ttu-id="f23d1-113">L'input può essere costituito da numeri decimali e può presentare segni negativi, delimitatori (ad esempio, due punti o trattini) e modificatori di unità.</span><span class="sxs-lookup"><span data-stu-id="f23d1-113">The input can be decimal numbers and it can have negative signs, delimiters (such as colons or hyphens), and unit modifiers.</span></span>

> [!Note]  
> <span data-ttu-id="f23d1-114">Le linee guida correlate alle [caselle di testo](ctrl-text-boxes.md) e al [layout](vis-layout.md) sono presentate in articoli distinti.</span><span class="sxs-lookup"><span data-stu-id="f23d1-114">Guidelines related to [text boxes](ctrl-text-boxes.md) and [layout](vis-layout.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="f23d1-115">È il controllo giusto?</span><span class="sxs-lookup"><span data-stu-id="f23d1-115">Is this the right control?</span></span>

<span data-ttu-id="f23d1-116">Per decidere, prendi in considerazione queste domande:</span><span class="sxs-lookup"><span data-stu-id="f23d1-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="f23d1-117">**Il controllo è utilizzato per l'input numerico?**</span><span class="sxs-lookup"><span data-stu-id="f23d1-117">**Is the control used for numeric input?**</span></span> <span data-ttu-id="f23d1-118">In caso contrario, utilizzare un altro controllo, ad esempio un [elenco a discesa](/windows/desktop/uxguide/ctrl-drop) o un [dispositivo di scorrimento](ctrl-sliders.md), per effettuare una selezione da un set fisso di valori.</span><span class="sxs-lookup"><span data-stu-id="f23d1-118">If not, use another control, such as a [drop-down list](/windows/desktop/uxguide/ctrl-drop) or [slider](ctrl-sliders.md), to select from a fixed set of values.</span></span> <span data-ttu-id="f23d1-119">Utilizzare le barre di scorrimento per lo scorrimento.</span><span class="sxs-lookup"><span data-stu-id="f23d1-119">Use scroll bars for scrolling.</span></span>
-   <span data-ttu-id="f23d1-120">**Gli utenti considerano il valore come una quantità relativa, non un valore numerico?**</span><span class="sxs-lookup"><span data-stu-id="f23d1-120">**Do users think of the value as a relative quantity, not a numeric value?**</span></span> <span data-ttu-id="f23d1-121">In caso affermativo, usare invece un dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="f23d1-121">If so, use a slider instead.</span></span> <span data-ttu-id="f23d1-122">Usare le caselle di selezione solo per i valori numerici esatti e noti.</span><span class="sxs-lookup"><span data-stu-id="f23d1-122">Use spin boxes only for exact, known numeric values.</span></span> <span data-ttu-id="f23d1-123">Ad esempio, gli utenti vogliono impostare il volume audio su basso o medio e non su 2 o 5.</span><span class="sxs-lookup"><span data-stu-id="f23d1-123">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>
-   <span data-ttu-id="f23d1-124">**Il controllo è associato a una casella di testo?**</span><span class="sxs-lookup"><span data-stu-id="f23d1-124">**Is the control paired with a text box?**</span></span> <span data-ttu-id="f23d1-125">In caso contrario, non usare.</span><span class="sxs-lookup"><span data-stu-id="f23d1-125">If not, don't use.</span></span> <span data-ttu-id="f23d1-126">I controlli di selezione non devono essere usati da solo o con altri tipi di controlli oltre a una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="f23d1-126">Spin controls shouldn't be used alone or with other types of controls besides a text box.</span></span>

    <span data-ttu-id="f23d1-127">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="f23d1-127">**Incorrect:**</span></span>

    ![<span data-ttu-id="f23d1-128">screenshot del controllo di selezione, immagine, nessuna casella di testo</span><span class="sxs-lookup"><span data-stu-id="f23d1-128">screen shot of spin control, graphic, no text box</span></span> ](images/ctrl-spin-controls-image2.png)

    <span data-ttu-id="f23d1-129">In questo esempio viene usato un controllo di selezione per controllare un'immagine dinamica.</span><span class="sxs-lookup"><span data-stu-id="f23d1-129">In this example, a spin control is used to control a dynamic graphic.</span></span>

-   <span data-ttu-id="f23d1-130">**Gli intervalli di valori contigui sono validi?**</span><span class="sxs-lookup"><span data-stu-id="f23d1-130">**Are contiguous value ranges valid?**</span></span> <span data-ttu-id="f23d1-131">In caso contrario, usare invece un elenco a discesa di valori validi.</span><span class="sxs-lookup"><span data-stu-id="f23d1-131">If not, use a drop-down list of valid values instead.</span></span>

    ![<span data-ttu-id="f23d1-132">screenshot dell'elenco a discesa</span><span class="sxs-lookup"><span data-stu-id="f23d1-132">screen shot of drop-down list</span></span> ](images/ctrl-spin-controls-image3.png)

    <span data-ttu-id="f23d1-133">In questo esempio, non tutti i numeri di unità disco sono validi, quindi un elenco a discesa rappresenta una scelta migliore.</span><span class="sxs-lookup"><span data-stu-id="f23d1-133">In this example, not all disk drive numbers are valid, so a drop-down list is a better choice.</span></span>

-   <span data-ttu-id="f23d1-134">**È possibile utilizzare il controllo di selezione?**</span><span class="sxs-lookup"><span data-stu-id="f23d1-134">**Is using the spin control practical?**</span></span> <span data-ttu-id="f23d1-135">L'uso di un controllo di selezione è utile per:</span><span class="sxs-lookup"><span data-stu-id="f23d1-135">Using a spin control is practical for:</span></span>

    -   <span data-ttu-id="f23d1-136">Immissione di un numero ridotto, in genere inferiore a 100.</span><span class="sxs-lookup"><span data-stu-id="f23d1-136">Entering a small number, typically under 100.</span></span>
    -   <span data-ttu-id="f23d1-137">Apportare piccole modifiche a un valore predefinito o esistente.</span><span class="sxs-lookup"><span data-stu-id="f23d1-137">Making small changes to an existing or default value.</span></span>

    <span data-ttu-id="f23d1-138">Sebbene i controlli di selezione possano essere usati per qualsiasi input numerico, sono inefficienti in situazioni diverse da queste.</span><span class="sxs-lookup"><span data-stu-id="f23d1-138">While spin controls can be used for any numeric input, they are inefficient in situations other than these.</span></span>

-   <span data-ttu-id="f23d1-139">**Il controllo di selezione è utile?**</span><span class="sxs-lookup"><span data-stu-id="f23d1-139">**Is the spin control helpful?**</span></span> <span data-ttu-id="f23d1-140">Il controllo viene utilizzato in un contesto in cui è probabile che gli utenti utilizzino il mouse?</span><span class="sxs-lookup"><span data-stu-id="f23d1-140">Is the control used in a context where users are likely to be using their mouse?</span></span> <span data-ttu-id="f23d1-141">In caso contrario, prendere in considerazione un controllo di selezione facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f23d1-141">If not, consider a spin control optional.</span></span>
-   <span data-ttu-id="f23d1-142">**Gli elenchi a discesa dei controlli di pari livello?**</span><span class="sxs-lookup"><span data-stu-id="f23d1-142">**Are the sibling controls drop-down lists?**</span></span> <span data-ttu-id="f23d1-143">Se sono presenti altri elenchi a discesa, provare a usare un elenco a discesa per verificarne la coerenza.</span><span class="sxs-lookup"><span data-stu-id="f23d1-143">If there are other drop-down lists, consider using a drop-down list for consistency.</span></span>

    ![<span data-ttu-id="f23d1-144">screenshot della finestra di dialogo con elenchi a discesa</span><span class="sxs-lookup"><span data-stu-id="f23d1-144">screen shot of dialog box with drop-down lists</span></span> ](images/ctrl-spin-controls-image4.png)

    <span data-ttu-id="f23d1-145">In questo esempio è possibile usare una casella di selezione, ma per coerenza viene usato un elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="f23d1-145">In this example, a spin box could be used, but a drop-down list is used for consistency.</span></span>

-   <span data-ttu-id="f23d1-146">**Gli utenti di touch o Pen sono una destinazione primaria?**</span><span class="sxs-lookup"><span data-stu-id="f23d1-146">**Are touch or pen users a primary target?**</span></span> <span data-ttu-id="f23d1-147">In tal caso, prendere in considerazione l'uso di un elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="f23d1-147">If so, consider using a drop-down list instead.</span></span> <span data-ttu-id="f23d1-148">I pulsanti freccia in un controllo di selezione sono troppo piccoli per essere usati in modo efficiente con il tocco o con una penna.</span><span class="sxs-lookup"><span data-stu-id="f23d1-148">The arrow buttons in a spin control are too small to be used efficiently with touch or a pen.</span></span>

<span data-ttu-id="f23d1-149">Se è possibile un dispositivo di scorrimento o una casella di selezione, utilizzare una casella di selezione se:</span><span class="sxs-lookup"><span data-stu-id="f23d1-149">If a slider or a spin box is possible, use a spin box if:</span></span>

-   <span data-ttu-id="f23d1-150">Lo spazio sullo schermo è limitato.</span><span class="sxs-lookup"><span data-stu-id="f23d1-150">Screen space is tight.</span></span>
-   <span data-ttu-id="f23d1-151">È probabile che un utente preferisca utilizzare la tastiera.</span><span class="sxs-lookup"><span data-stu-id="f23d1-151">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="f23d1-152">Usa un dispositivo di scorrimento se:</span><span class="sxs-lookup"><span data-stu-id="f23d1-152">Use a slider if:</span></span>

-   <span data-ttu-id="f23d1-153">Gli utenti trarranno vantaggio da un riscontro immediato.</span><span class="sxs-lookup"><span data-stu-id="f23d1-153">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="f23d1-154">Indicazioni</span><span class="sxs-lookup"><span data-stu-id="f23d1-154">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="f23d1-155">Generale</span><span class="sxs-lookup"><span data-stu-id="f23d1-155">General</span></span>

-   <span data-ttu-id="f23d1-156">**Usare i controlli di selezione ogni volta che sono pratici e utili.**</span><span class="sxs-lookup"><span data-stu-id="f23d1-156">**Use spin controls whenever they are practical and helpful.**</span></span> <span data-ttu-id="f23d1-157">Vedere qual [è il controllo corretto?](#is-this-the-right-control)</span><span class="sxs-lookup"><span data-stu-id="f23d1-157">See [Is this the right control?](#is-this-the-right-control)</span></span>

    -   <span data-ttu-id="f23d1-158">**Eccezione:** Per coerenza con altre caselle di testo nella stessa interfaccia utente, usare i controlli di selezione anche se non sono sempre pratici.</span><span class="sxs-lookup"><span data-stu-id="f23d1-158">**Exception:** To be consistent with other text boxes on the same user interface (UI), use spin controls even if they aren't always practical.</span></span>

    <span data-ttu-id="f23d1-159">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="f23d1-159">**Correct:**</span></span>

    ![<span data-ttu-id="f23d1-160">screenshot dei controlli di selezione mese, giorno e anno</span><span class="sxs-lookup"><span data-stu-id="f23d1-160">screen shot of month, day, year spin controls</span></span> ](images/ctrl-spin-controls-image5.png)

    <span data-ttu-id="f23d1-161">In questo esempio viene usato un controllo di selezione con il controllo Year per la coerenza, anche se non è sempre pratico.</span><span class="sxs-lookup"><span data-stu-id="f23d1-161">In this example, a spin control is used with the year control for consistency, even though it isn't always practical.</span></span>

    <span data-ttu-id="f23d1-162">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="f23d1-162">**Incorrect:**</span></span>

    ![<span data-ttu-id="f23d1-163">screenshot del controllo di selezione degli indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="f23d1-163">screen shot of ip address spin control</span></span> ](images/ctrl-spin-controls-image6.png)

    <span data-ttu-id="f23d1-164">In questo esempio, il controllo di selezione è inutilizzabile.</span><span class="sxs-lookup"><span data-stu-id="f23d1-164">In this example, the spin control is unusable.</span></span>

-   <span data-ttu-id="f23d1-165">**Creare sempre un controllo di rotazione per "Buddy" della casella di testo.**</span><span class="sxs-lookup"><span data-stu-id="f23d1-165">**Always make a spin control the "buddy" of the text box.**</span></span> <span data-ttu-id="f23d1-166">Questa operazione posiziona il controllo di selezione all'interno della casella di testo.</span><span class="sxs-lookup"><span data-stu-id="f23d1-166">Doing so places the spin control inside the text box.</span></span>

    <span data-ttu-id="f23d1-167">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="f23d1-167">**Correct:**</span></span>

    ![<span data-ttu-id="f23d1-168">screenshot del controllo di selezione inserito nella casella di testo</span><span class="sxs-lookup"><span data-stu-id="f23d1-168">screen shot of spin control placed inside text box</span></span> ](images/ctrl-spin-controls-image7.png)

    <span data-ttu-id="f23d1-169">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="f23d1-169">**Incorrect:**</span></span>

    ![<span data-ttu-id="f23d1-170">cattura di schermata del controllo di selezione inserito all'esterno della casella di testo</span><span class="sxs-lookup"><span data-stu-id="f23d1-170">screen shot of spin control placed outside text box</span></span> ](images/ctrl-spin-controls-image8.png)

    <span data-ttu-id="f23d1-171">Nell'esempio corretto, il controllo di selezione viene inserito all'interno della casella di testo associata.</span><span class="sxs-lookup"><span data-stu-id="f23d1-171">In the correct example, the spin control is placed inside its associated text box.</span></span>

-   <span data-ttu-id="f23d1-172">**Disabilitare un controllo di selezione quando la casella di testo associata è disabilitata.**</span><span class="sxs-lookup"><span data-stu-id="f23d1-172">**Disable a spin control when its associated text box is disabled.**</span></span> <span data-ttu-id="f23d1-173">Il controllo di selezione è un metodo di input supplementare, mai l'unico metodo di input.</span><span class="sxs-lookup"><span data-stu-id="f23d1-173">The spin control is a supplemental input method—never the only input method.</span></span>

### <a name="values"></a><span data-ttu-id="f23d1-174">Valori</span><span class="sxs-lookup"><span data-stu-id="f23d1-174">Values</span></span>

-   <span data-ttu-id="f23d1-175">**Definire il pulsante superiore per aumentare il valore di un'unità e il pulsante inferiore per ridurla di un'unità.**</span><span class="sxs-lookup"><span data-stu-id="f23d1-175">**Define the top button to increase the value by one unit and the bottom button to decrease by one unit.**</span></span> <span data-ttu-id="f23d1-176">In genere, l'unità è uno, ma deve essere la più piccola modifica comune nel valore.</span><span class="sxs-lookup"><span data-stu-id="f23d1-176">Typically, the unit is one, but it should be the smallest common change in value.</span></span> <span data-ttu-id="f23d1-177">Idealmente, il controllo di selezione dovrebbe coprire tutti i valori validi e dovrebbe essere più pratico rispetto alla digitazione del testo.</span><span class="sxs-lookup"><span data-stu-id="f23d1-177">Ideally, the spin control should cover all valid values, and it should be more convenient than typing in the text.</span></span>

    ![<span data-ttu-id="f23d1-178">screenshot del controllo di selezione dei margini</span><span class="sxs-lookup"><span data-stu-id="f23d1-178">screen shot of 'margins' spin control</span></span> ](images/ctrl-spin-controls-image9.png)

    <span data-ttu-id="f23d1-179">In questo esempio, se si fa clic su un controllo di selezione, i valori vengono modificati in base a 1, che è la più piccola modifica comune nel valore.</span><span class="sxs-lookup"><span data-stu-id="f23d1-179">In this example, clicking a spin control changes the values by .1, which is the smallest common change in value.</span></span> <span data-ttu-id="f23d1-180">L'uso di un'unità di dimensioni inferiori coprirebbe l'intervallo di valori validi, ma renderebbe inutilizzabili i controlli di rotazione.</span><span class="sxs-lookup"><span data-stu-id="f23d1-180">Using a smaller unit would cover the range of valid values but make the spin controls unusable.</span></span>

-   <span data-ttu-id="f23d1-181">**Usare il controllo di selezione per limitare l'input ai valori validi.**</span><span class="sxs-lookup"><span data-stu-id="f23d1-181">**Use the spin control to limit input to valid values.**</span></span> <span data-ttu-id="f23d1-182">L'uso di un controllo di selezione non dovrebbe mai produrre un valore non corretto.</span><span class="sxs-lookup"><span data-stu-id="f23d1-182">Using a spin control should never result in an incorrect value.</span></span>
-   <span data-ttu-id="f23d1-183">**Alla fine di un intervallo di valori validi, riavviare l'intervallo.**</span><span class="sxs-lookup"><span data-stu-id="f23d1-183">**At the end of a range of valid values, restart the range.**</span></span> <span data-ttu-id="f23d1-184">La metafora del controllo spin è che l'utente sta ruotando una rotellina di valori, quindi questo comportamento simile alla rotellina.</span><span class="sxs-lookup"><span data-stu-id="f23d1-184">The spin control metaphor is that the user is spinning a wheel of values, hence this wheel-like behavior.</span></span>
    -   <span data-ttu-id="f23d1-185">**Eccezione:** Non riavviare l'intervallo se il valore risultante è certo che non è corretto.</span><span class="sxs-lookup"><span data-stu-id="f23d1-185">**Exception:** Don't restart the range if the resulting value is certain to be incorrect.</span></span>

        ![<span data-ttu-id="f23d1-186">screenshot del controllo di selezione ' numero di copie '</span><span class="sxs-lookup"><span data-stu-id="f23d1-186">screen shot of 'number of copies' spin control</span></span> ](images/ctrl-spin-controls-image10.png)

        <span data-ttu-id="f23d1-187">In questo esempio, facendo clic sul pulsante freccia giù non viene riavviato l'intervallo (passando al valore massimo), perché tale valore è certo che non è corretto.</span><span class="sxs-lookup"><span data-stu-id="f23d1-187">In this example, clicking the down arrow button doesn't restart the range (by going to the maximum value) because that value is certain to be incorrect.</span></span>

-   <span data-ttu-id="f23d1-188">**Usare il testo anziché i valori numerici speciali.**</span><span class="sxs-lookup"><span data-stu-id="f23d1-188">**Use text instead of special numeric values.**</span></span> <span data-ttu-id="f23d1-189">Consentire agli utenti di passare a questi valori speciali invece di conoscerli e digitarli.</span><span class="sxs-lookup"><span data-stu-id="f23d1-189">Allow users to spin to these special values instead of having to know them and type them in.</span></span>

    ![<span data-ttu-id="f23d1-190">screenshot del controllo di selezione ' sospensione dopo (mai)'</span><span class="sxs-lookup"><span data-stu-id="f23d1-190">screen shot of 'sleep after (never)' spin control</span></span> ](images/ctrl-spin-controls-image11.png)

    <span data-ttu-id="f23d1-191">In questo esempio, non è mai un valore speciale, ma gli utenti possono eseguire la rotazione.</span><span class="sxs-lookup"><span data-stu-id="f23d1-191">In this example, Never is a special value but users can spin to it.</span></span>

-   <span data-ttu-id="f23d1-192">**Se il valore contiene delimitatori, nella casella di testo associata devono essere presenti più punti di interesse per l'input.**</span><span class="sxs-lookup"><span data-stu-id="f23d1-192">**If the value has delimiters, the associated text box should have multiple input focus points.**</span></span> <span data-ttu-id="f23d1-193">In questo modo è possibile modificare i segmenti numerici singolarmente.</span><span class="sxs-lookup"><span data-stu-id="f23d1-193">Doing so allows the numeric segments to be manipulated individually.</span></span>

    ![<span data-ttu-id="f23d1-194">cattura di schermata del controllo di selezione ora, minuti selezionati</span><span class="sxs-lookup"><span data-stu-id="f23d1-194">screen shot of time spin control, minutes selected</span></span> ](images/ctrl-spin-controls-image12.png)

    <span data-ttu-id="f23d1-195">In questo esempio, il controllo di selezione influiscono sui valori per hours, minutes, seconds e A.M./P.M., a seconda di quale sia lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="f23d1-195">In this example, the spin control affects the values for hours, minutes, seconds, and A.M./P.M.—whichever has the focus.</span></span>

-   <span data-ttu-id="f23d1-196">**Se il valore è costituito da unità, usare il controllo di selezione per modificare anche tali unità.**</span><span class="sxs-lookup"><span data-stu-id="f23d1-196">**If the value has units, use the spin control to change those units as well.**</span></span>

    ![<span data-ttu-id="f23d1-197">cattura di schermata del controllo di selezione ora,' a.m.'</span><span class="sxs-lookup"><span data-stu-id="f23d1-197">screen shot of time spin control, 'a.m.'</span></span> <span data-ttu-id="f23d1-198">selezionato</span><span class="sxs-lookup"><span data-stu-id="f23d1-198">selected</span></span> ](images/ctrl-spin-controls-image13.png)

    <span data-ttu-id="f23d1-199">In questo esempio, il controllo di selezione può essere usato per modificare le unità.</span><span class="sxs-lookup"><span data-stu-id="f23d1-199">In this example, the spin control can be used to change units.</span></span>

## <a name="labels"></a><span data-ttu-id="f23d1-200">Etichette</span><span class="sxs-lookup"><span data-stu-id="f23d1-200">Labels</span></span>

-   <span data-ttu-id="f23d1-201">Applicare le linee guida per l' [etichettatura della casella di testo](ctrl-text-boxes.md) per etichettare la casella di testo associata.</span><span class="sxs-lookup"><span data-stu-id="f23d1-201">Apply the [text box labeling](ctrl-text-boxes.md) guidelines to label the associated text box.</span></span> <span data-ttu-id="f23d1-202">I controlli di selezione non vengono mai etichettati direttamente.</span><span class="sxs-lookup"><span data-stu-id="f23d1-202">Spin controls are never labeled directly.</span></span>

## <a name="documentation"></a><span data-ttu-id="f23d1-203">Documentazione</span><span class="sxs-lookup"><span data-stu-id="f23d1-203">Documentation</span></span>

<span data-ttu-id="f23d1-204">Quando si fa riferimento ai controlli di selezione:</span><span class="sxs-lookup"><span data-stu-id="f23d1-204">When referring to spin controls:</span></span>

-   <span data-ttu-id="f23d1-205">Non fare riferimento ai controlli di selezione nella documentazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f23d1-205">Don't refer to spin controls in user documentation.</span></span> <span data-ttu-id="f23d1-206">Al contrario, fare riferimento all'etichetta della casella di testo associata.</span><span class="sxs-lookup"><span data-stu-id="f23d1-206">Instead, refer to the label of the associated text box.</span></span>
-   <span data-ttu-id="f23d1-207">Vedere controlli di selezione e caselle di selezione solo nella programmazione e in altri documenti tecnici.</span><span class="sxs-lookup"><span data-stu-id="f23d1-207">Refer to spin controls and spin boxes only in programming and other technical documentation.</span></span>

<span data-ttu-id="f23d1-208">Esempio: nella casella **Data** Digitare o selezionare la parte della data che si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="f23d1-208">Example: In the **Date** box, type or select the part of the date you want to change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f23d1-209">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f23d1-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f23d1-210">Glossario</span><span class="sxs-lookup"><span data-stu-id="f23d1-210">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 