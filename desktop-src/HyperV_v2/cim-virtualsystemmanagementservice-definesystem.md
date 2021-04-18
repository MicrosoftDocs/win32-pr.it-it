---
description: Definisce un sistema virtuale.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: Metodo DefineSystem della classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e38111d52044ed385fdd8cd19dd9094834e794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310552"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="4ccef-103">Metodo DefineSystem della classe CIM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="4ccef-103">DefineSystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="4ccef-104">Definisce un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="4ccef-104">Defines a virtual system.</span></span>

<span data-ttu-id="4ccef-105">L'input non completamente specificato può essere compilato con i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="4ccef-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ccef-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ccef-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4ccef-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ccef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ccef-108">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ccef-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccef-109">Stringa contenente un'istanza incorporata della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) utilizzata per definire gli attributi del sistema virtuale da creare.</span><span class="sxs-lookup"><span data-stu-id="4ccef-109">String containing an embedded instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to define attributes of the virtual system to be created.</span></span>

</dd> <dt>

<span data-ttu-id="4ccef-110">*ResourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ccef-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccef-111">Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che descrive gli aspetti virtuali di una risorsa virtuale da creare nell'ambito del nuovo sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="4ccef-111">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be created in the scope of the new virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="4ccef-112">*ReferenceConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ccef-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccef-113">Riferimento a un'istanza di oggetto [**\_ VirtualSystemSettingDat CIM**](cim-virtualsystemsettingdata.md) che rappresenta l'oggetto di primo livello di una configurazione di sistema virtuale di riferimento.</span><span class="sxs-lookup"><span data-stu-id="4ccef-113">Reference to a [**CIM\_VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) object instance that is the top level object of a reference virtual system configuration.</span></span> <span data-ttu-id="4ccef-114">La configurazione di riferimento viene utilizzata per completare la configurazione del nuovo sistema virtuale se i parametri *SystemSettings* e *ResourceSettings* non forniscono le rispettive informazioni.</span><span class="sxs-lookup"><span data-stu-id="4ccef-114">The reference configuration is used to complement the configuration of the new virtual system if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="4ccef-115">*ResultingSystem* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4ccef-115">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccef-116">Se un sistema di computer virtuale viene definito correttamente, viene restituito un riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta il sistema di computer virtuale appena definito.</span><span class="sxs-lookup"><span data-stu-id="4ccef-116">If a virtual computer system is successfully defined, a reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the newly defined virtual computer system is returned.</span></span>

</dd> <dt>

<span data-ttu-id="4ccef-117">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4ccef-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccef-118">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo.</span><span class="sxs-lookup"><span data-stu-id="4ccef-118">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="4ccef-119">In questo caso, l'istanza della classe [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta il nuovo sistema virtuale viene presentata tramite [**Association CIM \_ AffectedJobElement**](cim-affectedjobelement.md) con la proprietà **interessata** che fa riferimento alla nuova istanza della classe **CIM \_ ComputerSystem** e la proprietà **ElementEffects** impostata su 5 (Create).</span><span class="sxs-lookup"><span data-stu-id="4ccef-119">In this case, the instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the new virtual system is presented via association [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) with the property **AffectedElement** referring to the new instance of class **CIM\_ComputerSystem** and property **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ccef-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ccef-120">Return value</span></span>

<span data-ttu-id="4ccef-121">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4ccef-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4ccef-122">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="4ccef-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ccef-123">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="4ccef-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4ccef-124">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="4ccef-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4ccef-125">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="4ccef-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4ccef-126">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="4ccef-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4ccef-127">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="4ccef-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4ccef-128">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="4ccef-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4ccef-129">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4ccef-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="4ccef-130">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="4ccef-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4ccef-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ccef-131">Requirements</span></span>



| <span data-ttu-id="4ccef-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ccef-132">Requirement</span></span> | <span data-ttu-id="4ccef-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4ccef-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ccef-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ccef-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4ccef-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4ccef-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4ccef-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ccef-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4ccef-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4ccef-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4ccef-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4ccef-138">Namespace</span></span><br/>                | <span data-ttu-id="4ccef-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4ccef-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4ccef-140">MOF</span><span class="sxs-lookup"><span data-stu-id="4ccef-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ccef-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ccef-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ccef-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4ccef-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ccef-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ccef-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ccef-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ccef-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ccef-145">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4ccef-145">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




