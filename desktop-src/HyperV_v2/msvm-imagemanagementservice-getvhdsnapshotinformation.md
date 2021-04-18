---
description: Recupera le informazioni su uno snapshot del disco rigido virtuale all'interno di un file di set VHD.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Metodo GetVHDSnapshotInformation della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 85ea18e2be5329345ba49f4956307c4b29134ed6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307895"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="6e1ab-103">Metodo GetVHDSnapshotInformation della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="6e1ab-103">GetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="6e1ab-104">Recupera le informazioni su uno snapshot del disco rigido virtuale all'interno di un file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="6e1ab-104">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e1ab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e1ab-105">Syntax</span></span>


```mof
uint32 GetVHDSnapshotInformation(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotIds[],
  [in]  uint32              AdditionalInformation[],
  [out] string              SnapshotInformation[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6e1ab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e1ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e1ab-107">*VHDSetPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e1ab-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e1ab-108">Percorso completo che specifica il percorso del file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="6e1ab-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="6e1ab-109">*SnapshotIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e1ab-109">*SnapshotIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e1ab-110">Elenco di GUID che rappresentano gli ID snapshot di ogni snapshot per cui vengono richieste informazioni.</span><span class="sxs-lookup"><span data-stu-id="6e1ab-110">A list of GUIDs representing the Snapshot Ids of each Snapshot for which information is being requested.</span></span> <span data-ttu-id="6e1ab-111">Se questo parametro è NULL, verranno recuperate le informazioni per tutti gli snapshot.</span><span class="sxs-lookup"><span data-stu-id="6e1ab-111">If this parameter is NULL, information for all Snapshots will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="6e1ab-112">*AdditionalInformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e1ab-112">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e1ab-113">Matrice che specifica le informazioni aggiuntive da raccogliere per ogni snapshot del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e1ab-113">An array specifying what additional information should be gathered about each VHD Snapshot.</span></span> <span data-ttu-id="6e1ab-114">Ogni voce nella matrice è un tipo di informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="6e1ab-114">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="6e1ab-115">Se questo parametro è NULL, non verranno recuperate informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="6e1ab-115">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6e1ab-116">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6e1ab-117">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

<span data-ttu-id="6e1ab-118">**Percorsi padre** (2)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-118">**Parent Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="6e1ab-119">*SnapshotInformation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e1ab-119">*SnapshotInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e1ab-120">In caso di esito positivo, una matrice di informazioni su ogni snapshot richiesto.</span><span class="sxs-lookup"><span data-stu-id="6e1ab-120">If successful, an array of information about each requested snapshot.</span></span> <span data-ttu-id="6e1ab-121">Ogni elemento è un'istanza incorporata di [**MSVM \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span><span class="sxs-lookup"><span data-stu-id="6e1ab-121">Each element is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e1ab-122">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="6e1ab-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e1ab-123">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="6e1ab-123">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e1ab-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e1ab-124">Return value</span></span>

<span data-ttu-id="6e1ab-125">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6e1ab-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6e1ab-126">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-127">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-128">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-128">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-129">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-129">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-130">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-130">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-131">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-131">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-132">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-132">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-133">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-133">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-134">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-134">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-135">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-135">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-136">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-136">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-137">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-137">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-138">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-138">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ab-139">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="6e1ab-139">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6e1ab-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e1ab-140">Requirements</span></span>



| <span data-ttu-id="6e1ab-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e1ab-141">Requirement</span></span> | <span data-ttu-id="6e1ab-142">Valore</span><span class="sxs-lookup"><span data-stu-id="6e1ab-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e1ab-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e1ab-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6e1ab-144">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6e1ab-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6e1ab-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e1ab-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6e1ab-146">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6e1ab-146">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6e1ab-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6e1ab-147">Namespace</span></span><br/>                | <span data-ttu-id="6e1ab-148">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6e1ab-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6e1ab-149">MOF</span><span class="sxs-lookup"><span data-stu-id="6e1ab-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e1ab-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e1ab-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e1ab-151">DLL</span><span class="sxs-lookup"><span data-stu-id="6e1ab-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e1ab-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e1ab-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6e1ab-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e1ab-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e1ab-154">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="6e1ab-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




