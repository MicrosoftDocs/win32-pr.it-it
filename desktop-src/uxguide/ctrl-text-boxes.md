---
title: Caselle di testo
description: Con una casella di testo, gli utenti possono visualizzare, immettere o modificare un valore di testo o numerico.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2b5257e9772465f26815abb0f6ecbe0ff357ba4b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530433"
---
# <a name="text-boxes"></a><span data-ttu-id="c20cc-103">Caselle di testo</span><span class="sxs-lookup"><span data-stu-id="c20cc-103">Text Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="c20cc-104">Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="c20cc-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="c20cc-105">Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="c20cc-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="c20cc-106">Con una casella di testo, gli utenti possono visualizzare, immettere o modificare un valore di testo o numerico.</span><span class="sxs-lookup"><span data-stu-id="c20cc-106">With a text box, users can display, enter, or edit a text or numeric value.</span></span>

![<span data-ttu-id="c20cc-107">Screenshot di una casella di testo e di un'etichetta tipici</span><span class="sxs-lookup"><span data-stu-id="c20cc-107">screen shot of a typical text box and label</span></span> ](images/ctrl-text-boxes-image1.png)

<span data-ttu-id="c20cc-108">Casella di testo tipica.</span><span class="sxs-lookup"><span data-stu-id="c20cc-108">A typical text box.</span></span>

> [!Note]  
> <span data-ttu-id="c20cc-109">Le linee guida relative a [layout](vis-layout.md), [tipi di carattere](vis-fonts.md)e [palloni](ctrl-balloons.md) vengono presentate in articoli distinti.</span><span class="sxs-lookup"><span data-stu-id="c20cc-109">Guidelines related to [layout](vis-layout.md), [fonts](vis-fonts.md), and [balloons](ctrl-balloons.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="c20cc-110">È il controllo giusto?</span><span class="sxs-lookup"><span data-stu-id="c20cc-110">Is this the right control?</span></span>

<span data-ttu-id="c20cc-111">Per decidere, prendi in considerazione queste domande:</span><span class="sxs-lookup"><span data-stu-id="c20cc-111">To decide, consider these questions:</span></span>

-   <span data-ttu-id="c20cc-112">**È utile enumerare tutti i valori validi in modo efficiente?**</span><span class="sxs-lookup"><span data-stu-id="c20cc-112">**Is it practical to enumerate all the valid values efficiently?**</span></span> <span data-ttu-id="c20cc-113">In tal caso, prendere in considerazione un [elenco a selezione singola](ctrl-list-boxes.md), una [visualizzazione elenco](ctrl-list-views.md), un elenco [a discesa](/windows/desktop/uxguide/ctrl-drop), un elenco a discesa modificabile o un [dispositivo di scorrimento](ctrl-sliders.md) .</span><span class="sxs-lookup"><span data-stu-id="c20cc-113">If so, consider a [single-selection list](ctrl-list-boxes.md), [list view](ctrl-list-views.md), [drop-down list](/windows/desktop/uxguide/ctrl-drop), editable drop-down list, or [slider](ctrl-sliders.md) instead.</span></span>
-   <span data-ttu-id="c20cc-114">**I dati validi sono completamente non vincolati? O sono i dati validi vincolati solo in base al formato (lunghezza vincolata o tipi di carattere)?**</span><span class="sxs-lookup"><span data-stu-id="c20cc-114">**Is the valid data completely unconstrained? Or is the valid data constrained only by format (constrained length or character types)?**</span></span> <span data-ttu-id="c20cc-115">In tal caso, utilizzare una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-115">If so, use a text box.</span></span>
-   <span data-ttu-id="c20cc-116">**Il valore rappresenta un tipo di dati che dispone di un controllo comune specifico?**</span><span class="sxs-lookup"><span data-stu-id="c20cc-116">**Does the value represent a data type that has a specialized common control?**</span></span> <span data-ttu-id="c20cc-117">Gli esempi includono data, ora o indirizzo IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="c20cc-117">Examples include date, time, or IPv4 or IPv6 address.</span></span> <span data-ttu-id="c20cc-118">In tal caso, utilizzare il controllo appropriato, ad esempio un controllo data anziché una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-118">If so, use the appropriate control, such as a date control rather than a text box.</span></span>
-   <span data-ttu-id="c20cc-119">Se i dati sono numerici:</span><span class="sxs-lookup"><span data-stu-id="c20cc-119">If the data is numeric:</span></span>
    -   <span data-ttu-id="c20cc-120">**Gli utenti percepiscono l'impostazione come una quantità relativa?**</span><span class="sxs-lookup"><span data-stu-id="c20cc-120">**Do users perceive the setting as a relative quantity?**</span></span> <span data-ttu-id="c20cc-121">Se sì, usa un dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="c20cc-121">If so, use a slider.</span></span>
    -   <span data-ttu-id="c20cc-122">**L'utente trarrebbe vantaggio da un riscontro immediato sull'effetto delle modifiche dell'impostazione?**</span><span class="sxs-lookup"><span data-stu-id="c20cc-122">**Would the user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="c20cc-123">In tal caso, utilizzare un dispositivo di scorrimento, possibilmente insieme a una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-123">If so, use a slider, possibly along with a text box.</span></span> <span data-ttu-id="c20cc-124">Ad esempio, gli utenti possono scegliere facilmente un colore usando un dispositivo di scorrimento perché possono visualizzare immediatamente l'effetto delle modifiche ai valori di tonalità, saturazione o luminosità.</span><span class="sxs-lookup"><span data-stu-id="c20cc-124">For example, users can easily choose a color using a slider because they can immediately see the effect of changes to hue, saturation, or luminosity values.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="c20cc-125">Concetti relativi alla progettazione</span><span class="sxs-lookup"><span data-stu-id="c20cc-125">Design concepts</span></span>

<span data-ttu-id="c20cc-126">Mentre le caselle di testo hanno il vantaggio di essere molto flessibili, hanno lo svantaggio di avere limitazioni minime.</span><span class="sxs-lookup"><span data-stu-id="c20cc-126">While text boxes have the benefit of being very flexible, they have the drawback of having minimal constraints.</span></span> <span data-ttu-id="c20cc-127">Gli unici vincoli in una casella di testo modificabile sono:</span><span class="sxs-lookup"><span data-stu-id="c20cc-127">The only constraints on an editable text box are:</span></span>

-   <span data-ttu-id="c20cc-128">Facoltativamente, è possibile impostare il numero massimo di caratteri.</span><span class="sxs-lookup"><span data-stu-id="c20cc-128">You can optionally set the maximum number of characters.</span></span>
-   <span data-ttu-id="c20cc-129">Facoltativamente, è possibile limitare l'input solo ai caratteri numerici (0 9).</span><span class="sxs-lookup"><span data-stu-id="c20cc-129">You can optionally restrict input to numeric characters (0   9) only.</span></span>
-   <span data-ttu-id="c20cc-130">Se si usa un [controllo di selezione](ctrl-spin-controls.md), è possibile limitare le opzioni di controllo di selezione ai valori validi.</span><span class="sxs-lookup"><span data-stu-id="c20cc-130">If you use a [spin control](ctrl-spin-controls.md), you can limit spin control choices to valid values.</span></span>

<span data-ttu-id="c20cc-131">Oltre alla lunghezza e alla presenza facoltativa di un controllo di selezione, le caselle di testo non hanno indizi visivi che suggeriscono i valori validi o il formato.</span><span class="sxs-lookup"><span data-stu-id="c20cc-131">Aside from their length and the optional presence of a spin control, text boxes don't have any visual clues that suggest the valid values or their format.</span></span> <span data-ttu-id="c20cc-132">Ciò significa basarsi sulle etichette per fornire queste informazioni agli utenti.</span><span class="sxs-lookup"><span data-stu-id="c20cc-132">This means relying on labels to convey this information to users.</span></span> <span data-ttu-id="c20cc-133">Se gli utenti immettono testo non valido, è necessario gestire l'errore con un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="c20cc-133">If users enter text that's not valid, you must handle the error with an error message.</span></span>

<span data-ttu-id="c20cc-134">Come regola generale, **è consigliabile usare il controllo più vincolato possibile**.</span><span class="sxs-lookup"><span data-stu-id="c20cc-134">As a general rule, **you should use the most constrained control that you can**.</span></span> <span data-ttu-id="c20cc-135">Usare controlli non vincolati come le caselle di testo come ultima risorsa.</span><span class="sxs-lookup"><span data-stu-id="c20cc-135">Use unconstrained controls like text boxes as a last resort.</span></span> <span data-ttu-id="c20cc-136">Ciò detto, quando si considerano i vincoli, tenere presente le esigenze degli utenti globali.</span><span class="sxs-lookup"><span data-stu-id="c20cc-136">That said, when you are considering constraints, bear in mind the needs of global users.</span></span> <span data-ttu-id="c20cc-137">Ad esempio, un controllo vincolato a Stati Uniti CAP non è globalizzato, ma una casella di testo non vincolata che accetta qualsiasi formato di codice postale è.</span><span class="sxs-lookup"><span data-stu-id="c20cc-137">For example, a control that is constrained to United States ZIP Codes isn't globalized, but an unconstrained text box that accepts any postal code format is.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="c20cc-138">Modelli di utilizzo</span><span class="sxs-lookup"><span data-stu-id="c20cc-138">Usage patterns</span></span>

<span data-ttu-id="c20cc-139">Una casella di testo è un controllo flessibile con diversi usi possibili.</span><span class="sxs-lookup"><span data-stu-id="c20cc-139">A text box is a flexible control with several possible uses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c20cc-140"><strong>Input di dati</strong></span><span class="sxs-lookup"><span data-stu-id="c20cc-140"><strong>Data input</strong></span></span><br/> <span data-ttu-id="c20cc-141">Casella di testo a riga singola non vincolata utilizzata per inserire o modificare stringhe brevi.</span><span class="sxs-lookup"><span data-stu-id="c20cc-141">A single-line, unconstrained text box used to enter or edit short strings.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> <span data-ttu-id="c20cc-142">Casella di testo A riga singola non vincolata.</span><span class="sxs-lookup"><span data-stu-id="c20cc-142">A single-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c20cc-143"><strong>Input di dati formattato</strong></span><span class="sxs-lookup"><span data-stu-id="c20cc-143"><strong>Formatted data input</strong></span></span><br/> <span data-ttu-id="c20cc-144">Set di caselle di testo a dimensione fissa breve e a dimensione fissa utilizzate per immettere dati con un formato specifico.</span><span class="sxs-lookup"><span data-stu-id="c20cc-144">A set of short, fixed-sized, single-line text boxes used to enter data with a specific format.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> <span data-ttu-id="c20cc-145">Casella di testo utilizzata per l'input di dati formattato.</span><span class="sxs-lookup"><span data-stu-id="c20cc-145">A text box used for formatted data input.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c20cc-146">La funzionalità di <a href="glossary.md">uscita automatica</a> sposta automaticamente lo stato attivo di input da una casella di testo a quella successiva.</span><span class="sxs-lookup"><span data-stu-id="c20cc-146">The <a href="glossary.md">auto-exit</a> feature automatically advances the input focus from one text box to the next.</span></span> <span data-ttu-id="c20cc-147">Uno svantaggio di questo approccio è che i dati non possono essere copiati o incollati come singola unità.</span><span class="sxs-lookup"><span data-stu-id="c20cc-147">One disadvantage to this approach is that the data can't be copied or pasted as a single unit.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c20cc-148"><strong>Input di dati assistito</strong></span><span class="sxs-lookup"><span data-stu-id="c20cc-148"><strong>Assisted data input</strong></span></span><br/> <span data-ttu-id="c20cc-149">Casella di testo a riga singola non vincolata utilizzata per immettere o modificare le stringhe, insieme a un pulsante di comando che consente agli utenti di selezionare valori validi.</span><span class="sxs-lookup"><span data-stu-id="c20cc-149">A single-line, unconstrained text box used to enter or edit strings, combined with a command button that helps users select valid values.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> <span data-ttu-id="c20cc-150">In questo esempio, il comando Browse consente agli utenti di selezionare valori validi.</span><span class="sxs-lookup"><span data-stu-id="c20cc-150">In this example, the Browse command helps users select valid values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c20cc-151"><strong>Input testuale</strong></span><span class="sxs-lookup"><span data-stu-id="c20cc-151"><strong>Textual input</strong></span></span><br/> <span data-ttu-id="c20cc-152">Casella di testo a più righe, non vincolata utilizzata per inserire o modificare stringhe lunghe.</span><span class="sxs-lookup"><span data-stu-id="c20cc-152">A multi-line, unconstrained text box used to enter or edit long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> <span data-ttu-id="c20cc-153">Casella di testo A più righe, non vincolata.</span><span class="sxs-lookup"><span data-stu-id="c20cc-153">A multi-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c20cc-154"><strong>Input numerico</strong></span><span class="sxs-lookup"><span data-stu-id="c20cc-154"><strong>Numeric input</strong></span></span><br/> <span data-ttu-id="c20cc-155">Casella di testo a riga singola solo numerica utilizzata per inserire o modificare numeri, con un controllo di <a href="ctrl-spin-controls.md">selezione</a> facoltativo per facilitare l'input basato sul mouse.</span><span class="sxs-lookup"><span data-stu-id="c20cc-155">A single-line, numeric-only text box used to enter or edit numbers, with an optional <a href="ctrl-spin-controls.md">spin control</a> to facilitate mouse-based input.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> <span data-ttu-id="c20cc-156">Casella di testo utilizzata per l'input numerico.</span><span class="sxs-lookup"><span data-stu-id="c20cc-156">A text box used for numeric input.</span></span><br/> <span data-ttu-id="c20cc-157">La combinazione di una casella di testo e del controllo di selezione associato è detta <a href="ctrl-spin-controls.md">casella di selezione</a>.</span><span class="sxs-lookup"><span data-stu-id="c20cc-157">The combination of a text box and its associated spin control is called a <a href="ctrl-spin-controls.md">spin box</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c20cc-158"><strong>Input di password e PIN</strong></span><span class="sxs-lookup"><span data-stu-id="c20cc-158"><strong>Password and PIN input</strong></span></span><br/> <span data-ttu-id="c20cc-159">Casella di testo a riga singola non vincolata utilizzata per immettere le password e i pin in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="c20cc-159">A single-line, unconstrained text box used to enter passwords and PINs securely.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> <span data-ttu-id="c20cc-160">Casella di testo utilizzata per immettere le password.</span><span class="sxs-lookup"><span data-stu-id="c20cc-160">A text box used to enter passwords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c20cc-161"><strong>Output dei dati</strong></span><span class="sxs-lookup"><span data-stu-id="c20cc-161"><strong>Data output</strong></span></span><br/> <span data-ttu-id="c20cc-162">Una casella di testo a riga singola, di sola lettura, sempre visualizzata senza bordo, utilizzata per visualizzare le stringhe brevi.</span><span class="sxs-lookup"><span data-stu-id="c20cc-162">A single-line, read-only text box, always displayed without a border, used to display short strings.</span></span> <br/></td>
<td><span data-ttu-id="c20cc-163">A differenza del testo statico, è possibile scorrere i dati visualizzati utilizzando una casella di testo (utile se i dati sono più larghi del controllo), selezionati e copiati.</span><span class="sxs-lookup"><span data-stu-id="c20cc-163">Unlike static text, data displayed using a text box can be scrolled (useful if the data is wider than the control), selected, and copied.</span></span><br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> <span data-ttu-id="c20cc-164">Casella di testo di sola lettura a riga singola utilizzata per visualizzare i dati.</span><span class="sxs-lookup"><span data-stu-id="c20cc-164">A single-line, read-only text box used to display data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c20cc-165"><strong>Output testuale</strong></span><span class="sxs-lookup"><span data-stu-id="c20cc-165"><strong>Textual output</strong></span></span><br/> <span data-ttu-id="c20cc-166">Casella di testo di sola lettura a più righe utilizzata per visualizzare stringhe lunghe.</span><span class="sxs-lookup"><span data-stu-id="c20cc-166">A multi-line, read-only text box used to display long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> <span data-ttu-id="c20cc-167">Casella di testo di sola lettura utilizzata per visualizzare i dati.</span><span class="sxs-lookup"><span data-stu-id="c20cc-167">A read-only text box used to display data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="c20cc-168">Indicazioni</span><span class="sxs-lookup"><span data-stu-id="c20cc-168">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="c20cc-169">Generale</span><span class="sxs-lookup"><span data-stu-id="c20cc-169">General</span></span>

-   <span data-ttu-id="c20cc-170">**Quando si disabilita una casella di testo, disabilitare anche le etichette associate, le etichette di istruzione, i controlli di selezione e i pulsanti di comando.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-170">**When disabling a text box, also disable any associated labels, instruction labels, spin controls, and command buttons.**</span></span>
-   <span data-ttu-id="c20cc-171">**Usare il completamento automatico per consentire agli utenti di immettere dati che potrebbero essere usati ripetutamente**.</span><span class="sxs-lookup"><span data-stu-id="c20cc-171">**Use auto-complete to help users enter data that is likely to be used repeatedly**.</span></span> <span data-ttu-id="c20cc-172">Gli esempi includono nomi utente, indirizzi e nomi di file.</span><span class="sxs-lookup"><span data-stu-id="c20cc-172">Examples include user names, addresses, and file names.</span></span> <span data-ttu-id="c20cc-173">Tuttavia, non usare il completamento automatico per caselle di testo che possono contenere informazioni riservate, ad esempio password, pin, numeri di carta di credito o informazioni mediche.</span><span class="sxs-lookup"><span data-stu-id="c20cc-173">However, don't use auto-complete for text boxes that may contain sensitive information, such as passwords, PINs, credit card numbers, or medical information.</span></span>
-   <span data-ttu-id="c20cc-174">**Non fare in modo che gli utenti scorrano inutilmente.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-174">**Don't make users scroll unnecessarily.**</span></span> <span data-ttu-id="c20cc-175">Se si prevede che i dati siano più grandi della casella di testo ed è possibile fare in modo che la casella di testo sia più grande senza danneggiare il layout, ridimensionare la casella per eliminare la necessità di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="c20cc-175">If you expect data to be larger than the text box and you can readily make the text box larger without harming the layout, size the box to eliminate the need for scrolling.</span></span>

    <span data-ttu-id="c20cc-176">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-176">**Incorrect:**</span></span>

    ![<span data-ttu-id="c20cc-177">screenshot della casella di testo nome computer</span><span class="sxs-lookup"><span data-stu-id="c20cc-177">screen shot of a computer name text box</span></span> ](images/ctrl-text-boxes-image10.png)

    <span data-ttu-id="c20cc-178">In questo esempio la casella di testo deve essere resa più lunga per gestire i dati.</span><span class="sxs-lookup"><span data-stu-id="c20cc-178">In this example, the text box should be made much longer to handle its data.</span></span>

-   <span data-ttu-id="c20cc-179">Barre di scorrimento:</span><span class="sxs-lookup"><span data-stu-id="c20cc-179">Scroll bars:</span></span>
    -   <span data-ttu-id="c20cc-180">**Non inserire barre di scorrimento orizzontali nelle caselle di testo a più righe.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-180">**Don't put horizontal scroll bars on multi-line text boxes.**</span></span> <span data-ttu-id="c20cc-181">Usare invece lo scorrimento verticale e il ritorno a capo riga.</span><span class="sxs-lookup"><span data-stu-id="c20cc-181">Use vertical scrolling and line wrapping instead.</span></span>
    -   <span data-ttu-id="c20cc-182">**Non inserire barre di scorrimento sulle caselle di testo a riga singola.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-182">**Don't put any scroll bars on single-line text boxes.**</span></span>
-   <span data-ttu-id="c20cc-183">**Per l'input numerico, è possibile usare un controllo di selezione.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-183">**For numeric input, you may use a spin control.**</span></span> <span data-ttu-id="c20cc-184">Per l'input testuale, usare invece un elenco a discesa o un elenco a discesa modificabile.</span><span class="sxs-lookup"><span data-stu-id="c20cc-184">For textual input, use a drop-down list or editable drop-down list instead.</span></span>
-   <span data-ttu-id="c20cc-185">**Non usare la funzionalità di uscita automatica, ad eccezione dell'input di dati formattato.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-185">**Don't use the auto-exit feature except for formatted data input.**</span></span> <span data-ttu-id="c20cc-186">Lo spostamento automatico dello stato attivo può sorprendere gli utenti.</span><span class="sxs-lookup"><span data-stu-id="c20cc-186">The automatic shift of focus can surprise users.</span></span>

### <a name="editable-text-boxes"></a><span data-ttu-id="c20cc-187">Caselle di testo modificabili</span><span class="sxs-lookup"><span data-stu-id="c20cc-187">Editable text boxes</span></span>

-   <span data-ttu-id="c20cc-188">**Quando possibile, limitare la lunghezza del testo di input.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-188">**Limit the length of the input text when you can.**</span></span> <span data-ttu-id="c20cc-189">Se, ad esempio, l'input valido è un numero compreso tra 0 e 999, utilizzare una casella di testo numerica limitata a tre caratteri.</span><span class="sxs-lookup"><span data-stu-id="c20cc-189">For example, if the valid input is a number between 0 and 999, use a numeric text box that is limited to three characters.</span></span> <span data-ttu-id="c20cc-190">Tutte le parti di caselle di testo che utilizzano input di dati formattati devono avere una lunghezza fissa breve.</span><span class="sxs-lookup"><span data-stu-id="c20cc-190">All parts of text boxes that use formatted data input must have a short, fixed length.</span></span>
-   <span data-ttu-id="c20cc-191">**Essere flessibili con i formati di dati.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-191">**Be flexible with data formats.**</span></span> <span data-ttu-id="c20cc-192">Se è probabile che gli utenti immettano testo usando un'ampia gamma di formati, provare a gestire tutti i più comuni.</span><span class="sxs-lookup"><span data-stu-id="c20cc-192">If users are likely to enter text using a wide variety of formats, try to handle all the most common ones.</span></span> <span data-ttu-id="c20cc-193">È ad esempio possibile immettere molti nomi, numeri e identificatori con spazi e punteggiatura facoltativi e le maiuscole spesso non sono importanti.</span><span class="sxs-lookup"><span data-stu-id="c20cc-193">For example, many names, numbers, and identifiers can be entered with optional spaces and punctuation, and the capitalization often doesn't matter.</span></span>
-   <span data-ttu-id="c20cc-194">Se non è possibile gestire i formati probabili, richiedere un formato specifico usando input di dati formattati o indicare i formati validi nell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="c20cc-194">If you can't handle the likely formats, require a specific format by using formatted data input or indicate the valid formats in the label.</span></span>

    <span data-ttu-id="c20cc-195">**Accettabile:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-195">**Acceptable:**</span></span>

    ![<span data-ttu-id="c20cc-196">Screenshot di una casella di testo per l'input numerico</span><span class="sxs-lookup"><span data-stu-id="c20cc-196">screen shot of a text box for numeric input</span></span> ](images/ctrl-text-boxes-image11.png)

    <span data-ttu-id="c20cc-197">In questo esempio, una casella di testo richiede l'input in un formato specifico.</span><span class="sxs-lookup"><span data-stu-id="c20cc-197">In this example, a text box requires input in a specific format.</span></span>

    <span data-ttu-id="c20cc-198">**Migliore:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-198">**Better:**</span></span>

    ![<span data-ttu-id="c20cc-199">screenshot della casella di testo di input dei dati formattati</span><span class="sxs-lookup"><span data-stu-id="c20cc-199">screen shot of formatted data input text box</span></span> ](images/ctrl-text-boxes-image12.png)

    <span data-ttu-id="c20cc-200">In questo esempio, il modello di input dei dati formattato viene usato per richiedere un formato specifico.</span><span class="sxs-lookup"><span data-stu-id="c20cc-200">In this example, the formatted data input pattern is used to require a specific format.</span></span>

    <span data-ttu-id="c20cc-201">**Consigliate**</span><span class="sxs-lookup"><span data-stu-id="c20cc-201">**Best:**</span></span>

    ![<span data-ttu-id="c20cc-202">Screenshot di una casella di testo non vincolata</span><span class="sxs-lookup"><span data-stu-id="c20cc-202">screen shot of an unconstrained text box</span></span> ](images/ctrl-text-boxes-image13.png)

    <span data-ttu-id="c20cc-203">In questo esempio, una casella di testo gestisce tutti i formati probabili.</span><span class="sxs-lookup"><span data-stu-id="c20cc-203">In this example, a text box handles all likely formats.</span></span>

-   <span data-ttu-id="c20cc-204">Considerare la flessibilità del formato quando si sceglie la lunghezza massima di input.</span><span class="sxs-lookup"><span data-stu-id="c20cc-204">Consider format flexibility when choosing the maximum input length.</span></span> <span data-ttu-id="c20cc-205">Un numero di carta di credito valido, ad esempio, può utilizzare fino a 19 caratteri, quindi limitare la lunghezza a un valore più breve potrebbe rendere difficile l'immissione di numeri utilizzando i formati più lunghi.</span><span class="sxs-lookup"><span data-stu-id="c20cc-205">For example, a valid credit card number can use up to 19 characters so limiting the length to anything shorter would make it difficult to enter numbers using the longer formats.</span></span>
-   <span data-ttu-id="c20cc-206">**Non usare il modello di input dei dati formattato se gli utenti hanno più probabilità di incollare dati lunghi e complessi.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-206">**Don't use the formatted data input pattern if users are more likely to paste in long, complex data.**</span></span> <span data-ttu-id="c20cc-207">Riservare invece il modello di input dei dati formattato per le situazioni in cui è più probabile che gli utenti digitano i dati.</span><span class="sxs-lookup"><span data-stu-id="c20cc-207">Rather, reserve the formatted data input pattern for situations where users are more likely to type the data.</span></span>

    ![<span data-ttu-id="c20cc-208">Screenshot di una casella di testo con etichetta: indirizzo IPv6</span><span class="sxs-lookup"><span data-stu-id="c20cc-208">screen shot of a text box with label: ipv6 address</span></span> ](images/ctrl-text-boxes-image14.png)

    <span data-ttu-id="c20cc-209">In questo esempio, il modello di input dei dati formattato non viene usato, in modo che gli utenti possano incollare gli indirizzi IPv6.</span><span class="sxs-lookup"><span data-stu-id="c20cc-209">In this example, the formatted data input pattern isn't used, so that users can to paste IPv6 addresses.</span></span>

-   <span data-ttu-id="c20cc-210">**Se è più probabile che gli utenti immettano nuovamente l'intero valore, selezionare tutto il testo sullo stato attivo per l'input.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-210">**If users are more likely going to reenter the entire value, select all the text on input focus.**</span></span> <span data-ttu-id="c20cc-211">Se è più probabile che gli utenti modifichino, posizionare il punto di inserimento alla fine del testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-211">If users are more likely to edit, place the caret at the end of the text.</span></span>

    ![<span data-ttu-id="c20cc-212">screenshot della casella di testo della password</span><span class="sxs-lookup"><span data-stu-id="c20cc-212">screen shot of a password text box</span></span> ](images/ctrl-text-boxes-image15.png)

    <span data-ttu-id="c20cc-213">In questo esempio, è più probabile che gli utenti sostituiscano di Edit, quindi l'intero valore viene selezionato sullo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="c20cc-213">In this example, users are more likely to replace than edit, so the entire value is selected on input focus.</span></span>

    ![<span data-ttu-id="c20cc-214">Screenshot di una casella di testo per l'immissione di parole chiave</span><span class="sxs-lookup"><span data-stu-id="c20cc-214">screen shot of a text box for entering keywords</span></span> ](images/ctrl-text-boxes-image16.png)

    <span data-ttu-id="c20cc-215">In questo esempio, è più probabile che gli utenti aggiungano parole chiave che sostituiscono il testo, quindi il punto di inserimento si trova alla fine del testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-215">In this example, users are more likely to add keywords than replace the text, so the caret is placed at the end of the text.</span></span>

-   <span data-ttu-id="c20cc-216">**Usare sempre una casella di testo a più righe se i caratteri di nuova riga sono input validi.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-216">**Always use a multi-line text box if new-line characters are valid input.**</span></span>
-   <span data-ttu-id="c20cc-217">**Quando la casella di testo è per un file o un percorso, fornire sempre un pulsante Sfoglia.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-217">**When the text box is for a file or path, always provide a Browse button.**</span></span>

### <a name="numeric-text-boxes"></a><span data-ttu-id="c20cc-218">Caselle di testo numerici</span><span class="sxs-lookup"><span data-stu-id="c20cc-218">Numeric text boxes</span></span>

-   <span data-ttu-id="c20cc-219">**Scegliere l'unità più pratica ed etichettare le unità.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-219">**Choose the most convenient unit and label the units.**</span></span> <span data-ttu-id="c20cc-220">Si supponga, ad esempio, di usare millilitri anziché litri (o viceversa), percentuali anziché valori diretti (o viceversa) e così via.</span><span class="sxs-lookup"><span data-stu-id="c20cc-220">For example, consider using milliliters instead of liters (or vice versa), percentages instead of direct values (or vice versa), and so on.</span></span>

    <span data-ttu-id="c20cc-221">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-221">**Correct:**</span></span>

    ![<span data-ttu-id="c20cc-222">screenshot della casella di testo con litri come unità</span><span class="sxs-lookup"><span data-stu-id="c20cc-222">screen shot of text box with liters as unit</span></span> ](images/ctrl-text-boxes-image17.png)

    <span data-ttu-id="c20cc-223">In questo esempio, l'unità viene etichettata, ma è necessario che gli utenti immettano numeri decimali.</span><span class="sxs-lookup"><span data-stu-id="c20cc-223">In this example, the unit is labeled, but it requires users to enter decimal numbers.</span></span>

    <span data-ttu-id="c20cc-224">**Migliore:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-224">**Better:**</span></span>

    ![<span data-ttu-id="c20cc-225">screenshot della casella di testo con millilitri come unità</span><span class="sxs-lookup"><span data-stu-id="c20cc-225">screen shot of text box with milliliters as unit</span></span> ](images/ctrl-text-boxes-image18.png)

    <span data-ttu-id="c20cc-226">In questo esempio, la casella di testo usa un'unità più pratica.</span><span class="sxs-lookup"><span data-stu-id="c20cc-226">In this example, the text box uses a more convenient unit.</span></span>

-   <span data-ttu-id="c20cc-227">**Utilizzare un controllo di selezione ogni volta che è utile.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-227">**Use a spin control whenever it is helpful.**</span></span> <span data-ttu-id="c20cc-228">Tuttavia, a volte i controlli di selezione non sono pratici, ad esempio quando gli utenti devono immettere molti numeri elevati.</span><span class="sxs-lookup"><span data-stu-id="c20cc-228">However, sometimes spin controls aren't practical, such as when users need to enter many large numbers.</span></span> <span data-ttu-id="c20cc-229">Usare i controlli di selezione nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c20cc-229">Use spin controls when:</span></span>
    -   <span data-ttu-id="c20cc-230">È probabile che l'input sia un numero ridotto, in genere inferiore a 100.</span><span class="sxs-lookup"><span data-stu-id="c20cc-230">The input is likely to be a small number, typically under 100.</span></span>
    -   <span data-ttu-id="c20cc-231">È probabile che gli utenti apporteranno una piccola modifica a un numero esistente.</span><span class="sxs-lookup"><span data-stu-id="c20cc-231">Users are likely to make a small change to an existing number.</span></span>
    -   <span data-ttu-id="c20cc-232">È più probabile che gli utenti utilizzino il mouse anziché la tastiera.</span><span class="sxs-lookup"><span data-stu-id="c20cc-232">Users are more likely to be using the mouse than the keyboard.</span></span>
-   <span data-ttu-id="c20cc-233">**Allinea a destra il testo numerico ogni volta che:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-233">**Right-align numeric text whenever:**</span></span>

    -   <span data-ttu-id="c20cc-234">È presente più di una casella di testo numerica.</span><span class="sxs-lookup"><span data-stu-id="c20cc-234">There is more than one numeric text box.</span></span>
    -   <span data-ttu-id="c20cc-235">Le caselle di testo sono allineate verticalmente.</span><span class="sxs-lookup"><span data-stu-id="c20cc-235">The text boxes are vertically aligned.</span></span>
    -   <span data-ttu-id="c20cc-236">È probabile che gli utenti aggiungano o confrontino i valori.</span><span class="sxs-lookup"><span data-stu-id="c20cc-236">Users are likely to add or compare the values.</span></span>

    <span data-ttu-id="c20cc-237">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-237">**Correct:**</span></span>

    ![<span data-ttu-id="c20cc-238">screenshot delle caselle di testo spese (Hotel e così via)</span><span class="sxs-lookup"><span data-stu-id="c20cc-238">screen shot of expenses text boxes (hotel, etc.)</span></span> ](images/ctrl-text-boxes-image19.png)

    <span data-ttu-id="c20cc-239">In questo esempio il testo numerico è allineato a destra per facilitare il confronto dei valori.</span><span class="sxs-lookup"><span data-stu-id="c20cc-239">In this example, the numeric text is right-aligned to make it easy to compare values.</span></span>

    <span data-ttu-id="c20cc-240">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-240">**Incorrect:**</span></span>

    ![<span data-ttu-id="c20cc-241">screenshot delle caselle di testo per i valori RGB</span><span class="sxs-lookup"><span data-stu-id="c20cc-241">screen shot of text boxes for rgb values</span></span> ](images/ctrl-text-boxes-image20.png)

    <span data-ttu-id="c20cc-242">In questo esempio il testo numerico è allineato in modo non corretto.</span><span class="sxs-lookup"><span data-stu-id="c20cc-242">In this example, the numeric text is incorrectly left-aligned.</span></span>

-   <span data-ttu-id="c20cc-243">**Allinea sempre a destra i valori monetari.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-243">**Always right-align monetary values.**</span></span>
-   <span data-ttu-id="c20cc-244">**Non assegnare significati speciali a valori numerici specifici**, anche se questi significati speciali vengono usati internamente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c20cc-244">**Don't assign special meanings to specific numeric values**, even if those special meanings are used internally by your application.</span></span> <span data-ttu-id="c20cc-245">Usare invece caselle di controllo o pulsanti di opzione per una selezione esplicita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c20cc-245">Instead, use check boxes or radio buttons for an explicit user selection.</span></span>

    <span data-ttu-id="c20cc-246">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-246">**Incorrect:**</span></span>

    ![<span data-ttu-id="c20cc-247">screenshot dell'etichetta: usare-1 per disabilitare la memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="c20cc-247">screen shot of label: use -1 to disable caching</span></span> ](images/ctrl-text-boxes-image21.png)

    <span data-ttu-id="c20cc-248">In questo esempio, il valore-1 ha un significato speciale.</span><span class="sxs-lookup"><span data-stu-id="c20cc-248">In this example, the value -1 has a special meaning.</span></span>

    <span data-ttu-id="c20cc-249">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-249">**Correct:**</span></span>

    ![<span data-ttu-id="c20cc-250">screenshot dell'etichetta della casella di controllo: Caching</span><span class="sxs-lookup"><span data-stu-id="c20cc-250">screen shot of check box label: caching</span></span> ](images/ctrl-text-boxes-image22.png)

    <span data-ttu-id="c20cc-251">In questo esempio, una casella di controllo rende esplicita l'opzione.</span><span class="sxs-lookup"><span data-stu-id="c20cc-251">In this example, a check box makes the option explicit.</span></span>

### <a name="password-and-pin-input"></a><span data-ttu-id="c20cc-252">Input di password e PIN</span><span class="sxs-lookup"><span data-stu-id="c20cc-252">Password and PIN input</span></span>

-   <span data-ttu-id="c20cc-253">**Usare sempre il controllo comune password anziché crearne di personalizzati.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-253">**Always use the password common control instead of creating your own.**</span></span> <span data-ttu-id="c20cc-254">Le password e i pin richiedono un trattamento speciale per essere gestiti in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="c20cc-254">Passwords and PINs require special treatment to be handled securely.</span></span>

<span data-ttu-id="c20cc-255">Per altre linee guida ed esempi, vedere [Balloons](ctrl-balloons.md).</span><span class="sxs-lookup"><span data-stu-id="c20cc-255">For more guidelines and examples, see [Balloons](ctrl-balloons.md).</span></span>

### <a name="textual-output"></a><span data-ttu-id="c20cc-256">Output testuale</span><span class="sxs-lookup"><span data-stu-id="c20cc-256">Textual output</span></span>

-   <span data-ttu-id="c20cc-257">**Si consiglia di usare il colore di sistema in background bianco per il testo di sola lettura su larga linea e su più righe.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-257">**Consider using the white background system color for large, multi-line read-only text.**</span></span> <span data-ttu-id="c20cc-258">Uno sfondo bianco rende il testo più semplice da leggere.</span><span class="sxs-lookup"><span data-stu-id="c20cc-258">A white background makes the text easier to read.</span></span> <span data-ttu-id="c20cc-259">Molti testi su uno sfondo grigio sconsigliano la lettura.</span><span class="sxs-lookup"><span data-stu-id="c20cc-259">Lots of text on a gray background discourages reading.</span></span>

<span data-ttu-id="c20cc-260">Per ulteriori informazioni sui colori di sfondo, vedere [tipi di carattere](vis-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="c20cc-260">For more information on background colors, see [Fonts](vis-fonts.md).</span></span>

### <a name="data-output"></a><span data-ttu-id="c20cc-261">Output dei dati</span><span class="sxs-lookup"><span data-stu-id="c20cc-261">Data output</span></span>

-   <span data-ttu-id="c20cc-262">**Non usare un bordo per le caselle di testo a riga singola e di sola lettura.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-262">**Don't use a border for single-line, read-only text boxes.**</span></span> <span data-ttu-id="c20cc-263">Il bordo è un indizio visivo che il testo è modificabile.</span><span class="sxs-lookup"><span data-stu-id="c20cc-263">The border is a visual clue that the text is editable.</span></span>
-   <span data-ttu-id="c20cc-264">**Non disabilitare le caselle di testo di sola lettura a riga singola.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-264">**Don't disable single-line, read-only text boxes.**</span></span> <span data-ttu-id="c20cc-265">In questo modo si impedisce agli utenti di selezionare e copiare il testo negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="c20cc-265">This prevents users from selecting and copying the text to the clipboard.</span></span> <span data-ttu-id="c20cc-266">Impedisce inoltre agli utenti di scorrere i dati se superano le dimensioni dei relativi limiti.</span><span class="sxs-lookup"><span data-stu-id="c20cc-266">It also prevents users from scrolling the data if it exceeds the size of its boundaries.</span></span>
-   <span data-ttu-id="c20cc-267">**Non impostare una tabulazione su una sola riga di testo di sola lettura, a meno che non sia probabile che l'utente debba scorrere o copiare il testo.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-267">**Don't set a tab stop on single-line, read-only text box unless the user is likely to need to scroll or copy the text.**</span></span>

## <a name="input-validation-and-error-handling"></a><span data-ttu-id="c20cc-268">Convalida degli input e gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="c20cc-268">Input validation and error handling</span></span>

<span data-ttu-id="c20cc-269">Poiché le caselle di testo non sono in genere vincolate ad accettare solo un input valido, potrebbe essere necessario convalidare l'input e gestire eventuali problemi.</span><span class="sxs-lookup"><span data-stu-id="c20cc-269">Because text boxes are usually not constrained to accept only valid input, you may need to validate the input and handle any problems.</span></span> <span data-ttu-id="c20cc-270">Convalidare i vari tipi di problemi di input come segue:</span><span class="sxs-lookup"><span data-stu-id="c20cc-270">Validate the various types of input problems as follows:</span></span>

-   <span data-ttu-id="c20cc-271">Se l'utente immette un carattere non valido, ignorare il carattere e visualizzare un fumetto di un [problema di input](ctrl-balloons.md) che illustra i caratteri validi.</span><span class="sxs-lookup"><span data-stu-id="c20cc-271">If the user enters a character that isn't valid, ignore the character and display an [input problem balloon](ctrl-balloons.md) that explains the valid characters.</span></span>

    ![screenshot della casella di testo del codice Product Key](images/ctrl-text-boxes-image23.png)

    <span data-ttu-id="c20cc-273">In questo esempio un fumetto segnala un carattere di input non corretto.</span><span class="sxs-lookup"><span data-stu-id="c20cc-273">In this example, a balloon reports an incorrect input character.</span></span>

-   <span data-ttu-id="c20cc-274">Se i dati di input hanno un valore o un formato non valido, visualizzare un fumetto di problema di input quando la casella di testo perde lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="c20cc-274">If the input data has a value or format that isn't valid, display an input problem balloon when the text box loses input focus.</span></span>
-   <span data-ttu-id="c20cc-275">Se i dati di input non sono coerenti con altri controlli della finestra, fornire un messaggio di errore quando l'intero input è completo, ad esempio quando gli utenti fanno clic su OK per una finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="c20cc-275">If the input data is inconsistent with other controls on the window, give an error message when the entire input is complete, such as when users click OK for a modal dialog box.</span></span>

<span data-ttu-id="c20cc-276">**Non cancellare i dati di input non validi a meno che gli utenti non siano in grado di correggere facilmente gli errori.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-276">**Don't clear invalid input data unless users aren't able to correct errors easily.**</span></span> <span data-ttu-id="c20cc-277">Questa operazione consente agli utenti di correggere gli errori senza ricominciare.</span><span class="sxs-lookup"><span data-stu-id="c20cc-277">Doing so allows users to correct mistakes without starting over.</span></span> <span data-ttu-id="c20cc-278">Ad esempio, è consigliabile cancellare le password e i pin non corretti perché gli utenti non possono correggerli facilmente.</span><span class="sxs-lookup"><span data-stu-id="c20cc-278">For example, you should clear incorrect passwords and PINs because users can't correct them easily.</span></span>

<span data-ttu-id="c20cc-279">Per altre linee guida ed esempi, vedere [messaggi di errore](mess-error.md) e [palloncini](ctrl-balloons.md).</span><span class="sxs-lookup"><span data-stu-id="c20cc-279">For more guidelines and examples, see [Error Messages](mess-error.md) and [Balloons](ctrl-balloons.md).</span></span>

## <a name="prompts"></a><span data-ttu-id="c20cc-280">Prompt</span><span class="sxs-lookup"><span data-stu-id="c20cc-280">Prompts</span></span>

<span data-ttu-id="c20cc-281">Un messaggio di richiesta è un'etichetta o un'istruzione breve posizionata all'interno di una casella di testo come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c20cc-281">A prompt is a label or short instruction placed inside a text box as its default value.</span></span> <span data-ttu-id="c20cc-282">A differenza del testo statico, i messaggi di richiesta scompaiono dallo schermo una volta che gli utenti digitano qualcosa nella casella di testo o ottengono lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="c20cc-282">Unlike static text, prompts disappear from the screen once users type something into the text box or it gets input focus.</span></span>

![<span data-ttu-id="c20cc-283">screenshot della casella di testo della richiesta con etichetta: ricerca</span><span class="sxs-lookup"><span data-stu-id="c20cc-283">screen shot of prompt text box with label: search</span></span> ](images/ctrl-text-boxes-image24.png)

<span data-ttu-id="c20cc-284">Un prompt tipico.</span><span class="sxs-lookup"><span data-stu-id="c20cc-284">A typical prompt.</span></span>

<span data-ttu-id="c20cc-285">Usare un prompt nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c20cc-285">Use a prompt when:</span></span>

-   <span data-ttu-id="c20cc-286">Lo spazio dello schermo è a un livello superiore che l'uso di un'etichetta o di un'istruzione è indesiderato, ad esempio su una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="c20cc-286">Screen space is at such a premium that using a label or instruction is undesirable, such as on a toolbar.</span></span>
-   <span data-ttu-id="c20cc-287">Il prompt è principalmente per identificare lo scopo della casella di testo in modo compatto.</span><span class="sxs-lookup"><span data-stu-id="c20cc-287">The prompt is primarily for identifying the purpose of the text box in a compact way.</span></span> <span data-ttu-id="c20cc-288">Non devono essere informazioni cruciali che l'utente deve visualizzare durante l'uso della casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-288">It must not be crucial information that the user needs to see while using the text box.</span></span>

<span data-ttu-id="c20cc-289">Non usare i prompt solo per indicare agli utenti di digitare qualcosa o fare clic sui pulsanti.</span><span class="sxs-lookup"><span data-stu-id="c20cc-289">Don't use prompts just to direct users to type something or to click buttons.</span></span> <span data-ttu-id="c20cc-290">Ad esempio, non scrivere testo della richiesta di conferma immettere un nome file e quindi fare clic su Invia.</span><span class="sxs-lookup"><span data-stu-id="c20cc-290">For example, don't write prompt text that says Enter a filename and then click Send.</span></span>

<span data-ttu-id="c20cc-291">Quando si usano i prompt:</span><span class="sxs-lookup"><span data-stu-id="c20cc-291">When using prompts:</span></span>

-   <span data-ttu-id="c20cc-292">Creare il testo della richiesta in grigio corsivo e il testo di input effettivo in nero normale.</span><span class="sxs-lookup"><span data-stu-id="c20cc-292">Draw the prompt text in italic gray and the actual input text in normal black.</span></span> <span data-ttu-id="c20cc-293">Il testo della richiesta non deve essere confuso con il testo reale.</span><span class="sxs-lookup"><span data-stu-id="c20cc-293">The prompt text must not be confused with real text.</span></span>
-   <span data-ttu-id="c20cc-294">Conserva il testo della richiesta conciso.</span><span class="sxs-lookup"><span data-stu-id="c20cc-294">Keep the prompt text concise.</span></span> <span data-ttu-id="c20cc-295">È possibile utilizzare frammenti anziché frasi complete.</span><span class="sxs-lookup"><span data-stu-id="c20cc-295">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="c20cc-296">Usare le maiuscole/minuscole come nelle frasi comuni.</span><span class="sxs-lookup"><span data-stu-id="c20cc-296">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="c20cc-297">Non usare la punteggiatura finale o i puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="c20cc-297">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="c20cc-298">Il testo della richiesta non deve essere modificabile e dovrebbe scomparire quando gli utenti fanno clic nella casella di testo o nella scheda.</span><span class="sxs-lookup"><span data-stu-id="c20cc-298">The prompt text should not be editable and should disappear once users click in or tab into the text box.</span></span>
    -   <span data-ttu-id="c20cc-299">**Eccezione:** Se la casella di testo ha lo stato attivo per l'input predefinito, il prompt viene visualizzato e scompare una volta che l'utente inizia a digitare.</span><span class="sxs-lookup"><span data-stu-id="c20cc-299">**Exception:** If the text box has default input focus, the prompt is displayed, and it disappears once the user starts typing.</span></span>
-   <span data-ttu-id="c20cc-300">Il testo della richiesta viene ripristinato se la casella di testo è ancora vuota quando perde lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="c20cc-300">The prompt text is restored if the text box is still empty when it loses input focus.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="c20cc-301">Ridimensionamento e spaziatura consigliati</span><span class="sxs-lookup"><span data-stu-id="c20cc-301">Recommended sizing and spacing</span></span>

![<span data-ttu-id="c20cc-302">Figura di caselle di testo a riga singola e a due righe</span><span class="sxs-lookup"><span data-stu-id="c20cc-302">figure of one-line and two-line text boxes</span></span> ](images/ctrl-text-boxes-image25.png)

<span data-ttu-id="c20cc-303">Ridimensionamento e spaziatura consigliati per le caselle di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-303">Recommended sizing and spacing for text boxes.</span></span>

<span data-ttu-id="c20cc-304">La larghezza di una casella di testo è un indizio visivo delle dimensioni di input previste.</span><span class="sxs-lookup"><span data-stu-id="c20cc-304">The width of a text box is a visual clue of the expected input size.</span></span> <span data-ttu-id="c20cc-305">Quando si ridimensionano le caselle di testo:</span><span class="sxs-lookup"><span data-stu-id="c20cc-305">When sizing text boxes:</span></span>

-   <span data-ttu-id="c20cc-306">**Scegliere una larghezza appropriata per i dati più lunghi validi.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-306">**Choose a width appropriate for the longest valid data.**</span></span> <span data-ttu-id="c20cc-307">Nella maggior parte dei casi, gli utenti non dovrebbero dover scorrere la stringa più probabile che entreranno o visualizzano.</span><span class="sxs-lookup"><span data-stu-id="c20cc-307">In most situations, users shouldn't have to scroll the longest likely string they'll enter or view.</span></span>
-   <span data-ttu-id="c20cc-308">**Includere un ulteriore 30%** (fino al 200% per un testo più breve) per qualsiasi testo (ma non per i numeri) che verrà localizzato.</span><span class="sxs-lookup"><span data-stu-id="c20cc-308">**Include an additional 30 percent** (up to 200 percent for shorter text) for any text (but not numbers) that will be localized.</span></span>
-   <span data-ttu-id="c20cc-309">**Se l'input previsto non ha dimensioni particolari, scegliere una larghezza coerente con le altre caselle di testo o i controlli della finestra.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-309">**If the expected input has no particular size, choose a width that is consistent with the other text boxes or controls on the window.**</span></span>
-   <span data-ttu-id="c20cc-310">**Ridimensiona le caselle di testo su più righe per visualizzare un numero integrale di righe di testo.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-310">**Size multi-line text boxes to display an integral number of lines of text.**</span></span>

## <a name="labels"></a><span data-ttu-id="c20cc-311">Etichette</span><span class="sxs-lookup"><span data-stu-id="c20cc-311">Labels</span></span>

### <a name="text-box-labels"></a><span data-ttu-id="c20cc-312">Etichette casella di testo</span><span class="sxs-lookup"><span data-stu-id="c20cc-312">Text box labels</span></span>

-   <span data-ttu-id="c20cc-313">Tutte le caselle di testo necessitano di etichette.</span><span class="sxs-lookup"><span data-stu-id="c20cc-313">All text boxes need labels.</span></span> <span data-ttu-id="c20cc-314">Scrivere l'etichetta come una parola o una frase, non come una frase, terminando con i due punti e usando il [testo statico](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c20cc-314">Write the label as a word or phrase, not as a sentence, ending with a colon, and using [static text](glossary.md).</span></span>

    <span data-ttu-id="c20cc-315">**Eccezioni**</span><span class="sxs-lookup"><span data-stu-id="c20cc-315">**Exceptions:**</span></span>

    -   <span data-ttu-id="c20cc-316">Caselle di testo con prompt in cui lo spazio è disponibile a un livello Premium.</span><span class="sxs-lookup"><span data-stu-id="c20cc-316">Text boxes with prompts located where space is at a premium.</span></span>
    -   <span data-ttu-id="c20cc-317">Per l'assegnazione di etichette, un gruppo di caselle di testo utilizzate per l' **input di dati formattati** deve essere considerato come una singola casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-317">For labeling, a group of text boxes used for **formatted data input** should be treated as a single text box.</span></span>
    -   <span data-ttu-id="c20cc-318">Se una casella di testo è subordinata a un pulsante di opzione o a una casella di controllo e viene introdotta dall'etichetta che termina con i due punti, non inserire un'etichetta aggiuntiva nella casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-318">If a text box is subordinate to a radio button or check box, and is introduced by its label ending with a colon, don't put an additional label on the text box.</span></span>
    -   <span data-ttu-id="c20cc-319">**Omettere le etichette dei controlli che riportano l'istruzione principale.**</span><span class="sxs-lookup"><span data-stu-id="c20cc-319">**Omit control labels that restate the main instruction.**</span></span> <span data-ttu-id="c20cc-320">In questo caso, l'istruzione principale accetta i due punti, a meno che non si tratti di una domanda, e la chiave di accesso.</span><span class="sxs-lookup"><span data-stu-id="c20cc-320">In this case, the main instruction takes the colon (unless it's a question) and access key.</span></span>

        <span data-ttu-id="c20cc-321">**Accettabile:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-321">**Acceptable:**</span></span>

        ![screenshot della casella di testo con etichetta ripetitiva](images/ctrl-text-boxes-image26.png)

        <span data-ttu-id="c20cc-323">In questo esempio, l'etichetta della casella di testo è semplicemente una ripubblicazione dell'istruzione principale.</span><span class="sxs-lookup"><span data-stu-id="c20cc-323">In this example, the text box label is just a restatement of the main instruction.</span></span>

        <span data-ttu-id="c20cc-324">**Migliore:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-324">**Better:**</span></span>

        ![<span data-ttu-id="c20cc-325">screenshot della casella di testo con solo istruzione principale</span><span class="sxs-lookup"><span data-stu-id="c20cc-325">screen shot of text box with main instruction only</span></span> ](images/ctrl-text-boxes-image27.png)

        <span data-ttu-id="c20cc-326">In questo esempio, l'etichetta ridondante viene rimossa, quindi l'istruzione principale accetta i due punti e la chiave di accesso.</span><span class="sxs-lookup"><span data-stu-id="c20cc-326">In this example, the redundant label is removed, so the main instruction takes the colon and access key.</span></span>

-   <span data-ttu-id="c20cc-327">Assegnare una chiave di accesso univoca.</span><span class="sxs-lookup"><span data-stu-id="c20cc-327">Assign a unique access key.</span></span> <span data-ttu-id="c20cc-328">Per le linee guida per l'assegnazione delle chiavi di accesso, vedere [tastiera](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="c20cc-328">For access key assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="c20cc-329">Usare le maiuscole/minuscole come nelle frasi comuni.</span><span class="sxs-lookup"><span data-stu-id="c20cc-329">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="c20cc-330">Posizionare l'etichetta a sinistra o sopra la casella di testo e allineare l'etichetta al bordo sinistro della casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-330">Position the label either to the left of or above the text box, and align the label with the left edge of the text box.</span></span> <span data-ttu-id="c20cc-331">Se l'etichetta è a sinistra, allineare verticalmente il testo dell'etichetta con il testo della casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-331">If the label is on the left, vertically align the label text with the text box text.</span></span>

    <span data-ttu-id="c20cc-332">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-332">**Correct:**</span></span>

    ![<span data-ttu-id="c20cc-333">screenshot dell'etichetta allineata a sinistra sopra la casella di testo</span><span class="sxs-lookup"><span data-stu-id="c20cc-333">screen shot of left-aligned label above text box</span></span> ](images/ctrl-text-boxes-image28.png)

    ![<span data-ttu-id="c20cc-334">screenshot dell'etichetta allineata al testo a sinistra della casella di testo</span><span class="sxs-lookup"><span data-stu-id="c20cc-334">screen shot of text-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image29.png)

    <span data-ttu-id="c20cc-335">In questi esempi, l'etichetta nella parte superiore si allinea al bordo sinistro della casella di testo e l'etichetta a sinistra viene allineata al testo nella casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-335">In these examples, the label on top aligns with the left edge of the text box, and the label on the left aligns with the text in the text box.</span></span>

    <span data-ttu-id="c20cc-336">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-336">**Incorrect:**</span></span>

    ![<span data-ttu-id="c20cc-337">screenshot dell'etichetta allineata al testo sopra la casella di testo</span><span class="sxs-lookup"><span data-stu-id="c20cc-337">screen shot of text-aligned label above text box</span></span> ](images/ctrl-text-boxes-image30.png)

    ![<span data-ttu-id="c20cc-338">screenshot dell'etichetta allineata in alto a sinistra della casella di testo</span><span class="sxs-lookup"><span data-stu-id="c20cc-338">screen shot of top-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image31.png)

    <span data-ttu-id="c20cc-339">In questi esempi non corretti, l'etichetta nella parte superiore viene allineata al testo nella casella di testo e l'etichetta a sinistra viene allineata alla parte superiore della casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-339">In these incorrect examples, the label on top aligns with the text in the text box, and the label on the left aligns with the top of the text box.</span></span>

-   <span data-ttu-id="c20cc-340">È possibile specificare unità (ad esempio, secondi o connessioni) tra parentesi dopo l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="c20cc-340">You may specify units (for example, seconds or connections) in parentheses after the label.</span></span>
-   <span data-ttu-id="c20cc-341">Se una casella di testo accetta un numero massimo di caratteri arbitrariamente ridotto, è possibile indicare l'input massimo nell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="c20cc-341">If a text box accepts an arbitrarily small maximum number of characters, you can state the maximum input in the label.</span></span> <span data-ttu-id="c20cc-342">La larghezza della casella di testo suggerisce anche le dimensioni massime.</span><span class="sxs-lookup"><span data-stu-id="c20cc-342">The text box width should also suggest the maximum size.</span></span>

    ![<span data-ttu-id="c20cc-343">screenshot della casella di testo password</span><span class="sxs-lookup"><span data-stu-id="c20cc-343">screen shot of password text box</span></span> ](images/ctrl-text-boxes-image32.png)

    <span data-ttu-id="c20cc-344">In questo esempio, l'etichetta indica il numero massimo di caratteri.</span><span class="sxs-lookup"><span data-stu-id="c20cc-344">In this example, the label gives the maximum number of characters.</span></span>

-   <span data-ttu-id="c20cc-345">Non fare in modo che il contenuto della casella di testo (o etichetta unità) faccia parte di una frase, perché non è localizzabile.</span><span class="sxs-lookup"><span data-stu-id="c20cc-345">Don't make the content of the text box (or its units label) part of a sentence, because this is not localizable.</span></span>
-   <span data-ttu-id="c20cc-346">Se è possibile usare la casella di testo per immettere diversi elementi, deselezionare la modalità di separazione degli elementi nell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="c20cc-346">If the text box can be used to enter several items, make it clear how to separate the items in the label.</span></span>

    ![<span data-ttu-id="c20cc-347">screenshot dei nomi separati dall'etichetta con punto e virgola</span><span class="sxs-lookup"><span data-stu-id="c20cc-347">screen shot of label separate names with semicolon</span></span> ](images/ctrl-text-boxes-image33.png)

    <span data-ttu-id="c20cc-348">In questo esempio, il separatore di elementi viene specificato nell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="c20cc-348">In this example, the item separator is given in the label.</span></span>

-   <span data-ttu-id="c20cc-349">Per linee guida su come indicare l'input richiesto, vedere input obbligatorio nelle [finestre di dialogo](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="c20cc-349">For guidelines on indicating required input, see Required input in [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="instruction-labels"></a><span data-ttu-id="c20cc-350">Etichette di istruzioni</span><span class="sxs-lookup"><span data-stu-id="c20cc-350">Instruction labels</span></span>

-   <span data-ttu-id="c20cc-351">Se è necessario aggiungere testo di istruzioni su una casella di testo, aggiungerla sopra l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="c20cc-351">If you need to add instructional text about a text box, add it above the label.</span></span> <span data-ttu-id="c20cc-352">Utilizzare frasi complete con la punteggiatura finale.</span><span class="sxs-lookup"><span data-stu-id="c20cc-352">Use complete sentences with ending punctuation.</span></span>
-   <span data-ttu-id="c20cc-353">Usare le maiuscole/minuscole come nelle frasi comuni.</span><span class="sxs-lookup"><span data-stu-id="c20cc-353">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="c20cc-354">Informazioni aggiuntive utili ma non necessarie devono essere mantenute brevi.</span><span class="sxs-lookup"><span data-stu-id="c20cc-354">Additional information that is helpful but not necessary should be kept short.</span></span> <span data-ttu-id="c20cc-355">Inserire queste informazioni tra parentesi tra l'etichetta e i due punti o senza parentesi sotto la casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-355">Place this information either in parentheses between the label and colon, or without parentheses below the text box.</span></span>

    ![<span data-ttu-id="c20cc-356">screenshot delle informazioni aggiunte sotto la casella di testo</span><span class="sxs-lookup"><span data-stu-id="c20cc-356">screen shot of added information below text box</span></span> ](images/ctrl-text-boxes-image34.png)

    <span data-ttu-id="c20cc-357">In questo esempio, le informazioni aggiuntive vengono posizionate sotto la casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-357">In this example, additional information is placed below the text box.</span></span>

### <a name="prompt-labels"></a><span data-ttu-id="c20cc-358">Etichette dei messaggi di richiesta</span><span class="sxs-lookup"><span data-stu-id="c20cc-358">Prompt labels</span></span>

-   <span data-ttu-id="c20cc-359">Conserva il testo della richiesta conciso.</span><span class="sxs-lookup"><span data-stu-id="c20cc-359">Keep the prompt text concise.</span></span> <span data-ttu-id="c20cc-360">È possibile utilizzare frammenti anziché frasi complete.</span><span class="sxs-lookup"><span data-stu-id="c20cc-360">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="c20cc-361">Usare le maiuscole/minuscole come nelle frasi comuni.</span><span class="sxs-lookup"><span data-stu-id="c20cc-361">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="c20cc-362">Non usare la punteggiatura finale o i puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="c20cc-362">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="c20cc-363">Se il prompt indica agli utenti di immettere informazioni che verranno eseguite da un pulsante accanto alla casella di testo, è sufficiente posizionare il pulsante accanto alla casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-363">If the prompt directs users to enter information that will be acted upon by a button next to the text box, simply place the button next to the text box.</span></span> <span data-ttu-id="c20cc-364">Non usare il prompt per indirizzare gli utenti a fare clic sul pulsante (ad esempio, non scrivere il testo della richiesta, trascinare un file e quindi fare clic su Invia).</span><span class="sxs-lookup"><span data-stu-id="c20cc-364">Don't use the prompt to direct users to click the button (for example, don't write prompt text that says, Drag a file and then click Send).</span></span>

## <a name="documentation"></a><span data-ttu-id="c20cc-365">Documentazione</span><span class="sxs-lookup"><span data-stu-id="c20cc-365">Documentation</span></span>

<span data-ttu-id="c20cc-366">Quando si fa riferimento alle caselle di testo:</span><span class="sxs-lookup"><span data-stu-id="c20cc-366">When referring to text boxes:</span></span>

-   <span data-ttu-id="c20cc-367">Usare il tipo per fare riferimento a interazioni utente che richiedono la digitazione o incolla; in caso contrario, utilizzare invio se gli utenti possono inserire informazioni nella casella di testo utilizzando altri metodi, ad esempio selezionando il valore da un elenco o utilizzando un pulsante Sfoglia.</span><span class="sxs-lookup"><span data-stu-id="c20cc-367">Use type to refer to user interactions that require typing or pasting; otherwise use enter if users can put information into the text box using other means, such as selecting the value from a list or using a Browse button.</span></span>
-   <span data-ttu-id="c20cc-368">Usare SELECT per fare riferimento a una voce in una casella di testo di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c20cc-368">Use select to refer to an entry in a read-only text box.</span></span>
-   <span data-ttu-id="c20cc-369">Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, e includere la parola box.</span><span class="sxs-lookup"><span data-stu-id="c20cc-369">Use the exact label text, including its capitalization, and include the word box.</span></span> <span data-ttu-id="c20cc-370">Non includere il carattere di sottolineatura della chiave di accesso o i due punti.</span><span class="sxs-lookup"><span data-stu-id="c20cc-370">Don't include the access key underscore or colon.</span></span> <span data-ttu-id="c20cc-371">Non fare riferimento a una casella di testo come una casella di testo o un campo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-371">Don't refer to a text box as a text box or a field.</span></span>
-   <span data-ttu-id="c20cc-372">Quando possibile, formattare l'etichetta usando il testo in grassetto.</span><span class="sxs-lookup"><span data-stu-id="c20cc-372">When possible, format the label using bold text.</span></span> <span data-ttu-id="c20cc-373">In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.</span><span class="sxs-lookup"><span data-stu-id="c20cc-373">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

    <span data-ttu-id="c20cc-374">Esempio: digitare la password nella casella **password** e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c20cc-374">Example: Type your password into the **Password** box, and then click **OK**.</span></span>

-   <span data-ttu-id="c20cc-375">Se la casella di testo richiede un formato specifico, documentare solo il formato accettabile usato più di frequente.</span><span class="sxs-lookup"><span data-stu-id="c20cc-375">If the text box requires a specific format, document only the most commonly used acceptable format.</span></span> <span data-ttu-id="c20cc-376">Consentire agli utenti di individuare altri formati in modo autonomo.</span><span class="sxs-lookup"><span data-stu-id="c20cc-376">Let users discover any other formats on their own.</span></span> <span data-ttu-id="c20cc-377">Si desidera essere flessibili con i formati di dati, ma questa operazione non dovrebbe produrre una documentazione complessa.</span><span class="sxs-lookup"><span data-stu-id="c20cc-377">You want to be flexible with data formats, but doing so should not result in complex documentation.</span></span>

    <span data-ttu-id="c20cc-378">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-378">**Correct:**</span></span>

    <span data-ttu-id="c20cc-379">Immettere il numero di serie della parte usando il formato 1234-56-7890.</span><span class="sxs-lookup"><span data-stu-id="c20cc-379">Enter the part's serial number using the 1234-56-7890 format.</span></span>

    <span data-ttu-id="c20cc-380">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="c20cc-380">**Incorrect:**</span></span>

    <span data-ttu-id="c20cc-381">Immettere il numero di serie della parte usando uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="c20cc-381">Enter the part's serial number using any of the following formats:</span></span>

    <span data-ttu-id="c20cc-382">1234567890</span><span class="sxs-lookup"><span data-stu-id="c20cc-382">1234567890</span></span>

    <span data-ttu-id="c20cc-383">1234-56-7890</span><span class="sxs-lookup"><span data-stu-id="c20cc-383">1234-56-7890</span></span>

    <span data-ttu-id="c20cc-384">1234 56 7890</span><span class="sxs-lookup"><span data-stu-id="c20cc-384">1234 56 7890</span></span>

