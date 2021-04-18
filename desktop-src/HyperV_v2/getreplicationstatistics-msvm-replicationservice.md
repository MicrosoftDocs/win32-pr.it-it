---
description: Recupera le statistiche di replica per una macchina virtuale e agisce sulla relazione di replica primaria della macchina virtuale.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Metodo GetReplicationStatistics della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9dff711830ccdb805c362961671dff28f5bf0b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307734"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="4ce95-103">Metodo GetReplicationStatistics della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="4ce95-103">GetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="4ce95-104">Recupera le statistiche di replica per una macchina virtuale e agisce sulla relazione di replica primaria della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4ce95-104">Retrieves replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="4ce95-105">A partire da Windows 8.1, è consigliabile non usare più **GetReplicationStatistics** per recuperare le statistiche di replica.</span><span class="sxs-lookup"><span data-stu-id="4ce95-105">Starting with Windows 8.1, we recommend not to use **GetReplicationStatistics** anymore to retrieve replication statistics.</span></span> <span data-ttu-id="4ce95-106">Usare invece [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="4ce95-106">Instead, use [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4ce95-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ce95-107">Syntax</span></span>


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4ce95-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ce95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ce95-109">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ce95-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce95-110">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per la quale recuperare le statistiche di replica.</span><span class="sxs-lookup"><span data-stu-id="4ce95-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="4ce95-111">*ReplicationStatistics* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4ce95-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce95-112">In caso di esito positivo, riceve un'istanza incorporata della classe [**MSVM \_ ReplicationStatistics**](msvm-replicationstatistics.md) contenente le statistiche di replica per la macchina virtuale richiesta.</span><span class="sxs-lookup"><span data-stu-id="4ce95-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="4ce95-113">*ReplicationHealthIssues* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4ce95-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce95-114">In caso di esito positivo, riceve una matrice di istanze incorporate della classe di [**\_ errore MSVM**](msvm-error.md) che indicano eventuali avvisi o errori di replica per la macchina virtuale richiesta.</span><span class="sxs-lookup"><span data-stu-id="4ce95-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="4ce95-115">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4ce95-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce95-116">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4ce95-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ce95-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ce95-117">Return value</span></span>

<span data-ttu-id="4ce95-118">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4ce95-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4ce95-119">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="4ce95-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-120">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="4ce95-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-121">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="4ce95-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-122">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="4ce95-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-123">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="4ce95-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-124">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="4ce95-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-125">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="4ce95-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-126">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="4ce95-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-127">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="4ce95-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-128">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="4ce95-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-129">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="4ce95-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-130">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="4ce95-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-131">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="4ce95-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="4ce95-132">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="4ce95-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4ce95-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ce95-133">Requirements</span></span>



| <span data-ttu-id="4ce95-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ce95-134">Requirement</span></span> | <span data-ttu-id="4ce95-135">Valore</span><span class="sxs-lookup"><span data-stu-id="4ce95-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce95-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ce95-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4ce95-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4ce95-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4ce95-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ce95-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4ce95-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4ce95-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ce95-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4ce95-140">Namespace</span></span><br/>                | <span data-ttu-id="4ce95-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4ce95-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4ce95-142">MOF</span><span class="sxs-lookup"><span data-stu-id="4ce95-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ce95-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ce95-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ce95-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4ce95-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ce95-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ce95-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ce95-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ce95-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ce95-147">**ResetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="4ce95-147">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="4ce95-148">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="4ce95-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

