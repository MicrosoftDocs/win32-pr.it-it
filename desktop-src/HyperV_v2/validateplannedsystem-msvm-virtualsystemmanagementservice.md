---
description: Convalida il sistema pianificato specificato.
ms.assetid: cb969b38-f36d-4c70-b234-590f1c219d22
title: Metodo ValidatePlannedSystem della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ValidatePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 96137c3774291e06bfffdea3843658a427e36950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759047"
---
# <a name="validateplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="ff010-103">Metodo ValidatePlannedSystem della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="ff010-103">ValidatePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ff010-104">Convalida il sistema pianificato specificato.</span><span class="sxs-lookup"><span data-stu-id="ff010-104">Validates the specified planned system.</span></span> <span data-ttu-id="ff010-105">Ciò comporta controlli della configurazione della macchina virtuale, dei dispositivi, della configurazione dello snapshot, dei dispositivi snapshot, dei file di stato salvati e dei file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ff010-105">This involves checks of the virtual machine configuration, devices, snapshot configuration, snapshot devices, saved state files and storage files.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff010-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff010-106">Syntax</span></span>


```mof
uint32 ValidatePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ff010-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff010-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff010-108">*PlannedSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff010-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff010-109">Riferimento a un oggetto [**\_ PlannedComputerSystem MSVM**](msvm-plannedcomputersystem.md) che rappresenta il sistema pianificato da convalidare.</span><span class="sxs-lookup"><span data-stu-id="ff010-109">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned system to be validated.</span></span>

</dd> <dt>

<span data-ttu-id="ff010-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ff010-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff010-111">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ff010-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff010-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff010-112">Return value</span></span>

<span data-ttu-id="ff010-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ff010-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ff010-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ff010-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-115">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="ff010-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-116">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="ff010-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-117">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="ff010-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-118">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="ff010-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-119">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="ff010-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ff010-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-121">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ff010-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-122">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ff010-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-123">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="ff010-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-124">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ff010-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-125">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="ff010-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-126">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ff010-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ff010-127">**File in uso** (32779)</span><span class="sxs-lookup"><span data-stu-id="ff010-127">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="ff010-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="ff010-128">Examples</span></span>

<span data-ttu-id="ff010-129">Nell'esempio C# seguente viene usato il metodo **ValidatePlannedSystem** per convalidare una macchina virtuale pianificata.</span><span class="sxs-lookup"><span data-stu-id="ff010-129">The following C# sample uses the **ValidatePlannedSystem** method to validate a planned virtual machine.</span></span> <span data-ttu-id="ff010-130">Questo codice è tratto dall' [esempio di macchine virtuali pianificate Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="ff010-130">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="ff010-131">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="ff010-131">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff010-132">Per funzionare correttamente, il codice seguente deve essere eseguito sul server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="ff010-132">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and validates it, displaying
/// any warnings produced.
/// </summary>
/// <param name="pvmName">The name of the PVM to be validated.</param>
internal static void
ValidatePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams = 
        managementService.GetMethodParameters("ValidatePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Validating Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams = 
            managementService.InvokeMethod("ValidatePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope))
            {
                using (ManagementObject job = 
                    new ManagementObject((string)outParams["Job"]))
                {
                    WmiUtilities.PrintMsvmErrors(job);
                }
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="ff010-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff010-133">Requirements</span></span>



| <span data-ttu-id="ff010-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff010-134">Requirement</span></span> | <span data-ttu-id="ff010-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ff010-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff010-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff010-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ff010-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ff010-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ff010-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff010-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ff010-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ff010-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff010-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ff010-140">Namespace</span></span><br/>                | <span data-ttu-id="ff010-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ff010-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ff010-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ff010-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff010-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff010-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff010-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ff010-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff010-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ff010-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ff010-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff010-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff010-147">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="ff010-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

