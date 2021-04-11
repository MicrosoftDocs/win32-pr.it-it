---
description: Crea una nuova istanza di macchina virtuale.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Metodo DefineSystem della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 965d24313607a767d546503d005a6493234b2f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232691"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="85e41-103">Metodo DefineSystem della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="85e41-103">DefineSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="85e41-104">Crea una nuova istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="85e41-104">Creates a new virtual machine instance.</span></span> <span data-ttu-id="85e41-105">Le proprietà non specificate verranno popolate con i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="85e41-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="85e41-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85e41-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="85e41-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="85e41-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85e41-108">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85e41-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e41-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="85e41-109">Type: **string**</span></span>

<span data-ttu-id="85e41-110">Istanza incorporata della classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) utilizzata per definire gli attributi della macchina virtuale da creare.</span><span class="sxs-lookup"><span data-stu-id="85e41-110">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is used to define the attributes of the virtual machine to be created.</span></span> <span data-ttu-id="85e41-111">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="85e41-111">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="85e41-112">*ResourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85e41-112">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e41-113">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="85e41-113">Type: **string\[\]**</span></span>

<span data-ttu-id="85e41-114">Numero di istanze incorporate della classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) (o delle relative classi derivate).</span><span class="sxs-lookup"><span data-stu-id="85e41-114">A number of embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class (or derived classes thereof).</span></span> <span data-ttu-id="85e41-115">Insieme, queste istanze descrivono le risorse virtuali della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="85e41-115">Together these instances describe the virtual resources of the virtual machine.</span></span> <span data-ttu-id="85e41-116">Verrà creato un set predefinito di dispositivi per la macchina virtuale, indipendentemente dal fatto che questo parametro sia impostato.</span><span class="sxs-lookup"><span data-stu-id="85e41-116">A default set of devices will be created for the virtual machine regardless of whether this parameter is set.</span></span> <span data-ttu-id="85e41-117">Il processore e la memoria, ad esempio, vengono creati e configurati automaticamente con i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="85e41-117">For example, processor and memory are automatically created and configured with default values.</span></span>

</dd> <dt>

<span data-ttu-id="85e41-118">*ReferenceConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85e41-118">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e41-119">Tipo: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="85e41-119">Type: **CIM\_VirtualSystemSettingData**</span></span>

<span data-ttu-id="85e41-120">Riferimento a un'istanza della classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta l'oggetto di primo livello di una configurazione di macchina virtuale di riferimento.</span><span class="sxs-lookup"><span data-stu-id="85e41-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is the top level object of a reference virtual machine configuration.</span></span> <span data-ttu-id="85e41-121">La configurazione di riferimento viene usata per completare la configurazione della nuova macchina virtuale se i parametri *SystemSettings* e *ResourceSettings* non forniscono le rispettive informazioni.</span><span class="sxs-lookup"><span data-stu-id="85e41-121">The reference configuration is used to complement the configuration of the new virtual machine if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="85e41-122">*ResultingSystem* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="85e41-122">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85e41-123">Tipo: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="85e41-123">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="85e41-124">Riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale appena creata.</span><span class="sxs-lookup"><span data-stu-id="85e41-124">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly created virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="85e41-125">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="85e41-125">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85e41-126">Tipo: **CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="85e41-126">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="85e41-127">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85e41-127">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85e41-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85e41-128">Return value</span></span>

<span data-ttu-id="85e41-129">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85e41-129">Type: **uint32**</span></span>

<span data-ttu-id="85e41-130">Se questo metodo viene eseguito in modo sincrono, restituisce 0 se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="85e41-130">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="85e41-131">Se questo metodo viene eseguito in modo asincrono, restituisce 4096 e il parametro di output del *processo* può essere usato per tenere traccia dello stato di avanzamento dell'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="85e41-131">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="85e41-132">Qualsiasi altro valore restituito indica un errore.</span><span class="sxs-lookup"><span data-stu-id="85e41-132">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="85e41-133">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="85e41-133">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85e41-134">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="85e41-134">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="85e41-135">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="85e41-135">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85e41-136">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="85e41-136">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85e41-137">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="85e41-137">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="85e41-138">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="85e41-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="85e41-139">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="85e41-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="85e41-140">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="85e41-140">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="85e41-141">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="85e41-141">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="85e41-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="85e41-142">Remarks</span></span>

<span data-ttu-id="85e41-143">L'accesso alla [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="85e41-143">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="85e41-144">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="85e41-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="85e41-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85e41-145">Requirements</span></span>



| <span data-ttu-id="85e41-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="85e41-146">Requirement</span></span> | <span data-ttu-id="85e41-147">Valore</span><span class="sxs-lookup"><span data-stu-id="85e41-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85e41-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85e41-148">Minimum supported client</span></span><br/> | <span data-ttu-id="85e41-149">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="85e41-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="85e41-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85e41-150">Minimum supported server</span></span><br/> | <span data-ttu-id="85e41-151">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="85e41-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85e41-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="85e41-152">Namespace</span></span><br/>                | <span data-ttu-id="85e41-153">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="85e41-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="85e41-154">MOF</span><span class="sxs-lookup"><span data-stu-id="85e41-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85e41-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85e41-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85e41-156">DLL</span><span class="sxs-lookup"><span data-stu-id="85e41-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85e41-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85e41-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="85e41-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85e41-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85e41-159">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="85e41-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

