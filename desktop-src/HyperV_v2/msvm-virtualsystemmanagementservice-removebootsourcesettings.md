---
description: Rimuove le impostazioni delle risorse virtuali da una configurazione di sistema virtuale.
ms.assetid: 0deb7719-e605-4ba5-9bb2-037d0cafee24
title: Metodo RemoveBootSourceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2693be33d291ea5a975119a5478af580ef2bb3f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306007"
---
# <a name="removebootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="ac1cf-103">Metodo RemoveBootSourceSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="ac1cf-103">RemoveBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ac1cf-104">Rimuove le impostazioni delle risorse virtuali da una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="ac1cf-105">Quando applicato alle parti di una configurazione di sistema virtuale "corrente", è possibile che vengano rimosse le risorse degli effetti collaterali del sistema virtuale attivo.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1cf-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac1cf-106">Syntax</span></span>


```mof
uint32 RemoveBootSourceSettings(
  [in]  CIM_SettingData REF BootSourceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ac1cf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac1cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac1cf-108">*BootSourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac1cf-108">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1cf-109">Riferimento a una matrice di [**\_ SettingData CIM**](cim-settingdata.md) che descrivono le impostazioni dell'origine di avvio da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the boot source settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="ac1cf-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ac1cf-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1cf-111">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac1cf-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac1cf-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac1cf-112">Return value</span></span>

<span data-ttu-id="ac1cf-113">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ac1cf-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ac1cf-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ac1cf-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ac1cf-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ac1cf-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ac1cf-116">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="ac1cf-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ac1cf-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="ac1cf-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ac1cf-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="ac1cf-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ac1cf-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="ac1cf-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ac1cf-120">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="ac1cf-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ac1cf-121">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="ac1cf-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ac1cf-122">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ac1cf-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ac1cf-123">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ac1cf-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ac1cf-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac1cf-124">Requirements</span></span>



| <span data-ttu-id="ac1cf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac1cf-125">Requirement</span></span> | <span data-ttu-id="ac1cf-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ac1cf-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1cf-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac1cf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ac1cf-128">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ac1cf-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ac1cf-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac1cf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ac1cf-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ac1cf-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ac1cf-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ac1cf-131">Namespace</span></span><br/>                | <span data-ttu-id="ac1cf-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ac1cf-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ac1cf-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ac1cf-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac1cf-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac1cf-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac1cf-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ac1cf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac1cf-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac1cf-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ac1cf-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac1cf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac1cf-138">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="ac1cf-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

