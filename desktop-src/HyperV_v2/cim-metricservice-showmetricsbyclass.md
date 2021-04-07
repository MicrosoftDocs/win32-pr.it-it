---
description: "Segnala quanto segue: le metriche disponibili per la raccolta per tutte le istanze di una classe CIM, le classi CIM per le quali è disponibile una metrica definita da un'istanza di CIM \\_ BaseMetricDefinition e se è in corso la raccolta di una determinata metrica per un elemento gestito."
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Metodo ShowMetricsByClass della classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f843c835e6c92e39c4ac1f9628d0479b94a691bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882185"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="b2272-103">Metodo ShowMetricsByClass della classe CIM \_ MetricService</span><span class="sxs-lookup"><span data-stu-id="b2272-103">ShowMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="b2272-104">Segnala quanto segue: le metriche disponibili per la raccolta per tutte le istanze di una classe CIM, le classi CIM per le quali è disponibile una metrica definita da un'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) e se è in corso la raccolta di una determinata metrica per un elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="b2272-104">Reports the following: the metrics available to be collected for all instances of a CIM class, The CIM classes for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2272-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2272-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="b2272-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2272-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2272-107">*Oggetto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2272-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2272-108">Identifica una classe CIM per la quale il metodo restituisce riferimenti a istanze [**di \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) che definiscono le metriche che sono disponibili per l'acquisizione per tutte le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="b2272-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="b2272-109">*Definizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b2272-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2272-110">Identifica un'istanza di [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="b2272-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="b2272-111">Il metodo restituisce riferimenti a istanze di [**CIM \_ Managed**](cim-managedelement.md) per le quali è possibile raccogliere le metriche definite dall'istanza di **CIM \_ BaseMetricDefinition** .</span><span class="sxs-lookup"><span data-stu-id="b2272-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="b2272-112">*Definizione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b2272-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2272-113">In caso di esito positivo, può contenere riferimenti a istanze di oggetti [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) che definiscono le metriche disponibili per la raccolta per l'oggetto [**\_ gestito CIM**](cim-managedelement.md) identificato dal parametro *Subject* .</span><span class="sxs-lookup"><span data-stu-id="b2272-113">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b2272-114">*MetricNames* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b2272-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2272-115">In caso di esito positivo, ogni indice di matrice deve contenere il valore della proprietà **Name** per l'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a cui fa riferimento l'indice della matrice corrispondente del parametro *Definition* .</span><span class="sxs-lookup"><span data-stu-id="b2272-115">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b2272-116">*MetricCollectionEnabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b2272-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2272-117">Indica se viene raccolta una metrica per tutte le istanze di una classe di elementi gestiti.</span><span class="sxs-lookup"><span data-stu-id="b2272-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b2272-118">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="b2272-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b2272-119">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="b2272-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="b2272-120">**Riservato** (4)</span><span class="sxs-lookup"><span data-stu-id="b2272-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b2272-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b2272-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b2272-122">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b2272-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="b2272-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b2272-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="b2272-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2272-124">Return value</span></span>

<span data-ttu-id="b2272-125">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="b2272-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b2272-126">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="b2272-126">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b2272-127">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="b2272-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b2272-128">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="b2272-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b2272-129">**Metodo riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b2272-129">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b2272-130">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b2272-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b2272-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2272-131">Requirements</span></span>



| <span data-ttu-id="b2272-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2272-132">Requirement</span></span> | <span data-ttu-id="b2272-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b2272-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2272-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2272-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b2272-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b2272-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b2272-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2272-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b2272-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b2272-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b2272-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b2272-138">Namespace</span></span><br/>                | <span data-ttu-id="b2272-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b2272-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b2272-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b2272-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2272-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2272-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2272-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b2272-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2272-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2272-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2272-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2272-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2272-145">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b2272-145">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




