---
description: Determina se un file di disco rigido virtuale è valido.
ms.assetid: 5F7C99DB-0C81-46D5-A965-B6D87647ABF6
title: Metodo ValidateVirtualHardDisk della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 50c00dc4336e3e85b7db8ffd334de8868054c997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317178"
---
# <a name="validatevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="32e53-103">Metodo ValidateVirtualHardDisk della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="32e53-103">ValidateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="32e53-104">Determina se un file di disco rigido virtuale è valido.</span><span class="sxs-lookup"><span data-stu-id="32e53-104">Determines whether a virtual hard disk file is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e53-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32e53-105">Syntax</span></span>


```mof
uint32 ValidateVirtualHardDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="32e53-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32e53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32e53-107">*Percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32e53-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32e53-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="32e53-108">Type: **string**</span></span>

<span data-ttu-id="32e53-109">Percorso completo che specifica il percorso del file del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="32e53-109">A fully qualified path that specifies the location of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="32e53-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="32e53-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32e53-111">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="32e53-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="32e53-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32e53-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32e53-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32e53-113">Return value</span></span>

<span data-ttu-id="32e53-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32e53-114">Type: **uint32**</span></span>

<span data-ttu-id="32e53-115">Questo metodo può restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="32e53-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="32e53-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="32e53-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="32e53-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="32e53-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="32e53-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="32e53-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="32e53-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="32e53-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="32e53-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-124">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="32e53-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="32e53-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="32e53-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="32e53-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="32e53-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-129">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="32e53-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="32e53-130">**Rilevato ciclo della catena di differenze VHD** (32787)</span><span class="sxs-lookup"><span data-stu-id="32e53-130">**Vhd differencing chain cycle detected** (32787)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="32e53-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="32e53-131">Remarks</span></span>

<span data-ttu-id="32e53-132">Se il disco rigido virtuale è un disco differenze, viene aperta l'intera catena di dischi virtuali.</span><span class="sxs-lookup"><span data-stu-id="32e53-132">If the virtual hard disk is a differencing disk, the entire virtual disk chain is opened.</span></span> <span data-ttu-id="32e53-133">Se il collegamento viene rotto nella catena di dischi, viene restituito un oggetto processo con l'errore appropriato inizializzato e le proprietà figlio e padre vengono inizializzate nel percorso in cui il collegamento è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="32e53-133">If the link is broken in the disk chain, a job object is returned with the appropriate error initialized and the child and parent properties are initialized to the location where the link is broken.</span></span>

<span data-ttu-id="32e53-134">L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="32e53-134">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="32e53-135">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="32e53-135">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="32e53-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="32e53-136">Examples</span></span>

<span data-ttu-id="32e53-137">Nell'esempio C# seguente viene convalidata un'immagine del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="32e53-137">The following C# example validates a virtual hard disk image.</span></span> <span data-ttu-id="32e53-138">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="32e53-138">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void ValidateVirtualHardDisk(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ValidateVirtualHardDisk");
    inParams["Path"] = vhdPath;
    ManagementBaseObject outParams = imageService.InvokeMethod("ValidateVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} is a valid virtual hard disk.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to validate {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="32e53-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32e53-139">Requirements</span></span>



| <span data-ttu-id="32e53-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="32e53-140">Requirement</span></span> | <span data-ttu-id="32e53-141">Valore</span><span class="sxs-lookup"><span data-stu-id="32e53-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32e53-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32e53-142">Minimum supported client</span></span><br/> | <span data-ttu-id="32e53-143">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="32e53-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="32e53-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32e53-144">Minimum supported server</span></span><br/> | <span data-ttu-id="32e53-145">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="32e53-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32e53-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="32e53-146">Namespace</span></span><br/>                | <span data-ttu-id="32e53-147">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="32e53-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="32e53-148">MOF</span><span class="sxs-lookup"><span data-stu-id="32e53-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32e53-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32e53-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="32e53-150">DLL</span><span class="sxs-lookup"><span data-stu-id="32e53-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32e53-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="32e53-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="32e53-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32e53-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e53-153">**ValidateVirtualHardDisk (V1)**</span><span class="sxs-lookup"><span data-stu-id="32e53-153">**ValidateVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/validatevirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="32e53-154">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32e53-154">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="32e53-155">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="32e53-155">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

