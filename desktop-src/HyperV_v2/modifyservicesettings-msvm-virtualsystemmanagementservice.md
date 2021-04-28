---
description: "Metodo ModifyServiceSettings della classe Msvm_VirtualSystemManagementService: modifica i dati dell'impostazione per il servizio."
ms.assetid: 1CA49922-894D-4AA1-B741-6A0DC9F5654E
title: Metodo ModifyServiceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee4e8ae904292bae06770f23cf6c853d5e5448bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112169"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="93c7e-103">Metodo ModifyServiceSettings della classe Msvm \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="93c7e-103">ModifyServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="93c7e-104">Modifica i dati dell'impostazione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="93c7e-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c7e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93c7e-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="93c7e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="93c7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c7e-107">*Impostazione dei dati* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="93c7e-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93c7e-108">Tipo: **string**</span><span class="sxs-lookup"><span data-stu-id="93c7e-108">Type: **string**</span></span>

<span data-ttu-id="93c7e-109">Istanza incorporata della [**classe Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) che contiene gli aspetti modificati del servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="93c7e-109">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the modified aspects of the existing service.</span></span>

</dd> <dt>

<span data-ttu-id="93c7e-110">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="93c7e-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93c7e-111">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="93c7e-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="93c7e-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93c7e-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c7e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93c7e-113">Return value</span></span>

<span data-ttu-id="93c7e-114">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="93c7e-114">Type: **uint32**</span></span>

<span data-ttu-id="93c7e-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="93c7e-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="93c7e-116">**Completata senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="93c7e-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93c7e-117">**Parametri del metodo verificati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="93c7e-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="93c7e-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="93c7e-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="93c7e-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="93c7e-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="93c7e-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="93c7e-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="93c7e-121">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="93c7e-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="93c7e-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="93c7e-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="93c7e-123">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="93c7e-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="93c7e-124">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="93c7e-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="93c7e-125">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="93c7e-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="93c7e-126">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="93c7e-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="93c7e-127">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="93c7e-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="93c7e-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="93c7e-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="93c7e-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="93c7e-129">Remarks</span></span>

<span data-ttu-id="93c7e-130">L'accesso alla [**classe Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtro del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="93c7e-130">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="93c7e-131">Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="93c7e-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="93c7e-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93c7e-132">Requirements</span></span>



| <span data-ttu-id="93c7e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="93c7e-133">Requirement</span></span> | <span data-ttu-id="93c7e-134">Valore</span><span class="sxs-lookup"><span data-stu-id="93c7e-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93c7e-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93c7e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="93c7e-136">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="93c7e-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="93c7e-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93c7e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="93c7e-138">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="93c7e-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93c7e-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="93c7e-139">Namespace</span></span><br/>                | <span data-ttu-id="93c7e-140">Virtualizzazione \\ radice \\ V2</span><span class="sxs-lookup"><span data-stu-id="93c7e-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93c7e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="93c7e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93c7e-142"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="93c7e-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93c7e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="93c7e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93c7e-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93c7e-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93c7e-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93c7e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c7e-146">**ModifyServiceSettings (V1)**</span><span class="sxs-lookup"><span data-stu-id="93c7e-146">**ModifyServiceSettings (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyservicesettings-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="93c7e-147">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="93c7e-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="93c7e-148">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93c7e-148">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> </dl>

 

