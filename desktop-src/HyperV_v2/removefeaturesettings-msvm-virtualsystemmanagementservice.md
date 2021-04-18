---
description: Rimuove le impostazioni della funzionalità da una connessione Ethernet della macchina virtuale.
ms.assetid: 457056d0-7e69-47e4-8744-0136a1816f4a
title: Metodo RemoveFeatureSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c29151f6544d7eb803ec72ee49e455556d8b2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314820"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="7ff3a-103">Metodo RemoveFeatureSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="7ff3a-103">RemoveFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7ff3a-104">Rimuove le impostazioni della funzionalità da una connessione Ethernet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7ff3a-104">Removes feature settings from a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff3a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ff3a-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_EthernetSwitchPortFeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7ff3a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ff3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ff3a-107">*FeatureSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ff3a-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff3a-108">Matrice di stringhe che contengono un'istanza incorporata di una classe derivata dalla classe [**\_ EthernetSwitchFeatureSettingData di MSVM**](msvm-ethernetswitchfeaturesettingdata.md) , che definisce le impostazioni della funzionalità da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7ff3a-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that defines the feature settings to be removed.</span></span> <span data-ttu-id="7ff3a-109">La proprietà **InstanceID** di ognuna di queste istanze identifica le impostazioni della funzionalità da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7ff3a-109">The **InstanceID** property of each of these instances identifies the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="7ff3a-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="7ff3a-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff3a-111">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7ff3a-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ff3a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ff3a-112">Return value</span></span>

<span data-ttu-id="7ff3a-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ff3a-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7ff3a-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="7ff3a-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7ff3a-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="7ff3a-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7ff3a-116">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="7ff3a-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7ff3a-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="7ff3a-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7ff3a-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="7ff3a-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7ff3a-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="7ff3a-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7ff3a-120">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7ff3a-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7ff3a-121">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="7ff3a-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7ff3a-122">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7ff3a-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7ff3a-123">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7ff3a-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7ff3a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ff3a-124">Requirements</span></span>



| <span data-ttu-id="7ff3a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ff3a-125">Requirement</span></span> | <span data-ttu-id="7ff3a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7ff3a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff3a-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ff3a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff3a-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7ff3a-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7ff3a-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ff3a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff3a-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7ff3a-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ff3a-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7ff3a-131">Namespace</span></span><br/>                | <span data-ttu-id="7ff3a-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7ff3a-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7ff3a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="7ff3a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ff3a-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ff3a-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ff3a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7ff3a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ff3a-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ff3a-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7ff3a-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ff3a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff3a-138">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="7ff3a-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

