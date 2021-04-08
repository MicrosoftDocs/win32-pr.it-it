---
title: Identificatori Right di accesso (Fwpmu. h)
description: Windows Filtering Platform (WFP) utilizza i diritti di accesso Win32 standard e un set di diritti di accesso specifici di WFP incorporati nella piattaforma di filtro.
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af182a087ade590e278bd3dd1d2bb1a64b5c598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964891"
---
# <a name="access-right-identifiers"></a><span data-ttu-id="92e29-103">Identificatori Right di accesso</span><span class="sxs-lookup"><span data-stu-id="92e29-103">Access Right Identifiers</span></span>

<span data-ttu-id="92e29-104">Windows Filtering Platform (WFP) utilizza i [diritti di accesso Win32 standard](/windows/desktop/SecAuthZ/standard-access-rights) e un set di diritti di accesso specifici di WFP incorporati nella piattaforma di filtro.</span><span class="sxs-lookup"><span data-stu-id="92e29-104">Windows Filtering Platform (WFP) uses the [standard Win32 access rights](/windows/desktop/SecAuthZ/standard-access-rights) plus a set of WFP-specific access rights built into the filtering platform.</span></span> <span data-ttu-id="92e29-105">Questi diritti di accesso vengono usati per proteggere gli oggetti solo in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="92e29-105">These access rights are used to secure objects in user mode only.</span></span> <span data-ttu-id="92e29-106">I chiamanti in modalità kernel ignorano tutti i controlli di accesso.</span><span class="sxs-lookup"><span data-stu-id="92e29-106">Kernel-mode callers bypass all access checks.</span></span>

<span data-ttu-id="92e29-107">Gli identificatori corretti di accesso specifici di WFP sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="92e29-107">WFP specific access right identifiers are as follows.</span></span>

<dl> <dt>

<span data-ttu-id="92e29-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**\_aggiunta FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="92e29-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-109">Aggiungere un oggetto al motore di filtro di base (BFE).</span><span class="sxs-lookup"><span data-stu-id="92e29-109">Add an object to the Base Filtering Engine (BFE).</span></span> <span data-ttu-id="92e29-110">Questo diritto di accesso è necessario per chiamare le [**funzioni \* Add0 di Fwpm**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) .</span><span class="sxs-lookup"><span data-stu-id="92e29-110">This access right is needed in order to call [**Fwpm\*Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ Aggiungi \_ collegamento**</span><span class="sxs-lookup"><span data-stu-id="92e29-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-112">Aggiungere un oggetto a cui si fa riferimento tramite un collegamento.</span><span class="sxs-lookup"><span data-stu-id="92e29-112">Add an object referenced through a link.</span></span> <span data-ttu-id="92e29-113">Ad esempio, questo diritto di accesso è necessario per i callout a cui viene fatto riferimento tramite GUID.</span><span class="sxs-lookup"><span data-stu-id="92e29-113">For example, this access right is needed for callouts referenced through GUIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Read \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="92e29-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-115">Inizia una transazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="92e29-115">Begin a read-only transaction.</span></span> <span data-ttu-id="92e29-116">Questo diritto di accesso è necessario per chiamare [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).</span><span class="sxs-lookup"><span data-stu-id="92e29-116">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Write \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="92e29-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-118">Inizia una transazione di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="92e29-118">Begin a read/write transaction.</span></span> <span data-ttu-id="92e29-119">Questo diritto di accesso è necessario per chiamare [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) per una transazione di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="92e29-119">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) for a read/write transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_classificazione FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="92e29-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-121">Classificazione RPC (Remote Procedure Call).</span><span class="sxs-lookup"><span data-stu-id="92e29-121">Classify Remote Procedure Call (RPC).</span></span> <span data-ttu-id="92e29-122">Questo diritto di accesso è necessario per la fase di esecuzione RPC per applicare i filtri RPC.</span><span class="sxs-lookup"><span data-stu-id="92e29-122">This access right is needed by the RPC run-time in order to enforce RPC filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**\_enumerazione FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="92e29-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-124">Enumerare.</span><span class="sxs-lookup"><span data-stu-id="92e29-124">Enumerate.</span></span> <span data-ttu-id="92e29-125">Questo diritto di accesso è necessario per chiamare le [**funzioni \* CreateEnumHandle0 di Fwpm**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) .</span><span class="sxs-lookup"><span data-stu-id="92e29-125">This access right is needed in order to call [**Fwpm\*CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) functions.</span></span> <span data-ttu-id="92e29-126">Per enumerare un oggetto, il chiamante deve anche \_ \_ avere l'accesso in lettura ACTRL FWPM all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="92e29-126">To enumerate an object, the caller also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="92e29-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-128">Aprire una sessione del motore di filtro.</span><span class="sxs-lookup"><span data-stu-id="92e29-128">Open a session to the filter engine.</span></span> <span data-ttu-id="92e29-129">Questo diritto di accesso è necessario per chiamare [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="92e29-129">This access right is needed in order to call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="92e29-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-131">Lettura.</span><span class="sxs-lookup"><span data-stu-id="92e29-131">Read.</span></span> <span data-ttu-id="92e29-132">Questo diritto di accesso è necessario per chiamare le funzioni [**Fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) e [**Fwpm \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) .</span><span class="sxs-lookup"><span data-stu-id="92e29-132">This access right is needed in order to call [**Fwpm\*GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) and [**Fwpm\*GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**\_ \_ statistiche leggere FWPM \_ ACTRL**</span><span class="sxs-lookup"><span data-stu-id="92e29-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-134">Leggere le statistiche.</span><span class="sxs-lookup"><span data-stu-id="92e29-134">Read statistics.</span></span> <span data-ttu-id="92e29-135">Questo diritto di accesso è necessario per chiamare [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) e [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).</span><span class="sxs-lookup"><span data-stu-id="92e29-135">This access right is needed in order to call [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) and [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**sottoscrizione di FWPM \_ ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="92e29-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-137">Eseguire la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="92e29-137">Subscribe.</span></span> <span data-ttu-id="92e29-138">Questo diritto di accesso è necessario per chiamare le [**funzioni \* SubscribeChanges0 di Fwpm**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) .</span><span class="sxs-lookup"><span data-stu-id="92e29-138">This access right is needed in order to call [**Fwpm\*SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) functions.</span></span> <span data-ttu-id="92e29-139">Per ricevere una notifica per un oggetto, un Sottoscrittore deve \_ \_ avere anche l'accesso in lettura a FWPM ACTRL per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="92e29-139">To receive a notification for an object, a subscriber also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**\_scrittura FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="92e29-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-141">Opzioni del motore di scrittura.</span><span class="sxs-lookup"><span data-stu-id="92e29-141">Write engine options.</span></span> <span data-ttu-id="92e29-142">Questo diritto di accesso è necessario per chiamare [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).</span><span class="sxs-lookup"><span data-stu-id="92e29-142">This access right is needed in order to call [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**\_lettura generica FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="92e29-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**FWPM\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-144">\_diritti standard \_ letti \| FWPM \_ ACTRL \_ Begin \_ Read \_ transazione \| FWPM \_ ACTRL \_ classifica \| FWPM \_ ACTRL \_ Open \| FWPM \_ ACTRL \_ Read \| FWPM \_ ACTRL \_ Read \_ Statistics</span><span class="sxs-lookup"><span data-stu-id="92e29-144">STANDARD\_RIGHTS\_READ \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**\_esecuzione generica FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="92e29-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**FWPM\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-146">\_diritti standard \_ Execute \| FWPM \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ Subscribe</span><span class="sxs-lookup"><span data-stu-id="92e29-146">STANDARD\_RIGHTS\_EXECUTE \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_SUBSCRIBE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**\_scrittura generica FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="92e29-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**FWPM\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-148">\_Rights \_ Write \| ( \| FWPM) \_ ACTRL \_ Aggiungi \| FWPM ACTRL Aggiungi \_ \_ \_ collegamento \| FWPM \_ ACTRL \_ Begin \_ Write \_ transazione \| \_ \_ FWPM ACTRL Write</span><span class="sxs-lookup"><span data-stu-id="92e29-148">STANDARD\_RIGHTS\_WRITE \| DELETE \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92e29-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ generico \_ All**</span><span class="sxs-lookup"><span data-stu-id="92e29-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM\_GENERIC\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92e29-150">\_diritti standard \_ necessari \| FWPM \_ ACTRL \_ Aggiungi \| FWPM \_ ACTRL \_ Aggiungi \_ collegamento \| FWPM \_ ACTRL \_ Begin \_ Read \_ transazione \| FWPM \_ ACTRL \_ Begin \_ Write \_ transazione FWPM ACTRL \| \_ \_ classifica \| FWPM \_ ACTRL enum FWPM ACTRL \_ \| \_ \_ Open \| FWPM \_ ACTRL \_ Read \| FWPM \_ ACTRL \_ Read \_ Statistics \| FWPM ACTRL Subscribe FWPM \_ \_ \| \_ ACTRL \_ Write</span><span class="sxs-lookup"><span data-stu-id="92e29-150">STANDARD\_RIGHTS\_REQUIRED \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS \| FWPM\_ACTRL\_SUBSCRIBE \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92e29-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92e29-151">Requirements</span></span>



| <span data-ttu-id="92e29-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="92e29-152">Requirement</span></span> | <span data-ttu-id="92e29-153">Valore</span><span class="sxs-lookup"><span data-stu-id="92e29-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92e29-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92e29-154">Minimum supported client</span></span><br/> | <span data-ttu-id="92e29-155">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92e29-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92e29-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92e29-156">Minimum supported server</span></span><br/> | <span data-ttu-id="92e29-157">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92e29-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92e29-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92e29-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="92e29-159"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="92e29-159"><dt>Fwpmu.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92e29-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92e29-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e29-161">Modello di controllo di accesso della piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="92e29-161">Windows Filtering Platform Access Control Model</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="92e29-162">Diritti di accesso standard</span><span class="sxs-lookup"><span data-stu-id="92e29-162">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

