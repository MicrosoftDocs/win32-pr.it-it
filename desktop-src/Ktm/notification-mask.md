---
description: Elenca i diversi tipi di notifiche che possono essere ricevute da un elenco.
ms.assetid: 65db8ba5-193c-439b-8e8c-6cb4a9bd4efd
title: NOTIFICATION_MASK (KtmTypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3650c10f619cf45db34d9172476261838897a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314799"
---
# <a name="notification_mask"></a><span data-ttu-id="d1fc4-103">maschera di notifica \_</span><span class="sxs-lookup"><span data-stu-id="d1fc4-103">NOTIFICATION\_MASK</span></span>

<span data-ttu-id="d1fc4-104">Elenca i diversi tipi di notifiche che possono essere ricevute da un elenco.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-104">Lists the different types of notifications that can be received by an enlistment.</span></span>

<dl> <dt>

<span data-ttu-id="d1fc4-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**\_maschera notifiche \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-105"><span id="TRANSACTION_NOTIFY_MASK"></span><span id="transaction_notify_mask"></span>**TRANSACTION\_NOTIFY\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-106">0x3FFFFFFF</span><span class="sxs-lookup"><span data-stu-id="d1fc4-106">0x3FFFFFFF</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-107">Maschera che indica tutti i bit validi per una notifica di transazione.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-107">A mask that indicates all valid bits for a transaction notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**\_notifica \_ PREpreparazione transazione**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-108"><span id="TRANSACTION_NOTIFY_PREPREPARE"></span><span id="transaction_notify_preprepare"></span>**TRANSACTION\_NOTIFY\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d1fc4-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-110">Questa notifica viene chiamata dopo che un client chiama [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) e nessun Resource Manager (RM) supporta il commit a fase singola o una gestione transazioni (TM) superiore chiama [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment).</span><span class="sxs-lookup"><span data-stu-id="d1fc4-110">This notification is called after a client calls [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) and either no resource manager (RM) supports single-phase commit or a superior transaction manager (TM) calls [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment).</span></span> <span data-ttu-id="d1fc4-111">Questa notifica viene ricevuta da RMs indicante che è necessario completare qualsiasi lavoro che potrebbe causare l'integrazione di altri RMs in una transazione, ad esempio lo svuotamento della cache.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-111">This notification is received by the RMs indicating that they should complete any work that could cause other RMs to need to enlist in a transaction, such as flushing its cache.</span></span> <span data-ttu-id="d1fc4-112">Al termine di queste operazioni, è necessario che RM chiami [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete).</span><span class="sxs-lookup"><span data-stu-id="d1fc4-112">After completing these operations the RM must call [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete).</span></span> <span data-ttu-id="d1fc4-113">Per ricevere questa notifica, è necessario che RM supporti inoltre il **\_ \_ commit** della notifica **della transazione e \_ \_** della notifica della transazione.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-113">To receive this notification the RM must also support **TRANSACTION\_NOTIFY\_PREPARE** and **TRANSACTION\_NOTIFY\_COMMIT**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**notifica della transazione- \_ \_ prepara**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-114"><span id="TRANSACTION_NOTIFY_PREPARE"></span><span id="transaction_notify_prepare"></span>**TRANSACTION\_NOTIFY\_PREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d1fc4-115">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-116">Questa notifica viene chiamata dopo il completamento dell'elaborazione della **\_ notifica \_** preliminare della transazione.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-116">This notification is called after the **TRANSACTION\_NOTIFY\_PREPREPARE** processing is complete.</span></span> <span data-ttu-id="d1fc4-117">Segnala a RM di completare tutte le operazioni associate a questa integrazione, in modo da garantire che un'operazione di commit possa avere esito positivo e che anche un'operazione di interruzione possa avere esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-117">It signals the RM to complete all the work that is associated with this enlistment so that it can guarantee that a commit operation could succeed and an abort operation could also succeed.</span></span> <span data-ttu-id="d1fc4-118">In genere, la maggior parte del lavoro per una transazione viene eseguita durante la fase di preparazione.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-118">Typically, the bulk of the work for a transaction is done during the prepare phase.</span></span> <span data-ttu-id="d1fc4-119">Per RMs durevole, è necessario che registrino il proprio stato prima di chiamare la funzione [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) .</span><span class="sxs-lookup"><span data-stu-id="d1fc4-119">For durable RMs, they must log their state prior to calling the [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) function.</span></span> <span data-ttu-id="d1fc4-120">Questa è l'ultima possibilità per l'RM di richiedere che venga eseguito il rollback della transazione.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-120">This is the last chance for the RM to request that the transaction be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**\_commit notifica \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-121"><span id="TRANSACTION_NOTIFY_COMMIT"></span><span id="transaction_notify_commit"></span>**TRANSACTION\_NOTIFY\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d1fc4-122">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-123">Questa notifica segnala a RM di completare tutte le operazioni associate a questa integrazione.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-123">This notification signals the RM to complete all the work that is associated with this enlistment.</span></span> <span data-ttu-id="d1fc4-124">In genere, RM rilascia tutti i blocchi, rilascia tutte le informazioni necessarie per eseguire il rollback della transazione.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-124">Typically, the RM releases any locks, releases any information necessary to roll back the transaction.</span></span> <span data-ttu-id="d1fc4-125">Il RM deve rispondere chiamando la funzione [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) al termine di queste operazioni.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-125">The RM must respond by calling the [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) function when it has finished these operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**\_rollback notifiche \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-126"><span id="TRANSACTION_NOTIFY_ROLLBACK"></span><span id="transaction_notify_rollback"></span>**TRANSACTION\_NOTIFY\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-127">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d1fc4-127">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-128">Questa notifica segnala a RM di annullare tutte le operazioni eseguite associate alla transazione.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-128">This notification signals the RM to undo all the work it has done that is associated with the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**\_pre- \_ preparazione notifica transazioni \_ completata**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-129"><span id="TRANSACTION_NOTIFY_PREPREPARE_COMPLETE"></span><span id="transaction_notify_preprepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-130">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d1fc4-130">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-131">Questa notifica segnala al TM superiore che un'operazione di pre-preparazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-131">This notification signals to the superior TM that a pre-prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**\_preparazione notifica \_ transazioni \_ completata**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-132"><span id="TRANSACTION_NOTIFY_PREPARE_COMPLETE"></span><span id="transaction_notify_prepare_complete"></span>**TRANSACTION\_NOTIFY\_PREPARE\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-133">0x00000020</span><span class="sxs-lookup"><span data-stu-id="d1fc4-133">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-134">Questa notifica segnala al TM superiore che un'operazione di preparazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-134">This notification signals to the superior TM that a prepare operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**\_commit notifica \_ transazioni \_ completato**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-135"><span id="TRANSACTION_NOTIFY_COMMIT_COMPLETE"></span><span id="transaction_notify_commit_complete"></span>**TRANSACTION\_NOTIFY\_COMMIT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-136">0x00000040</span><span class="sxs-lookup"><span data-stu-id="d1fc4-136">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-137">Questa notifica segnala al TM superiore che un'operazione di commit è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-137">This notification signals to the superior TM that a commit operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**\_rollback notifiche \_ transazioni \_ completato**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-138"><span id="TRANSACTION_NOTIFY_ROLLBACK_COMPLETE"></span><span id="transaction_notify_rollback_complete"></span>**TRANSACTION\_NOTIFY\_ROLLBACK\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="d1fc4-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-140">Questa notifica segnala al TM superiore che un'operazione di rollback è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-140">This notification signals to the superior TM that a rollback operation was completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**\_recupero notifiche \_ transazioni**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-141"><span id="TRANSACTION_NOTIFY_RECOVER"></span><span id="transaction_notify_recover"></span>**TRANSACTION\_NOTIFY\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="d1fc4-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-143">Questa notifica segnala a RMs che devono ripristinare il proprio stato perché è necessario recapitare il risultato di una transazione.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-143">This notification signals to RMs that they should recover their state because a transaction outcome must be redelivered.</span></span> <span data-ttu-id="d1fc4-144">Ad esempio, quando un RM viene recuperato e in caso di transazioni rimaste in dubbio.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-144">For example, when an RM is recovered, and when there are transactions left in-doubt.</span></span> <span data-ttu-id="d1fc4-145">Questa notifica viene recapitata una volta risolto lo stato in dubbio.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-145">This notification is delivered once the in-doubt state is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**COMMIT di una \_ \_ singola \_ fase di notifica transazione \_**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-146"><span id="TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT"></span><span id="transaction_notify_single_phase_commit"></span>**TRANSACTION\_NOTIFY\_SINGLE\_PHASE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-147">0x00000200</span><span class="sxs-lookup"><span data-stu-id="d1fc4-147">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-148">Questa notifica segnala a RM di completare ed eseguire il commit della transazione senza utilizzare un protocollo di commit in due fasi.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-148">This notification signals the RM to complete and commit the transaction without using a two-phase commit protocol.</span></span> <span data-ttu-id="d1fc4-149">Se RM vuole usare un'operazione in due fasi, deve rispondere chiamando la funzione [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) .</span><span class="sxs-lookup"><span data-stu-id="d1fc4-149">If the RM wants to use a two-phase operation, it must respond by calling the [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**\_commit del \_ delegato \_ Notify transazione**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-150"><span id="TRANSACTION_NOTIFY_DELEGATE_COMMIT"></span><span id="transaction_notify_delegate_commit"></span>**TRANSACTION\_NOTIFY\_DELEGATE\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-151">0x00000400</span><span class="sxs-lookup"><span data-stu-id="d1fc4-151">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-152">KTM segnala alla TM superiore di eseguire un'operazione di commit.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-152">KTM is signaling to the superior TM to perform a commit operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**\_query di \_ recupero \_ notifica transazioni**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-153"><span id="TRANSACTION_NOTIFY_RECOVER_QUERY"></span><span id="transaction_notify_recover_query"></span>**TRANSACTION\_NOTIFY\_RECOVER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-154">0x00000800</span><span class="sxs-lookup"><span data-stu-id="d1fc4-154">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-155">KTM segnala alla TM superiore di eseguire una query sullo stato di una transazione in dubbio.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-155">KTM is signaling to the superior TM to query the status of an in-doubt transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**\_pre- \_ \_ preparazione della notifica della transazione**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-156"><span id="TRANSACTION_NOTIFY_ENLIST_PREPREPARE"></span><span id="transaction_notify_enlist_preprepare"></span>**TRANSACTION\_NOTIFY\_ENLIST\_PREPREPARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-157">0x00001000</span><span class="sxs-lookup"><span data-stu-id="d1fc4-157">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-158">Questa notifica segnala al TM superiore che le notifiche preliminari devono essere recapitate nell'elenco specificato.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-158">This notification signals to the superior TM that pre-prepare notifications must be delivered on the specified enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**\_ \_ ultimo ripristino notifiche \_ transazioni**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-159"><span id="TRANSACTION_NOTIFY_LAST_RECOVER"></span><span id="transaction_notify_last_recover"></span>**TRANSACTION\_NOTIFY\_LAST\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="d1fc4-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-161">Questa notifica indica che l'operazione di ripristino è stata completata per questo RM.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-161">This notification indicates that the recovery operation is complete for this RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**notifica di transazione \_ \_ indubbia**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-162"><span id="TRANSACTION_NOTIFY_INDOUBT"></span><span id="transaction_notify_indoubt"></span>**TRANSACTION\_NOTIFY\_INDOUBT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-163">0x00004000</span><span class="sxs-lookup"><span data-stu-id="d1fc4-163">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-164">Lo stato della transazione specificata è in dubbio.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-164">The specified transaction is in an in-doubt state.</span></span> <span data-ttu-id="d1fc4-165">Il RM riceve questa notifica durante le operazioni di ripristino quando una transazione è stata preparata, ma non è disponibile una gestione transazioni superiore (TM).</span><span class="sxs-lookup"><span data-stu-id="d1fc4-165">The RM receives this notification during recovery operations when a transaction has been prepared, but there is no superior transaction manager (TM) available.</span></span> <span data-ttu-id="d1fc4-166">Ad esempio, quando una transazione include una TM remota e tale nodo non è disponibile, il nodo non è disponibile o il servizio [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) locale non è disponibile, lo stato della transazione è in dubbio.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-166">For example, when a transaction involves a remote TM and that node is unavailable, its node is unavailable, or the local [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) service is unavailable, the transaction state is in-doubt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**\_notifica transazioni \_ TM \_ online**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-167"><span id="TRANSACTION_NOTIFY_TM_ONLINE"></span><span id="transaction_notify_tm_online"></span>**TRANSACTION\_NOTIFY\_TM\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-168">0x02000000</span><span class="sxs-lookup"><span data-stu-id="d1fc4-168">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-169">TM è online e accetta le richieste.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-169">The TM is online and accepting requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**\_risultato della \_ richiesta di notifica della transazione \_**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-170"><span id="TRANSACTION_NOTIFY_REQUEST_OUTCOME"></span><span id="transaction_notify_request_outcome"></span>**TRANSACTION\_NOTIFY\_REQUEST\_OUTCOME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-171">0x20000000</span><span class="sxs-lookup"><span data-stu-id="d1fc4-171">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-172">Segnala a RMs che sono disponibili informazioni sul risultato e che è necessario effettuare una richiesta per tali informazioni.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-172">Signals to RMs that there is outcome information available, and that a request for that information should be made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1fc4-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**\_ \_ finalizzazione commit notifica transazione \_**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-173"><span id="TRANSACTION_NOTIFY_COMMIT_FINALIZE"></span><span id="transaction_notify_commit_finalize"></span>**TRANSACTION\_NOTIFY\_COMMIT\_FINALIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1fc4-174">0x40000000</span><span class="sxs-lookup"><span data-stu-id="d1fc4-174">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="d1fc4-175">Riservato.</span><span class="sxs-lookup"><span data-stu-id="d1fc4-175">Reserved.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1fc4-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1fc4-176">Requirements</span></span>



| <span data-ttu-id="d1fc4-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1fc4-177">Requirement</span></span> | <span data-ttu-id="d1fc4-178">Valore</span><span class="sxs-lookup"><span data-stu-id="d1fc4-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1fc4-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1fc4-179">Minimum supported client</span></span><br/> | <span data-ttu-id="d1fc4-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1fc4-180">Windows Vista</span></span><br/>                                                                                  |
| <span data-ttu-id="d1fc4-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1fc4-181">Minimum supported server</span></span><br/> | <span data-ttu-id="d1fc4-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1fc4-182">Windows Server 2008</span></span><br/>                                                                            |
| <span data-ttu-id="d1fc4-183">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1fc4-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1fc4-184"><dt>KtmTypes. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1fc4-184"><dt>KtmTypes.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1fc4-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1fc4-185">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1fc4-186">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1fc4-186">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d1fc4-187">Costanti di gestione transazioni kernel</span><span class="sxs-lookup"><span data-stu-id="d1fc4-187">Kernel Transaction Manager Constants</span></span>](kernel-transaction-manager-constants.md)
</dt> <dt>

[<span data-ttu-id="d1fc4-188">**CreateEnlistment**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-188">**CreateEnlistment**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)
</dt> <dt>

[<span data-ttu-id="d1fc4-189">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-189">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
</dt> <dt>

[<span data-ttu-id="d1fc4-190">**GetNotificationResourceManager**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-190">**GetNotificationResourceManager**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)
</dt> <dt>

[<span data-ttu-id="d1fc4-191">**GetNotificationResourceManagerAsync**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-191">**GetNotificationResourceManagerAsync**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync)
</dt> <dt>

[<span data-ttu-id="d1fc4-192">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-192">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
</dt> <dt>

[<span data-ttu-id="d1fc4-193">**SinglePhaseReject**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-193">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)
</dt> <dt>

[<span data-ttu-id="d1fc4-194">**\_notifica transazioni**</span><span class="sxs-lookup"><span data-stu-id="d1fc4-194">**TRANSACTION\_NOTIFICATION**</span></span>](/windows/desktop/api/KtmTypes/ns-ktmtypes-transaction_notification)
</dt> </dl>

 

