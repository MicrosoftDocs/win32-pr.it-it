---
description: Mostra la metrica specificata.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Metodo ShowMetrics della classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9823ea61864b0d87245ebe8b171195a2fd3c411a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885150"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="c173b-103">Metodo ShowMetrics della classe MSVM \_ MetricService</span><span class="sxs-lookup"><span data-stu-id="c173b-103">ShowMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="c173b-104">Mostra la metrica specificata.</span><span class="sxs-lookup"><span data-stu-id="c173b-104">Shows the specified metrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="c173b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c173b-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c173b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c173b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c173b-107">*Oggetto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c173b-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c173b-108">Il parametro Subject identifica un'istanza di [**CIM \_ Managed**](cim-managedelement.md) per la quale il metodo restituisce riferimenti a istanze di [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) che definiscono le metriche acquisite per **CIM \_ managementelement**.</span><span class="sxs-lookup"><span data-stu-id="c173b-108">The Subject parameter identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="c173b-109">*Definizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c173b-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c173b-110">Il parametro Definition identifica un'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="c173b-110">The Definition parameter identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="c173b-111">Il metodo restituisce riferimenti a istanze di [**CIM \_ Managed**](cim-managedelement.md) per le quali è possibile raccogliere le metriche definite dall'istanza di **CIM \_ BaseMetricDefinition** .</span><span class="sxs-lookup"><span data-stu-id="c173b-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="c173b-112">*ManagedElements* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c173b-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c173b-113">Al completamento del metodo, il parametro *ManagedElements* \[ \] può contenere riferimenti a [**CIM \_ Managed**](cim-managedelement.md) per il quale la metrica identificata dal parametro *Definition* è disponibile per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="c173b-113">Upon successful completion of the method, the *ManagedElements*\[\] parameter may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) for which the metric identified by *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="c173b-114">*Definizione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c173b-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c173b-115">Al completamento del metodo, il parametro *definitionName* può contenere riferimenti a istanze di [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) che definiscono le metriche disponibili per la raccolta per l'oggetto [**\_ gestito CIM**](cim-managedelement.md) identificato dal parametro *Subject* .</span><span class="sxs-lookup"><span data-stu-id="c173b-115">Upon successful completion of the method, the *DefinitionList* parameter may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c173b-116">*MetricNames* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c173b-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c173b-117">Al completamento del metodo, ogni indice della matrice del parametro *MetricNames* deve contenere il valore della proprietà Name per l'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a cui fa riferimento l'indice della matrice corrispondente del parametro *Definition* .</span><span class="sxs-lookup"><span data-stu-id="c173b-117">Upon successful completion of the method, each array index of the *MetricNames* parameter shall contain the value of the Name property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c173b-118">*MetricCollectionEnabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c173b-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c173b-119">Il parametro *MetricCollectionEnabled* indica se viene raccolta una metrica per un elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="c173b-119">The *MetricCollectionEnabled* parameter indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="c173b-120">**Abilita** (2)</span><span class="sxs-lookup"><span data-stu-id="c173b-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="c173b-121">**Disabilita** (3)</span><span class="sxs-lookup"><span data-stu-id="c173b-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="c173b-122">**Riservato** (4)</span><span class="sxs-lookup"><span data-stu-id="c173b-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c173b-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="c173b-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c173b-124">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c173b-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="c173b-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c173b-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="c173b-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c173b-126">Return value</span></span>

<span data-ttu-id="c173b-127">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c173b-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c173b-128">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="c173b-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c173b-129">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="c173b-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c173b-130">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="c173b-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c173b-131">**Metodo riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="c173b-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c173b-132">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c173b-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c173b-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c173b-133">Requirements</span></span>



| <span data-ttu-id="c173b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c173b-134">Requirement</span></span> | <span data-ttu-id="c173b-135">Valore</span><span class="sxs-lookup"><span data-stu-id="c173b-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c173b-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c173b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c173b-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c173b-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c173b-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c173b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c173b-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c173b-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c173b-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c173b-140">Namespace</span></span><br/>                | <span data-ttu-id="c173b-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c173b-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c173b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c173b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c173b-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c173b-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c173b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c173b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c173b-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c173b-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c173b-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c173b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c173b-147">**\_MetricService MSVM**</span><span class="sxs-lookup"><span data-stu-id="c173b-147">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




