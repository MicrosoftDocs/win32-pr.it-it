---
description: Trova un \_ oggetto MSVM MountedStorageImage per un determinato percorso di immagine disco.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Metodo FindMountedStorageImageInstance della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526833"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="0d2fb-103">Metodo FindMountedStorageImageInstance della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="0d2fb-103">FindMountedStorageImageInstance method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="0d2fb-104">Trova un oggetto [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) per un determinato percorso di immagine disco.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-104">Finds an [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) object for a given disk image path.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d2fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d2fb-105">Syntax</span></span>


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a><span data-ttu-id="0d2fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d2fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d2fb-107">*SelectionCriterion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d2fb-107">*SelectionCriterion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d2fb-108">Percorso completo che specifica il percorso di un file di immagine disco.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-108">A fully-qualified path that specifies the location of a disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="0d2fb-109">*CriterionType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d2fb-109">*CriterionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d2fb-110">Tipo di criterio da cercare quando si trova l'immagine del disco.</span><span class="sxs-lookup"><span data-stu-id="0d2fb-110">The type of criterion to look for when finding the disk image.</span></span>

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d2fb-111">**sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-111">**unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

<span data-ttu-id="0d2fb-112">**Percorso** (2)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-112">**Path** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="0d2fb-113">*Immagine* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="0d2fb-113">*Image* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d2fb-114">Riferimento a [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) (può essere null se l'immagine non è montata).</span><span class="sxs-lookup"><span data-stu-id="0d2fb-114">A reference to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) (can be null if the image is not mounted).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d2fb-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d2fb-115">Return value</span></span>

<span data-ttu-id="0d2fb-116">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d2fb-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="0d2fb-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-124">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-129">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="0d2fb-130">**Oggetto non trovato** (32789)</span><span class="sxs-lookup"><span data-stu-id="0d2fb-130">**Object not found** (32789)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0d2fb-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d2fb-131">Requirements</span></span>



| <span data-ttu-id="0d2fb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d2fb-132">Requirement</span></span> | <span data-ttu-id="0d2fb-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0d2fb-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d2fb-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d2fb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0d2fb-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0d2fb-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0d2fb-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d2fb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0d2fb-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0d2fb-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0d2fb-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0d2fb-138">Namespace</span></span><br/>                | <span data-ttu-id="0d2fb-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0d2fb-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0d2fb-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0d2fb-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d2fb-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d2fb-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d2fb-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0d2fb-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d2fb-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d2fb-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0d2fb-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d2fb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d2fb-145">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="0d2fb-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




