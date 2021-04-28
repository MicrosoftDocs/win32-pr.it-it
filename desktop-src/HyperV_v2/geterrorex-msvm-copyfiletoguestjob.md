---
description: 'Msvm_CopyFileToGuestJob::GetErrorEx : recupera gli oggetti errore per il processo, se presenti.'
ms.assetid: 817AF83B-B601-4AE4-AB5B-CFEACB9A7F41
title: Msvm_CopyFileToGuestJob::GetErrorEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 81a570c42457257212e83f9c0c034c4a390e4c04
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109669"
---
# <a name="msvm_copyfiletoguestjobgeterrorex-method"></a><span data-ttu-id="1010c-103">Metodo Msvm \_ CopyFileToGuestJob::GetErrorEx</span><span class="sxs-lookup"><span data-stu-id="1010c-103">Msvm\_CopyFileToGuestJob::GetErrorEx method</span></span>

<span data-ttu-id="1010c-104">Recupera gli oggetti errore per il processo, se presenti.</span><span class="sxs-lookup"><span data-stu-id="1010c-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="1010c-105">Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce alcuna [**istanza di Msvm \_ Error.**](msvm-error.md)</span><span class="sxs-lookup"><span data-stu-id="1010c-105">When the job is executing or has terminated without error, this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="1010c-106">Tuttavia, se il processo ha avuto esito negativo a causa di un problema interno o perché il processo è stato terminato da un client, vengono restituite una o più **istanze di Msvm \_ Error.**</span><span class="sxs-lookup"><span data-stu-id="1010c-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="1010c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1010c-107">Syntax</span></span>


```C++
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="1010c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1010c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1010c-109">*Errori* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="1010c-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1010c-110">Se lo stato operativo del processo non è 2 (OK), questo metodo restituisce una o più istanze incorporate della classe [**Msvm \_ Error,**](msvm-error.md) in formato CIM-XML, che rappresentano gli errori rilevati nel processo.</span><span class="sxs-lookup"><span data-stu-id="1010c-110">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="1010c-111">Se lo stato operativo del processo è 2 (OK), viene **restituito Null.**</span><span class="sxs-lookup"><span data-stu-id="1010c-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1010c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1010c-112">Return value</span></span>

<span data-ttu-id="1010c-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1010c-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1010c-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="1010c-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1010c-115">**Operazione non** riuscita (32768)</span><span class="sxs-lookup"><span data-stu-id="1010c-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1010c-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="1010c-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1010c-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="1010c-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1010c-118">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="1010c-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1010c-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="1010c-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1010c-120">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="1010c-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1010c-121">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="1010c-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1010c-122">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="1010c-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1010c-123">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="1010c-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1010c-124">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="1010c-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1010c-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="1010c-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1010c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1010c-126">Requirements</span></span>



| <span data-ttu-id="1010c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1010c-127">Requirement</span></span> | <span data-ttu-id="1010c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="1010c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1010c-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1010c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1010c-130">Windows 8.1 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1010c-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1010c-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1010c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1010c-132">Solo app desktop di Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1010c-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1010c-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1010c-133">Namespace</span></span><br/>                | <span data-ttu-id="1010c-134">\\\\Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="1010c-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="1010c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="1010c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1010c-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="1010c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1010c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1010c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1010c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1010c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1010c-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1010c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1010c-140">**Msvm \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="1010c-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




