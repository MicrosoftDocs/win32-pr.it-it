---
description: Rimuove la relazione di replica della macchina virtuale specificata.
ms.assetid: 0D5013CE-7BAE-4A99-ABF2-F1ECC644A1B2
title: 'Metodo Msvm_ReplicationService:: RemoveReplicationRelationshipEx'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationshipEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c57ed7f9a88789d04a20de0fd199d460b47c1eb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307869"
---
# <a name="msvm_replicationserviceremovereplicationrelationshipex-method"></a><span data-ttu-id="45ab7-103">\_Metodo MSVM ReplicationService:: RemoveReplicationRelationshipEx</span><span class="sxs-lookup"><span data-stu-id="45ab7-103">Msvm\_ReplicationService::RemoveReplicationRelationshipEx method</span></span>

<span data-ttu-id="45ab7-104">Rimuove la relazione di replica della macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="45ab7-104">Removes the specified virtual machine replication relationship.</span></span>

## <a name="syntax"></a><span data-ttu-id="45ab7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45ab7-105">Syntax</span></span>


```C++
uint32 RemoveReplicationRelationshipEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="45ab7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="45ab7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45ab7-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45ab7-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45ab7-108">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per la quale rimuovere la replica.</span><span class="sxs-lookup"><span data-stu-id="45ab7-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to remove the replication.</span></span>

</dd> <dt>

<span data-ttu-id="45ab7-109">*ReplicationRelationship* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45ab7-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45ab7-110">Rappresentazione di stringa di un'istanza incorporata della classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) che definisce la relazione di replica da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="45ab7-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship to remove.</span></span>

</dd> <dt>

<span data-ttu-id="45ab7-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="45ab7-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45ab7-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45ab7-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="45ab7-113">Questo riferimento può essere **null** se l'attività è stata completata.</span><span class="sxs-lookup"><span data-stu-id="45ab7-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45ab7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45ab7-114">Return value</span></span>

<span data-ttu-id="45ab7-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="45ab7-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="45ab7-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="45ab7-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="45ab7-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="45ab7-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="45ab7-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="45ab7-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="45ab7-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="45ab7-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="45ab7-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-124">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="45ab7-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="45ab7-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="45ab7-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="45ab7-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="45ab7-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="45ab7-129">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="45ab7-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="45ab7-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="45ab7-130">Remarks</span></span>

<span data-ttu-id="45ab7-131">Per una macchina virtuale di replica, non è possibile rimuovere la replica primaria se è abilitata la replica estesa.</span><span class="sxs-lookup"><span data-stu-id="45ab7-131">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="45ab7-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45ab7-132">Requirements</span></span>



| <span data-ttu-id="45ab7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="45ab7-133">Requirement</span></span> | <span data-ttu-id="45ab7-134">Valore</span><span class="sxs-lookup"><span data-stu-id="45ab7-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ab7-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45ab7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="45ab7-136">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45ab7-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="45ab7-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45ab7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="45ab7-138">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="45ab7-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="45ab7-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="45ab7-139">Namespace</span></span><br/>                | <span data-ttu-id="45ab7-140">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="45ab7-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="45ab7-141">MOF</span><span class="sxs-lookup"><span data-stu-id="45ab7-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45ab7-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45ab7-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45ab7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="45ab7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45ab7-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45ab7-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="45ab7-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45ab7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ab7-146">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="45ab7-146">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="45ab7-147">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="45ab7-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

