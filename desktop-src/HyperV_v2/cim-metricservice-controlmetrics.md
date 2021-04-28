---
description: 'Metodo ControlMetrics della classe CIM_MetricService: abilita e disabilita la raccolta di metriche.'
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Metodo ControlMetrics della CIM_MetricService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 19e732e50f8c367463e7f528a520a736117999b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090869"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="f525b-103">Metodo ControlMetrics della classe \_ CIM MetricService</span><span class="sxs-lookup"><span data-stu-id="f525b-103">ControlMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="f525b-104">Abilita e disabilita la raccolta di metriche. **ControlMetrics** viene usato per controllare la raccolta di ogni tipo di metrica per un Elemento gestito [**CIM, \_**](cim-managedelement.md)la raccolta di un determinato tipo di metrica per tutti gli elementi gestiti o la raccolta di una metrica specifica per un elemento gestito specifico.</span><span class="sxs-lookup"><span data-stu-id="f525b-104">Enables and disables the collection of metrics.**ControlMetrics** is used to control the collection of each type of metric for a [**CIM\_ManagedElement**](cim-managedelement.md), the collection of a given type of metric for all managed elements, or the collection of a specific metric for a specific managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="f525b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f525b-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="f525b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f525b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f525b-107">*Oggetto* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f525b-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f525b-108">[**ManagedElement \_ CIM**](cim-managedelement.md) che identifica gli elementi gestiti per i quali verranno controllate le metriche.</span><span class="sxs-lookup"><span data-stu-id="f525b-108">A [**CIM\_ManagedElement**](cim-managedelement.md) that identifies managed element(s) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="f525b-109">*Definizione* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f525b-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f525b-110">Identifica un [**oggetto \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) per il quale verranno controllate le metriche.</span><span class="sxs-lookup"><span data-stu-id="f525b-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="f525b-111">*MetricCollectionEnabled* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f525b-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f525b-112">Indica l'operazione desiderata da eseguire sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="f525b-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="f525b-113">**Abilita** (2)</span><span class="sxs-lookup"><span data-stu-id="f525b-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="f525b-114">**Disabilita** (3)</span><span class="sxs-lookup"><span data-stu-id="f525b-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="f525b-115">**Reimpostazione** (4)</span><span class="sxs-lookup"><span data-stu-id="f525b-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f525b-116">**DmTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="f525b-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f525b-117">**Vendor Reserved** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="f525b-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="f525b-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f525b-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="f525b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f525b-119">Return value</span></span>

<span data-ttu-id="f525b-120">Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="f525b-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f525b-121">**Operazione** riuscita (0)</span><span class="sxs-lookup"><span data-stu-id="f525b-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f525b-122">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="f525b-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f525b-123">**Operazione non** riuscita (2)</span><span class="sxs-lookup"><span data-stu-id="f525b-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f525b-124">**Metodo riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f525b-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f525b-125">**Specifico del** fornitore (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="f525b-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f525b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f525b-126">Requirements</span></span>



| <span data-ttu-id="f525b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f525b-127">Requirement</span></span> | <span data-ttu-id="f525b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="f525b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f525b-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f525b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f525b-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f525b-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f525b-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f525b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f525b-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f525b-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f525b-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f525b-133">Namespace</span></span><br/>                | <span data-ttu-id="f525b-134">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f525b-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f525b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f525b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f525b-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="f525b-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f525b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f525b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f525b-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f525b-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f525b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f525b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f525b-140">**CIM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="f525b-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




