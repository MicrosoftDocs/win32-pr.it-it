---
description: Reimposta le statistiche di replica associate alla relazione di replica specificata della macchina virtuale specificata.
ms.assetid: 6E49A7C0-2F60-444E-964E-420470EE1538
title: 'Metodo Msvm_ReplicationService:: ResetReplicationStatisticsEx'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c1acb234660e71636b4a69a697b11385d65cf1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883029"
---
# <a name="msvm_replicationserviceresetreplicationstatisticsex-method"></a><span data-ttu-id="02717-103">\_Metodo MSVM ReplicationService:: ResetReplicationStatisticsEx</span><span class="sxs-lookup"><span data-stu-id="02717-103">Msvm\_ReplicationService::ResetReplicationStatisticsEx method</span></span>

<span data-ttu-id="02717-104">Reimposta le statistiche di replica associate alla relazione di replica specificata della macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="02717-104">Resets replication statistics that are associated with the specified replication relationship of the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="02717-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02717-105">Syntax</span></span>


```C++
uint32 ResetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="02717-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="02717-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02717-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02717-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02717-108">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale abilitata per la replica.</span><span class="sxs-lookup"><span data-stu-id="02717-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the replica-enabled virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="02717-109">*ReplicationRelationship* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02717-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02717-110">Rappresentazione di stringa di un'istanza incorporata della classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) che definisce la relazione di replica per la quale reimpostare le statistiche di replica.</span><span class="sxs-lookup"><span data-stu-id="02717-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to reset the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="02717-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="02717-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02717-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="02717-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="02717-113">Questo riferimento può essere **null** se l'attività è stata completata.</span><span class="sxs-lookup"><span data-stu-id="02717-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02717-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02717-114">Return value</span></span>

<span data-ttu-id="02717-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="02717-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="02717-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="02717-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="02717-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="02717-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="02717-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="02717-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="02717-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="02717-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="02717-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="02717-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="02717-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="02717-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="02717-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="02717-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="02717-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="02717-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="02717-124">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="02717-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="02717-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="02717-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="02717-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="02717-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="02717-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="02717-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="02717-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="02717-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="02717-129">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="02717-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="02717-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02717-130">Requirements</span></span>



| <span data-ttu-id="02717-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="02717-131">Requirement</span></span> | <span data-ttu-id="02717-132">Valore</span><span class="sxs-lookup"><span data-stu-id="02717-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02717-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02717-133">Minimum supported client</span></span><br/> | <span data-ttu-id="02717-134">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="02717-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="02717-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02717-135">Minimum supported server</span></span><br/> | <span data-ttu-id="02717-136">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="02717-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="02717-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="02717-137">Namespace</span></span><br/>                | <span data-ttu-id="02717-138">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="02717-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="02717-139">MOF</span><span class="sxs-lookup"><span data-stu-id="02717-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02717-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02717-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02717-141">DLL</span><span class="sxs-lookup"><span data-stu-id="02717-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02717-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02717-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="02717-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02717-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02717-144">**GetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="02717-144">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="02717-145">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="02717-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

