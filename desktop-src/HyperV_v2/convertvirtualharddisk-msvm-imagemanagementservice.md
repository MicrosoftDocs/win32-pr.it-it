---
description: Converte un disco rigido virtuale esistente in un tipo o formato diverso.
ms.assetid: D4F3A030-D860-4569-B6CD-31661BD40D54
title: Metodo ConvertVirtualHardDisk della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 766b117b69ecfebd13986d02ca21df3725981bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314355"
---
# <a name="convertvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="3d062-103">Metodo ConvertVirtualHardDisk della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="3d062-103">ConvertVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="3d062-104">Converte un disco rigido virtuale esistente in un tipo o formato diverso.</span><span class="sxs-lookup"><span data-stu-id="3d062-104">Converts an existing virtual hard disk to a different type or format.</span></span> <span data-ttu-id="3d062-105">Questo metodo crea un nuovo disco rigido virtuale e non converte il disco rigido virtuale di origine sul posto.</span><span class="sxs-lookup"><span data-stu-id="3d062-105">This method creates a new virtual hard disk and does not convert the source virtual hard disk in place.</span></span> <span data-ttu-id="3d062-106">Per informazioni sulle restrizioni di utilizzo di questo metodo, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="3d062-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d062-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d062-107">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3d062-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d062-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d062-109">*SourcePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d062-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d062-110">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="3d062-110">Type: **string**</span></span>

<span data-ttu-id="3d062-111">Percorso completo del file di disco rigido virtuale di origine da convertire.</span><span class="sxs-lookup"><span data-stu-id="3d062-111">The fully qualified path of the source virtual hard disk file to convert.</span></span> <span data-ttu-id="3d062-112">Il file non verrà modificato in seguito a questa operazione.</span><span class="sxs-lookup"><span data-stu-id="3d062-112">This file will not be modified as a result of this operation.</span></span>

</dd> <dt>

<span data-ttu-id="3d062-113">*VirtualDiskSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d062-113">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d062-114">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="3d062-114">Type: **string**</span></span>

<span data-ttu-id="3d062-115">Rappresentazione di stringa della classe [**\_ VirtualHardDiskSettingData di MSVM**](msvm-virtualharddisksettingdata.md) che specifica gli attributi del nuovo disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d062-115">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the attributes of the new virtual hard disk.</span></span> <span data-ttu-id="3d062-116">È necessario impostare le proprietà **path**, **Type**, **Format**, **ParentPath**, **blockSize** e **LogicalSectorSize** .</span><span class="sxs-lookup"><span data-stu-id="3d062-116">The **Path**, **Type**, **Format**, **ParentPath**, **BlockSize**, and **LogicalSectorSize** properties must be set.</span></span> <span data-ttu-id="3d062-117">Se non è necessario, la proprietà **ParentPath** può essere **null** .</span><span class="sxs-lookup"><span data-stu-id="3d062-117">The **ParentPath** property can be **Null** if it is not needed.</span></span> <span data-ttu-id="3d062-118">Impostare le proprietà **blockSize** e **LogicalSectorSize** su 0 per usare i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="3d062-118">Set the **BlockSize** and **LogicalSectorSize** properties to 0 to use the default values.</span></span>

<span data-ttu-id="3d062-119">Per specificare il formato (VHD o VHDX) del nuovo disco rigido virtuale, impostare l'estensione del **percorso** sul valore appropriato (". VHD" o ". vhdx").</span><span class="sxs-lookup"><span data-stu-id="3d062-119">To specify the format (VHD or VHDX) of the new virtual hard disk, set the extension of the **Path** to the appropriate value (".vhd" or ".vhdx").</span></span> <span data-ttu-id="3d062-120">La proprietà **Format** deve corrispondere all'estensione del nome di file nel **percorso**.</span><span class="sxs-lookup"><span data-stu-id="3d062-120">The **Format** property must match the file name extension in the **Path**.</span></span>

<span data-ttu-id="3d062-121">La proprietà **LogicalSectorSize** verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="3d062-121">The **LogicalSectorSize** property will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="3d062-122">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="3d062-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d062-123">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="3d062-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="3d062-124">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3d062-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d062-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d062-125">Return value</span></span>

<span data-ttu-id="3d062-126">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d062-126">Type: **uint32**</span></span>

<span data-ttu-id="3d062-127">Questo metodo può restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d062-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3d062-128">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="3d062-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-129">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="3d062-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-130">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="3d062-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-131">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="3d062-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-132">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="3d062-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-133">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="3d062-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-134">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3d062-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-135">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="3d062-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-136">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3d062-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-137">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="3d062-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-138">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="3d062-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-139">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="3d062-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-140">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="3d062-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3d062-141">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="3d062-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3d062-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d062-142">Remarks</span></span>

<span data-ttu-id="3d062-143">Con questo metodo è possibile usare solo i tipi di dischi rigidi virtuali seguenti:</span><span class="sxs-lookup"><span data-stu-id="3d062-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="3d062-144">VHD fisso</span><span class="sxs-lookup"><span data-stu-id="3d062-144">Fixed VHD</span></span>
-   <span data-ttu-id="3d062-145">Correzione di VHDX</span><span class="sxs-lookup"><span data-stu-id="3d062-145">Fixed VHDX</span></span>
-   <span data-ttu-id="3d062-146">VHD dinamico</span><span class="sxs-lookup"><span data-stu-id="3d062-146">Dynamic VHD</span></span>
-   <span data-ttu-id="3d062-147">VHDX dinamico</span><span class="sxs-lookup"><span data-stu-id="3d062-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="3d062-148">Disco rigido virtuale differenze</span><span class="sxs-lookup"><span data-stu-id="3d062-148">Differencing VHD</span></span>
-   <span data-ttu-id="3d062-149">VHDX differenze</span><span class="sxs-lookup"><span data-stu-id="3d062-149">Differencing VHDX</span></span>

<span data-ttu-id="3d062-150">L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="3d062-150">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3d062-151">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3d062-151">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="3d062-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="3d062-152">Examples</span></span>

<span data-ttu-id="3d062-153">Nell'esempio C# seguente viene convertito un disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="3d062-153">The following C# example converts a virtual hard disk.</span></span> <span data-ttu-id="3d062-154">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="3d062-154">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskType
{
    Fixed = 2,
    Dynamic = 3,
    Differencing = 4
}

public enum VirtualHardDiskFormat
{
    Unknown = 0,
    Vhd = 2,
    Vhdx = 3
}

public static void ConvertVirtualHardDisk(string sourcePath, string destinationPath, VirtualHardDiskType diskType, VirtualHardDiskFormat diskFormat)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementPath path = new ManagementPath()
    {
        Server = null,
        NamespacePath = imageService.Path.Path,
        ClassName = "Msvm_VirtualHardDiskSettingData"
    };

    ManagementClass settingsClass = new ManagementClass(path);
    ManagementObject settingsInstance = settingsClass.CreateInstance();
    settingsInstance["Path"] = destinationPath;
    settingsInstance["Type"] = diskType;
    settingsInstance["Format"] = diskFormat;
    settingsInstance["ParentPath"] = null;
    settingsInstance["MaxInternalSize"] = 0;
    settingsInstance["BlockSize"] = 0;
    settingsInstance["LogicalSectorSize"] = 0;
    settingsInstance["PhysicalSectorSize"] = 0;

    ManagementBaseObject inParams = imageService.GetMethodParameters("ConvertVirtualHardDisk");

    inParams["SourcePath"] = sourcePath;
    inParams["VirtualDiskSettingData"] = settingsInstance.GetText(TextFormat.WmiDtd20);

    ManagementBaseObject outParams = imageService.InvokeMethod("ConvertVirtualHardDisk", inParams, null);
    UInt32 result = (UInt32)outParams["ReturnValue"];
    if (ReturnCode.Completed == result)
    {
        Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
    }
    else if (ReturnCode.Started == result)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
        }
        else
        {
            Console.WriteLine("Unable to convert {0}", inParams["SourcePath"]);
        }
    }
    else
    {
        // The method failed.
        Console.WriteLine("ConvertVirtualHardDisk failed with error code {0}.", result);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="3d062-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d062-155">Requirements</span></span>



| <span data-ttu-id="3d062-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d062-156">Requirement</span></span> | <span data-ttu-id="3d062-157">Valore</span><span class="sxs-lookup"><span data-stu-id="3d062-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d062-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d062-158">Minimum supported client</span></span><br/> | <span data-ttu-id="3d062-159">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3d062-159">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3d062-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d062-160">Minimum supported server</span></span><br/> | <span data-ttu-id="3d062-161">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3d062-161">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3d062-162">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3d062-162">Namespace</span></span><br/>                | <span data-ttu-id="3d062-163">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3d062-163">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3d062-164">MOF</span><span class="sxs-lookup"><span data-stu-id="3d062-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d062-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d062-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d062-166">DLL</span><span class="sxs-lookup"><span data-stu-id="3d062-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d062-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3d062-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3d062-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d062-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d062-169">**ConvertVirtualHardDisk (V1)**</span><span class="sxs-lookup"><span data-stu-id="3d062-169">**ConvertVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/convertvirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="3d062-170">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d062-170">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3d062-171">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="3d062-171">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

