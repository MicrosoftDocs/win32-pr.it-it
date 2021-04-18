---
description: Modifica le impostazioni delle funzionalità di una porta di commutazione Ethernet.
ms.assetid: 8c21a932-fffb-40fd-9166-d7e351329217
title: Metodo ModifyFeatureSettings della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0bee92019f9457a42a0c87ab619f7de1f7d203ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313860"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="7669c-103">Metodo ModifyFeatureSettings della classe MSVM \_ VirtualEthernetSwitchManagementService</span><span class="sxs-lookup"><span data-stu-id="7669c-103">ModifyFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="7669c-104">Modifica le impostazioni delle funzionalità di una porta di commutazione Ethernet.</span><span class="sxs-lookup"><span data-stu-id="7669c-104">Modifies the feature settings of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="7669c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7669c-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7669c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7669c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7669c-107">*FeatureSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7669c-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7669c-108">Matrice di stringhe che contengono un'istanza incorporata di una classe derivata dalla classe [**\_ FeatureSettingData di MSVM**](msvm-featuresettingdata.md) , che descrive le impostazioni della funzionalità della porta di commutazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="7669c-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the switch port feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="7669c-109">*ResultingFeatureSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7669c-109">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7669c-110">Matrice di riferimenti a istanze della classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) che rappresentano le impostazioni delle funzionalità modificate.</span><span class="sxs-lookup"><span data-stu-id="7669c-110">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="7669c-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="7669c-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7669c-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7669c-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7669c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7669c-113">Return value</span></span>

<span data-ttu-id="7669c-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7669c-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7669c-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="7669c-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7669c-116">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="7669c-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7669c-117">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="7669c-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7669c-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="7669c-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7669c-119">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="7669c-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7669c-120">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="7669c-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7669c-121">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="7669c-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7669c-122">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7669c-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7669c-123">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="7669c-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7669c-124">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7669c-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7669c-125">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7669c-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7669c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7669c-126">Requirements</span></span>



| <span data-ttu-id="7669c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7669c-127">Requirement</span></span> | <span data-ttu-id="7669c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="7669c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7669c-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7669c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7669c-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7669c-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7669c-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7669c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7669c-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7669c-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7669c-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7669c-133">Namespace</span></span><br/>                | <span data-ttu-id="7669c-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7669c-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7669c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="7669c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7669c-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7669c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7669c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7669c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7669c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7669c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7669c-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7669c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7669c-140">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="7669c-140">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="7669c-141">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="7669c-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="7669c-142">**\_VirtualEthernetSwitchManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="7669c-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

