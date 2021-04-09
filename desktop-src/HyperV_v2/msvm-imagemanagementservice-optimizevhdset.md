---
description: Ottimizza un file di set VHD in modo da utilizzare meno spazio su disco.
ms.assetid: 2d2f4531-5d2d-4334-bcc2-d3d3c15b1f46
title: Metodo OptimizeVHDSet della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.OptimizeVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c360dcd8acf0a4721b8921cd2ca914c34002d078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879578"
---
# <a name="optimizevhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="c5a4d-103">Metodo OptimizeVHDSet della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="c5a4d-103">OptimizeVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="c5a4d-104">Ottimizza un file di set VHD in modo da utilizzare meno spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="c5a4d-104">Optimizes a VHD Set file to use less disk space.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a4d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5a4d-105">Syntax</span></span>


```mof
uint32 OptimizeVHDSet(
  [in]  string              VHDSetPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c5a4d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5a4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5a4d-107">*VHDSetPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5a4d-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a4d-108">Percorso completo che specifica il percorso del file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="c5a4d-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="c5a4d-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c5a4d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5a4d-110">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="c5a4d-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5a4d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5a4d-111">Return value</span></span>

<span data-ttu-id="c5a4d-112">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5a4d-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c5a4d-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-121">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c5a4d-126">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="c5a4d-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c5a4d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5a4d-127">Requirements</span></span>



| <span data-ttu-id="c5a4d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5a4d-128">Requirement</span></span> | <span data-ttu-id="c5a4d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c5a4d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a4d-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5a4d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c5a4d-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c5a4d-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c5a4d-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5a4d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c5a4d-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c5a4d-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c5a4d-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c5a4d-134">Namespace</span></span><br/>                | <span data-ttu-id="c5a4d-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c5a4d-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c5a4d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c5a4d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5a4d-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5a4d-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5a4d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c5a4d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5a4d-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5a4d-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c5a4d-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5a4d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5a4d-141">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="c5a4d-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




