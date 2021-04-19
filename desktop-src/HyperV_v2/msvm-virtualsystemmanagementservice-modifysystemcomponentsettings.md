---
description: Modifica le impostazioni del componente di sistema generico.
ms.assetid: e745be32-c26a-4343-99c8-950788243adf
title: Metodo ModifySystemComponentSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9495256d1b7610bebdac1fb2cc8b70960a63304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306008"
---
# <a name="modifysystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a6472-103">Metodo ModifySystemComponentSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="a6472-103">ModifySystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a6472-104">Modifica le impostazioni del componente di sistema generico.</span><span class="sxs-lookup"><span data-stu-id="a6472-104">Modifies generic system component settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6472-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6472-105">Syntax</span></span>


```mof
uint32 ModifySystemComponentSettings(
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a6472-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6472-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6472-107">*ComponentSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6472-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6472-108">Matrice di impostazioni del componente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="a6472-108">An array of component settings to update.</span></span>

</dd> <dt>

<span data-ttu-id="a6472-109">*ResultingComponentSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a6472-109">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6472-110">Se l'operazione riesce, restituisce una matrice di [**\_ SystemComponentSettingData MSVM**](msvm-systemcomponentsettingdata.md) che fanno riferimento alle impostazioni del componente risultante.</span><span class="sxs-lookup"><span data-stu-id="a6472-110">On success, returns an array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="a6472-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a6472-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6472-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a6472-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6472-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6472-113">Return value</span></span>

<span data-ttu-id="a6472-114">In caso di esito positivo, restituisce 0 o 4096; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="a6472-114">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a6472-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="a6472-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a6472-116">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="a6472-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a6472-117">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="a6472-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a6472-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="a6472-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a6472-119">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="a6472-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a6472-120">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="a6472-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a6472-121">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="a6472-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a6472-122">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="a6472-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a6472-123">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="a6472-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a6472-124">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a6472-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a6472-125">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a6472-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a6472-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6472-126">Requirements</span></span>



| <span data-ttu-id="a6472-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6472-127">Requirement</span></span> | <span data-ttu-id="a6472-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a6472-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6472-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6472-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a6472-130">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6472-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a6472-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6472-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a6472-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a6472-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a6472-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6472-133">Namespace</span></span><br/>                | <span data-ttu-id="a6472-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a6472-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a6472-135">MOF</span><span class="sxs-lookup"><span data-stu-id="a6472-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6472-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6472-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6472-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a6472-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6472-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a6472-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a6472-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6472-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6472-140">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="a6472-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

