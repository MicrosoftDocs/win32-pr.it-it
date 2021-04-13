---
description: Richiede che lo stato di replica della macchina virtuale venga modificato in base al valore specificato e agisca sulla relazione di replica primaria della macchina virtuale.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Metodo RequestReplicationStateChange della classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 32f0136662f043627a5fad152ee0e0aaa1845e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528531"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="6e004-103">Metodo RequestReplicationStateChange della classe MSVM \_ ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="6e004-103">RequestReplicationStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="6e004-104">Richiede che lo stato di replica della macchina virtuale venga modificato in base al valore specificato e agisca sulla relazione di replica primaria della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e004-104">Requests that the replication state of the virtual machine be changed to the specified value and acts on the primary replication relationship of the virtual machine.</span></span> <span data-ttu-id="6e004-105">Mentre è in corso la modifica dello stato, la proprietà **ReplicationState** viene modificata nel valore del parametro *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="6e004-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="6e004-106">Questo metodo è supportato solo per le istanze della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresentano una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e004-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="6e004-107">A partire da Windows 8.1, è consigliabile non usare più **RequestReplicationStateChange** per richiedere la modifica dello stato di replica.</span><span class="sxs-lookup"><span data-stu-id="6e004-107">Starting with Windows 8.1, we recommend not to use **RequestReplicationStateChange** anymore to request changing of replication state.</span></span> <span data-ttu-id="6e004-108">Usare invece [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="6e004-108">Instead, use [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6e004-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e004-109">Syntax</span></span>


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="6e004-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e004-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e004-111">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e004-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e004-112">Nuovo stato di replica.</span><span class="sxs-lookup"><span data-stu-id="6e004-112">The new replication state.</span></span> <span data-ttu-id="6e004-113">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e004-113">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="6e004-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Pronto per l'avvio della replica iniziale** (1)</span><span class="sxs-lookup"><span data-stu-id="6e004-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6e004-115">Pronto per avviare la replica iniziale.</span><span class="sxs-lookup"><span data-stu-id="6e004-115">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="6e004-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**In attesa del completamento della replica iniziale** (2)</span><span class="sxs-lookup"><span data-stu-id="6e004-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6e004-117">In attesa del completamento della replica iniziale.</span><span class="sxs-lookup"><span data-stu-id="6e004-117">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="6e004-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replica** in corso (3)</span><span class="sxs-lookup"><span data-stu-id="6e004-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6e004-119">replica in corso.</span><span class="sxs-lookup"><span data-stu-id="6e004-119">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="6e004-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replica sincronizzata completata** (4)</span><span class="sxs-lookup"><span data-stu-id="6e004-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6e004-121">Replica sincronizzata completata.</span><span class="sxs-lookup"><span data-stu-id="6e004-121">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="6e004-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (7)</span><span class="sxs-lookup"><span data-stu-id="6e004-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6e004-123">Sospendere la replica.</span><span class="sxs-lookup"><span data-stu-id="6e004-123">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="6e004-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Annulla risincronizzazione** (9)</span><span class="sxs-lookup"><span data-stu-id="6e004-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="6e004-125">Annulla la risincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="6e004-125">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6e004-126">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="6e004-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e004-127">Riferimento facoltativo a un oggetto [**MSVM \_ ConcreteJob**](msvm-concretejob.md) restituito se l'operazione viene eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="6e004-127">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="6e004-128">Se presente, il riferimento restituito può essere usato per monitorare lo stato di avanzamento e ottenere il risultato del metodo.</span><span class="sxs-lookup"><span data-stu-id="6e004-128">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="6e004-129">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e004-129">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e004-130">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="6e004-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e004-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e004-131">Return value</span></span>

<span data-ttu-id="6e004-132">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e004-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="6e004-133">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e004-133">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="6e004-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e004-134">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e004-135"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="6e004-136">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="6e004-136">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="6e004-137"><dt>**Parametri del metodo controllati-processo avviato**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-137"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="6e004-138">La transizione è asincrona.</span><span class="sxs-lookup"><span data-stu-id="6e004-138">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="6e004-139"><dt>**Errore**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-139"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="6e004-140"><dt>**Accesso negato**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-140"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="6e004-141"><dt>**Non supportato**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-141"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="6e004-142"><dt>**Stato sconosciuto**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-142"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="6e004-143"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-143"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="6e004-144"><dt>**Parametro non valido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-144"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="6e004-145">Il valore specificato in uno dei parametri non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6e004-145">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="6e004-146">Il <dt>**sistema è in uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-146"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="6e004-147"><dt>**Stato non valido per l'operazione**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-147"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="6e004-148">Il valore specificato nel parametro *RequestedState* non è supportato nella modalità o nello stato di replica corrente.</span><span class="sxs-lookup"><span data-stu-id="6e004-148">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="6e004-149"><dt>**Tipo di dati non corretto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-149"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="6e004-150">Il <dt>**sistema non è disponibile**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-150"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="6e004-151"><dt>**Memoria insufficiente**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-151"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="6e004-152"><dt>**File non trovato**</dt> <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-152"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="6e004-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e004-153">Requirements</span></span>



| <span data-ttu-id="6e004-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e004-154">Requirement</span></span> | <span data-ttu-id="6e004-155">Valore</span><span class="sxs-lookup"><span data-stu-id="6e004-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e004-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e004-156">Minimum supported client</span></span><br/> | <span data-ttu-id="6e004-157">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6e004-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6e004-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e004-158">Minimum supported server</span></span><br/> | <span data-ttu-id="6e004-159">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6e004-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e004-160">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6e004-160">Namespace</span></span><br/>                | <span data-ttu-id="6e004-161">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6e004-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6e004-162">MOF</span><span class="sxs-lookup"><span data-stu-id="6e004-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e004-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e004-164">DLL</span><span class="sxs-lookup"><span data-stu-id="6e004-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e004-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e004-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6e004-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e004-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e004-167">**\_ComputerSystem MSVM**</span><span class="sxs-lookup"><span data-stu-id="6e004-167">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




