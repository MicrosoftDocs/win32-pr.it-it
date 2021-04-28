---
description: 'Metodo ControlMetricsByClass della CIM_MetricService: abilita e disabilita la raccolta di metriche.'
ms.assetid: 1a53c7a7-c0fc-49d7-ad1b-d185d776ede5
title: Metodo ControlMetricsByClass della CIM_MetricService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fda8407d49ed3eec7ff86abc94ced6b63d2d77c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109709"
---
# <a name="controlmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="2e9e1-103">Metodo ControlMetricsByClass della classe \_ CIM MetricService</span><span class="sxs-lookup"><span data-stu-id="2e9e1-103">ControlMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="2e9e1-104">Abilita e disabilita la raccolta di metriche. **ControlMetricsByClass** viene usato per controllare la raccolta di ogni tipo di metrica per tutte le istanze di una classe o la raccolta di una metrica specifica per tutte le istanze di una classe.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-104">Enables and disables the collection of metrics.**ControlMetricsByClass** is used to control the collection of each type of metric for all instances of a class or the collection of a specific metric for all instances of a class.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e9e1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e9e1-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="2e9e1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e9e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e9e1-107">*Oggetto* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2e9e1-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9e1-108">Identifica la [**classe CIM \_ ManagedElement**](cim-managedelement.md) per cui verranno controllate le metriche.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-108">Identifies the [**CIM\_ManagedElement**](cim-managedelement.md) class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="2e9e1-109">*Definizione* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2e9e1-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9e1-110">Identifica una [**\_ baseMetricDefinition CIM**](cim-basemetricdefinition.md) per cui verranno controllate le metriche.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="2e9e1-111">*MetricCollectionEnabled* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2e9e1-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9e1-112">Indica l'operazione desiderata da eseguire sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="2e9e1-113">**Abilita** (2)</span><span class="sxs-lookup"><span data-stu-id="2e9e1-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="2e9e1-114">**Disabilita** (3)</span><span class="sxs-lookup"><span data-stu-id="2e9e1-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="2e9e1-115">**Reimposta** (4)</span><span class="sxs-lookup"><span data-stu-id="2e9e1-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2e9e1-116">**DmTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="2e9e1-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2e9e1-117">**Fornitore riservato** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="2e9e1-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="2e9e1-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2e9e1-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="2e9e1-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e9e1-119">Return value</span></span>

<span data-ttu-id="2e9e1-120">Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="2e9e1-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2e9e1-121">**Operazione** riuscita (0)</span><span class="sxs-lookup"><span data-stu-id="2e9e1-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2e9e1-122">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="2e9e1-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2e9e1-123">**Operazione non** riuscita (2)</span><span class="sxs-lookup"><span data-stu-id="2e9e1-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2e9e1-124">**Metodo riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="2e9e1-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2e9e1-125">**Specifico del** fornitore (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="2e9e1-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2e9e1-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e9e1-126">Requirements</span></span>



| <span data-ttu-id="2e9e1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e9e1-127">Requirement</span></span> | <span data-ttu-id="2e9e1-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2e9e1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e9e1-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e9e1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2e9e1-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2e9e1-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2e9e1-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e9e1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2e9e1-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2e9e1-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2e9e1-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2e9e1-133">Namespace</span></span><br/>                | <span data-ttu-id="2e9e1-134">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2e9e1-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2e9e1-135">MOF</span><span class="sxs-lookup"><span data-stu-id="2e9e1-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e9e1-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e9e1-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e9e1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2e9e1-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e9e1-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2e9e1-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2e9e1-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e9e1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e9e1-140">**CIM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="2e9e1-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




