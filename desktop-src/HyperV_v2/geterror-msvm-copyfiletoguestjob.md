---
description: "Msvm_CopyFileToGuestJob::GetError : recupera l'oggetto errore per il processo, se esistente."
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: Msvm_CopyFileToGuestJob::GetError
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
ms.openlocfilehash: c7cecaf7254788ae064ca42f2ae0c26e8ad83d7e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119369"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a><span data-ttu-id="919f2-103">Metodo \_ Msvm CopyFileToGuestJob::GetError</span><span class="sxs-lookup"><span data-stu-id="919f2-103">Msvm\_CopyFileToGuestJob::GetError method</span></span>

<span data-ttu-id="919f2-104">Recupera l'oggetto errore per il processo, se esistente.</span><span class="sxs-lookup"><span data-stu-id="919f2-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="919f2-105">Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce un [**oggetto \_ Errore CIM.**](/previous-versions//cc150671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="919f2-105">When the job is executing or has terminated without error, this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="919f2-106">Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, viene restituita un'istanza **\_ Di errore CIM.**</span><span class="sxs-lookup"><span data-stu-id="919f2-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="919f2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="919f2-107">Syntax</span></span>


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="919f2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="919f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="919f2-109">*Errore* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="919f2-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="919f2-110">Se lo stato operativo del processo non è 2 (OK), questo metodo restituisce un'istanza incorporata della [**classe Msvm \_ Error,**](msvm-error.md) in formato CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="919f2-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="919f2-111">Se lo stato operativo del processo è 2 (OK), **viene restituito** Null.</span><span class="sxs-lookup"><span data-stu-id="919f2-111">If the operational status of the job is 2 (OK), **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="919f2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="919f2-112">Return value</span></span>

<span data-ttu-id="919f2-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="919f2-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="919f2-114">**Completata senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="919f2-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="919f2-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="919f2-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="919f2-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="919f2-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="919f2-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="919f2-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="919f2-118">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="919f2-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="919f2-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="919f2-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="919f2-120">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="919f2-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="919f2-121">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="919f2-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="919f2-122">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="919f2-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="919f2-123">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="919f2-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="919f2-124">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="919f2-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="919f2-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="919f2-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="919f2-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="919f2-126">Requirements</span></span>



| <span data-ttu-id="919f2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="919f2-127">Requirement</span></span> | <span data-ttu-id="919f2-128">Valore</span><span class="sxs-lookup"><span data-stu-id="919f2-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="919f2-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="919f2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="919f2-130">Windows 8.1 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="919f2-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="919f2-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="919f2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="919f2-132">Solo app desktop di Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="919f2-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="919f2-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="919f2-133">Namespace</span></span><br/>                | <span data-ttu-id="919f2-134">\\\\Virtualizzazione \\ radice \\ V2</span><span class="sxs-lookup"><span data-stu-id="919f2-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="919f2-135">MOF</span><span class="sxs-lookup"><span data-stu-id="919f2-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="919f2-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="919f2-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="919f2-137">DLL</span><span class="sxs-lookup"><span data-stu-id="919f2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="919f2-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="919f2-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="919f2-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="919f2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="919f2-140">**Msvm \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="919f2-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

