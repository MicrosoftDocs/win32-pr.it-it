---
title: Messaggi di avviso
description: Un messaggio di avviso è una finestra di dialogo modale, un messaggio sul posto, una notifica o un fumetto che avvisa l'utente di una condizione che potrebbe causare un problema in futuro.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d704890b2471e205b933e2995950716c269488e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351086"
---
# <a name="warning-messages"></a><span data-ttu-id="9cec3-103">Messaggi di avviso</span><span class="sxs-lookup"><span data-stu-id="9cec3-103">Warning Messages</span></span>

> [!NOTE]
> <span data-ttu-id="9cec3-104">Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="9cec3-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="9cec3-105">Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="9cec3-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="9cec3-106">Un messaggio di avviso è una finestra di dialogo modale, un messaggio sul posto, una notifica o un fumetto che avvisa l'utente di una condizione che potrebbe causare un problema in futuro.</span><span class="sxs-lookup"><span data-stu-id="9cec3-106">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span>

![Screenshot di un messaggio di avviso tipico](images/mess-warn-image1.png)

<span data-ttu-id="9cec3-108">Un messaggio di avviso modale tipico.</span><span class="sxs-lookup"><span data-stu-id="9cec3-108">A typical modal warning message.</span></span>

<span data-ttu-id="9cec3-109">La caratteristica fondamentale degli avvisi è che coinvolgono il rischio di perdita di uno o più dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="9cec3-109">The fundamental characteristic of warnings is that they involve the risk of losing one or more of the following:</span></span>

-   <span data-ttu-id="9cec3-110">Una risorsa preziosa, ad esempio dati finanziari o altri dati importanti.</span><span class="sxs-lookup"><span data-stu-id="9cec3-110">A valuable asset, such as important financial or other data.</span></span>
-   <span data-ttu-id="9cec3-111">Accesso al sistema o integrità.</span><span class="sxs-lookup"><span data-stu-id="9cec3-111">System access or integrity.</span></span>
-   <span data-ttu-id="9cec3-112">Privacy o controllo sulle informazioni riservate.</span><span class="sxs-lookup"><span data-stu-id="9cec3-112">Privacy or control over confidential information.</span></span>
-   <span data-ttu-id="9cec3-113">Tempo utente (un importo significativo, ad esempio 30 secondi o più).</span><span class="sxs-lookup"><span data-stu-id="9cec3-113">User's time (a significant amount, such as 30 seconds or more).</span></span>

<span data-ttu-id="9cec3-114">Al contrario, una conferma è una finestra di dialogo modale che chiede se l'utente desidera procedere con un'azione.</span><span class="sxs-lookup"><span data-stu-id="9cec3-114">By contrast, a confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span> <span data-ttu-id="9cec3-115">Alcuni tipi di avvisi vengono presentati come conferme e, in tal caso, vengono applicate anche le linee guida di conferma.</span><span class="sxs-lookup"><span data-stu-id="9cec3-115">Some types of warnings are presented as confirmations, and if so, the confirmation guidelines also apply.</span></span>

<span data-ttu-id="9cec3-116">**Nota:** Le linee guida relative alle [finestre di dialogo](win-dialog-box.md), le [conferme](mess-confirm.md), [i messaggi di errore](mess-error.md)[icone standard](vis-std-icons.md), le [notifiche](mess-notif.md)e il [layout](vis-layout.md) vengono presentate in articoli distinti.</span><span class="sxs-lookup"><span data-stu-id="9cec3-116">**Note:** Guidelines related to [dialog boxes](win-dialog-box.md), [confirmations](mess-confirm.md), [error messages](mess-error.md)[standard icons](vis-std-icons.md), [notifications](mess-notif.md), and [layout](vis-layout.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="9cec3-117">Si tratta dell'interfaccia utente corretta?</span><span class="sxs-lookup"><span data-stu-id="9cec3-117">Is this the right user interface?</span></span>

<span data-ttu-id="9cec3-118">Per decidere, prendi in considerazione queste domande:</span><span class="sxs-lookup"><span data-stu-id="9cec3-118">To decide, consider these questions:</span></span>

-   <span data-ttu-id="9cec3-119">**L'utente viene avvisato di una condizione che potrebbe causare un problema in futuro?**</span><span class="sxs-lookup"><span data-stu-id="9cec3-119">**Is the user being alerted of a condition that might cause a problem in the future?**</span></span> <span data-ttu-id="9cec3-120">In caso contrario, il messaggio non è un avviso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-120">If not, the message isn't a warning.</span></span>
-   <span data-ttu-id="9cec3-121">**L'interfaccia utente presenta un errore o un problema che si è già verificato?**</span><span class="sxs-lookup"><span data-stu-id="9cec3-121">**Is the UI presenting an error or problem that has already occurred?**</span></span> <span data-ttu-id="9cec3-122">In caso affermativo, usare invece un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="9cec3-122">If so, use an error message instead.</span></span>
-   <span data-ttu-id="9cec3-123">**È probabile che gli utenti eseguano un'azione o modifichino il proprio comportamento come risultato del messaggio?**</span><span class="sxs-lookup"><span data-stu-id="9cec3-123">**Are users likely to perform an action or change their behavior as the result of the message?**</span></span> <span data-ttu-id="9cec3-124">In caso contrario, la condizione non giustifica l'interruzione dell'utente, quindi è preferibile eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="9cec3-124">If not, the condition doesn't justify interrupting the user so it's better to suppress the warning.</span></span>
-   <span data-ttu-id="9cec3-125">**La condizione è il risultato diretto di un'azione iniziata dall'utente?**</span><span class="sxs-lookup"><span data-stu-id="9cec3-125">**Is the condition the direct result of an action initiated by the user?**</span></span> <span data-ttu-id="9cec3-126">In caso contrario, prendere in considerazione l'uso di [notifiche di eventi non critiche](mess-notif.md).</span><span class="sxs-lookup"><span data-stu-id="9cec3-126">If not, consider using a [non-critical event notifications](mess-notif.md).</span></span>
-   <span data-ttu-id="9cec3-127">**La condizione è una condizione speciale in un controllo?**</span><span class="sxs-lookup"><span data-stu-id="9cec3-127">**Is the condition a special condition in a control?**</span></span> <span data-ttu-id="9cec3-128">In caso affermativo, usare invece un [fumetto](ctrl-balloons.md) .</span><span class="sxs-lookup"><span data-stu-id="9cec3-128">If so, use a [balloon](ctrl-balloons.md) instead.</span></span>
-   <span data-ttu-id="9cec3-129">**Per le conferme, l'utente sta per eseguire un'azione rischiosa?**</span><span class="sxs-lookup"><span data-stu-id="9cec3-129">**For confirmations, is the user about to perform a risky action?**</span></span> <span data-ttu-id="9cec3-130">In tal caso, è opportuno un avviso se l'azione ha conseguenze significative o non può essere facilmente annullata.</span><span class="sxs-lookup"><span data-stu-id="9cec3-130">If so, a warning is appropriate if the action has significant consequences or cannot be easily undone.</span></span>
-   <span data-ttu-id="9cec3-131">**Per altri tipi di avvisi, è necessario che l'utente agisca ora o nel futuro immediato?**</span><span class="sxs-lookup"><span data-stu-id="9cec3-131">**For other types of warnings, does the user need to act now or in the immediate future?**</span></span> <span data-ttu-id="9cec3-132">Non visualizzare avvisi se gli utenti possono continuare a lavorare in modo produttivo senza problemi immediati.</span><span class="sxs-lookup"><span data-stu-id="9cec3-132">Don't display warnings if users can continue to work productively without immediate problems.</span></span> <span data-ttu-id="9cec3-133">Posticipare l'avviso fino a quando la condizione non è più immediata e pertinente.</span><span class="sxs-lookup"><span data-stu-id="9cec3-133">Postpone the warning until the condition is more immediate and relevant.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="9cec3-134">Concetti relativi alla progettazione</span><span class="sxs-lookup"><span data-stu-id="9cec3-134">Design concepts</span></span>

### <a name="avoid-overwarning"></a><span data-ttu-id="9cec3-135">Evitare l'overwarning</span><span class="sxs-lookup"><span data-stu-id="9cec3-135">Avoid overwarning</span></span>

<span data-ttu-id="9cec3-136">I programmi Microsoft Windows sono sovrainformati.</span><span class="sxs-lookup"><span data-stu-id="9cec3-136">We overwarn in Microsoft Windows programs.</span></span> <span data-ttu-id="9cec3-137">Il normale programma Windows presenta avvisi apparentemente ovunque, in cui si verificano elementi che hanno un significato ridotto.</span><span class="sxs-lookup"><span data-stu-id="9cec3-137">The typical Windows program has warnings seemingly everywhere, warning about things that have little significance.</span></span> <span data-ttu-id="9cec3-138">In alcuni programmi, quasi tutte le domande vengono presentate come un avviso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-138">In some programs, nearly every question is presented as a warning.</span></span> <span data-ttu-id="9cec3-139">L'overwarning fa in modo che l'uso di un programma risulti un'attività pericolosa e si riducono da problemi realmente significativi.</span><span class="sxs-lookup"><span data-stu-id="9cec3-139">Overwarning makes using a program feel like a hazardous activity, and it detracts from truly significant issues.</span></span>

<span data-ttu-id="9cec3-140">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-140">**Incorrect:**</span></span>

![<span data-ttu-id="9cec3-141">Screenshot di un messaggio di avviso non necessario</span><span class="sxs-lookup"><span data-stu-id="9cec3-141">screen shot of an unnecessary warning message</span></span> ](images/mess-warn-image2.png)

<span data-ttu-id="9cec3-142">Overwarning rende il programma più pericoloso e sembra che sia stato progettato dagli avvocati.</span><span class="sxs-lookup"><span data-stu-id="9cec3-142">Overwarning makes your program feel hazardous and look like it was designed by lawyers.</span></span>

<span data-ttu-id="9cec3-143">Il mero potenziale per la perdita di dati o un problema futuro da solo non è sufficiente per chiamare un avviso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-143">The mere potential for data loss or a future problem alone is insufficient to call for a warning.</span></span> <span data-ttu-id="9cec3-144">Inoltre, tutti i risultati indesiderati devono essere imprevisti o non intenzionali e non sono facilmente corretti.</span><span class="sxs-lookup"><span data-stu-id="9cec3-144">Additionally, any undesirable results should be unexpected or unintended, and not easily corrected.</span></span> <span data-ttu-id="9cec3-145">In caso contrario, quasi tutti gli errori utente potrebbero essere interpretati per comportare la perdita di dati o un potenziale problema di qualche tipo e meritare un avviso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-145">Otherwise, just about any user mistake could be construed to result in data loss or a potential problem of some kind and merit a warning.</span></span>

### <a name="characteristics-of-good-warnings"></a><span data-ttu-id="9cec3-146">Caratteristiche degli avvisi validi</span><span class="sxs-lookup"><span data-stu-id="9cec3-146">Characteristics of good warnings</span></span>

<span data-ttu-id="9cec3-147">Avvisi positivi:</span><span class="sxs-lookup"><span data-stu-id="9cec3-147">Good warnings:</span></span>

-   <span data-ttu-id="9cec3-148">**Coinvolgere i rischi.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-148">**Involve risk.**</span></span> <span data-ttu-id="9cec3-149">Avvisi validi avvisano gli utenti di qualcosa di significativo.</span><span class="sxs-lookup"><span data-stu-id="9cec3-149">Good warnings alert users of something significant.</span></span>

<span data-ttu-id="9cec3-150">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-150">**Incorrect:**</span></span>

![<span data-ttu-id="9cec3-151">Screenshot di ' si desidera uscire?'</span><span class="sxs-lookup"><span data-stu-id="9cec3-151">screen shot of 'do you want to exit?'</span></span> <span data-ttu-id="9cec3-152">warning</span><span class="sxs-lookup"><span data-stu-id="9cec3-152">warning</span></span> ](images/mess-warn-image3.png)

<span data-ttu-id="9cec3-153">E allora?</span><span class="sxs-lookup"><span data-stu-id="9cec3-153">So what?</span></span> <span data-ttu-id="9cec3-154">Questa conferma presuppone che gli utenti riescano spesso i programmi per errore.</span><span class="sxs-lookup"><span data-stu-id="9cec3-154">This confirmation assumes that users often exit programs by accident.</span></span>

-   <span data-ttu-id="9cec3-155">**Hanno una rilevanza immediata.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-155">**Have immediate relevance.**</span></span> <span data-ttu-id="9cec3-156">Non solo gli utenti devono occuparsi di questo.</span><span class="sxs-lookup"><span data-stu-id="9cec3-156">Not only do users have to care, they have to care now.</span></span> <span data-ttu-id="9cec3-157">Gli utenti in genere non sono interessati ai problemi che potrebbero avere in un secondo momento, purché possano svolgere il proprio lavoro.</span><span class="sxs-lookup"><span data-stu-id="9cec3-157">Users typically aren't interested in problems they might have later as long as they can do their work now.</span></span>

<span data-ttu-id="9cec3-158">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-158">**Incorrect:**</span></span>

![<span data-ttu-id="9cec3-159">screenshot della batteria: avviso minimo di tre ore</span><span class="sxs-lookup"><span data-stu-id="9cec3-159">screen shot of battery-low-in-three-hours warning</span></span> ](images/mess-warn-image4.png)

<span data-ttu-id="9cec3-160">In questo caso, è preferibile solo avvisare l'utente in tre ore.</span><span class="sxs-lookup"><span data-stu-id="9cec3-160">In this case, it's better just to warn the user in three hours.</span></span>

-   <span data-ttu-id="9cec3-161">**Condurre l'azione.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-161">**Lead to action.**</span></span> <span data-ttu-id="9cec3-162">È necessario che gli utenti eseguano o siano a conoscenza di come il risultato dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-162">There is something users must do or be aware of as the result of the warning.</span></span> <span data-ttu-id="9cec3-163">Forse è necessario eseguire un'azione subito o in un secondo momento nel futuro immediato.</span><span class="sxs-lookup"><span data-stu-id="9cec3-163">Perhaps they must take an action now or sometime in the immediate future.</span></span> <span data-ttu-id="9cec3-164">Probabilmente eseguiranno un'attività in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-164">Perhaps they will perform a task differently as a result.</span></span> <span data-ttu-id="9cec3-165">La conseguenza di ignorare l'avviso dovrebbe essere chiara.</span><span class="sxs-lookup"><span data-stu-id="9cec3-165">The consequence of ignoring the warning should be clear.</span></span> <span data-ttu-id="9cec3-166">Gli avvisi senza azioni fanno solo sentire paranoici.</span><span class="sxs-lookup"><span data-stu-id="9cec3-166">Warnings without actions just make users feel paranoid.</span></span>

<span data-ttu-id="9cec3-167">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-167">**Incorrect:**</span></span>

![<span data-ttu-id="9cec3-168">screenshot dell'avviso "Live Messenger is running"</span><span class="sxs-lookup"><span data-stu-id="9cec3-168">screen shot of 'live messenger is running' warning</span></span> ](images/mess-warn-image5.png)

<span data-ttu-id="9cec3-169">Perché si tratta di una notifica di avviso?</span><span class="sxs-lookup"><span data-stu-id="9cec3-169">Why is this notification a warning?</span></span> <span data-ttu-id="9cec3-170">Che cosa dovrebbero fare gli utenti (oltre a preoccuparsi)?</span><span class="sxs-lookup"><span data-stu-id="9cec3-170">What are users supposed to do (beside worry)?</span></span>

-   <span data-ttu-id="9cec3-171">**Non sono evidenti.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-171">**Are not obvious.**</span></span> <span data-ttu-id="9cec3-172">Non visualizzare un avviso per indicare la conseguenza ovvia di un'azione.</span><span class="sxs-lookup"><span data-stu-id="9cec3-172">Don't display a warning to state the obvious consequence of an action.</span></span> <span data-ttu-id="9cec3-173">Si supponga, ad esempio, che gli utenti capiscano le conseguenze del mancato completamento di un'attività.</span><span class="sxs-lookup"><span data-stu-id="9cec3-173">For example, assume users understand the consequences of not completing a task.</span></span>

<span data-ttu-id="9cec3-174">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-174">**Incorrect:**</span></span>

![<span data-ttu-id="9cec3-175">Screenshot di uscire dalla procedura guidata? avviso</span><span class="sxs-lookup"><span data-stu-id="9cec3-175">screen shot of do you want to exit wizard? warning</span></span> ](images/mess-warn-image6.png)

<span data-ttu-id="9cec3-176">L'annullamento di una procedura guidata incompleta significa che l'attività non viene eseguita... Chi sa?</span><span class="sxs-lookup"><span data-stu-id="9cec3-176">Canceling an incomplete wizard means the task doesn't get done...who knew?</span></span>

-   <span data-ttu-id="9cec3-177">**Si verificano raramente.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-177">**Occur infrequently.**</span></span> <span data-ttu-id="9cec3-178">Gli avvisi costanti diventano rapidamente inefficaci e fastidiosi.</span><span class="sxs-lookup"><span data-stu-id="9cec3-178">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="9cec3-179">Gli utenti spesso diventano più mirati a eliminare l'avviso rispetto al problema.</span><span class="sxs-lookup"><span data-stu-id="9cec3-179">Users often become more focused on getting rid of the warning than addressing the problem.</span></span>

<span data-ttu-id="9cec3-180">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-180">**Incorrect:**</span></span>

![<span data-ttu-id="9cec3-181">screenshot dell'avviso ' Aggiorna firme virus '</span><span class="sxs-lookup"><span data-stu-id="9cec3-181">screen shot of 'update virus signatures' warning</span></span> ](images/mess-warn-image7.png)

<span data-ttu-id="9cec3-182">È più probabile che gli utenti si concentrino su come eliminare l'avviso rispetto alla risoluzione del problema sottostante.</span><span class="sxs-lookup"><span data-stu-id="9cec3-182">Users are more likely to focus on getting rid of the warning than fixing the underlying problem.</span></span>

<span data-ttu-id="9cec3-183">Un messaggio che non ha queste caratteristiche potrebbe essere ancora un messaggio valido, ma non un avviso valido.</span><span class="sxs-lookup"><span data-stu-id="9cec3-183">A message that doesn't have these characteristics might still be a good message, just not a good warning.</span></span>

### <a name="determine-the-appropriate-message-type"></a><span data-ttu-id="9cec3-184">Determinare il tipo di messaggio appropriato</span><span class="sxs-lookup"><span data-stu-id="9cec3-184">Determine the appropriate message type</span></span>

<span data-ttu-id="9cec3-185">Alcuni problemi possono essere presentati come un errore, un avviso o informazioni, a seconda dell'enfasi e della formulazione.</span><span class="sxs-lookup"><span data-stu-id="9cec3-185">Some issues can be presented as an error, warning, or information, depending on the emphasis and phrasing.</span></span> <span data-ttu-id="9cec3-186">Si supponga, ad esempio, che una pagina Web non possa caricare un controllo ActiveX non firmato basato sulla configurazione corrente di Windows Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="9cec3-186">For example, suppose a Web page cannot load an unsigned ActiveX control based on the current Windows Internet Explorer configuration:</span></span>

-   <span data-ttu-id="9cec3-187">**Errore.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-187">**Error.**</span></span> <span data-ttu-id="9cec3-188">"Questa pagina non può caricare un controllo ActiveX senza segno".</span><span class="sxs-lookup"><span data-stu-id="9cec3-188">"This page cannot load an unsigned ActiveX control."</span></span> <span data-ttu-id="9cec3-189">(Frase come problema esistente).</span><span class="sxs-lookup"><span data-stu-id="9cec3-189">(Phrased as an existing problem.)</span></span>
-   <span data-ttu-id="9cec3-190">**Avviso.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-190">**Warning.**</span></span> <span data-ttu-id="9cec3-191">"Questa pagina potrebbe non comportarsi come previsto perché Windows Internet Explorer non è configurato per il caricamento di controlli ActiveX non firmati".</span><span class="sxs-lookup"><span data-stu-id="9cec3-191">"This page might not behave as expected because Windows Internet Explorer isn't configured to load unsigned ActiveX controls."</span></span> <span data-ttu-id="9cec3-192">oppure "Consenti a questa pagina di installare un controllo ActiveX senza segno?</span><span class="sxs-lookup"><span data-stu-id="9cec3-192">or "Allow this page to install an unsigned ActiveX Control?</span></span> <span data-ttu-id="9cec3-193">Questa operazione da origini non attendibili potrebbe danneggiare il computer ".</span><span class="sxs-lookup"><span data-stu-id="9cec3-193">Doing so from untrusted sources may harm your computer."</span></span> <span data-ttu-id="9cec3-194">(Entrambe espresse come condizioni che possono causare problemi futuri).</span><span class="sxs-lookup"><span data-stu-id="9cec3-194">(Both phrased as conditions that may cause future problems.)</span></span>
-   <span data-ttu-id="9cec3-195">**Informazioni.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-195">**Information.**</span></span> <span data-ttu-id="9cec3-196">"È stato configurato Windows Internet Explorer per bloccare i controlli ActiveX non firmati."</span><span class="sxs-lookup"><span data-stu-id="9cec3-196">"You have configured Windows Internet Explorer to block unsigned ActiveX controls."</span></span> <span data-ttu-id="9cec3-197">(Enunciato come dichiarazione di fatto).</span><span class="sxs-lookup"><span data-stu-id="9cec3-197">(Phrased as a statement of fact.)</span></span>

<span data-ttu-id="9cec3-198">**Per determinare il tipo di messaggio appropriato, concentrarsi sull'aspetto più importante del problema che gli utenti devono sapere o su cui intervenire.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-198">**To determine the appropriate message type, focus on the most important aspect of the issue that users need to know or act upon.**</span></span> <span data-ttu-id="9cec3-199">In genere, se un problema impedisce all'utente di procedere, è necessario presentarlo come errore; Se l'utente può continuare, presentarlo come avviso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-199">Typically, if an issue blocks the user from proceeding, you should present it as an error; if the user can proceed, present it as a warning.</span></span> <span data-ttu-id="9cec3-200">Creare l' [istruzione principale](text-ui.md) o un altro testo corrispondente in base a tale stato attivo, quindi scegliere un'icona ([standard](vis-std-icons.md) o altro) che corrisponda al testo.</span><span class="sxs-lookup"><span data-stu-id="9cec3-200">Craft the [main instruction](text-ui.md) or other corresponding text based on that focus, then choose an icon ([standard](vis-std-icons.md) or otherwise) that matches the text.</span></span> <span data-ttu-id="9cec3-201">Il testo dell'istruzione principale e le icone devono sempre corrispondere.</span><span class="sxs-lookup"><span data-stu-id="9cec3-201">The main instruction text and icons should always match.</span></span>

### <a name="be-specific"></a><span data-ttu-id="9cec3-202">Specifica</span><span class="sxs-lookup"><span data-stu-id="9cec3-202">Be specific</span></span>

<span data-ttu-id="9cec3-203">Gli avvisi sono più interessanti quando le informazioni seguenti sono specifiche e chiare:</span><span class="sxs-lookup"><span data-stu-id="9cec3-203">Warnings are more compelling when the following information is specific and clear:</span></span>

-   <span data-ttu-id="9cec3-204">Origine dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-204">The source of the warning.</span></span>
-   <span data-ttu-id="9cec3-205">Condizione specifica e potenziale problema.</span><span class="sxs-lookup"><span data-stu-id="9cec3-205">The specific condition and potential problem.</span></span>
-   <span data-ttu-id="9cec3-206">Operazioni che l'utente deve eseguire.</span><span class="sxs-lookup"><span data-stu-id="9cec3-206">What the user should do about it.</span></span>
-   <span data-ttu-id="9cec3-207">Cosa accade se l'utente non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="9cec3-207">What happens if the user doesn't do anything.</span></span>

<span data-ttu-id="9cec3-208">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-208">**Incorrect:**</span></span>

![<span data-ttu-id="9cec3-209">Screenshot di un avviso vago di rischio significativo</span><span class="sxs-lookup"><span data-stu-id="9cec3-209">screen shot of vague warning of significant risk</span></span> ](images/mess-warn-image8.png)

<span data-ttu-id="9cec3-210">In questo esempio, qual è il potenziale problema?</span><span class="sxs-lookup"><span data-stu-id="9cec3-210">In this example, what is the potential problem?</span></span> <span data-ttu-id="9cec3-211">Che cosa deve fare l'utente, oltre a non usare il proiettore sulla rete?</span><span class="sxs-lookup"><span data-stu-id="9cec3-211">What is the user supposed to do, aside from not using the projector over the network?</span></span> <span data-ttu-id="9cec3-212">Senza informazioni più specifiche, è possibile che l'utente non sia in grado di procedere.</span><span class="sxs-lookup"><span data-stu-id="9cec3-212">Without more specific information, all the user can do is feel bad about proceeding.</span></span>

<span data-ttu-id="9cec3-213">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-213">**Correct:**</span></span>

![<span data-ttu-id="9cec3-214">screenshot dell'avviso di problemi e conseguenze</span><span class="sxs-lookup"><span data-stu-id="9cec3-214">screen shot of warning of problem and consequences</span></span> ](images/mess-warn-image9.png)

<span data-ttu-id="9cec3-215">In questo esempio il problema e le conseguenze sono evidenti.</span><span class="sxs-lookup"><span data-stu-id="9cec3-215">In this example, the problem and consequences are clear.</span></span>

<span data-ttu-id="9cec3-216">In alcuni casi è possibile che si verifichi un problema legittimo per informare gli utenti, ma la soluzione e le conseguenze non sono note.</span><span class="sxs-lookup"><span data-stu-id="9cec3-216">Sometimes there is a legitimate potential problem worthy of informing users about, but the solution and consequences aren't known for sure.</span></span> <span data-ttu-id="9cec3-217">Anziché fornire un avviso vago, essere specifici fornendo le informazioni più probabili o l'esempio più comune.</span><span class="sxs-lookup"><span data-stu-id="9cec3-217">Rather than give a vague warning, be specific by giving the most likely information or the most common example.</span></span>

<span data-ttu-id="9cec3-218">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-218">**Correct:**</span></span>

![<span data-ttu-id="9cec3-219">screenshot dell'avviso di errore di rete e delle soluzioni</span><span class="sxs-lookup"><span data-stu-id="9cec3-219">screen shot of network error warning and solutions</span></span> ](images/mess-warn-image10.png)

<span data-ttu-id="9cec3-220">In questo esempio, l'avviso viene reso specifico fornendo la soluzione più probabile.</span><span class="sxs-lookup"><span data-stu-id="9cec3-220">In this example, the warning is made specific by providing the most likely solution.</span></span>

<span data-ttu-id="9cec3-221">In questi casi, tuttavia, utilizzare la formulazione che indica che esistono altre possibilità.</span><span class="sxs-lookup"><span data-stu-id="9cec3-221">However, in such cases, use wording that indicates that there are other possibilities.</span></span> <span data-ttu-id="9cec3-222">In caso contrario, gli utenti potrebbero essere fuorviati.</span><span class="sxs-lookup"><span data-stu-id="9cec3-222">Otherwise, users might be misled.</span></span>

<span data-ttu-id="9cec3-223">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-223">**Incorrect:**</span></span>

![<span data-ttu-id="9cec3-224">screenshot del cavo di rete-avviso scollegato</span><span class="sxs-lookup"><span data-stu-id="9cec3-224">screen shot of network cable unplugged warning</span></span> ](images/mess-warn-image11.png)

<span data-ttu-id="9cec3-225">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-225">**Correct:**</span></span>

![<span data-ttu-id="9cec3-226">è possibile che lo screenshot del cavo sia scollegato dall'avviso</span><span class="sxs-lookup"><span data-stu-id="9cec3-226">screen shot of cable might be unplugged warning</span></span> ](images/mess-warn-image12.png)

<span data-ttu-id="9cec3-227">Nell'esempio errato, gli utenti saranno confusi se il cavo è chiaramente collegato.</span><span class="sxs-lookup"><span data-stu-id="9cec3-227">In the incorrect example, users will be confused if the cable is clearly plugged in.</span></span>

<span data-ttu-id="9cec3-228">**Se si eseguono solo due operazioni...**</span><span class="sxs-lookup"><span data-stu-id="9cec3-228">**If you do only two things...**</span></span>

1. <span data-ttu-id="9cec3-229">Non sovraavvisare.</span><span class="sxs-lookup"><span data-stu-id="9cec3-229">Don't overwarn.</span></span> <span data-ttu-id="9cec3-230">Limitare gli avvisi alle condizioni che coinvolgono il rischio e sono immediatamente rilevanti, interoperabili, non evidenti e poco frequenti.</span><span class="sxs-lookup"><span data-stu-id="9cec3-230">Limit warnings to conditions that involve risk and are immediately relevant, actionable, not obvious, and infrequent.</span></span> <span data-ttu-id="9cec3-231">In caso contrario, rimuovere o riformulare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="9cec3-231">Otherwise, remove or rephrase the message.</span></span>

2. <span data-ttu-id="9cec3-232">Fornire informazioni utili specifiche.</span><span class="sxs-lookup"><span data-stu-id="9cec3-232">Provide specific, useful information.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="9cec3-233">Modelli di utilizzo</span><span class="sxs-lookup"><span data-stu-id="9cec3-233">Usage patterns</span></span>

<span data-ttu-id="9cec3-234">Gli avvisi hanno diversi modelli di utilizzo:</span><span class="sxs-lookup"><span data-stu-id="9cec3-234">Warnings have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cec3-235"><strong>Informazioni</strong></span><span class="sxs-lookup"><span data-stu-id="9cec3-235"><strong>Awareness</strong></span></span><br/> <span data-ttu-id="9cec3-236">Informare l'utente di una condizione o di un potenziale problema, ma l'utente potrebbe non dover eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="9cec3-236">Make user aware of a condition or potential problem, but user may not have to do anything now.</span></span> <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> <span data-ttu-id="9cec3-237">Esempi di avvisi di consapevolezza.</span><span class="sxs-lookup"><span data-stu-id="9cec3-237">Examples of awareness warnings.</span></span><br/> <span data-ttu-id="9cec3-238">Gli avvisi di sensibilizzazione hanno la presentazione seguente:</span><span class="sxs-lookup"><span data-stu-id="9cec3-238">Awareness warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="9cec3-239"><strong>Istruzione principale:</strong> Descrizione della condizione o del potenziale problema.</span><span class="sxs-lookup"><span data-stu-id="9cec3-239"><strong>Main instruction:</strong> Describe the condition or potential problem.</span></span></li>
<li><span data-ttu-id="9cec3-240"><strong>Istruzione supplementare:</strong> Illustrare le implicazioni e il motivo per cui è importante.</span><span class="sxs-lookup"><span data-stu-id="9cec3-240"><strong>Supplemental instruction:</strong> Explain the implication and why it is important.</span></span></li>
<li><span data-ttu-id="9cec3-241"><strong>Pulsanti di commit:</strong> Vicino.</span><span class="sxs-lookup"><span data-stu-id="9cec3-241"><strong>Commit buttons:</strong> Close.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cec3-242"><strong>Prevenzione degli errori</strong></span><span class="sxs-lookup"><span data-stu-id="9cec3-242"><strong>Error prevention</strong></span></span><br/> <span data-ttu-id="9cec3-243">Informare gli utenti delle informazioni che potrebbero impedire un problema, soprattutto quando si effettuano scelte.</span><span class="sxs-lookup"><span data-stu-id="9cec3-243">Make user aware of information that might prevent a problem, especially when making choices.</span></span> <br/></td>
<td><span data-ttu-id="9cec3-244">Gli avvisi di prevenzione degli errori vengono presentati in modo ottimale usando un'icona di avviso sul posto e un testo esplicativo.</span><span class="sxs-lookup"><span data-stu-id="9cec3-244">Error prevention warnings are best presented using an in-place warning icon and explanatory text.</span></span> <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> <span data-ttu-id="9cec3-245">Esempi di avvisi di prevenzione degli errori.</span><span class="sxs-lookup"><span data-stu-id="9cec3-245">Examples of error prevention warnings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cec3-246"><strong>Problema imminente</strong></span><span class="sxs-lookup"><span data-stu-id="9cec3-246"><strong>Imminent problem</strong></span></span><br/> <span data-ttu-id="9cec3-247">L'utente deve ora eseguire un'operazione per evitare un problema imminente.</span><span class="sxs-lookup"><span data-stu-id="9cec3-247">The user needs to do something now to prevent an imminent problem.</span></span> <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> <span data-ttu-id="9cec3-248">Un esempio di avviso imminente di un problema.</span><span class="sxs-lookup"><span data-stu-id="9cec3-248">An example of an imminent problem warning.</span></span><br/> <span data-ttu-id="9cec3-249">Gli avvisi imminenti per i problemi hanno la seguente presentazione:</span><span class="sxs-lookup"><span data-stu-id="9cec3-249">Imminent problem warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="9cec3-250"><strong>Istruzione principale:</strong> Descrivere le operazioni che l'utente deve eseguire.</span><span class="sxs-lookup"><span data-stu-id="9cec3-250"><strong>Main instruction:</strong> Describe what the user needs to do now.</span></span></li>
<li><span data-ttu-id="9cec3-251"><strong>Istruzione supplementare:</strong> Illustrare la condizione e il motivo per cui è importante.</span><span class="sxs-lookup"><span data-stu-id="9cec3-251"><strong>Supplemental instruction:</strong> Explain the condition and why it is important.</span></span></li>
<li><span data-ttu-id="9cec3-252"><strong>Pulsanti di commit:</strong> Un pulsante di comando o un collegamento al comando per ogni opzione oppure OK se l'azione si verifica all'esterno della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="9cec3-252"><strong>Commit buttons:</strong> A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cec3-253"><strong>Conferma dell'azione rischiosa</strong></span><span class="sxs-lookup"><span data-stu-id="9cec3-253"><strong>Risky action confirmation</strong></span></span><br/> <span data-ttu-id="9cec3-254">Confermare che l'utente desidera procedere con un'azione che presenta un certo rischio e non può essere annullata facilmente.</span><span class="sxs-lookup"><span data-stu-id="9cec3-254">Confirm that the user wants to proceed with an action that has some risk and can't be easily undone.</span></span> <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> <span data-ttu-id="9cec3-255">Esempio di conferma dell'azione rischiosa.</span><span class="sxs-lookup"><span data-stu-id="9cec3-255">An example of risky action confirmation.</span></span><br/> <span data-ttu-id="9cec3-256">Per le conferme di azione rischiosa sono disponibili le seguenti presentazioni:</span><span class="sxs-lookup"><span data-stu-id="9cec3-256">Risky action confirmations have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="9cec3-257"><strong>Istruzione principale:</strong> Porre una domanda per determinare se l'utente vuole continuare.</span><span class="sxs-lookup"><span data-stu-id="9cec3-257"><strong>Main instruction:</strong> Ask a question to determine if the user wants to proceed.</span></span></li>
<li><span data-ttu-id="9cec3-258"><strong>Istruzione supplementare:</strong> Spiega tutti i motivi non evidenti per cui l'utente potrebbe non voler procedere.</span><span class="sxs-lookup"><span data-stu-id="9cec3-258"><strong>Supplemental instruction:</strong> Explain any non-obvious reasons why the user might not want to proceed.</span></span></li>
<li><span data-ttu-id="9cec3-259"><strong>Pulsanti di commit:</strong> Sì, no.</span><span class="sxs-lookup"><span data-stu-id="9cec3-259"><strong>Commit buttons:</strong> Yes, No.</span></span></li>
</ul>
<span data-ttu-id="9cec3-260">Per le linee guida su questo modello, vedere <a href="mess-confirm.md">conferme</a>.</span><span class="sxs-lookup"><span data-stu-id="9cec3-260">For guidelines on this pattern, see <a href="mess-confirm.md">Confirmations</a>.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="9cec3-261">Indicazioni</span><span class="sxs-lookup"><span data-stu-id="9cec3-261">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="9cec3-262">Presentazione</span><span class="sxs-lookup"><span data-stu-id="9cec3-262">Presentation</span></span>

-   <span data-ttu-id="9cec3-263">**Scegliere l'interfaccia utente di presentazione in base al tipo di informazioni:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-263">**Choose the presentation UI based on the type of information:**</span></span>



|                               |                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cec3-264">**Interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="9cec3-264">**User interface**</span></span><br/> | <span data-ttu-id="9cec3-265">**Migliore uso per**</span><span class="sxs-lookup"><span data-stu-id="9cec3-265">**Best used for**</span></span><br/>                                                                                                           |
| <span data-ttu-id="9cec3-266">Finestre di dialogo modali</span><span class="sxs-lookup"><span data-stu-id="9cec3-266">Modal dialog boxes</span></span><br/> | <span data-ttu-id="9cec3-267">Avvisi critici (incluse le conferme) a cui gli utenti devono rispondere ora.</span><span class="sxs-lookup"><span data-stu-id="9cec3-267">Critical warnings (including confirmations) that users must respond to now.</span></span><br/>                                                 |
| <span data-ttu-id="9cec3-268">Sul posto</span><span class="sxs-lookup"><span data-stu-id="9cec3-268">In-place</span></span><br/>           | <span data-ttu-id="9cec3-269">Informazioni che potrebbero impedire un problema, specialmente quando gli utenti effettuano scelte.</span><span class="sxs-lookup"><span data-stu-id="9cec3-269">Information that might prevent a problem, especially when users are making choices.</span></span><br/>                                         |
| <span data-ttu-id="9cec3-270">Banner</span><span class="sxs-lookup"><span data-stu-id="9cec3-270">Banners</span></span><br/>            | <span data-ttu-id="9cec3-271">Informazioni che potrebbero impedire un problema, soprattutto quando sono correlate al completamento di un'attività.</span><span class="sxs-lookup"><span data-stu-id="9cec3-271">Information that might prevent a problem, especially when related to completing a task.</span></span><br/>                                     |
| <span data-ttu-id="9cec3-272">Notifiche</span><span class="sxs-lookup"><span data-stu-id="9cec3-272">Notifications</span></span><br/>      | <span data-ttu-id="9cec3-273">Eventi o stati significativi che possono essere tranquillamente ignorati, almeno temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="9cec3-273">Significant events or status that can be safely ignored, at least temporarily.</span></span><br/>                                              |
| <span data-ttu-id="9cec3-274">Palloncini</span><span class="sxs-lookup"><span data-stu-id="9cec3-274">Balloons</span></span><br/>           | <span data-ttu-id="9cec3-275">Un controllo si trova in uno stato che influiscono sull'input.</span><span class="sxs-lookup"><span data-stu-id="9cec3-275">A control is in a state that affects input.</span></span> <span data-ttu-id="9cec3-276">È probabile che questo stato non sia intenzionale e che l'utente non possa realizzare l'input interessato.</span><span class="sxs-lookup"><span data-stu-id="9cec3-276">This state is likely unintended and the user may not realize input is affected.</span></span><br/> |



 

-   <span data-ttu-id="9cec3-277">**Per le finestre di dialogo modali:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-277">**For modal dialog boxes:**</span></span>
    -   <span data-ttu-id="9cec3-278">**Usare le finestre di dialogo delle attività quando appropriato per ottenere un aspetto e un layout coerenti.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-278">**Use task dialogs whenever appropriate to achieve a consistent look and layout.**</span></span> <span data-ttu-id="9cec3-279">Le finestre di dialogo delle attività richiedono Windows Vista o versioni successive, quindi non sono adatte per le versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="9cec3-279">Task dialogs require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span>
    -   <span data-ttu-id="9cec3-280">**Visualizza solo un messaggio di avviso per condizione.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-280">**Display only one warning message per condition.**</span></span> <span data-ttu-id="9cec3-281">Ad esempio, viene visualizzato un singolo avviso che spiega completamente una condizione invece di descriverlo un dettaglio alla volta per ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="9cec3-281">For example, display a single warning that completely explains a condition instead of describing it one detail at a time per message.</span></span> <span data-ttu-id="9cec3-282">La visualizzazione di una sequenza di finestre di dialogo di avviso per una singola condizione è confusa e fastidiosa.</span><span class="sxs-lookup"><span data-stu-id="9cec3-282">Displaying a sequence of warning dialogs for a single condition is confusing and annoying.</span></span>
    -   <span data-ttu-id="9cec3-283">**Non visualizzare più di una volta un avviso per condizione.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-283">**Don't display a warning more than once per condition.**</span></span> <span data-ttu-id="9cec3-284">Gli avvisi costanti diventano rapidamente inefficaci e fastidiosi.</span><span class="sxs-lookup"><span data-stu-id="9cec3-284">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="9cec3-285">Gli utenti spesso diventano più mirati a eliminare l'avviso rispetto al problema.</span><span class="sxs-lookup"><span data-stu-id="9cec3-285">Users often become more focused on getting rid of the warning than addressing the problem.</span></span> <span data-ttu-id="9cec3-286">Se è necessario avvisare ripetutamente per una singola condizione, usare l' [escalation progressiva](mess-notif.md).</span><span class="sxs-lookup"><span data-stu-id="9cec3-286">If you must warn repeatedly for a single condition, use [progressive escalation](mess-notif.md).</span></span>
-   <span data-ttu-id="9cec3-287">**Non accompagnare avvisi con un effetto acustico o un segnale acustico.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-287">**Don't accompany warnings with a sound effect or beep.**</span></span> <span data-ttu-id="9cec3-288">Questa operazione è stonata e non necessaria.</span><span class="sxs-lookup"><span data-stu-id="9cec3-288">Doing so is jarring and unnecessary.</span></span>
    -   <span data-ttu-id="9cec3-289">**Eccezione:** Se l'utente deve rispondere immediatamente, è possibile usare un effetto acustico.</span><span class="sxs-lookup"><span data-stu-id="9cec3-289">**Exception:** If the user must respond immediately, you can use a sound effect.</span></span>

### <a name="icons"></a><span data-ttu-id="9cec3-290">Icone</span><span class="sxs-lookup"><span data-stu-id="9cec3-290">Icons</span></span>

-   <span data-ttu-id="9cec3-291">Non inserire un'icona di avviso nella barra del titolo di una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="9cec3-291">Don't place a warning icon in the title bar of a dialog box.</span></span>
-   <span data-ttu-id="9cec3-292">**Usare un'icona di avviso.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-292">**Use a warning icon.**</span></span> <span data-ttu-id="9cec3-293">Eccezioni:</span><span class="sxs-lookup"><span data-stu-id="9cec3-293">Exceptions:</span></span>
    -   <span data-ttu-id="9cec3-294">Se l'avviso è relativo a una funzionalità con un'icona, è possibile usare l'icona della funzionalità con una sovrimpressione di avviso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-294">If the warning is for a feature that has an icon, you can use the feature icon with a warning overlay.</span></span>

        <span data-ttu-id="9cec3-295">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-295">**Correct:**</span></span>

        ![<span data-ttu-id="9cec3-296">screenshot dell'icona di blocco con sovrapposizione dell'icona di avviso</span><span class="sxs-lookup"><span data-stu-id="9cec3-296">screen shot of lock icon with warning icon overlay</span></span> ](images/mess-warn-image21.png)

        <span data-ttu-id="9cec3-297">In questo esempio, l'icona della funzionalità presenta una sovrapposizione di avviso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-297">In this example, the feature icon has a warning overlay.</span></span>

-   <span data-ttu-id="9cec3-298">Per le finestre di dialogo modali con una nota di avviso, inserire l'icona di avviso nella nota a piè di pagina anziché nell'area del contenuto.</span><span class="sxs-lookup"><span data-stu-id="9cec3-298">For modal dialog boxes with a warning footnote, put the warning icon in the footnote instead of the content area.</span></span>

    <span data-ttu-id="9cec3-299">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-299">**Correct:**</span></span>

    ![<span data-ttu-id="9cec3-300">screenshot dell'icona di avviso nella nota a piè di pagina della finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="9cec3-300">screen shot of warning icon in dialog-box footnote</span></span> ](images/mess-warn-image22.png)

    <span data-ttu-id="9cec3-301">In questo esempio, la nota contiene l'icona di avviso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-301">In this example, the footnote has the warning icon.</span></span>

<span data-ttu-id="9cec3-302">Per altre linee guida ed esempi, vedere [icone standard](vis-std-icons.md).</span><span class="sxs-lookup"><span data-stu-id="9cec3-302">For more guidelines and examples, see [Standard Icons](vis-std-icons.md).</span></span>

### <a name="dont-show-this-message-again"></a><span data-ttu-id="9cec3-303">Non visualizzare più questo messaggio</span><span class="sxs-lookup"><span data-stu-id="9cec3-303">Don't show this message again</span></span>

-   <span data-ttu-id="9cec3-304">**Se una finestra di dialogo di avviso richiede questa opzione, riconsiderare l'avviso e la relativa frequenza.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-304">**If a warning dialog box needs this option, reconsider the warning and its frequency.**</span></span> <span data-ttu-id="9cec3-305">Se dispone di tutte le caratteristiche di un avviso valido (comporta il rischio ed è immediatamente pertinente, praticabile, non ovvia e poco frequente), non dovrebbe essere utile per gli utenti eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="9cec3-305">If it has all the characteristics of a good warning (involves risk, and is immediately relevant, actionable, not obvious, and infrequent), it shouldn't make sense for users to suppress it.</span></span>

<span data-ttu-id="9cec3-306">Per altre linee guida, vedere [finestre di dialogo](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="9cec3-306">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="progressive-disclosure"></a><span data-ttu-id="9cec3-307">Rivelazione progressiva</span><span class="sxs-lookup"><span data-stu-id="9cec3-307">Progressive disclosure</span></span>

-   <span data-ttu-id="9cec3-308">**Se è necessario includere informazioni avanzate in un messaggio di avviso, visualizzarlo usando i pulsanti di divulgazione progressiva** (ad esempio, "Mostra dettagli").</span><span class="sxs-lookup"><span data-stu-id="9cec3-308">**If you must include advanced information in a warning message, reveal it by using progressive disclosure buttons** (for example, "Show details").</span></span> <span data-ttu-id="9cec3-309">In questo modo, l'avviso viene semplificato per l'utilizzo tipico.</span><span class="sxs-lookup"><span data-stu-id="9cec3-309">Doing so simplifies the warning for typical usage.</span></span> <span data-ttu-id="9cec3-310">Non nascondere le informazioni necessarie perché gli utenti potrebbero non trovarlo.</span><span class="sxs-lookup"><span data-stu-id="9cec3-310">Don't hide needed information because users might not find it.</span></span>
-   <span data-ttu-id="9cec3-311">**Non usare "Show Details", a meno che non vi siano effettivamente più dettagli.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-311">**Don't use "Show details" unless there really is more detail.**</span></span> <span data-ttu-id="9cec3-312">Non solo riformulare le informazioni esistenti in un formato diverso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-312">Don't just restate the existing information in a different format.</span></span>

<span data-ttu-id="9cec3-313">Per le linee guida sulle etichette, vedere [divulgazione progressiva](ctrl-progressive-disclosure-controls.md).</span><span class="sxs-lookup"><span data-stu-id="9cec3-313">For labeling guidelines, see [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="9cec3-314">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="9cec3-314">Default values</span></span>

-   <span data-ttu-id="9cec3-315">**Selezionare la risposta più sicura, meno distruttiva o più sicura come predefinita.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-315">**Select the safest, least destructive, or most secure response to be the default.**</span></span>

## <a name="text"></a><span data-ttu-id="9cec3-316">Testo</span><span class="sxs-lookup"><span data-stu-id="9cec3-316">Text</span></span>

### <a name="general"></a><span data-ttu-id="9cec3-317">Generale</span><span class="sxs-lookup"><span data-stu-id="9cec3-317">General</span></span>

-   <span data-ttu-id="9cec3-318">**Rimuovere il testo ridondante.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-318">**Remove redundant text.**</span></span> <span data-ttu-id="9cec3-319">Cercarla in titoli, istruzioni principali, istruzioni aggiuntive, aree di contenuto, collegamenti ai comandi e pulsanti di commit.</span><span class="sxs-lookup"><span data-stu-id="9cec3-319">Look for it in titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="9cec3-320">In genere, lasciare il testo completo nelle istruzioni e nei controlli interattivi e rimuovere qualsiasi ridondanza dalle altre posizioni.</span><span class="sxs-lookup"><span data-stu-id="9cec3-320">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="9cec3-321">**Non usare i termini "avviso" o "attenzione" nel testo.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-321">**Don't use the terms "warning" or "caution" in the text.**</span></span> <span data-ttu-id="9cec3-322">Se [usato correttamente](vis-std-icons.md), l'icona di avviso comunica sufficientemente che gli utenti devono procedere con cautela.</span><span class="sxs-lookup"><span data-stu-id="9cec3-322">When [used correctly](vis-std-icons.md), the warning icon sufficiently communicates that users must proceed with caution.</span></span>

<span data-ttu-id="9cec3-323">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-323">**Incorrect:**</span></span>

![<span data-ttu-id="9cec3-324">screenshot dell'utilizzo non necessario dell'avviso nel testo</span><span class="sxs-lookup"><span data-stu-id="9cec3-324">screen shot of unnecessary use of warning in text</span></span> ](images/mess-warn-image23.png)

<span data-ttu-id="9cec3-325">In questo esempio, il termine "avviso" non è necessario.</span><span class="sxs-lookup"><span data-stu-id="9cec3-325">In this example, the term "warning" is unnecessary.</span></span>

### <a name="titles"></a><span data-ttu-id="9cec3-326">Titoli</span><span class="sxs-lookup"><span data-stu-id="9cec3-326">Titles</span></span>

-   <span data-ttu-id="9cec3-327">**Usare il titolo per identificare il comando o la funzionalità da cui proviene l'avviso.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-327">**Use the title to identify the command or feature where the warning came from.**</span></span> <span data-ttu-id="9cec3-328">Eccezioni:</span><span class="sxs-lookup"><span data-stu-id="9cec3-328">Exceptions:</span></span>
    -   <span data-ttu-id="9cec3-329">Se un avviso viene visualizzato con molti comandi diversi, provare a usare il nome del programma.</span><span class="sxs-lookup"><span data-stu-id="9cec3-329">If a warning is displayed by many different commands, consider using the program name instead.</span></span>
    -   <span data-ttu-id="9cec3-330">Se il titolo è ridondante o confuso con l'istruzione principale, usare invece il nome del programma.</span><span class="sxs-lookup"><span data-stu-id="9cec3-330">If that title would be redundant or confusing with the main instruction, use the program name instead.</span></span>

<span data-ttu-id="9cec3-331">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-331">**Incorrect:**</span></span>

![<span data-ttu-id="9cec3-332">screenshot del titolo della finestra di dialogo avviso di sicurezza</span><span class="sxs-lookup"><span data-stu-id="9cec3-332">screen shot of security warning dialog box title</span></span> ](images/mess-warn-image24.png)

<span data-ttu-id="9cec3-333">In questo esempio "avviso di sicurezza" non identifica il comando o la funzionalità da cui proviene l'avviso.</span><span class="sxs-lookup"><span data-stu-id="9cec3-333">In this example, "Security Warning" doesn't identify the command or feature where the warning came from.</span></span>

-   <span data-ttu-id="9cec3-334">**Non usare il titolo per spiegare cosa fare nella finestra di dialogo** che è lo scopo dell'istruzione principale.</span><span class="sxs-lookup"><span data-stu-id="9cec3-334">**Don't use the title to explain what to do in the dialog** that's the purpose of the main instruction.</span></span>
-   <span data-ttu-id="9cec3-335">Usare l'uso [di maiuscole in stile titolo](glossary.md)senza la punteggiatura finale.</span><span class="sxs-lookup"><span data-stu-id="9cec3-335">Use [title-style capitalization](glossary.md), without ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="9cec3-336">Istruzioni principali</span><span class="sxs-lookup"><span data-stu-id="9cec3-336">Main instructions</span></span>

-   <span data-ttu-id="9cec3-337">L'istruzione principale di un avviso è basata sul modello di progettazione:</span><span class="sxs-lookup"><span data-stu-id="9cec3-337">The main instruction for a warning is based on its design pattern:</span></span>



|                                      |                                                                      |
|--------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="9cec3-338">**Modello**</span><span class="sxs-lookup"><span data-stu-id="9cec3-338">**Pattern**</span></span><br/>               | <span data-ttu-id="9cec3-339">**Istruzione principale**</span><span class="sxs-lookup"><span data-stu-id="9cec3-339">**Main instruction**</span></span><br/>                                      |
| <span data-ttu-id="9cec3-340">Riconoscimento</span><span class="sxs-lookup"><span data-stu-id="9cec3-340">Awareness</span></span><br/>                 | <span data-ttu-id="9cec3-341">Descrizione della condizione o del potenziale problema.</span><span class="sxs-lookup"><span data-stu-id="9cec3-341">Describe the condition or potential problem.</span></span><br/>              |
| <span data-ttu-id="9cec3-342">Problema imminente</span><span class="sxs-lookup"><span data-stu-id="9cec3-342">Imminent problem</span></span><br/>          | <span data-ttu-id="9cec3-343">Descrivere le operazioni che l'utente deve eseguire.</span><span class="sxs-lookup"><span data-stu-id="9cec3-343">Describe what the user needs to do now.</span></span><br/>                   |
| <span data-ttu-id="9cec3-344">Conferma dell'azione rischiosa</span><span class="sxs-lookup"><span data-stu-id="9cec3-344">Risky action confirmation</span></span><br/> | <span data-ttu-id="9cec3-345">Porre una domanda per determinare se l'utente vuole continuare.</span><span class="sxs-lookup"><span data-stu-id="9cec3-345">Ask a question to determine if the user wants to proceed.</span></span><br/> |



 

-   ![<span data-ttu-id="9cec3-346">Screenshot di una notifica con batteria insufficiente</span><span class="sxs-lookup"><span data-stu-id="9cec3-346">screen shot of a low-battery notification</span></span> ](images/mess-warn-image25.png)
-   <span data-ttu-id="9cec3-347">In questo esempio, la notifica della batteria insufficiente è un avviso di consapevolezza, quindi l'istruzione principale descrive la condizione.</span><span class="sxs-lookup"><span data-stu-id="9cec3-347">In this example, the low battery notification is an awareness warning, so the main instruction describes the condition.</span></span>
-   ![<span data-ttu-id="9cec3-348">screenshot della batteria di modifica immediatamente avviso</span><span class="sxs-lookup"><span data-stu-id="9cec3-348">screen shot of change battery immediately warning</span></span> ](images/mess-warn-image1.png)
-   <span data-ttu-id="9cec3-349">In questo esempio, la finestra di dialogo batteria insufficiente è un problema imminente, quindi l'istruzione principale descrive le operazioni che l'utente deve eseguire.</span><span class="sxs-lookup"><span data-stu-id="9cec3-349">In this example, the low battery dialog box is an imminent problem, so the main instruction describes what the user needs to do now.</span></span>
-   <span data-ttu-id="9cec3-350">**Usare concise solo una singola frase completa.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-350">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="9cec3-351">Rimuovere l'istruzione principale fino alle informazioni essenziali.</span><span class="sxs-lookup"><span data-stu-id="9cec3-351">Strip the main instruction down to the essential information.</span></span> <span data-ttu-id="9cec3-352">Se è necessario spiegare altro, utilizzare un'istruzione supplementare.</span><span class="sxs-lookup"><span data-stu-id="9cec3-352">If you must explain anything more, use a supplemental instruction.</span></span>
-   <span data-ttu-id="9cec3-353">**Usare parole come "Now" e "immediate" se l'utente deve agire immediatamente.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-353">**Use words like "now" and "immediately" if the user must act immediately.**</span></span> <span data-ttu-id="9cec3-354">Non usare queste parole se non è prevista alcuna urgenza.</span><span class="sxs-lookup"><span data-stu-id="9cec3-354">Don't use these words if there is no urgency.</span></span>
-   <span data-ttu-id="9cec3-355">**Essere specifici se sono presenti oggetti interessati, assegnare i nomi completi.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-355">**Be specific if there are objects involved, give their full names.**</span></span>
-   <span data-ttu-id="9cec3-356">Usare l'uso [di maiuscole in stile frase](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="9cec3-356">Use [sentence-style capitalization](glossary.md).</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="9cec3-357">Istruzioni supplementari</span><span class="sxs-lookup"><span data-stu-id="9cec3-357">Supplemental instructions</span></span>

-   <span data-ttu-id="9cec3-358">L'istruzione supplementare per un avviso è basata sul modello di progettazione:</span><span class="sxs-lookup"><span data-stu-id="9cec3-358">The supplemental instruction for a warning is based on its design pattern:</span></span>



|                                      |                                                                                    |
|--------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9cec3-359">**Modello**</span><span class="sxs-lookup"><span data-stu-id="9cec3-359">**Pattern**</span></span><br/>               | <span data-ttu-id="9cec3-360">**Istruzione supplementare**</span><span class="sxs-lookup"><span data-stu-id="9cec3-360">**Supplemental instruction**</span></span><br/>                                            |
| <span data-ttu-id="9cec3-361">Riconoscimento</span><span class="sxs-lookup"><span data-stu-id="9cec3-361">Awareness</span></span><br/>                 | <span data-ttu-id="9cec3-362">Illustrare le implicazioni e il motivo per cui è importante.</span><span class="sxs-lookup"><span data-stu-id="9cec3-362">Explain the implication and why it is important.</span></span><br/>                        |
| <span data-ttu-id="9cec3-363">Problema imminente</span><span class="sxs-lookup"><span data-stu-id="9cec3-363">Imminent problem</span></span><br/>          | <span data-ttu-id="9cec3-364">Illustrare la condizione e il motivo per cui è importante.</span><span class="sxs-lookup"><span data-stu-id="9cec3-364">Explain the condition and why it is important.</span></span><br/>                          |
| <span data-ttu-id="9cec3-365">Conferma dell'azione rischiosa</span><span class="sxs-lookup"><span data-stu-id="9cec3-365">Risky action confirmation</span></span><br/> | <span data-ttu-id="9cec3-366">Spiega tutti i motivi non evidenti per cui l'utente potrebbe non voler procedere.</span><span class="sxs-lookup"><span data-stu-id="9cec3-366">Explain any non-obvious reasons why the user might not want to proceed.</span></span><br/> |



 

-   <span data-ttu-id="9cec3-367">**Non ripetere l'istruzione principale con una formulazione leggermente diversa.**</span><span class="sxs-lookup"><span data-stu-id="9cec3-367">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="9cec3-368">Omettere invece l'istruzione supplementare se non è più necessario aggiungere.</span><span class="sxs-lookup"><span data-stu-id="9cec3-368">Instead, omit the supplemental instruction if there is not more to add.</span></span>
-   <span data-ttu-id="9cec3-369">Usare frasi complete, maiuscole e minuscole in stile frase e punteggiatura finale.</span><span class="sxs-lookup"><span data-stu-id="9cec3-369">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="9cec3-370">Pulsanti di commit</span><span class="sxs-lookup"><span data-stu-id="9cec3-370">Commit buttons</span></span>

-   <span data-ttu-id="9cec3-371">Per le finestre di dialogo di avviso, i pulsanti commit sono basati sul modello di progettazione:</span><span class="sxs-lookup"><span data-stu-id="9cec3-371">For warning dialog boxes, the commit buttons are based on its design pattern:</span></span>



|                                      |                                                                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cec3-372">**Modello**</span><span class="sxs-lookup"><span data-stu-id="9cec3-372">**Pattern**</span></span><br/>               | <span data-ttu-id="9cec3-373">**Pulsanti di commit**</span><span class="sxs-lookup"><span data-stu-id="9cec3-373">**Commit buttons**</span></span><br/>                                                                                   |
| <span data-ttu-id="9cec3-374">Riconoscimento</span><span class="sxs-lookup"><span data-stu-id="9cec3-374">Awareness</span></span><br/>                 | <span data-ttu-id="9cec3-375">Quasi.</span><span class="sxs-lookup"><span data-stu-id="9cec3-375">Close.</span></span> <span data-ttu-id="9cec3-376">Non usare OK perché suggerisce che i potenziali problemi sono OK.</span><span class="sxs-lookup"><span data-stu-id="9cec3-376">Don't use OK because it suggests that potential problems are OK.</span></span><br/>                              |
| <span data-ttu-id="9cec3-377">Problema imminente</span><span class="sxs-lookup"><span data-stu-id="9cec3-377">Imminent problem</span></span><br/>          | <span data-ttu-id="9cec3-378">Un pulsante di comando o un collegamento al comando per ogni opzione oppure OK se l'azione si verifica all'esterno della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="9cec3-378">A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span><br/> |
| <span data-ttu-id="9cec3-379">Conferma dell'azione rischiosa</span><span class="sxs-lookup"><span data-stu-id="9cec3-379">Risky action confirmation</span></span><br/> | <span data-ttu-id="9cec3-380">Sì, no.</span><span class="sxs-lookup"><span data-stu-id="9cec3-380">Yes, No.</span></span><br/>                                                                                             |



 

-   <span data-ttu-id="9cec3-381">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="9cec3-381">**Incorrect:**</span></span>
-   ![<span data-ttu-id="9cec3-382">screenshot della finestra di dialogo di avviso con pulsante OK</span><span class="sxs-lookup"><span data-stu-id="9cec3-382">screen shot of warning dialog box with ok button</span></span> ](images/mess-warn-image26.png)
-   <span data-ttu-id="9cec3-383">I problemi non sono OK. usare invece Close.</span><span class="sxs-lookup"><span data-stu-id="9cec3-383">Problems aren't OK, so use Close instead.</span></span>

## <a name="documentation"></a><span data-ttu-id="9cec3-384">Documentazione</span><span class="sxs-lookup"><span data-stu-id="9cec3-384">Documentation</span></span>

<span data-ttu-id="9cec3-385">Quando si fa riferimento agli avvisi:</span><span class="sxs-lookup"><span data-stu-id="9cec3-385">When referring to warnings:</span></span>

-   <span data-ttu-id="9cec3-386">Se l'avviso pone una domanda, fare riferimento a un avviso in base alla domanda. in caso contrario, utilizzare l'istruzione principale.</span><span class="sxs-lookup"><span data-stu-id="9cec3-386">If the warning asks a question, refer to a warning by its question; otherwise, use the main instruction.</span></span> <span data-ttu-id="9cec3-387">Se la domanda o l'istruzione principale è estesa o dettagliata, riepilogarla.</span><span class="sxs-lookup"><span data-stu-id="9cec3-387">If the question or main instruction is long or detailed, summarize it.</span></span>
-   <span data-ttu-id="9cec3-388">Se necessario, è possibile fare riferimento a una finestra di dialogo di avviso come messaggio.</span><span class="sxs-lookup"><span data-stu-id="9cec3-388">If necessary, you may refer to a warning dialog box as a message.</span></span>
-   <span data-ttu-id="9cec3-389">Quando possibile, formattare il testo usando grassetto.</span><span class="sxs-lookup"><span data-stu-id="9cec3-389">When possible, format the text using bold.</span></span> <span data-ttu-id="9cec3-390">In caso contrario, inserire il testo tra virgolette solo se necessario per evitare confusione.</span><span class="sxs-lookup"><span data-stu-id="9cec3-390">Otherwise, put the text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="9cec3-391">Esempio: nel messaggio **visualizzare gli elementi non protetti?** fare clic su Sì.</span><span class="sxs-lookup"><span data-stu-id="9cec3-391">Example: In the **Do you want to display the nonsecure items?** message, click Yes.</span></span>

 

