---
description: Metodo che consente di terminare il processo e tutti i processi sottostanti e di rimuovere tutte le associazioni in sospeso. Questo metodo è deprecato; in alternativa, usare RequestChangeState.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: Metodo KillJob della classe CIM_Job
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 967e5e8510d4456a085f393291f8c41afb5be446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967314"
---
# <a name="killjob-method-of-the-cim_job-class"></a><span data-ttu-id="cd37c-104">Metodo KillJob della classe di \_ processi CIM</span><span class="sxs-lookup"><span data-stu-id="cd37c-104">KillJob method of the CIM\_Job class</span></span>

<span data-ttu-id="cd37c-105">Metodo che consente di terminare il processo e tutti i processi sottostanti e di rimuovere tutte le associazioni "penzoloni".</span><span class="sxs-lookup"><span data-stu-id="cd37c-105">A method to kill this job and any underlying processes, and to remove any 'dangling' associations.</span></span> <span data-ttu-id="cd37c-106">Questo metodo è deprecato; in alternativa, usare **RequestChangeState** .</span><span class="sxs-lookup"><span data-stu-id="cd37c-106">This method is deprecated; use **RequestChangeState** instead.</span></span> <span data-ttu-id="cd37c-107">**KillJob** è stato deprecato perché non vi è alcuna distinzione tra un arresto ordinato e un kill immediato.</span><span class="sxs-lookup"><span data-stu-id="cd37c-107">**KillJob** is being deprecated because there is no distinction made between an orderly shutdown and an immediate kill.</span></span> <span data-ttu-id="cd37c-108">[**CIM \_ ConcreteJob**](cim-concretejob.md). **RequestStateChange**() fornisce le opzioni ' terminate ' è Kill ' per consentire questa distinzione.</span><span class="sxs-lookup"><span data-stu-id="cd37c-108">[**CIM\_ConcreteJob**](cim-concretejob.md).**RequestStateChange**() provides 'Terminate' and 'Kill' options to allow this distinction.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd37c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd37c-109">Syntax</span></span>


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a><span data-ttu-id="cd37c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd37c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd37c-111">*DeleteOnKill* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd37c-111">*DeleteOnKill* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd37c-112">Indica se il processo deve essere eliminato automaticamente al termine della terminazione.</span><span class="sxs-lookup"><span data-stu-id="cd37c-112">Indicates whether or not the Job should be automatically deleted upon termination.</span></span> <span data-ttu-id="cd37c-113">Questo parametro ha la precedenza sulla proprietà **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="cd37c-113">This parameter takes precedence over the **DeleteOnCompletion** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd37c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd37c-114">Return value</span></span>

<span data-ttu-id="cd37c-115">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="cd37c-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="cd37c-116">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="cd37c-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cd37c-117">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="cd37c-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cd37c-118">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="cd37c-118">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cd37c-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="cd37c-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cd37c-120">**Non riuscito** (4)</span><span class="sxs-lookup"><span data-stu-id="cd37c-120">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cd37c-121">**Accesso negato** (6)</span><span class="sxs-lookup"><span data-stu-id="cd37c-121">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="cd37c-122">**Non trovato** (7)</span><span class="sxs-lookup"><span data-stu-id="cd37c-122">**Not Found** (7)</span></span>
</dt> <dt>

<span data-ttu-id="cd37c-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="cd37c-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cd37c-124">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="cd37c-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cd37c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd37c-125">Requirements</span></span>



| <span data-ttu-id="cd37c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd37c-126">Requirement</span></span> | <span data-ttu-id="cd37c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="cd37c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd37c-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd37c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cd37c-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cd37c-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="cd37c-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd37c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cd37c-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="cd37c-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="cd37c-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd37c-132">Namespace</span></span><br/>                | <span data-ttu-id="cd37c-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="cd37c-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cd37c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cd37c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd37c-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd37c-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd37c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cd37c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd37c-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd37c-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd37c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd37c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd37c-139">**\_Processo CIM**</span><span class="sxs-lookup"><span data-stu-id="cd37c-139">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

 




