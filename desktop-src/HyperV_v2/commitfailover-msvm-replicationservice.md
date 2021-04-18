---
description: Consente di eseguire il commit dello snapshot di recupero utilizzato dal metodo InitiateFailover per un failover.
ms.assetid: 05c27211-adc7-400a-83e2-81792ae7577f
title: Metodo CommitFailover della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CommitFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 04687ea29f39645c2407de44faf6bba6ecc75832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313372"
---
# <a name="commitfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="8b6e9-103">Metodo CommitFailover della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="8b6e9-103">CommitFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="8b6e9-104">Consente di eseguire il commit dello snapshot di recupero utilizzato dal metodo [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) per un failover.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-104">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span>

<span data-ttu-id="8b6e9-105">Questo metodo rende Flat i punti di ripristino nella macchina virtuale di ripristino applicando lo snapshot di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-105">This method flattens the recovery points on the recovery virtual machine by applying the recovery snapshot.</span></span> <span data-ttu-id="8b6e9-106">Al termine di questa operazione, non è possibile annullare l'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-106">After this is done, the failover operation cannot be canceled.</span></span> <span data-ttu-id="8b6e9-107">In genere, gli utenti eseguono questa operazione quando il punto di replica usato per il failover è soddisfacente e la macchina virtuale di ripristino può modificare il ruolo in modo che sia primario.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-107">Users will typically perform this when the replication point used for failover is satisfactory and the recovery virtual machine can change role to be primary.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b6e9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b6e9-108">Syntax</span></span>


```mof
uint32 CommitFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8b6e9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b6e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b6e9-110">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b6e9-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b6e9-111">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per la quale eseguire il commit del failover.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-111">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to commit the failover.</span></span>

</dd> <dt>

<span data-ttu-id="8b6e9-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="8b6e9-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b6e9-113">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b6e9-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b6e9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b6e9-114">Return value</span></span>

<span data-ttu-id="8b6e9-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8b6e9-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-124">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="8b6e9-129">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="8b6e9-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8b6e9-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b6e9-130">Requirements</span></span>



| <span data-ttu-id="8b6e9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b6e9-131">Requirement</span></span> | <span data-ttu-id="8b6e9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="8b6e9-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b6e9-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b6e9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8b6e9-134">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8b6e9-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8b6e9-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b6e9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8b6e9-136">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8b6e9-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b6e9-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8b6e9-137">Namespace</span></span><br/>                | <span data-ttu-id="8b6e9-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8b6e9-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8b6e9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8b6e9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b6e9-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b6e9-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b6e9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8b6e9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b6e9-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b6e9-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b6e9-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b6e9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b6e9-144">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="8b6e9-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

