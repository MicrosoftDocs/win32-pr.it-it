---
title: Dispositivi di scorrimento (nozioni di base sulla progettazione)
description: Con un dispositivo di scorrimento, gli utenti possono scegliere tra un intervallo continuo di valori.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ff9791ab49c338e4c11e014a3e996771571add9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104555191"
---
# <a name="sliders-design-basics"></a><span data-ttu-id="cfd28-103">Dispositivi di scorrimento (nozioni di base sulla progettazione)</span><span class="sxs-lookup"><span data-stu-id="cfd28-103">Sliders (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="cfd28-104">Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="cfd28-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="cfd28-105">Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="cfd28-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="cfd28-106">Con un dispositivo di scorrimento, gli utenti possono scegliere tra un intervallo continuo di valori.</span><span class="sxs-lookup"><span data-stu-id="cfd28-106">With a slider, users can choose from a continuous range of values.</span></span> <span data-ttu-id="cfd28-107">Un dispositivo di scorrimento ha una barra che mostra l'intervallo e un indicatore che mostra il valore corrente.</span><span class="sxs-lookup"><span data-stu-id="cfd28-107">A slider has a bar that shows the range and an indicator that shows the current value.</span></span> <span data-ttu-id="cfd28-108">I segni di graduazione facoltativi mostrano i valori.</span><span class="sxs-lookup"><span data-stu-id="cfd28-108">Optional tick marks show values.</span></span>

![<span data-ttu-id="cfd28-109">figura che Mostra barra, dispositivo di scorrimento e segni di graduazione</span><span class="sxs-lookup"><span data-stu-id="cfd28-109">figure showing bar, slider, and tick marks</span></span> ](images/ctrl-sliders-image1.png)

<span data-ttu-id="cfd28-110">Un dispositivo di scorrimento tipico.</span><span class="sxs-lookup"><span data-stu-id="cfd28-110">A typical slider.</span></span>

> [!Note]  
> <span data-ttu-id="cfd28-111">Le linee guida correlate al [layout](vis-layout.md) sono presentate in un articolo separato.</span><span class="sxs-lookup"><span data-stu-id="cfd28-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="cfd28-112">È il controllo giusto?</span><span class="sxs-lookup"><span data-stu-id="cfd28-112">Is this the right control?</span></span>

<span data-ttu-id="cfd28-113">Utilizzare un dispositivo di scorrimento quando si desidera che gli utenti siano in grado di **impostare valori contigui definiti, ad esempio volume o luminosità, oppure un intervallo di valori discreti, ad esempio le impostazioni di risoluzione dello schermo.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-113">Use a slider when you want your users to be able to **set defined, contiguous values (such as volume or brightness) or a range of discrete values (such as screen resolution settings).**</span></span>

<span data-ttu-id="cfd28-114">Un dispositivo di scorrimento è una buona scelta quando sai che gli utenti considerano il valore una quantità relativa e non un valore numerico.</span><span class="sxs-lookup"><span data-stu-id="cfd28-114">A slider is a good choice when you know that users think of the value as a relative quantity, not a numeric value.</span></span> <span data-ttu-id="cfd28-115">Ad esempio, gli utenti vogliono impostare il volume audio su basso o medio e non su 2 o 5.</span><span class="sxs-lookup"><span data-stu-id="cfd28-115">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>

<span data-ttu-id="cfd28-116">Per decidere, prendi in considerazione queste domande:</span><span class="sxs-lookup"><span data-stu-id="cfd28-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="cfd28-117">**L'impostazione sembra una quantità relativa?**</span><span class="sxs-lookup"><span data-stu-id="cfd28-117">**Does the setting seem like a relative quantity?**</span></span> <span data-ttu-id="cfd28-118">In caso contrario, utilizzare [pulsanti di opzione](ctrl-radio-buttons.md)o un elenco a [discesa](/windows/desktop/uxguide/ctrl-drop) o a [selezione singola](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="cfd28-118">If not, use [radio buttons](ctrl-radio-buttons.md), or a [drop-down](/windows/desktop/uxguide/ctrl-drop) or [single-selection list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="cfd28-119">**L'impostazione è un valore numerico noto esatto?**</span><span class="sxs-lookup"><span data-stu-id="cfd28-119">**Is the setting an exact, known numeric value?**</span></span> <span data-ttu-id="cfd28-120">In tal caso, utilizzare una [casella di testo numerica](ctrl-text-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="cfd28-120">If so, use a [numeric text boxes](ctrl-text-boxes.md).</span></span>
-   <span data-ttu-id="cfd28-121">**Un utente trarrebbe vantaggio da un riscontro immediato sull'effetto delle modifiche dell'impostazione?**</span><span class="sxs-lookup"><span data-stu-id="cfd28-121">**Would a user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="cfd28-122">Se sì, usa un dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="cfd28-122">If so, use a slider.</span></span> <span data-ttu-id="cfd28-123">Gli utenti possono ad esempio scegliere più facilmente un colore esaminando immediatamente l'effetto delle modifiche dei valori di tonalità, saturazione o luminosità.</span><span class="sxs-lookup"><span data-stu-id="cfd28-123">For example, users can choose a color more easily by immediately seeing the effect of changes to hue, saturation, or luminosity values.</span></span>
-   <span data-ttu-id="cfd28-124">**L'impostazione ha un intervallo di quattro o più valori?**</span><span class="sxs-lookup"><span data-stu-id="cfd28-124">**Does the setting have a range of four or more values?**</span></span> <span data-ttu-id="cfd28-125">In caso contrario, usa pulsanti di opzione.</span><span class="sxs-lookup"><span data-stu-id="cfd28-125">If not, use radio buttons.</span></span>
-   <span data-ttu-id="cfd28-126">**L'utente può modificare il valore?**</span><span class="sxs-lookup"><span data-stu-id="cfd28-126">**Can the user change the value?**</span></span> <span data-ttu-id="cfd28-127">I dispositivi di scorrimento consentono l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cfd28-127">Sliders are for user interaction.</span></span> <span data-ttu-id="cfd28-128">Se un utente non può modificare il valore, usare invece una casella di [testo](ctrl-text-boxes.md) di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cfd28-128">If a user can't ever change the value, use a read-only [text box](ctrl-text-boxes.md) instead.</span></span>

<span data-ttu-id="cfd28-129">Se è possibile un dispositivo di scorrimento o una casella di testo numerica, utilizzare una casella di testo numerica se:</span><span class="sxs-lookup"><span data-stu-id="cfd28-129">If a slider or a numeric text box is possible, use a numeric text box if:</span></span>

-   <span data-ttu-id="cfd28-130">Lo spazio sullo schermo è limitato.</span><span class="sxs-lookup"><span data-stu-id="cfd28-130">Screen space is tight.</span></span>
-   <span data-ttu-id="cfd28-131">È probabile che un utente preferisca utilizzare la tastiera.</span><span class="sxs-lookup"><span data-stu-id="cfd28-131">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="cfd28-132">Usa un dispositivo di scorrimento se:</span><span class="sxs-lookup"><span data-stu-id="cfd28-132">Use a slider if:</span></span>

-   <span data-ttu-id="cfd28-133">Gli utenti trarranno vantaggio da un riscontro immediato.</span><span class="sxs-lookup"><span data-stu-id="cfd28-133">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="cfd28-134">Indicazioni</span><span class="sxs-lookup"><span data-stu-id="cfd28-134">Guidelines</span></span>

-   <span data-ttu-id="cfd28-135">**Usa un orientamento naturale.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-135">**Use a natural orientation.**</span></span> <span data-ttu-id="cfd28-136">Ad esempio, se il dispositivo di scorrimento rappresenta un valore reale indicato di solito in verticale (come la temperatura), usa un orientamento verticale.</span><span class="sxs-lookup"><span data-stu-id="cfd28-136">For example, if the slider represents a real-world value that is normally shown vertically (such as temperature), use a vertical orientation.</span></span>
-   <span data-ttu-id="cfd28-137">**Orientare il dispositivo di scorrimento in modo da riflettere le impostazioni cultura degli utenti.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-137">**Orient the slider to reflect the culture of your users.**</span></span> <span data-ttu-id="cfd28-138">Ad esempio, le impostazioni cultura occidentali sono lette da sinistra a destra, quindi per i dispositivi di scorrimento orizzontali posizionare la parte inferiore dell'intervallo a sinistra e l'estremità superiore a destra.</span><span class="sxs-lookup"><span data-stu-id="cfd28-138">For example, Western cultures read from left to right, so for horizontal sliders, put the low end of the range on the left and the high end on the right.</span></span> <span data-ttu-id="cfd28-139">Per le impostazioni cultura che leggono da destra a sinistra, eseguire l'operazione opposta.</span><span class="sxs-lookup"><span data-stu-id="cfd28-139">For cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="cfd28-140">**Ridimensionare il controllo in modo che un utente possa facilmente impostare il valore desiderato.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-140">**Size the control so that a user can easily set the desired value.**</span></span> <span data-ttu-id="cfd28-141">Per le impostazioni con valori discreti, assicurati che l'utente possa selezionare agevolmente i valori con il mouse.</span><span class="sxs-lookup"><span data-stu-id="cfd28-141">For settings with discrete values, make sure the user can easily select any value using the mouse.</span></span>
-   <span data-ttu-id="cfd28-142">**Si consiglia di usare una scala non lineare se l'intervallo di valori è elevato e gli utenti possono selezionare i valori in un'estremità dell'intervallo.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-142">**Consider using a non-linear scale if the range of values is large and users will likely select values at one end of the range.**</span></span> <span data-ttu-id="cfd28-143">Ad esempio, il valore di ora può essere 1 minuto, 1 ora, 1 giorno o 1 mese.</span><span class="sxs-lookup"><span data-stu-id="cfd28-143">For example, time value might be 1 minute, 1 hour, 1 day, or 1 month.</span></span>
-   <span data-ttu-id="cfd28-144">**Quando si pratica, è possibile fornire commenti e suggerimenti immediatamente durante o dopo la selezione di un utente.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-144">**Whenever practical, give immediate feedback while or after a user makes a selection.**</span></span> <span data-ttu-id="cfd28-145">Il controllo del volume di Microsoft Windows, ad esempio, emette un segnale acustico per indicare il volume audio risultante.</span><span class="sxs-lookup"><span data-stu-id="cfd28-145">For example, the Microsoft Windows volume control beeps to indicate the resulting audio volume.</span></span>
-   <span data-ttu-id="cfd28-146">**Usa etichette per indicare l'intervallo di valori.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-146">**Use labels to show the range of values.**</span></span>

    <span data-ttu-id="cfd28-147">**Eccezione:** Se il dispositivo di scorrimento è orientato verticalmente e l'etichetta superiore è massima, alta, più o equivalente, è possibile omettere le altre etichette perché il significato è chiaro.</span><span class="sxs-lookup"><span data-stu-id="cfd28-147">**Exception:** If the slider is vertically oriented and the top label is Maximum, High, More, or equivalent, you can omit the other labels since the meaning is clear.</span></span>

    ![<span data-ttu-id="cfd28-148">Figura di un dispositivo di scorrimento verticale</span><span class="sxs-lookup"><span data-stu-id="cfd28-148">figure of a vertical slider</span></span> ](images/ctrl-sliders-image2.png)

    <span data-ttu-id="cfd28-149">In questo esempio, l'orientamento verticale del dispositivo di scorrimento rende le etichette di intervallo non necessarie.</span><span class="sxs-lookup"><span data-stu-id="cfd28-149">In this example, the slider's vertical orientation makes the range labels unnecessary.</span></span>

-   <span data-ttu-id="cfd28-150">**Usare i segni di graduazione quando è necessario che gli utenti conoscano il valore approssimativo dell'impostazione.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-150">**Use tick marks when users need to know the approximate value of the setting.**</span></span>
-   <span data-ttu-id="cfd28-151">**Usare i segni di graduazione e un'etichetta del valore quando gli utenti devono ottenere il valore esatto dell'impostazione scelta.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-151">**Use tick marks and a value label when users need to know the exact value of the setting they choose.**</span></span> <span data-ttu-id="cfd28-152">Usare sempre un'etichetta di valore se un utente deve essere a conoscenza delle unità per dare senso all'impostazione.</span><span class="sxs-lookup"><span data-stu-id="cfd28-152">Always use a value label if a user needs to know the units to make sense of the setting.</span></span>

    ![<span data-ttu-id="cfd28-153">Figura del dispositivo di scorrimento che mostra il numero di pixel selezionati</span><span class="sxs-lookup"><span data-stu-id="cfd28-153">figure of slider showing number of pixels selected</span></span> ](images/ctrl-sliders-image3.png)

    <span data-ttu-id="cfd28-154">In questo esempio viene usata un'etichetta per indicare chiaramente il valore selezionato.</span><span class="sxs-lookup"><span data-stu-id="cfd28-154">In this example, a label is used to clearly indicate the selected value.</span></span>

-   <span data-ttu-id="cfd28-155">**Per i dispositivi di scorrimento orientati orizzontalmente, posizionare i segni di graduazione sotto il dispositivo di scorrimento.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-155">**For horizontally-oriented sliders, place tick marks under the slider.**</span></span> <span data-ttu-id="cfd28-156">Per i dispositivi di scorrimento orientati verticalmente, posizionare i segni di graduazione a destra per le impostazioni cultura occidentali; per le impostazioni cultura che leggono da destra a sinistra, eseguire l'operazione opposta.</span><span class="sxs-lookup"><span data-stu-id="cfd28-156">For vertically-oriented sliders, place tick marks to the right for Western cultures; for cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="cfd28-157">**Posizionare l'etichetta del valore completamente sotto il controllo dispositivo di scorrimento in modo che la relazione sia chiara.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-157">**Place the value label completely under the slider control so that the relationship is clear.**</span></span>

    <span data-ttu-id="cfd28-158">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="cfd28-158">**Incorrect:**</span></span>

    ![<span data-ttu-id="cfd28-159">Figura di un'etichetta più lunga del relativo dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="cfd28-159">figure of a label that is longer than its slider</span></span> ](images/ctrl-sliders-image4.png)

    <span data-ttu-id="cfd28-160">In questo esempio, l'etichetta del valore non è allineata sotto il dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="cfd28-160">In this example, the value label isn't aligned under the slider.</span></span>

-   <span data-ttu-id="cfd28-161">**Quando si disabilita un dispositivo di scorrimento, disabilitare anche le etichette associate.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-161">**When disabling a slider, also disable any associated labels.**</span></span>
-   <span data-ttu-id="cfd28-162">**Non usare sia un dispositivo di scorrimento che una casella di testo numerica per la stessa impostazione.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-162">**Don't use both a slider and a numeric text box for the same setting.**</span></span> <span data-ttu-id="cfd28-163">Usare solo il controllo più appropriato.</span><span class="sxs-lookup"><span data-stu-id="cfd28-163">Use only the more appropriate control.</span></span>

    <span data-ttu-id="cfd28-164">**Eccezione:** Usare entrambi i controlli quando l'utente necessita di un feedback immediato e della possibilità di impostare un valore numerico esatto.</span><span class="sxs-lookup"><span data-stu-id="cfd28-164">**Exception:** Use both controls when the user needs both immediate feedback and the ability to set an exact numeric value.</span></span>

-   <span data-ttu-id="cfd28-165">**Non usare un dispositivo di scorrimento come indicatore di stato.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-165">**Don't use a slider as a progress indicator.**</span></span>
-   <span data-ttu-id="cfd28-166">**Non modificare le dimensioni dell'indicatore del dispositivo di scorrimento dalla dimensione predefinita.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-166">**Don't change the size of the slider indicator from the default size.**</span></span>

    <span data-ttu-id="cfd28-167">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="cfd28-167">**Incorrect:**</span></span>

    ![<span data-ttu-id="cfd28-168">Figura del dispositivo di scorrimento minore del valore predefinito</span><span class="sxs-lookup"><span data-stu-id="cfd28-168">figure of slider that is smaller than the default</span></span> ](images/ctrl-sliders-image5.png)

    <span data-ttu-id="cfd28-169">In questo esempio viene usata una dimensione inferiore a quella predefinita.</span><span class="sxs-lookup"><span data-stu-id="cfd28-169">In this example, a size smaller than the default is used.</span></span>

    <span data-ttu-id="cfd28-170">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="cfd28-170">**Correct:**</span></span>

    ![<span data-ttu-id="cfd28-171">figura che mostra il dispositivo di scorrimento predefinito</span><span class="sxs-lookup"><span data-stu-id="cfd28-171">figure showing the default slider</span></span> ](images/ctrl-sliders-image6.png)

    <span data-ttu-id="cfd28-172">In questo esempio vengono usate le dimensioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="cfd28-172">In this example, the default size is used.</span></span>

-   <span data-ttu-id="cfd28-173">**Non etichettare ogni segno di graduazione.**</span><span class="sxs-lookup"><span data-stu-id="cfd28-173">**Don't label every tick mark.**</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="cfd28-174">Ridimensionamento e spaziatura consigliati</span><span class="sxs-lookup"><span data-stu-id="cfd28-174">Recommended sizing and spacing</span></span>

![<span data-ttu-id="cfd28-175">Figura di ridimensionamento e spaziatura del dispositivo di scorrimento consigliati</span><span class="sxs-lookup"><span data-stu-id="cfd28-175">figure of recommended slider sizing and spacing</span></span> ](images/ctrl-sliders-image7.png)

<span data-ttu-id="cfd28-176">Dimensionamento e spaziatura consigliati per i dispositivi di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="cfd28-176">Recommended sizing and spacing for sliders.</span></span>

## <a name="labels"></a><span data-ttu-id="cfd28-177">Etichette</span><span class="sxs-lookup"><span data-stu-id="cfd28-177">Labels</span></span>

### <a name="slider-labels"></a><span data-ttu-id="cfd28-178">Etichette del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="cfd28-178">Slider labels</span></span>

-   <span data-ttu-id="cfd28-179">Utilizzare un'etichetta di testo statico che termina con i due punti oppure un'etichetta di casella di gruppo senza punteggiatura finale.</span><span class="sxs-lookup"><span data-stu-id="cfd28-179">Use a static text label ending with a colon, or a group box label with no ending punctuation.</span></span>
-   <span data-ttu-id="cfd28-180">Assegnare una chiave di accesso univoca a ogni etichetta.</span><span class="sxs-lookup"><span data-stu-id="cfd28-180">Assign a unique access key to each label.</span></span> <span data-ttu-id="cfd28-181">Per le linee guida di assegnazione, vedere [tastiera](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="cfd28-181">For assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="cfd28-182">Usare le maiuscole/minuscole come nelle frasi comuni.</span><span class="sxs-lookup"><span data-stu-id="cfd28-182">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="cfd28-183">Posizionare l'etichetta del dispositivo di scorrimento a sinistra del dispositivo di scorrimento o superiore e allineato al bordo sinistro del dispositivo di scorrimento (o all'identificatore di intervallo sinistro, se presente).</span><span class="sxs-lookup"><span data-stu-id="cfd28-183">Position the slider label either to the left of the slider, or above and aligned with the left edge of the slider (or its left range identifier, if present).</span></span>

### <a name="range-labels"></a><span data-ttu-id="cfd28-184">Etichette di intervallo</span><span class="sxs-lookup"><span data-stu-id="cfd28-184">Range labels</span></span>

-   <span data-ttu-id="cfd28-185">Usa due etichette per le due estremità dell'intervallo del dispositivo di scorrimento, se non usi un orientamento verticale che le rende superflue.</span><span class="sxs-lookup"><span data-stu-id="cfd28-185">Label the two ends of the slider range, unless a vertical orientation makes this unnecessary.</span></span>
-   <span data-ttu-id="cfd28-186">Usare solo Word, se possibile, per ogni etichetta.</span><span class="sxs-lookup"><span data-stu-id="cfd28-186">Use only word, if possible, for each label.</span></span>
-   <span data-ttu-id="cfd28-187">Non usare punteggiatura finale.</span><span class="sxs-lookup"><span data-stu-id="cfd28-187">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="cfd28-188">Controlla che queste etichette siano descrittive e parallele.</span><span class="sxs-lookup"><span data-stu-id="cfd28-188">Make sure these labels are descriptive and parallel.</span></span> <span data-ttu-id="cfd28-189">Di seguito sono riportati alcuni esempi. Massimo/Minimo, Più/Meno, Alto/Basso, Piano/Forte.</span><span class="sxs-lookup"><span data-stu-id="cfd28-189">Examples: Maximum/Minimum, More/Less, Low/High, Soft/Loud.</span></span>
-   <span data-ttu-id="cfd28-190">Usare le maiuscole/minuscole come nelle frasi comuni.</span><span class="sxs-lookup"><span data-stu-id="cfd28-190">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="cfd28-191">Non assegnare chiavi di accesso.</span><span class="sxs-lookup"><span data-stu-id="cfd28-191">Don't assign access keys.</span></span>

### <a name="value-labels"></a><span data-ttu-id="cfd28-192">Etichette di valore</span><span class="sxs-lookup"><span data-stu-id="cfd28-192">Value labels</span></span>

-   <span data-ttu-id="cfd28-193">Se ti serve un'etichetta di valore, visualizzala sotto il dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="cfd28-193">If you need a value label, display it below the slider.</span></span>
-   <span data-ttu-id="cfd28-194">Centra il testo rispetto al controllo e includi le unità (ad esempio, i pixel).</span><span class="sxs-lookup"><span data-stu-id="cfd28-194">Center the text relative to the control and include the units (such as pixels).</span></span>

    ![<span data-ttu-id="cfd28-195">Figura dell'etichetta centrata sotto il dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="cfd28-195">figure of label centered under the slider</span></span> ](images/ctrl-sliders-image8.png)

    <span data-ttu-id="cfd28-196">In questo esempio, l'etichetta del valore viene centrata sotto il dispositivo di scorrimento e include le unità.</span><span class="sxs-lookup"><span data-stu-id="cfd28-196">In this example, the value label is centered under the slider and includes the units.</span></span>

## <a name="documentation"></a><span data-ttu-id="cfd28-197">Documentazione</span><span class="sxs-lookup"><span data-stu-id="cfd28-197">Documentation</span></span>

<span data-ttu-id="cfd28-198">Quando si fa riferimento ai dispositivi di scorrimento:</span><span class="sxs-lookup"><span data-stu-id="cfd28-198">When referring to sliders:</span></span>

-   <span data-ttu-id="cfd28-199">Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, e includere la parola slider.</span><span class="sxs-lookup"><span data-stu-id="cfd28-199">Use the exact label text, including its capitalization, and include the word slider.</span></span> <span data-ttu-id="cfd28-200">Non includere il carattere di sottolineatura della chiave di accesso o i due punti.</span><span class="sxs-lookup"><span data-stu-id="cfd28-200">Don't include the access key underscore or colon.</span></span>
-   <span data-ttu-id="cfd28-201">Per descrivere l'interazione dell'utente, utilizzare Move.</span><span class="sxs-lookup"><span data-stu-id="cfd28-201">To describe user interaction, use move.</span></span>
-   <span data-ttu-id="cfd28-202">Quando possibile, formattare l'etichetta usando il testo in grassetto.</span><span class="sxs-lookup"><span data-stu-id="cfd28-202">When possible, format the label using bold text.</span></span> <span data-ttu-id="cfd28-203">In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.</span><span class="sxs-lookup"><span data-stu-id="cfd28-203">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="cfd28-204">Esempio: per aumentare la risoluzione dello schermo, spostare il dispositivo di scorrimento **risoluzione schermo** a destra.</span><span class="sxs-lookup"><span data-stu-id="cfd28-204">Example: To increase your screen resolution, move the **Screen resolution** slider to the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfd28-205">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cfd28-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfd28-206">Glossario</span><span class="sxs-lookup"><span data-stu-id="cfd28-206">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 