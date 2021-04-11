---
description: Crea uno snapshot di una macchina virtuale.
ms.assetid: 2de12fe7-5ec2-49d0-87ff-cd48c34fec46
title: Metodo CreateSnapshot della classe Msvm_VirtualSystemSnapshotService (DBDAOINT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c62b4abf60e367da1c4ac4b176e5f5d70f547c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346366"
---
# <a name="createsnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="d1c69-103">Metodo CreateSnapshot della classe MSVM \_ VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="d1c69-103">CreateSnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="d1c69-104">Crea uno snapshot di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1c69-104">Creates a snapshot of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c69-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1c69-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d1c69-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1c69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c69-107">*AffectedSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1c69-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c69-108">Riferimento a una classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale per la creazione di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="d1c69-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to create a snapshot of.</span></span>

</dd> <dt>

<span data-ttu-id="d1c69-109">*SnapshotSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1c69-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c69-110">Stringa che contiene un'istanza incorporata di una classe [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) che contiene le impostazioni dei parametri per lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="d1c69-110">A string that contains an embedded instance of a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) class that contains the parameter settings for the snapshot.</span></span> <span data-ttu-id="d1c69-111">Questo parametro è facoltativo e può essere una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="d1c69-111">This parameter is optional and may be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="d1c69-112">*SnapshotType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1c69-112">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c69-113">Specifica il tipo di snapshot richiesto.</span><span class="sxs-lookup"><span data-stu-id="d1c69-113">Specifies the type of snapshot requested.</span></span> <span data-ttu-id="d1c69-114">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d1c69-114">This must be one of the following values.</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="d1c69-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Snapshot completo** (2)</span><span class="sxs-lookup"><span data-stu-id="d1c69-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d1c69-116">Snapshot completo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1c69-116">Complete snapshot of the virtual machine.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="d1c69-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Snapshot del disco** (3)</span><span class="sxs-lookup"><span data-stu-id="d1c69-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d1c69-118">Snapshot dei dischi delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="d1c69-118">Snapshot of virtual machine disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d1c69-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d1c69-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="d1c69-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d1c69-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="d1c69-121">*ResultingSnapshot* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d1c69-121">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c69-122">Riferimento a un oggetto [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) che rappresenta lo snapshot della macchina virtuale risultante.</span><span class="sxs-lookup"><span data-stu-id="d1c69-122">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the resulting virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d1c69-123">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="d1c69-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c69-124">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d1c69-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c69-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1c69-125">Return value</span></span>

<span data-ttu-id="d1c69-126">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d1c69-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d1c69-127">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="d1c69-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d1c69-128">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="d1c69-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d1c69-129">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="d1c69-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d1c69-130">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="d1c69-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d1c69-131">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="d1c69-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d1c69-132">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="d1c69-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d1c69-133">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="d1c69-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d1c69-134">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d1c69-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d1c69-135">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="d1c69-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d1c69-136">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d1c69-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d1c69-137">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d1c69-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="d1c69-138">Esempio</span><span class="sxs-lookup"><span data-stu-id="d1c69-138">Examples</span></span>

<span data-ttu-id="d1c69-139">Il codice di esempio C# seguente crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1c69-139">The following C# example code creates a virtual machine.</span></span> <span data-ttu-id="d1c69-140">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="d1c69-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1c69-141">Per funzionare correttamente, il codice seguente deve essere eseguito sul server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="d1c69-141">To function correctly, the following code must be run on the virtual machine host server, and it must be run with Administrator privileges.</span></span>

 


```CSharp
public static void CreateSnapshot(string vmName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemSnapshotService");

    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("CreateSnapshot");

    // Set the AffectedSystem property.
    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    if (null == vm)
    {
        throw new ArgumentException(string.Format("The virtual machine \"{0}\" could not be found.", vmName));
    }

    inParams["AffectedSystem"] = vm.Path.Path;

    // Set the SnapshotSettings property.
#if(true)
    inParams["SnapshotSettings"] = "";
#else
    ManagementObject snapshotSettings = Utility.GetServiceObject(scope, "CIM_SettingData"); 
    inParams["SnapshotSettings"] = snapshotSettings.ToString();
#endif       
    // Set the SnapshotType property.
    inParams["SnapshotType"] = 2; // Full snapshot.

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("CreateSnapshot", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Snapshot was created successfully.");

            MiscClass.GetAffectedElement(outParams, scope);
        }
        else
        {
            Console.WriteLine("Failed to create snapshot VM");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Snapshot was created successfully.");
    }
    else
    {
        Console.WriteLine("Create virtual system snapshot failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="d1c69-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1c69-142">Requirements</span></span>



| <span data-ttu-id="d1c69-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1c69-143">Requirement</span></span> | <span data-ttu-id="d1c69-144">Valore</span><span class="sxs-lookup"><span data-stu-id="d1c69-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c69-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1c69-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c69-146">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d1c69-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d1c69-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1c69-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c69-148">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d1c69-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1c69-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d1c69-149">Namespace</span></span><br/>                | <span data-ttu-id="d1c69-150">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d1c69-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d1c69-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1c69-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1c69-152"><dt>DBDAOINT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1c69-152"><dt>Dbdaoint.h</dt></span></span> </dl>                   |
| <span data-ttu-id="d1c69-153">MOF</span><span class="sxs-lookup"><span data-stu-id="d1c69-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1c69-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1c69-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1c69-155">DLL</span><span class="sxs-lookup"><span data-stu-id="d1c69-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1c69-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1c69-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d1c69-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1c69-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c69-158">**\_VirtualSystemSnapshotService MSVM**</span><span class="sxs-lookup"><span data-stu-id="d1c69-158">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="d1c69-159">**CreateVirtualSystemSnapshot (V1)**</span><span class="sxs-lookup"><span data-stu-id="d1c69-159">**CreateVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/createvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

