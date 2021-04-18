---
description: Aggiunge impostazioni generiche a una configurazione di sistema virtuale.
ms.assetid: ae04be39-0401-43e9-b19b-3539ca1786ec
title: Metodo AddSystemComponentSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56ca8bed752bab52f6a82e18975dd5df72dbe12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306010"
---
# <a name="addsystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="d2c88-103">Metodo AddSystemComponentSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="d2c88-103">AddSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="d2c88-104">Aggiunge impostazioni generiche a una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d2c88-104">Adds generic settings to a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c88-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2c88-105">Syntax</span></span>


```mof
uint32 AddSystemComponentSettings(
  [in]  Msvm_VirtualSystemSettingData   REF AffectedConfiguration,
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d2c88-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2c88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2c88-107">*AffectedConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2c88-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="d2c88-108">*ComponentSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2c88-108">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c88-109">Impostazioni del componente da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="d2c88-109">The component settings to add.</span></span>

</dd> <dt>

<span data-ttu-id="d2c88-110">*ResultingComponentSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d2c88-110">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c88-111">Se l'operazione riesce, fa riferimento a un [**\_ SystemComponentSettingData MSVM**](msvm-systemcomponentsettingdata.md) che contiene le impostazioni dei componenti risultanti.</span><span class="sxs-lookup"><span data-stu-id="d2c88-111">On success, references a [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that contains the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="d2c88-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="d2c88-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c88-113">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2c88-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2c88-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2c88-114">Return value</span></span>

<span data-ttu-id="d2c88-115">In caso di esito positivo, restituisce 0 o 4096; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="d2c88-115">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d2c88-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="d2c88-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2c88-117">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="d2c88-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2c88-118">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="d2c88-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2c88-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="d2c88-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2c88-120">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="d2c88-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2c88-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d2c88-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2c88-122">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="d2c88-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d2c88-123">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d2c88-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d2c88-124">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d2c88-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d2c88-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2c88-125">Requirements</span></span>



| <span data-ttu-id="d2c88-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2c88-126">Requirement</span></span> | <span data-ttu-id="d2c88-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d2c88-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c88-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2c88-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c88-129">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="d2c88-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d2c88-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2c88-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c88-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d2c88-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d2c88-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d2c88-132">Namespace</span></span><br/>                | <span data-ttu-id="d2c88-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d2c88-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d2c88-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d2c88-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2c88-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2c88-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2c88-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d2c88-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2c88-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2c88-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d2c88-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2c88-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2c88-139">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="d2c88-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

