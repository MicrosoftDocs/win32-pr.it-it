---
description: 'Metodo ModifyResourceSettings della classe Msvm_VirtualSystemManagementService: modifica le impostazioni delle risorse virtuali.'
ms.assetid: 3fb2a65f-9f40-4eb9-99e8-8fe1451427d9
title: Metodo ModifyResourceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 09ca0bb9fea02b6acc5599d9f907b1e60fdbd9ec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119339"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6deb3-103">Metodo ModifyResourceSettings della classe Msvm \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="6deb3-103">ModifyResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6deb3-104">Modifica le impostazioni delle risorse virtuali.</span><span class="sxs-lookup"><span data-stu-id="6deb3-104">Modifies virtual resource settings.</span></span> <span data-ttu-id="6deb3-105">Se applicato a parti di una configurazione di macchina virtuale corrente, come effetto collaterale, le risorse della macchina virtuale attiva possono essere modificate.</span><span class="sxs-lookup"><span data-stu-id="6deb3-105">When applied to parts of a current virtual machine configuration, as a side effect, the resources of the active virtual machine may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="6deb3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6deb3-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6deb3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6deb3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6deb3-108">*ResourceSettings* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6deb3-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6deb3-109">Matrice di stringhe che contengono un'istanza incorporata di una classe derivata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), che contengono gli aspetti modificati delle risorse virtuali esistenti.</span><span class="sxs-lookup"><span data-stu-id="6deb3-109">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="6deb3-110">La **proprietà InstanceID** di ogni istanza identifica l'impostazione della risorsa virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="6deb3-110">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="6deb3-111">*ResultingResourceSettings* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="6deb3-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6deb3-112">Matrice di riferimenti a istanze di oggetti derivati da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che rappresentano gli aspetti virtuali delle risorse virtuali modificate.</span><span class="sxs-lookup"><span data-stu-id="6deb3-112">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="6deb3-113">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="6deb3-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6deb3-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6deb3-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6deb3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6deb3-115">Return value</span></span>

<span data-ttu-id="6deb3-116">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6deb3-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6deb3-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="6deb3-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6deb3-118">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="6deb3-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6deb3-119">**Operazione non** riuscita (2)</span><span class="sxs-lookup"><span data-stu-id="6deb3-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6deb3-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="6deb3-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6deb3-121">**Parametro non** valido (4)</span><span class="sxs-lookup"><span data-stu-id="6deb3-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6deb3-122">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="6deb3-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6deb3-123">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="6deb3-123">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6deb3-124">**DmTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="6deb3-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6deb3-125">**Parametri del metodo verificati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="6deb3-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6deb3-126">**Metodo riservato** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="6deb3-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6deb3-127">**Specifico del** fornitore (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="6deb3-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6deb3-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6deb3-128">Requirements</span></span>



| <span data-ttu-id="6deb3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6deb3-129">Requirement</span></span> | <span data-ttu-id="6deb3-130">Valore</span><span class="sxs-lookup"><span data-stu-id="6deb3-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6deb3-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6deb3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6deb3-132">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6deb3-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6deb3-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6deb3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6deb3-134">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="6deb3-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6deb3-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6deb3-135">Namespace</span></span><br/>                | <span data-ttu-id="6deb3-136">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="6deb3-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6deb3-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6deb3-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6deb3-138"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="6deb3-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6deb3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6deb3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6deb3-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6deb3-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6deb3-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6deb3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6deb3-142">**ModifyVirtualSystemResources (V1)**</span><span class="sxs-lookup"><span data-stu-id="6deb3-142">**ModifyVirtualSystemResources (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="6deb3-143">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="6deb3-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

