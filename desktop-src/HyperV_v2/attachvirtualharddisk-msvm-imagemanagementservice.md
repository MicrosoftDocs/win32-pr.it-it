---
description: Connette un file di disco rigido virtuale in modalità loopback.
ms.assetid: 54bd8e67-e309-4bf3-94bd-e29bc3300a3d
title: Metodo AttachVirtualHardDisk della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.AttachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f8a22ac377eb96fdc01fa54877cdc6c12619c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881865"
---
# <a name="attachvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="b2454-103">Metodo AttachVirtualHardDisk della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="b2454-103">AttachVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="b2454-104">Connette un file di disco rigido virtuale in modalità loopback.</span><span class="sxs-lookup"><span data-stu-id="b2454-104">Attaches a virtual hard disk file in loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2454-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2454-105">Syntax</span></span>


```mof
uint32 AttachVirtualHardDisk(
  [in]  string              Path,
  [in]  boolean             AssignDriveLetter,
  [in]  boolean             ReadOnly,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b2454-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2454-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2454-107">*Percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2454-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2454-108">Percorso completo che specifica il percorso del file del disco rigido virtuale da alporre.</span><span class="sxs-lookup"><span data-stu-id="b2454-108">A fully qualified path that specifies the location of the virtual hard disk file to attach.</span></span>

</dd> <dt>

<span data-ttu-id="b2454-109">*AssignDriveLetter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2454-109">*AssignDriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2454-110">Indica se le lettere di unità vengono assegnate ai volumi del disco.</span><span class="sxs-lookup"><span data-stu-id="b2454-110">Indicates if drive letters are assigned to the disk's volumes.</span></span>

</dd> <dt>

<span data-ttu-id="b2454-111">*ReadOnly* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2454-111">*ReadOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2454-112">Indica se il disco rigido collegato deve essere di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b2454-112">Indicates if the attached hard disk should be read-only.</span></span>

</dd> <dt>

<span data-ttu-id="b2454-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="b2454-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2454-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b2454-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2454-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2454-115">Return value</span></span>

<span data-ttu-id="b2454-116">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b2454-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b2454-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="b2454-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-118">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="b2454-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="b2454-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="b2454-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="b2454-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-122">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="b2454-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="b2454-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b2454-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-125">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b2454-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-126">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="b2454-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-127">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b2454-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-128">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="b2454-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b2454-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b2454-130">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="b2454-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b2454-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2454-131">Remarks</span></span>

<span data-ttu-id="b2454-132">Per scollegare il disco rigido virtuale, usare il metodo [**MSVM \_ MountedStorageImage. DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) .</span><span class="sxs-lookup"><span data-stu-id="b2454-132">To detach the virtual hard disk, use the [**Msvm\_MountedStorageImage.DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) method.</span></span>

<span data-ttu-id="b2454-133">L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="b2454-133">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b2454-134">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b2454-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="b2454-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="b2454-135">Examples</span></span>

<span data-ttu-id="b2454-136">Nell'esempio C# riportato di seguito viene illustrato come aggiungere un file di disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2454-136">The following C# example shows how to attach a virtual hard disk file.</span></span> <span data-ttu-id="b2454-137">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="b2454-137">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void AttachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("AttachVirtualHardDisk");
    inParams["Path"] = path;
    inParams["AssignDriveLetter"] = true;
    inParams["ReadOnly"] = false;
    ManagementBaseObject outParams = imageService.InvokeMethod("AttachVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was attached successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to attach {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="b2454-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2454-138">Requirements</span></span>



| <span data-ttu-id="b2454-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2454-139">Requirement</span></span> | <span data-ttu-id="b2454-140">Valore</span><span class="sxs-lookup"><span data-stu-id="b2454-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2454-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2454-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b2454-142">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b2454-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b2454-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2454-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b2454-144">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b2454-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2454-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b2454-145">Namespace</span></span><br/>                | <span data-ttu-id="b2454-146">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b2454-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b2454-147">MOF</span><span class="sxs-lookup"><span data-stu-id="b2454-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2454-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2454-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2454-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b2454-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2454-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2454-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2454-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2454-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2454-152">**MSVM \_ MountedStorageImage. DetachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="b2454-152">**Msvm\_MountedStorageImage.DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md)
</dt> <dt>

[<span data-ttu-id="b2454-153">**Montaggio (V1)**</span><span class="sxs-lookup"><span data-stu-id="b2454-153">**Mount (V1)**</span></span>](/previous-versions/windows/desktop/virtual/mount-msvm-imagemanagementservice)
</dt> <dt>

[<span data-ttu-id="b2454-154">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="b2454-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

