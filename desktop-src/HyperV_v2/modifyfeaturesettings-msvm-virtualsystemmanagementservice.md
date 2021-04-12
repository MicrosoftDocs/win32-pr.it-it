---
description: Modifica le impostazioni correnti della funzionalità di una connessione Ethernet della macchina virtuale.
ms.assetid: 3caa810f-0444-45cf-88a4-e93d04accb46
title: Metodo ModifyFeatureSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c376158008c5ad0e611d3a05c7e73d2e7d1b44cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346066"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="90630-103">Metodo ModifyFeatureSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="90630-103">ModifyFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="90630-104">Modifica le impostazioni correnti della funzionalità di una connessione Ethernet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="90630-104">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="90630-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90630-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="90630-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="90630-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90630-107">*FeatureSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90630-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90630-108">Matrice di stringhe che contengono un'istanza incorporata di una classe derivata dalla classe [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) , che descrive le modifiche apportate alle impostazioni della funzionalità corrente di una connessione Ethernet esistente.</span><span class="sxs-lookup"><span data-stu-id="90630-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that describes modifications to the current feature settings of an existing Ethernet connection.</span></span> <span data-ttu-id="90630-109">La proprietà **InstanceID** di ognuna di queste istanze identifica le impostazioni della funzionalità da modificare.</span><span class="sxs-lookup"><span data-stu-id="90630-109">The **InstanceID** property of each of these instances identifies the feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="90630-110">*ResultingFeatureSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="90630-110">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90630-111">Matrice di riferimenti a istanze della classe [**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) che rappresentano le impostazioni delle funzionalità modificate.</span><span class="sxs-lookup"><span data-stu-id="90630-111">An array of references to instances of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="90630-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="90630-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90630-113">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="90630-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90630-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90630-114">Return value</span></span>

<span data-ttu-id="90630-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="90630-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="90630-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="90630-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="90630-117">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="90630-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="90630-118">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="90630-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="90630-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="90630-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="90630-120">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="90630-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="90630-121">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="90630-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="90630-122">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="90630-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="90630-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="90630-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="90630-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="90630-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="90630-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="90630-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="90630-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="90630-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="90630-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90630-127">Requirements</span></span>



| <span data-ttu-id="90630-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="90630-128">Requirement</span></span> | <span data-ttu-id="90630-129">Valore</span><span class="sxs-lookup"><span data-stu-id="90630-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90630-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90630-130">Minimum supported client</span></span><br/> | <span data-ttu-id="90630-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="90630-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="90630-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90630-132">Minimum supported server</span></span><br/> | <span data-ttu-id="90630-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="90630-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90630-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="90630-134">Namespace</span></span><br/>                | <span data-ttu-id="90630-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="90630-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="90630-136">MOF</span><span class="sxs-lookup"><span data-stu-id="90630-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90630-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90630-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90630-138">DLL</span><span class="sxs-lookup"><span data-stu-id="90630-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90630-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90630-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90630-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90630-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90630-141">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="90630-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

