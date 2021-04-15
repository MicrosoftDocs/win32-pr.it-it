---
title: Classe MSAD_ReplPendingOp
description: Rappresenta la \_ struttura op REPL di DS \_ , che descrive un'attività di replica attualmente in esecuzione o in attesa di esecuzione.
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- Classe MSAD_ReplPendingOp Active Directory
- Classe MSAD_ReplPendingOp Active Directory, descritta
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f1c3faddac915f602104d7e5dc4e9b6bc7d6944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400635"
---
# <a name="msad_replpendingop-class"></a><span data-ttu-id="00fd5-105">\_Classe MSAD ReplPendingOp</span><span class="sxs-lookup"><span data-stu-id="00fd5-105">MSAD\_ReplPendingOp class</span></span>

<span data-ttu-id="00fd5-106">Rappresenta la [**struttura \_ \_ op REPL di DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) , che descrive un'attività di replica attualmente in esecuzione o in attesa di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="00fd5-106">Represents the [**DS\_REPL\_OP**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) structure, which describes a replication task that is currently executing or pending execution.</span></span> <span data-ttu-id="00fd5-107">Questa struttura viene restituita dalla funzione [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .</span><span class="sxs-lookup"><span data-stu-id="00fd5-107">This structure is returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="00fd5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00fd5-108">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a><span data-ttu-id="00fd5-109">Members</span><span class="sxs-lookup"><span data-stu-id="00fd5-109">Members</span></span>

<span data-ttu-id="00fd5-110">La **classe \_ ReplPendingOp di MSAD** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="00fd5-110">The **MSAD\_ReplPendingOp** class has these types of members:</span></span>

-   [<span data-ttu-id="00fd5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="00fd5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00fd5-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="00fd5-112">Properties</span></span>

<span data-ttu-id="00fd5-113">La **classe \_ ReplPendingOp di MSAD** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="00fd5-113">The **MSAD\_ReplPendingOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00fd5-114">**DsaAddress**</span><span class="sxs-lookup"><span data-stu-id="00fd5-114">**DsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00fd5-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="00fd5-115">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00fd5-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00fd5-117">Ottiene l'indirizzo di rete specifico del trasporto del server remoto associato a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="00fd5-117">Gets the transport-specific network address of the remote server that is associated with this operation.</span></span> <span data-ttu-id="00fd5-118">**Null** se non è presente alcun server remoto associato a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="00fd5-118">**NULL** if there is no remote server that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="00fd5-119">**DsaDN**</span><span class="sxs-lookup"><span data-stu-id="00fd5-119">**DsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00fd5-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="00fd5-120">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00fd5-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00fd5-122">Ottiene il percorso X. 500 del DSA associato al server remoto che corrisponde a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="00fd5-122">Gets the X.500 path of the DSA that is associated with the remote server that corresponds to this operation.</span></span> <span data-ttu-id="00fd5-123">**Null** se nessun server remoto corrisponde a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="00fd5-123">**NULL** if no remote server corresponds to this operation.</span></span>

</dd> <dt>

<span data-ttu-id="00fd5-124">**DsaObjGuid**</span><span class="sxs-lookup"><span data-stu-id="00fd5-124">**DsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00fd5-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="00fd5-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00fd5-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00fd5-127">Ottiene il valore dell'attributo [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) dell'oggetto DSA identificato dalla proprietà **DsaDN** .</span><span class="sxs-lookup"><span data-stu-id="00fd5-127">Gets the value of the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the DSA that is identified by the **DsaDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="00fd5-128">**NamingContextDN**</span><span class="sxs-lookup"><span data-stu-id="00fd5-128">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00fd5-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="00fd5-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00fd5-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00fd5-131">Ottiene il percorso X. 500 del contesto dei nomi (NC) associato a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="00fd5-131">Gets the X.500 path of the naming context (NC) that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="00fd5-132">**NamingContextObjGuid**</span><span class="sxs-lookup"><span data-stu-id="00fd5-132">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00fd5-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="00fd5-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00fd5-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00fd5-135">Ottiene l'attributo [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) del NC identificato dalla proprietà **NamingContextDN** .</span><span class="sxs-lookup"><span data-stu-id="00fd5-135">Gets the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the NC that is identified by the **NamingContextDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="00fd5-136">**OpStartTime**</span><span class="sxs-lookup"><span data-stu-id="00fd5-136">**OpStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00fd5-137">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="00fd5-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00fd5-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00fd5-139">Ottiene l'ora in cui è stata avviata l'operazione.</span><span class="sxs-lookup"><span data-stu-id="00fd5-139">Gets the time when the operation was started.</span></span> <span data-ttu-id="00fd5-140">**Null** se l'operazione è ancora in coda.</span><span class="sxs-lookup"><span data-stu-id="00fd5-140">**NULL** if this operation is still in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="00fd5-141">**Opzioni**</span><span class="sxs-lookup"><span data-stu-id="00fd5-141">**Options**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00fd5-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00fd5-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00fd5-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00fd5-144">Ottiene il set di flag che fornisce dati aggiuntivi sull'operazione.</span><span class="sxs-lookup"><span data-stu-id="00fd5-144">Gets the set of flags that provides additional data about the operation.</span></span> <span data-ttu-id="00fd5-145">Il contenuto di questo membro è determinato dal valore della proprietà **optype** .</span><span class="sxs-lookup"><span data-stu-id="00fd5-145">The contents of this member are determined by the value of the **OpType** property.</span></span>

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span data-ttu-id="00fd5-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**\_sincronizzazione del \_ \_ tipo op REPL DS \_**</span><span class="sxs-lookup"><span data-stu-id="00fd5-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS\_REPL\_OP\_TYPE\_SYNC**</span></span>


</dt> <dd>

<span data-ttu-id="00fd5-147">Contiene zero o una combinazione di uno o più valori di \**DS \_ REPSYNC \_ \** _ come definito per il parametro _Options \* in [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).</span><span class="sxs-lookup"><span data-stu-id="00fd5-147">Contains zero or a combination of one or more of the **DS\_REPSYNC\_\** _ values as defined for the _Options* parameter in [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span data-ttu-id="00fd5-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**\_aggiunta del \_ \_ tipo op REPL DS \_**</span><span class="sxs-lookup"><span data-stu-id="00fd5-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS\_REPL\_OP\_TYPE\_ADD**</span></span>


</dt> <dd>

<span data-ttu-id="00fd5-149">Contiene zero o una combinazione di uno o più valori di \**DS \_ REPADD \_ \** _ come definito per il parametro _Options \* in [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).</span><span class="sxs-lookup"><span data-stu-id="00fd5-149">Contains zero or a combination of one or more of the **DS\_REPADD\_\** _ values as defined for the _Options* parameter in [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span data-ttu-id="00fd5-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**\_eliminazione del \_ \_ tipo op REPL DS \_**</span><span class="sxs-lookup"><span data-stu-id="00fd5-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS\_REPL\_OP\_TYPE\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="00fd5-151">Contiene zero o una combinazione di uno o più valori di \**DS \_ REPDEL \_ \** _ come definito per il parametro _Options \* in [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).</span><span class="sxs-lookup"><span data-stu-id="00fd5-151">Contains zero or a combination of one or more of the **DS\_REPDEL\_\** _ values as defined for the _Options* parameter in [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span data-ttu-id="00fd5-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**\_ \_ \_ modifica tipo op REPL \_ di DS**</span><span class="sxs-lookup"><span data-stu-id="00fd5-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS\_REPL\_OP\_TYPE\_MODIFY**</span></span>


</dt> <dd>

<span data-ttu-id="00fd5-153">Contiene zero o una combinazione di uno o più valori di \**DS \_ REPMOD \_ \** _ come definito per il parametro _Options \* in [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).</span><span class="sxs-lookup"><span data-stu-id="00fd5-153">Contains zero or a combination of one or more of the **DS\_REPMOD\_\** _ values as defined for the _Options* parameter in [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span data-ttu-id="00fd5-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**\_ \_ \_ refs aggiornamento del tipo \_ op \_ di DS repl**</span><span class="sxs-lookup"><span data-stu-id="00fd5-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS\_REPL\_OP\_TYPE\_UPDATE\_REFS**</span></span>


</dt> <dd>

<span data-ttu-id="00fd5-155">Contiene zero o una combinazione di uno o più valori di \**DS \_ REPSUPD \_ \** _ come definito per il parametro _Options \* in [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).</span><span class="sxs-lookup"><span data-stu-id="00fd5-155">Contains zero or a combination of one or more of the **DS\_REPSUPD\_\** _ values as defined for the _Options* parameter in [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="00fd5-156">**OpType**</span><span class="sxs-lookup"><span data-stu-id="00fd5-156">**OpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00fd5-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00fd5-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00fd5-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00fd5-159">Ottiene il valore del [**\_ \_ \_ tipo op REPL di DS**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) che indica il tipo di operazione rappresentata da questa classe.</span><span class="sxs-lookup"><span data-stu-id="00fd5-159">Gets the [**DS\_REPL\_OP\_TYPE**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) value that indicates the type of operation that this class represents.</span></span>

</dd> <dt>

<span data-ttu-id="00fd5-160">**PositionInQ**</span><span class="sxs-lookup"><span data-stu-id="00fd5-160">**PositionInQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00fd5-161">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00fd5-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00fd5-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00fd5-163">Ottiene la posizione di questa operazione nella coda.</span><span class="sxs-lookup"><span data-stu-id="00fd5-163">Gets the position of this operation in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="00fd5-164">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="00fd5-164">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00fd5-165">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00fd5-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00fd5-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00fd5-167">Ottiene la priorità di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="00fd5-167">Gets the priority of this operation.</span></span> <span data-ttu-id="00fd5-168">Le attività con priorità più alta vengono eseguite per prime.</span><span class="sxs-lookup"><span data-stu-id="00fd5-168">Higher-priority tasks are executed first.</span></span> <span data-ttu-id="00fd5-169">La priorità viene calcolata dal server in base al tipo di operazione rappresentata da questa classe e ai parametri dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="00fd5-169">The priority is calculated by the server based on the type of operation that this class represents and the parameters of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="00fd5-170">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="00fd5-170">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00fd5-171">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00fd5-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00fd5-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-173">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="00fd5-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="00fd5-174">Ottiene l'ID dell'operazione, che è univoco per computer e per avvio.</span><span class="sxs-lookup"><span data-stu-id="00fd5-174">Gets the ID of the operation, which is unique per-machine and per-boot.</span></span>

</dd> <dt>

<span data-ttu-id="00fd5-175">**TimeEnqueued**</span><span class="sxs-lookup"><span data-stu-id="00fd5-175">**TimeEnqueued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00fd5-176">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="00fd5-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="00fd5-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="00fd5-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00fd5-178">Ottiene l'ora in cui l'operazione è stata aggiunta alla coda.</span><span class="sxs-lookup"><span data-stu-id="00fd5-178">Gets the time at which this operation was added to the queue.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00fd5-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00fd5-179">Requirements</span></span>



| <span data-ttu-id="00fd5-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="00fd5-180">Requirement</span></span> | <span data-ttu-id="00fd5-181">Valore</span><span class="sxs-lookup"><span data-stu-id="00fd5-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00fd5-182">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00fd5-182">Minimum supported client</span></span><br/> | <span data-ttu-id="00fd5-183">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="00fd5-183">None supported</span></span><br/>                                                               |
| <span data-ttu-id="00fd5-184">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00fd5-184">Minimum supported server</span></span><br/> | <span data-ttu-id="00fd5-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00fd5-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="00fd5-186">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="00fd5-186">Namespace</span></span><br/>                | <span data-ttu-id="00fd5-187">\\MicrosoftActiveDirectory radice</span><span class="sxs-lookup"><span data-stu-id="00fd5-187">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="00fd5-188">MOF</span><span class="sxs-lookup"><span data-stu-id="00fd5-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00fd5-189"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00fd5-189"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="00fd5-190">DLL</span><span class="sxs-lookup"><span data-stu-id="00fd5-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00fd5-191"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00fd5-191"><dt>Replprov.dll</dt></span></span> </dl> |



 

