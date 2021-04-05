---
description: Aggiorna il nome dell'elemento per l' \_ oggetto COLLECTIONOFMSES CIM specificato.
ms.assetid: 03d3979b-f3d2-4192-8bba-bdf4a19aa47c
title: Metodo renamecollection della classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RenameCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4bb127fc8fba528e883631602fcea8ba0b4de2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884610"
---
# <a name="renamecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="53361-103">Metodo rinominacollection della \_ classe MSVM CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="53361-103">RenameCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="53361-104">Aggiorna il nome dell'elemento per l' [**oggetto \_ CollectionOfMSEs CIM**](cim-collectionofmses.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="53361-104">Updates the element name for the specified [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="53361-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53361-105">Syntax</span></span>


```mof
uint32 RenameCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [in]  string                   NewName,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="53361-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="53361-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53361-107">*Raccolta* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="53361-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53361-108">Raccolta da rinominare.</span><span class="sxs-lookup"><span data-stu-id="53361-108">The collection to rename.</span></span>

</dd> <dt>

<span data-ttu-id="53361-109">*Newname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53361-109">*NewName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53361-110">Nuovo nome da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="53361-110">The new name to use.</span></span>

</dd> <dt>

<span data-ttu-id="53361-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="53361-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53361-112">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="53361-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53361-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53361-113">Return value</span></span>

<span data-ttu-id="53361-114">Restituisce 0 se ha esito positivo oppure 4096 se il processo è stato avviato. in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="53361-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="53361-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="53361-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="53361-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="53361-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="53361-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="53361-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="53361-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="53361-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="53361-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="53361-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="53361-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="53361-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="53361-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="53361-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="53361-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="53361-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="53361-123">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="53361-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="53361-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="53361-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="53361-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="53361-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="53361-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="53361-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="53361-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="53361-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="53361-128">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="53361-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="53361-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53361-129">Requirements</span></span>



| <span data-ttu-id="53361-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="53361-130">Requirement</span></span> | <span data-ttu-id="53361-131">Valore</span><span class="sxs-lookup"><span data-stu-id="53361-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53361-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53361-132">Minimum supported client</span></span><br/> | <span data-ttu-id="53361-133">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="53361-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="53361-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53361-134">Minimum supported server</span></span><br/> | <span data-ttu-id="53361-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="53361-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="53361-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="53361-136">Namespace</span></span><br/>                | <span data-ttu-id="53361-137">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="53361-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="53361-138">MOF</span><span class="sxs-lookup"><span data-stu-id="53361-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53361-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53361-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53361-140">DLL</span><span class="sxs-lookup"><span data-stu-id="53361-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53361-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53361-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53361-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53361-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53361-143">**\_CollectionManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="53361-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




