---
description: Rappresenta un'associazione tra un'istanza di un valore di metrica e una definizione di metrica.
ms.assetid: 4c620a7a-8b15-49ad-ae84-246e2fca175d
title: Classe CIM_MetricInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricInstance
- CIM_MetricInstance.Antecedent
- CIM_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: defba85f46e037c226a96cfaa8ffac44b99244f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313864"
---
# <a name="cim_metricinstance-class"></a><span data-ttu-id="81b0c-103">CIM \_ MetricInstance (classe)</span><span class="sxs-lookup"><span data-stu-id="81b0c-103">CIM\_MetricInstance class</span></span>

<span data-ttu-id="81b0c-104">Rappresenta un'associazione tra un'istanza di un valore di metrica e una definizione di metrica.</span><span class="sxs-lookup"><span data-stu-id="81b0c-104">Represents an association between an instance of a metric value and a metric definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="81b0c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81b0c-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricInstance : CIM_Dependency
{
  CIM_BaseMetricDefinition REF Antecedent;
  CIM_BaseMetricValue      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="81b0c-106">Members</span><span class="sxs-lookup"><span data-stu-id="81b0c-106">Members</span></span>

<span data-ttu-id="81b0c-107">La classe **CIM \_ MetricInstance** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="81b0c-107">The **CIM\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="81b0c-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="81b0c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81b0c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="81b0c-109">Properties</span></span>

<span data-ttu-id="81b0c-110">La classe **CIM \_ MetricInstance** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="81b0c-110">The **CIM\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81b0c-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="81b0c-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81b0c-112">Tipo di dati: **CIM \_ BaseMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="81b0c-112">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="81b0c-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81b0c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81b0c-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="81b0c-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="81b0c-115">Definizione del valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="81b0c-115">The definition of the metric value.</span></span>

</dd> <dt>

<span data-ttu-id="81b0c-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="81b0c-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81b0c-117">Tipo di dati: **CIM \_ BaseMetricValue**</span><span class="sxs-lookup"><span data-stu-id="81b0c-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="81b0c-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81b0c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81b0c-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="81b0c-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="81b0c-120">Valore della metrica associato alla definizione della metrica.</span><span class="sxs-lookup"><span data-stu-id="81b0c-120">The metric value that is associated with the metric definition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81b0c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81b0c-121">Requirements</span></span>



| <span data-ttu-id="81b0c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="81b0c-122">Requirement</span></span> | <span data-ttu-id="81b0c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="81b0c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b0c-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81b0c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="81b0c-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="81b0c-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="81b0c-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81b0c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="81b0c-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81b0c-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="81b0c-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="81b0c-128">Namespace</span></span><br/>                | <span data-ttu-id="81b0c-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="81b0c-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="81b0c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="81b0c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81b0c-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81b0c-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81b0c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="81b0c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81b0c-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81b0c-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81b0c-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81b0c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81b0c-135">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="81b0c-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

