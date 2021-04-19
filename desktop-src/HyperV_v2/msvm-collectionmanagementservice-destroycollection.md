---
description: Elimina l' \_ oggetto COLLECTIONOFMSES CIM specificato.
ms.assetid: 2c79e281-44c3-4a91-98d5-fdf973d149c3
title: Metodo destroycollection della classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DestroyCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 69b35bfac3601bd92bc7b1fea967de404b716773
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319516"
---
# <a name="destroycollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="00544-103">Metodo destroycollection della \_ classe CollectionManagementService di MSVM</span><span class="sxs-lookup"><span data-stu-id="00544-103">DestroyCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="00544-104">Elimina l'oggetto [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="00544-104">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="00544-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00544-105">Syntax</span></span>


```mof
uint32 DestroyCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="00544-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00544-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00544-107">*Raccolta* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="00544-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00544-108">Raccolta da eliminare definitivamente.</span><span class="sxs-lookup"><span data-stu-id="00544-108">The collection to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="00544-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="00544-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00544-110">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="00544-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00544-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00544-111">Return value</span></span>

<span data-ttu-id="00544-112">Restituisce 0 se ha esito positivo oppure 4096 se il processo è stato avviato. in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="00544-112">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="00544-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="00544-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="00544-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="00544-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="00544-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="00544-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="00544-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="00544-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="00544-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="00544-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="00544-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="00544-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="00544-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="00544-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="00544-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="00544-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="00544-121">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="00544-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="00544-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="00544-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="00544-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="00544-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="00544-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="00544-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="00544-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="00544-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="00544-126">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="00544-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="00544-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00544-127">Requirements</span></span>



| <span data-ttu-id="00544-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="00544-128">Requirement</span></span> | <span data-ttu-id="00544-129">Valore</span><span class="sxs-lookup"><span data-stu-id="00544-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00544-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00544-130">Minimum supported client</span></span><br/> | <span data-ttu-id="00544-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="00544-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="00544-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00544-132">Minimum supported server</span></span><br/> | <span data-ttu-id="00544-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="00544-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="00544-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="00544-134">Namespace</span></span><br/>                | <span data-ttu-id="00544-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="00544-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="00544-136">MOF</span><span class="sxs-lookup"><span data-stu-id="00544-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00544-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00544-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="00544-138">DLL</span><span class="sxs-lookup"><span data-stu-id="00544-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00544-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="00544-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="00544-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00544-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00544-141">**\_CollectionManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="00544-141">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




