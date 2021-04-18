---
description: Modifica le impostazioni di replica per una macchina virtuale. Quando un client chiama questo metodo per una macchina virtuale di replica, modifica le impostazioni di replica della relazione di replica con la replica estesa.
ms.assetid: e68514a5-f508-4047-8dcc-6a95f3e3353e
title: Metodo ModifyReplicationSettings della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyReplicationSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1c932f06350324e0d84559724f7ba0412dfb3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315492"
---
# <a name="modifyreplicationsettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="04162-104">Metodo ModifyReplicationSettings della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="04162-104">ModifyReplicationSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="04162-105">Modifica le impostazioni di replica per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="04162-105">Modifies the replication settings for a virtual machine.</span></span> <span data-ttu-id="04162-106">Quando un client chiama questo metodo per una macchina virtuale di replica, modifica le impostazioni di replica della relazione di replica con la replica estesa.</span><span class="sxs-lookup"><span data-stu-id="04162-106">When a client calls this method for a replica virtual machine, it modifies the replication settings of the replication relationship with the extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="04162-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04162-107">Syntax</span></span>


```mof
uint32 ModifyReplicationSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="04162-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="04162-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04162-109">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04162-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04162-110">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui devono essere modificate le impostazioni di replica.</span><span class="sxs-lookup"><span data-stu-id="04162-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication settings should be modified.</span></span>

</dd> <dt>

<span data-ttu-id="04162-111">*ReplicationSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04162-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04162-112">Rappresentazione di stringa della classe [**\_ ReplicationSettingData MSVM**](msvm-replicationsettingdata.md) che definisce le nuove impostazioni di replica.</span><span class="sxs-lookup"><span data-stu-id="04162-112">A string representation of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the new replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="04162-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="04162-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04162-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04162-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04162-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04162-115">Return value</span></span>

<span data-ttu-id="04162-116">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="04162-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="04162-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="04162-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04162-118">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="04162-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="04162-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="04162-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="04162-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="04162-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="04162-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="04162-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="04162-122">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="04162-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="04162-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="04162-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="04162-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="04162-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="04162-125">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="04162-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="04162-126">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="04162-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="04162-127">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="04162-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="04162-128">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="04162-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="04162-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="04162-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="04162-130">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="04162-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="04162-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="04162-131">Remarks</span></span>

<span data-ttu-id="04162-132">**ModifyReplicationSettings** accetta un'istanza di [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) come input.</span><span class="sxs-lookup"><span data-stu-id="04162-132">**ModifyReplicationSettings** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="04162-133">Il FRSD associato per la macchina virtuale come provider da host a host è la scelta predefinita.</span><span class="sxs-lookup"><span data-stu-id="04162-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="04162-134">FRSD di input viene convalidato per le impostazioni valide per ogni proprietà del provider predefinito.</span><span class="sxs-lookup"><span data-stu-id="04162-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="04162-135">In questa tabella vengono riepilogate le differenze di convalida rispetto al provider esterno.</span><span class="sxs-lookup"><span data-stu-id="04162-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="04162-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04162-136">Property</span></span>                                             | <span data-ttu-id="04162-137">Provider esterni</span><span class="sxs-lookup"><span data-stu-id="04162-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="04162-138">ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="04162-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="04162-139">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-139">Same as default provider</span></span>                           |
| <span data-ttu-id="04162-140">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="04162-140">AuthenticationType</span></span>                                   | <span data-ttu-id="04162-141">Ignorato</span><span class="sxs-lookup"><span data-stu-id="04162-141">Ignored</span></span>                                            |
| <span data-ttu-id="04162-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="04162-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="04162-143">Ignorato</span><span class="sxs-lookup"><span data-stu-id="04162-143">Ignored</span></span>                                            |
| <span data-ttu-id="04162-144">RootCertificateThumbPrint (RO)</span><span class="sxs-lookup"><span data-stu-id="04162-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="04162-145">Ignorato</span><span class="sxs-lookup"><span data-stu-id="04162-145">Ignored</span></span>                                            |
| <span data-ttu-id="04162-146">CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="04162-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="04162-147">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-147">Same as default provider</span></span>                           |
| <span data-ttu-id="04162-148">BypassProxyServer</span><span class="sxs-lookup"><span data-stu-id="04162-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="04162-149">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-149">Same as default provider</span></span>                           |
| <span data-ttu-id="04162-150">RecoveryConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="04162-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="04162-151">Ignorato \* (può cambiare se il provider ha requisito)</span><span class="sxs-lookup"><span data-stu-id="04162-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="04162-152">RecoveryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="04162-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="04162-153">Ignorato</span><span class="sxs-lookup"><span data-stu-id="04162-153">Ignored</span></span>                                            |
| <span data-ttu-id="04162-154">PrimaryConnectionPoint (RO)</span><span class="sxs-lookup"><span data-stu-id="04162-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="04162-155">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-155">Same as default provider</span></span>                           |
| <span data-ttu-id="04162-156">PrimaryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="04162-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="04162-157">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-157">Same as default provider</span></span>                           |
| <span data-ttu-id="04162-158">RecoveryServerPortNumber</span><span class="sxs-lookup"><span data-stu-id="04162-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="04162-159">Ignorato \* (può cambiare se il provider ha requisito)</span><span class="sxs-lookup"><span data-stu-id="04162-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="04162-160">ReplicateHostKvpItems</span><span class="sxs-lookup"><span data-stu-id="04162-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="04162-161">Ignorato</span><span class="sxs-lookup"><span data-stu-id="04162-161">Ignored</span></span>                                            |
| <span data-ttu-id="04162-162">ApplicationConsistentSnapshotInterval</span><span class="sxs-lookup"><span data-stu-id="04162-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="04162-163">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-163">Same as default provider</span></span>                           |
| <span data-ttu-id="04162-164">RecoveryHistory</span><span class="sxs-lookup"><span data-stu-id="04162-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="04162-165">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-165">Same as default provider</span></span>                           |
| <span data-ttu-id="04162-166">IncludedDisks\[\]</span><span class="sxs-lookup"><span data-stu-id="04162-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="04162-167">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-167">Same as default provider</span></span>                           |
| <span data-ttu-id="04162-168">AutoResynchronizeEnabled</span><span class="sxs-lookup"><span data-stu-id="04162-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="04162-169">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-169">Same as default provider</span></span>                           |
| <span data-ttu-id="04162-170">AutoResynchronizeIntervalStart</span><span class="sxs-lookup"><span data-stu-id="04162-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="04162-171">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-171">Same as default provider</span></span>                           |
| <span data-ttu-id="04162-172">AutoResynchronizeIntervalEnd</span><span class="sxs-lookup"><span data-stu-id="04162-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="04162-173">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-173">Same as default provider</span></span>                           |
| <span data-ttu-id="04162-174">EnableWriteOrderPreservationAcrossDisks (deprecato)</span><span class="sxs-lookup"><span data-stu-id="04162-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="04162-175">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-175">Same as default provider</span></span>                           |
| <span data-ttu-id="04162-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="04162-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="04162-177">Uguale al provider predefinito</span><span class="sxs-lookup"><span data-stu-id="04162-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="04162-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04162-178">Requirements</span></span>



| <span data-ttu-id="04162-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="04162-179">Requirement</span></span> | <span data-ttu-id="04162-180">Valore</span><span class="sxs-lookup"><span data-stu-id="04162-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04162-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04162-181">Minimum supported client</span></span><br/> | <span data-ttu-id="04162-182">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="04162-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="04162-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04162-183">Minimum supported server</span></span><br/> | <span data-ttu-id="04162-184">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="04162-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04162-185">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="04162-185">Namespace</span></span><br/>                | <span data-ttu-id="04162-186">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="04162-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="04162-187">MOF</span><span class="sxs-lookup"><span data-stu-id="04162-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04162-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04162-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04162-189">DLL</span><span class="sxs-lookup"><span data-stu-id="04162-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04162-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04162-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="04162-191">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04162-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04162-192">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="04162-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

