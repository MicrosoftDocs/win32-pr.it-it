---
description: Applica una raccolta snapshot alla raccolta del sistema di computer virtuale.
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Metodo ApplySnapshot della classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1fa5b664b39541b9d697dfbbfd0493f7a6f7cf96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306635"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="e78b9-103">Metodo ApplySnapshot della classe MSVM \_ CollectionSnapshotService</span><span class="sxs-lookup"><span data-stu-id="e78b9-103">ApplySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="e78b9-104">Applica una raccolta snapshot alla raccolta del sistema di computer virtuale.</span><span class="sxs-lookup"><span data-stu-id="e78b9-104">Applies a snapshot collection to the collection of virtual computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e78b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e78b9-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e78b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e78b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e78b9-107">*Snapshotcollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e78b9-107">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e78b9-108">Riferimento a una [**\_ raccolta CIM**](cim-collection.md) che rappresenta la raccolta di snapshot da applicare.</span><span class="sxs-lookup"><span data-stu-id="e78b9-108">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="e78b9-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="e78b9-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e78b9-110">Riferimento facoltativo restituito se l'operazione viene eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="e78b9-110">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="e78b9-111">Se presente, il riferimento restituito a un'istanza di [**CIM \_ ConcreteJob**](cim-concretejob.md) può essere usato per monitorare lo stato di avanzamento e per ottenere il risultato del metodo.</span><span class="sxs-lookup"><span data-stu-id="e78b9-111">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e78b9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e78b9-112">Return value</span></span>

<span data-ttu-id="e78b9-113">In caso di esito positivo, restituisce 0. in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e78b9-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e78b9-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="e78b9-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e78b9-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="e78b9-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e78b9-116">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="e78b9-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e78b9-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="e78b9-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e78b9-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="e78b9-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e78b9-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="e78b9-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e78b9-120">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="e78b9-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e78b9-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="e78b9-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e78b9-122">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="e78b9-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e78b9-123">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e78b9-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e78b9-124">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e78b9-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e78b9-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e78b9-125">Requirements</span></span>



| <span data-ttu-id="e78b9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e78b9-126">Requirement</span></span> | <span data-ttu-id="e78b9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e78b9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e78b9-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e78b9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e78b9-129">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="e78b9-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e78b9-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e78b9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e78b9-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e78b9-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e78b9-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e78b9-132">Namespace</span></span><br/>                | <span data-ttu-id="e78b9-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e78b9-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e78b9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e78b9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e78b9-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e78b9-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e78b9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e78b9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e78b9-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e78b9-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e78b9-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e78b9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e78b9-139">**\_CollectionSnapshotService MSVM**</span><span class="sxs-lookup"><span data-stu-id="e78b9-139">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




