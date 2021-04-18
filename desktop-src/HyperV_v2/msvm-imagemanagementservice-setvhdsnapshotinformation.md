---
description: Modifica una voce di snapshot VHD all'interno di un file di set VHD. Se l'ID dello snapshot in questione esiste già, la voce di snapshot esistente verrà sovrascritta con la nuova voce. In caso contrario, la nuova voce verrà aggiunta al file di set VHD.
ms.assetid: dd14960d-3fb8-4d47-986f-fbbbb08eb37d
title: Metodo SetVHDSnapshotInformation della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 54f5ac23cdf8f49532a05eee3fd23293715cd02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307888"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="9914c-105">Metodo SetVHDSnapshotInformation della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="9914c-105">SetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="9914c-106">Modifica una voce di snapshot VHD all'interno di un file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="9914c-106">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="9914c-107">Se l'ID dello snapshot in questione esiste già, la voce di snapshot esistente verrà sovrascritta con la nuova voce.</span><span class="sxs-lookup"><span data-stu-id="9914c-107">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="9914c-108">In caso contrario, la nuova voce verrà aggiunta al file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="9914c-108">Otherwise, the new entry will be added to the VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9914c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9914c-109">Syntax</span></span>


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9914c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9914c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9914c-111">*Informazioni* \[ su in\]</span><span class="sxs-lookup"><span data-stu-id="9914c-111">*Information* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9914c-112">Informazioni snapshot VHD da modificare o aggiungere nel file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="9914c-112">VHD Snapshot Information to be changed or added in the VHD Set file.</span></span> <span data-ttu-id="9914c-113">La stringa è un'istanza incorporata di [**MSVM \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span><span class="sxs-lookup"><span data-stu-id="9914c-113">The string is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="9914c-114">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="9914c-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9914c-115">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="9914c-115">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9914c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9914c-116">Return value</span></span>

<span data-ttu-id="9914c-117">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="9914c-117">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="9914c-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="9914c-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-119">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="9914c-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-120">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="9914c-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="9914c-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="9914c-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-123">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="9914c-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="9914c-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-125">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="9914c-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-126">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="9914c-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-127">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="9914c-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-128">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="9914c-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-129">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="9914c-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="9914c-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="9914c-131">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="9914c-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9914c-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9914c-132">Requirements</span></span>



| <span data-ttu-id="9914c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9914c-133">Requirement</span></span> | <span data-ttu-id="9914c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="9914c-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9914c-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9914c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9914c-136">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9914c-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9914c-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9914c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9914c-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9914c-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9914c-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9914c-139">Namespace</span></span><br/>                | <span data-ttu-id="9914c-140">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="9914c-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9914c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="9914c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9914c-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9914c-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9914c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9914c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9914c-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9914c-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9914c-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9914c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9914c-146">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="9914c-146">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




