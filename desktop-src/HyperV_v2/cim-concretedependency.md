---
description: Rappresenta un'associazione generica in cui un elemento gestito dipende da un altro oggetto. CIM \_ ConcreteDependency sottoclassi CIM \_ dipendenza per fornire una versione di classe concreta di \_ dipendenza CIM.
ms.assetid: c0e1527d-d350-410d-9b5f-c9d4dedf7393
title: Classe CIM_ConcreteDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteDependency
- CIM_ConcreteDependency.Antecedent
- CIM_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 253f57b1fd29c3844f0e87d488974ced7bec98bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315523"
---
# <a name="cim_concretedependency-class"></a><span data-ttu-id="5eb9d-104">CIM \_ ConcreteDependency (classe)</span><span class="sxs-lookup"><span data-stu-id="5eb9d-104">CIM\_ConcreteDependency class</span></span>

<span data-ttu-id="5eb9d-105">Rappresenta un'associazione generica in cui un elemento gestito dipende da un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="5eb9d-105">Represents a generic association in which a managed element depends on another.</span></span> <span data-ttu-id="5eb9d-106">**CIM \_ ConcreteDependency** sottoclassi di [**\_ dipendenza CIM**](cim-dependency.md) per fornire una versione di classe concreta della **\_ dipendenza CIM**.</span><span class="sxs-lookup"><span data-stu-id="5eb9d-106">**CIM\_ConcreteDependency** subclasses [**CIM\_Dependency**](cim-dependency.md) to provide a concrete class version of **CIM\_Dependency**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb9d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5eb9d-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5eb9d-108">Members</span><span class="sxs-lookup"><span data-stu-id="5eb9d-108">Members</span></span>

<span data-ttu-id="5eb9d-109">La classe **CIM \_ ConcreteDependency** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5eb9d-109">The **CIM\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="5eb9d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5eb9d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5eb9d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5eb9d-111">Properties</span></span>

<span data-ttu-id="5eb9d-112">La classe **CIM \_ ConcreteDependency** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5eb9d-112">The **CIM\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5eb9d-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5eb9d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb9d-114">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="5eb9d-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="5eb9d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb9d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5eb9d-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="5eb9d-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5eb9d-117">Oggetto indipendente nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="5eb9d-117">The independent object in the association.</span></span>

</dd> <dt>

<span data-ttu-id="5eb9d-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="5eb9d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb9d-119">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="5eb9d-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="5eb9d-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb9d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5eb9d-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="5eb9d-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5eb9d-122">Oggetto dipendente nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="5eb9d-122">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5eb9d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5eb9d-123">Requirements</span></span>



| <span data-ttu-id="5eb9d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eb9d-124">Requirement</span></span> | <span data-ttu-id="5eb9d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5eb9d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb9d-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5eb9d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5eb9d-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5eb9d-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5eb9d-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5eb9d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5eb9d-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5eb9d-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5eb9d-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5eb9d-130">Namespace</span></span><br/>                | <span data-ttu-id="5eb9d-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5eb9d-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5eb9d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5eb9d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5eb9d-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5eb9d-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5eb9d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5eb9d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5eb9d-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5eb9d-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5eb9d-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5eb9d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb9d-137">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="5eb9d-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

