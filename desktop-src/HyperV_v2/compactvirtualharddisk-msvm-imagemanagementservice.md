---
description: Compatta un file di disco rigido virtuale.
ms.assetid: 1E64BD91-6FE6-4658-9EBF-615FC705B920
title: Metodo CompactVirtualHardDisk della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CompactVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e8c148e51105d8c78021b58366e2f2df3913f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314357"
---
# <a name="compactvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="521e9-103">Metodo CompactVirtualHardDisk della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="521e9-103">CompactVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="521e9-104">Compatta un file di disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="521e9-104">Compacts a virtual hard disk file.</span></span> <span data-ttu-id="521e9-105">La compattazione è il processo che consente di liberare parti inutilizzate del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="521e9-105">Compacting is the process of freeing unused portions of the virtual hard disk.</span></span> <span data-ttu-id="521e9-106">Il disco rigido virtuale non viene montato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="521e9-106">The virtual hard disk is not automatically mounted.</span></span> <span data-ttu-id="521e9-107">Per informazioni sulle restrizioni di utilizzo di questo metodo, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="521e9-107">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="521e9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="521e9-108">Syntax</span></span>


```mof
uint32 CompactVirtualHardDisk(
  [in]  string              Path,
  [in]  uint16              Mode,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="521e9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="521e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="521e9-110">*Percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="521e9-110">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521e9-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="521e9-111">Type: **string**</span></span>

<span data-ttu-id="521e9-112">Percorso completo che specifica il percorso del file di Unione.</span><span class="sxs-lookup"><span data-stu-id="521e9-112">A fully qualified path that specifies the location of the merging file.</span></span>

</dd> <dt>

<span data-ttu-id="521e9-113">*Modalità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="521e9-113">*Mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="521e9-114">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="521e9-114">Type: **uint16**</span></span>

<span data-ttu-id="521e9-115">Specifica la modalità per l'operazione di compattazione.</span><span class="sxs-lookup"><span data-stu-id="521e9-115">Specifies the mode for the compact operation.</span></span> <span data-ttu-id="521e9-116">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="521e9-116">This must be one of the following values.</span></span>

<dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="521e9-117">**Completo** (0)</span><span class="sxs-lookup"><span data-stu-id="521e9-117">**Full** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Quick"></span><span id="quick"></span><span id="QUICK"></span>

<span data-ttu-id="521e9-118">**Rapido** (1)</span><span class="sxs-lookup"><span data-stu-id="521e9-118">**Quick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Retrim"></span><span id="retrim"></span><span id="RETRIM"></span>

<span data-ttu-id="521e9-119">**Ritaglia** (2)</span><span class="sxs-lookup"><span data-stu-id="521e9-119">**Retrim** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Pretrimmed"></span><span id="pretrimmed"></span><span id="PRETRIMMED"></span>

<span data-ttu-id="521e9-120">**Pretagliato** (3)</span><span class="sxs-lookup"><span data-stu-id="521e9-120">**Pretrimmed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Prezeroed"></span><span id="prezeroed"></span><span id="PREZEROED"></span>

<span data-ttu-id="521e9-121">**Preazzerato** (4)</span><span class="sxs-lookup"><span data-stu-id="521e9-121">**Prezeroed** (4)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="521e9-122">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="521e9-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="521e9-123">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="521e9-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="521e9-124">Riferimento al processo (può essere **null** se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="521e9-124">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="521e9-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="521e9-125">Return value</span></span>

<span data-ttu-id="521e9-126">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="521e9-126">Type: **uint32**</span></span>

<span data-ttu-id="521e9-127">Questo metodo può restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="521e9-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="521e9-128">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="521e9-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-129">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="521e9-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-130">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="521e9-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-131">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="521e9-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-132">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="521e9-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-133">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="521e9-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-134">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="521e9-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-135">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="521e9-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-136">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="521e9-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-137">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="521e9-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-138">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="521e9-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-139">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="521e9-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-140">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="521e9-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="521e9-141">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="521e9-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="521e9-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="521e9-142">Remarks</span></span>

<span data-ttu-id="521e9-143">Con questo metodo è possibile usare solo i tipi di dischi rigidi virtuali seguenti:</span><span class="sxs-lookup"><span data-stu-id="521e9-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="521e9-144">Correzione di VHDX</span><span class="sxs-lookup"><span data-stu-id="521e9-144">Fixed VHDX</span></span>
-   <span data-ttu-id="521e9-145">VHD dinamico</span><span class="sxs-lookup"><span data-stu-id="521e9-145">Dynamic VHD</span></span>
-   <span data-ttu-id="521e9-146">VHDX dinamico</span><span class="sxs-lookup"><span data-stu-id="521e9-146">Dynamic VHDX</span></span>
-   <span data-ttu-id="521e9-147">Disco rigido virtuale differenze</span><span class="sxs-lookup"><span data-stu-id="521e9-147">Differencing VHD</span></span>
-   <span data-ttu-id="521e9-148">VHDX differenze</span><span class="sxs-lookup"><span data-stu-id="521e9-148">Differencing VHDX</span></span>

<span data-ttu-id="521e9-149">L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="521e9-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="521e9-150">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="521e9-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="521e9-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="521e9-151">Examples</span></span>

<span data-ttu-id="521e9-152">Nell'esempio C# seguente viene compattato un disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="521e9-152">The following C# example compacts a virtual hard disk.</span></span> <span data-ttu-id="521e9-153">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="521e9-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskCompactMode
{
    Full = 0,
    Quick = 1,
    Retrim = 2,
    Pretrimmed = 3,
    Prezeroed = 4
}

public static void CompactVirtualHardDisk(string vhdPath, VirtualHardDiskCompactMode compactMode)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("CompactVirtualHardDisk");
    inParams["Path"] = vhdPath;
    inParams["Mode"] = compactMode;
    ManagementBaseObject outParams = imageService.InvokeMethod("CompactVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was compacted successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to compact {0}", inParams["Path"]);
        }
    }
    else
    {
        Console.WriteLine("Compact {0} returned error {1}", inParams["Path"], outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="521e9-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="521e9-154">Requirements</span></span>



| <span data-ttu-id="521e9-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="521e9-155">Requirement</span></span> | <span data-ttu-id="521e9-156">Valore</span><span class="sxs-lookup"><span data-stu-id="521e9-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="521e9-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="521e9-157">Minimum supported client</span></span><br/> | <span data-ttu-id="521e9-158">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="521e9-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="521e9-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="521e9-159">Minimum supported server</span></span><br/> | <span data-ttu-id="521e9-160">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="521e9-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="521e9-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="521e9-161">Namespace</span></span><br/>                | <span data-ttu-id="521e9-162">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="521e9-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="521e9-163">MOF</span><span class="sxs-lookup"><span data-stu-id="521e9-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="521e9-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="521e9-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="521e9-165">DLL</span><span class="sxs-lookup"><span data-stu-id="521e9-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="521e9-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="521e9-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="521e9-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="521e9-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="521e9-168">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="521e9-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="521e9-169">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="521e9-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

