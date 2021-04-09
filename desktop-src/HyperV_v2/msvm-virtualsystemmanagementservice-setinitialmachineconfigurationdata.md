---
description: Imposta i dati di configurazione iniziali della macchina virtuale.
ms.assetid: 0f174d29-ddb2-4a8c-b664-926245573778
title: Metodo SetInitialMachineConfigurationData della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetInitialMachineConfigurationData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08028358d6bb53406abe15c88e0acd02e748d387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750178"
---
# <a name="setinitialmachineconfigurationdata-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="e8856-103">Metodo SetInitialMachineConfigurationData della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="e8856-103">SetInitialMachineConfigurationData method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="e8856-104">Imposta i dati di configurazione iniziale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e8856-104">Sets a VM's initial machine configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8856-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8856-105">Syntax</span></span>


```mof
uint32 SetInitialMachineConfigurationData(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  uint8                  ImcData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e8856-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8856-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8856-107">*TargetSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8856-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8856-108">Riferimento al sistema virtuale in cui verranno impostati i dati IMC.</span><span class="sxs-lookup"><span data-stu-id="e8856-108">A reference to the virtual computer system on which the IMC data will be set.</span></span>

</dd> <dt>

<span data-ttu-id="e8856-109">*Imcdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8856-109">*ImcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8856-110">Dati IMC da impostare.</span><span class="sxs-lookup"><span data-stu-id="e8856-110">The IMC data to set.</span></span> <span data-ttu-id="e8856-111">I primi quattro byte devono essere la lunghezza della matrice nell'ordine big-endian</span><span class="sxs-lookup"><span data-stu-id="e8856-111">The first four bytes must be the length of the array in big-endian order</span></span>

</dd> <dt>

<span data-ttu-id="e8856-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="e8856-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8856-113">Parametro facoltativo per il monitoraggio dello stato di avanzamento dell'operazione, che viene utilizzato se non è stato possibile eseguire in modo sincrono il metodo.</span><span class="sxs-lookup"><span data-stu-id="e8856-113">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="e8856-114">Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.</span><span class="sxs-lookup"><span data-stu-id="e8856-114">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8856-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8856-115">Return value</span></span>

<span data-ttu-id="e8856-116">In caso di esito positivo, restituisce 0 o 4096; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e8856-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e8856-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="e8856-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e8856-118">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="e8856-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e8856-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="e8856-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e8856-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="e8856-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e8856-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="e8856-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e8856-122">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="e8856-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e8856-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="e8856-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e8856-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e8856-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e8856-125">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e8856-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e8856-126">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="e8856-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e8856-127">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e8856-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e8856-128">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="e8856-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e8856-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e8856-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e8856-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8856-130">Requirements</span></span>



| <span data-ttu-id="e8856-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8856-131">Requirement</span></span> | <span data-ttu-id="e8856-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e8856-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8856-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8856-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e8856-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e8856-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e8856-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8856-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e8856-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e8856-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e8856-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e8856-137">Namespace</span></span><br/>                | <span data-ttu-id="e8856-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e8856-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e8856-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e8856-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8856-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8856-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8856-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e8856-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8856-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e8856-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e8856-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8856-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8856-144">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="e8856-144">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




