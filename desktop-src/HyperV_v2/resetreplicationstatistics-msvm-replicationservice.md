---
description: Reimposta le statistiche di replica per una macchina virtuale e agisce sulla relazione di replica primaria della macchina virtuale.
ms.assetid: da4b60f8-6964-45af-8412-935234c7c0ff
title: Metodo ResetReplicationStatistics della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8407e20cb38c9aecac26ab0bcee99ce0c8a6be2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312331"
---
# <a name="resetreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="87f32-103">Metodo ResetReplicationStatistics della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="87f32-103">ResetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="87f32-104">Reimposta le statistiche di replica per una macchina virtuale e agisce sulla relazione di replica primaria della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="87f32-104">Resets the replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="87f32-105">A partire da Windows 8.1, è consigliabile non usare più **ResetReplicationStatistics** per reimpostare le statistiche di replica.</span><span class="sxs-lookup"><span data-stu-id="87f32-105">Starting with Windows 8.1, we recommend not to use **ResetReplicationStatistics** anymore to reset replication statistics.</span></span> <span data-ttu-id="87f32-106">Usare invece [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="87f32-106">Instead, use [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="87f32-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87f32-107">Syntax</span></span>


```mof
uint32 ResetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="87f32-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="87f32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f32-109">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87f32-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f32-110">Riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per la quale reimpostare le statistiche di replica.</span><span class="sxs-lookup"><span data-stu-id="87f32-110">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to reset the replication statistics for.</span></span>

</dd> <dt>

<span data-ttu-id="87f32-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="87f32-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87f32-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="87f32-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f32-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87f32-113">Return value</span></span>

<span data-ttu-id="87f32-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="87f32-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="87f32-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="87f32-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="87f32-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="87f32-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="87f32-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="87f32-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="87f32-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="87f32-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="87f32-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-123">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="87f32-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="87f32-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="87f32-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="87f32-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="87f32-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="87f32-128">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="87f32-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="87f32-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87f32-129">Requirements</span></span>



| <span data-ttu-id="87f32-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="87f32-130">Requirement</span></span> | <span data-ttu-id="87f32-131">Valore</span><span class="sxs-lookup"><span data-stu-id="87f32-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87f32-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87f32-132">Minimum supported client</span></span><br/> | <span data-ttu-id="87f32-133">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="87f32-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="87f32-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87f32-134">Minimum supported server</span></span><br/> | <span data-ttu-id="87f32-135">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="87f32-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87f32-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="87f32-136">Namespace</span></span><br/>                | <span data-ttu-id="87f32-137">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="87f32-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="87f32-138">MOF</span><span class="sxs-lookup"><span data-stu-id="87f32-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87f32-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87f32-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87f32-140">DLL</span><span class="sxs-lookup"><span data-stu-id="87f32-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87f32-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87f32-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="87f32-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87f32-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87f32-143">**GetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="87f32-143">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="87f32-144">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="87f32-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

