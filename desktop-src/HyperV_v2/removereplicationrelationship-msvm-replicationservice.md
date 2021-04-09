---
description: Rimuove una relazione di replica della macchina virtuale e agisce sulla relazione di replica primaria della macchina virtuale.
ms.assetid: a9a20aa1-378d-4a2a-9ebc-9786ab2dfda7
title: Metodo RemoveReplicationRelationship della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb897ff72cd927390362f076114fc8757baa6c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879574"
---
# <a name="removereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="4c058-103">Metodo RemoveReplicationRelationship della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="4c058-103">RemoveReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="4c058-104">Rimuove una relazione di replica della macchina virtuale e agisce sulla relazione di replica primaria della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4c058-104">Removes a virtual machine replication relationship and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="4c058-105">A partire da Windows 8.1, è consigliabile non usare più **RemoveReplicationRelationship** per rimuovere una relazione di replica della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4c058-105">Starting with Windows 8.1, we recommend not to use **RemoveReplicationRelationship** anymore to remove a virtual machine replication relationship.</span></span> <span data-ttu-id="4c058-106">Usare invece [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="4c058-106">Instead, use [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4c058-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c058-107">Syntax</span></span>


```mof
uint32 RemoveReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4c058-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c058-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c058-109">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c058-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c058-110">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui deve essere rimossa la relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="4c058-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication relationship should be removed.</span></span>

</dd> <dt>

<span data-ttu-id="4c058-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4c058-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c058-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4c058-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c058-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c058-113">Return value</span></span>

<span data-ttu-id="4c058-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4c058-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4c058-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="4c058-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="4c058-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="4c058-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="4c058-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="4c058-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="4c058-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="4c058-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="4c058-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-123">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="4c058-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="4c058-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="4c058-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="4c058-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="4c058-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="4c058-128">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="4c058-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4c058-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c058-129">Requirements</span></span>



| <span data-ttu-id="4c058-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c058-130">Requirement</span></span> | <span data-ttu-id="4c058-131">Valore</span><span class="sxs-lookup"><span data-stu-id="4c058-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c058-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c058-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4c058-133">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4c058-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4c058-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c058-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4c058-135">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4c058-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c058-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4c058-136">Namespace</span></span><br/>                | <span data-ttu-id="4c058-137">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4c058-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4c058-138">MOF</span><span class="sxs-lookup"><span data-stu-id="4c058-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c058-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c058-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c058-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4c058-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c058-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4c058-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4c058-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c058-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c058-143">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="4c058-143">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="4c058-144">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="4c058-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

