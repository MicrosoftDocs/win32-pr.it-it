---
description: Aggiunge le impostazioni delle funzionalità Ethernet alla configurazione di una connessione Ethernet della macchina virtuale.
ms.assetid: f233bf2f-5201-4b02-8384-bb7e2d1e7dee
title: Metodo AddFeatureSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9acbaaf6ff1da6439dcb243869e09133e0031e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345561"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="49241-103">Metodo AddFeatureSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="49241-103">AddFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="49241-104">Aggiunge le impostazioni delle funzionalità Ethernet alla configurazione di una connessione Ethernet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="49241-104">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="49241-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49241-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  Msvm_EthernetPortAllocationSettingData    REF AffectedConfiguration,
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="49241-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49241-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49241-107">*AffectedConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49241-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49241-108">Riferimento a un'istanza della classe [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) che rappresenta la connessione Ethernet interessata.</span><span class="sxs-lookup"><span data-stu-id="49241-108">Reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the affected Ethernet connection.</span></span>

</dd> <dt>

<span data-ttu-id="49241-109">*FeatureSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49241-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49241-110">Matrice di stringhe che contengono un'istanza incorporata della classe [**\_ EthernetSwitchFeatureSettingData MSVM**](msvm-ethernetswitchfeaturesettingdata.md) che descrive le impostazioni della funzionalità da aggiungere alla configurazione della connessione.</span><span class="sxs-lookup"><span data-stu-id="49241-110">An array of strings that contain one embedded instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that describes the feature settings to be added to the connection configuration.</span></span>

</dd> <dt>

<span data-ttu-id="49241-111">*ResultingFeatureSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="49241-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49241-112">Matrice di riferimenti a istanze della classe [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) che rappresenta le impostazioni della funzionalità aggiunte.</span><span class="sxs-lookup"><span data-stu-id="49241-112">An array of references to instances of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="49241-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="49241-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49241-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="49241-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49241-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49241-115">Return value</span></span>

<span data-ttu-id="49241-116">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="49241-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="49241-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="49241-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="49241-118">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="49241-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="49241-119">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="49241-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="49241-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="49241-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="49241-121">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="49241-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="49241-122">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="49241-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="49241-123">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="49241-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="49241-124">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="49241-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="49241-125">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="49241-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="49241-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49241-126">Requirements</span></span>



| <span data-ttu-id="49241-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="49241-127">Requirement</span></span> | <span data-ttu-id="49241-128">Valore</span><span class="sxs-lookup"><span data-stu-id="49241-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49241-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49241-129">Minimum supported client</span></span><br/> | <span data-ttu-id="49241-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="49241-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="49241-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49241-131">Minimum supported server</span></span><br/> | <span data-ttu-id="49241-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="49241-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49241-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="49241-133">Namespace</span></span><br/>                | <span data-ttu-id="49241-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="49241-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="49241-135">MOF</span><span class="sxs-lookup"><span data-stu-id="49241-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49241-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49241-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="49241-137">DLL</span><span class="sxs-lookup"><span data-stu-id="49241-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49241-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="49241-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="49241-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49241-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49241-140">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="49241-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

