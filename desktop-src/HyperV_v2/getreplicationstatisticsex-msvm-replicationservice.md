---
description: Recupera le statistiche di replica associate alla relazione di replica specificata della macchina virtuale.
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: 'Metodo Msvm_ReplicationService:: GetReplicationStatisticsEx'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7fdb60addc94094082fe83e70af06a2f5ae11f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307733"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a><span data-ttu-id="b5153-103">\_Metodo MSVM ReplicationService:: GetReplicationStatisticsEx</span><span class="sxs-lookup"><span data-stu-id="b5153-103">Msvm\_ReplicationService::GetReplicationStatisticsEx method</span></span>

<span data-ttu-id="b5153-104">Recupera le statistiche di replica associate alla relazione di replica specificata della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5153-104">Retrieves the replication statistics that are associated with the specified replication relationship of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5153-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5153-105">Syntax</span></span>


```C++
uint32 GetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="b5153-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5153-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5153-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5153-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5153-108">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per la quale recuperare le statistiche di replica.</span><span class="sxs-lookup"><span data-stu-id="b5153-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="b5153-109">*ReplicationRelationship* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5153-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5153-110">Rappresentazione di stringa di un'istanza incorporata della classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) che definisce la relazione di replica per la quale recuperare le statistiche di replica.</span><span class="sxs-lookup"><span data-stu-id="b5153-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="b5153-111">*ReplicationStatistics* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5153-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5153-112">In caso di esito positivo, riceve un'istanza incorporata della classe [**\_ ReplicationStatistics di MSVM**](msvm-replicationstatistics.md) contenente le statistiche di replica per la relazione di replica richiesta.</span><span class="sxs-lookup"><span data-stu-id="b5153-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="b5153-113">*ReplicationHealthIssues* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5153-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5153-114">In caso di esito positivo, riceve una matrice di istanze incorporate della classe di [**\_ errore MSVM**](msvm-error.md) che indicano eventuali avvisi o errori di replica per la macchina virtuale richiesta.</span><span class="sxs-lookup"><span data-stu-id="b5153-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="b5153-115">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="b5153-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5153-116">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5153-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="b5153-117">Questo riferimento può essere **null** se l'attività è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b5153-117">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5153-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5153-118">Return value</span></span>

<span data-ttu-id="b5153-119">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b5153-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b5153-120">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="b5153-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-121">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="b5153-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-122">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="b5153-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-123">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="b5153-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-124">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="b5153-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-125">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="b5153-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-126">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="b5153-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-127">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b5153-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-128">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b5153-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-129">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="b5153-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-130">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b5153-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-131">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="b5153-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-132">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b5153-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b5153-133">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="b5153-133">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b5153-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5153-134">Requirements</span></span>



| <span data-ttu-id="b5153-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5153-135">Requirement</span></span> | <span data-ttu-id="b5153-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b5153-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5153-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5153-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b5153-138">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b5153-138">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b5153-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5153-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b5153-140">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5153-140">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b5153-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b5153-141">Namespace</span></span><br/>                | <span data-ttu-id="b5153-142">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b5153-142">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="b5153-143">MOF</span><span class="sxs-lookup"><span data-stu-id="b5153-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5153-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5153-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5153-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b5153-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5153-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5153-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5153-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5153-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5153-148">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="b5153-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="b5153-149">**ResetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="b5153-149">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

