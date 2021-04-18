---
description: Recupera un errore a causa di un processo non riuscito.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: Metodo GetError della classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aa9ed87f2d484286d91d14c4183d2ce3b6f41cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308369"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a><span data-ttu-id="a0b5a-103">Metodo GetError della classe CIM \_ ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="a0b5a-103">GetError method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="a0b5a-104">Recupera un errore a causa di un processo non riuscito.</span><span class="sxs-lookup"><span data-stu-id="a0b5a-104">Retrieves an error due to a failed job.</span></span> <span data-ttu-id="a0b5a-105">Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce alcuna istanza di [**\_ errore CIM**](cim-error.md) .</span><span class="sxs-lookup"><span data-stu-id="a0b5a-105">When the job is executing or has terminated without error, then this method returns no [**CIM\_Error**](cim-error.md) instance.</span></span> <span data-ttu-id="a0b5a-106">Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, viene restituita un'istanza di **\_ errore CIM** .</span><span class="sxs-lookup"><span data-stu-id="a0b5a-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b5a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0b5a-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="a0b5a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0b5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0b5a-109">*Errore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a0b5a-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0b5a-110">Restituisce un'istanza di [**\_ errore CIM**](cim-error.md) se il **OperationalStatus** del processo non è "OK"; in caso contrario, restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="a0b5a-110">Returns a [**CIM\_Error**](cim-error.md) instance if the **OperationalStatus** on the Job is not "OK"; otherwise, returns **null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0b5a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0b5a-111">Return value</span></span>

<span data-ttu-id="a0b5a-112">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="a0b5a-112">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a0b5a-113">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="a0b5a-113">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0b5a-114">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="a0b5a-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0b5a-115">**Errore non specificato** (2)</span><span class="sxs-lookup"><span data-stu-id="a0b5a-115">**Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0b5a-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="a0b5a-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0b5a-117">**Non riuscito** (4)</span><span class="sxs-lookup"><span data-stu-id="a0b5a-117">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0b5a-118">**Parametro non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="a0b5a-118">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a0b5a-119">**Accesso negato** (6)</span><span class="sxs-lookup"><span data-stu-id="a0b5a-119">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a0b5a-120">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="a0b5a-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0b5a-121">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a0b5a-121">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a0b5a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0b5a-122">Requirements</span></span>



| <span data-ttu-id="a0b5a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0b5a-123">Requirement</span></span> | <span data-ttu-id="a0b5a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a0b5a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b5a-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0b5a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a0b5a-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a0b5a-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a0b5a-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0b5a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a0b5a-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a0b5a-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a0b5a-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a0b5a-129">Namespace</span></span><br/>                | <span data-ttu-id="a0b5a-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a0b5a-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a0b5a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a0b5a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0b5a-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0b5a-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0b5a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a0b5a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0b5a-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0b5a-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a0b5a-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0b5a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b5a-136">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="a0b5a-136">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




