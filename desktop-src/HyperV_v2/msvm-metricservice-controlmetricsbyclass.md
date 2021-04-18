---
description: Controlla le metriche in base alla classe.
ms.assetid: f848fdec-561b-4be0-b1e9-a59e15196d1d
title: Metodo ControlMetricsByClass della classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4149da6327edf774afda20e64f34ae0958f7c3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318337"
---
# <a name="controlmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="dd780-103">Metodo ControlMetricsByClass della classe MSVM \_ MetricService</span><span class="sxs-lookup"><span data-stu-id="dd780-103">ControlMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="dd780-104">Controlla le metriche in base alla classe.</span><span class="sxs-lookup"><span data-stu-id="dd780-104">Controls metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd780-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd780-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="dd780-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd780-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd780-107">*Oggetto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd780-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd780-108">Identifica la classe CIM per cui verranno controllate le metriche.</span><span class="sxs-lookup"><span data-stu-id="dd780-108">Identifies the CIM class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="dd780-109">*Definizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="dd780-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd780-110">Identifica un [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) per cui verranno controllate le metriche.</span><span class="sxs-lookup"><span data-stu-id="dd780-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="dd780-111">*MetricCollectionEnabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd780-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd780-112">Indica l'operazione desiderata da eseguire sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="dd780-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="dd780-113">**Abilita** (2)</span><span class="sxs-lookup"><span data-stu-id="dd780-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="dd780-114">**Disabilita** (3)</span><span class="sxs-lookup"><span data-stu-id="dd780-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="dd780-115">**Reimposta** (4)</span><span class="sxs-lookup"><span data-stu-id="dd780-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="dd780-116">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="dd780-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="dd780-117">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="dd780-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="dd780-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dd780-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="dd780-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd780-119">Return value</span></span>

<span data-ttu-id="dd780-120">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd780-120">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="dd780-121">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="dd780-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd780-122">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="dd780-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dd780-123">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="dd780-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dd780-124">**Metodo riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="dd780-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dd780-125">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="dd780-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dd780-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd780-126">Requirements</span></span>



| <span data-ttu-id="dd780-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd780-127">Requirement</span></span> | <span data-ttu-id="dd780-128">Valore</span><span class="sxs-lookup"><span data-stu-id="dd780-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd780-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd780-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd780-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dd780-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="dd780-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd780-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd780-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dd780-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="dd780-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dd780-133">Namespace</span></span><br/>                | <span data-ttu-id="dd780-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="dd780-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dd780-135">MOF</span><span class="sxs-lookup"><span data-stu-id="dd780-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd780-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd780-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd780-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dd780-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd780-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd780-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd780-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd780-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd780-140">**\_MetricService MSVM**</span><span class="sxs-lookup"><span data-stu-id="dd780-140">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




