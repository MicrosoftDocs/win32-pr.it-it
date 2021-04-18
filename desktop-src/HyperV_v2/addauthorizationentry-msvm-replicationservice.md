---
description: Aggiunge una voce di autorizzazione a un server di ripristino.
ms.assetid: edc11c5b-b1a1-45e0-a920-2f1f1b0b8779
title: Metodo AddAuthorizationEntry della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.AddAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fd4c47bd4468d5804ec7e096d35db271726c92b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312347"
---
# <a name="addauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="1addb-103">Metodo AddAuthorizationEntry della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="1addb-103">AddAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="1addb-104">Aggiunge una voce di autorizzazione a un server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1addb-104">Adds an authorization entry to a recovery server.</span></span> <span data-ttu-id="1addb-105">Queste voci vengono utilizzate per autorizzare le connessioni al server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1addb-105">These entries are used for authorizing connections to the recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1addb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1addb-106">Syntax</span></span>


```mof
uint32 AddAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1addb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1addb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1addb-108">*AuthorizationEntry* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1addb-108">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1addb-109">Rappresentazione di stringa di un'istanza della classe [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) che definisce la voce di autorizzazione da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="1addb-109">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be added.</span></span>

</dd> <dt>

<span data-ttu-id="1addb-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="1addb-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1addb-111">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1addb-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1addb-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1addb-112">Return value</span></span>

<span data-ttu-id="1addb-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1addb-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1addb-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="1addb-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-115">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="1addb-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-116">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="1addb-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-117">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="1addb-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-118">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="1addb-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-119">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="1addb-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="1addb-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-121">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="1addb-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-122">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="1addb-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-123">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="1addb-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-124">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="1addb-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-125">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="1addb-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-126">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="1addb-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="1addb-127">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="1addb-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1addb-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1addb-128">Requirements</span></span>



| <span data-ttu-id="1addb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1addb-129">Requirement</span></span> | <span data-ttu-id="1addb-130">Valore</span><span class="sxs-lookup"><span data-stu-id="1addb-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1addb-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1addb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1addb-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1addb-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1addb-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1addb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1addb-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1addb-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1addb-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1addb-135">Namespace</span></span><br/>                | <span data-ttu-id="1addb-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1addb-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1addb-137">MOF</span><span class="sxs-lookup"><span data-stu-id="1addb-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1addb-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1addb-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1addb-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1addb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1addb-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1addb-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1addb-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1addb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1addb-142">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="1addb-142">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="1addb-143">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="1addb-143">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="1addb-144">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="1addb-144">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="1addb-145">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="1addb-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

