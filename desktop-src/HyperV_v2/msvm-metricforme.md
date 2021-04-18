---
description: Questa associazione collega un elemento gestito ai valori della metrica gestiti.
ms.assetid: 89b43736-90ae-49e0-a0ed-7918ddec8558
title: Classe Msvm_MetricForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricForME
- Msvm_MetricForME.Antecedent
- Msvm_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 554f77390737b336b8660d09f737049be193b448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318338"
---
# <a name="msvm_metricforme-class"></a><span data-ttu-id="cba61-103">\_Classe MSVM MetricForME</span><span class="sxs-lookup"><span data-stu-id="cba61-103">Msvm\_MetricForME class</span></span>

<span data-ttu-id="cba61-104">Questa associazione collega un elemento gestito ai valori della metrica gestiti.</span><span class="sxs-lookup"><span data-stu-id="cba61-104">This association links a managed element to the metric values being maintained for it.</span></span>

<span data-ttu-id="cba61-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cba61-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba61-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cba61-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricForME : CIM_MetricForME
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="cba61-107">Members</span><span class="sxs-lookup"><span data-stu-id="cba61-107">Members</span></span>

<span data-ttu-id="cba61-108">La **classe \_ MetricForME di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cba61-108">The **Msvm\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="cba61-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cba61-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cba61-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cba61-110">Properties</span></span>

<span data-ttu-id="cba61-111">La **classe \_ MetricForME di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cba61-111">The **Msvm\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cba61-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="cba61-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cba61-113">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="cba61-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="cba61-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cba61-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cba61-115">Riferimento a un'istanza della classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che rappresenta l'elemento gestito con le metriche definite dall'oggetto **dipendente** gestito.</span><span class="sxs-lookup"><span data-stu-id="cba61-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that has metrics defined by **Dependent** maintained for it.</span></span> <span data-ttu-id="cba61-116">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="cba61-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="cba61-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="cba61-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cba61-118">Tipo di dati: \* \* \* \* CIM \_ BaseMetricValue \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="cba61-118">Data type: \*\*\*\*CIM\_BaseMetricValue\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="cba61-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cba61-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cba61-120">Riferimento a un'istanza della classe **CIM \_ BaseMetricValue** che rappresenta la metrica raccolta dall'attività **precedente** .</span><span class="sxs-lookup"><span data-stu-id="cba61-120">A reference to an instance of the **CIM\_BaseMetricValue** class that represents the metric that the **Antecedent** has collected for it.</span></span> <span data-ttu-id="cba61-121">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="cba61-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cba61-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cba61-122">Requirements</span></span>



| <span data-ttu-id="cba61-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cba61-123">Requirement</span></span> | <span data-ttu-id="cba61-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cba61-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cba61-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cba61-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cba61-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cba61-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cba61-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cba61-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cba61-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cba61-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cba61-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cba61-129">Namespace</span></span><br/>                | <span data-ttu-id="cba61-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="cba61-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cba61-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cba61-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cba61-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cba61-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cba61-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cba61-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cba61-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cba61-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

