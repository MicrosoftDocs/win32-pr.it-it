---
description: Elimina una voce di snapshot VHD all'interno di un file di set VHD.
ms.assetid: 37d55a5f-209d-42ce-8f69-8b494055e263
title: Metodo DeleteVHDSnapshot della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.DeleteVHDSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5c7f3f115825aedb3a21a8f33326a712c52e0780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307897"
---
# <a name="deletevhdsnapshot-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="74ff8-103">Metodo DeleteVHDSnapshot della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="74ff8-103">DeleteVHDSnapshot method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="74ff8-104">Elimina una voce di snapshot VHD all'interno di un file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="74ff8-104">Deletes a VHD Snapshot entry within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="74ff8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74ff8-105">Syntax</span></span>


```mof
uint32 DeleteVHDSnapshot(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotId,
  [in]  boolean             PersistReferenceSnapshot,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="74ff8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74ff8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74ff8-107">*VHDSetPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74ff8-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ff8-108">Stringa contenente il percorso del file di set VHD contenente lo snapshot in questione.</span><span class="sxs-lookup"><span data-stu-id="74ff8-108">String containing the path to the VHD Set file containing the snapshot in question.</span></span>

</dd> <dt>

<span data-ttu-id="74ff8-109">*SnapshotID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74ff8-109">*SnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ff8-110">GUID che rappresenta l'ID dello snapshot per la voce dello snapshot del disco rigido virtuale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="74ff8-110">A GUID representing the Snapshot ID for the VHD Snapshot entry to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="74ff8-111">*PersistReferenceSnapshot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74ff8-111">*PersistReferenceSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ff8-112">Indica se un record di snapshot di solo riferimento deve essere reso permanente dopo l'eliminazione dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="74ff8-112">Whether or not a reference-only snapshot record should be persisted after the snapshot is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="74ff8-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="74ff8-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74ff8-114">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="74ff8-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74ff8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74ff8-115">Return value</span></span>

<span data-ttu-id="74ff8-116">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="74ff8-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="74ff8-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="74ff8-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-118">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="74ff8-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="74ff8-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="74ff8-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="74ff8-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-122">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="74ff8-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="74ff8-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="74ff8-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-125">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="74ff8-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-126">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="74ff8-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-127">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="74ff8-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-128">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="74ff8-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="74ff8-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="74ff8-130">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="74ff8-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="74ff8-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74ff8-131">Requirements</span></span>



| <span data-ttu-id="74ff8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="74ff8-132">Requirement</span></span> | <span data-ttu-id="74ff8-133">Valore</span><span class="sxs-lookup"><span data-stu-id="74ff8-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74ff8-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74ff8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="74ff8-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="74ff8-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="74ff8-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74ff8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="74ff8-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="74ff8-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="74ff8-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="74ff8-138">Namespace</span></span><br/>                | <span data-ttu-id="74ff8-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="74ff8-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="74ff8-140">MOF</span><span class="sxs-lookup"><span data-stu-id="74ff8-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74ff8-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74ff8-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74ff8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="74ff8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74ff8-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74ff8-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74ff8-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74ff8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74ff8-145">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="74ff8-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




