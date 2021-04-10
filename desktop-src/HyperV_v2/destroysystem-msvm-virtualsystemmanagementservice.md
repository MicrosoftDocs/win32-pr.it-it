---
description: Rimuove la macchina virtuale definita in precedenza dall'ambito di gestione del sistema host.
ms.assetid: 16E6EEB0-CB29-4FFC-AEFF-872E099337FA
title: Metodo DestroySystem della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1caf4e4a590bdbfe2f7543e23d5ca00018300fb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883718"
---
# <a name="destroysystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="81e15-103">Metodo DestroySystem della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="81e15-103">DestroySystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="81e15-104">Rimuove la macchina virtuale definita in precedenza dall'ambito di gestione del sistema host.</span><span class="sxs-lookup"><span data-stu-id="81e15-104">Removes the previously defined virtual machine from the management scope of the host system.</span></span> <span data-ttu-id="81e15-105">Verranno rimosse anche tutte le definizioni di risorse associate.</span><span class="sxs-lookup"><span data-stu-id="81e15-105">Any associated resource definitions will also be removed.</span></span> <span data-ttu-id="81e15-106">Prima di chiamare questo metodo, la macchina virtuale deve trovarsi nello stato spento o salvato.</span><span class="sxs-lookup"><span data-stu-id="81e15-106">The virtual machine must be in the powered off or saved state prior to calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e15-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81e15-107">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="81e15-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="81e15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81e15-109">*AffectedSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81e15-109">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81e15-110">Tipo: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="81e15-110">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="81e15-111">Riferimento a un'istanza del [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta l'istanza di macchina virtuale da eliminare definitivamente.</span><span class="sxs-lookup"><span data-stu-id="81e15-111">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine instance to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="81e15-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="81e15-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81e15-113">Tipo: **CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="81e15-113">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="81e15-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81e15-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81e15-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81e15-115">Return value</span></span>

<span data-ttu-id="81e15-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81e15-116">Type: **uint32**</span></span>

<span data-ttu-id="81e15-117">Se questo metodo viene eseguito in modo sincrono, restituisce 0 se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="81e15-117">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="81e15-118">Se questo metodo viene eseguito in modo asincrono, restituisce 4096 e il parametro di output del *processo* può essere usato per tenere traccia dello stato di avanzamento dell'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="81e15-118">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="81e15-119">Qualsiasi altro valore restituito indica un errore.</span><span class="sxs-lookup"><span data-stu-id="81e15-119">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="81e15-120">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="81e15-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81e15-121">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="81e15-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81e15-122">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="81e15-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81e15-123">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="81e15-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81e15-124">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="81e15-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81e15-125">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="81e15-125">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="81e15-126">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="81e15-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81e15-127">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="81e15-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="81e15-128">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="81e15-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="81e15-129">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="81e15-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="81e15-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="81e15-130">Remarks</span></span>

<span data-ttu-id="81e15-131">L'accesso alla [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="81e15-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="81e15-132">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="81e15-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="81e15-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="81e15-133">Examples</span></span>

<span data-ttu-id="81e15-134">Nell'esempio C# seguente viene usato il metodo **DestroySystem** per rimuovere una macchina virtuale pianificata.</span><span class="sxs-lookup"><span data-stu-id="81e15-134">The following C# sample uses the **DestroySystem** method to remove a planned virtual machine.</span></span> <span data-ttu-id="81e15-135">Questo codice è tratto dall' [esempio di macchine virtuali pianificate Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="81e15-135">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="81e15-136">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="81e15-136">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81e15-137">Per funzionare correttamente, il codice seguente deve essere eseguito sul server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="81e15-137">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and removes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be removed.</param>
internal static void
RemovePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("DestroySystem"))
    {
        inParams["AffectedSystem"] = pvm.Path;

        Console.WriteLine("Removing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("DestroySystem", inParams, null))
        {
            WmiUtilities.ValidateOutput(outParams, scope);
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="81e15-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81e15-138">Requirements</span></span>



| <span data-ttu-id="81e15-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="81e15-139">Requirement</span></span> | <span data-ttu-id="81e15-140">Valore</span><span class="sxs-lookup"><span data-stu-id="81e15-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81e15-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81e15-141">Minimum supported client</span></span><br/> | <span data-ttu-id="81e15-142">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="81e15-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="81e15-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81e15-143">Minimum supported server</span></span><br/> | <span data-ttu-id="81e15-144">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="81e15-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81e15-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="81e15-145">Namespace</span></span><br/>                | <span data-ttu-id="81e15-146">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="81e15-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="81e15-147">MOF</span><span class="sxs-lookup"><span data-stu-id="81e15-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81e15-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81e15-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81e15-149">DLL</span><span class="sxs-lookup"><span data-stu-id="81e15-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81e15-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81e15-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81e15-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81e15-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e15-152">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="81e15-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

