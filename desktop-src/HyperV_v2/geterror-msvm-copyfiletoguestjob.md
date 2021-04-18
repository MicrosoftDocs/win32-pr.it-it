---
description: Recupera l'oggetto errore per il processo, se disponibile.
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: 'Metodo Msvm_CopyFileToGuestJob:: GetError'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a0a89feab4e78ba3703e117972598c4de5f70310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307745"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a><span data-ttu-id="8eb2b-103">\_Metodo MSVM CopyFileToGuestJob:: GetError</span><span class="sxs-lookup"><span data-stu-id="8eb2b-103">Msvm\_CopyFileToGuestJob::GetError method</span></span>

<span data-ttu-id="8eb2b-104">Recupera l'oggetto errore per il processo, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="8eb2b-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="8eb2b-105">Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce un oggetto [**\_ errore CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8eb2b-105">When the job is executing or has terminated without error, this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="8eb2b-106">Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, viene restituita un'istanza di **\_ errore CIM** .</span><span class="sxs-lookup"><span data-stu-id="8eb2b-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb2b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8eb2b-107">Syntax</span></span>


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="8eb2b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8eb2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eb2b-109">*Errore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8eb2b-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8eb2b-110">Se lo stato operativo del processo non è 2 (OK), questo metodo restituisce un'istanza incorporata della classe [**di \_ errore MSVM**](msvm-error.md) in formato CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="8eb2b-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="8eb2b-111">Se lo stato operativo del processo è 2 (OK), viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="8eb2b-111">If the operational status of the job is 2 (OK), **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eb2b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8eb2b-112">Return value</span></span>

<span data-ttu-id="8eb2b-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8eb2b-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8eb2b-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="8eb2b-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8eb2b-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="8eb2b-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8eb2b-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="8eb2b-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8eb2b-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="8eb2b-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8eb2b-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="8eb2b-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8eb2b-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="8eb2b-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8eb2b-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="8eb2b-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8eb2b-121">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="8eb2b-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8eb2b-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="8eb2b-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8eb2b-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="8eb2b-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8eb2b-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="8eb2b-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8eb2b-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="8eb2b-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8eb2b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8eb2b-126">Requirements</span></span>



| <span data-ttu-id="8eb2b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eb2b-127">Requirement</span></span> | <span data-ttu-id="8eb2b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8eb2b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb2b-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8eb2b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8eb2b-130">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8eb2b-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8eb2b-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8eb2b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8eb2b-132">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8eb2b-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8eb2b-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8eb2b-133">Namespace</span></span><br/>                | <span data-ttu-id="8eb2b-134">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8eb2b-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="8eb2b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="8eb2b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8eb2b-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8eb2b-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8eb2b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8eb2b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eb2b-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8eb2b-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8eb2b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8eb2b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb2b-140">**\_CopyFileToGuestJob MSVM**</span><span class="sxs-lookup"><span data-stu-id="8eb2b-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

