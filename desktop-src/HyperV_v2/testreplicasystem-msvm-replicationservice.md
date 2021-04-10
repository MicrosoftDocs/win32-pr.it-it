---
description: Crea una nuova replica di una macchina virtuale con lo snapshot specificato a scopo di test.
ms.assetid: 447f3c8f-8c57-4874-9466-91c6aea533bc
title: Metodo TestReplicaSystem della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicaSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 029130e619aa36d0aa9b9c1c85a877fb26e1b22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884597"
---
# <a name="testreplicasystem-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="5eadb-103">Metodo TestReplicaSystem della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="5eadb-103">TestReplicaSystem method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="5eadb-104">Crea una nuova replica di una macchina virtuale con lo snapshot specificato a scopo di test.</span><span class="sxs-lookup"><span data-stu-id="5eadb-104">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eadb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5eadb-105">Syntax</span></span>


```mof
uint32 TestReplicaSystem(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5eadb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5eadb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eadb-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5eadb-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eadb-108">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui deve essere testata la replica.</span><span class="sxs-lookup"><span data-stu-id="5eadb-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be tested.</span></span>

</dd> <dt>

<span data-ttu-id="5eadb-109">*SnapshotSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5eadb-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eadb-110">Riferimento a un'istanza [**di \_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) che rappresenta lo snapshot utilizzato per creare il sistema di failover di test.</span><span class="sxs-lookup"><span data-stu-id="5eadb-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used to create the test failover system.</span></span> <span data-ttu-id="5eadb-111">Se questo parametro è **null**, il failover deve essere eseguito al di fuori dell'ultimo punto nel tempo.</span><span class="sxs-lookup"><span data-stu-id="5eadb-111">If this parameter is **Null**, the failover is to be performed off the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="5eadb-112">*ResultingSystem* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5eadb-112">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eadb-113">Se una macchina virtuale è definita correttamente, riceve un riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale di test appena definita.</span><span class="sxs-lookup"><span data-stu-id="5eadb-113">If a virtual machine is successfully defined, receives a reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly defined test virtual machine.</span></span> <span data-ttu-id="5eadb-114">Quando il sistema non è più necessario, eliminarlo chiamando il metodo [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="5eadb-114">When this system is no longer needed, destroy it by calling the [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="5eadb-115">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="5eadb-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eadb-116">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5eadb-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eadb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5eadb-117">Return value</span></span>

<span data-ttu-id="5eadb-118">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5eadb-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5eadb-119">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="5eadb-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-120">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="5eadb-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-121">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="5eadb-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-122">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="5eadb-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-123">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="5eadb-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-124">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="5eadb-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-125">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="5eadb-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-126">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="5eadb-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-127">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="5eadb-127">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-128">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="5eadb-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-129">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="5eadb-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-130">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="5eadb-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-131">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="5eadb-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="5eadb-132">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="5eadb-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5eadb-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5eadb-133">Requirements</span></span>



| <span data-ttu-id="5eadb-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eadb-134">Requirement</span></span> | <span data-ttu-id="5eadb-135">Valore</span><span class="sxs-lookup"><span data-stu-id="5eadb-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eadb-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5eadb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5eadb-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5eadb-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5eadb-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5eadb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5eadb-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5eadb-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5eadb-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5eadb-140">Namespace</span></span><br/>                | <span data-ttu-id="5eadb-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5eadb-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5eadb-142">MOF</span><span class="sxs-lookup"><span data-stu-id="5eadb-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5eadb-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5eadb-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5eadb-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5eadb-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5eadb-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5eadb-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5eadb-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5eadb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eadb-147">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="5eadb-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

