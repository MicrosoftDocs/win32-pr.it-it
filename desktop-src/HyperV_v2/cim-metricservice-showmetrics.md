---
description: "Segnala quanto segue: le metriche disponibili per essere raccolte per un elemento gestito, gli elementi gestiti per i quali è disponibile una metrica definita da un'istanza di CIM \\_ BaseMetricDefinition e se è in corso la raccolta di una determinata metrica per un elemento gestito."
ms.assetid: 5af430d2-9ab3-4bee-ad51-d9045b51172a
title: Metodo ShowMetrics della classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1e0e062adaefd6c6d9bdabe6f168bd64e789acc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131747"
---
# <a name="showmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="e70e7-103">Metodo ShowMetrics della classe CIM \_ MetricService</span><span class="sxs-lookup"><span data-stu-id="e70e7-103">ShowMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="e70e7-104">Segnala quanto segue: le metriche disponibili per essere raccolte per un elemento gestito, gli elementi gestiti per i quali è disponibile una metrica definita da un'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) e se è in corso la raccolta di una determinata metrica per un elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="e70e7-104">Reports the following: the metrics available to be collected for a managed element, the managed elements for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e70e7-105">Syntax</span></span>


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="e70e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e70e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e70e7-107">*Oggetto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e70e7-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e70e7-108">Identifica un'istanza di [**CIM \_ Managed**](cim-managedelement.md) per la quale il metodo restituisce riferimenti a istanze di [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) che definiscono le metriche acquisite per **CIM \_ managementelement**.</span><span class="sxs-lookup"><span data-stu-id="e70e7-108">Identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="e70e7-109">*Definizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e70e7-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e70e7-110">Identifica un'istanza di [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="e70e7-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="e70e7-111">Il metodo restituisce riferimenti a istanze di [**CIM \_ Managed**](cim-managedelement.md) per le quali è possibile raccogliere le metriche definite dall'istanza di **CIM \_ BaseMetricDefinition** .</span><span class="sxs-lookup"><span data-stu-id="e70e7-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="e70e7-112">*ManagedElements* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e70e7-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e70e7-113">In presenza di esito positivo, può contenere riferimenti a oggetti [**CIM \_ gestitielement**](cim-managedelement.md) per i quali la metrica identificata dal parametro della *definizione* è disponibile per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="e70e7-113">On success, may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) objects for which the metric identified by the *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="e70e7-114">*Definizione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e70e7-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e70e7-115">In caso di esito positivo, può contenere riferimenti a istanze di oggetti [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) che definiscono le metriche disponibili per la raccolta per l'oggetto [**\_ gestito CIM**](cim-managedelement.md) identificato dal parametro *Subject* .</span><span class="sxs-lookup"><span data-stu-id="e70e7-115">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e70e7-116">*MetricNames* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e70e7-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e70e7-117">In caso di esito positivo, ogni indice di matrice deve contenere il valore della proprietà **Name** per l'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a cui fa riferimento l'indice della matrice corrispondente del parametro *Definition* .</span><span class="sxs-lookup"><span data-stu-id="e70e7-117">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e70e7-118">*MetricCollectionEnabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e70e7-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e70e7-119">Indica se viene raccolta una metrica per un elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="e70e7-119">Indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="e70e7-120">**Abilita** (2)</span><span class="sxs-lookup"><span data-stu-id="e70e7-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="e70e7-121">**Disabilita** (3)</span><span class="sxs-lookup"><span data-stu-id="e70e7-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="e70e7-122">**Riservato** (4)</span><span class="sxs-lookup"><span data-stu-id="e70e7-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e70e7-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="e70e7-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e70e7-124">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e70e7-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="e70e7-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e70e7-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="e70e7-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e70e7-126">Return value</span></span>

<span data-ttu-id="e70e7-127">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e70e7-127">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e70e7-128">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="e70e7-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e70e7-129">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="e70e7-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e70e7-130">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="e70e7-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e70e7-131">**Metodo riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="e70e7-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e70e7-132">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e70e7-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e70e7-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e70e7-133">Requirements</span></span>



| <span data-ttu-id="e70e7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e70e7-134">Requirement</span></span> | <span data-ttu-id="e70e7-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e70e7-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e70e7-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e70e7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e70e7-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e70e7-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e70e7-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e70e7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e70e7-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e70e7-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e70e7-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e70e7-140">Namespace</span></span><br/>                | <span data-ttu-id="e70e7-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e70e7-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e70e7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e70e7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e70e7-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e70e7-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e70e7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e70e7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e70e7-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e70e7-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e70e7-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e70e7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70e7-147">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e70e7-147">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




