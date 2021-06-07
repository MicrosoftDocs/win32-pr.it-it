---
title: Messaggi di avviso
description: Un messaggio di avviso è una finestra di dialogo modale, un messaggio sul posto, una notifica o un balloon che avvisa l'utente di una condizione che potrebbe causare un problema in futuro.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 42f7c669a68790ec290f931165b4aa937b5008d5
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524505"
---
# <a name="warning-messages"></a><span data-ttu-id="b8688-103">Messaggi di avviso</span><span class="sxs-lookup"><span data-stu-id="b8688-103">Warning Messages</span></span>

> [!NOTE]
> <span data-ttu-id="b8688-104">Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="b8688-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="b8688-105">Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)</span><span class="sxs-lookup"><span data-stu-id="b8688-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="b8688-106">Un messaggio di avviso è una finestra di dialogo modale, un messaggio sul posto, una notifica o un balloon che avvisa l'utente di una condizione che potrebbe causare un problema in futuro.</span><span class="sxs-lookup"><span data-stu-id="b8688-106">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span>

![screenshot di un messaggio di avviso tipico](images/mess-warn-image1.png)

<span data-ttu-id="b8688-108">Messaggio di avviso modale tipico.</span><span class="sxs-lookup"><span data-stu-id="b8688-108">A typical modal warning message.</span></span>

<span data-ttu-id="b8688-109">La caratteristica fondamentale degli avvisi è che comportano il rischio di perdere uno o più degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b8688-109">The fundamental characteristic of warnings is that they involve the risk of losing one or more of the following:</span></span>

-   <span data-ttu-id="b8688-110">Un asset prezioso, ad esempio dati finanziari o di altro tipo importanti.</span><span class="sxs-lookup"><span data-stu-id="b8688-110">A valuable asset, such as important financial or other data.</span></span>
-   <span data-ttu-id="b8688-111">Accesso o integrità del sistema.</span><span class="sxs-lookup"><span data-stu-id="b8688-111">System access or integrity.</span></span>
-   <span data-ttu-id="b8688-112">Privacy o controllo sulle informazioni riservate.</span><span class="sxs-lookup"><span data-stu-id="b8688-112">Privacy or control over confidential information.</span></span>
-   <span data-ttu-id="b8688-113">Tempo dell'utente (una quantità significativa, ad esempio 30 secondi o più).</span><span class="sxs-lookup"><span data-stu-id="b8688-113">User's time (a significant amount, such as 30 seconds or more).</span></span>

<span data-ttu-id="b8688-114">Al contrario, una conferma è una finestra di dialogo modale che chiede se l'utente vuole procedere con un'azione.</span><span class="sxs-lookup"><span data-stu-id="b8688-114">By contrast, a confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span> <span data-ttu-id="b8688-115">Alcuni tipi di avvisi vengono presentati come conferme e, in tal caso, si applicano anche le linee guida per la conferma.</span><span class="sxs-lookup"><span data-stu-id="b8688-115">Some types of warnings are presented as confirmations, and if so, the confirmation guidelines also apply.</span></span>

<span data-ttu-id="b8688-116">**Nota:** Le linee guida relative [a finestre di dialogo,](win-dialog-box.md) [conferme,](mess-confirm.md) [messaggi](mess-error.md)di errore [icone](mess-notif.md)[standard,](vis-std-icons.md)notifiche e [layout](vis-layout.md) vengono presentate in articoli separati.</span><span class="sxs-lookup"><span data-stu-id="b8688-116">**Note:** Guidelines related to [dialog boxes](win-dialog-box.md), [confirmations](mess-confirm.md), [error messages](mess-error.md)[standard icons](vis-std-icons.md), [notifications](mess-notif.md), and [layout](vis-layout.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="b8688-117">Si tratta dell'interfaccia utente giusta?</span><span class="sxs-lookup"><span data-stu-id="b8688-117">Is this the right user interface?</span></span>

<span data-ttu-id="b8688-118">Per decidere, prendi in considerazione queste domande:</span><span class="sxs-lookup"><span data-stu-id="b8688-118">To decide, consider these questions:</span></span>

-   <span data-ttu-id="b8688-119">**L'utente viene avvisato di una condizione che potrebbe causare un problema in futuro?**</span><span class="sxs-lookup"><span data-stu-id="b8688-119">**Is the user being alerted of a condition that might cause a problem in the future?**</span></span> <span data-ttu-id="b8688-120">In caso contrario, il messaggio non è un avviso.</span><span class="sxs-lookup"><span data-stu-id="b8688-120">If not, the message isn't a warning.</span></span>
-   <span data-ttu-id="b8688-121">**L'interfaccia utente presenta un errore o un problema che si è già verificato?**</span><span class="sxs-lookup"><span data-stu-id="b8688-121">**Is the UI presenting an error or problem that has already occurred?**</span></span> <span data-ttu-id="b8688-122">In tal caso, usare invece un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="b8688-122">If so, use an error message instead.</span></span>
-   <span data-ttu-id="b8688-123">**Gli utenti probabilmente eseguiranno un'azione o modificheranno il comportamento come risultato del messaggio?**</span><span class="sxs-lookup"><span data-stu-id="b8688-123">**Are users likely to perform an action or change their behavior as the result of the message?**</span></span> <span data-ttu-id="b8688-124">In caso contrario, la condizione non giustifica l'interruzione dell'utente, quindi è meglio eliminare l'avviso.</span><span class="sxs-lookup"><span data-stu-id="b8688-124">If not, the condition doesn't justify interrupting the user so it's better to suppress the warning.</span></span>
-   <span data-ttu-id="b8688-125">**La condizione è il risultato diretto di un'azione avviata dall'utente?**</span><span class="sxs-lookup"><span data-stu-id="b8688-125">**Is the condition the direct result of an action initiated by the user?**</span></span> <span data-ttu-id="b8688-126">In caso contrario, è consigliabile usare [una notifica degli eventi non critica.](mess-notif.md)</span><span class="sxs-lookup"><span data-stu-id="b8688-126">If not, consider using a [non-critical event notifications](mess-notif.md).</span></span>
-   <span data-ttu-id="b8688-127">**La condizione è una condizione speciale in un controllo?**</span><span class="sxs-lookup"><span data-stu-id="b8688-127">**Is the condition a special condition in a control?**</span></span> <span data-ttu-id="b8688-128">In tal caso, usare invece [un balloon.](ctrl-balloons.md)</span><span class="sxs-lookup"><span data-stu-id="b8688-128">If so, use a [balloon](ctrl-balloons.md) instead.</span></span>
-   <span data-ttu-id="b8688-129">**Per le conferme, l'utente sta per eseguire un'azione rischiosa?**</span><span class="sxs-lookup"><span data-stu-id="b8688-129">**For confirmations, is the user about to perform a risky action?**</span></span> <span data-ttu-id="b8688-130">In tal caso, è appropriato un avviso se l'azione ha conseguenze significative o non può essere facilmente annullata.</span><span class="sxs-lookup"><span data-stu-id="b8688-130">If so, a warning is appropriate if the action has significant consequences or cannot be easily undone.</span></span>
-   <span data-ttu-id="b8688-131">**Per altri tipi di avvisi, l'utente deve agire ora o nell'immediato futuro?**</span><span class="sxs-lookup"><span data-stu-id="b8688-131">**For other types of warnings, does the user need to act now or in the immediate future?**</span></span> <span data-ttu-id="b8688-132">Non visualizzare avvisi se gli utenti possono continuare a lavorare in modo produttivo senza problemi immediati.</span><span class="sxs-lookup"><span data-stu-id="b8688-132">Don't display warnings if users can continue to work productively without immediate problems.</span></span> <span data-ttu-id="b8688-133">Posticipare l'avviso finché la condizione non è più immediata e pertinente.</span><span class="sxs-lookup"><span data-stu-id="b8688-133">Postpone the warning until the condition is more immediate and relevant.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="b8688-134">Concetti relativi alla progettazione</span><span class="sxs-lookup"><span data-stu-id="b8688-134">Design concepts</span></span>

### <a name="avoid-overwarning"></a><span data-ttu-id="b8688-135">Evitare l'overwarning</span><span class="sxs-lookup"><span data-stu-id="b8688-135">Avoid overwarning</span></span>

<span data-ttu-id="b8688-136">L'overwarn è stato fatto nei programmi Di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b8688-136">We overwarn in Microsoft Windows programs.</span></span> <span data-ttu-id="b8688-137">Il tipico programma Windows presenta avvisi apparentemente ovunque, con avvisi relativi a elementi poco significativi.</span><span class="sxs-lookup"><span data-stu-id="b8688-137">The typical Windows program has warnings seemingly everywhere, warning about things that have little significance.</span></span> <span data-ttu-id="b8688-138">In alcuni programmi quasi tutte le domande vengono presentate come avviso.</span><span class="sxs-lookup"><span data-stu-id="b8688-138">In some programs, nearly every question is presented as a warning.</span></span> <span data-ttu-id="b8688-139">L'overwarning fa in modo che l'uso di un programma sia un'attività rischiosa e sminuziona i problemi realmente significativi.</span><span class="sxs-lookup"><span data-stu-id="b8688-139">Overwarning makes using a program feel like a hazardous activity, and it detracts from truly significant issues.</span></span>

<span data-ttu-id="b8688-140">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-140">**Incorrect:**</span></span>

![<span data-ttu-id="b8688-141">screenshot di un messaggio di avviso non necessario</span><span class="sxs-lookup"><span data-stu-id="b8688-141">screen shot of an unnecessary warning message</span></span> ](images/mess-warn-image2.png)

<span data-ttu-id="b8688-142">L'overwarning rende il programma pericoloso e sembra che sia stato progettato da altri.</span><span class="sxs-lookup"><span data-stu-id="b8688-142">Overwarning makes your program feel hazardous and look like it was designed by lawyers.</span></span>

<span data-ttu-id="b8688-143">Il semplice rischio di perdita di dati o un problema futuro da solo non è sufficiente per chiamare un avviso.</span><span class="sxs-lookup"><span data-stu-id="b8688-143">The mere potential for data loss or a future problem alone is insufficient to call for a warning.</span></span> <span data-ttu-id="b8688-144">Inoltre, eventuali risultati indesiderati dovrebbero essere imprevisti o imprevisti e non essere facilmente corretti.</span><span class="sxs-lookup"><span data-stu-id="b8688-144">Additionally, any undesirable results should be unexpected or unintended, and not easily corrected.</span></span> <span data-ttu-id="b8688-145">In caso contrario, è possibile che qualsiasi errore dell'utente possa comportare la perdita di dati o un potenziale problema di qualche tipo e causare un avviso.</span><span class="sxs-lookup"><span data-stu-id="b8688-145">Otherwise, just about any user mistake could be construed to result in data loss or a potential problem of some kind and merit a warning.</span></span>

### <a name="characteristics-of-good-warnings"></a><span data-ttu-id="b8688-146">Caratteristiche degli avvisi di qualità</span><span class="sxs-lookup"><span data-stu-id="b8688-146">Characteristics of good warnings</span></span>

<span data-ttu-id="b8688-147">Avvisi di qualità:</span><span class="sxs-lookup"><span data-stu-id="b8688-147">Good warnings:</span></span>

-   <span data-ttu-id="b8688-148">**Coinvolgere il rischio.**</span><span class="sxs-lookup"><span data-stu-id="b8688-148">**Involve risk.**</span></span> <span data-ttu-id="b8688-149">Gli avvisi di qualità avvisano gli utenti di qualcosa di significativo.</span><span class="sxs-lookup"><span data-stu-id="b8688-149">Good warnings alert users of something significant.</span></span>

<span data-ttu-id="b8688-150">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-150">**Incorrect:**</span></span>

![<span data-ttu-id="b8688-151">screenshot di 'do you want to exit?'</span><span class="sxs-lookup"><span data-stu-id="b8688-151">screen shot of 'do you want to exit?'</span></span> <span data-ttu-id="b8688-152">warning</span><span class="sxs-lookup"><span data-stu-id="b8688-152">warning</span></span> ](images/mess-warn-image3.png)

<span data-ttu-id="b8688-153">E allora?</span><span class="sxs-lookup"><span data-stu-id="b8688-153">So what?</span></span> <span data-ttu-id="b8688-154">Questa conferma presuppone che gli utenti spesso escono dai programmi per errore.</span><span class="sxs-lookup"><span data-stu-id="b8688-154">This confirmation assumes that users often exit programs by accident.</span></span>

-   <span data-ttu-id="b8688-155">**Avere rilevanza immediata.**</span><span class="sxs-lookup"><span data-stu-id="b8688-155">**Have immediate relevance.**</span></span> <span data-ttu-id="b8688-156">Non solo gli utenti devono fare attenzione, ma ora devono fare attenzione.</span><span class="sxs-lookup"><span data-stu-id="b8688-156">Not only do users have to care, they have to care now.</span></span> <span data-ttu-id="b8688-157">Gli utenti in genere non sono interessati ai problemi che potrebbero avere in seguito, purché possano lavorare ora.</span><span class="sxs-lookup"><span data-stu-id="b8688-157">Users typically aren't interested in problems they might have later as long as they can do their work now.</span></span>

<span data-ttu-id="b8688-158">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-158">**Incorrect:**</span></span>

![<span data-ttu-id="b8688-159">Screenshot dell'avviso di batteria in esaurimento in tre ore</span><span class="sxs-lookup"><span data-stu-id="b8688-159">screen shot of battery-low-in-three-hours warning</span></span> ](images/mess-warn-image4.png)

<span data-ttu-id="b8688-160">In questo caso, è meglio solo avvisare l'utente in tre ore.</span><span class="sxs-lookup"><span data-stu-id="b8688-160">In this case, it's better just to warn the user in three hours.</span></span>

-   <span data-ttu-id="b8688-161">**Portare all'azione.**</span><span class="sxs-lookup"><span data-stu-id="b8688-161">**Lead to action.**</span></span> <span data-ttu-id="b8688-162">Come risultato dell'avviso, gli utenti devono eseguire o essere a conoscenza di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="b8688-162">There is something users must do or be aware of as the result of the warning.</span></span> <span data-ttu-id="b8688-163">Potrebbe essere necessario eseguire un'azione ora o in un certo momento nell'immediato futuro.</span><span class="sxs-lookup"><span data-stu-id="b8688-163">Perhaps they must take an action now or sometime in the immediate future.</span></span> <span data-ttu-id="b8688-164">Probabilmente eseguiranno un'attività in modo diverso di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="b8688-164">Perhaps they will perform a task differently as a result.</span></span> <span data-ttu-id="b8688-165">La conseguenza dell'ignorare l'avviso dovrebbe essere chiara.</span><span class="sxs-lookup"><span data-stu-id="b8688-165">The consequence of ignoring the warning should be clear.</span></span> <span data-ttu-id="b8688-166">Gli avvisi senza azioni fanno solo in modo che gli utenti si senta paranoico.</span><span class="sxs-lookup"><span data-stu-id="b8688-166">Warnings without actions just make users feel paranoid.</span></span>

<span data-ttu-id="b8688-167">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-167">**Incorrect:**</span></span>

![<span data-ttu-id="b8688-168">Screenshot dell'avviso "Live Messenger in esecuzione"</span><span class="sxs-lookup"><span data-stu-id="b8688-168">screen shot of 'live messenger is running' warning</span></span> ](images/mess-warn-image5.png)

<span data-ttu-id="b8688-169">Perché questa notifica è un avviso?</span><span class="sxs-lookup"><span data-stu-id="b8688-169">Why is this notification a warning?</span></span> <span data-ttu-id="b8688-170">Cosa dovrebbero fare gli utenti (oltre alla preoccupazione)?</span><span class="sxs-lookup"><span data-stu-id="b8688-170">What are users supposed to do (beside worry)?</span></span>

-   <span data-ttu-id="b8688-171">**Non sono ovvi.**</span><span class="sxs-lookup"><span data-stu-id="b8688-171">**Are not obvious.**</span></span> <span data-ttu-id="b8688-172">Non visualizzare un avviso che indica la conseguenza ovvia di un'azione.</span><span class="sxs-lookup"><span data-stu-id="b8688-172">Don't display a warning to state the obvious consequence of an action.</span></span> <span data-ttu-id="b8688-173">Si supponga, ad esempio, che gli utenti comprendono le conseguenze del non completamento di un'attività.</span><span class="sxs-lookup"><span data-stu-id="b8688-173">For example, assume users understand the consequences of not completing a task.</span></span>

<span data-ttu-id="b8688-174">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-174">**Incorrect:**</span></span>

![<span data-ttu-id="b8688-175">Screenshot dell'uscita dalla procedura guidata? Avviso</span><span class="sxs-lookup"><span data-stu-id="b8688-175">screen shot of do you want to exit wizard? warning</span></span> ](images/mess-warn-image6.png)

<span data-ttu-id="b8688-176">L'annullamento di una procedura guidata incompleta significa che l'attività non viene completata... chi ha conosciuto?</span><span class="sxs-lookup"><span data-stu-id="b8688-176">Canceling an incomplete wizard means the task doesn't get done...who knew?</span></span>

-   <span data-ttu-id="b8688-177">**Si verificano raramente.**</span><span class="sxs-lookup"><span data-stu-id="b8688-177">**Occur infrequently.**</span></span> <span data-ttu-id="b8688-178">Gli avvisi costanti diventano rapidamente inefficaci e fastidiosi.</span><span class="sxs-lookup"><span data-stu-id="b8688-178">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="b8688-179">Gli utenti spesso si concentrano più sull'eliminazione dell'avviso che sulla risoluzione del problema.</span><span class="sxs-lookup"><span data-stu-id="b8688-179">Users often become more focused on getting rid of the warning than addressing the problem.</span></span>

<span data-ttu-id="b8688-180">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-180">**Incorrect:**</span></span>

![<span data-ttu-id="b8688-181">Screenshot dell'avviso di aggiornamento delle firme antivirus</span><span class="sxs-lookup"><span data-stu-id="b8688-181">screen shot of 'update virus signatures' warning</span></span> ](images/mess-warn-image7.png)

<span data-ttu-id="b8688-182">È più probabile che gli utenti si concentrino sull'eliminazione dell'avviso rispetto alla risoluzione del problema sottostante.</span><span class="sxs-lookup"><span data-stu-id="b8688-182">Users are more likely to focus on getting rid of the warning than fixing the underlying problem.</span></span>

<span data-ttu-id="b8688-183">Un messaggio che non ha queste caratteristiche potrebbe comunque essere un messaggio positivo, ma non un avviso.</span><span class="sxs-lookup"><span data-stu-id="b8688-183">A message that doesn't have these characteristics might still be a good message, just not a good warning.</span></span>

### <a name="determine-the-appropriate-message-type"></a><span data-ttu-id="b8688-184">Determinare il tipo di messaggio appropriato</span><span class="sxs-lookup"><span data-stu-id="b8688-184">Determine the appropriate message type</span></span>

<span data-ttu-id="b8688-185">Alcuni problemi possono essere presentati come un errore, un avviso o informazioni, a seconda dell'enfasi e della formulazione.</span><span class="sxs-lookup"><span data-stu-id="b8688-185">Some issues can be presented as an error, warning, or information, depending on the emphasis and phrasing.</span></span> <span data-ttu-id="b8688-186">Si supponga, ad esempio, che una pagina Web non possa caricare un controllo ActiveX non firmato in base alla configurazione corrente Internet Explorer Windows:</span><span class="sxs-lookup"><span data-stu-id="b8688-186">For example, suppose a Web page cannot load an unsigned ActiveX control based on the current Windows Internet Explorer configuration:</span></span>

-   <span data-ttu-id="b8688-187">**Errore.**</span><span class="sxs-lookup"><span data-stu-id="b8688-187">**Error.**</span></span> <span data-ttu-id="b8688-188">"Questa pagina non può caricare un controllo ActiveX non firmato".</span><span class="sxs-lookup"><span data-stu-id="b8688-188">"This page cannot load an unsigned ActiveX control."</span></span> <span data-ttu-id="b8688-189">Si è formulato come un problema esistente.</span><span class="sxs-lookup"><span data-stu-id="b8688-189">(Phrased as an existing problem.)</span></span>
-   <span data-ttu-id="b8688-190">**Avviso.**</span><span class="sxs-lookup"><span data-stu-id="b8688-190">**Warning.**</span></span> <span data-ttu-id="b8688-191">"Questa pagina potrebbe non comportarsi come previsto perché Windows Internet Explorer non è configurato per caricare controlli ActiveX non firmati."</span><span class="sxs-lookup"><span data-stu-id="b8688-191">"This page might not behave as expected because Windows Internet Explorer isn't configured to load unsigned ActiveX controls."</span></span> <span data-ttu-id="b8688-192">o "Consenti a questa pagina di installare un controllo ActiveX non firmato?</span><span class="sxs-lookup"><span data-stu-id="b8688-192">or "Allow this page to install an unsigned ActiveX Control?</span></span> <span data-ttu-id="b8688-193">Questa operazione da origini non attendibili può danneggiare il computer."</span><span class="sxs-lookup"><span data-stu-id="b8688-193">Doing so from untrusted sources may harm your computer."</span></span> <span data-ttu-id="b8688-194">Entrambe formulate come condizioni che possono causare problemi futuri.</span><span class="sxs-lookup"><span data-stu-id="b8688-194">(Both phrased as conditions that may cause future problems.)</span></span>
-   <span data-ttu-id="b8688-195">**Informazioni.**</span><span class="sxs-lookup"><span data-stu-id="b8688-195">**Information.**</span></span> <span data-ttu-id="b8688-196">"È stato configurato Windows Internet Explorer per bloccare i controlli ActiveX non firmati".</span><span class="sxs-lookup"><span data-stu-id="b8688-196">"You have configured Windows Internet Explorer to block unsigned ActiveX controls."</span></span> <span data-ttu-id="b8688-197">(formulata come dichiarazione di fatto).</span><span class="sxs-lookup"><span data-stu-id="b8688-197">(Phrased as a statement of fact.)</span></span>

<span data-ttu-id="b8688-198">**Per determinare il tipo di messaggio appropriato, concentrarsi sull'aspetto più importante del problema che gli utenti devono conoscere o su cui intervenire.**</span><span class="sxs-lookup"><span data-stu-id="b8688-198">**To determine the appropriate message type, focus on the most important aspect of the issue that users need to know or act upon.**</span></span> <span data-ttu-id="b8688-199">In genere, se un problema impedisce all'utente di procedere, è necessario presentarlo come errore. se l'utente può procedere, presentarlo come avviso.</span><span class="sxs-lookup"><span data-stu-id="b8688-199">Typically, if an issue blocks the user from proceeding, you should present it as an error; if the user can proceed, present it as a warning.</span></span> <span data-ttu-id="b8688-200">Creare [l'istruzione principale](text-ui.md) o altro testo corrispondente in base a tale stato attivo, quindi scegliere un'icona[(standard](vis-std-icons.md) o altro) corrispondente al testo.</span><span class="sxs-lookup"><span data-stu-id="b8688-200">Craft the [main instruction](text-ui.md) or other corresponding text based on that focus, then choose an icon ([standard](vis-std-icons.md) or otherwise) that matches the text.</span></span> <span data-ttu-id="b8688-201">Il testo dell'istruzione principale e le icone devono sempre corrispondere.</span><span class="sxs-lookup"><span data-stu-id="b8688-201">The main instruction text and icons should always match.</span></span>

### <a name="be-specific"></a><span data-ttu-id="b8688-202">Essere specifici</span><span class="sxs-lookup"><span data-stu-id="b8688-202">Be specific</span></span>

<span data-ttu-id="b8688-203">Gli avvisi sono più interessanti quando le informazioni seguenti sono specifiche e chiare:</span><span class="sxs-lookup"><span data-stu-id="b8688-203">Warnings are more compelling when the following information is specific and clear:</span></span>

-   <span data-ttu-id="b8688-204">Origine dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="b8688-204">The source of the warning.</span></span>
-   <span data-ttu-id="b8688-205">Condizione specifica e potenziale problema.</span><span class="sxs-lookup"><span data-stu-id="b8688-205">The specific condition and potential problem.</span></span>
-   <span data-ttu-id="b8688-206">Che cosa deve fare l'utente al riguardo.</span><span class="sxs-lookup"><span data-stu-id="b8688-206">What the user should do about it.</span></span>
-   <span data-ttu-id="b8688-207">Cosa accade se l'utente non fa nulla.</span><span class="sxs-lookup"><span data-stu-id="b8688-207">What happens if the user doesn't do anything.</span></span>

<span data-ttu-id="b8688-208">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-208">**Incorrect:**</span></span>

![<span data-ttu-id="b8688-209">Screenshot di un avviso vago di rischio significativo</span><span class="sxs-lookup"><span data-stu-id="b8688-209">screen shot of vague warning of significant risk</span></span> ](images/mess-warn-image8.png)

<span data-ttu-id="b8688-210">In questo esempio, qual è il potenziale problema?</span><span class="sxs-lookup"><span data-stu-id="b8688-210">In this example, what is the potential problem?</span></span> <span data-ttu-id="b8688-211">Cosa dovrebbe fare l'utente, oltre a non usare il proiettore in rete?</span><span class="sxs-lookup"><span data-stu-id="b8688-211">What is the user supposed to do, aside from not using the projector over the network?</span></span> <span data-ttu-id="b8688-212">Senza informazioni più specifiche, tutto ciò che l'utente può fare è provare a procedere.</span><span class="sxs-lookup"><span data-stu-id="b8688-212">Without more specific information, all the user can do is feel bad about proceeding.</span></span>

<span data-ttu-id="b8688-213">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-213">**Correct:**</span></span>

![<span data-ttu-id="b8688-214">Screenshot di avviso relativo a problemi e conseguenze</span><span class="sxs-lookup"><span data-stu-id="b8688-214">screen shot of warning of problem and consequences</span></span> ](images/mess-warn-image9.png)

<span data-ttu-id="b8688-215">In questo esempio il problema e le conseguenze sono chiari.</span><span class="sxs-lookup"><span data-stu-id="b8688-215">In this example, the problem and consequences are clear.</span></span>

<span data-ttu-id="b8688-216">A volte esiste un potenziale problema legittimo che è importante informare gli utenti, ma la soluzione e le conseguenze non sono note con certezza.</span><span class="sxs-lookup"><span data-stu-id="b8688-216">Sometimes there is a legitimate potential problem worthy of informing users about, but the solution and consequences aren't known for sure.</span></span> <span data-ttu-id="b8688-217">Anziché fornire un avviso vago, essere specifici fornendo le informazioni più probabili o l'esempio più comune.</span><span class="sxs-lookup"><span data-stu-id="b8688-217">Rather than give a vague warning, be specific by giving the most likely information or the most common example.</span></span>

<span data-ttu-id="b8688-218">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-218">**Correct:**</span></span>

![<span data-ttu-id="b8688-219">Screenshot dell'avviso di errore di rete e delle soluzioni</span><span class="sxs-lookup"><span data-stu-id="b8688-219">screen shot of network error warning and solutions</span></span> ](images/mess-warn-image10.png)

<span data-ttu-id="b8688-220">In questo esempio l'avviso viene reso specifico fornendo la soluzione più probabile.</span><span class="sxs-lookup"><span data-stu-id="b8688-220">In this example, the warning is made specific by providing the most likely solution.</span></span>

<span data-ttu-id="b8688-221">Tuttavia, in questi casi, usare una formulazione che indica che esistono altre possibilità.</span><span class="sxs-lookup"><span data-stu-id="b8688-221">However, in such cases, use wording that indicates that there are other possibilities.</span></span> <span data-ttu-id="b8688-222">In caso contrario, gli utenti potrebbero essere in errore.</span><span class="sxs-lookup"><span data-stu-id="b8688-222">Otherwise, users might be misled.</span></span>

<span data-ttu-id="b8688-223">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-223">**Incorrect:**</span></span>

![<span data-ttu-id="b8688-224">Screenshot dell'avviso di scollegamento del cavo di rete</span><span class="sxs-lookup"><span data-stu-id="b8688-224">screen shot of network cable unplugged warning</span></span> ](images/mess-warn-image11.png)

<span data-ttu-id="b8688-225">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-225">**Correct:**</span></span>

![<span data-ttu-id="b8688-226">Screenshot del cavo potrebbe essere unplugged warning</span><span class="sxs-lookup"><span data-stu-id="b8688-226">screen shot of cable might be unplugged warning</span></span> ](images/mess-warn-image12.png)

<span data-ttu-id="b8688-227">Nell'esempio non corretto, gli utenti saranno confusi se il cavo è chiaramente collegato.</span><span class="sxs-lookup"><span data-stu-id="b8688-227">In the incorrect example, users will be confused if the cable is clearly plugged in.</span></span>

<span data-ttu-id="b8688-228">**Se si eservino solo due operazioni...**</span><span class="sxs-lookup"><span data-stu-id="b8688-228">**If you do only two things...**</span></span>

1. <span data-ttu-id="b8688-229">Non sopravavare.</span><span class="sxs-lookup"><span data-stu-id="b8688-229">Don't overwarn.</span></span> <span data-ttu-id="b8688-230">Limitare gli avvisi alle condizioni che comportano rischi e sono immediatamente rilevanti, utilizzabili, non ovvie e poco frequenti.</span><span class="sxs-lookup"><span data-stu-id="b8688-230">Limit warnings to conditions that involve risk and are immediately relevant, actionable, not obvious, and infrequent.</span></span> <span data-ttu-id="b8688-231">In caso contrario, rimuovere o riformizza il messaggio.</span><span class="sxs-lookup"><span data-stu-id="b8688-231">Otherwise, remove or rephrase the message.</span></span>

2. <span data-ttu-id="b8688-232">Fornire informazioni specifiche e utili.</span><span class="sxs-lookup"><span data-stu-id="b8688-232">Provide specific, useful information.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="b8688-233">Modelli di utilizzo</span><span class="sxs-lookup"><span data-stu-id="b8688-233">Usage patterns</span></span>

<span data-ttu-id="b8688-234">Gli avvisi hanno diversi modelli di utilizzo:</span><span class="sxs-lookup"><span data-stu-id="b8688-234">Warnings have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b8688-235"><strong>Informazioni</strong></span><span class="sxs-lookup"><span data-stu-id="b8688-235"><strong>Awareness</strong></span></span><br/> <span data-ttu-id="b8688-236">Rendere l'utente a conoscenza di una condizione o di un potenziale problema, ma l'utente potrebbe non avere a che fare ora.</span><span class="sxs-lookup"><span data-stu-id="b8688-236">Make user aware of a condition or potential problem, but user may not have to do anything now.</span></span> <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> <span data-ttu-id="b8688-237">Esempi di avvisi di sensibilizzazione.</span><span class="sxs-lookup"><span data-stu-id="b8688-237">Examples of awareness warnings.</span></span><br/> <span data-ttu-id="b8688-238">Gli avvisi di sensibilizzazione hanno la presentazione seguente:</span><span class="sxs-lookup"><span data-stu-id="b8688-238">Awareness warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="b8688-239"><strong>Istruzione principale:</strong> Descrivere la condizione o il potenziale problema.</span><span class="sxs-lookup"><span data-stu-id="b8688-239"><strong>Main instruction:</strong> Describe the condition or potential problem.</span></span></li>
<li><span data-ttu-id="b8688-240"><strong>Istruzioni supplementari:</strong> Spiegare l'implicazione e il motivo per cui è importante.</span><span class="sxs-lookup"><span data-stu-id="b8688-240"><strong>Supplemental instruction:</strong> Explain the implication and why it is important.</span></span></li>
<li><span data-ttu-id="b8688-241"><strong>Pulsanti commit:</strong> Vicino.</span><span class="sxs-lookup"><span data-stu-id="b8688-241"><strong>Commit buttons:</strong> Close.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8688-242"><strong>Prevenzione degli errori</strong></span><span class="sxs-lookup"><span data-stu-id="b8688-242"><strong>Error prevention</strong></span></span><br/> <span data-ttu-id="b8688-243">Rendere gli utenti consapevoli delle informazioni che potrebbero impedire un problema, soprattutto quando si effettuano scelte.</span><span class="sxs-lookup"><span data-stu-id="b8688-243">Make user aware of information that might prevent a problem, especially when making choices.</span></span> <br/></td>
<td><span data-ttu-id="b8688-244">Gli avvisi di prevenzione degli errori vengono presentati meglio usando un'icona di avviso sul posto e un testo esplicativo.</span><span class="sxs-lookup"><span data-stu-id="b8688-244">Error prevention warnings are best presented using an in-place warning icon and explanatory text.</span></span> <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> <span data-ttu-id="b8688-245">Esempi di avvisi di prevenzione degli errori.</span><span class="sxs-lookup"><span data-stu-id="b8688-245">Examples of error prevention warnings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b8688-246"><strong>Problema imminente</strong></span><span class="sxs-lookup"><span data-stu-id="b8688-246"><strong>Imminent problem</strong></span></span><br/> <span data-ttu-id="b8688-247">L'utente deve eseguire ora un'operazione per evitare un problema imminente.</span><span class="sxs-lookup"><span data-stu-id="b8688-247">The user needs to do something now to prevent an imminent problem.</span></span> <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> <span data-ttu-id="b8688-248">Esempio di avviso di problema imminente.</span><span class="sxs-lookup"><span data-stu-id="b8688-248">An example of an imminent problem warning.</span></span><br/> <span data-ttu-id="b8688-249">Gli avvisi di problema imminenti hanno la presentazione seguente:</span><span class="sxs-lookup"><span data-stu-id="b8688-249">Imminent problem warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="b8688-250"><strong>Istruzione principale:</strong> Descrivere l'operazione che l'utente deve eseguire ora.</span><span class="sxs-lookup"><span data-stu-id="b8688-250"><strong>Main instruction:</strong> Describe what the user needs to do now.</span></span></li>
<li><span data-ttu-id="b8688-251"><strong>Istruzioni supplementari:</strong> Spiegare la condizione e il motivo per cui è importante.</span><span class="sxs-lookup"><span data-stu-id="b8688-251"><strong>Supplemental instruction:</strong> Explain the condition and why it is important.</span></span></li>
<li><span data-ttu-id="b8688-252"><strong>Pulsanti commit:</strong> Un pulsante di comando o un collegamento di comando per ogni opzione oppure OK se l'azione si verifica all'esterno della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b8688-252"><strong>Commit buttons:</strong> A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8688-253"><strong>Conferma dell'azione rischiosa</strong></span><span class="sxs-lookup"><span data-stu-id="b8688-253"><strong>Risky action confirmation</strong></span></span><br/> <span data-ttu-id="b8688-254">Verificare che l'utente voglia procedere con un'azione che presenta un rischio e non può essere facilmente annullata.</span><span class="sxs-lookup"><span data-stu-id="b8688-254">Confirm that the user wants to proceed with an action that has some risk and can't be easily undone.</span></span> <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> <span data-ttu-id="b8688-255">Esempio di conferma dell'azione rischiosa.</span><span class="sxs-lookup"><span data-stu-id="b8688-255">An example of risky action confirmation.</span></span><br/> <span data-ttu-id="b8688-256">Le conferme di azioni rischiose hanno la presentazione seguente:</span><span class="sxs-lookup"><span data-stu-id="b8688-256">Risky action confirmations have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="b8688-257"><strong>Istruzione principale:</strong> Porre una domanda per determinare se l'utente vuole procedere.</span><span class="sxs-lookup"><span data-stu-id="b8688-257"><strong>Main instruction:</strong> Ask a question to determine if the user wants to proceed.</span></span></li>
<li><span data-ttu-id="b8688-258"><strong>Istruzioni supplementari:</strong> Spiegare i motivi non ovvi per cui l'utente potrebbe non voler procedere.</span><span class="sxs-lookup"><span data-stu-id="b8688-258"><strong>Supplemental instruction:</strong> Explain any non-obvious reasons why the user might not want to proceed.</span></span></li>
<li><span data-ttu-id="b8688-259"><strong>Pulsanti commit:</strong> Sì, No.</span><span class="sxs-lookup"><span data-stu-id="b8688-259"><strong>Commit buttons:</strong> Yes, No.</span></span></li>
</ul>
<span data-ttu-id="b8688-260">Per linee guida su questo modello, vedere <a href="mess-confirm.md">Conferme</a>.</span><span class="sxs-lookup"><span data-stu-id="b8688-260">For guidelines on this pattern, see <a href="mess-confirm.md">Confirmations</a>.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="b8688-261">Indicazioni</span><span class="sxs-lookup"><span data-stu-id="b8688-261">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="b8688-262">Presentazione</span><span class="sxs-lookup"><span data-stu-id="b8688-262">Presentation</span></span>

-   <span data-ttu-id="b8688-263">**Scegliere l'interfaccia utente della presentazione in base al tipo di informazioni:**</span><span class="sxs-lookup"><span data-stu-id="b8688-263">**Choose the presentation UI based on the type of information:**</span></span>



| <span data-ttu-id="b8688-264">Interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="b8688-264">User interface</span></span>  | <span data-ttu-id="b8688-265">Utilizzo ottimale per</span><span class="sxs-lookup"><span data-stu-id="b8688-265">Best used for</span></span> |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8688-266">Finestre di dialogo modali</span><span class="sxs-lookup"><span data-stu-id="b8688-266">Modal dialog boxes</span></span><br/> | <span data-ttu-id="b8688-267">Avvisi critici (incluse le conferme) a cui gli utenti devono rispondere ora.</span><span class="sxs-lookup"><span data-stu-id="b8688-267">Critical warnings (including confirmations) that users must respond to now.</span></span><br/>                                                 |
| <span data-ttu-id="b8688-268">Sul posto</span><span class="sxs-lookup"><span data-stu-id="b8688-268">In-place</span></span><br/>           | <span data-ttu-id="b8688-269">Informazioni che potrebbero impedire un problema, soprattutto quando gli utenti effettuano scelte.</span><span class="sxs-lookup"><span data-stu-id="b8688-269">Information that might prevent a problem, especially when users are making choices.</span></span><br/>                                         |
| <span data-ttu-id="b8688-270">Banner</span><span class="sxs-lookup"><span data-stu-id="b8688-270">Banners</span></span><br/>            | <span data-ttu-id="b8688-271">Informazioni che potrebbero impedire un problema, soprattutto quando sono correlate al completamento di un'attività.</span><span class="sxs-lookup"><span data-stu-id="b8688-271">Information that might prevent a problem, especially when related to completing a task.</span></span><br/>                                     |
| <span data-ttu-id="b8688-272">Notifiche</span><span class="sxs-lookup"><span data-stu-id="b8688-272">Notifications</span></span><br/>      | <span data-ttu-id="b8688-273">Eventi significativi o stato che possono essere ignorati in modo sicuro, almeno temporaneamente.</span><span class="sxs-lookup"><span data-stu-id="b8688-273">Significant events or status that can be safely ignored, at least temporarily.</span></span><br/>                                              |
| <span data-ttu-id="b8688-274">Palloncini</span><span class="sxs-lookup"><span data-stu-id="b8688-274">Balloons</span></span><br/>           | <span data-ttu-id="b8688-275">Un controllo si trova in uno stato che influisce sull'input.</span><span class="sxs-lookup"><span data-stu-id="b8688-275">A control is in a state that affects input.</span></span> <span data-ttu-id="b8688-276">Questo stato è probabilmente imprevisto e l'utente potrebbe non rendersi conto che l'input è interessato.</span><span class="sxs-lookup"><span data-stu-id="b8688-276">This state is likely unintended and the user may not realize input is affected.</span></span><br/> |



 

-   <span data-ttu-id="b8688-277">**Per le finestre di dialogo modali:**</span><span class="sxs-lookup"><span data-stu-id="b8688-277">**For modal dialog boxes:**</span></span>
    -   <span data-ttu-id="b8688-278">**Usare le finestre di dialogo delle attività quando appropriato per ottenere un aspetto e un layout coerenti.**</span><span class="sxs-lookup"><span data-stu-id="b8688-278">**Use task dialogs whenever appropriate to achieve a consistent look and layout.**</span></span> <span data-ttu-id="b8688-279">Le finestre di dialogo delle attività richiedono Windows Vista o versioni successive, quindi non sono adatte alle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="b8688-279">Task dialogs require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span>
    -   <span data-ttu-id="b8688-280">**Visualizzare un solo messaggio di avviso per ogni condizione.**</span><span class="sxs-lookup"><span data-stu-id="b8688-280">**Display only one warning message per condition.**</span></span> <span data-ttu-id="b8688-281">Ad esempio, visualizzare un singolo avviso che spiega completamente una condizione anziché descriverla un dettaglio alla volta per ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="b8688-281">For example, display a single warning that completely explains a condition instead of describing it one detail at a time per message.</span></span> <span data-ttu-id="b8688-282">La visualizzazione di una sequenza di finestre di dialogo di avviso per una singola condizione è fonte di confusione e fastidiosa.</span><span class="sxs-lookup"><span data-stu-id="b8688-282">Displaying a sequence of warning dialogs for a single condition is confusing and annoying.</span></span>
    -   <span data-ttu-id="b8688-283">**Non visualizzare un avviso più di una volta per ogni condizione.**</span><span class="sxs-lookup"><span data-stu-id="b8688-283">**Don't display a warning more than once per condition.**</span></span> <span data-ttu-id="b8688-284">Gli avvisi costanti diventano rapidamente inefficaci e fastidiosi.</span><span class="sxs-lookup"><span data-stu-id="b8688-284">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="b8688-285">Gli utenti spesso si concentrano più sull'eliminazione dell'avviso che sulla risoluzione del problema.</span><span class="sxs-lookup"><span data-stu-id="b8688-285">Users often become more focused on getting rid of the warning than addressing the problem.</span></span> <span data-ttu-id="b8688-286">Se è necessario avvisare ripetutamente per una singola condizione, usare [l'escalation progressiva.](mess-notif.md)</span><span class="sxs-lookup"><span data-stu-id="b8688-286">If you must warn repeatedly for a single condition, use [progressive escalation](mess-notif.md).</span></span>
-   <span data-ttu-id="b8688-287">**Non accompagnare gli avvisi con un effetto sonoro o un segnale acustico.**</span><span class="sxs-lookup"><span data-stu-id="b8688-287">**Don't accompany warnings with a sound effect or beep.**</span></span> <span data-ttu-id="b8688-288">Questa operazione è insoddura e non necessaria.</span><span class="sxs-lookup"><span data-stu-id="b8688-288">Doing so is jarring and unnecessary.</span></span>
    -   <span data-ttu-id="b8688-289">**Eccezione:** Se l'utente deve rispondere immediatamente, è possibile usare un effetto sonoro.</span><span class="sxs-lookup"><span data-stu-id="b8688-289">**Exception:** If the user must respond immediately, you can use a sound effect.</span></span>

### <a name="icons"></a><span data-ttu-id="b8688-290">Icone</span><span class="sxs-lookup"><span data-stu-id="b8688-290">Icons</span></span>

-   <span data-ttu-id="b8688-291">Non posizionare un'icona di avviso nella barra del titolo di una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b8688-291">Don't place a warning icon in the title bar of a dialog box.</span></span>
-   <span data-ttu-id="b8688-292">**Usare un'icona di avviso.**</span><span class="sxs-lookup"><span data-stu-id="b8688-292">**Use a warning icon.**</span></span> <span data-ttu-id="b8688-293">Eccezioni:</span><span class="sxs-lookup"><span data-stu-id="b8688-293">Exceptions:</span></span>
    -   <span data-ttu-id="b8688-294">Se l'avviso è relativo a una funzionalità con un'icona, è possibile usare l'icona della funzionalità con una sovrapposizione di avviso.</span><span class="sxs-lookup"><span data-stu-id="b8688-294">If the warning is for a feature that has an icon, you can use the feature icon with a warning overlay.</span></span>

        <span data-ttu-id="b8688-295">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-295">**Correct:**</span></span>

        ![<span data-ttu-id="b8688-296">Screenshot dell'icona di blocco con sovrimpressione dell'icona di avviso</span><span class="sxs-lookup"><span data-stu-id="b8688-296">screen shot of lock icon with warning icon overlay</span></span> ](images/mess-warn-image21.png)

        <span data-ttu-id="b8688-297">In questo esempio l'icona della funzionalità ha una sovrapposizione di avviso.</span><span class="sxs-lookup"><span data-stu-id="b8688-297">In this example, the feature icon has a warning overlay.</span></span>

-   <span data-ttu-id="b8688-298">Per le finestre di dialogo modali con una nota a piè di pagina di avviso, inserire l'icona di avviso nella nota a piè di pagina anziché nell'area del contenuto.</span><span class="sxs-lookup"><span data-stu-id="b8688-298">For modal dialog boxes with a warning footnote, put the warning icon in the footnote instead of the content area.</span></span>

    <span data-ttu-id="b8688-299">**Corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-299">**Correct:**</span></span>

    ![<span data-ttu-id="b8688-300">Screenshot dell'icona di avviso nella nota a piè di pagina della finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="b8688-300">screen shot of warning icon in dialog-box footnote</span></span> ](images/mess-warn-image22.png)

    <span data-ttu-id="b8688-301">In questo esempio la nota a piè di pagina contiene l'icona di avviso.</span><span class="sxs-lookup"><span data-stu-id="b8688-301">In this example, the footnote has the warning icon.</span></span>

<span data-ttu-id="b8688-302">Per altre linee guida ed esempi, vedere [Icone standard.](vis-std-icons.md)</span><span class="sxs-lookup"><span data-stu-id="b8688-302">For more guidelines and examples, see [Standard Icons](vis-std-icons.md).</span></span>

### <a name="dont-show-this-message-again"></a><span data-ttu-id="b8688-303">Non visualizzare più questo messaggio</span><span class="sxs-lookup"><span data-stu-id="b8688-303">Don't show this message again</span></span>

-   <span data-ttu-id="b8688-304">**Se questa opzione è richiesta da una finestra di dialogo di avviso, riconsiderare l'avviso e la relativa frequenza.**</span><span class="sxs-lookup"><span data-stu-id="b8688-304">**If a warning dialog box needs this option, reconsider the warning and its frequency.**</span></span> <span data-ttu-id="b8688-305">Se ha tutte le caratteristiche di un avviso utile (comporta rischi ed è immediatamente pertinente, fattibile, non ovvio e poco comune), non dovrebbe avere senso per gli utenti sopprimerlo.</span><span class="sxs-lookup"><span data-stu-id="b8688-305">If it has all the characteristics of a good warning (involves risk, and is immediately relevant, actionable, not obvious, and infrequent), it shouldn't make sense for users to suppress it.</span></span>

<span data-ttu-id="b8688-306">Per altre linee guida, vedere [Finestre di dialogo.](win-dialog-box.md)</span><span class="sxs-lookup"><span data-stu-id="b8688-306">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="progressive-disclosure"></a><span data-ttu-id="b8688-307">Rivelazione progressiva</span><span class="sxs-lookup"><span data-stu-id="b8688-307">Progressive disclosure</span></span>

-   <span data-ttu-id="b8688-308">**Se è necessario includere informazioni avanzate in un messaggio di avviso,** rivelarlo usando i pulsanti di divulgazione progressiva (ad esempio, "Mostra dettagli").</span><span class="sxs-lookup"><span data-stu-id="b8688-308">**If you must include advanced information in a warning message, reveal it by using progressive disclosure buttons** (for example, "Show details").</span></span> <span data-ttu-id="b8688-309">Questa operazione semplifica l'avviso per l'utilizzo tipico.</span><span class="sxs-lookup"><span data-stu-id="b8688-309">Doing so simplifies the warning for typical usage.</span></span> <span data-ttu-id="b8688-310">Non nascondere le informazioni necessarie perché gli utenti potrebbero non trovarle.</span><span class="sxs-lookup"><span data-stu-id="b8688-310">Don't hide needed information because users might not find it.</span></span>
-   <span data-ttu-id="b8688-311">**Non usare "Mostra dettagli" a meno che non siano presenti altri dettagli.**</span><span class="sxs-lookup"><span data-stu-id="b8688-311">**Don't use "Show details" unless there really is more detail.**</span></span> <span data-ttu-id="b8688-312">Non solo rievalutare le informazioni esistenti in un formato diverso.</span><span class="sxs-lookup"><span data-stu-id="b8688-312">Don't just restate the existing information in a different format.</span></span>

<span data-ttu-id="b8688-313">Per le linee guida sull'etichettatura, vedere [Diffusione progressiva.](ctrl-progressive-disclosure-controls.md)</span><span class="sxs-lookup"><span data-stu-id="b8688-313">For labeling guidelines, see [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="b8688-314">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="b8688-314">Default values</span></span>

-   <span data-ttu-id="b8688-315">**Selezionare la risposta più sicura, meno distruttiva o più sicura come predefinita.**</span><span class="sxs-lookup"><span data-stu-id="b8688-315">**Select the safest, least destructive, or most secure response to be the default.**</span></span>

## <a name="text"></a><span data-ttu-id="b8688-316">Testo</span><span class="sxs-lookup"><span data-stu-id="b8688-316">Text</span></span>

### <a name="general"></a><span data-ttu-id="b8688-317">Generale</span><span class="sxs-lookup"><span data-stu-id="b8688-317">General</span></span>

-   <span data-ttu-id="b8688-318">**Rimuovere il testo ridondante.**</span><span class="sxs-lookup"><span data-stu-id="b8688-318">**Remove redundant text.**</span></span> <span data-ttu-id="b8688-319">Cercarlo in titoli, istruzioni principali, istruzioni supplementari, aree di contenuto, collegamenti di comando e pulsanti di commit.</span><span class="sxs-lookup"><span data-stu-id="b8688-319">Look for it in titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="b8688-320">In genere, lasciare il testo completo nelle istruzioni e nei controlli interattivi e rimuovere qualsiasi ridondanza dalle altre posizioni.</span><span class="sxs-lookup"><span data-stu-id="b8688-320">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="b8688-321">**Non usare i termini "avviso" o "attenzione" nel testo.**</span><span class="sxs-lookup"><span data-stu-id="b8688-321">**Don't use the terms "warning" or "caution" in the text.**</span></span> <span data-ttu-id="b8688-322">Se [usata correttamente,](vis-std-icons.md)l'icona di avviso comunica sufficientemente che gli utenti devono procedere con cautela.</span><span class="sxs-lookup"><span data-stu-id="b8688-322">When [used correctly](vis-std-icons.md), the warning icon sufficiently communicates that users must proceed with caution.</span></span>

<span data-ttu-id="b8688-323">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-323">**Incorrect:**</span></span>

![<span data-ttu-id="b8688-324">Screenshot dell'uso non necessario di un avviso nel testo</span><span class="sxs-lookup"><span data-stu-id="b8688-324">screen shot of unnecessary use of warning in text</span></span> ](images/mess-warn-image23.png)

<span data-ttu-id="b8688-325">In questo esempio il termine "avviso" non è necessario.</span><span class="sxs-lookup"><span data-stu-id="b8688-325">In this example, the term "warning" is unnecessary.</span></span>

### <a name="titles"></a><span data-ttu-id="b8688-326">Titoli</span><span class="sxs-lookup"><span data-stu-id="b8688-326">Titles</span></span>

-   <span data-ttu-id="b8688-327">**Usare il titolo per identificare il comando o la funzionalità da cui è stato generato l'avviso.**</span><span class="sxs-lookup"><span data-stu-id="b8688-327">**Use the title to identify the command or feature where the warning came from.**</span></span> <span data-ttu-id="b8688-328">Eccezioni:</span><span class="sxs-lookup"><span data-stu-id="b8688-328">Exceptions:</span></span>
    -   <span data-ttu-id="b8688-329">Se viene visualizzato un avviso da molti comandi diversi, prendere in considerazione l'uso del nome del programma.</span><span class="sxs-lookup"><span data-stu-id="b8688-329">If a warning is displayed by many different commands, consider using the program name instead.</span></span>
    -   <span data-ttu-id="b8688-330">Se il titolo sarebbe ridondante o confondere con l'istruzione principale, usare invece il nome del programma.</span><span class="sxs-lookup"><span data-stu-id="b8688-330">If that title would be redundant or confusing with the main instruction, use the program name instead.</span></span>

<span data-ttu-id="b8688-331">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-331">**Incorrect:**</span></span>

![<span data-ttu-id="b8688-332">Screenshot del titolo della finestra di dialogo di avviso di sicurezza</span><span class="sxs-lookup"><span data-stu-id="b8688-332">screen shot of security warning dialog box title</span></span> ](images/mess-warn-image24.png)

<span data-ttu-id="b8688-333">In questo esempio "Avviso di sicurezza" non identifica il comando o la funzionalità da cui è stato generato l'avviso.</span><span class="sxs-lookup"><span data-stu-id="b8688-333">In this example, "Security Warning" doesn't identify the command or feature where the warning came from.</span></span>

-   <span data-ttu-id="b8688-334">**Non usare il titolo per spiegare cosa fare nel** dialogo che è lo scopo dell'istruzione principale.</span><span class="sxs-lookup"><span data-stu-id="b8688-334">**Don't use the title to explain what to do in the dialog** that's the purpose of the main instruction.</span></span>
-   <span data-ttu-id="b8688-335">Usare [l'iniziale maiuscola in stile](glossary.md)titolo, senza terminare la punteggiatura.</span><span class="sxs-lookup"><span data-stu-id="b8688-335">Use [title-style capitalization](glossary.md), without ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="b8688-336">Istruzioni principali</span><span class="sxs-lookup"><span data-stu-id="b8688-336">Main instructions</span></span>

-   <span data-ttu-id="b8688-337">L'istruzione principale per un avviso si basa sul relativo schema progettuale:</span><span class="sxs-lookup"><span data-stu-id="b8688-337">The main instruction for a warning is based on its design pattern:</span></span>



| <span data-ttu-id="b8688-338">Modello</span><span class="sxs-lookup"><span data-stu-id="b8688-338">Pattern</span></span>                        | <span data-ttu-id="b8688-339">Istruzione main</span><span class="sxs-lookup"><span data-stu-id="b8688-339">Main instruction</span></span>                                               |
|--------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="b8688-340">Riconoscimento</span><span class="sxs-lookup"><span data-stu-id="b8688-340">Awareness</span></span><br/>                 | <span data-ttu-id="b8688-341">Descrivere la condizione o il potenziale problema.</span><span class="sxs-lookup"><span data-stu-id="b8688-341">Describe the condition or potential problem.</span></span><br/>              |
| <span data-ttu-id="b8688-342">Problema imminente</span><span class="sxs-lookup"><span data-stu-id="b8688-342">Imminent problem</span></span><br/>          | <span data-ttu-id="b8688-343">Descrivere le esigenze dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b8688-343">Describe what the user needs to do now.</span></span><br/>                   |
| <span data-ttu-id="b8688-344">Conferma dell'azione rischiosa</span><span class="sxs-lookup"><span data-stu-id="b8688-344">Risky action confirmation</span></span><br/> | <span data-ttu-id="b8688-345">Porre una domanda per determinare se l'utente vuole procedere.</span><span class="sxs-lookup"><span data-stu-id="b8688-345">Ask a question to determine if the user wants to proceed.</span></span><br/> |



 

-   ![<span data-ttu-id="b8688-346">Screenshot di una notifica di batteria in esaurimento</span><span class="sxs-lookup"><span data-stu-id="b8688-346">screen shot of a low-battery notification</span></span> ](images/mess-warn-image25.png)
-   <span data-ttu-id="b8688-347">In questo esempio la notifica di batteria in esaurimento è un avviso di consapevolezza, quindi l'istruzione principale descrive la condizione.</span><span class="sxs-lookup"><span data-stu-id="b8688-347">In this example, the low battery notification is an awareness warning, so the main instruction describes the condition.</span></span>
-   ![<span data-ttu-id="b8688-348">screenshot dell'avviso di modifica della batteria immediatamente</span><span class="sxs-lookup"><span data-stu-id="b8688-348">screen shot of change battery immediately warning</span></span> ](images/mess-warn-image1.png)
-   <span data-ttu-id="b8688-349">In questo esempio la finestra di dialogo batteria in esaurimento è un problema imminente, quindi l'istruzione principale descrive le attività che l'utente deve eseguire ora.</span><span class="sxs-lookup"><span data-stu-id="b8688-349">In this example, the low battery dialog box is an imminent problem, so the main instruction describes what the user needs to do now.</span></span>
-   <span data-ttu-id="b8688-350">**Usare concisa una sola frase completa.**</span><span class="sxs-lookup"><span data-stu-id="b8688-350">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="b8688-351">Rimuovere l'istruzione principale fino alle informazioni essenziali.</span><span class="sxs-lookup"><span data-stu-id="b8688-351">Strip the main instruction down to the essential information.</span></span> <span data-ttu-id="b8688-352">Se è necessario spiegare altro, usare un'istruzione supplementare.</span><span class="sxs-lookup"><span data-stu-id="b8688-352">If you must explain anything more, use a supplemental instruction.</span></span>
-   <span data-ttu-id="b8688-353">**Usare parole come "ora" e "immediatamente" se l'utente deve agire immediatamente.**</span><span class="sxs-lookup"><span data-stu-id="b8688-353">**Use words like "now" and "immediately" if the user must act immediately.**</span></span> <span data-ttu-id="b8688-354">Non usare queste parole in assenza di urgenza.</span><span class="sxs-lookup"><span data-stu-id="b8688-354">Don't use these words if there is no urgency.</span></span>
-   <span data-ttu-id="b8688-355">**Se sono presenti oggetti coinvolti, specificarne i nomi completi.**</span><span class="sxs-lookup"><span data-stu-id="b8688-355">**Be specific if there are objects involved, give their full names.**</span></span>
-   <span data-ttu-id="b8688-356">Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)</span><span class="sxs-lookup"><span data-stu-id="b8688-356">Use [sentence-style capitalization](glossary.md).</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="b8688-357">Istruzioni supplementari</span><span class="sxs-lookup"><span data-stu-id="b8688-357">Supplemental instructions</span></span>

-   <span data-ttu-id="b8688-358">L'istruzione supplementare per un avviso si basa sul relativo schema progettuale:</span><span class="sxs-lookup"><span data-stu-id="b8688-358">The supplemental instruction for a warning is based on its design pattern:</span></span>



| <span data-ttu-id="b8688-359">Modello</span><span class="sxs-lookup"><span data-stu-id="b8688-359">Pattern</span></span>            | <span data-ttu-id="b8688-360">Istruzione supplementare</span><span class="sxs-lookup"><span data-stu-id="b8688-360">Supplemental instruction</span></span>                                            |
|--------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8688-361">Riconoscimento</span><span class="sxs-lookup"><span data-stu-id="b8688-361">Awareness</span></span><br/>                 | <span data-ttu-id="b8688-362">Spiegare l'implicazione e il motivo per cui è importante.</span><span class="sxs-lookup"><span data-stu-id="b8688-362">Explain the implication and why it is important.</span></span><br/>                        |
| <span data-ttu-id="b8688-363">Problema imminente</span><span class="sxs-lookup"><span data-stu-id="b8688-363">Imminent problem</span></span><br/>          | <span data-ttu-id="b8688-364">Spiegare la condizione e il motivo per cui è importante.</span><span class="sxs-lookup"><span data-stu-id="b8688-364">Explain the condition and why it is important.</span></span><br/>                          |
| <span data-ttu-id="b8688-365">Conferma dell'azione rischiosa</span><span class="sxs-lookup"><span data-stu-id="b8688-365">Risky action confirmation</span></span><br/> | <span data-ttu-id="b8688-366">Spiegare eventuali motivi non ovvi per cui l'utente potrebbe non voler procedere.</span><span class="sxs-lookup"><span data-stu-id="b8688-366">Explain any non-obvious reasons why the user might not want to proceed.</span></span><br/> |



 

-   <span data-ttu-id="b8688-367">**Non ripetere l'istruzione principale con una formulazione leggermente diversa.**</span><span class="sxs-lookup"><span data-stu-id="b8688-367">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="b8688-368">In alternativa, omettere l'istruzione supplementare se non sono presenti altri elementi da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="b8688-368">Instead, omit the supplemental instruction if there is not more to add.</span></span>
-   <span data-ttu-id="b8688-369">Usare frasi complete, lettere maiuscole in stile frase e punteggiatura finale.</span><span class="sxs-lookup"><span data-stu-id="b8688-369">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="b8688-370">Pulsanti di commit</span><span class="sxs-lookup"><span data-stu-id="b8688-370">Commit buttons</span></span>

-   <span data-ttu-id="b8688-371">Per le finestre di dialogo di avviso, i pulsanti di commit si basano sul relativo modello di progettazione:</span><span class="sxs-lookup"><span data-stu-id="b8688-371">For warning dialog boxes, the commit buttons are based on its design pattern:</span></span>



| <span data-ttu-id="b8688-372">Modello</span><span class="sxs-lookup"><span data-stu-id="b8688-372">Pattern</span></span>               | <span data-ttu-id="b8688-373">Pulsanti di commit</span><span class="sxs-lookup"><span data-stu-id="b8688-373">Commit buttons</span></span>        |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8688-374">Riconoscimento</span><span class="sxs-lookup"><span data-stu-id="b8688-374">Awareness</span></span><br/>                 | <span data-ttu-id="b8688-375">Quasi.</span><span class="sxs-lookup"><span data-stu-id="b8688-375">Close.</span></span> <span data-ttu-id="b8688-376">Non usare OK perché suggerisce che i potenziali problemi sono ok.</span><span class="sxs-lookup"><span data-stu-id="b8688-376">Don't use OK because it suggests that potential problems are OK.</span></span><br/>                              |
| <span data-ttu-id="b8688-377">Problema imminente</span><span class="sxs-lookup"><span data-stu-id="b8688-377">Imminent problem</span></span><br/>          | <span data-ttu-id="b8688-378">Un pulsante di comando o un collegamento di comando per ogni opzione oppure OK se l'azione si verifica all'esterno della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b8688-378">A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span><br/> |
| <span data-ttu-id="b8688-379">Conferma dell'azione rischiosa</span><span class="sxs-lookup"><span data-stu-id="b8688-379">Risky action confirmation</span></span><br/> | <span data-ttu-id="b8688-380">Sì, no.</span><span class="sxs-lookup"><span data-stu-id="b8688-380">Yes, No.</span></span><br/>                                                                                             |



 

-   <span data-ttu-id="b8688-381">**Non corretto:**</span><span class="sxs-lookup"><span data-stu-id="b8688-381">**Incorrect:**</span></span>
-   ![<span data-ttu-id="b8688-382">Screenshot della finestra di dialogo di avviso con il pulsante OK</span><span class="sxs-lookup"><span data-stu-id="b8688-382">screen shot of warning dialog box with ok button</span></span> ](images/mess-warn-image26.png)
-   <span data-ttu-id="b8688-383">I problemi non sono ok, quindi usare Close.</span><span class="sxs-lookup"><span data-stu-id="b8688-383">Problems aren't OK, so use Close instead.</span></span>

## <a name="documentation"></a><span data-ttu-id="b8688-384">Documentazione</span><span class="sxs-lookup"><span data-stu-id="b8688-384">Documentation</span></span>

<span data-ttu-id="b8688-385">Quando si fa riferimento agli avvisi:</span><span class="sxs-lookup"><span data-stu-id="b8688-385">When referring to warnings:</span></span>

-   <span data-ttu-id="b8688-386">Se l'avviso pone una domanda, fare riferimento a un avviso in base alla domanda; In caso contrario, usare l'istruzione main.</span><span class="sxs-lookup"><span data-stu-id="b8688-386">If the warning asks a question, refer to a warning by its question; otherwise, use the main instruction.</span></span> <span data-ttu-id="b8688-387">Se la domanda o l'istruzione principale è lunga o dettagliata, riepilogarla.</span><span class="sxs-lookup"><span data-stu-id="b8688-387">If the question or main instruction is long or detailed, summarize it.</span></span>
-   <span data-ttu-id="b8688-388">Se necessario, è possibile fare riferimento a una finestra di dialogo di avviso come messaggio.</span><span class="sxs-lookup"><span data-stu-id="b8688-388">If necessary, you may refer to a warning dialog box as a message.</span></span>
-   <span data-ttu-id="b8688-389">Quando possibile, formattare il testo in grassetto.</span><span class="sxs-lookup"><span data-stu-id="b8688-389">When possible, format the text using bold.</span></span> <span data-ttu-id="b8688-390">In caso contrario, inserire il testo tra virgolette solo se necessario per evitare confusione.</span><span class="sxs-lookup"><span data-stu-id="b8688-390">Otherwise, put the text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="b8688-391">Esempio: nel **messaggio Do you want to display the nonsecure items? (Visualizzare gli elementi non sicuri?)** fare clic su Sì.</span><span class="sxs-lookup"><span data-stu-id="b8688-391">Example: In the **Do you want to display the nonsecure items?** message, click Yes.</span></span>

 

