---
description: Rappresenta un'associazione in cui un \_ oggetto CIM BaseMetricDefinition definisce le metriche per un elemento gestito.
ms.assetid: 10905038-fc23-4018-bae8-f336e4f001e7
title: Classe CIM_MetricDefForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricDefForME
- CIM_MetricDefForME.Antecedent
- CIM_MetricDefForME.Dependent
- CIM_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d0bcc115bdb5d501567223a307dd30e62f624214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883062"
---
# <a name="cim_metricdefforme-class"></a><span data-ttu-id="5e623-103">CIM \_ MetricDefForME (classe)</span><span class="sxs-lookup"><span data-stu-id="5e623-103">CIM\_MetricDefForME class</span></span>

<span data-ttu-id="5e623-104">Rappresenta un'associazione in cui un oggetto [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) definisce le metriche per un elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="5e623-104">Represents an association in which a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object defines metrics for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e623-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e623-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricDefForME : CIM_Dependency
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="5e623-106">Members</span><span class="sxs-lookup"><span data-stu-id="5e623-106">Members</span></span>

<span data-ttu-id="5e623-107">La classe **CIM \_ MetricDefForME** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5e623-107">The **CIM\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="5e623-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5e623-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e623-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5e623-109">Properties</span></span>

<span data-ttu-id="5e623-110">La classe **CIM \_ MetricDefForME** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5e623-110">The **CIM\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e623-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5e623-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e623-112">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="5e623-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="5e623-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e623-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e623-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="5e623-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5e623-115">Elemento gestito associato alla definizione della metrica.</span><span class="sxs-lookup"><span data-stu-id="5e623-115">The managed element that is associated with the metric definition.</span></span>

</dd> <dt>

<span data-ttu-id="5e623-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="5e623-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e623-117">Tipo di dati: **CIM \_ BaseMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="5e623-117">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="5e623-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e623-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e623-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="5e623-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5e623-120">Definizione della metrica associata all'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="5e623-120">The metric definition that is associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="5e623-121">**MetricCollectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="5e623-121">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e623-122">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e623-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e623-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e623-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e623-124">Indica se la metrica viene raccolta per l'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="5e623-124">Indicates whether the metric is being collected for the managed element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5e623-125">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="5e623-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5e623-126">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="5e623-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="5e623-127">**Riservato** (4)</span><span class="sxs-lookup"><span data-stu-id="5e623-127">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5e623-128">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="5e623-128">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="5e623-129">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5e623-129">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="5e623-130"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5e623-130"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5e623-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e623-131">Requirements</span></span>



| <span data-ttu-id="5e623-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e623-132">Requirement</span></span> | <span data-ttu-id="5e623-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5e623-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e623-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e623-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5e623-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5e623-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5e623-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e623-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5e623-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5e623-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5e623-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5e623-138">Namespace</span></span><br/>                | <span data-ttu-id="5e623-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5e623-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5e623-140">MOF</span><span class="sxs-lookup"><span data-stu-id="5e623-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e623-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e623-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e623-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5e623-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e623-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e623-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5e623-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e623-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e623-145">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="5e623-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

