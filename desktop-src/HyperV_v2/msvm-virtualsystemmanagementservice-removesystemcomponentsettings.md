---
description: Rimuove le impostazioni del componente generico da una configurazione di sistema virtuale.
ms.assetid: 54ddb960-65b7-409d-ad80-f3685562a1a1
title: Metodo RemoveSystemComponentSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93ef7b794b901212fad72a1fcdf6223d8344b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306002"
---
# <a name="removesystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="ae6fd-103">Metodo RemoveSystemComponentSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="ae6fd-103">RemoveSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ae6fd-104">Rimuove le impostazioni del componente generico da una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="ae6fd-104">Removes generic component settings from a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae6fd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae6fd-105">Syntax</span></span>


```mof
uint32 RemoveSystemComponentSettings(
  [in]  Msvm_SystemComponentSettingData REF ComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ae6fd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae6fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae6fd-107">*ComponentSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae6fd-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae6fd-108">Matrice di [**\_ SystemComponentSettingData MSVM**](msvm-systemcomponentsettingdata.md) che fanno riferimento alle impostazioni del componente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ae6fd-108">Array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the component settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="ae6fd-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ae6fd-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae6fd-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae6fd-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae6fd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae6fd-111">Return value</span></span>

<span data-ttu-id="ae6fd-112">Restituisce 0 o 4096 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ae6fd-112">Returns 0 or 4096 on a success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ae6fd-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ae6fd-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fd-114">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ae6fd-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fd-115">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="ae6fd-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fd-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="ae6fd-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fd-117">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="ae6fd-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fd-118">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="ae6fd-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fd-119">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="ae6fd-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fd-120">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="ae6fd-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fd-121">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ae6fd-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fd-122">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ae6fd-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ae6fd-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae6fd-123">Requirements</span></span>



| <span data-ttu-id="ae6fd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae6fd-124">Requirement</span></span> | <span data-ttu-id="ae6fd-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ae6fd-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6fd-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae6fd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ae6fd-127">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae6fd-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ae6fd-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae6fd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ae6fd-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ae6fd-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ae6fd-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ae6fd-130">Namespace</span></span><br/>                | <span data-ttu-id="ae6fd-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ae6fd-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ae6fd-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ae6fd-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae6fd-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae6fd-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae6fd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ae6fd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae6fd-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae6fd-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ae6fd-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae6fd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae6fd-137">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="ae6fd-137">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

