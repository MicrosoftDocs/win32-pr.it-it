---
description: Importa la replica iniziale per una macchina virtuale.
ms.assetid: 151211fe-e58e-4fd4-87cd-cdb2ad55c0b1
title: Metodo ImportInitialReplica della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ImportInitialReplica
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b60ab10c6387127c294a472c9e1e86be7fd84146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130702"
---
# <a name="importinitialreplica-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="6e117-103">Metodo ImportInitialReplica della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="6e117-103">ImportInitialReplica method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="6e117-104">Importa la replica iniziale per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e117-104">Imports the initial replication for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e117-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e117-105">Syntax</span></span>


```mof
uint32 ImportInitialReplica(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 InitialReplicationImportLocation,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6e117-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e117-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e117-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e117-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e117-108">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui deve essere importata la replica iniziale.</span><span class="sxs-lookup"><span data-stu-id="6e117-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the initial replication should be imported.</span></span>

</dd> <dt>

<span data-ttu-id="6e117-109">*InitialReplicationImportLocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e117-109">*InitialReplicationImportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e117-110">Percorso completo della directory da cui deve essere importata la replica iniziale.</span><span class="sxs-lookup"><span data-stu-id="6e117-110">The fully qualified path of the directory from which the initial replication is to be imported.</span></span> <span data-ttu-id="6e117-111">Non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="6e117-111">This cannot be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6e117-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="6e117-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e117-113">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6e117-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e117-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e117-114">Return value</span></span>

<span data-ttu-id="6e117-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e117-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6e117-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="6e117-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="6e117-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="6e117-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="6e117-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="6e117-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="6e117-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="6e117-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="6e117-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-124">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="6e117-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="6e117-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="6e117-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="6e117-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="6e117-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="6e117-129">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="6e117-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6e117-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e117-130">Requirements</span></span>



| <span data-ttu-id="6e117-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e117-131">Requirement</span></span> | <span data-ttu-id="6e117-132">Valore</span><span class="sxs-lookup"><span data-stu-id="6e117-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e117-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e117-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6e117-134">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6e117-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6e117-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e117-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6e117-136">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6e117-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e117-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6e117-137">Namespace</span></span><br/>                | <span data-ttu-id="6e117-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6e117-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6e117-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6e117-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e117-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e117-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e117-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6e117-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e117-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e117-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6e117-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e117-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e117-144">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="6e117-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

