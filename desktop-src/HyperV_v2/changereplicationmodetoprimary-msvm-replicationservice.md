---
description: Consente di modificare la relazione di replica estesa con la relazione primaria per una macchina virtuale di replica. La macchina virtuale di replica deve trovarsi in uno stato di commit del failover.
ms.assetid: B593A155-B5E6-44E5-8835-09DEB1FF868E
title: 'Metodo Msvm_ReplicationService:: ChangeReplicationModeToPrimary'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ChangeReplicationModeToPrimary
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0a18b3c9f1003ff7b263f5c6b7cc89abedccfd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306050"
---
# <a name="msvm_replicationservicechangereplicationmodetoprimary-method"></a><span data-ttu-id="d9bfd-104">\_Metodo MSVM ReplicationService:: ChangeReplicationModeToPrimary</span><span class="sxs-lookup"><span data-stu-id="d9bfd-104">Msvm\_ReplicationService::ChangeReplicationModeToPrimary method</span></span>

<span data-ttu-id="d9bfd-105">Consente di modificare la relazione di replica estesa con la relazione primaria per una macchina virtuale di replica.</span><span class="sxs-lookup"><span data-stu-id="d9bfd-105">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="d9bfd-106">La macchina virtuale di replica deve trovarsi in uno stato di commit del failover.</span><span class="sxs-lookup"><span data-stu-id="d9bfd-106">The replica virtual machine must be in a failover committed state.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9bfd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9bfd-107">Syntax</span></span>


```C++
uint32 ChangeReplicationModeToPrimary(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="d9bfd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9bfd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9bfd-109">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9bfd-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9bfd-110">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per la quale questo metodo modifica la relazione di replica estesa con la relazione primaria.</span><span class="sxs-lookup"><span data-stu-id="d9bfd-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which this method changes the extended replication relationship to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="d9bfd-111">*ReplicationRelationship* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9bfd-111">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9bfd-112">Rappresentazione in forma di stringa di un'istanza incorporata della classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) che definisce la relazione di replica estesa che questo metodo modifica alla relazione primaria.</span><span class="sxs-lookup"><span data-stu-id="d9bfd-112">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the extended replication relationship that this method changes to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="d9bfd-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="d9bfd-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9bfd-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9bfd-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="d9bfd-115">Questo riferimento può essere **null** se l'attività è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d9bfd-115">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9bfd-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9bfd-116">Return value</span></span>

<span data-ttu-id="d9bfd-117">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d9bfd-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d9bfd-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-119">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-120">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-123">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-125">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-126">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-127">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-128">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-129">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d9bfd-131">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="d9bfd-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d9bfd-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9bfd-132">Requirements</span></span>



| <span data-ttu-id="d9bfd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9bfd-133">Requirement</span></span> | <span data-ttu-id="d9bfd-134">Valore</span><span class="sxs-lookup"><span data-stu-id="d9bfd-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9bfd-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9bfd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d9bfd-136">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d9bfd-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d9bfd-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9bfd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d9bfd-138">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9bfd-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d9bfd-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d9bfd-139">Namespace</span></span><br/>                | <span data-ttu-id="d9bfd-140">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d9bfd-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="d9bfd-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d9bfd-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9bfd-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9bfd-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9bfd-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d9bfd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9bfd-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d9bfd-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d9bfd-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9bfd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9bfd-146">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="d9bfd-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

