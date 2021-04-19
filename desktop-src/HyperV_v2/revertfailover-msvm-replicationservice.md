---
description: Annulla il failover corrente per una macchina virtuale ignorando il disco di failover corrente.
ms.assetid: 99d3a3d3-49e4-4410-b979-47b62ebc6aa6
title: Metodo RevertFailover della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RevertFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: db20abf34fdad2e0eba499fd1b4cc390bf93b754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319503"
---
# <a name="revertfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="067e3-103">Metodo RevertFailover della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="067e3-103">RevertFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="067e3-104">Annulla il failover corrente per una macchina virtuale ignorando il disco di failover corrente.</span><span class="sxs-lookup"><span data-stu-id="067e3-104">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span> <span data-ttu-id="067e3-105">Dopo questa operazione, è possibile chiamare di nuovo [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="067e3-105">After this operation, [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) can be called again.</span></span>

## <a name="syntax"></a><span data-ttu-id="067e3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="067e3-106">Syntax</span></span>


```mof
uint32 RevertFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="067e3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="067e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="067e3-108">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="067e3-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="067e3-109">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per la quale ripristinare il failover.</span><span class="sxs-lookup"><span data-stu-id="067e3-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to revert the failover.</span></span>

</dd> <dt>

<span data-ttu-id="067e3-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="067e3-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="067e3-111">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="067e3-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="067e3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="067e3-112">Return value</span></span>

<span data-ttu-id="067e3-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="067e3-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="067e3-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="067e3-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-115">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="067e3-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-116">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="067e3-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-117">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="067e3-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-118">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="067e3-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-119">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="067e3-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="067e3-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-121">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="067e3-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-122">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="067e3-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-123">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="067e3-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-124">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="067e3-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-125">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="067e3-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-126">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="067e3-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="067e3-127">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="067e3-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="067e3-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="067e3-128">Requirements</span></span>



| <span data-ttu-id="067e3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="067e3-129">Requirement</span></span> | <span data-ttu-id="067e3-130">Valore</span><span class="sxs-lookup"><span data-stu-id="067e3-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="067e3-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="067e3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="067e3-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="067e3-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="067e3-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="067e3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="067e3-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="067e3-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="067e3-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="067e3-135">Namespace</span></span><br/>                | <span data-ttu-id="067e3-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="067e3-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="067e3-137">MOF</span><span class="sxs-lookup"><span data-stu-id="067e3-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="067e3-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="067e3-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="067e3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="067e3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="067e3-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="067e3-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="067e3-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="067e3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="067e3-142">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="067e3-142">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="067e3-143">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="067e3-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="067e3-144">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="067e3-144">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

