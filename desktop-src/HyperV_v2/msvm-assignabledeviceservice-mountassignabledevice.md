---
description: Monta il dispositivo PCI specificato in modo che possa essere utilizzato dal computer host.
ms.assetid: 2a07174e-c221-4c04-81b8-5968aa67e235
title: Metodo MountAssignableDevice della classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.MountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: df5f8a337fbf4baf47a4f695322944ed0b97e82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314343"
---
# <a name="mountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="4e69c-103">Metodo MountAssignableDevice della classe MSVM \_ AssignableDeviceService</span><span class="sxs-lookup"><span data-stu-id="4e69c-103">MountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="4e69c-104">Monta il dispositivo PCI specificato in modo che possa essere utilizzato dal computer host.</span><span class="sxs-lookup"><span data-stu-id="4e69c-104">Mounts the specified PCI device so that it can be used by the host computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e69c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e69c-105">Syntax</span></span>


```mof
uint32 MountAssignableDevice(
  [in]  string              DeviceInstancePath,
  [in]  string              DeviceLocationPath,
  [out] string              MountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4e69c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e69c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e69c-107">*DeviceInstancePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e69c-107">*DeviceInstancePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e69c-108">Stringa contenente il percorso dell'istanza del dispositivo a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e69c-108">String containing the device instance path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="4e69c-109">*DeviceLocationPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e69c-109">*DeviceLocationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e69c-110">Stringa contenente il percorso del dispositivo a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e69c-110">String containing the device location path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="4e69c-111">*MountedDeviceInstancePath* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4e69c-111">*MountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e69c-112">Stringa contenente il percorso dell'istanza di dispositivo al dispositivo montato.</span><span class="sxs-lookup"><span data-stu-id="4e69c-112">String containing the device instance path to the mounted device.</span></span>

</dd> <dt>

<span data-ttu-id="4e69c-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4e69c-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e69c-114">Riferimento al processo (può essere null se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="4e69c-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e69c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e69c-115">Return value</span></span>

<span data-ttu-id="4e69c-116">In caso di esito positivo, restituisce 0 o 4096; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4e69c-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4e69c-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="4e69c-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-118">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="4e69c-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="4e69c-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="4e69c-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="4e69c-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-122">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="4e69c-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="4e69c-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="4e69c-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-125">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="4e69c-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-126">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="4e69c-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-127">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="4e69c-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-128">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="4e69c-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="4e69c-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="4e69c-130">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="4e69c-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4e69c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e69c-131">Requirements</span></span>



| <span data-ttu-id="4e69c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e69c-132">Requirement</span></span> | <span data-ttu-id="4e69c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4e69c-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e69c-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e69c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4e69c-135">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e69c-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4e69c-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e69c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4e69c-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4e69c-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4e69c-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4e69c-138">Namespace</span></span><br/>                | <span data-ttu-id="4e69c-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4e69c-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4e69c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="4e69c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e69c-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e69c-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e69c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4e69c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e69c-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4e69c-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4e69c-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e69c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e69c-145">**\_AssignableDeviceService MSVM**</span><span class="sxs-lookup"><span data-stu-id="4e69c-145">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




