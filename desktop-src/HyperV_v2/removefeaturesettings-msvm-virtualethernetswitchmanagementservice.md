---
description: Rimuove le impostazioni della funzionalità da una porta di commutazione Ethernet.
ms.assetid: 3d45259e-34e4-417b-a895-4926b0eaaf59
title: Metodo RemoveFeatureSettings della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 919e2b69e2a0ef215a522c601088cb7aa2976a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314821"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="2e050-103">Metodo RemoveFeatureSettings della classe MSVM \_ VirtualEthernetSwitchManagementService</span><span class="sxs-lookup"><span data-stu-id="2e050-103">RemoveFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="2e050-104">Rimuove le impostazioni della funzionalità da una porta di commutazione Ethernet.</span><span class="sxs-lookup"><span data-stu-id="2e050-104">Removes feature settings from an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e050-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e050-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_FeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2e050-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e050-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e050-107">*FeatureSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e050-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e050-108">Matrice di riferimenti a istanze della classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) che rappresentano le impostazioni della funzionalità da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2e050-108">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="2e050-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="2e050-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e050-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2e050-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e050-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e050-111">Return value</span></span>

<span data-ttu-id="2e050-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e050-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2e050-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="2e050-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2e050-114">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="2e050-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2e050-115">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="2e050-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2e050-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="2e050-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2e050-117">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="2e050-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2e050-118">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="2e050-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2e050-119">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="2e050-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2e050-120">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="2e050-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2e050-121">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="2e050-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2e050-122">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2e050-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2e050-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e050-123">Requirements</span></span>



| <span data-ttu-id="2e050-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e050-124">Requirement</span></span> | <span data-ttu-id="2e050-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2e050-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e050-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e050-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2e050-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2e050-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2e050-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e050-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2e050-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2e050-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e050-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2e050-130">Namespace</span></span><br/>                | <span data-ttu-id="2e050-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2e050-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2e050-132">MOF</span><span class="sxs-lookup"><span data-stu-id="2e050-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e050-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e050-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e050-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2e050-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e050-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2e050-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2e050-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e050-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e050-137">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="2e050-137">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="2e050-138">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="2e050-138">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="2e050-139">**\_VirtualEthernetSwitchManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="2e050-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

