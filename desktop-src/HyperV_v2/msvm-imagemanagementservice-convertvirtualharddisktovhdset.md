---
description: Converte un file di disco rigido virtuale creando un nuovo file di set VHD insieme al disco rigido virtuale esistente.
ms.assetid: 04ae723e-e3c5-4640-a0e5-0e1b75bb2e6d
title: Metodo ConvertVirtualHardDiskToVHDSet della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDiskToVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6113a14f321ff7319f8be15767621db3a7e833de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968468"
---
# <a name="convertvirtualharddisktovhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="8a62f-103">Metodo ConvertVirtualHardDiskToVHDSet della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="8a62f-103">ConvertVirtualHardDiskToVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="8a62f-104">Converte un file di disco rigido virtuale creando un nuovo file di set VHD insieme al disco rigido virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="8a62f-104">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a62f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a62f-105">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDiskToVHDSet(
  [in]  string              VirtualHardDiskPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8a62f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a62f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a62f-107">*VirtualHardDiskPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a62f-107">*VirtualHardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a62f-108">Stringa contenente il percorso del file del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a62f-108">String containing the path to the virtual hard disk file.</span></span> <span data-ttu-id="8a62f-109">Il nuovo file di set VHD avrà lo stesso nome file, ma con. Estensione vhd.</span><span class="sxs-lookup"><span data-stu-id="8a62f-109">The new VHD Set file will have the same filename but with the .VHDS extension.</span></span>

</dd> <dt>

<span data-ttu-id="8a62f-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="8a62f-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a62f-111">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="8a62f-111">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a62f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a62f-112">Return value</span></span>

<span data-ttu-id="8a62f-113">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8a62f-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="8a62f-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="8a62f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-115">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="8a62f-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-116">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="8a62f-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-117">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="8a62f-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-118">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="8a62f-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-119">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="8a62f-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="8a62f-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-121">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="8a62f-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-122">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="8a62f-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-123">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="8a62f-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-124">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="8a62f-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-125">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="8a62f-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-126">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="8a62f-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="8a62f-127">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="8a62f-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8a62f-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a62f-128">Requirements</span></span>



| <span data-ttu-id="8a62f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a62f-129">Requirement</span></span> | <span data-ttu-id="8a62f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="8a62f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a62f-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a62f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8a62f-132">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8a62f-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8a62f-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a62f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8a62f-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8a62f-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8a62f-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8a62f-135">Namespace</span></span><br/>                | <span data-ttu-id="8a62f-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8a62f-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8a62f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="8a62f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a62f-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a62f-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a62f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8a62f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a62f-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a62f-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8a62f-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a62f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a62f-142">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="8a62f-142">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




