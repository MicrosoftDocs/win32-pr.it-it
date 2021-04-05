---
description: Aggiunge le impostazioni della funzionalità alla configurazione di una porta di commutazione Ethernet.
ms.assetid: 628a6546-cc78-4fde-be0c-533a2c3f9483
title: Metodo AddFeatureSettings della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e3b46a26d3c67f5efce4944c8b2e874febced32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967559"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="a92e8-103">Metodo AddFeatureSettings della classe MSVM \_ VirtualEthernetSwitchManagementService</span><span class="sxs-lookup"><span data-stu-id="a92e8-103">AddFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="a92e8-104">Aggiunge le impostazioni della funzionalità alla configurazione di una porta di commutazione Ethernet.</span><span class="sxs-lookup"><span data-stu-id="a92e8-104">Adds feature settings to the configuration of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="a92e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a92e8-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  CIM_SettingData         REF AffectedConfiguration,
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a92e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a92e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a92e8-107">*AffectedConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a92e8-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a92e8-108">Riferimento a una classe derivata [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) che rappresenta la porta del compartitore Ethernet interessata o la configurazione del Commuter Ethernet.</span><span class="sxs-lookup"><span data-stu-id="a92e8-108">A reference to a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) derived class that represents the affected Ethernet switch port or Ethernet switch configuration.</span></span>

</dd> <dt>

<span data-ttu-id="a92e8-109">*FeatureSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a92e8-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a92e8-110">Matrice di stringhe che contengono un'istanza incorporata di una classe derivata dalla classe [**\_ FeatureSettingData di MSVM**](msvm-featuresettingdata.md) , che descrive le impostazioni della funzionalità da aggiungere alla configurazione della porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="a92e8-110">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the feature settings to be added to the switch port configuration.</span></span>

</dd> <dt>

<span data-ttu-id="a92e8-111">*ResultingFeatureSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a92e8-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a92e8-112">Matrice di riferimenti a istanze della classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) che rappresentano le impostazioni della funzionalità aggiunte.</span><span class="sxs-lookup"><span data-stu-id="a92e8-112">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="a92e8-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a92e8-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a92e8-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a92e8-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a92e8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a92e8-115">Return value</span></span>

<span data-ttu-id="a92e8-116">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a92e8-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a92e8-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="a92e8-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a92e8-118">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="a92e8-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a92e8-119">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="a92e8-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a92e8-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="a92e8-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a92e8-121">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="a92e8-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a92e8-122">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="a92e8-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a92e8-123">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="a92e8-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a92e8-124">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a92e8-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a92e8-125">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a92e8-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a92e8-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a92e8-126">Requirements</span></span>



| <span data-ttu-id="a92e8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a92e8-127">Requirement</span></span> | <span data-ttu-id="a92e8-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a92e8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a92e8-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a92e8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a92e8-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a92e8-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a92e8-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a92e8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a92e8-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a92e8-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a92e8-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a92e8-133">Namespace</span></span><br/>                | <span data-ttu-id="a92e8-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a92e8-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a92e8-135">MOF</span><span class="sxs-lookup"><span data-stu-id="a92e8-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a92e8-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a92e8-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a92e8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a92e8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a92e8-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a92e8-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a92e8-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a92e8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a92e8-140">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="a92e8-140">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="a92e8-141">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="a92e8-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="a92e8-142">**\_VirtualEthernetSwitchManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="a92e8-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

