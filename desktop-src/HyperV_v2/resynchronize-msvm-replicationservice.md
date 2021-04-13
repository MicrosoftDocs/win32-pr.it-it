---
description: Esegue un'operazione di risincronizzazione nella macchina virtuale specificata.
ms.assetid: a3d06780-f43b-45c4-a186-a3544f9c7963
title: Risincronizzare il metodo della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.Resynchronize
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: dcd4865d110843de27f0a242b31253310439e1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346356"
---
# <a name="resynchronize-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="dcd19-103">Metodo resynchronize della \_ classe ReplicationService di MSVM</span><span class="sxs-lookup"><span data-stu-id="dcd19-103">Resynchronize method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="dcd19-104">Esegue un'operazione di risincronizzazione nella macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="dcd19-104">Performs a resynchronization operation on the specified virtual machine.</span></span> <span data-ttu-id="dcd19-105">Quando un client chiama questo metodo per una macchina virtuale di replica, viene risincronizzato con la replica estesa.</span><span class="sxs-lookup"><span data-stu-id="dcd19-105">When a client calls this method for a replica virtual machine, it resynchronizes with extended replica.</span></span>

<span data-ttu-id="dcd19-106">Questo metodo confronta i dischi abilitati per la replica nelle macchine virtuali primarie e di ripristino e corregge eventuali problemi di integrità dei dati di replica replicando i diversi blocchi dal database primario al recupero.</span><span class="sxs-lookup"><span data-stu-id="dcd19-106">This methods compares the replication enabled disks on the primary and recovery virtual machines, and fixes any replication data integrity issues by replicating the different blocks from the primary to the recovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcd19-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcd19-107">Syntax</span></span>


```mof
uint32 Resynchronize(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="dcd19-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcd19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcd19-109">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcd19-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd19-110">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale da risincronizzare.</span><span class="sxs-lookup"><span data-stu-id="dcd19-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to be resynchronized.</span></span>

</dd> <dt>

<span data-ttu-id="dcd19-111">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcd19-111">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd19-112">Ora di inizio pianificata in cui iniziare l'operazione di risincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="dcd19-112">The scheduled start time for the resynchronization operation to begin.</span></span> <span data-ttu-id="dcd19-113">Se questo parametro è **null**, l'operazione di risincronizzazione viene avviata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="dcd19-113">If this parameter is **Null**, the resynchronization operation starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="dcd19-114">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="dcd19-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd19-115">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dcd19-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcd19-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcd19-116">Return value</span></span>

<span data-ttu-id="dcd19-117">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="dcd19-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dcd19-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="dcd19-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-119">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="dcd19-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-120">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="dcd19-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="dcd19-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="dcd19-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-123">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="dcd19-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="dcd19-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-125">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="dcd19-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-126">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="dcd19-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-127">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="dcd19-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-128">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="dcd19-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-129">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="dcd19-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="dcd19-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="dcd19-131">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="dcd19-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dcd19-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcd19-132">Requirements</span></span>



| <span data-ttu-id="dcd19-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcd19-133">Requirement</span></span> | <span data-ttu-id="dcd19-134">Valore</span><span class="sxs-lookup"><span data-stu-id="dcd19-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd19-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcd19-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dcd19-136">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dcd19-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dcd19-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcd19-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dcd19-138">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dcd19-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dcd19-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dcd19-139">Namespace</span></span><br/>                | <span data-ttu-id="dcd19-140">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="dcd19-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dcd19-141">MOF</span><span class="sxs-lookup"><span data-stu-id="dcd19-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcd19-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcd19-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcd19-143">DLL</span><span class="sxs-lookup"><span data-stu-id="dcd19-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcd19-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dcd19-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dcd19-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcd19-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd19-146">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="dcd19-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

