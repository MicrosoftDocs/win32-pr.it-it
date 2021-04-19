---
description: Replica una macchina virtuale di cui è stato eseguito il failover sul server primario.
ms.assetid: 21806a66-85b4-4d9e-8a50-52d2b1933b67
title: Metodo ReverseReplicationRelationship della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ReverseReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 25ab0c754c5139b0b3419db74162a8ac0495cf1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311781"
---
# <a name="reversereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="fb859-103">Metodo ReverseReplicationRelationship della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="fb859-103">ReverseReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="fb859-104">Replica una macchina virtuale di cui è stato eseguito il failover sul server primario.</span><span class="sxs-lookup"><span data-stu-id="fb859-104">Replicates a failed-over virtual machine back to the primary server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb859-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb859-105">Syntax</span></span>


```mof
uint32 ReverseReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fb859-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb859-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb859-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb859-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb859-108">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui deve essere annullata la replica.</span><span class="sxs-lookup"><span data-stu-id="fb859-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be reversed.</span></span>

</dd> <dt>

<span data-ttu-id="fb859-109">*ReplicationSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb859-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb859-110">Rappresentazione di stringa di un'istanza della classe [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) che definisce le impostazioni di replica.</span><span class="sxs-lookup"><span data-stu-id="fb859-110">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="fb859-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="fb859-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb859-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fb859-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb859-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb859-113">Return value</span></span>

<span data-ttu-id="fb859-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fb859-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fb859-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="fb859-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="fb859-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="fb859-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="fb859-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="fb859-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="fb859-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="fb859-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="fb859-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-123">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="fb859-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="fb859-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="fb859-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="fb859-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="fb859-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="fb859-128">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="fb859-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fb859-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb859-129">Requirements</span></span>



| <span data-ttu-id="fb859-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb859-130">Requirement</span></span> | <span data-ttu-id="fb859-131">Valore</span><span class="sxs-lookup"><span data-stu-id="fb859-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb859-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb859-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fb859-133">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fb859-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fb859-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb859-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fb859-135">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fb859-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb859-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fb859-136">Namespace</span></span><br/>                | <span data-ttu-id="fb859-137">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fb859-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fb859-138">MOF</span><span class="sxs-lookup"><span data-stu-id="fb859-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb859-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb859-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb859-140">DLL</span><span class="sxs-lookup"><span data-stu-id="fb859-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb859-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fb859-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fb859-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb859-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb859-143">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="fb859-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

