---
description: Recupera le informazioni su un file di set VHD.
ms.assetid: efdfd4c6-b762-4369-add3-e152652c6802
title: Metodo GetVHDSetInformation della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSetInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cdcf4a354e6d6b47b6a67c071daf8883905f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307896"
---
# <a name="getvhdsetinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="9df9b-103">Metodo GetVHDSetInformation della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="9df9b-103">GetVHDSetInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="9df9b-104">Recupera le informazioni su un file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="9df9b-104">Retrieves information about a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9df9b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9df9b-105">Syntax</span></span>


```mof
uint32 GetVHDSetInformation(
  [in]  string              VHDSetPath,
  [in]  uint32              AdditionalInformation[],
  [out] string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9df9b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9df9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9df9b-107">*VHDSetPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9df9b-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9df9b-108">Percorso completo che specifica il percorso del file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="9df9b-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="9df9b-109">*AdditionalInformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9df9b-109">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9df9b-110">Matrice che specifica le informazioni aggiuntive da raccogliere sul file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="9df9b-110">An array specifying what additional information should be gathered about the VHD Set file.</span></span> <span data-ttu-id="9df9b-111">Ogni voce nella matrice è un tipo di informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="9df9b-111">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="9df9b-112">Se questo parametro è NULL, non verranno recuperate informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="9df9b-112">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9df9b-113">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="9df9b-113">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9df9b-114">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9df9b-114">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Paths"></span><span id="paths"></span><span id="PATHS"></span>

<span data-ttu-id="9df9b-115">**Percorsi** (2)</span><span class="sxs-lookup"><span data-stu-id="9df9b-115">**Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="9df9b-116">*Informazioni* \[ su out\]</span><span class="sxs-lookup"><span data-stu-id="9df9b-116">*Information* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9df9b-117">In caso di esito positivo, questo oggetto contiene le informazioni per il file di set VHD richiesto.</span><span class="sxs-lookup"><span data-stu-id="9df9b-117">If successful, this object contains the information for the requested VHD Set file.</span></span> <span data-ttu-id="9df9b-118">Si tratta di un'istanza incorporata di [**MSVM \_ VHDSetInformation**](msvm-vhdsetinformation.md).</span><span class="sxs-lookup"><span data-stu-id="9df9b-118">This is an embedded instance of [**Msvm\_VHDSetInformation**](msvm-vhdsetinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="9df9b-119">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="9df9b-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9df9b-120">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="9df9b-120">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9df9b-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9df9b-121">Return value</span></span>

<span data-ttu-id="9df9b-122">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="9df9b-122">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="9df9b-123">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="9df9b-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="9df9b-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-125">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="9df9b-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-126">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="9df9b-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-127">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="9df9b-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-128">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="9df9b-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-129">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="9df9b-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-130">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="9df9b-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-131">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="9df9b-131">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-132">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="9df9b-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-133">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="9df9b-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-134">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="9df9b-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-135">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="9df9b-135">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="9df9b-136">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="9df9b-136">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9df9b-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9df9b-137">Requirements</span></span>



| <span data-ttu-id="9df9b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9df9b-138">Requirement</span></span> | <span data-ttu-id="9df9b-139">Valore</span><span class="sxs-lookup"><span data-stu-id="9df9b-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9df9b-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9df9b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9df9b-141">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9df9b-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9df9b-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9df9b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9df9b-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9df9b-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9df9b-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9df9b-144">Namespace</span></span><br/>                | <span data-ttu-id="9df9b-145">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="9df9b-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9df9b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="9df9b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9df9b-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9df9b-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9df9b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="9df9b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9df9b-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9df9b-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9df9b-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9df9b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9df9b-151">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="9df9b-151">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




