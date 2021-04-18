---
description: Elimina il punto di riferimento specificato.
ms.assetid: cb5245b6-5984-40ec-a37e-e4a0a62e318a
title: Metodo DestroyReferencePoint della classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cf7a21e60369a928cc1d617e24db5f5fc70c522
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320628"
---
# <a name="destroyreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="e0751-103">Metodo DestroyReferencePoint della classe MSVM \_ VirtualSystemReferencePointService</span><span class="sxs-lookup"><span data-stu-id="e0751-103">DestroyReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="e0751-104">Elimina il punto di riferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="e0751-104">Deletes the specified reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0751-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0751-105">Syntax</span></span>


```mof
uint32 DestroyReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e0751-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0751-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0751-107">*AffectedReferencePoint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0751-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0751-108">Riferimento all'istanza di [**\_ VirtualSystemReferencePoint MSVM**](msvm-virtualsystemreferencepoint.md) che rappresenta il punto di riferimento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e0751-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="e0751-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="e0751-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0751-110">Parametro facoltativo per il monitoraggio dello stato di avanzamento dell'operazione, che viene utilizzato se non è stato possibile eseguire in modo sincrono il metodo.</span><span class="sxs-lookup"><span data-stu-id="e0751-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="e0751-111">Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.</span><span class="sxs-lookup"><span data-stu-id="e0751-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0751-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0751-112">Return value</span></span>

<span data-ttu-id="e0751-113">In caso di esito positivo, restituisce 0 (completa senza errori) o 4096 (processo avviato); in caso contrario, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="e0751-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="e0751-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="e0751-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e0751-115">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="e0751-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e0751-116">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="e0751-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e0751-117">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="e0751-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e0751-118">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="e0751-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e0751-119">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="e0751-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e0751-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="e0751-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e0751-121">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e0751-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e0751-122">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e0751-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e0751-123">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="e0751-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e0751-124">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e0751-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e0751-125">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="e0751-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e0751-126">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e0751-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e0751-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0751-127">Requirements</span></span>



| <span data-ttu-id="e0751-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0751-128">Requirement</span></span> | <span data-ttu-id="e0751-129">Valore</span><span class="sxs-lookup"><span data-stu-id="e0751-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0751-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0751-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e0751-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e0751-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e0751-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0751-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e0751-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e0751-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e0751-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e0751-134">Namespace</span></span><br/>                | <span data-ttu-id="e0751-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e0751-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e0751-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e0751-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0751-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0751-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0751-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e0751-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0751-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e0751-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e0751-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0751-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0751-141">**\_VirtualSystemReferencePointService MSVM**</span><span class="sxs-lookup"><span data-stu-id="e0751-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




