---
description: Mostra le metriche per classe.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Metodo ShowMetricsByClass della classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93f132b24c6c20826b1551e979c128b1aa38c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311785"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="79819-103">Metodo ShowMetricsByClass della classe MSVM \_ MetricService</span><span class="sxs-lookup"><span data-stu-id="79819-103">ShowMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="79819-104">Mostra le metriche per classe.</span><span class="sxs-lookup"><span data-stu-id="79819-104">Shows metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="79819-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79819-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="79819-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="79819-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79819-107">*Oggetto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79819-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79819-108">Identifica una classe CIM per la quale il metodo restituisce riferimenti a istanze [**di \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) che definiscono le metriche che sono disponibili per l'acquisizione per tutte le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="79819-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="79819-109">*Definizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="79819-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79819-110">Identifica un'istanza di [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="79819-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="79819-111">Il metodo restituisce riferimenti a istanze di [**CIM \_ Managed**](cim-managedelement.md) per le quali è possibile raccogliere le metriche definite dall'istanza di **CIM \_ BaseMetricDefinition** .</span><span class="sxs-lookup"><span data-stu-id="79819-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="79819-112">*Definizione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="79819-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79819-113">Al completamento del metodo, può contenere riferimenti a istanze di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) che definiscono le metriche disponibili per la raccolta per l'oggetto [**\_ gestito CIM**](cim-managedelement.md) identificato dal parametro *Subject* .</span><span class="sxs-lookup"><span data-stu-id="79819-113">Upon successful completion of the method, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="79819-114">*MetricNames* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="79819-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79819-115">Al completamento del metodo, ogni indice di matrice contiene il valore della proprietà **Name** per l'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a cui fa riferimento l'indice della matrice corrispondente del parametro *Definition* .</span><span class="sxs-lookup"><span data-stu-id="79819-115">Upon successful completion of the method, each array index contains the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="79819-116">*MetricCollectionEnabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="79819-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79819-117">Indica se viene raccolta una metrica per tutte le istanze di una classe di elementi gestiti.</span><span class="sxs-lookup"><span data-stu-id="79819-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="79819-118">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="79819-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="79819-119">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="79819-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="79819-120">**Riservato** (4)</span><span class="sxs-lookup"><span data-stu-id="79819-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="79819-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="79819-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="79819-122">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="79819-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="79819-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="79819-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="79819-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79819-124">Return value</span></span>

<span data-ttu-id="79819-125">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="79819-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="79819-126">**Operazione riuscita** ()</span><span class="sxs-lookup"><span data-stu-id="79819-126">**Success** ()</span></span>
</dt> <dt>

<span data-ttu-id="79819-127">**Non supportato** ()</span><span class="sxs-lookup"><span data-stu-id="79819-127">**Not Supported** ()</span></span>
</dt> <dt>

<span data-ttu-id="79819-128">**Non riuscito** ()</span><span class="sxs-lookup"><span data-stu-id="79819-128">**Failed** ()</span></span>
</dt> <dt>

<span data-ttu-id="79819-129">**Metodo riservato** ()</span><span class="sxs-lookup"><span data-stu-id="79819-129">**Method Reserved** ()</span></span>
</dt> <dt>

<span data-ttu-id="79819-130">**Specifico del fornitore** ()</span><span class="sxs-lookup"><span data-stu-id="79819-130">**Vendor Specific** ()</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="79819-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79819-131">Requirements</span></span>



| <span data-ttu-id="79819-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="79819-132">Requirement</span></span> | <span data-ttu-id="79819-133">Valore</span><span class="sxs-lookup"><span data-stu-id="79819-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79819-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79819-134">Minimum supported client</span></span><br/> | <span data-ttu-id="79819-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="79819-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="79819-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79819-136">Minimum supported server</span></span><br/> | <span data-ttu-id="79819-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="79819-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="79819-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="79819-138">Namespace</span></span><br/>                | <span data-ttu-id="79819-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="79819-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="79819-140">MOF</span><span class="sxs-lookup"><span data-stu-id="79819-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79819-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79819-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79819-142">DLL</span><span class="sxs-lookup"><span data-stu-id="79819-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79819-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79819-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79819-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79819-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79819-145">**\_MetricService MSVM**</span><span class="sxs-lookup"><span data-stu-id="79819-145">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




