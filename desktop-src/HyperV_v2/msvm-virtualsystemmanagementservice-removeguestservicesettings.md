---
description: Rimuove le impostazioni del servizio Guest da una configurazione di sistema virtuale.
ms.assetid: 33e55d74-adfd-4174-8f05-14e797a33806
title: Metodo RemoveGuestServiceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0aee1f8f9d729c093bff2a580e054d93fa7fc033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306004"
---
# <a name="removeguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="ed8e4-103">Metodo RemoveGuestServiceSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="ed8e4-103">RemoveGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ed8e4-104">Rimuove le impostazioni del servizio Guest da una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="ed8e4-104">Removes guest service settings from a virtual system configuration.</span></span>

<span data-ttu-id="ed8e4-105">Quando applicato alle parti di una configurazione di sistema virtuale "corrente", è possibile che vengano modificati i servizi guest di un effetto collaterale del sistema virtuale attivo.</span><span class="sxs-lookup"><span data-stu-id="ed8e4-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed8e4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed8e4-106">Syntax</span></span>


```mof
uint32 RemoveGuestServiceSettings(
  [in]  CIM_SettingData REF GuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ed8e4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed8e4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed8e4-108">*GuestServiceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed8e4-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8e4-109">Riferimento a una matrice di [**\_ SettingData CIM**](cim-settingdata.md) che descrivono l'impostazione del servizio Guest da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ed8e4-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the guest service setting to remove.</span></span>

</dd> <dt>

<span data-ttu-id="ed8e4-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ed8e4-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8e4-111">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ed8e4-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed8e4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed8e4-112">Return value</span></span>

<span data-ttu-id="ed8e4-113">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ed8e4-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ed8e4-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ed8e4-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ed8e4-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ed8e4-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ed8e4-116">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="ed8e4-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ed8e4-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="ed8e4-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ed8e4-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="ed8e4-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ed8e4-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="ed8e4-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ed8e4-120">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="ed8e4-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ed8e4-121">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="ed8e4-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ed8e4-122">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ed8e4-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ed8e4-123">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ed8e4-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ed8e4-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed8e4-124">Requirements</span></span>



| <span data-ttu-id="ed8e4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed8e4-125">Requirement</span></span> | <span data-ttu-id="ed8e4-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ed8e4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8e4-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed8e4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ed8e4-128">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ed8e4-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ed8e4-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed8e4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ed8e4-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ed8e4-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ed8e4-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed8e4-131">Namespace</span></span><br/>                | <span data-ttu-id="ed8e4-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ed8e4-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ed8e4-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ed8e4-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed8e4-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed8e4-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed8e4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ed8e4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed8e4-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ed8e4-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ed8e4-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed8e4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed8e4-138">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="ed8e4-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

