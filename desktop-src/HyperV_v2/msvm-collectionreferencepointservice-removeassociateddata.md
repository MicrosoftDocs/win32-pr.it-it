---
description: 'Metodo RemoveAssociatedData della Msvm_CollectionReferencePointService: rimuove il log dei dati associato al punto di riferimento.'
ms.assetid: 42242b76-9123-41a7-b8b1-82d2e827ea53
title: Metodo RemoveAssociatedData della classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66a5cf068545f31f9919a9da60a1b09b32f78e4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119229"
---
# <a name="removeassociateddata-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="6a40e-103">Metodo RemoveAssociatedData della classe Msvm \_ CollectionReferencePointService</span><span class="sxs-lookup"><span data-stu-id="6a40e-103">RemoveAssociatedData method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="6a40e-104">Rimuove il log di dati associato al punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="6a40e-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a40e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a40e-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6a40e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a40e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a40e-107">*AffectedReferencePointCollection* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6a40e-107">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a40e-108">Riferimento alla raccolta di punti di riferimento del sistema virtuale interessata.</span><span class="sxs-lookup"><span data-stu-id="6a40e-108">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="6a40e-109">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="6a40e-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a40e-110">Se l'operazione è a esecuzione lunga, facoltativamente può essere restituito un processo.</span><span class="sxs-lookup"><span data-stu-id="6a40e-110">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a40e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a40e-111">Return value</span></span>

<span data-ttu-id="6a40e-112">In caso di esito positivo, restituisce 0 (nessun errore) o 4096 (processo avviato); In caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="6a40e-112">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="6a40e-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="6a40e-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6a40e-114">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="6a40e-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6a40e-115">**Operazione non** riuscita (2)</span><span class="sxs-lookup"><span data-stu-id="6a40e-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6a40e-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="6a40e-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6a40e-117">**Parametro non** valido (4)</span><span class="sxs-lookup"><span data-stu-id="6a40e-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6a40e-118">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="6a40e-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6a40e-119">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="6a40e-119">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6a40e-120">**DmTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6a40e-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6a40e-121">**Parametri del metodo controllati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="6a40e-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6a40e-122">**Metodo riservato** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="6a40e-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6a40e-123">**Specifico del** fornitore (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="6a40e-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6a40e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a40e-124">Requirements</span></span>



| <span data-ttu-id="6a40e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a40e-125">Requirement</span></span> | <span data-ttu-id="6a40e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="6a40e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a40e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a40e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6a40e-128">Windows 10 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6a40e-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6a40e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a40e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6a40e-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6a40e-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6a40e-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6a40e-131">Namespace</span></span><br/>                | <span data-ttu-id="6a40e-132">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6a40e-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6a40e-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6a40e-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a40e-134"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a40e-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a40e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6a40e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a40e-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a40e-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6a40e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a40e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a40e-138">**Msvm \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="6a40e-138">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




