---
description: Aggiorna le impostazioni per un disco rigido virtuale.
ms.assetid: 10f80313-bc78-447e-bdf2-5635d7354e3c
title: Metodo SetVirtualHardDiskSettingData della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 969e9019d05b49f2f171f2177e1e74f135e212da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349031"
---
# <a name="setvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="f792c-103">Metodo SetVirtualHardDiskSettingData della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="f792c-103">SetVirtualHardDiskSettingData method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="f792c-104">Aggiorna le impostazioni per un disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="f792c-104">Updates the settings for a virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="f792c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f792c-105">Syntax</span></span>


```mof
uint32 SetVirtualHardDiskSettingData(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f792c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f792c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f792c-107">*VirtualDiskSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f792c-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f792c-108">Rappresentazione di stringa della classe [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) che specifica il disco rigido virtuale da aggiornare e contenente i nuovi dati di impostazione.</span><span class="sxs-lookup"><span data-stu-id="f792c-108">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the virtual hard disk to update and that contains the new setting data.</span></span> <span data-ttu-id="f792c-109">Con questo metodo è possibile aggiornare solo le proprietà **ParentPath**, **PhysicalSectorSize** o **VirtualDiskId** .</span><span class="sxs-lookup"><span data-stu-id="f792c-109">Only the **ParentPath**, **PhysicalSectorSize**, or **VirtualDiskId** properties can be updated with this method.</span></span> <span data-ttu-id="f792c-110">Non è possibile aggiornare queste proprietà con una chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="f792c-110">You can't update these properties with one method call.</span></span> <span data-ttu-id="f792c-111">È possibile aggiornare solo una di queste proprietà con una singola chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="f792c-111">You can only update one of these properties with a single method call.</span></span>

</dd> <dt>

<span data-ttu-id="f792c-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f792c-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f792c-113">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f792c-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f792c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f792c-114">Return value</span></span>

<span data-ttu-id="f792c-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f792c-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f792c-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="f792c-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="f792c-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="f792c-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="f792c-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="f792c-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="f792c-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="f792c-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f792c-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-124">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f792c-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="f792c-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f792c-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="f792c-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f792c-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f792c-129">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="f792c-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f792c-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="f792c-130">Remarks</span></span>

<span data-ttu-id="f792c-131">L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="f792c-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f792c-132">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f792c-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f792c-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f792c-133">Requirements</span></span>



| <span data-ttu-id="f792c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f792c-134">Requirement</span></span> | <span data-ttu-id="f792c-135">Valore</span><span class="sxs-lookup"><span data-stu-id="f792c-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f792c-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f792c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f792c-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f792c-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f792c-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f792c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f792c-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f792c-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f792c-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f792c-140">Namespace</span></span><br/>                | <span data-ttu-id="f792c-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f792c-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f792c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f792c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f792c-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f792c-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f792c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f792c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f792c-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f792c-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f792c-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f792c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f792c-147">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="f792c-147">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

