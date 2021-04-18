---
description: Modifica una voce di autorizzazione per un server di ripristino.
ms.assetid: fbdf3ecd-42de-49a8-85b8-51fc9c9fcf26
title: Metodo ModifyAuthorizationEntry della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 17f5ff1a0e4e1cca95dc5f7764d2f8e2bf9d2c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315499"
---
# <a name="modifyauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="17426-103">Metodo ModifyAuthorizationEntry della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="17426-103">ModifyAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="17426-104">Modifica una voce di autorizzazione per un server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="17426-104">Modifies an authorization entry for a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="17426-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17426-105">Syntax</span></span>


```mof
uint32 ModifyAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="17426-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="17426-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17426-107">*AuthorizationEntry* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17426-107">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17426-108">Rappresentazione di stringa di un'istanza della classe [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) che definisce la voce di autorizzazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="17426-108">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="17426-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="17426-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17426-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17426-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17426-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17426-111">Return value</span></span>

<span data-ttu-id="17426-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="17426-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="17426-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="17426-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="17426-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="17426-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="17426-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="17426-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="17426-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="17426-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="17426-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="17426-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="17426-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="17426-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="17426-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="17426-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="17426-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="17426-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="17426-121">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="17426-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="17426-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="17426-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="17426-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="17426-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="17426-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="17426-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="17426-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="17426-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="17426-126">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="17426-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="17426-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17426-127">Requirements</span></span>



| <span data-ttu-id="17426-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="17426-128">Requirement</span></span> | <span data-ttu-id="17426-129">Valore</span><span class="sxs-lookup"><span data-stu-id="17426-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17426-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17426-130">Minimum supported client</span></span><br/> | <span data-ttu-id="17426-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="17426-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="17426-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17426-132">Minimum supported server</span></span><br/> | <span data-ttu-id="17426-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="17426-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17426-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17426-134">Namespace</span></span><br/>                | <span data-ttu-id="17426-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="17426-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="17426-136">MOF</span><span class="sxs-lookup"><span data-stu-id="17426-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17426-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17426-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="17426-138">DLL</span><span class="sxs-lookup"><span data-stu-id="17426-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17426-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="17426-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="17426-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17426-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17426-141">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="17426-141">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="17426-142">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="17426-142">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="17426-143">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="17426-143">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="17426-144">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="17426-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

