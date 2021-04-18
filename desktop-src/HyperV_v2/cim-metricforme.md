---
description: Rappresenta un'associazione in cui vengono raccolti i valori delle metriche per un elemento gestito.
ms.assetid: 00752751-bc27-463b-a4ac-4db8e5040077
title: Classe CIM_MetricForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricForME
- CIM_MetricForME.Antecedent
- CIM_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89c119ad622b778d0402100a64ff15befe623685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314358"
---
# <a name="cim_metricforme-class"></a><span data-ttu-id="99d11-103">CIM \_ MetricForME (classe)</span><span class="sxs-lookup"><span data-stu-id="99d11-103">CIM\_MetricForME class</span></span>

<span data-ttu-id="99d11-104">Rappresenta un'associazione in cui vengono raccolti i valori delle metriche per un elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="99d11-104">Represents an association in which a metric values are collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="99d11-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99d11-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricForME : CIM_Dependency
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="99d11-106">Members</span><span class="sxs-lookup"><span data-stu-id="99d11-106">Members</span></span>

<span data-ttu-id="99d11-107">La classe **CIM \_ MetricForME** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="99d11-107">The **CIM\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="99d11-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="99d11-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99d11-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="99d11-109">Properties</span></span>

<span data-ttu-id="99d11-110">La classe **CIM \_ MetricForME** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="99d11-110">The **CIM\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99d11-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="99d11-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99d11-112">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="99d11-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="99d11-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="99d11-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99d11-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="99d11-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="99d11-115">Elemento gestito nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="99d11-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="99d11-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="99d11-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99d11-117">Tipo di dati: **CIM \_ BaseMetricValue**</span><span class="sxs-lookup"><span data-stu-id="99d11-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="99d11-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="99d11-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99d11-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="99d11-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="99d11-120">Valore della metrica nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="99d11-120">The metric value in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99d11-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99d11-121">Requirements</span></span>



| <span data-ttu-id="99d11-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="99d11-122">Requirement</span></span> | <span data-ttu-id="99d11-123">Valore</span><span class="sxs-lookup"><span data-stu-id="99d11-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99d11-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99d11-124">Minimum supported client</span></span><br/> | <span data-ttu-id="99d11-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="99d11-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="99d11-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99d11-126">Minimum supported server</span></span><br/> | <span data-ttu-id="99d11-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="99d11-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="99d11-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="99d11-128">Namespace</span></span><br/>                | <span data-ttu-id="99d11-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="99d11-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="99d11-130">MOF</span><span class="sxs-lookup"><span data-stu-id="99d11-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99d11-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99d11-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="99d11-132">DLL</span><span class="sxs-lookup"><span data-stu-id="99d11-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99d11-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="99d11-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="99d11-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99d11-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99d11-135">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="99d11-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

