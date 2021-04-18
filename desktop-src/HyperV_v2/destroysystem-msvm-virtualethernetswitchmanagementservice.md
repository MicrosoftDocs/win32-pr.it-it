---
description: Elimina definitivamente un commutire virtuale.
ms.assetid: f0b6b4cc-e9b7-4255-a9e1-a2a826b8f119
title: Metodo DestroySystem della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d8f01a3f72d15fba908c7891f76b4128a1ee8200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315512"
---
# <a name="destroysystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="4af81-103">Metodo DestroySystem della classe MSVM \_ VirtualEthernetSwitchManagementService</span><span class="sxs-lookup"><span data-stu-id="4af81-103">DestroySystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="4af81-104">Elimina definitivamente un commutire virtuale.</span><span class="sxs-lookup"><span data-stu-id="4af81-104">Destroys a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="4af81-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4af81-105">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4af81-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4af81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4af81-107">*AffectedSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4af81-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4af81-108">Riferimento a un'istanza della classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) che rappresenta il Commuter virtuale da eliminare definitivamente.</span><span class="sxs-lookup"><span data-stu-id="4af81-108">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="4af81-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4af81-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4af81-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4af81-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4af81-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4af81-111">Return value</span></span>

<span data-ttu-id="4af81-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4af81-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4af81-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="4af81-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4af81-114">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="4af81-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4af81-115">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="4af81-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4af81-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="4af81-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4af81-117">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="4af81-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4af81-118">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="4af81-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4af81-119">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="4af81-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4af81-120">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="4af81-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4af81-121">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4af81-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="4af81-122">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="4af81-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4af81-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4af81-123">Requirements</span></span>



| <span data-ttu-id="4af81-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4af81-124">Requirement</span></span> | <span data-ttu-id="4af81-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4af81-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4af81-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4af81-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4af81-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4af81-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4af81-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4af81-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4af81-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4af81-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4af81-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4af81-130">Namespace</span></span><br/>                | <span data-ttu-id="4af81-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4af81-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4af81-132">MOF</span><span class="sxs-lookup"><span data-stu-id="4af81-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4af81-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4af81-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4af81-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4af81-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4af81-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4af81-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4af81-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4af81-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4af81-137">**\_VirtualEthernetSwitchManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="4af81-137">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

