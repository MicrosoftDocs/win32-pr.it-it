---
title: Codici di errore WFP (Winerror.h)
description: (WFP) codici di errore specifici.
ms.assetid: 11f3085a-f044-4a78-b47a-59b9086562bf
topic_type:
- apiref
api_name:
- FWP_E_CALLOUT_NOT_FOUND
- FWP_E_CONDITION_NOT_FOUND
- FWP_E_FILTER_NOT_FOUND
- FWP_E_LAYER_NOT_FOUND
- FWP_E_PROVIDER_NOT_FOUND
- FWP_E_PROVIDER_CONTEXT_NOT_FOUND
- FWP_E_SUBLAYER_NOT_FOUND
- FWP_E_NOT_FOUND
- FWP_E_ALREADY_EXISTS
- FWP_E_IN_USE
- FWP_E_DYNAMIC_SESSION_IN_PROGRESS
- FWP_E_WRONG_SESSION
- FWP_E_NO_TXN_IN_PROGRESS
- FWP_E_TXN_IN_PROGRESS
- FWP_E_TXN_ABORTED
- FWP_E_SESSION_ABORTED
- FWP_E_INCOMPATIBLE_TXN
- FWP_E_TIMEOUT
- FWP_E_NET_EVENTS_DISABLED
- FWP_E_INCOMPATIBLE_LAYER
- FWP_E_KM_CLIENTS_ONLY
- FWP_E_LIFETIME_MISMATCH
- FWP_E_BUILTIN_OBJECT
- FWP_E_TOO_MANY_CALLOUTS
- FWP_E_NOTIFICATION_DROPPED
- FWP_E_TRAFFIC_MISMATCH
- FWP_E_INCOMPATIBLE_SA_STATE
- FWP_E_NULL_POINTER
- FWP_E_INVALID_ENUMERATOR
- FWP_E_INVALID_FLAGS
- FWP_E_INVALID_NET_MASK
- FWP_E_INVALID_RANGE
- FWP_E_INVALID_INTERVAL
- FWP_E_ZERO_LENGTH_ARRAY
- FWP_E_NULL_DISPLAY_NAME
- FWP_E_INVALID_ACTION_TYPE
- FWP_E_INVALID_WEIGHT
- FWP_E_MATCH_TYPE_MISMATCH
- FWP_E_TYPE_MISMATCH
- FWP_E_OUT_OF_BOUNDS
- FWP_E_RESERVED
- FWP_E_DUPLICATE_CONDITION
- FWP_E_DUPLICATE_KEYMOD
- FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER
- FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT
- FWP_E_INCOMPATIBLE_AUTH_METHOD
- FWP_E_INCOMPATIBLE_DH_GROUP
- FWP_E_EM_NOT_SUPPORTED
- FWP_E_NEVER_MATCH
- FWP_E_PROVIDER_CONTEXT_MISMATCH
- FWP_E_INVALID_PARAMETER
- FWP_E_TOO_MANY_SUBLAYERS
- FWP_E_CALLOUT_NOTIFICATION_FAILED
- FWP_E_INVALID_AUTH_TRANSFORM
- FWP_E_INVALID_CIPHER_TRANSFORM
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e7ee1ab0364a31f136f0c0cdbf87f459225b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477836"
---
# <a name="wfp-error-codes"></a><span data-ttu-id="a7f6a-103">Codici di errore di WFP</span><span class="sxs-lookup"><span data-stu-id="a7f6a-103">WFP Error Codes</span></span>

<span data-ttu-id="a7f6a-104">I codici di errore specifici di Windows Filtering Platform (WFP) sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-104">Windows Filtering Platform (WFP) specific error codes are as follows.</span></span>

<dl> <dt>

<span data-ttu-id="a7f6a-105"><span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**\_CALLOUT FWP \_ E \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-105"><span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**FWP\_E\_CALLOUT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-106">0x80320001</span><span class="sxs-lookup"><span data-stu-id="a7f6a-106">0x80320001</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-107">Il callout non esiste.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-107">The callout does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-108"><span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**\_condizione FWP \_ E \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-108"><span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**FWP\_E\_CONDITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-109">0x80320002</span><span class="sxs-lookup"><span data-stu-id="a7f6a-109">0x80320002</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-110">La condizione di filtro non esiste.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-110">The filter condition does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-111"><span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**\_filtro FWP \_ E \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-111"><span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**FWP\_E\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-112">0x80320003</span><span class="sxs-lookup"><span data-stu-id="a7f6a-112">0x80320003</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-113">Il filtro non esiste.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-113">The filter does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-114"><span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**livello di FWP \_ E \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-114"><span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**FWP\_E\_LAYER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-115">0x80320004</span><span class="sxs-lookup"><span data-stu-id="a7f6a-115">0x80320004</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-116">Il livello non esiste.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-116">The layer does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-117"><span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**il \_ provider di FWP E \_ non è stato \_ \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-117"><span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**FWP\_E\_PROVIDER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-118">0x80320005</span><span class="sxs-lookup"><span data-stu-id="a7f6a-118">0x80320005</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-119">Il provider non esiste.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-119">The provider does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-120"><span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**il \_ contesto del provider FWP E \_ non è stato \_ \_ \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-120"><span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**FWP\_E\_PROVIDER\_CONTEXT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-121">0x80320006</span><span class="sxs-lookup"><span data-stu-id="a7f6a-121">0x80320006</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-122">Il contesto del provider non esiste.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-122">The provider context does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-123"><span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**sottolivello di FWP \_ E \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-123"><span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**FWP\_E\_SUBLAYER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-124">0x80320007</span><span class="sxs-lookup"><span data-stu-id="a7f6a-124">0x80320007</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-125">Il sottolivello non esiste.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-125">The sub-layer does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-126"><span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP \_ E \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-126"><span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-127">0x80320008</span><span class="sxs-lookup"><span data-stu-id="a7f6a-127">0x80320008</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-128">L'oggetto non esiste.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-128">The object does not exist.</span></span>

<span data-ttu-id="a7f6a-129">Le [funzioni \* IPsecSaContext](fwp-ipsec-functions.md) restituiscono questo errore se l'ID del contesto SA non viene trovato.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-129">The [IPsecSaContext\*](fwp-ipsec-functions.md) functions return this error if the SA context ID is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-130"><span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP \_ E \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-130"><span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-131">0x80320009</span><span class="sxs-lookup"><span data-stu-id="a7f6a-131">0x80320009</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-132">Un oggetto con tale GUID o LUID esiste già.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-132">An object with that GUID or LUID already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-133"><span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP \_ E \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-133"><span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP\_E\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-134">0x8032000A</span><span class="sxs-lookup"><span data-stu-id="a7f6a-134">0x8032000A</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-135">Gli altri oggetti fanno riferimento all'oggetto, pertanto non può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-135">The object is referenced by other objects, so it cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-136"><span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**\_ \_ sessione dinamica FWP \_ E \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-136"><span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**FWP\_E\_DYNAMIC\_SESSION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-137">0x8032000B</span><span class="sxs-lookup"><span data-stu-id="a7f6a-137">0x8032000B</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-138">La chiamata non è consentita all'interno di una sessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-138">The call is not allowed from within a dynamic session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-139"><span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP \_ E \_ sessione errata \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-139"><span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP\_E\_WRONG\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-140">0x8032000C</span><span class="sxs-lookup"><span data-stu-id="a7f6a-140">0x8032000C</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-141">La chiamata è stata eseguita dalla sessione errata, quindi non può essere completata.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-141">The call was made from the wrong session, so it cannot be completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-142"><span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP \_ E \_ nessun \_ transazione \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-142"><span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP\_E\_NO\_TXN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-143">0x8032000D</span><span class="sxs-lookup"><span data-stu-id="a7f6a-143">0x8032000D</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-144">La chiamata deve essere eseguita dall'interno di una transazione esplicita.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-144">The call must be made from within an explicit transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-145"><span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP \_ E \_ transazione \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-145"><span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP\_E\_TXN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-146">0x8032000E</span><span class="sxs-lookup"><span data-stu-id="a7f6a-146">0x8032000E</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-147">La chiamata non è consentita all'interno di una transazione esplicita.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-147">The call is not allowed from within an explicit transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-148"><span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP \_ E \_ transazione \_ interrotti**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-148"><span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP\_E\_TXN\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-149">0x8032000F</span><span class="sxs-lookup"><span data-stu-id="a7f6a-149">0x8032000F</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-150">La transazione esplicita è stata annullata forzatamente.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-150">The explicit transaction has been forcibly canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-151"><span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**\_sessione FWP \_ E \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-151"><span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**FWP\_E\_SESSION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-152">0x80320010</span><span class="sxs-lookup"><span data-stu-id="a7f6a-152">0x80320010</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-153">La sessione è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-153">The session has been canceled.</span></span>

<span data-ttu-id="a7f6a-154">È necessario chiudere l'handle di sessione chiamando [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), anche se non è più valido. in caso contrario, lo stato del lato client verrà perso.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-154">The session handle needs to be closed by calling [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), even though it is no longer valid; otherwise, the client-side state will be leaked.</span></span> <span data-ttu-id="a7f6a-155">È necessario creare una nuova sessione chiamando [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="a7f6a-155">A new session should be created by calling [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-156"><span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**\_transazione FWP E \_ incompatibile \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-156"><span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**FWP\_E\_INCOMPATIBLE\_TXN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-157">0x80320011</span><span class="sxs-lookup"><span data-stu-id="a7f6a-157">0x80320011</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-158">La chiamata non è consentita all'interno di una transazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-158">The call is not allowed from within a read-only transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-159"><span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**FWP \_ E \_ timeout**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-159"><span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**FWP\_E\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-160">0x80320012</span><span class="sxs-lookup"><span data-stu-id="a7f6a-160">0x80320012</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-161">Timeout della chiamata durante l'attesa dell'acquisizione del blocco della transazione.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-161">The call timed out while waiting to acquire the transaction lock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-162"><span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**\_eventi FWP \_ E \_ net \_ disabilitati**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-162"><span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**FWP\_E\_NET\_EVENTS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-163">0x80320013</span><span class="sxs-lookup"><span data-stu-id="a7f6a-163">0x80320013</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-164">La raccolta di eventi di diagnostica di rete è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-164">The collection of network diagnostic events is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-165"><span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**\_livello FWP E \_ incompatibile \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-165"><span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**FWP\_E\_INCOMPATIBLE\_LAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-166">0x80320014</span><span class="sxs-lookup"><span data-stu-id="a7f6a-166">0x80320014</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-167">L'operazione non è supportata dal livello specificato.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-167">The operation is not supported by the specified layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-168"><span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**\_ \_ \_ solo client FWP E \_ km**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-168"><span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**FWP\_E\_KM\_CLIENTS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-169">0x80320015</span><span class="sxs-lookup"><span data-stu-id="a7f6a-169">0x80320015</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-170">La chiamata è consentita solo per i chiamanti in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-170">The call is allowed for kernel-mode callers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-171"><span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**FWP \_ E \_ durata non \_ corrispondenti**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-171"><span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**FWP\_E\_LIFETIME\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-172">0x80320016</span><span class="sxs-lookup"><span data-stu-id="a7f6a-172">0x80320016</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-173">La chiamata ha tentato di associare due oggetti con durate incompatibili.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-173">The call tried to associate two objects with incompatible lifetimes.</span></span>

<span data-ttu-id="a7f6a-174">Per ulteriori informazioni sulla durata degli oggetti e sull'associazione di oggetti, vedere [gestione](object-management.md) degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-174">See [Object Management](object-management.md) for more information on object lifetime and object association.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-175"><span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**\_oggetto FWP E \_ Builtin \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-175"><span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**FWP\_E\_BUILTIN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-176">0x80320017</span><span class="sxs-lookup"><span data-stu-id="a7f6a-176">0x80320017</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-177">L'oggetto è incorporato, pertanto non può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-177">The object is built-in, so it cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-178"><span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP \_ E \_ troppi \_ \_ callout**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-178"><span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP\_E\_TOO\_MANY\_CALLOUTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-179">0x80320018</span><span class="sxs-lookup"><span data-stu-id="a7f6a-179">0x80320018</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-180">È stato raggiunto il numero massimo di callout.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-180">The maximum number of callouts has been reached.</span></span>

<span data-ttu-id="a7f6a-181">Al massimo, i callout 100.000 possono essere registrati nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-181">At most, 100,000 callouts can be registered at the same time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-182"><span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**notifica di FWP \_ E \_ \_ rilasciata**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-182"><span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**FWP\_E\_NOTIFICATION\_DROPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-183">0x80320019</span><span class="sxs-lookup"><span data-stu-id="a7f6a-183">0x80320019</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-184">Non è stato possibile recapitare una notifica perché una coda di messaggi è alla capacità massima.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-184">A notification could not be delivered because a message queue is at its maximum capacity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-185"><span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**FWP \_ E \_ traffico non \_ corrispondenti**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-185"><span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**FWP\_E\_TRAFFIC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-186">0x8032001A</span><span class="sxs-lookup"><span data-stu-id="a7f6a-186">0x8032001A</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-187">I parametri del traffico di rete non corrispondono a quelli per il contesto dell'associazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-187">The network traffic parameters do not match those for the security association context.</span></span>

<span data-ttu-id="a7f6a-188">[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) può essere chiamato più volte, ma il chiamante deve specificare lo stesso [**\_ TRAFFIC0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) ogni volta.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-188">[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) can be called multiple times, but the caller must specify the same [**IPSEC\_TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) each time.</span></span> <span data-ttu-id="a7f6a-189">Questo errore viene restituito se una chiamata successiva fornisce un **\_ TRAFFIC0 IPSec** diverso.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-189">This error is returned if a subsequent call supplies a different **IPSEC\_TRAFFIC0**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-190"><span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**\_stato sa FWP E \_ incompatibile \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-190"><span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**FWP\_E\_INCOMPATIBLE\_SA\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-191">0x8032001B</span><span class="sxs-lookup"><span data-stu-id="a7f6a-191">0x8032001B</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-192">La chiamata non è consentita per lo stato dell'associazione di sicurezza (SA) corrente.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-192">The call is not allowed for the current security association (SA) state.</span></span>

<span data-ttu-id="a7f6a-193">Le funzioni di contesto SA devono essere chiamate in un ordine specifico:</span><span class="sxs-lookup"><span data-stu-id="a7f6a-193">The SA context functions must be called in a specific order:</span></span>

-   [<span data-ttu-id="a7f6a-194">**IPsecSaContextCreate0**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-194">**IPsecSaContextCreate0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [<span data-ttu-id="a7f6a-195">**IPsecSaContextGetSpi0**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-195">**IPsecSaContextGetSpi0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [<span data-ttu-id="a7f6a-196">**IPsecSaContextAddInbound0**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-196">**IPsecSaContextAddInbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [<span data-ttu-id="a7f6a-197">**IPsecSaContextAddOutbound0**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-197">**IPsecSaContextAddOutbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

<span data-ttu-id="a7f6a-198">Questo errore viene restituito se viene chiamato fuori ordine.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-198">This error is returned if they are called out of order.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-199"><span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**FWP \_ E \_ \_ puntatore null**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-199"><span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**FWP\_E\_NULL\_POINTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-200">0x8032001C</span><span class="sxs-lookup"><span data-stu-id="a7f6a-200">0x8032001C</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-201">Un puntatore obbligatorio è null.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-201">A required pointer is null.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-202"><span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**\_ \_ enumeratore FWP E non valido \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-202"><span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**FWP\_E\_INVALID\_ENUMERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-203">0x8032001D</span><span class="sxs-lookup"><span data-stu-id="a7f6a-203">0x8032001D</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-204">Un valore di enumeratore in una struttura non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-204">An enumerator value in a structure is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-205"><span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**\_flag FWP E \_ non validi \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-205"><span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**FWP\_E\_INVALID\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-206">0x8032001E</span><span class="sxs-lookup"><span data-stu-id="a7f6a-206">0x8032001E</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-207">Il campo dei flag contiene un valore non valido.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-207">The flags field contains an invalid value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-208"><span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**FWP \_ E \_ \_ net \_ mask non valido**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-208"><span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**FWP\_E\_INVALID\_NET\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-209">0x8032001F</span><span class="sxs-lookup"><span data-stu-id="a7f6a-209">0x8032001F</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-210">Una network mask non è valida.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-210">A network mask is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-211"><span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**FWP \_ E \_ intervallo non valido \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-211"><span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**FWP\_E\_INVALID\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-212">0x80320020</span><span class="sxs-lookup"><span data-stu-id="a7f6a-212">0x80320020</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-213">Una [**struttura \_ RANGE0 di FWP**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) non è valida.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-213">An [**FWP\_RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) structure is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-214"><span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**FWP \_ E \_ intervallo non valido \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-214"><span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**FWP\_E\_INVALID\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-215">0x80320021</span><span class="sxs-lookup"><span data-stu-id="a7f6a-215">0x80320021</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-216">L'intervallo di tempo non è valido.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-216">The time interval is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-217"><span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**FWP \_ E \_ \_ matrice di lunghezza zero \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-217"><span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**FWP\_E\_ZERO\_LENGTH\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-218">0x80320022</span><span class="sxs-lookup"><span data-stu-id="a7f6a-218">0x80320022</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-219">Una matrice che deve contenere almeno un elemento ha lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-219">An array that must contain at least one element has zero length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-220"><span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**\_ \_ \_ nome visualizzato FWP E \_ null**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-220"><span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**FWP\_E\_NULL\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-221">0x80320023</span><span class="sxs-lookup"><span data-stu-id="a7f6a-221">0x80320023</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-222">Il campo **displayData.Name** non può essere null.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-222">The **displayData.name** field cannot be null.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-223"><span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**FWP \_ E \_ \_ tipo di azione non valido \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-223"><span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**FWP\_E\_INVALID\_ACTION\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-224">0x80320024</span><span class="sxs-lookup"><span data-stu-id="a7f6a-224">0x80320024</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-225">Il tipo di azione non è uno dei tipi di azione consentiti per un filtro.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-225">The action type is not one of the allowed action types for a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-226"><span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**FWP \_ E \_ peso non valido \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-226"><span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**FWP\_E\_INVALID\_WEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-227">0x80320025</span><span class="sxs-lookup"><span data-stu-id="a7f6a-227">0x80320025</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-228">Il peso del filtro non è valido.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-228">The filter weight is not valid.</span></span>

<span data-ttu-id="a7f6a-229">Per ulteriori informazioni, vedere l' [assegnazione del peso del filtro](filter-weight-assignment.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f6a-229">See [Filter Weight Assignment](filter-weight-assignment.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-230"><span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**tipo di corrispondenza di FWP \_ E non \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-230"><span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**FWP\_E\_MATCH\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-231">0x80320026</span><span class="sxs-lookup"><span data-stu-id="a7f6a-231">0x80320026</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-232">Una condizione di filtro contiene un tipo di corrispondenza che non è compatibile con gli operandi.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-232">A filter condition contains a match type that is not compatible with the operands.</span></span>

<span data-ttu-id="a7f6a-233">Per ulteriori informazioni, vedere [**\_ \_ tipo di corrispondenza FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) .</span><span class="sxs-lookup"><span data-stu-id="a7f6a-233">See [**FWP\_MATCH\_TYPE**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-234"><span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**tipo di FWP \_ E non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-234"><span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**FWP\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-235">0x80320027</span><span class="sxs-lookup"><span data-stu-id="a7f6a-235">0x80320027</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-236">Una struttura [**FWP \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) o una [**struttura \_ \_ VALUE0 di FWPM Condition**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) è di tipo errato.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-236">An [**FWP\_VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) structure or an [**FWPM\_CONDITION\_VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) structure is of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-237"><span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP \_ E \_ fuori \_ \_ limite**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-237"><span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP\_E\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-238">0x80320028</span><span class="sxs-lookup"><span data-stu-id="a7f6a-238">0x80320028</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-239">Un valore integer non è compreso nell'intervallo consentito.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-239">An integer value is outside the allowed range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-240"><span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP \_ E \_ riservato**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-240"><span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP\_E\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-241">0x80320029</span><span class="sxs-lookup"><span data-stu-id="a7f6a-241">0x80320029</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-242">Un campo riservato è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-242">A reserved field is nonzero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-243"><span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**FWP \_ E \_ condizione duplicata \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-243"><span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**FWP\_E\_DUPLICATE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-244">0x8032002A</span><span class="sxs-lookup"><span data-stu-id="a7f6a-244">0x8032002A</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-245">Un filtro non può contenere più condizioni che operano su un singolo campo.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-245">A filter cannot contain multiple conditions operating on a single field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-246"><span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**\_KEYMOD FWP E \_ duplicati \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-246"><span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**FWP\_E\_DUPLICATE\_KEYMOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-247">0x8032002B</span><span class="sxs-lookup"><span data-stu-id="a7f6a-247">0x8032002B</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-248">Un criterio non può contenere lo stesso modulo di trasparenza più di una volta.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-248">A policy cannot contain the same keying module more than once.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-249"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**\_azione FWP \_ E \_ incompatibile \_ con il \_ livello**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-249"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**FWP\_E\_ACTION\_INCOMPATIBLE\_WITH\_LAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-250">0x8032002C</span><span class="sxs-lookup"><span data-stu-id="a7f6a-250">0x8032002C</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-251">Il tipo di azione non è compatibile con il livello.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-251">The action type is not compatible with the layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-252"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**\_azione FWP \_ E \_ incompatibile \_ con il \_ sottolivello**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-252"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**FWP\_E\_ACTION\_INCOMPATIBLE\_WITH\_SUBLAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-253">0x8032002D</span><span class="sxs-lookup"><span data-stu-id="a7f6a-253">0x8032002D</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-254">Il tipo di azione non è compatibile con il sottolivello.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-254">The action type is not compatible with the sub-layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-255"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**\_ \_ contesto di FWP E \_ incompatibile \_ con il \_ livello**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-255"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**FWP\_E\_CONTEXT\_INCOMPATIBLE\_WITH\_LAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-256">0x8032002E</span><span class="sxs-lookup"><span data-stu-id="a7f6a-256">0x8032002E</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-257">Il contesto non elaborato o il contesto del provider non è compatibile con il livello.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-257">The raw context or the provider context is not compatible with the layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-258"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**\_ \_ contesto di FWP E \_ incompatibile \_ con il \_ CALLOUT**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-258"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**FWP\_E\_CONTEXT\_INCOMPATIBLE\_WITH\_CALLOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-259">0x8032002F</span><span class="sxs-lookup"><span data-stu-id="a7f6a-259">0x8032002F</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-260">Il contesto non elaborato o il contesto del provider non è compatibile con il callout.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-260">The raw context or the provider context is not compatible with the callout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-261"><span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**FWP \_ E \_ metodo di \_ autenticazione incompatibile \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-261"><span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**FWP\_E\_INCOMPATIBLE\_AUTH\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-262">0x80320030</span><span class="sxs-lookup"><span data-stu-id="a7f6a-262">0x80320030</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-263">Il metodo di autenticazione non è compatibile con il tipo di criteri.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-263">The authentication method is not compatible with the policy type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-264"><span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP \_ E \_ \_ gruppo DH incompatibile \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-264"><span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP\_E\_INCOMPATIBLE\_DH\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-265">0x80320031L</span><span class="sxs-lookup"><span data-stu-id="a7f6a-265">0x80320031L</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-266">Il gruppo di Diffie-Hellman non è compatibile con il tipo di criteri.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-266">The Diffie-Hellman group is not compatible with the policy type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-267"><span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**FWP \_ E \_ em \_ non \_ supportati**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-267"><span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**FWP\_E\_EM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-268">0x80320032</span><span class="sxs-lookup"><span data-stu-id="a7f6a-268">0x80320032</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-269">Un criterio IKE non può contenere criteri per la modalità estesa.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-269">An IKE policy cannot contain an Extended Mode policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-270"><span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP \_ E \_ non \_ corrispondono mai**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-270"><span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP\_E\_NEVER\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-271">0x80320033</span><span class="sxs-lookup"><span data-stu-id="a7f6a-271">0x80320033</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-272">Il modello di enumerazione o la sottoscrizione non corrisponderà mai ad alcun oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-272">The enumeration template or subscription will never match any objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-273"><span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**contesto del provider di FWP \_ E non \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-273"><span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**FWP\_E\_PROVIDER\_CONTEXT\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-274">0x80320034</span><span class="sxs-lookup"><span data-stu-id="a7f6a-274">0x80320034</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-275">Il tipo del contesto del provider non è corretto.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-275">The provider context is of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-276"><span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**\_parametro FWP E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-276"><span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**FWP\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-277">0x80320035</span><span class="sxs-lookup"><span data-stu-id="a7f6a-277">0x80320035</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-278">Parametro non corretto.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-278">The parameter is incorrect.</span></span>

<span data-ttu-id="a7f6a-279">Possibili cause dell'errore:</span><span class="sxs-lookup"><span data-stu-id="a7f6a-279">Possible reasons for this error:</span></span>

-   <span data-ttu-id="a7f6a-280">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) è stato chiamato senza impostare il flag **FWPM \_ tunnel \_ flag \_ Point \_ su \_ Point** e con condizioni diverse dall'indirizzo locale/remoto.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-280">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) was called without setting the flag **FWPM\_TUNNEL\_FLAG\_POINT\_TO\_POINT** and with conditions other than local/remote address.</span></span>
-   <span data-ttu-id="a7f6a-281">Stringa Unicode non valida o stringa Unicode contenente caratteri non stampabili.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-281">An invalid Unicode string, or a Unicode string that contains unprintable characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-282"><span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP \_ E \_ troppi \_ \_ sottolivelli**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-282"><span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP\_E\_TOO\_MANY\_SUBLAYERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-283">0x80320036</span><span class="sxs-lookup"><span data-stu-id="a7f6a-283">0x80320036</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-284">È stato raggiunto il numero massimo di sottolivelli.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-284">The maximum number of sublayers has been reached.</span></span>

<span data-ttu-id="a7f6a-285">WFP supporta al massimo 2 6 sottolivelli.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-285">WFP supports at most 2 6 sublayers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-286"><span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**\_notifica FWP \_ E \_ CALLOUT \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-286"><span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**FWP\_E\_CALLOUT\_NOTIFICATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-287">0x80320037</span><span class="sxs-lookup"><span data-stu-id="a7f6a-287">0x80320037</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-288">La funzione di notifica per un callout ha restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-288">The notification function for a callout returned an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-289"><span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP \_ E \_ \_ trasformazione autenticazione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-289"><span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP\_E\_INVALID\_AUTH\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-290">0x80320038</span><span class="sxs-lookup"><span data-stu-id="a7f6a-290">0x80320038</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-291">Trasformazione autenticazione IPsec non valida.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-291">The IPsec authentication transform is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7f6a-292"><span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**FWP \_ E \_ \_ trasformazione di crittografia non valida \_**</span><span class="sxs-lookup"><span data-stu-id="a7f6a-292"><span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**FWP\_E\_INVALID\_CIPHER\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7f6a-293">0x80320039</span><span class="sxs-lookup"><span data-stu-id="a7f6a-293">0x80320039</span></span>
</dt> <dt>



<span data-ttu-id="a7f6a-294">Trasformazione crittografia IPsec non valida.</span><span class="sxs-lookup"><span data-stu-id="a7f6a-294">The IPsec cipher transform is not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7f6a-295">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7f6a-295">Requirements</span></span>



| <span data-ttu-id="a7f6a-296">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7f6a-296">Requirement</span></span> | <span data-ttu-id="a7f6a-297">Valore</span><span class="sxs-lookup"><span data-stu-id="a7f6a-297">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f6a-298">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7f6a-298">Minimum supported client</span></span><br/> | <span data-ttu-id="a7f6a-299">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7f6a-299">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a7f6a-300">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7f6a-300">Minimum supported server</span></span><br/> | <span data-ttu-id="a7f6a-301">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a7f6a-301">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7f6a-302">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7f6a-302">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7f6a-303"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7f6a-303"><dt>Winerror.h</dt></span></span> </dl> |



 

 





