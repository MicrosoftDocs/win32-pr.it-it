---
description: Ottiene un elenco di \_ istanze di CompatibilityVector MSVM che possono essere usate per verificare la compatibilità della macchina virtuale (VM) con l'host.
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: 'Metodo Msvm_VirtualSystemMigrationService:: GetSystemCompatibilityVectors'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ef8a374d992468247f6dc8f914d7252e7cd2829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966502"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a><span data-ttu-id="ac8a2-103">\_Metodo MSVM VirtualSystemMigrationService:: GetSystemCompatibilityVectors</span><span class="sxs-lookup"><span data-stu-id="ac8a2-103">Msvm\_VirtualSystemMigrationService::GetSystemCompatibilityVectors method</span></span>

<span data-ttu-id="ac8a2-104">Ottiene un elenco di istanze di [**\_ CompatibilityVector MSVM**](msvm-compatibilityvector.md) che possono essere usate per verificare la compatibilità della macchina virtuale (VM) con l'host.</span><span class="sxs-lookup"><span data-stu-id="ac8a2-104">Gets a list of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that can be used to check for virtual machine (VM) to host compatibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac8a2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac8a2-105">Syntax</span></span>


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a><span data-ttu-id="ac8a2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac8a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac8a2-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac8a2-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac8a2-108">Riferimento a una classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale per cui recuperare i vettori di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="ac8a2-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the VM to retrieve compatibility vectors for.</span></span> <span data-ttu-id="ac8a2-109">Se questo parametro fa riferimento al sistema del computer host, i dati restituiti nel parametro *CompatibilityVectors* possono essere usati per determinare se è possibile eseguire rapidamente la migrazione di una o più macchine virtuali nel computer host a un altro computer host.</span><span class="sxs-lookup"><span data-stu-id="ac8a2-109">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityVectors* parameter can be used to determine whether any of the VMs on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="ac8a2-110">*CompatibilityVectors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ac8a2-110">*CompatibilityVectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac8a2-111">Matrice di istanze [**di \_ CompatibilityVector MSVM**](msvm-compatibilityvector.md) che contengono le informazioni sulla compatibilità per le macchine virtuali o il computer host.</span><span class="sxs-lookup"><span data-stu-id="ac8a2-111">An array of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that contain the compatibility info for the VMs or hosting computer system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac8a2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac8a2-112">Return value</span></span>

<span data-ttu-id="ac8a2-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ac8a2-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ac8a2-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ac8a2-115">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ac8a2-116">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ac8a2-117">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ac8a2-118">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ac8a2-119">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ac8a2-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ac8a2-121">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ac8a2-122">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ac8a2-123">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ac8a2-124">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ac8a2-125">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ac8a2-126">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ac8a2-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ac8a2-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac8a2-127">Remarks</span></span>

<span data-ttu-id="ac8a2-128">**GetSystemCompatibilityVectors** ottiene le informazioni sulla compatibilità per una macchina virtuale (VM) (quando viene eseguita in un computer VM) o un host (quando viene eseguito in un computer host).</span><span class="sxs-lookup"><span data-stu-id="ac8a2-128">**GetSystemCompatibilityVectors** gets compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span> <span data-ttu-id="ac8a2-129">Le informazioni sulla compatibilità rimangono opache per il client mentre le informazioni consentono di confrontare le informazioni di compatibilità dell'host con quelle della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ac8a2-129">The compatibility info remains opaque to the client while the info provides a way to compare the host compatibility info with that of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac8a2-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac8a2-130">Requirements</span></span>



| <span data-ttu-id="ac8a2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac8a2-131">Requirement</span></span> | <span data-ttu-id="ac8a2-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ac8a2-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac8a2-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac8a2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ac8a2-134">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ac8a2-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ac8a2-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac8a2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ac8a2-136">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac8a2-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ac8a2-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ac8a2-137">Namespace</span></span><br/>                | <span data-ttu-id="ac8a2-138">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ac8a2-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="ac8a2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ac8a2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac8a2-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac8a2-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac8a2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ac8a2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac8a2-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac8a2-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ac8a2-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac8a2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac8a2-144">**\_CompatibilityVector MSVM**</span><span class="sxs-lookup"><span data-stu-id="ac8a2-144">**Msvm\_CompatibilityVector**</span></span>](msvm-compatibilityvector.md)
</dt> <dt>

[<span data-ttu-id="ac8a2-145">**\_VirtualSystemMigrationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="ac8a2-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




