---
description: Copia i file dall'host Hyper-V alla macchina virtuale.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: 'Metodo Msvm_GuestFileService:: CopyFilesToGuest'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9424dee6d28e0bd9cd6ac43c15ad27cdebdb7017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314354"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a><span data-ttu-id="e12ba-103">\_Metodo MSVM GuestFileService:: CopyFilesToGuest</span><span class="sxs-lookup"><span data-stu-id="e12ba-103">Msvm\_GuestFileService::CopyFilesToGuest method</span></span>

<span data-ttu-id="e12ba-104">Copia i file dall'host Hyper-V alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e12ba-104">Copies files from the Hyper-V host to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="e12ba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e12ba-105">Syntax</span></span>


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a><span data-ttu-id="e12ba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e12ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e12ba-107">*CopyFileToGuestSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e12ba-107">*CopyFileToGuestSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e12ba-108">Matrice di istanze della classe [**\_ CopyFileToGuestSettingData MSVM**](msvm-copyfiletoguestsettingdata.md) che rappresenta un processo di operazione del servizio file Guest.</span><span class="sxs-lookup"><span data-stu-id="e12ba-108">An array of instances of the [**Msvm\_CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) class that represents a guest file service operation job.</span></span>

</dd> <dt>

<span data-ttu-id="e12ba-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="e12ba-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e12ba-110">Parametro facoltativo per il monitoraggio dello stato di avanzamento dell'operazione, che viene utilizzato se non è stato possibile eseguire in modo sincrono il metodo.</span><span class="sxs-lookup"><span data-stu-id="e12ba-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="e12ba-111">Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.</span><span class="sxs-lookup"><span data-stu-id="e12ba-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="e12ba-112">Questo parametro è stato aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e12ba-112">This parameter was added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="e12ba-113">*ParentPools* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e12ba-113">*ParentPools* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e12ba-114">Matrice facoltativa di riferimenti [**MSVM \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) utilizzati per il monitoraggio dello stato di avanzamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e12ba-114">An optional array of [**Msvm\_CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) references that are used for monitoring progress of the operation.</span></span> <span data-ttu-id="e12ba-115">**CopyFilesToGuest** utilizza *ParentPools* se non può essere eseguito in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="e12ba-115">**CopyFilesToGuest** uses *ParentPools* if it can't execute synchronously.</span></span> <span data-ttu-id="e12ba-116">Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.</span><span class="sxs-lookup"><span data-stu-id="e12ba-116">If the operation executes asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="e12ba-117">Questo parametro è stato rimosso in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e12ba-117">This parameter was removed in Windows 10.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e12ba-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e12ba-118">Return value</span></span>

<span data-ttu-id="e12ba-119">In caso di esito positivo, restituisce 0; in caso contrario, restituisce un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="e12ba-119">On success, returns 0; otherwise, returns an error value.</span></span>

<dl> <dt>

<span data-ttu-id="e12ba-120">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="e12ba-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e12ba-121">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="e12ba-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e12ba-122">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="e12ba-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e12ba-123">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="e12ba-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e12ba-124">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="e12ba-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e12ba-125">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="e12ba-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e12ba-126">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="e12ba-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e12ba-127">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e12ba-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e12ba-128">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e12ba-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e12ba-129">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="e12ba-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e12ba-130">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e12ba-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e12ba-131">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="e12ba-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e12ba-132">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e12ba-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e12ba-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e12ba-133">Requirements</span></span>



| <span data-ttu-id="e12ba-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e12ba-134">Requirement</span></span> | <span data-ttu-id="e12ba-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e12ba-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e12ba-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e12ba-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e12ba-137">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e12ba-137">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e12ba-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e12ba-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e12ba-139">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e12ba-139">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e12ba-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e12ba-140">Namespace</span></span><br/>                | <span data-ttu-id="e12ba-141">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e12ba-141">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="e12ba-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e12ba-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e12ba-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e12ba-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e12ba-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e12ba-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e12ba-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e12ba-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e12ba-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e12ba-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e12ba-147">**\_GuestFileService MSVM**</span><span class="sxs-lookup"><span data-stu-id="e12ba-147">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> </dl>

 

 




