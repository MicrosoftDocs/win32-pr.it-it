---
description: Avvia la replica di una macchina virtuale.
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Metodo StartReplication della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4702b5b73a989e2889bf1da9e4d284afdfe5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343161"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="08d88-103">Metodo StartReplication della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="08d88-103">StartReplication method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="08d88-104">Avvia la replica di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="08d88-104">Starts the replication of a virtual machine.</span></span> <span data-ttu-id="08d88-105">Quando un client chiama questo metodo per una macchina virtuale di replica, avvia la replica con la replica estesa.</span><span class="sxs-lookup"><span data-stu-id="08d88-105">When a client calls this method for a replica virtual machine, it starts the replication with extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d88-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08d88-106">Syntax</span></span>


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="08d88-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="08d88-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08d88-108">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08d88-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08d88-109">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui deve essere avviata la replica.</span><span class="sxs-lookup"><span data-stu-id="08d88-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be started.</span></span>

</dd> <dt>

<span data-ttu-id="08d88-110">*InitialReplicationType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08d88-110">*InitialReplicationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08d88-111">Tipo di trasferimento da utilizzare per l'esecuzione della replica iniziale.</span><span class="sxs-lookup"><span data-stu-id="08d88-111">The type of transfer to be used for performing the initial replication.</span></span>

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span data-ttu-id="08d88-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Trasferimento di rete** (1)</span><span class="sxs-lookup"><span data-stu-id="08d88-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Network Transfer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="08d88-113">Trasferimento tramite rete.</span><span class="sxs-lookup"><span data-stu-id="08d88-113">Network transfer.</span></span>

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span data-ttu-id="08d88-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Esporta** (2)</span><span class="sxs-lookup"><span data-stu-id="08d88-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Export** (2)</span></span>


</dt> <dd>

<span data-ttu-id="08d88-115">Esportazione.</span><span class="sxs-lookup"><span data-stu-id="08d88-115">Export.</span></span>

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span data-ttu-id="08d88-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Trasferimento di rete con seeding** (3)</span><span class="sxs-lookup"><span data-stu-id="08d88-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Seeded Network Transfer** (3)</span></span>


</dt> <dd>

<span data-ttu-id="08d88-117">Trasferimento di rete con seeding.</span><span class="sxs-lookup"><span data-stu-id="08d88-117">Seeded network transfer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="08d88-118">*InitialReplicationExportLocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08d88-118">*InitialReplicationExportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08d88-119">Se *InitialReplicationType* è 2 (Export), questo parametro contiene il percorso completo della directory in cui deve essere esportata la replica iniziale.</span><span class="sxs-lookup"><span data-stu-id="08d88-119">If *InitialReplicationType* is 2 (Export), this parameter contains the fully qualified path of the directory to which the initial replication is to be exported.</span></span> <span data-ttu-id="08d88-120">Questo parametro non viene utilizzato per altri valori di *InitialReplicationType* e può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="08d88-120">This parameter is not used for other values of *InitialReplicationType*, and can be **Null**.</span></span> <span data-ttu-id="08d88-121">Questa directory può essere riutilizzata per l'esportazione di più repliche di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="08d88-121">This directory can be reused for exporting multiple virtual machine replication.</span></span> <span data-ttu-id="08d88-122">Questo metodo inserisce ogni replica della macchina virtuale in una sottodirectory separata in questo percorso.</span><span class="sxs-lookup"><span data-stu-id="08d88-122">This method places each virtual machine replication in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="08d88-123">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08d88-123">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08d88-124">Ora di inizio pianificata per la replica iniziale sulla connessione di rete al server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="08d88-124">The scheduled start time for the initial replication over the network connection to recovery server.</span></span> <span data-ttu-id="08d88-125">Questo parametro viene ignorato quando *InitialReplicationType* è 2 (Export).</span><span class="sxs-lookup"><span data-stu-id="08d88-125">This parameter is ignored when *InitialReplicationType* is 2 (Export).</span></span> <span data-ttu-id="08d88-126">Se questo parametro è **null**, la replica iniziale viene avviata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="08d88-126">If this parameter is **Null**, the initial replication starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="08d88-127">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="08d88-127">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08d88-128">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08d88-128">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08d88-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08d88-129">Return value</span></span>

<span data-ttu-id="08d88-130">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="08d88-130">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="08d88-131">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="08d88-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-132">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="08d88-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-133">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="08d88-133">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-134">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="08d88-134">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-135">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="08d88-135">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-136">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="08d88-136">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-137">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="08d88-137">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-138">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="08d88-138">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-139">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="08d88-139">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-140">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="08d88-140">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-141">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="08d88-141">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-142">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="08d88-142">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-143">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="08d88-143">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="08d88-144">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="08d88-144">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="08d88-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08d88-145">Requirements</span></span>



| <span data-ttu-id="08d88-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="08d88-146">Requirement</span></span> | <span data-ttu-id="08d88-147">Valore</span><span class="sxs-lookup"><span data-stu-id="08d88-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08d88-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08d88-148">Minimum supported client</span></span><br/> | <span data-ttu-id="08d88-149">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="08d88-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="08d88-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08d88-150">Minimum supported server</span></span><br/> | <span data-ttu-id="08d88-151">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="08d88-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08d88-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="08d88-152">Namespace</span></span><br/>                | <span data-ttu-id="08d88-153">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="08d88-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="08d88-154">MOF</span><span class="sxs-lookup"><span data-stu-id="08d88-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08d88-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08d88-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08d88-156">DLL</span><span class="sxs-lookup"><span data-stu-id="08d88-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08d88-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08d88-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="08d88-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08d88-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d88-159">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="08d88-159">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

