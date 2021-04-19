---
description: Aggiorna l'elemento padre per i file di disco rigido virtuale foglia e figlio specificati.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Metodo SetParentVirtualHardDisk della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetParentVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f1d14d3b2ee19a9768e1ee9ed9333a452153cc9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311767"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="0ca21-103">Metodo SetParentVirtualHardDisk della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="0ca21-103">SetParentVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="0ca21-104">Aggiorna l'elemento padre per i file di disco rigido virtuale foglia e figlio specificati.</span><span class="sxs-lookup"><span data-stu-id="0ca21-104">Updates the parent for the specified leaf and child virtual hard disk files.</span></span> <span data-ttu-id="0ca21-105">Per informazioni sulle restrizioni di utilizzo di questo metodo, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="0ca21-105">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca21-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ca21-106">Syntax</span></span>


```mof
uint32 SetParentVirtualHardDisk(
  [in]  string              ChildPath,
  [in]  string              ParentPath,
  [in]  string              LeafPath,
  [in]  boolean             IgnoreIDMismatch,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0ca21-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ca21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ca21-108">*Childpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ca21-108">*ChildPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ca21-109">Percorso completo che specifica il percorso del file del disco rigido virtuale figlio.</span><span class="sxs-lookup"><span data-stu-id="0ca21-109">A fully qualified path that specifies the location of the child virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="0ca21-110">*ParentPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ca21-110">*ParentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ca21-111">Percorso completo che specifica il percorso del file del disco rigido virtuale padre.</span><span class="sxs-lookup"><span data-stu-id="0ca21-111">A fully qualified path that specifies the location of the parent virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="0ca21-112">*LeafPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ca21-112">*LeafPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ca21-113">Percorso completo che specifica il percorso del file del disco rigido virtuale foglia.</span><span class="sxs-lookup"><span data-stu-id="0ca21-113">A fully qualified path that specifies the location of the leaf virtual hard disk file.</span></span> <span data-ttu-id="0ca21-114">Il parametro può essere **null** se il disco rigido virtuale è offline, ma deve essere specificato se il disco rigido virtuale è in uso.</span><span class="sxs-lookup"><span data-stu-id="0ca21-114">The parameter can be **Null** if the virtual hard disk is offline, but must be specified if the virtual hard disk is in use.</span></span>

</dd> <dt>

<span data-ttu-id="0ca21-115">*IgnoreIDMismatch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ca21-115">*IgnoreIDMismatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ca21-116">Indica se l'elemento padre deve essere impostato forzatamente quando gli identificatori del disco virtuale non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="0ca21-116">Indicates if the parent should be forcibly set when the virtual disk identifiers do not match.</span></span> <span data-ttu-id="0ca21-117">Questo parametro deve essere utilizzato con cautela perché se il nuovo disco rigido virtuale padre non è identico all'elemento padre originale, è possibile che si verifichi un danneggiamento dei dati.</span><span class="sxs-lookup"><span data-stu-id="0ca21-117">This parameter must be used with caution because if the new parent virtual hard disk is not identical to the original parent, data corruption can occur.</span></span>

</dd> <dt>

<span data-ttu-id="0ca21-118">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="0ca21-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ca21-119">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0ca21-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ca21-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ca21-120">Return value</span></span>

<span data-ttu-id="0ca21-121">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0ca21-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0ca21-122">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="0ca21-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-123">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="0ca21-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-124">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="0ca21-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-125">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="0ca21-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-126">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="0ca21-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-127">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="0ca21-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-128">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="0ca21-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-129">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="0ca21-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-130">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="0ca21-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-131">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="0ca21-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-132">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="0ca21-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-133">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="0ca21-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-134">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="0ca21-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0ca21-135">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="0ca21-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0ca21-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ca21-136">Remarks</span></span>

<span data-ttu-id="0ca21-137">Con questo metodo è possibile usare solo i tipi di dischi rigidi virtuali seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ca21-137">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="0ca21-138">Disco rigido virtuale differenze</span><span class="sxs-lookup"><span data-stu-id="0ca21-138">Differencing VHD</span></span>
-   <span data-ttu-id="0ca21-139">VHDX differenze</span><span class="sxs-lookup"><span data-stu-id="0ca21-139">Differencing VHDX</span></span>

<span data-ttu-id="0ca21-140">L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="0ca21-140">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0ca21-141">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0ca21-141">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca21-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ca21-142">Requirements</span></span>



| <span data-ttu-id="0ca21-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ca21-143">Requirement</span></span> | <span data-ttu-id="0ca21-144">Valore</span><span class="sxs-lookup"><span data-stu-id="0ca21-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca21-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ca21-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0ca21-146">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0ca21-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0ca21-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ca21-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0ca21-148">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0ca21-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ca21-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0ca21-149">Namespace</span></span><br/>                | <span data-ttu-id="0ca21-150">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0ca21-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0ca21-151">MOF</span><span class="sxs-lookup"><span data-stu-id="0ca21-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ca21-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ca21-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ca21-153">DLL</span><span class="sxs-lookup"><span data-stu-id="0ca21-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ca21-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0ca21-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0ca21-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ca21-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca21-156">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="0ca21-156">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

