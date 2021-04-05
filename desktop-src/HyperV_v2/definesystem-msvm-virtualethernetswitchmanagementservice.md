---
description: Crea un nuovo commutire virtuale.
ms.assetid: de7495e9-48c5-427a-b9bb-0821b53a9b09
title: Metodo DefineSystem della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd6e2dfb7d9cf7e64fb76c35f6f3c3b8457d69d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883721"
---
# <a name="definesystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="72853-103">Metodo DefineSystem della classe MSVM \_ VirtualEthernetSwitchManagementService</span><span class="sxs-lookup"><span data-stu-id="72853-103">DefineSystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="72853-104">Crea un nuovo commutire virtuale.</span><span class="sxs-lookup"><span data-stu-id="72853-104">Creates a new virtual switch.</span></span> <span data-ttu-id="72853-105">Le proprietà non specificate verranno popolate con i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="72853-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="72853-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72853-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="72853-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="72853-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72853-108">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72853-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72853-109">Istanza incorporata della classe [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) utilizzata per definire gli attributi del commutere virtuale da creare.</span><span class="sxs-lookup"><span data-stu-id="72853-109">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that is used to define the attributes of the virtual switch to be created.</span></span> <span data-ttu-id="72853-110">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="72853-110">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="72853-111">*ResourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72853-111">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72853-112">Matrice di istanze incorporate della classe [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) che descrive le impostazioni delle porte di commutazione da creare nell'ambito del nuovo commutitore virtuale.</span><span class="sxs-lookup"><span data-stu-id="72853-112">An array of embedded instances of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that describes the settings of the switch ports to be created in the scope of the new virtual switch.</span></span> <span data-ttu-id="72853-113">Se viene specificato **null** , verrà creato il Commuter virtuale senza risorse (ovvero nessuna porta di commutazione).</span><span class="sxs-lookup"><span data-stu-id="72853-113">If **Null** is specified, the virtual switch will be created with no resources (i.e. no switch ports).</span></span>

</dd> <dt>

<span data-ttu-id="72853-114">*ReferenceConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72853-114">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72853-115">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="72853-115">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="72853-116">*ResultingSystem* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="72853-116">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72853-117">Se viene creato correttamente un commutire virtuale, un riferimento a un'istanza della classe [**\_ VirtualEthernetSwitch di MSVM**](msvm-virtualethernetswitch.md) che rappresenta il Commuter virtuale appena definito.</span><span class="sxs-lookup"><span data-stu-id="72853-117">If a virtual switch is successfully created, a reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the newly defined virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="72853-118">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="72853-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72853-119">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="72853-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72853-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72853-120">Return value</span></span>

<span data-ttu-id="72853-121">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="72853-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="72853-122">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="72853-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72853-123">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="72853-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="72853-124">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="72853-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="72853-125">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="72853-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="72853-126">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="72853-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="72853-127">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="72853-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="72853-128">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="72853-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="72853-129">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="72853-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="72853-130">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="72853-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="72853-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72853-131">Requirements</span></span>



| <span data-ttu-id="72853-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="72853-132">Requirement</span></span> | <span data-ttu-id="72853-133">Valore</span><span class="sxs-lookup"><span data-stu-id="72853-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72853-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72853-134">Minimum supported client</span></span><br/> | <span data-ttu-id="72853-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="72853-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="72853-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72853-136">Minimum supported server</span></span><br/> | <span data-ttu-id="72853-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="72853-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72853-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="72853-138">Namespace</span></span><br/>                | <span data-ttu-id="72853-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="72853-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="72853-140">MOF</span><span class="sxs-lookup"><span data-stu-id="72853-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72853-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72853-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72853-142">DLL</span><span class="sxs-lookup"><span data-stu-id="72853-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72853-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72853-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72853-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72853-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72853-145">**\_VirtualEthernetSwitchManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="72853-145">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

