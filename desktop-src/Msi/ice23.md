---
description: ICE23 convalida l'ordine di tabulazione del controllo per ogni finestra di dialogo.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c1823a70e50d7dd3c42c2e90d6a2d0f11f2fa5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314227"
---
# <a name="ice23"></a><span data-ttu-id="9107d-103">ICE23</span><span class="sxs-lookup"><span data-stu-id="9107d-103">ICE23</span></span>

<span data-ttu-id="9107d-104">ICE23 convalida l'ordine di tabulazione del controllo per ogni finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="9107d-104">ICE23 validates the control tab order for each dialog box.</span></span>

<span data-ttu-id="9107d-105">ICE23 convalida quanto segue nella tabella della [finestra di dialogo](dialog-table.md) e nella [tabella dei controlli](control-table.md):</span><span class="sxs-lookup"><span data-stu-id="9107d-105">ICE23 validates the following in the [Dialog table](dialog-table.md) and [Control table](control-table.md):</span></span>

-   <span data-ttu-id="9107d-106">Che ogni record nella tabella della finestra di dialogo specifichi un controllo nella \_ prima colonna del controllo presente nella finestra di dialogo specificata dalla colonna della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="9107d-106">That every record in the Dialog table specifies a control in the Control\_First column that exists in the dialog box specified by the Dialog column.</span></span>
-   <span data-ttu-id="9107d-107">Che ogni record nella tabella dei controlli specifichi un controllo nella \_ colonna successiva del controllo che si trova nella stessa finestra di dialogo del controllo elencato nella colonna di controllo oppure \_ il controllo successivo contiene il valore null.</span><span class="sxs-lookup"><span data-stu-id="9107d-107">That every record in the Control table specifies a control in the Control\_Next column that is on the same dialog as the control listed in the Control column, or Control\_Next contains the Null value.</span></span>
-   <span data-ttu-id="9107d-108">Che dopo il controllo delle \_ voci successive dal controllo al controllo nella tabella dei controlli viene eseguito un ciclo singolo, chiuso, che torna al controllo iniziale.</span><span class="sxs-lookup"><span data-stu-id="9107d-108">That following the Control\_Next entries from control to control in the Control table makes a single, closed, loop that comes back to the initial control.</span></span> <span data-ttu-id="9107d-109">Non è necessario che tutti i controlli siano presenti nel ciclo, ma il ciclo deve passare tutti i controlli con una voce nella colonna del controllo \_ successiva.</span><span class="sxs-lookup"><span data-stu-id="9107d-109">Not every control needs to be in the loop, but the loop must pass through every control that has an entry in the Control\_Next column.</span></span>

## <a name="result"></a><span data-ttu-id="9107d-110">Risultato</span><span class="sxs-lookup"><span data-stu-id="9107d-110">Result</span></span>

<span data-ttu-id="9107d-111">ICE23 Invia un messaggio di errore se l'ordine di tabulazione dei controlli non costituisce un singolo ciclo chiuso nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="9107d-111">ICE23 posts an error message if the tab order of controls does not form a single closed loop in the dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="9107d-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="9107d-112">Example</span></span>

<span data-ttu-id="9107d-113">ICE23 invierà i messaggi di errore seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="9107d-113">ICE23 would post the following error messages for the example shown.</span></span>

-   <span data-ttu-id="9107d-114">Dialog1 non dispone prima di controllo \_ .</span><span class="sxs-lookup"><span data-stu-id="9107d-114">Dialog1 has no Control\_First.</span></span>
-   <span data-ttu-id="9107d-115">Il \_ primo controllo della finestra di dialogo Dialog2 fa riferimento a ControlX del controllo inesistente.</span><span class="sxs-lookup"><span data-stu-id="9107d-115">Control\_First of dialog Dialog2 refers to nonexistent control ControlX.</span></span>
-   <span data-ttu-id="9107d-116">Dialog3 ha un ordine di tabulazione non recapitabile a ControlB del controllo.</span><span class="sxs-lookup"><span data-stu-id="9107d-116">Dialog3 has dead-end tab order at control ControlB.</span></span>
-   <span data-ttu-id="9107d-117">Dialog4 ha un ordine di tabulazione in formato non corretto nel controllo ControlC</span><span class="sxs-lookup"><span data-stu-id="9107d-117">Dialog4 has malformed tab order at control ControlC</span></span>
-   <span data-ttu-id="9107d-118">Dialog5 dispone di un ordine di tabulazione in formato non corretto in ControlC del controllo.</span><span class="sxs-lookup"><span data-stu-id="9107d-118">Dialog5 has malformed tab order at control ControlC.</span></span>
-   <span data-ttu-id="9107d-119">Controllare il controllo \_ Next del controllo Dialog6. controlc collegamenti a un controllo sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9107d-119">Control\_Next of control Dialog6.ControlC links to unknown control.</span></span>

<span data-ttu-id="9107d-120">[Tabella finestra di dialogo](dialog-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="9107d-120">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="9107d-121">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="9107d-121">Dialog</span></span>  | <span data-ttu-id="9107d-122">\_Primo controllo</span><span class="sxs-lookup"><span data-stu-id="9107d-122">Control\_First</span></span> |
|---------|----------------|
| <span data-ttu-id="9107d-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="9107d-123">Dialog1</span></span> |                |
| <span data-ttu-id="9107d-124">Dialog2</span><span class="sxs-lookup"><span data-stu-id="9107d-124">Dialog2</span></span> | <span data-ttu-id="9107d-125">ControlX</span><span class="sxs-lookup"><span data-stu-id="9107d-125">ControlX</span></span>       |
| <span data-ttu-id="9107d-126">Dialog3</span><span class="sxs-lookup"><span data-stu-id="9107d-126">Dialog3</span></span> | <span data-ttu-id="9107d-127">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-127">ControlA</span></span>       |
| <span data-ttu-id="9107d-128">Dialog4</span><span class="sxs-lookup"><span data-stu-id="9107d-128">Dialog4</span></span> | <span data-ttu-id="9107d-129">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-129">ControlA</span></span>       |
| <span data-ttu-id="9107d-130">Dialog5</span><span class="sxs-lookup"><span data-stu-id="9107d-130">Dialog5</span></span> | <span data-ttu-id="9107d-131">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-131">ControlA</span></span>       |



 

<span data-ttu-id="9107d-132">[Tabella di controllo](control-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="9107d-132">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="9107d-133">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="9107d-133">Dialog</span></span>  | <span data-ttu-id="9107d-134">Control</span><span class="sxs-lookup"><span data-stu-id="9107d-134">Control</span></span>  | <span data-ttu-id="9107d-135">Controllo \_ successivo</span><span class="sxs-lookup"><span data-stu-id="9107d-135">Control\_Next</span></span> |
|---------|----------|---------------|
| <span data-ttu-id="9107d-136">Dialog1</span><span class="sxs-lookup"><span data-stu-id="9107d-136">Dialog1</span></span> | <span data-ttu-id="9107d-137">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-137">ControlA</span></span> |               |
| <span data-ttu-id="9107d-138">Dialog1</span><span class="sxs-lookup"><span data-stu-id="9107d-138">Dialog1</span></span> | <span data-ttu-id="9107d-139">ControlB</span><span class="sxs-lookup"><span data-stu-id="9107d-139">ControlB</span></span> | <span data-ttu-id="9107d-140">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-140">ControlA</span></span>      |
| <span data-ttu-id="9107d-141">Dialog2</span><span class="sxs-lookup"><span data-stu-id="9107d-141">Dialog2</span></span> | <span data-ttu-id="9107d-142">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-142">ControlA</span></span> | <span data-ttu-id="9107d-143">ControlB</span><span class="sxs-lookup"><span data-stu-id="9107d-143">ControlB</span></span>      |
| <span data-ttu-id="9107d-144">Dialog2</span><span class="sxs-lookup"><span data-stu-id="9107d-144">Dialog2</span></span> | <span data-ttu-id="9107d-145">ControlB</span><span class="sxs-lookup"><span data-stu-id="9107d-145">ControlB</span></span> | <span data-ttu-id="9107d-146">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-146">ControlA</span></span>      |
| <span data-ttu-id="9107d-147">Dialog3</span><span class="sxs-lookup"><span data-stu-id="9107d-147">Dialog3</span></span> | <span data-ttu-id="9107d-148">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-148">ControlA</span></span> | <span data-ttu-id="9107d-149">ControlB</span><span class="sxs-lookup"><span data-stu-id="9107d-149">ControlB</span></span>      |
| <span data-ttu-id="9107d-150">Dialog3</span><span class="sxs-lookup"><span data-stu-id="9107d-150">Dialog3</span></span> | <span data-ttu-id="9107d-151">ControlB</span><span class="sxs-lookup"><span data-stu-id="9107d-151">ControlB</span></span> |               |
| <span data-ttu-id="9107d-152">Dialog4</span><span class="sxs-lookup"><span data-stu-id="9107d-152">Dialog4</span></span> | <span data-ttu-id="9107d-153">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-153">ControlA</span></span> | <span data-ttu-id="9107d-154">ControlB</span><span class="sxs-lookup"><span data-stu-id="9107d-154">ControlB</span></span>      |
| <span data-ttu-id="9107d-155">Dialog4</span><span class="sxs-lookup"><span data-stu-id="9107d-155">Dialog4</span></span> | <span data-ttu-id="9107d-156">ControlB</span><span class="sxs-lookup"><span data-stu-id="9107d-156">ControlB</span></span> | <span data-ttu-id="9107d-157">ControlC</span><span class="sxs-lookup"><span data-stu-id="9107d-157">ControlC</span></span>      |
| <span data-ttu-id="9107d-158">Dialog4</span><span class="sxs-lookup"><span data-stu-id="9107d-158">Dialog4</span></span> | <span data-ttu-id="9107d-159">ControlC</span><span class="sxs-lookup"><span data-stu-id="9107d-159">ControlC</span></span> | <span data-ttu-id="9107d-160">ControlB</span><span class="sxs-lookup"><span data-stu-id="9107d-160">ControlB</span></span>      |
| <span data-ttu-id="9107d-161">Dialog5</span><span class="sxs-lookup"><span data-stu-id="9107d-161">Dialog5</span></span> | <span data-ttu-id="9107d-162">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-162">ControlA</span></span> | <span data-ttu-id="9107d-163">ControlB</span><span class="sxs-lookup"><span data-stu-id="9107d-163">ControlB</span></span>      |
| <span data-ttu-id="9107d-164">Dialog5</span><span class="sxs-lookup"><span data-stu-id="9107d-164">Dialog5</span></span> | <span data-ttu-id="9107d-165">ControlB</span><span class="sxs-lookup"><span data-stu-id="9107d-165">ControlB</span></span> | <span data-ttu-id="9107d-166">ControlC</span><span class="sxs-lookup"><span data-stu-id="9107d-166">ControlC</span></span>      |
| <span data-ttu-id="9107d-167">Dialog5</span><span class="sxs-lookup"><span data-stu-id="9107d-167">Dialog5</span></span> | <span data-ttu-id="9107d-168">ControlC</span><span class="sxs-lookup"><span data-stu-id="9107d-168">ControlC</span></span> | <span data-ttu-id="9107d-169">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-169">ControlA</span></span>      |
| <span data-ttu-id="9107d-170">Dialog5</span><span class="sxs-lookup"><span data-stu-id="9107d-170">Dialog5</span></span> | <span data-ttu-id="9107d-171">ControlD</span><span class="sxs-lookup"><span data-stu-id="9107d-171">ControlD</span></span> | <span data-ttu-id="9107d-172">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-172">ControlA</span></span>      |
| <span data-ttu-id="9107d-173">Dialog6</span><span class="sxs-lookup"><span data-stu-id="9107d-173">Dialog6</span></span> | <span data-ttu-id="9107d-174">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-174">ControlA</span></span> | <span data-ttu-id="9107d-175">ControlB</span><span class="sxs-lookup"><span data-stu-id="9107d-175">ControlB</span></span>      |
| <span data-ttu-id="9107d-176">Dialog6</span><span class="sxs-lookup"><span data-stu-id="9107d-176">Dialog6</span></span> | <span data-ttu-id="9107d-177">ControlB</span><span class="sxs-lookup"><span data-stu-id="9107d-177">ControlB</span></span> | <span data-ttu-id="9107d-178">ControlC</span><span class="sxs-lookup"><span data-stu-id="9107d-178">ControlC</span></span>      |
| <span data-ttu-id="9107d-179">Dialog6</span><span class="sxs-lookup"><span data-stu-id="9107d-179">Dialog6</span></span> | <span data-ttu-id="9107d-180">ControlC</span><span class="sxs-lookup"><span data-stu-id="9107d-180">ControlC</span></span> | <span data-ttu-id="9107d-181">ControlX</span><span class="sxs-lookup"><span data-stu-id="9107d-181">ControlX</span></span>      |
| <span data-ttu-id="9107d-182">Dialog6</span><span class="sxs-lookup"><span data-stu-id="9107d-182">Dialog6</span></span> | <span data-ttu-id="9107d-183">ControlD</span><span class="sxs-lookup"><span data-stu-id="9107d-183">ControlD</span></span> | <span data-ttu-id="9107d-184">ControlA</span><span class="sxs-lookup"><span data-stu-id="9107d-184">ControlA</span></span>      |



 

<span data-ttu-id="9107d-185">Per correggere questi errori, tenere presente quanto riportato di seguito nelle tabelle precedenti e apportare le modifiche indicate.</span><span class="sxs-lookup"><span data-stu-id="9107d-185">To fix these errors note the following in the above tables and make the indicated changes.</span></span>

<span data-ttu-id="9107d-186">Non tutte le righe nella tabella della finestra di dialogo hanno un controllo specificato nella \_ prima colonna del controllo.</span><span class="sxs-lookup"><span data-stu-id="9107d-186">Not every row in the Dialog table has a control specified in the Control\_First column.</span></span> <span data-ttu-id="9107d-187">Modificare la \_ prima colonna controllo del record Dialog1 nella tabella della finestra di dialogo in un controllo presente in Dialog1.</span><span class="sxs-lookup"><span data-stu-id="9107d-187">Change the Control\_First column of the Dialog1 record in the Dialog table to a control that exists in Dialog1.</span></span>

<span data-ttu-id="9107d-188">Non tutte le righe della tabella della finestra di dialogo hanno un controllo specificato nella prima colonna del controllo presente nella finestra di \_ dialogo.</span><span class="sxs-lookup"><span data-stu-id="9107d-188">Not every row in the Dialog table has a control specified in the Control\_First column that exists on the dialog box.</span></span> <span data-ttu-id="9107d-189">Modificare la \_ prima colonna del controllo di Dialog2 in un controllo esistente in Dialog2.</span><span class="sxs-lookup"><span data-stu-id="9107d-189">Change the Control\_First column of the Dialog2 to a control that exists in Dialog2.</span></span>

<span data-ttu-id="9107d-190">Dopo il controllo \_ , le voci successive della tabella dei controlli dal controllo al controllo non rendono un ciclo chiuso in ogni caso.</span><span class="sxs-lookup"><span data-stu-id="9107d-190">Following the Control\_Next entries in the Control table from control to control does not make a closed loop in every case.</span></span> <span data-ttu-id="9107d-191">Modificare la colonna del controllo \_ successiva per ControlB in Dialog3 in ControlA.</span><span class="sxs-lookup"><span data-stu-id="9107d-191">Change the Control\_Next column for ControlB in Dialog3 to ControlA.</span></span>

<span data-ttu-id="9107d-192">Dopo il controllo \_ , le voci successive nella tabella dei controlli dal controllo al controllo non restituiscono il controllo iniziale in ogni caso.</span><span class="sxs-lookup"><span data-stu-id="9107d-192">Following the Control\_Next entries in the Control table from control to control does not lead back to the initial control in every case.</span></span> <span data-ttu-id="9107d-193">Modificare la colonna del controllo \_ successiva per controlc in Dialog4 per fare riferimento a ControlA.</span><span class="sxs-lookup"><span data-stu-id="9107d-193">Change the Control\_Next column for ControlC in Dialog4 to refer to ControlA.</span></span>

<span data-ttu-id="9107d-194">Dopo il controllo \_ , le voci successive nella tabella dei controlli dal controllo al controllo non passano attraverso ogni controllo nella finestra di dialogo con una voce nella colonna del controllo \_ successiva.</span><span class="sxs-lookup"><span data-stu-id="9107d-194">Following the Control\_Next entries in the Control table from control to control does not pass through every control in the dialog box having an entry in the Control\_Next column.</span></span> <span data-ttu-id="9107d-195">Modificare la colonna del controllo \_ successiva per controlc in Dialog5 in controllo.</span><span class="sxs-lookup"><span data-stu-id="9107d-195">Change the Control\_Next column for ControlC in Dialog5 to ControlD.</span></span>

<span data-ttu-id="9107d-196">Il controllo \_ successivo non fa riferimento a un controllo valido che si trova nella stessa finestra di dialogo del controllo elencato nella colonna del controllo.</span><span class="sxs-lookup"><span data-stu-id="9107d-196">Control\_Next does not refer to a valid control that is in the same dialog as the control listed in the Control column.</span></span> <span data-ttu-id="9107d-197">Modificare la colonna del controllo \_ successiva per controlc in Dialog6 per fare riferimento a controld.</span><span class="sxs-lookup"><span data-stu-id="9107d-197">Change the Control\_Next column for ControlC in Dialog6 to refer to ControlD.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9107d-198">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9107d-198">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9107d-199">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="9107d-199">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



