---
title: Classe MSAD_ReplNeighbor
description: Rappresenta la \_ \_ struttura Neighbor REPL di DS, che contiene le informazioni sullo stato di replica in ingresso per un particolare contesto dei nomi (NC) e una coppia di server di origine.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- Classe MSAD_ReplNeighbor Active Directory
- Classe MSAD_ReplNeighbor Active Directory, descritta
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor
- MSAD_ReplNeighbor.NamingContextDN
- MSAD_ReplNeighbor.SourceDsaObjGuid
- MSAD_ReplNeighbor.NamingContextObjGuid
- MSAD_ReplNeighbor.SourceDsaDN
- MSAD_ReplNeighbor.SourceDsaAddress
- MSAD_ReplNeighbor.SourceDsaInvocationID
- MSAD_ReplNeighbor.AsyncIntersiteTransportDN
- MSAD_ReplNeighbor.AsyncIntersiteTransportObjGuid
- MSAD_ReplNeighbor.USNLastObjChangeSynced
- MSAD_ReplNeighbor.USNAttributeFilter
- MSAD_ReplNeighbor.TimeOfLastSyncSuccess
- MSAD_ReplNeighbor.TimeOfLastSyncAttempt
- MSAD_ReplNeighbor.LastSyncResult
- MSAD_ReplNeighbor.NumConsecutiveSyncFailures
- MSAD_ReplNeighbor.ReplicaFlags
- MSAD_ReplNeighbor.Writeable
- MSAD_ReplNeighbor.SyncOnStartup
- MSAD_ReplNeighbor.DoScheduledSyncs
- MSAD_ReplNeighbor.UseAsyncIntersiteTransport
- MSAD_ReplNeighbor.TwoWaySync
- MSAD_ReplNeighbor.FullSyncInProgress
- MSAD_ReplNeighbor.FullSyncNextPacket
- MSAD_ReplNeighbor.NeverSynced
- MSAD_ReplNeighbor.IgnoreChangeNotifications
- MSAD_ReplNeighbor.DisableScheduledSync
- MSAD_ReplNeighbor.CompressChanges
- MSAD_ReplNeighbor.NoChangeNotifications
- MSAD_ReplNeighbor.SourceDsaSite
- MSAD_ReplNeighbor.SourceDsaCN
- MSAD_ReplNeighbor.Domain
- MSAD_ReplNeighbor.IsDeletedSourceDsa
- MSAD_ReplNeighbor.ModifiedNumConsecutiveSyncFailures
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9554c73c7fb84aad10ae6dda51480a7644d8434a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964264"
---
# <a name="msad_replneighbor-class"></a><span data-ttu-id="4bf44-105">\_Classe MSAD ReplNeighbor</span><span class="sxs-lookup"><span data-stu-id="4bf44-105">MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="4bf44-106">Rappresenta la [**struttura \_ \_ Neighbor REPL di DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) , che contiene le informazioni sullo stato di replica in ingresso per una determinata coppia di contesto dei nomi e server di origine, come restituito dalla funzione [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .</span><span class="sxs-lookup"><span data-stu-id="4bf44-106">Represents the [**DS\_REPL\_NEIGHBOR**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) structure, which contains the inbound replication state information for a particular naming context (NC) and source server pair, as returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bf44-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4bf44-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplNeighbor
{
  String   NamingContextDN;
  String   SourceDsaObjGuid;
  String   NamingContextObjGuid;
  String   SourceDsaDN;
  String   SourceDsaAddress;
  String   SourceDsaInvocationID;
  String   AsyncIntersiteTransportDN;
  String   AsyncIntersiteTransportObjGuid;
  uint64   USNLastObjChangeSynced;
  uint64   USNAttributeFilter;
  datetime TimeOfLastSyncSuccess;
  datetime TimeOfLastSyncAttempt;
  uint32   LastSyncResult;
  uint32   NumConsecutiveSyncFailures;
  uint32   ReplicaFlags;
  boolean  Writeable = FALSE;
  boolean  SyncOnStartup = FALSE;
  boolean  DoScheduledSyncs = FALSE;
  boolean  UseAsyncIntersiteTransport = FALSE;
  boolean  TwoWaySync = FALSE;
  boolean  FullSyncInProgress = FALSE;
  boolean  FullSyncNextPacket = FALSE;
  boolean  NeverSynced = FALSE;
  boolean  IgnoreChangeNotifications = FALSE;
  boolean  DisableScheduledSync = FALSE;
  boolean  CompressChanges = FALSE;
  boolean  NoChangeNotifications = FALSE;
  String   SourceDsaSite;
  String   SourceDsaCN;
  String   Domain;
  boolean  IsDeletedSourceDsa = FALSE;
  uint32   ModifiedNumConsecutiveSyncFailures;
};
```

## <a name="members"></a><span data-ttu-id="4bf44-108">Members</span><span class="sxs-lookup"><span data-stu-id="4bf44-108">Members</span></span>

<span data-ttu-id="4bf44-109">La **classe \_ ReplNeighbor di MSAD** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4bf44-109">The **MSAD\_ReplNeighbor** class has these types of members:</span></span>

-   [<span data-ttu-id="4bf44-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="4bf44-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4bf44-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4bf44-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4bf44-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="4bf44-112">Methods</span></span>

<span data-ttu-id="4bf44-113">La **classe \_ ReplNeighbor di MSAD** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4bf44-113">The **MSAD\_ReplNeighbor** class has these methods.</span></span>



| <span data-ttu-id="4bf44-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="4bf44-114">Method</span></span>                                                           | <span data-ttu-id="4bf44-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bf44-115">Description</span></span>                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="4bf44-116">**SyncNamingContext**</span><span class="sxs-lookup"><span data-stu-id="4bf44-116">**SyncNamingContext**</span></span>](syncnamingcontext-msad-replneighbor.md) | <span data-ttu-id="4bf44-117">Sincronizza un contesto dei nomi di destinazione con una delle relative origini.</span><span class="sxs-lookup"><span data-stu-id="4bf44-117">Synchronizes a destination naming context with one of its sources.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4bf44-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4bf44-118">Properties</span></span>

<span data-ttu-id="4bf44-119">La **classe \_ ReplNeighbor di MSAD** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4bf44-119">The **MSAD\_ReplNeighbor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4bf44-120">**AsyncIntersiteTransportDN**</span><span class="sxs-lookup"><span data-stu-id="4bf44-120">**AsyncIntersiteTransportDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4bf44-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-123">Ottiene il percorso X. 500 dell'oggetto [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) che corrisponde al trasporto su cui viene eseguita la replica.</span><span class="sxs-lookup"><span data-stu-id="4bf44-123">Gets the X.500 path of the [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) object that corresponds to the transport over which replication is performed.</span></span> <span data-ttu-id="4bf44-124">Impostare su **null** per la replica RPC/IP.</span><span class="sxs-lookup"><span data-stu-id="4bf44-124">Set to **NULL** for RPC/IP replication.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-125">**AsyncIntersiteTransportObjGuid**</span><span class="sxs-lookup"><span data-stu-id="4bf44-125">**AsyncIntersiteTransportObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4bf44-126">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-128">Ottiene il GUID dell'oggetto trasporto tra siti che corrisponde alla proprietà **AsyncIntersiteTransportDN** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-128">Gets the GUID of the intersite transport object that corresponds to the **AsyncIntersiteTransportDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-129">**CompressChanges**</span><span class="sxs-lookup"><span data-stu-id="4bf44-129">**CompressChanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-130">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-132">Ottiene il valore che indica se il flag **DS \_ REPL \_ NBR \_ compress \_ changes** è stato impostato nella proprietà **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-132">Gets the value that indicates whether the **DS\_REPL\_NBR\_COMPRESS\_CHANGES** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-133">**DisableScheduledSync**</span><span class="sxs-lookup"><span data-stu-id="4bf44-133">**DisableScheduledSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-136">Ottiene il valore che indica se il flag di **\_ \_ \_ \_ \_ sincronizzazione pianificata per la disabilitazione di DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-136">Gets the value that indicates whether the **DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-137">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="4bf44-137">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4bf44-138">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-140">Ottiene il nome canonico del dominio del NC replicato.</span><span class="sxs-lookup"><span data-stu-id="4bf44-140">Gets the canonical name of the domain of the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-141">**DoScheduledSyncs**</span><span class="sxs-lookup"><span data-stu-id="4bf44-141">**DoScheduledSyncs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-142">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-144">Ottiene il valore che indica se il flag di **\_ \_ \_ \_ \_ sincronizzazione pianificato DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-144">Gets the value that indicates whether the **DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-145">**FullSyncInProgress**</span><span class="sxs-lookup"><span data-stu-id="4bf44-145">**FullSyncInProgress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-146">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-148">Ottiene il valore che indica se il **flag \_ \_ \_ \_ \_ di sincronizzazione \_ completa DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-148">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-149">**FullSyncNextPacket**</span><span class="sxs-lookup"><span data-stu-id="4bf44-149">**FullSyncNextPacket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-150">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-152">Ottiene il valore che indica se il flag del **\_ \_ \_ \_ \_ \_ pacchetto successivo DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-152">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-153">**IgnoreChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="4bf44-153">**IgnoreChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-154">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-156">Ottiene il valore che indica se il flag di **notifica delle \_ \_ \_ \_ modifiche \_ di DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-156">Gets the value that indicates whether the **DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-157">**IsDeletedSourceDsa**</span><span class="sxs-lookup"><span data-stu-id="4bf44-157">**IsDeletedSourceDsa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-158">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-160">Ottiene il valore che indica se questa connessione rappresenta un controller di dominio di origine che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="4bf44-160">Gets the value that indicates whether this connection represents a source DC that has been deleted.</span></span> <span data-ttu-id="4bf44-161">**True** se questa connessione rappresenta un controller di dominio di origine che è stato eliminato. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="4bf44-161">**TRUE** if this connection represents a source DC that has been deleted; otherwise, **FALSE**.</span></span> <span data-ttu-id="4bf44-162">Per impostazione predefinita, il servizio DS continuerà a replicare queste connessioni per un certo periodo di tempo dopo l'eliminazione del controller di dominio di origine.</span><span class="sxs-lookup"><span data-stu-id="4bf44-162">By design, the DS will continue to replicate these connections for some time for some time after the source DC is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-163">**LastSyncResult**</span><span class="sxs-lookup"><span data-stu-id="4bf44-163">**LastSyncResult**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-164">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4bf44-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-166">Ottiene il codice di errore **HRESULT** per l'ultimo tentativo di replica.</span><span class="sxs-lookup"><span data-stu-id="4bf44-166">Gets the **HRESULT** error code for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-167">**ModifiedNumConsecutiveSyncFailures**</span><span class="sxs-lookup"><span data-stu-id="4bf44-167">**ModifiedNumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-168">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4bf44-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-170">Ottiene il numero di tentativi consecutivi di replica non riusciti, escluse le connessioni che dovrebbero avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4bf44-170">Gets the number of consecutive failed replication attempts, not including the connections that are expected to fail.</span></span> <span data-ttu-id="4bf44-171">Se, ad esempio, la proprietà **IsDeletedSourceDsa** è impostata su **true**, è previsto che abbia esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4bf44-171">For example, if the **IsDeletedSourceDsa** property is set to **TRUE**, it is expected to fail.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-172">**NamingContextDN**</span><span class="sxs-lookup"><span data-stu-id="4bf44-172">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4bf44-173">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-175">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4bf44-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-176">Ottiene il percorso X. 500 per il NC replicato da questa connessione.</span><span class="sxs-lookup"><span data-stu-id="4bf44-176">Gets the X.500 path for the NC that is replicated by this connection.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-177">**NamingContextObjGuid**</span><span class="sxs-lookup"><span data-stu-id="4bf44-177">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4bf44-178">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-180">Ottiene il GUID per il NC replicato.</span><span class="sxs-lookup"><span data-stu-id="4bf44-180">Gets the GUID for the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-181">**NeverSynced**</span><span class="sxs-lookup"><span data-stu-id="4bf44-181">**NeverSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-182">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-184">Ottiene il valore che indica se il flag **DS \_ REPL \_ NBR \_ mai \_ sincronizzato** è stato impostato nella proprietà **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-184">Gets the value that indicates whether the **DS\_REPL\_NBR\_NEVER\_SYNCED** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-185">**NoChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="4bf44-185">**NoChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-186">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-188">Ottiene il valore che indica se il flag **DS \_ REPL \_ NBR \_ No \_ Change \_ Notifications** è stato impostato nella proprietà **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-188">Gets the value that indicates whether the **DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-189">**NumConsecutiveSyncFailures**</span><span class="sxs-lookup"><span data-stu-id="4bf44-189">**NumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-190">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4bf44-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-192">Ottiene il numero di tentativi consecutivi di replica non riusciti.</span><span class="sxs-lookup"><span data-stu-id="4bf44-192">Gets the number of consecutive failed replication attempts.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-193">**ReplicaFlags**</span><span class="sxs-lookup"><span data-stu-id="4bf44-193">**ReplicaFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-194">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4bf44-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-196">Ottiene il set di flag che specificano attributi e opzioni per i dati di replica.</span><span class="sxs-lookup"><span data-stu-id="4bf44-196">Gets the set of flags that specify attributes and options for the replication data.</span></span> <span data-ttu-id="4bf44-197">Questa proprietà può essere zero o una combinazione di uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="4bf44-197">This property can be zero or a combination of one or more of the following flags.</span></span>

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span data-ttu-id="4bf44-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ scrivibile** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="4bf44-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS\_REPL\_NBR\_WRITEABLE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-199">La copia locale del contesto di denominazione è modificabile.</span><span class="sxs-lookup"><span data-stu-id="4bf44-199">The local copy of the naming context is writable.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span data-ttu-id="4bf44-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ Sync \_ all' \_ avvio** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="4bf44-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-201">Viene eseguito un tentativo di replica del contesto dei nomi da questa origine quando viene avviato il server di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4bf44-201">Replication of this naming context from this source is attempted when the destination server is booted.</span></span> <span data-ttu-id="4bf44-202">Questo flag in genere si applica solo agli elementi adiacenti all'interno del sito.</span><span class="sxs-lookup"><span data-stu-id="4bf44-202">This flag usually only applies to intra-site neighbors.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span data-ttu-id="4bf44-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ do \_ \_ syncs scheduled** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="4bf44-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-204">La replica viene eseguita in base a una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4bf44-204">Perform replication on a schedule.</span></span> <span data-ttu-id="4bf44-205">Questo flag viene in genere impostato a meno che la pianificazione per questo contesto dei nomi o origine non sia "mai", ovvero la pianificazione vuota.</span><span class="sxs-lookup"><span data-stu-id="4bf44-205">This flag is usually set unless the schedule for this naming context or source is "never", that is, the empty schedule.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span data-ttu-id="4bf44-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ Usa \_ il \_ \_ trasporto asincrono tra siti** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="4bf44-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-207">La replica viene eseguita indirettamente tramite il servizio Messaggistica tra siti (ISM).</span><span class="sxs-lookup"><span data-stu-id="4bf44-207">Perform replication indirectly through the Inter-Site Messaging Service.</span></span> <span data-ttu-id="4bf44-208">Questo flag è impostato solo per la replica tramite SMTP.</span><span class="sxs-lookup"><span data-stu-id="4bf44-208">This flag is set only when replicating over SMTP.</span></span> <span data-ttu-id="4bf44-209">Il flag non è impostato durante la replica tramite RPC/IP tra siti.</span><span class="sxs-lookup"><span data-stu-id="4bf44-209">This flag is not set when replicating over inter-site RPC/IP.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span data-ttu-id="4bf44-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ \_ bidirezionale \_ Sync** (512 (0x200))</span><span class="sxs-lookup"><span data-stu-id="4bf44-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS\_REPL\_NBR\_TWO\_WAY\_SYNC** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-211">Se impostato, indica che quando la replica in ingresso è completa, il server di destinazione deve indicare al server di origine di eseguire la sincronizzazione in direzione inversa.</span><span class="sxs-lookup"><span data-stu-id="4bf44-211">If set, indicates that when inbound replication is complete, the destination server must tell the source server to synchronize in the reverse direction.</span></span> <span data-ttu-id="4bf44-212">Questa funzionalità viene utilizzata nel caso di connessioni remote, qualora solo uno dei due server sia in grado di inizializzare la connessione.</span><span class="sxs-lookup"><span data-stu-id="4bf44-212">This feature is used in dial-up scenarios where only one of the two servers can initiate a dial-up connection.</span></span> <span data-ttu-id="4bf44-213">Questa opzione, ad esempio, può essere usata in una sede aziendale e in una succursale, in cui la succursale si connette alla sede aziendale tramite Internet per mezzo di una connessione ISP remota.</span><span class="sxs-lookup"><span data-stu-id="4bf44-213">For example, this option could be used in a corporate headquarters and branch office, where the branch office connects to the corporate headquarters over the Internet by means of a dial-up ISP connection.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span data-ttu-id="4bf44-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ Restituisci \_ oggetti \_ padre** (2048 (0x800))</span><span class="sxs-lookup"><span data-stu-id="4bf44-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS\_REPL\_NBR\_RETURN\_OBJECT\_PARENTS** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-215">L'elemento adiacente restituisce gli oggetti padre prima degli oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="4bf44-215">This neighbor is in a state where it returns parent objects before children objects.</span></span> <span data-ttu-id="4bf44-216">Questo stato viene attivato quando l'elemento adiacente riceve un oggetto figlio prima del padre.</span><span class="sxs-lookup"><span data-stu-id="4bf44-216">It goes into this state after it receives a child object before its parent.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span data-ttu-id="4bf44-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>Servizi di **dominio Active Directory \_ \_ \_ Sincronizzazione completa REPL \_ NBR \_ in \_ corso** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="4bf44-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-218">È in corso una sincronizzazione completa del server di destinazione dal server di origine.</span><span class="sxs-lookup"><span data-stu-id="4bf44-218">The destination server is performing a full synchronization from the source server.</span></span> <span data-ttu-id="4bf44-219">Le sincronizzazioni complete non utilizzano vettori per la creazione di aggiornamenti (ad esempio, i [**\_ \_ cursori REPL DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) per filtrare gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="4bf44-219">Full synchronizations do not use vectors that create updates (such as [**DS\_REPL\_CURSORS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) for filtering updates.</span></span> <span data-ttu-id="4bf44-220">Le sincronizzazioni complete non vengono utilizzate come parte del protocollo di replica predefinito.</span><span class="sxs-lookup"><span data-stu-id="4bf44-220">Full synchronizations are not used as a part of the default replication protocol.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span data-ttu-id="4bf44-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>Servizi di **dominio Active Directory \_ \_ \_ \_ \_ \_ Pacchetto successivo sincronizzazione completa REPL NBR** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="4bf44-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-222">L'ultimo pacchetto dall'origine indica una modifica di un oggetto non ancora creato dal server di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4bf44-222">The last packet from the source indicated a modification of an object that the destination server has not yet created.</span></span> <span data-ttu-id="4bf44-223">Il pacchetto successivo da richiedere indica al server di origine di inserire tutti gli attributi dell'oggetto modificato nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4bf44-223">The next packet to be requested instructs the source server to put all attributes of the modified object into the packet.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span data-ttu-id="4bf44-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ mai \_ sincronizzato** (2097152 (0x200000))</span><span class="sxs-lookup"><span data-stu-id="4bf44-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS\_REPL\_NBR\_NEVER\_SYNCED** (2097152 (0x200000))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-225">Non è mai stata completata alcuna operazione di sincronizzazione da questa origine.</span><span class="sxs-lookup"><span data-stu-id="4bf44-225">A synchronization has never been successfully completed from this source.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span data-ttu-id="4bf44-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR con \_ precedenza** (16777216 (0x1000000))</span><span class="sxs-lookup"><span data-stu-id="4bf44-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS\_REPL\_NBR\_PREEMPTED** (16777216 (0x1000000))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-227">Il motore di replica ha interrotto temporaneamente l'elaborazione di questo elemento adiacente per poter servire un altro Neighbor con priorità più alta, per questa partizione o per un'altra partizione.</span><span class="sxs-lookup"><span data-stu-id="4bf44-227">The replication engine has temporarily stopped processing this neighbor in order to service another higher-priority neighbor, either for this partition or for another partition.</span></span> <span data-ttu-id="4bf44-228">L'elaborazione dell'elemento adiacente verrà ripresa dal motore di replica una volta completato il lavoro con priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="4bf44-228">The replication engine will resume processing this neighbor after the higher-priority work is completed.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span data-ttu-id="4bf44-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ Ignora \_ le \_ notifiche di modifica** (67108864 (0x4000000))</span><span class="sxs-lookup"><span data-stu-id="4bf44-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** (67108864 (0x4000000))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-230">Questa adiacente è impostata per disabilitare le sincronizzazioni basate sulla notifica.</span><span class="sxs-lookup"><span data-stu-id="4bf44-230">This neighbor is set to disable notification-based synchronizations.</span></span> <span data-ttu-id="4bf44-231">All'interno di un sito, la sincronizzazione tra ciascun controller di dominio avviene in base alle notifiche inviate in caso di modifica.</span><span class="sxs-lookup"><span data-stu-id="4bf44-231">Within a site, domain controllers synchronize with each other based on notifications when changes occur.</span></span> <span data-ttu-id="4bf44-232">Questa impostazione impedisce al router adiacente di eseguire sincronizzazioni attivate da notifiche.</span><span class="sxs-lookup"><span data-stu-id="4bf44-232">This setting prevents this neighbor from performing synchronizations that are triggered by notifications.</span></span> <span data-ttu-id="4bf44-233">Il router adiacente eseguirà comunque le sincronizzazioni in base alla pianificazione o in risposta alle sincronizzazioni richieste manualmente.</span><span class="sxs-lookup"><span data-stu-id="4bf44-233">The neighbor will still do synchronizations based on its schedule, or in response to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span data-ttu-id="4bf44-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ Disable \_ scheduled \_ Sync** (134217728 (0x8000000))</span><span class="sxs-lookup"><span data-stu-id="4bf44-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** (134217728 (0x8000000))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-235">Questo elemento adiacente è impostato in modo da non eseguire sincronizzazioni in base alla pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4bf44-235">This neighbor is set to not perform synchronizations based on its schedule.</span></span> <span data-ttu-id="4bf44-236">L'unico modo in cui il prossimo eseguirà le sincronizzazioni è in risposta alle notifiche di modifica o alle sincronizzazioni richieste manualmente.</span><span class="sxs-lookup"><span data-stu-id="4bf44-236">The only way this neighbor will perform synchronizations is in response to change notifications or to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span data-ttu-id="4bf44-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>Servizi di **dominio Active Directory \_ \_ \_ \_ Modifiche REPL NBR Compress** (268435456 (0x10000000))</span><span class="sxs-lookup"><span data-stu-id="4bf44-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS\_REPL\_NBR\_COMPRESS\_CHANGES** (268435456 (0x10000000))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-238">Le modifiche ricevute da questa origine devono essere compresse.</span><span class="sxs-lookup"><span data-stu-id="4bf44-238">Changes received from this source are to be compressed.</span></span> <span data-ttu-id="4bf44-239">La compressione viene in genere eseguita solo se il server di origine si trova in un sito diverso.</span><span class="sxs-lookup"><span data-stu-id="4bf44-239">Compression usually occurs only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span data-ttu-id="4bf44-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>Servizi di **dominio Active Directory \_ REPL \_ NBR \_ senza \_ \_ notifiche di modifica** (536870912 (0x20000000))</span><span class="sxs-lookup"><span data-stu-id="4bf44-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** (536870912 (0x20000000))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-241">Nessuna notifica delle modifiche deve essere ricevuta da questa origine.</span><span class="sxs-lookup"><span data-stu-id="4bf44-241">No change notifications should be received from this source.</span></span> <span data-ttu-id="4bf44-242">Viene in genere impostato solo se il server di origine si trova in un sito diverso.</span><span class="sxs-lookup"><span data-stu-id="4bf44-242">Usually set only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span data-ttu-id="4bf44-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>Servizi di **dominio Active Directory \_ \_Set di \_ \_ attributi \_ parziali REPL NBR** (1073741824 (0x40000000))</span><span class="sxs-lookup"><span data-stu-id="4bf44-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS\_REPL\_NBR\_PARTIAL\_ATTRIBUTE\_SET** (1073741824 (0x40000000))</span></span>


</dt> <dd>

<span data-ttu-id="4bf44-244">È in corso la ricompilazione da parte dell'elemento adiacente del contenuto di questa replica, in seguito a una modifica nell'insieme di attributi parziali.</span><span class="sxs-lookup"><span data-stu-id="4bf44-244">This neighbor is in a state where it is rebuilding the contents of this replica because of a change in the partial attribute set.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4bf44-245">**SourceDsaAddress**</span><span class="sxs-lookup"><span data-stu-id="4bf44-245">**SourceDsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-246">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4bf44-246">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-248">Ottiene l'indirizzo DNS del controller di dominio di origine.</span><span class="sxs-lookup"><span data-stu-id="4bf44-248">Gets the DNS address of the source DC.</span></span>

> [!Note]  
> <span data-ttu-id="4bf44-249">Questa stringa contiene un GUID modificato, non il nome DNS canonico comunemente usato.</span><span class="sxs-lookup"><span data-stu-id="4bf44-249">This string contains a modified GUID, not the commonly used canonical DNS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="4bf44-250">**SourceDsaCN**</span><span class="sxs-lookup"><span data-stu-id="4bf44-250">**SourceDsaCN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4bf44-251">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-253">Ottiene il componente del percorso dell'oggetto per il DSA che rappresenta il controller di dominio di origine.</span><span class="sxs-lookup"><span data-stu-id="4bf44-253">Gets the object path component for the DSA that represents the source DC.</span></span> <span data-ttu-id="4bf44-254">Questa stringa è spesso simile al nome del computer, ma non è sempre identica.</span><span class="sxs-lookup"><span data-stu-id="4bf44-254">This string is often similar to the computer name but is not always identical.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-255">**SourceDsaDN**</span><span class="sxs-lookup"><span data-stu-id="4bf44-255">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-256">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4bf44-256">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-258">Ottiene il percorso X. 500 per il DSA che rappresenta il controller di dominio di origine.</span><span class="sxs-lookup"><span data-stu-id="4bf44-258">Gets the X.500 path for the DSA that represents the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-259">**SourceDsaInvocationID**</span><span class="sxs-lookup"><span data-stu-id="4bf44-259">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-260">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4bf44-260">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-262">Ottiene l'ID di chiamata utilizzato dal server di origine nell'ultima replica.</span><span class="sxs-lookup"><span data-stu-id="4bf44-262">Gets the invocation ID that was used by the source server as of the last replication.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-263">**SourceDsaObjGuid**</span><span class="sxs-lookup"><span data-stu-id="4bf44-263">**SourceDsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4bf44-264">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-266">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4bf44-266">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-267">Ottiene il GUID per l'agente del servizio directory (DSA) che rappresenta il controller di dominio di origine (DC).</span><span class="sxs-lookup"><span data-stu-id="4bf44-267">Gets the GUID for the directory service agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-268">**SourceDsaSite**</span><span class="sxs-lookup"><span data-stu-id="4bf44-268">**SourceDsaSite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-269">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4bf44-269">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-271">Ottiene il sito che contiene il controller di dominio di origine.</span><span class="sxs-lookup"><span data-stu-id="4bf44-271">Gets the site that contains the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-272">**SyncOnStartup**</span><span class="sxs-lookup"><span data-stu-id="4bf44-272">**SyncOnStartup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-273">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-275">Ottiene il valore che indica se il flag **DS \_ REPL \_ NBR \_ Sync \_ on \_ Startup** è stato impostato nella proprietà **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-275">Gets the value that indicates whether the **DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-276">**TimeOfLastSyncAttempt**</span><span class="sxs-lookup"><span data-stu-id="4bf44-276">**TimeOfLastSyncAttempt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-277">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4bf44-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-279">Ottiene il timestamp per l'ultimo tentativo di replica.</span><span class="sxs-lookup"><span data-stu-id="4bf44-279">Gets the timestamp for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-280">**TimeOfLastSyncSuccess**</span><span class="sxs-lookup"><span data-stu-id="4bf44-280">**TimeOfLastSyncSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-281">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4bf44-281">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-283">Ottiene il timestamp per l'ultimo tentativo di replica riuscito.</span><span class="sxs-lookup"><span data-stu-id="4bf44-283">Gets the timestamp for the last successful replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-284">**TwoWaySync**</span><span class="sxs-lookup"><span data-stu-id="4bf44-284">**TwoWaySync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-285">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-287">Ottiene il valore che indica se il flag di **\_ \_ \_ \_ \_ sincronizzazione bidirezionale DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-287">Gets the value that indicates whether the **DS\_REPL\_NBR\_TWO\_WAY\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-288">**UseAsyncIntersiteTransport**</span><span class="sxs-lookup"><span data-stu-id="4bf44-288">**UseAsyncIntersiteTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-289">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-291">Ottiene il valore che indica se il flag di **\_ \_ \_ \_ \_ \_ trasporto tra siti DS REPL NBR** è stato impostato nella proprietà **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-291">Gets the value that indicates whether the **DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-292">**USNAttributeFilter**</span><span class="sxs-lookup"><span data-stu-id="4bf44-292">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-293">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4bf44-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-295">Ottiene il valore della proprietà **USNLastObjChangeSynced** alla fine dell'ultimo ciclo di replica completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="4bf44-295">Gets the **USNLastObjChangeSynced** property value at the end of the last successful completed replication cycle.</span></span> <span data-ttu-id="4bf44-296">Zero se i cicli di replica non sono stati completati correttamente.</span><span class="sxs-lookup"><span data-stu-id="4bf44-296">Zero if there were no successfully completed replication cycles.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-297">**USNLastObjChangeSynced**</span><span class="sxs-lookup"><span data-stu-id="4bf44-297">**USNLastObjChangeSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-298">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4bf44-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-300">Ottiene il valore dell'attributo non [**modificato**](/windows/desktop/ADSchema/a-usnchanged) dell'ultimo aggiornamento dell'oggetto ricevuto.</span><span class="sxs-lookup"><span data-stu-id="4bf44-300">Gets the [**unchanged**](/windows/desktop/ADSchema/a-usnchanged) attribute value of the last object update that was received.</span></span>

</dd> <dt>

<span data-ttu-id="4bf44-301">**Scrivibile**</span><span class="sxs-lookup"><span data-stu-id="4bf44-301">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bf44-302">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bf44-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bf44-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bf44-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bf44-304">Ottiene il valore che indica se il **flag \_ scrivibile di DS REPL \_ NBR \_** è stato impostato nella proprietà **ReplicaFlags** .</span><span class="sxs-lookup"><span data-stu-id="4bf44-304">Gets the value that indicates whether the **DS\_REPL\_NBR\_WRITEABLE** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4bf44-305">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bf44-305">Requirements</span></span>



| <span data-ttu-id="4bf44-306">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bf44-306">Requirement</span></span> | <span data-ttu-id="4bf44-307">Valore</span><span class="sxs-lookup"><span data-stu-id="4bf44-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf44-308">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bf44-308">Minimum supported client</span></span><br/> | <span data-ttu-id="4bf44-309">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4bf44-309">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4bf44-310">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bf44-310">Minimum supported server</span></span><br/> | <span data-ttu-id="4bf44-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bf44-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4bf44-312">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4bf44-312">Namespace</span></span><br/>                | <span data-ttu-id="4bf44-313">\\MicrosoftActiveDirectory radice</span><span class="sxs-lookup"><span data-stu-id="4bf44-313">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="4bf44-314">MOF</span><span class="sxs-lookup"><span data-stu-id="4bf44-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bf44-315"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bf44-315"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bf44-316">DLL</span><span class="sxs-lookup"><span data-stu-id="4bf44-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bf44-317"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bf44-317"><dt>Replprov.dll</dt></span></span> </dl> |



 

