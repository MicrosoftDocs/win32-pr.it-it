---
title: Metodo SyncNamingContext della classe MSAD_ReplNeighbor
description: Chiama la funzione DsReplicaSync che sincronizza un contesto dei nomi di destinazione con una delle relative origini.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Active Directory del metodo SyncNamingContext
- Metodo SyncNamingContext Active Directory, classe MSAD_ReplNeighbor
- Classe MSAD_ReplNeighbor Active Directory, metodo SyncNamingContext
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691bd3e943f491ba93d867097ac0167c97be6108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478286"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a><span data-ttu-id="675df-106">Metodo SyncNamingContext della classe MSAD \_ ReplNeighbor</span><span class="sxs-lookup"><span data-stu-id="675df-106">SyncNamingContext method of the MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="675df-107">Chiama la funzione [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) che sincronizza un contesto dei nomi di destinazione con una delle relative origini.</span><span class="sxs-lookup"><span data-stu-id="675df-107">Calls the [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) function that synchronizes a destination naming context with one of its sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="675df-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="675df-108">Syntax</span></span>


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a><span data-ttu-id="675df-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="675df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="675df-110">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="675df-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="675df-111">Dati aggiuntivi che determinano la modalità di elaborazione della richiesta da parte del metodo.</span><span class="sxs-lookup"><span data-stu-id="675df-111">Additional data that determines how the method processes the request.</span></span> <span data-ttu-id="675df-112">Questo parametro può essere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="675df-112">This parameter can be a combination of the following values.</span></span>

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span data-ttu-id="675df-113"><span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**\_ \_ Aggiungi \_ riferimento a DS REPSYNC**</span><span class="sxs-lookup"><span data-stu-id="675df-113"><span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**DS\_REPSYNC\_ADD\_REFERENCE**</span></span>


</dt> <dd>

<span data-ttu-id="675df-114">Fa in modo che il Directory System Agent di origine (DSA) verifichi che il DSA locale sia presente nell'elenco replicate di origine.</span><span class="sxs-lookup"><span data-stu-id="675df-114">Causes the source directory system agent (DSA) to verify that the local DSA is present in the source replicates-to list.</span></span> <span data-ttu-id="675df-115">Se il DSA locale non è presente, viene aggiunto.</span><span class="sxs-lookup"><span data-stu-id="675df-115">If the local DSA is not present, it is added.</span></span> <span data-ttu-id="675df-116">In questo modo si garantisce che l'origine invii le notifiche di modifica.</span><span class="sxs-lookup"><span data-stu-id="675df-116">This ensures that the source sends change notifications.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span data-ttu-id="675df-117"><span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ REPSYNC \_ tutte le \_ origini**</span><span class="sxs-lookup"><span data-stu-id="675df-117"><span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS\_REPSYNC\_ALL\_SOURCES**</span></span>


</dt> <dd>

<span data-ttu-id="675df-118">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="675df-118">This value is not supported.</span></span>

<span data-ttu-id="675df-119">**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Sincronizza da tutte le origini.</span><span class="sxs-lookup"><span data-stu-id="675df-119">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** Synchronizes from all sources.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span data-ttu-id="675df-120"><span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**\_ \_ operazione asincrona REPSYNC \_ DS**</span><span class="sxs-lookup"><span data-stu-id="675df-120"><span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**DS\_REPSYNC\_ASYNCHRONOUS\_OPERATION**</span></span>


</dt> <dd>

<span data-ttu-id="675df-121">Esegue questa operazione in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="675df-121">Performs this operation asynchronously.</span></span>

<span data-ttu-id="675df-122">**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Obbligatorio quando si usa **DS \_ REPSYNC \_ tutte le \_ origini**.</span><span class="sxs-lookup"><span data-stu-id="675df-122">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** Required when using **DS\_REPSYNC\_ALL\_SOURCES**.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span data-ttu-id="675df-123"><span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**\_forza REPSYNC \_ DS**</span><span class="sxs-lookup"><span data-stu-id="675df-123"><span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS\_REPSYNC\_FORCE**</span></span>


</dt> <dd>

<span data-ttu-id="675df-124">Viene sincronizzato anche se il collegamento è attualmente disabilitato.</span><span class="sxs-lookup"><span data-stu-id="675df-124">Synchronizes even if the link is currently disabled.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span data-ttu-id="675df-125"><span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS \_ REPSYNC \_ completo**</span><span class="sxs-lookup"><span data-stu-id="675df-125"><span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS\_REPSYNC\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="675df-126">Viene sincronizzato a partire dal primo numero di sequenza di aggiornamento (USN).</span><span class="sxs-lookup"><span data-stu-id="675df-126">Synchronizes starting from the first Update Sequence Number (USN).</span></span>

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span data-ttu-id="675df-127"><span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**\_messaggistica tra \_ siti DS \_ REPSYNC**</span><span class="sxs-lookup"><span data-stu-id="675df-127"><span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**DS\_REPSYNC\_INTERSITE\_MESSAGING**</span></span>


</dt> <dd>

<span data-ttu-id="675df-128">Viene sincronizzato utilizzando ISM.</span><span class="sxs-lookup"><span data-stu-id="675df-128">Synchronizes using an ISM.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span data-ttu-id="675df-129"><span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS \_ REPSYNC \_ No \_ scarto**</span><span class="sxs-lookup"><span data-stu-id="675df-129"><span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS\_REPSYNC\_NO\_DISCARD**</span></span>


</dt> <dd>

<span data-ttu-id="675df-130">Non rimuove questa richiesta di sincronizzazione, anche se è in sospeso una sincronizzazione simile.</span><span class="sxs-lookup"><span data-stu-id="675df-130">Does not discard this synchronization request, even if a similar synchronization is pending.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span data-ttu-id="675df-131"><span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ REPSYNC \_ periodica**</span><span class="sxs-lookup"><span data-stu-id="675df-131"><span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS\_REPSYNC\_PERIODIC**</span></span>


</dt> <dd>

<span data-ttu-id="675df-132">Indica che questa operazione è una richiesta di sincronizzazione periodica pianificata dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="675df-132">Indicates that this operation is a periodic synchronization request that is scheduled by the administrator.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span data-ttu-id="675df-133"><span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS \_ REPSYNC \_ urgente**</span><span class="sxs-lookup"><span data-stu-id="675df-133"><span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS\_REPSYNC\_URGENT**</span></span>


</dt> <dd>

<span data-ttu-id="675df-134">Indica che questa operazione è una notifica di un aggiornamento contrassegnato come urgente.</span><span class="sxs-lookup"><span data-stu-id="675df-134">Indicates that this operation is a notification of an update that is marked as urgent.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span data-ttu-id="675df-135"><span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS \_ REPSYNC \_ scrivibile**</span><span class="sxs-lookup"><span data-stu-id="675df-135"><span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS\_REPSYNC\_WRITEABLE**</span></span>


</dt> <dd>

<span data-ttu-id="675df-136">Indica che la replica è scrivibile.</span><span class="sxs-lookup"><span data-stu-id="675df-136">Indicates that this replica is writable.</span></span> <span data-ttu-id="675df-137">Se questo flag non è impostato, la replica è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="675df-137">If this flag is not set, the replica is read-only.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="675df-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="675df-138">Return value</span></span>

<span data-ttu-id="675df-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="675df-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="675df-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="675df-140">Requirements</span></span>



| <span data-ttu-id="675df-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="675df-141">Requirement</span></span> | <span data-ttu-id="675df-142">Valore</span><span class="sxs-lookup"><span data-stu-id="675df-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="675df-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="675df-143">Minimum supported client</span></span><br/> | <span data-ttu-id="675df-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="675df-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="675df-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="675df-145">Minimum supported server</span></span><br/> | <span data-ttu-id="675df-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="675df-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="675df-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="675df-147">Namespace</span></span><br/>                | <span data-ttu-id="675df-148">\\MicrosoftActiveDirectory radice</span><span class="sxs-lookup"><span data-stu-id="675df-148">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="675df-149">MOF</span><span class="sxs-lookup"><span data-stu-id="675df-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="675df-150"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="675df-150"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="675df-151">DLL</span><span class="sxs-lookup"><span data-stu-id="675df-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="675df-152"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="675df-152"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="675df-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="675df-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="675df-154">**\_REPLNEIGHBOR MSAD**</span><span class="sxs-lookup"><span data-stu-id="675df-154">**MSAD\_ReplNeighbor**</span></span>](msad-replneighbor.md)
</dt> </dl>

 

 





