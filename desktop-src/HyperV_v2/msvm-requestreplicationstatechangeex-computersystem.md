---
description: Richiede che lo stato di replica della relazione di replica della macchina virtuale venga modificato nel valore specificato.
ms.assetid: 8EC78CCC-2997-4239-A20C-BA56F848ECB6
title: 'Metodo Msvm_ComputerSystem:: RequestReplicationStateChangeEx'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChangeEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d77db9dff90f985991c8e9013ea4f239cb6479f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313850"
---
# <a name="msvm_computersystemrequestreplicationstatechangeex-method"></a><span data-ttu-id="2d0df-103">\_Metodo MSVM ComputerSystem:: RequestReplicationStateChangeEx</span><span class="sxs-lookup"><span data-stu-id="2d0df-103">Msvm\_ComputerSystem::RequestReplicationStateChangeEx method</span></span>

<span data-ttu-id="2d0df-104">Richiede che lo stato di replica della relazione di replica della macchina virtuale venga modificato nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="2d0df-104">Requests that the replication state of the replication relationship of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="2d0df-105">Mentre è in corso la modifica dello stato, la proprietà **ReplicationState** viene modificata nel valore del parametro *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="2d0df-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="2d0df-106">Questo metodo è supportato solo per le istanze della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresentano una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2d0df-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d0df-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d0df-107">Syntax</span></span>


```C++
uint32 RequestReplicationStateChangeEx(
  [in]  string              ReplicationRelationship,
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="2d0df-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d0df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d0df-109">*ReplicationRelationship* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d0df-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d0df-110">Rappresentazione in forma di stringa di un'istanza incorporata della classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) che definisce la relazione di replica per la richiesta di modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="2d0df-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for state change request.</span></span> <span data-ttu-id="2d0df-111">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2d0df-111">This parameter is optional.</span></span> <span data-ttu-id="2d0df-112">Quando non è specificato, la richiesta viene eseguita sulla relazione di replica primaria.</span><span class="sxs-lookup"><span data-stu-id="2d0df-112">When it's unspecified, the request runs on the primary replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="2d0df-113">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d0df-113">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d0df-114">Nuovo stato di replica.</span><span class="sxs-lookup"><span data-stu-id="2d0df-114">The new replication state.</span></span> <span data-ttu-id="2d0df-115">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2d0df-115">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="2d0df-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Pronto per l'avvio della replica iniziale** (1)</span><span class="sxs-lookup"><span data-stu-id="2d0df-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2d0df-117">Pronto per avviare la replica iniziale.</span><span class="sxs-lookup"><span data-stu-id="2d0df-117">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="2d0df-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**In attesa del completamento della replica iniziale** (2)</span><span class="sxs-lookup"><span data-stu-id="2d0df-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2d0df-119">In attesa del completamento della replica iniziale.</span><span class="sxs-lookup"><span data-stu-id="2d0df-119">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="2d0df-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replica** in corso (3)</span><span class="sxs-lookup"><span data-stu-id="2d0df-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2d0df-121">replica in corso.</span><span class="sxs-lookup"><span data-stu-id="2d0df-121">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="2d0df-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replica sincronizzata completata** (4)</span><span class="sxs-lookup"><span data-stu-id="2d0df-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2d0df-123">Replica sincronizzata completata.</span><span class="sxs-lookup"><span data-stu-id="2d0df-123">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="2d0df-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (7)</span><span class="sxs-lookup"><span data-stu-id="2d0df-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2d0df-125">Sospendere la replica.</span><span class="sxs-lookup"><span data-stu-id="2d0df-125">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="2d0df-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Annulla risincronizzazione** (9)</span><span class="sxs-lookup"><span data-stu-id="2d0df-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="2d0df-127">Annulla la risincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2d0df-127">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2d0df-128">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="2d0df-128">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d0df-129">Riferimento facoltativo a un oggetto [**MSVM \_ ConcreteJob**](msvm-concretejob.md) restituito se l'operazione viene eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="2d0df-129">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="2d0df-130">Se presente, il riferimento restituito può essere usato per monitorare lo stato di avanzamento e ottenere il risultato del metodo.</span><span class="sxs-lookup"><span data-stu-id="2d0df-130">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="2d0df-131">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d0df-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d0df-132">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="2d0df-132">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d0df-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d0df-133">Return value</span></span>

<span data-ttu-id="2d0df-134">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2d0df-134">This method returns one of the following values.</span></span>



| <span data-ttu-id="2d0df-135">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d0df-135">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="2d0df-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d0df-136">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d0df-137"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-137"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="2d0df-138">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="2d0df-138">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="2d0df-139"><dt>**Parametri del metodo controllati-processo avviato**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-139"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="2d0df-140">La transizione è asincrona.</span><span class="sxs-lookup"><span data-stu-id="2d0df-140">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="2d0df-141"><dt>**Errore**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-141"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="2d0df-142"><dt>**Accesso negato**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-142"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="2d0df-143"><dt>**Non supportato**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-143"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="2d0df-144"><dt>**Stato sconosciuto**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-144"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="2d0df-145"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-145"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="2d0df-146"><dt>**Parametro non valido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-146"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="2d0df-147">Il valore specificato in uno dei parametri non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2d0df-147">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="2d0df-148">Il <dt>**sistema è in uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-148"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="2d0df-149"><dt>**Stato non valido per l'operazione**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-149"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="2d0df-150">Il valore specificato nel parametro *RequestedState* non è supportato nella modalità o nello stato di replica corrente.</span><span class="sxs-lookup"><span data-stu-id="2d0df-150">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="2d0df-151"><dt>**Tipo di dati non corretto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-151"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="2d0df-152">Il <dt>**sistema non è disponibile**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-152"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="2d0df-153"><dt>**Memoria insufficiente**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-153"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="2d0df-154"><dt>**File non trovato**</dt> <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-154"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="2d0df-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d0df-155">Requirements</span></span>



| <span data-ttu-id="2d0df-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d0df-156">Requirement</span></span> | <span data-ttu-id="2d0df-157">Valore</span><span class="sxs-lookup"><span data-stu-id="2d0df-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d0df-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d0df-158">Minimum supported client</span></span><br/> | <span data-ttu-id="2d0df-159">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d0df-159">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2d0df-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d0df-160">Minimum supported server</span></span><br/> | <span data-ttu-id="2d0df-161">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="2d0df-161">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d0df-162">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2d0df-162">Namespace</span></span><br/>                | <span data-ttu-id="2d0df-163">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2d0df-163">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="2d0df-164">MOF</span><span class="sxs-lookup"><span data-stu-id="2d0df-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d0df-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d0df-166">DLL</span><span class="sxs-lookup"><span data-stu-id="2d0df-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d0df-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d0df-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d0df-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d0df-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d0df-169">**\_ComputerSystem MSVM**</span><span class="sxs-lookup"><span data-stu-id="2d0df-169">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




