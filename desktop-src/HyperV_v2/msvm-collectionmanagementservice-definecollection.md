---
description: Crea un nuovo \_ oggetto COLLECTIONOFMSES CIM.
ms.assetid: cd2a0cde-d4c6-4ba8-8140-fcc7546c1006
title: Metodo definicollection della classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DefineCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 34ab998f2b742997d588190db80bd342628a07e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317204"
---
# <a name="definecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="c15ba-103">Metodo definicollection della classe MSVM \_ CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="c15ba-103">DefineCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="c15ba-104">Crea un nuovo [**oggetto \_ CollectionOfMSEs CIM**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="c15ba-104">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c15ba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c15ba-105">Syntax</span></span>


```mof
uint32 DefineCollection(
  [in]  string                   Name,
  [in]  string                   Id,
  [in]  uint16                   Type,
  [out] CIM_CollectionOfMSEs REF DefinedCollection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c15ba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c15ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c15ba-107">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c15ba-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c15ba-108">Nome della nuova raccolta.</span><span class="sxs-lookup"><span data-stu-id="c15ba-108">The name of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="c15ba-109">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c15ba-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c15ba-110">ID della nuova raccolta.</span><span class="sxs-lookup"><span data-stu-id="c15ba-110">The ID of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="c15ba-111">*Tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c15ba-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c15ba-112">Tipo della nuova raccolta.</span><span class="sxs-lookup"><span data-stu-id="c15ba-112">The type of the new collection.</span></span>

<dt>

<span id="Collection_of_Virtual_Systems"></span><span id="collection_of_virtual_systems"></span><span id="COLLECTION_OF_VIRTUAL_SYSTEMS"></span>

<span data-ttu-id="c15ba-113">**Raccolta di sistemi virtuali** (0)</span><span class="sxs-lookup"><span data-stu-id="c15ba-113">**Collection of Virtual Systems** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Collection_of_Collections"></span><span id="collection_of_collections"></span><span id="COLLECTION_OF_COLLECTIONS"></span>

<span data-ttu-id="c15ba-114">**Raccolta di raccolte** (1)</span><span class="sxs-lookup"><span data-stu-id="c15ba-114">**Collection of Collections** (1)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="c15ba-115">*Definitocollection* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c15ba-115">*DefinedCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c15ba-116">Riferimento agli oggetti che definiscono la raccolta.</span><span class="sxs-lookup"><span data-stu-id="c15ba-116">Reference to the objects that define the collection.</span></span>

</dd> <dt>

<span data-ttu-id="c15ba-117">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c15ba-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c15ba-118">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="c15ba-118">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c15ba-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c15ba-119">Return value</span></span>

<span data-ttu-id="c15ba-120">Se ha esito positivo, restituisce 0 o 4096 (processo avviato); in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="c15ba-120">If successful, returns a 0 or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="c15ba-121">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="c15ba-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-122">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="c15ba-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-123">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="c15ba-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-124">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="c15ba-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-125">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="c15ba-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-126">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="c15ba-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-127">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="c15ba-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-128">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c15ba-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-129">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c15ba-129">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-130">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="c15ba-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-131">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c15ba-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-132">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="c15ba-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-133">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c15ba-133">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c15ba-134">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="c15ba-134">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c15ba-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c15ba-135">Requirements</span></span>



| <span data-ttu-id="c15ba-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c15ba-136">Requirement</span></span> | <span data-ttu-id="c15ba-137">Valore</span><span class="sxs-lookup"><span data-stu-id="c15ba-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c15ba-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c15ba-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c15ba-139">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c15ba-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c15ba-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c15ba-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c15ba-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c15ba-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c15ba-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c15ba-142">Namespace</span></span><br/>                | <span data-ttu-id="c15ba-143">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c15ba-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c15ba-144">MOF</span><span class="sxs-lookup"><span data-stu-id="c15ba-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c15ba-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c15ba-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c15ba-146">DLL</span><span class="sxs-lookup"><span data-stu-id="c15ba-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c15ba-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c15ba-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c15ba-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c15ba-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c15ba-149">**\_CollectionManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="c15ba-149">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




