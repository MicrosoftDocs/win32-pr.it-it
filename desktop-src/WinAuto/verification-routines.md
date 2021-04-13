---
title: Routine di verifica
description: Questa sezione descrive le routine di verifica che possono essere eseguite da controllo dell'accessibilità dell'interfaccia utente per testare l'implementazione dell'accessibilità di un'applicazione.
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78eea821a4c918078c6390e33fa7046de1452f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330215"
---
# <a name="verification-routines"></a><span data-ttu-id="acb68-103">Routine di verifica</span><span class="sxs-lookup"><span data-stu-id="acb68-103">Verification Routines</span></span>

<span data-ttu-id="acb68-104">Questa sezione descrive le routine di verifica che possono essere eseguite da controllo dell'accessibilità dell'interfaccia utente per testare l'implementazione dell'accessibilità di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="acb68-104">This section describes the verification routines that UI Accessibility Checker can run to test an application's accessibility implementation.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="acb68-105">Category</span><span class="sxs-lookup"><span data-stu-id="acb68-105">Category</span></span></th>
<th><span data-ttu-id="acb68-106">Routine</span><span class="sxs-lookup"><span data-stu-id="acb68-106">Routine</span></span></th>
<th><span data-ttu-id="acb68-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acb68-107">Description</span></span></th>
</tr><span data-ttu-id="acb68-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Coerenza</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="acb68-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Consistency</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="acb68-109"><strong>ScreenReader</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-109"><strong>ScreenReader</strong></span></span></td>
<td><span data-ttu-id="acb68-110">Compila tutti gli elementi visibili nella destinazione di verifica e li visualizza in un controllo ListView nell'ordine in cui un'operazione di lettura dello schermo standard li annuncia a un utente.</span><span class="sxs-lookup"><span data-stu-id="acb68-110">Compiles all visible elements in the verification target and displays them in a ListView control in the order that a standard screen reader announces them to a user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acb68-111"><strong>UiaScreenReader</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-111"><strong>UiaScreenReader</strong></span></span></td>
<td><span data-ttu-id="acb68-112">Uguale a <strong>ScreenReader</strong>, ma per le implementazioni di UIA.</span><span class="sxs-lookup"><span data-stu-id="acb68-112">Same as <strong>ScreenReader</strong>, but for UIA implementations.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="acb68-113"><strong>Spostamento</strong>di $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="acb68-113"><strong>Navigation</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="acb68-114"><strong>CheckTreeDepth</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-114"><strong>CheckTreeDepth</strong></span></span></td>
<td><span data-ttu-id="acb68-115">Invia i caratteri di tabulazione (o MAIUSC + TAB) come input alla destinazione di verifica per verificare che l'interfaccia utente della destinazione non sia eccessivamente complessa o inaccessibile mediante la navigazione da tastiera standard.</span><span class="sxs-lookup"><span data-stu-id="acb68-115">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that the target's UI isn't overly complex or inaccessible using standard keyboard navigation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acb68-116"><strong>CheckTabbingUia</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-116"><strong>CheckTabbingUia</strong></span></span></td>
<td><span data-ttu-id="acb68-117">Invia i caratteri di tabulazione (o MAIUSC + TAB) come input alla destinazione di verifica per confermare che tutti gli elementi attivabili nell'interfaccia utente sono raggiungibili in modo ordinato e logico utilizzando la navigazione da tastiera standard.</span><span class="sxs-lookup"><span data-stu-id="acb68-117">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that all focusable elements in the UI are reachable in an orderly, logical fashion using standard keyboard navigation.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="acb68-118"><strong>Proprietà</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="acb68-118"><strong>Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="acb68-119"><strong>CheckRole</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-119"><strong>CheckRole</strong></span></span></td>
<td><span data-ttu-id="acb68-120">Conferma che ogni elemento attivabile nell'interfaccia utente segnala un ruolo di MSAA logico valido e che il controllo ha un valore come richiesto da tale ruolo.</span><span class="sxs-lookup"><span data-stu-id="acb68-120">Confirms that each focusable element in the UI reports a valid, logical MSAA role, and that the control has a value as required by that role.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acb68-121"><strong>CheckState</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-121"><strong>CheckState</strong></span></span></td>
<td><span data-ttu-id="acb68-122">Conferma che ogni elemento attivabile nell'interfaccia utente segnala uno stato MSAA logico valido.</span><span class="sxs-lookup"><span data-stu-id="acb68-122">Confirms that each focusable element in the UI reports a valid, logical MSAA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-123"><strong>Elaborazioni nomecontrollo</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-123"><strong>CheckName</strong></span></span></td>
<td><span data-ttu-id="acb68-124">Conferma che ogni elemento attivabile nell'interfaccia utente segnala un nome di MSAA logico valido.</span><span class="sxs-lookup"><span data-stu-id="acb68-124">Confirms that each focusable element in the UI reports a valid, logical MSAA name.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="acb68-125"><strong>CheckAccessKeys</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-125"><strong>CheckAccessKeys</strong></span></span></td>
<td><span data-ttu-id="acb68-126">Conferma che le chiavi di accesso assegnate agli elementi nella destinazione di verifica sono univoche all'interno della destinazione di verifica.</span><span class="sxs-lookup"><span data-stu-id="acb68-126">Confirms that access keys that are assigned to elements in the verification target are unique within the verification target.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-127"><strong>CheckBoundingRect</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-127"><strong>CheckBoundingRect</strong></span></span></td>
<td><span data-ttu-id="acb68-128">Conferma che ogni elemento attivabile nell'interfaccia utente dispone di un rettangolo di delimitazione che può essere utilizzato come destinazione per l'hit testing.</span><span class="sxs-lookup"><span data-stu-id="acb68-128">Confirms that each focusable element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="acb68-129"><strong>Albero</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="acb68-129"><strong>Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="acb68-130"><strong>CheckParentChild</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-130"><strong>CheckParentChild</strong></span></span></td>
<td><span data-ttu-id="acb68-131">Le relazioni padre e figlio nell'albero degli elementi sono coerenti e prevedibili.</span><span class="sxs-lookup"><span data-stu-id="acb68-131">Parent and child relationships in the element tree are consistent and predictable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-132"><strong>CheckOrphanChildren</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-132"><strong>CheckOrphanChildren</strong></span></span></td>
<td><span data-ttu-id="acb68-133">Conferma che ogni elemento attivabile nell'interfaccia utente segnala un padre MSAA valido.</span><span class="sxs-lookup"><span data-stu-id="acb68-133">Confirms that each focusable element in the UI reports a valid MSAA parent.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="acb68-134"><strong>Proprietà UIA</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="acb68-134"><strong>UIA Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="acb68-135"><strong>CheckNameUIA</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-135"><strong>CheckNameUIA</strong></span></span></td>
<td><span data-ttu-id="acb68-136">Conferma che ogni elemento attivabile nell'interfaccia utente segnala un nome di UIA logico valido.</span><span class="sxs-lookup"><span data-stu-id="acb68-136">Confirms that each focusable element in the UI reports a valid, logical UIA name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-137"><strong>CheckTreeDepthUIA</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-137"><strong>CheckTreeDepthUIA</strong></span></span></td>
<td><span data-ttu-id="acb68-138">Invia i caratteri di tabulazione (o MAIUSC + TAB) come input alla destinazione di verifica per confermare che gli elementi dell'interfaccia utente nell'interfaccia utente della destinazione non sono eccessivamente complessi o inaccessibili tramite la navigazione da tastiera standard.</span><span class="sxs-lookup"><span data-stu-id="acb68-138">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that to UIA elements in the target's UI aren't overly complex or inaccessible using standard keyboard navigation.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="acb68-139"><strong>CheckStateUIA</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-139"><strong>CheckStateUIA</strong></span></span></td>
<td><span data-ttu-id="acb68-140">Conferma che ogni elemento attivabile nell'interfaccia utente segnala uno stato UIA logico valido.</span><span class="sxs-lookup"><span data-stu-id="acb68-140">Confirms that each focusable element in the UI reports a valid, logical UIA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-141"><strong>CheckAccessKeysUIA</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-141"><strong>CheckAccessKeysUIA</strong></span></span></td>
<td><span data-ttu-id="acb68-142">Conferma che gli elementi di pari livello non hanno lo stesso accesso e/o il tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="acb68-142">Confirms that sibling elements do not have the same access and/or accelerator key.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="acb68-143"><strong>CheckBoundingRectUIA</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-143"><strong>CheckBoundingRectUIA</strong></span></span></td>
<td><span data-ttu-id="acb68-144">Conferma che ogni elemento UIA attivabile nell'interfaccia utente dispone di un rettangolo di delimitazione che può essere usato come destinazione per l'hit testing.</span><span class="sxs-lookup"><span data-stu-id="acb68-144">Confirms that each focusable UIA element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-145"><strong>CheckControlTypeUIA</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-145"><strong>CheckControlTypeUIA</strong></span></span></td>
<td><span data-ttu-id="acb68-146">Conferma che ogni elemento attivabile nell'interfaccia utente segnala un tipo di controllo UIA logico valido.</span><span class="sxs-lookup"><span data-stu-id="acb68-146">Confirms that each focusable element in the UI reports a valid, logical UIA control type.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="acb68-147"><strong>Albero UIA</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="acb68-147"><strong>UIA Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="acb68-148"><strong>CheckNavigateUia</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-148"><strong>CheckNavigateUia</strong></span></span></td>
<td><span data-ttu-id="acb68-149">Conferma che il TreeWalker di interfaccia di interfaccia di stato può spostarsi tra gli elementi figlio di un elemento.</span><span class="sxs-lookup"><span data-stu-id="acb68-149">Confirms that the UIA TreeWalker can navigate through an element's children.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-150"><strong>CheckOrphanChildrenUia</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-150"><strong>CheckOrphanChildrenUia</strong></span></span></td>
<td><span data-ttu-id="acb68-151">Conferma che ogni elemento attivabile nell'interfaccia utente segnala un elemento padre dell'elemento del controllo dell'associazione valido.</span><span class="sxs-lookup"><span data-stu-id="acb68-151">Confirms that each focusable element in the UI reports a valid UIA parent.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="acb68-152"><strong>CheckSiblingsUia</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-152"><strong>CheckSiblingsUia</strong></span></span></td>
<td><span data-ttu-id="acb68-153">Conferma che gli elementi di pari livello non hanno lo stesso nome: coppie ControlType, né lo stesso AutomationId.</span><span class="sxs-lookup"><span data-stu-id="acb68-153">Confirms that sibling elements do not have the same Name:ControlType pairs, nor the same AutomationId's.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-154">$ {ROWSPAN9} $<strong>aria Web VERIFICATIONS</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="acb68-154">${ROWSPAN9}$<strong>ARIA Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="acb68-155"><strong>CheckARIARole</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-155"><strong>CheckARIARole</strong></span></span></td>
<td><span data-ttu-id="acb68-156">Conferma che tutti gli elementi hanno un ruolo ARIA valido.</span><span class="sxs-lookup"><span data-stu-id="acb68-156">Confirms that all elements have a valid ARIA role.</span></span> <span data-ttu-id="acb68-157">Il tag HTML associato e il ruolo ARIA sono elementi informativi con ruoli non validi contrassegnati come errori.</span><span class="sxs-lookup"><span data-stu-id="acb68-157">The associated HTML tag and ARIA role are information elements with invalid roles flagged as errors.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acb68-158"><strong>CheckLabel</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-158"><strong>CheckLabel</strong></span></span></td>
<td><span data-ttu-id="acb68-159">Conferma che ogni elemento con il ruolo di input, pulsante, immagine o punto di riferimento dispone di un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="acb68-159">Confirms each element with input, button, image-button, or landmark role has a label.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-160"><strong>CheckRangeControls</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-160"><strong>CheckRangeControls</strong></span></span></td>
<td><span data-ttu-id="acb68-161">Conferma che i controlli intervallo con dispositivo di scorrimento o indicatore di stato hanno attributi ARIA corretti definiti.</span><span class="sxs-lookup"><span data-stu-id="acb68-161">Confirms range controls with slider or progress bar role have proper ARIA attributes defined.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="acb68-162"><strong>CheckContainerRole</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-162"><strong>CheckContainerRole</strong></span></span></td>
<td><span data-ttu-id="acb68-163">Conferma che un elemento o almeno uno dei relativi elementi figlio ha definito OnKeyDown/OnKeyPress.</span><span class="sxs-lookup"><span data-stu-id="acb68-163">Confirms an element, or at least one of its children, has onkeydown/onkeypress defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-164"><strong>CheckLayoutTable</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-164"><strong>CheckLayoutTable</strong></span></span></td>
<td><span data-ttu-id="acb68-165">Conferma che un layout di tabella contiene un riepilogo/aria-describedby inclusi.</span><span class="sxs-lookup"><span data-stu-id="acb68-165">Confirms a table layout has a summary/th/aria-describedby included.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="acb68-166"><strong>CheckGridStructure</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-166"><strong>CheckGridStructure</strong></span></span></td>
<td><span data-ttu-id="acb68-167">Conferma che un elemento non tabella con il ruolo Grid ha una struttura di Grid>Row>GridCell con attributi associati.</span><span class="sxs-lookup"><span data-stu-id="acb68-167">Confirms a non-table element with grid role has a structure of grid>row>gridcell with associated attributes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-168"><strong>CheckDataTable</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-168"><strong>CheckDataTable</strong></span></span></td>
<td><span data-ttu-id="acb68-169">Conferma le proprietà delle tabelle di dati.</span><span class="sxs-lookup"><span data-stu-id="acb68-169">Confirms the properties of data tables.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="acb68-170"><strong>CheckActiveDescendants</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-170"><strong>CheckActiveDescendants</strong></span></span></td>
<td><span data-ttu-id="acb68-171">Conferma le proprietà degli elementi con un discendente attivo definito.</span><span class="sxs-lookup"><span data-stu-id="acb68-171">Confirms the properties of elements with an active descendant defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-172"><strong>CheckElementsWithClickHandler</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-172"><strong>CheckElementsWithClickHandler</strong></span></span></td>
<td><span data-ttu-id="acb68-173">Conferma l'indice di tabulazione degli elementi con gestori di clic.</span><span class="sxs-lookup"><span data-stu-id="acb68-173">Confirms the tab index of elements with click handlers.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="acb68-174"><strong>Verifiche Web</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="acb68-174"><strong>Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="acb68-175"><strong>CheckHtml (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-175"><strong>CheckHtml (Web)</strong></span></span></td>
<td><span data-ttu-id="acb68-176">Conferma varie caratteristiche HTML, ad esempio intestazioni, nomi, frame e titoli.</span><span class="sxs-lookup"><span data-stu-id="acb68-176">Confirms various HTML characteristics such as headers, name, frames, and titles.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acb68-177"><strong>CheckName (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-177"><strong>CheckName (Web)</strong></span></span></td>
<td><span data-ttu-id="acb68-178">Conferma le caratteristiche del nome, ad esempio la lunghezza, i caratteri non validi e l'inclusione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="acb68-178">Confirms name characteristics such as length, invalid characters, and role inclusion.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="acb68-179"><strong>CheckRole (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="acb68-179"><strong>CheckRole (Web)</strong></span></span></td>
<td><span data-ttu-id="acb68-180">Conferma i ruoli non validi, i ruoli che devono avere valori e/o ruoli non implementati.</span><span class="sxs-lookup"><span data-stu-id="acb68-180">Confirms invalid roles, roles that should have values, and/or roles not implemented.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="acb68-181">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="acb68-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acb68-182">Verifica dell'accessibilità dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="acb68-182">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




