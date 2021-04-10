---
description: Recupera i dati delle impostazioni associati a un file di disco rigido virtuale.
ms.assetid: b82c018e-8d23-4615-99c1-3b622a8f41da
title: Metodo GetVirtualHardDiskSettingData della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: cf8f19d3bbdac593dabef0a1ff8e9c9b60027301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966501"
---
# <a name="getvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="ae1e3-103">Metodo GetVirtualHardDiskSettingData della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="ae1e3-103">GetVirtualHardDiskSettingData method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="ae1e3-104">Recupera i dati delle impostazioni associati a un file di disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-104">Retrieves the setting data associated with a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae1e3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae1e3-105">Syntax</span></span>


```mof
uint32 GetVirtualHardDiskSettingData(
  [in]  string              Path,
  [out] string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ae1e3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae1e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae1e3-107">*Percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae1e3-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae1e3-108">Percorso completo del file di immagine del disco.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-108">The fully qualified path of the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="ae1e3-109">*SettingData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ae1e3-109">*SettingData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae1e3-110">Se ha esito positivo, riceve un'istanza incorporata della classe [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) che contiene i dati dell'impostazione per il disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-110">If successful, receives an embedded instance of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that contains the setting data for the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="ae1e3-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ae1e3-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae1e3-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae1e3-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae1e3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae1e3-113">Return value</span></span>

<span data-ttu-id="ae1e3-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ae1e3-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-123">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ae1e3-128">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ae1e3-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae1e3-129">Remarks</span></span>

<span data-ttu-id="ae1e3-130">L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-130">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ae1e3-131">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ae1e3-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ae1e3-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="ae1e3-132">Examples</span></span>

<span data-ttu-id="ae1e3-133">Nell'esempio C# riportato di seguito viene illustrato come chiamare il metodo [**GetVirtualHardDiskState**](getvirtualharddiskstate-msvm-imagemanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ae1e3-133">The following C# example shows how to call the [**GetVirtualHardDiskState**](getvirtualharddiskstate-msvm-imagemanagementservice.md) method.</span></span> <span data-ttu-id="ae1e3-134">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="ae1e3-134">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void GetVirtualHardDiskSettingData(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");
    ManagementBaseObject inParams = imageService.GetMethodParameters("GetVirtualHardDiskSettingData");

    inParams["Path"] = vhdPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("GetVirtualHardDiskSettingData", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("GetVirtualHardDiskSettingData was successful.");
        }
        else
        {
            Console.WriteLine("GetVirtualHardDiskSettingData was not successful.");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        string diskStateString = outParams["SettingData"].ToString();
        Utility.PrintEmbeddedInstance(diskStateString);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="ae1e3-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae1e3-135">Requirements</span></span>



| <span data-ttu-id="ae1e3-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae1e3-136">Requirement</span></span> | <span data-ttu-id="ae1e3-137">Valore</span><span class="sxs-lookup"><span data-stu-id="ae1e3-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae1e3-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae1e3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ae1e3-139">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ae1e3-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ae1e3-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae1e3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ae1e3-141">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ae1e3-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ae1e3-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ae1e3-142">Namespace</span></span><br/>                | <span data-ttu-id="ae1e3-143">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ae1e3-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ae1e3-144">MOF</span><span class="sxs-lookup"><span data-stu-id="ae1e3-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae1e3-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae1e3-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae1e3-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ae1e3-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae1e3-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae1e3-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ae1e3-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae1e3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae1e3-149">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="ae1e3-149">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

