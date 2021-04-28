---
description: 'Metodo RemoveAssociatedData della Msvm_VirtualSystemReferencePointService: rimuove il log dei dati associato al punto di riferimento.'
ms.assetid: b6206bda-c195-4c6f-9b80-508c20b53ce5
title: Metodo RemoveAssociatedData della classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b5291e4e018edc89909ccde36ce0e420698af8e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118619"
---
# <a name="removeassociateddata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="19f0f-103">Metodo RemoveAssociatedData della classe Msvm \_ VirtualSystemReferencePointService</span><span class="sxs-lookup"><span data-stu-id="19f0f-103">RemoveAssociatedData method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="19f0f-104">Rimuove il log di dati associato al punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="19f0f-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="19f0f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19f0f-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="19f0f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="19f0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19f0f-107">*AffectedReferencePoint* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="19f0f-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19f0f-108">Riferimento [**all'istanza di Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) che rappresenta il punto di riferimento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="19f0f-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="19f0f-109">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="19f0f-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19f0f-110">Parametro facoltativo per il monitoraggio dello stato dell'operazione, che viene utilizzato se non è stato possibile eseguire il metodo in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="19f0f-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="19f0f-111">Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.</span><span class="sxs-lookup"><span data-stu-id="19f0f-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19f0f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19f0f-112">Return value</span></span>

<span data-ttu-id="19f0f-113">In caso di esito positivo, restituisce 0 (completo senza errori) o 4096 (processo avviato). In caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="19f0f-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="19f0f-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="19f0f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="19f0f-115">**Parametri del metodo controllati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="19f0f-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="19f0f-116">**Operazione non** riuscita (32768)</span><span class="sxs-lookup"><span data-stu-id="19f0f-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="19f0f-117">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="19f0f-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="19f0f-118">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="19f0f-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="19f0f-119">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="19f0f-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="19f0f-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="19f0f-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="19f0f-121">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="19f0f-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="19f0f-122">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="19f0f-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="19f0f-123">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="19f0f-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="19f0f-124">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="19f0f-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="19f0f-125">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="19f0f-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="19f0f-126">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="19f0f-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="19f0f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19f0f-127">Requirements</span></span>



| <span data-ttu-id="19f0f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="19f0f-128">Requirement</span></span> | <span data-ttu-id="19f0f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="19f0f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f0f-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19f0f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="19f0f-131">Windows 10 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="19f0f-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="19f0f-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19f0f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="19f0f-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="19f0f-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="19f0f-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="19f0f-134">Namespace</span></span><br/>                | <span data-ttu-id="19f0f-135">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="19f0f-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="19f0f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="19f0f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19f0f-137"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="19f0f-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="19f0f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="19f0f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19f0f-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="19f0f-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="19f0f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19f0f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19f0f-141">**Msvm \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="19f0f-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




