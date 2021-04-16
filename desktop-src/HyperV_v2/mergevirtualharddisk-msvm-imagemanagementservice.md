---
description: Unisce un disco rigido virtuale figlio in una catena di differenze con uno o più dischi rigidi virtuali padre nella catena.
ms.assetid: 10633176-F0C3-4CA0-8E7B-2B11FF93B0EA
title: Metodo MergeVirtualHardDisk della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.MergeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 347e11d55357a8b3366aeb09badc53c1afad9e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529664"
---
# <a name="mergevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="915f2-103">Metodo MergeVirtualHardDisk della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="915f2-103">MergeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="915f2-104">Unisce un disco rigido virtuale figlio in una catena di differenze con uno o più dischi rigidi virtuali padre nella catena.</span><span class="sxs-lookup"><span data-stu-id="915f2-104">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span> <span data-ttu-id="915f2-105">Per informazioni sulle restrizioni di utilizzo di questo metodo, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="915f2-105">See Remarks for usage restrictions for this method.</span></span>

<span data-ttu-id="915f2-106">Se l'utente che esegue questa funzione non dispone dell'autorizzazione per aggiornare le macchine virtuali, la funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="915f2-106">If the user executing this function does not have permission to update the virtual machines, then this function will fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="915f2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="915f2-107">Syntax</span></span>


```mof
uint32 MergeVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              DestinationPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="915f2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="915f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="915f2-109">*SourcePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="915f2-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="915f2-110">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="915f2-110">Type: **string**</span></span>

<span data-ttu-id="915f2-111">Percorso completo che specifica il percorso del file del disco rigido virtuale da unire.</span><span class="sxs-lookup"><span data-stu-id="915f2-111">A fully qualified path that specifies the location of the virtual hard disk file to merge.</span></span>

</dd> <dt>

<span data-ttu-id="915f2-112">*DestinationPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="915f2-112">*DestinationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="915f2-113">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="915f2-113">Type: **string**</span></span>

<span data-ttu-id="915f2-114">Percorso completo che specifica il percorso del file del disco rigido virtuale padre in cui deve essere eseguito il merge dei dati.</span><span class="sxs-lookup"><span data-stu-id="915f2-114">A fully qualified path that specifies the location of the parent virtual hard disk file into which data is to be merged.</span></span> <span data-ttu-id="915f2-115">Potrebbe trattarsi del disco rigido virtuale padre diretto del file di Unione o dell'immagine del disco padre, in modo da aumentare la catena di differenziazione.</span><span class="sxs-lookup"><span data-stu-id="915f2-115">This could be the immediate parent virtual hard disk of the merging file or the parent disk image a few levels up the differencing chain.</span></span>

</dd> <dt>

<span data-ttu-id="915f2-116">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="915f2-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="915f2-117">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="915f2-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="915f2-118">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="915f2-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="915f2-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="915f2-119">Return value</span></span>

<span data-ttu-id="915f2-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="915f2-120">Type: **uint32**</span></span>

<span data-ttu-id="915f2-121">Questo metodo può restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="915f2-121">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="915f2-122">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="915f2-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-123">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="915f2-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-124">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="915f2-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-125">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="915f2-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-126">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="915f2-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-127">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="915f2-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-128">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="915f2-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-129">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="915f2-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-130">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="915f2-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-131">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="915f2-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-132">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="915f2-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-133">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="915f2-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-134">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="915f2-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="915f2-135">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="915f2-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="915f2-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="915f2-136">Remarks</span></span>

<span data-ttu-id="915f2-137">Il disco rigido virtuale figlio deve essere offline.</span><span class="sxs-lookup"><span data-stu-id="915f2-137">The child virtual hard disk must be offline.</span></span>

<span data-ttu-id="915f2-138">Con questo metodo è possibile usare solo i tipi di dischi rigidi virtuali seguenti:</span><span class="sxs-lookup"><span data-stu-id="915f2-138">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="915f2-139">Disco rigido virtuale differenze</span><span class="sxs-lookup"><span data-stu-id="915f2-139">Differencing VHD</span></span>
-   <span data-ttu-id="915f2-140">VHDX differenze</span><span class="sxs-lookup"><span data-stu-id="915f2-140">Differencing VHDX</span></span>

<span data-ttu-id="915f2-141">L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="915f2-141">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="915f2-142">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="915f2-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="915f2-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="915f2-143">Examples</span></span>

<span data-ttu-id="915f2-144">Nell'esempio C# seguente viene espanso un file di disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="915f2-144">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="915f2-145">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="915f2-145">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
// Merges a VHD into a parent VHD.
// ChildPath: The path to the VHD to merge.</param>
// ParentPath: The path to the parent into which to merge.</param>
public static void MergeVirtualHardDisk(string ChildPath, string ParentPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("MergeVirtualHardDisk");

    inParams["SourcePath"] = ChildPath;
    inParams["DestinationPath"] = ParentPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("MergeVirtualHardDisk", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("MergeVirtualHardDisk succeeded.");
        }
        else
        {
            Console.WriteLine("MergeVirtualHardDisk failed.");
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="915f2-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="915f2-146">Requirements</span></span>



| <span data-ttu-id="915f2-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="915f2-147">Requirement</span></span> | <span data-ttu-id="915f2-148">Valore</span><span class="sxs-lookup"><span data-stu-id="915f2-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="915f2-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="915f2-149">Minimum supported client</span></span><br/> | <span data-ttu-id="915f2-150">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="915f2-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="915f2-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="915f2-151">Minimum supported server</span></span><br/> | <span data-ttu-id="915f2-152">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="915f2-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="915f2-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="915f2-153">Namespace</span></span><br/>                | <span data-ttu-id="915f2-154">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="915f2-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="915f2-155">MOF</span><span class="sxs-lookup"><span data-stu-id="915f2-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="915f2-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="915f2-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="915f2-157">DLL</span><span class="sxs-lookup"><span data-stu-id="915f2-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="915f2-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="915f2-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="915f2-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="915f2-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="915f2-160">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="915f2-160">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="915f2-161">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="915f2-161">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

