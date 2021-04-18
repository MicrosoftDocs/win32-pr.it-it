---
description: Rimuove una voce di autorizzazione da un server di ripristino.
ms.assetid: 1647b35d-1c2f-4fb5-84c0-10b357326abf
title: Metodo RemoveAuthorizationEntry della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d0bb0d24c9cf4936c6e0187e5091b9fac14ee28c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318307"
---
# <a name="removeauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="a0cce-103">Metodo RemoveAuthorizationEntry della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="a0cce-103">RemoveAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="a0cce-104">Rimuove una voce di autorizzazione da un server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a0cce-104">Removes an authorization entry from a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0cce-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0cce-105">Syntax</span></span>


```mof
uint32 RemoveAuthorizationEntry(
  [in]  string              AllowedPrimaryHostSystem,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a0cce-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0cce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0cce-107">*AllowedPrimaryHostSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0cce-107">*AllowedPrimaryHostSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0cce-108">Server primario per il quale verrà rimossa la voce di autorizzazione dal server.</span><span class="sxs-lookup"><span data-stu-id="a0cce-108">The primary server for which the authorization entry will be removed from the server.</span></span> <span data-ttu-id="a0cce-109">Corrisponde alla proprietà **AllowedPrimaryHostSystem** della classe [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="a0cce-109">This is the same as the **AllowedPrimaryHostSystem** property of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a0cce-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a0cce-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0cce-111">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0cce-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0cce-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0cce-112">Return value</span></span>

<span data-ttu-id="a0cce-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a0cce-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a0cce-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="a0cce-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-115">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="a0cce-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-116">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="a0cce-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-117">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="a0cce-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-118">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="a0cce-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-119">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="a0cce-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="a0cce-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-121">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a0cce-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-122">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a0cce-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-123">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="a0cce-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-124">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a0cce-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-125">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="a0cce-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-126">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a0cce-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="a0cce-127">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="a0cce-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a0cce-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0cce-128">Remarks</span></span>

<span data-ttu-id="a0cce-129">La rimozione di una voce di autorizzazione arresterà la replica per tutte le macchine virtuali autorizzate con la voce.</span><span class="sxs-lookup"><span data-stu-id="a0cce-129">Removing an authorization entry will stop replication for any virtual machines that are authorized with the entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0cce-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0cce-130">Requirements</span></span>



| <span data-ttu-id="a0cce-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0cce-131">Requirement</span></span> | <span data-ttu-id="a0cce-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a0cce-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0cce-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0cce-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a0cce-134">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a0cce-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a0cce-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0cce-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a0cce-136">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a0cce-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0cce-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a0cce-137">Namespace</span></span><br/>                | <span data-ttu-id="a0cce-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a0cce-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a0cce-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a0cce-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0cce-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0cce-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0cce-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a0cce-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0cce-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0cce-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a0cce-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0cce-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0cce-144">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="a0cce-144">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="a0cce-145">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="a0cce-145">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="a0cce-146">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="a0cce-146">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="a0cce-147">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="a0cce-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

