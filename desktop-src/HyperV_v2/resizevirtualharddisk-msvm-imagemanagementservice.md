---
description: Ridimensiona un disco rigido virtuale esistente.
ms.assetid: 54FDCA3B-E12B-4E68-B7EE-893C9CD97E1A
title: Metodo ResizeVirtualHardDisk della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ResizeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5fcd88a9063dcbe4e19705245b36af33672dfc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307864"
---
# <a name="resizevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="3cec3-103">Metodo ResizeVirtualHardDisk della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="3cec3-103">ResizeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="3cec3-104">Ridimensiona un disco rigido virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="3cec3-104">Resizes an existing virtual hard disk.</span></span> <span data-ttu-id="3cec3-105">Il disco rigido virtuale deve essere offline.</span><span class="sxs-lookup"><span data-stu-id="3cec3-105">The virtual hard disk must be offline.</span></span> <span data-ttu-id="3cec3-106">Per informazioni sulle restrizioni di utilizzo di questo metodo, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="3cec3-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cec3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3cec3-107">Syntax</span></span>


```mof
uint32 ResizeVirtualHardDisk(
  [in]  string              Path,
  [in]  uint64              MaxInternalSize,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3cec3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3cec3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cec3-109">*Percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3cec3-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cec3-110">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="3cec3-110">Type: **string**</span></span>

<span data-ttu-id="3cec3-111">Percorso completo del file del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="3cec3-111">The fully qualified path of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="3cec3-112">*MaxInternalSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3cec3-112">*MaxInternalSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cec3-113">Tipo: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3cec3-113">Type: **uint64**</span></span>

<span data-ttu-id="3cec3-114">Dimensione massima del disco rigido virtuale, in byte, visualizzabile dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3cec3-114">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="3cec3-115">Il valore minimo di *MaxInternalSize* è *fissoDimensione* + 512-(*fissoDimensione* mod 512).</span><span class="sxs-lookup"><span data-stu-id="3cec3-115">*MaxInternalSize* minimum value is *DiskSize* + 512 - (*DiskSize* mod 512).</span></span> <span data-ttu-id="3cec3-116">*FissoDimensione* è la dimensione in byte del file del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="3cec3-116">*DiskSize* is the size of the virtual hard disk file, in bytes.</span></span> <span data-ttu-id="3cec3-117">Se il valore *MaxInternalSize* specificato è minore del valore minimo, viene restituito l'errore InvalidParameter (32773).</span><span class="sxs-lookup"><span data-stu-id="3cec3-117">The InvalidParameter error (32773) is returned if the *MaxInternalSize* value specified is less than the minimum value.</span></span>

</dd> <dt>

<span data-ttu-id="3cec3-118">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="3cec3-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cec3-119">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="3cec3-119">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="3cec3-120">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3cec3-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cec3-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3cec3-121">Return value</span></span>

<span data-ttu-id="3cec3-122">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3cec3-122">Type: **uint32**</span></span>

<span data-ttu-id="3cec3-123">Questo metodo può restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3cec3-123">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3cec3-124">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="3cec3-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-125">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="3cec3-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-126">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="3cec3-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-127">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="3cec3-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-128">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="3cec3-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-129">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="3cec3-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-130">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3cec3-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-131">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="3cec3-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-132">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3cec3-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-133">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="3cec3-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-134">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="3cec3-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-135">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="3cec3-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-136">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="3cec3-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3cec3-137">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="3cec3-137">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3cec3-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="3cec3-138">Remarks</span></span>

<span data-ttu-id="3cec3-139">Con questo metodo è possibile usare solo i tipi di dischi rigidi virtuali seguenti quando è in corso l'aumento delle dimensioni del disco rigido virtuale:</span><span class="sxs-lookup"><span data-stu-id="3cec3-139">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being increased:</span></span>

-   <span data-ttu-id="3cec3-140">VHD fisso</span><span class="sxs-lookup"><span data-stu-id="3cec3-140">Fixed VHD</span></span>
-   <span data-ttu-id="3cec3-141">Correzione di VHDX</span><span class="sxs-lookup"><span data-stu-id="3cec3-141">Fixed VHDX</span></span>
-   <span data-ttu-id="3cec3-142">VHD dinamico</span><span class="sxs-lookup"><span data-stu-id="3cec3-142">Dynamic VHD</span></span>
-   <span data-ttu-id="3cec3-143">VHDX dinamico</span><span class="sxs-lookup"><span data-stu-id="3cec3-143">Dynamic VHDX</span></span>
-   <span data-ttu-id="3cec3-144">VHDX differenze</span><span class="sxs-lookup"><span data-stu-id="3cec3-144">Differencing VHDX</span></span>

<span data-ttu-id="3cec3-145">Con questo metodo è possibile utilizzare solo i tipi di dischi rigidi virtuali seguenti quando si riduce la dimensione del disco rigido virtuale:</span><span class="sxs-lookup"><span data-stu-id="3cec3-145">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being decreased:</span></span>

-   <span data-ttu-id="3cec3-146">Correzione di VHDX</span><span class="sxs-lookup"><span data-stu-id="3cec3-146">Fixed VHDX</span></span>
-   <span data-ttu-id="3cec3-147">VHDX dinamico</span><span class="sxs-lookup"><span data-stu-id="3cec3-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="3cec3-148">VHDX differenze</span><span class="sxs-lookup"><span data-stu-id="3cec3-148">Differencing VHDX</span></span>

<span data-ttu-id="3cec3-149">L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="3cec3-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3cec3-150">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3cec3-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="3cec3-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="3cec3-151">Examples</span></span>

<span data-ttu-id="3cec3-152">Nell'esempio C# seguente viene espanso un file di disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="3cec3-152">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="3cec3-153">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="3cec3-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
const UInt64 size1G = 0x40000000;

public static void ResizeVirtualHardDisk(string path, UInt64 maxInternalSize)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ResizeVirtualHardDisk");
    inParams["Path"] = path;
    inParams["MaxInternalSize"] = maxInternalSize * size1G;
    ManagementBaseObject outParams = imageService.InvokeMethod("ResizeVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was resized successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to resize {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="3cec3-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3cec3-154">Requirements</span></span>



| <span data-ttu-id="3cec3-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cec3-155">Requirement</span></span> | <span data-ttu-id="3cec3-156">Valore</span><span class="sxs-lookup"><span data-stu-id="3cec3-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cec3-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3cec3-157">Minimum supported client</span></span><br/> | <span data-ttu-id="3cec3-158">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3cec3-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3cec3-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3cec3-159">Minimum supported server</span></span><br/> | <span data-ttu-id="3cec3-160">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3cec3-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3cec3-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3cec3-161">Namespace</span></span><br/>                | <span data-ttu-id="3cec3-162">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3cec3-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3cec3-163">MOF</span><span class="sxs-lookup"><span data-stu-id="3cec3-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cec3-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cec3-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cec3-165">DLL</span><span class="sxs-lookup"><span data-stu-id="3cec3-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cec3-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3cec3-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3cec3-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3cec3-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="3cec3-168">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3cec3-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3cec3-169">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="3cec3-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

