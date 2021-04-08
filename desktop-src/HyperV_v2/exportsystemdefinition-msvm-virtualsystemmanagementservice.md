---
description: Esporta in un file una macchina virtuale o uno snapshot di una macchina virtuale.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Metodo ExportSystemDefinition della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9f6b6dc5728a4275965ccd482d851601ecd1c6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749639"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="c1960-103">Metodo ExportSystemDefinition della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="c1960-103">ExportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="c1960-104">Esporta in un file una macchina virtuale o uno snapshot di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1960-104">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span> <span data-ttu-id="c1960-105">Lo stato della macchina virtuale deve essere "spento" o "salvato" per l'esportazione.</span><span class="sxs-lookup"><span data-stu-id="c1960-105">The virtual machine must be in the "powered off" or "saved" state to be exported.</span></span> <span data-ttu-id="c1960-106">La macchina virtuale, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.</span><span class="sxs-lookup"><span data-stu-id="c1960-106">The virtual machine, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1960-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1960-107">Syntax</span></span>


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c1960-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1960-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1960-109">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1960-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1960-110">Riferimento a un [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale da esportare.</span><span class="sxs-lookup"><span data-stu-id="c1960-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="c1960-111">*ExportDirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1960-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1960-112">Percorso completo della directory in cui deve essere esportata la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1960-112">The fully qualified path of the directory to which the virtual machine is to be exported.</span></span> <span data-ttu-id="c1960-113">Se la proprietà **CreateVmExportSubdirectory** della classe [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) nel parametro *ExportSettingData* è impostata su **true**, questa directory può essere riutilizzata per l'esportazione di più macchine virtuali e questo metodo inserisce ogni definizione di macchina virtuale in una sottodirectory separata in questo percorso.</span><span class="sxs-lookup"><span data-stu-id="c1960-113">If the **CreateVmExportSubdirectory** property of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class in the *ExportSettingData* parameter is set to **True**, then this directory can be reused for exporting multiple virtual machines and this method places each virtual machine definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="c1960-114">*ExportSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1960-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1960-115">Istanza incorporata della classe [**\_ VirtualSystemExportSettingData MSVM**](msvm-virtualsystemexportsettingdata.md) che rappresenta le impostazioni per l'operazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="c1960-115">An embedded instance of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="c1960-116">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c1960-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1960-117">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c1960-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1960-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1960-118">Return value</span></span>

<span data-ttu-id="c1960-119">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c1960-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c1960-120">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="c1960-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c1960-121">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="c1960-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c1960-122">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="c1960-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c1960-123">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="c1960-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c1960-124">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="c1960-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c1960-125">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="c1960-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c1960-126">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="c1960-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c1960-127">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c1960-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c1960-128">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c1960-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c1960-129">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="c1960-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c1960-130">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c1960-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c1960-131">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="c1960-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c1960-132">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c1960-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c1960-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1960-133">Requirements</span></span>



| <span data-ttu-id="c1960-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1960-134">Requirement</span></span> | <span data-ttu-id="c1960-135">Valore</span><span class="sxs-lookup"><span data-stu-id="c1960-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1960-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1960-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c1960-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c1960-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c1960-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1960-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c1960-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c1960-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1960-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c1960-140">Namespace</span></span><br/>                | <span data-ttu-id="c1960-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c1960-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c1960-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c1960-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1960-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1960-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1960-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c1960-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1960-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1960-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c1960-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1960-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1960-147">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="c1960-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

