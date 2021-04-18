---
description: Smonta il dispositivo PCI specificato in modo che possa essere assegnato.
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: Metodo DismountAssignableDevice della classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 53036cd09113430d1045c8e9eae7a8d782b35960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314342"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="64608-103">Metodo DismountAssignableDevice della classe MSVM \_ AssignableDeviceService</span><span class="sxs-lookup"><span data-stu-id="64608-103">DismountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="64608-104">Smonta il dispositivo PCI specificato in modo che possa essere assegnato.</span><span class="sxs-lookup"><span data-stu-id="64608-104">Dismounts the specified PCI device so that it can be assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="64608-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64608-105">Syntax</span></span>


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="64608-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="64608-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64608-107">*DismountSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64608-107">*DismountSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64608-108">Istanza incorporata di un oggetto dati di impostazione che specifica il dispositivo PCI da smontare.</span><span class="sxs-lookup"><span data-stu-id="64608-108">Embedded instance of a setting data object that specifies the PCI device to dismount.</span></span>

</dd> <dt>

<span data-ttu-id="64608-109">*DismountedDeviceInstancePath* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="64608-109">*DismountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64608-110">Stringa contenente il percorso dell'istanza del dispositivo per il dispositivo smontato.</span><span class="sxs-lookup"><span data-stu-id="64608-110">String containing the device instance path to the dismounted device.</span></span>

</dd> <dt>

<span data-ttu-id="64608-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="64608-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64608-112">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="64608-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64608-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64608-113">Return value</span></span>

<span data-ttu-id="64608-114">In caso di esito positivo, restituisce 0 o 4096; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="64608-114">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="64608-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="64608-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="64608-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="64608-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="64608-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="64608-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="64608-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="64608-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="64608-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="64608-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="64608-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="64608-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="64608-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="64608-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="64608-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="64608-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="64608-123">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="64608-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="64608-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="64608-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="64608-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="64608-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="64608-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="64608-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="64608-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="64608-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="64608-128">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="64608-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="64608-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64608-129">Requirements</span></span>



| <span data-ttu-id="64608-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="64608-130">Requirement</span></span> | <span data-ttu-id="64608-131">Valore</span><span class="sxs-lookup"><span data-stu-id="64608-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64608-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64608-132">Minimum supported client</span></span><br/> | <span data-ttu-id="64608-133">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="64608-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="64608-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64608-134">Minimum supported server</span></span><br/> | <span data-ttu-id="64608-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="64608-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="64608-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="64608-136">Namespace</span></span><br/>                | <span data-ttu-id="64608-137">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="64608-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="64608-138">MOF</span><span class="sxs-lookup"><span data-stu-id="64608-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64608-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64608-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64608-140">DLL</span><span class="sxs-lookup"><span data-stu-id="64608-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64608-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64608-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64608-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64608-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64608-143">**\_AssignableDeviceService MSVM**</span><span class="sxs-lookup"><span data-stu-id="64608-143">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




