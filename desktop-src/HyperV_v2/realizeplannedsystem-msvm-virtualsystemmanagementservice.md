---
description: Convalida la configurazione di una macchina virtuale pianificata e la converte in una macchina virtuale realizzata.
ms.assetid: bddbdc35-4603-45c3-96b4-04f445dbb3a6
title: Metodo RealizePlannedSystem della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RealizePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fc69cbc9be9fc72bc7c1184ec30d9e2b58ba2b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233316"
---
# <a name="realizeplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a6dd2-103">Metodo RealizePlannedSystem della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="a6dd2-103">RealizePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a6dd2-104">Convalida la configurazione di una macchina virtuale pianificata e la converte in una macchina virtuale realizzata.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-104">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span> <span data-ttu-id="a6dd2-105">Eventuali file di runtime o di stato salvati associati alla macchina virtuale verranno copiati dalla directory di importazione alla radice dati della macchina virtuale, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-105">Any runtime or saved state files associated with the virtual machine will be copied from the import directory to the virtual machine's data root, if applicable.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6dd2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6dd2-106">Syntax</span></span>


```mof
uint32 RealizePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ComputerSystem         REF ResultingSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a6dd2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6dd2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6dd2-108">*PlannedSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6dd2-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6dd2-109">Riferimento all'istanza di [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) che deve essere convertita in una macchina virtuale realizzata.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-109">A reference to the [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) instance which is to be converted into a realized virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="a6dd2-110">*ResultingSystem* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a6dd2-110">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6dd2-111">Se l'operazione viene completata in modo sincrono, un riferimento a un oggetto [**\_ ComputerSystem CIM**](msvm-computersystem.md) che rappresenta la macchina virtuale realizzata risultante.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-111">If the operation is completed synchronously, a reference to a [**CIM\_ComputerSystem**](msvm-computersystem.md) object that represents the resulting realized virtual machine.</span></span>

<span data-ttu-id="a6dd2-112">DataType aggiornato da [**MSVM \_ ComputerSystem**](msvm-computersystem.md) in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-112">Datatype updated from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

</dd> <dt>

<span data-ttu-id="a6dd2-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a6dd2-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6dd2-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a6dd2-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6dd2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6dd2-115">Return value</span></span>

<span data-ttu-id="a6dd2-116">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a6dd2-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a6dd2-118">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a6dd2-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a6dd2-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a6dd2-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a6dd2-122">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a6dd2-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a6dd2-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a6dd2-125">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a6dd2-126">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a6dd2-127">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a6dd2-128">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a6dd2-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a6dd2-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="a6dd2-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="a6dd2-130">Examples</span></span>

<span data-ttu-id="a6dd2-131">Nell'esempio C# seguente viene usato il metodo **RealizePlannedSystem** per realizzare una macchina virtuale pianificata.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-131">The following C# sample uses the **RealizePlannedSystem** method to realize a planned virtual machine.</span></span> <span data-ttu-id="a6dd2-132">Questo codice è tratto dall' [esempio di macchine virtuali pianificate Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="a6dd2-132">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="a6dd2-133">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="a6dd2-133">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6dd2-134">Per funzionare correttamente, il codice seguente deve essere eseguito sul server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="a6dd2-134">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and realizes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be realized.</param>
/// <returns>The Realized Virtual Machine.</returns>
internal static ManagementObject
RealizePvm(
    string pvmName
    )
{
    ManagementObject vm = null;
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("RealizePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Realizing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("RealizePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope, true, true))
            {
                using (ManagementObject job =
                    new ManagementObject((string)outParams["Job"]))
                using (ManagementObjectCollection pvmCollection =
                    job.GetRelated("Msvm_ComputerSystem",
                        "Msvm_AffectedJobElement", null, null, null, null, false, null))
                {
                    vm = WmiUtilities.GetFirstObjectFromCollection(pvmCollection);
                }
            }
        }
    }

    return vm;
}
```



## <a name="requirements"></a><span data-ttu-id="a6dd2-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6dd2-135">Requirements</span></span>



| <span data-ttu-id="a6dd2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6dd2-136">Requirement</span></span> | <span data-ttu-id="a6dd2-137">Valore</span><span class="sxs-lookup"><span data-stu-id="a6dd2-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6dd2-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6dd2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a6dd2-139">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a6dd2-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a6dd2-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6dd2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a6dd2-141">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a6dd2-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6dd2-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6dd2-142">Namespace</span></span><br/>                | <span data-ttu-id="a6dd2-143">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a6dd2-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a6dd2-144">MOF</span><span class="sxs-lookup"><span data-stu-id="a6dd2-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6dd2-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6dd2-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6dd2-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a6dd2-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6dd2-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a6dd2-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a6dd2-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6dd2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6dd2-149">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="a6dd2-149">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

