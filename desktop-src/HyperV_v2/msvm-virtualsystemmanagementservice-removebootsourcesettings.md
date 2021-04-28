---
description: 'Metodo RemoveBootSourceSettings della classe Msvm_VirtualSystemManagementService : rimuove le impostazioni delle risorse virtuali da una configurazione di sistema virtuale.'
ms.assetid: 0deb7719-e605-4ba5-9bb2-037d0cafee24
title: Metodo RemoveBootSourceSettings della Msvm_VirtualSystemManagementService classe
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
ms.openlocfilehash: 5407e56b761dd545d20b89e0a28742f9c542b15a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109399"
---
# <a name="removebootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="3667b-103">Metodo RemoveBootSourceSettings della classe Msvm \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="3667b-103">RemoveBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="3667b-104">Rimuove le impostazioni delle risorse virtuali da una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="3667b-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="3667b-105">Se applicato a parti di una configurazione di sistema virtuale "corrente", come effetto collaterale le risorse del sistema virtuale attivo possono essere rimosse.</span><span class="sxs-lookup"><span data-stu-id="3667b-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3667b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3667b-106">Syntax</span></span>


```mof
uint32 RemoveBootSourceSettings(
  [in]  CIM_SettingData REF BootSourceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3667b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3667b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3667b-108">*BootSourceSettings* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3667b-108">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3667b-109">Riferimento a una matrice di [**CIM \_ SettingData**](cim-settingdata.md) che descrivono le impostazioni dell'origine di avvio da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3667b-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the boot source settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="3667b-110">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3667b-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3667b-111">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3667b-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3667b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3667b-112">Return value</span></span>

<span data-ttu-id="3667b-113">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3667b-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="3667b-114">**Completata senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="3667b-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3667b-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="3667b-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3667b-116">**Operazione non** riuscita (2)</span><span class="sxs-lookup"><span data-stu-id="3667b-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3667b-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="3667b-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3667b-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="3667b-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3667b-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="3667b-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3667b-120">**DmTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="3667b-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3667b-121">**Parametri del metodo verificati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="3667b-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3667b-122">**Metodo riservato** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="3667b-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3667b-123">**Specifico del** fornitore (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="3667b-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3667b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3667b-124">Requirements</span></span>



| <span data-ttu-id="3667b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3667b-125">Requirement</span></span> | <span data-ttu-id="3667b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3667b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3667b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3667b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3667b-128">Windows 10 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3667b-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3667b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3667b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3667b-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3667b-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3667b-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3667b-131">Namespace</span></span><br/>                | <span data-ttu-id="3667b-132">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3667b-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3667b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="3667b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3667b-134"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="3667b-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3667b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3667b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3667b-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3667b-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3667b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3667b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3667b-138">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="3667b-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

