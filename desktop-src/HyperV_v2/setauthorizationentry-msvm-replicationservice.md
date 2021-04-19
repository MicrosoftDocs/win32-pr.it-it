---
description: Imposta la voce di autorizzazione di replica per una macchina virtuale.
ms.assetid: 39b6b0c4-5515-4863-9038-4c37421abe65
title: Metodo SetAuthorizationEntry della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 03b2c2c37a38e957a1b560e2314845abf204ee01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311774"
---
# <a name="setauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="c05b7-103">Metodo SetAuthorizationEntry della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="c05b7-103">SetAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="c05b7-104">Imposta la voce di autorizzazione di replica per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c05b7-104">Sets the replication authorization entry for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c05b7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c05b7-105">Syntax</span></span>


```mof
uint32 SetAuthorizationEntry(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 AuthorizationEntry,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c05b7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c05b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c05b7-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c05b7-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c05b7-108">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per cui impostare la voce di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="c05b7-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to set the authorization entry for.</span></span>

</dd> <dt>

<span data-ttu-id="c05b7-109">*AuthorizationEntry* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c05b7-109">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c05b7-110">Rappresentazione in forma di stringa di un'istanza della classe [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) che definisce la voce di autorizzazione da utilizzare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c05b7-110">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be used for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c05b7-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c05b7-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c05b7-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c05b7-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c05b7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c05b7-113">Return value</span></span>

<span data-ttu-id="c05b7-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c05b7-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c05b7-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="c05b7-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="c05b7-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="c05b7-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="c05b7-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="c05b7-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="c05b7-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="c05b7-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c05b7-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-123">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c05b7-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="c05b7-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c05b7-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="c05b7-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c05b7-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c05b7-128">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="c05b7-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c05b7-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c05b7-129">Requirements</span></span>



| <span data-ttu-id="c05b7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c05b7-130">Requirement</span></span> | <span data-ttu-id="c05b7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c05b7-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c05b7-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c05b7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c05b7-133">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c05b7-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c05b7-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c05b7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c05b7-135">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c05b7-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c05b7-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c05b7-136">Namespace</span></span><br/>                | <span data-ttu-id="c05b7-137">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c05b7-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c05b7-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c05b7-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c05b7-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c05b7-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c05b7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c05b7-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c05b7-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c05b7-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c05b7-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c05b7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c05b7-143">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="c05b7-143">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="c05b7-144">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="c05b7-144">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="c05b7-145">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="c05b7-145">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="c05b7-146">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="c05b7-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

