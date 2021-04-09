---
description: Modifica le impostazioni del servizio Guest.
ms.assetid: a308aa59-bd43-4dd5-a690-c435102e8043
title: Metodo ModifyGuestServiceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bc0af24346c445022ba3f8725ea6102c61dc9c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878706"
---
# <a name="modifyguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="35a59-103">Metodo ModifyGuestServiceSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="35a59-103">ModifyGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="35a59-104">Modifica le impostazioni del servizio Guest.</span><span class="sxs-lookup"><span data-stu-id="35a59-104">Modifies guest service settings.</span></span>

<span data-ttu-id="35a59-105">Quando applicato alle parti di una configurazione di sistema virtuale "corrente", è possibile che vengano modificati i servizi guest di un effetto collaterale del sistema virtuale attivo.</span><span class="sxs-lookup"><span data-stu-id="35a59-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a59-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35a59-106">Syntax</span></span>


```mof
uint32 ModifyGuestServiceSettings(
  [in]  string              GuestServiceSettings[],
  [out] CIM_SettingData REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="35a59-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="35a59-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a59-108">*GuestServiceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35a59-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a59-109">Matrice che contiene le nuove impostazioni del servizio Guest.</span><span class="sxs-lookup"><span data-stu-id="35a59-109">An array that contains the new guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="35a59-110">*ResultingGuestServiceSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="35a59-110">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35a59-111">Se l'operazione riesce, contiains una matrice di [**\_ SettingData CIM**](cim-settingdata.md) che fanno riferimento alle impostazioni del servizio Guest risultante.</span><span class="sxs-lookup"><span data-stu-id="35a59-111">On success, contiains an array of [**CIM\_SettingData**](cim-settingdata.md) that reference the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="35a59-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="35a59-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35a59-113">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="35a59-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a59-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35a59-114">Return value</span></span>

<span data-ttu-id="35a59-115">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="35a59-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="35a59-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="35a59-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="35a59-117">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="35a59-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="35a59-118">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="35a59-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="35a59-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="35a59-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="35a59-120">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="35a59-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="35a59-121">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="35a59-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="35a59-122">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="35a59-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="35a59-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="35a59-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="35a59-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="35a59-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="35a59-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="35a59-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="35a59-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="35a59-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="35a59-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35a59-127">Requirements</span></span>



| <span data-ttu-id="35a59-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="35a59-128">Requirement</span></span> | <span data-ttu-id="35a59-129">Valore</span><span class="sxs-lookup"><span data-stu-id="35a59-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35a59-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35a59-130">Minimum supported client</span></span><br/> | <span data-ttu-id="35a59-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="35a59-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="35a59-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35a59-132">Minimum supported server</span></span><br/> | <span data-ttu-id="35a59-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="35a59-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="35a59-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35a59-134">Namespace</span></span><br/>                | <span data-ttu-id="35a59-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="35a59-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="35a59-136">MOF</span><span class="sxs-lookup"><span data-stu-id="35a59-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35a59-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35a59-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35a59-138">DLL</span><span class="sxs-lookup"><span data-stu-id="35a59-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35a59-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35a59-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="35a59-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35a59-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a59-141">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="35a59-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

