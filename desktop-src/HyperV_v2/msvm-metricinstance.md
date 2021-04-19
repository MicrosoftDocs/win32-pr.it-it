---
description: Rappresenta un'associazione di oggetti valore della metrica con le rispettive definizioni di metrica.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Classe Msvm_MetricInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab17dce339e866fb22654a0bd75c6f3945d320a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311789"
---
# <a name="msvm_metricinstance-class"></a><span data-ttu-id="9d772-103">\_Classe MSVM MetricInstance</span><span class="sxs-lookup"><span data-stu-id="9d772-103">Msvm\_MetricInstance class</span></span>

<span data-ttu-id="9d772-104">Rappresenta un'associazione di oggetti valore della metrica con le rispettive definizioni di metrica.</span><span class="sxs-lookup"><span data-stu-id="9d772-104">Represents an association of metric value objects with their metrics definitions.</span></span> <span data-ttu-id="9d772-105">Questa associazione associa un'istanza di [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) al relativo [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="9d772-105">This association ties an instance of [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) to its [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span>

<span data-ttu-id="9d772-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9d772-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d772-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d772-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9d772-108">Members</span><span class="sxs-lookup"><span data-stu-id="9d772-108">Members</span></span>

<span data-ttu-id="9d772-109">La **classe \_ MetricInstance di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9d772-109">The **Msvm\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="9d772-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d772-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d772-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d772-111">Properties</span></span>

<span data-ttu-id="9d772-112">La **classe \_ MetricInstance di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9d772-112">The **Msvm\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d772-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9d772-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d772-114">Tipo di dati: \* \* \* \* CIM \_ Managed \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="9d772-114">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="9d772-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d772-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d772-116">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="9d772-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9d772-117">Riferimento a un'istanza della classe [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) che rappresenta le definizioni di metrica.</span><span class="sxs-lookup"><span data-stu-id="9d772-117">A reference to an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class that represents the metrics definitions.</span></span>

</dd> <dt>

<span data-ttu-id="9d772-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="9d772-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d772-119">Tipo di dati: \* \* \* \* CIM \_ Managed \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="9d772-119">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="9d772-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d772-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d772-121">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="9d772-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9d772-122">Riferimento a un'istanza della classe [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) che rappresenta le metriche che dipendono dall'attività **precedente**.</span><span class="sxs-lookup"><span data-stu-id="9d772-122">A reference to an instance of the [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) class that represents the metrics that are dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d772-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d772-123">Requirements</span></span>



| <span data-ttu-id="9d772-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d772-124">Requirement</span></span> | <span data-ttu-id="9d772-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9d772-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d772-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d772-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9d772-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9d772-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9d772-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d772-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9d772-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9d772-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d772-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d772-130">Namespace</span></span><br/>                | <span data-ttu-id="9d772-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="9d772-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9d772-132">MOF</span><span class="sxs-lookup"><span data-stu-id="9d772-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d772-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d772-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d772-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9d772-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d772-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d772-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




