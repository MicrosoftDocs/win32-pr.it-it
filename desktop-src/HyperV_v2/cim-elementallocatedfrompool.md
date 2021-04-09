---
description: Rappresenta un'associazione in cui un \_ oggetto logico CIM rappresenta una risorsa allocata da un \_ oggetto ResourcePool CIM.
ms.assetid: 5e3c95c5-1cbb-40de-b285-0bf9b34a5ca8
title: Classe CIM_ElementAllocatedFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementAllocatedFromPool
- CIM_ElementAllocatedFromPool.Antecedent
- CIM_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5fc6d58f5ebf82013f38b39027e0cd02e0e3595a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879761"
---
# <a name="cim_elementallocatedfrompool-class"></a><span data-ttu-id="407ba-103">CIM \_ ElementAllocatedFromPool (classe)</span><span class="sxs-lookup"><span data-stu-id="407ba-103">CIM\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="407ba-104">Rappresenta un'associazione in cui un [**oggetto \_ logico CIM**](cim-logicalelement.md) rappresenta una risorsa allocata da un [**oggetto \_ ResourcePool CIM**](cim-resourcepool.md) .</span><span class="sxs-lookup"><span data-stu-id="407ba-104">Represents an association in which a [**CIM\_LogicalElement**](cim-logicalelement.md) object represents a resource allocated from a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="407ba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="407ba-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ElementAllocatedFromPool : CIM_Dependency
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="407ba-106">Members</span><span class="sxs-lookup"><span data-stu-id="407ba-106">Members</span></span>

<span data-ttu-id="407ba-107">La classe **CIM \_ ElementAllocatedFromPool** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="407ba-107">The **CIM\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="407ba-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="407ba-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="407ba-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="407ba-109">Properties</span></span>

<span data-ttu-id="407ba-110">La classe **CIM \_ ElementAllocatedFromPool** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="407ba-110">The **CIM\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="407ba-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="407ba-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="407ba-112">Tipo di dati: **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="407ba-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="407ba-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="407ba-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="407ba-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="407ba-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="407ba-115">Pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="407ba-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="407ba-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="407ba-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="407ba-117">Tipo di dati **: \_ LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="407ba-117">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="407ba-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="407ba-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="407ba-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="407ba-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="407ba-120">Risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="407ba-120">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="407ba-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="407ba-121">Requirements</span></span>



| <span data-ttu-id="407ba-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="407ba-122">Requirement</span></span> | <span data-ttu-id="407ba-123">Valore</span><span class="sxs-lookup"><span data-stu-id="407ba-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="407ba-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="407ba-124">Minimum supported client</span></span><br/> | <span data-ttu-id="407ba-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="407ba-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="407ba-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="407ba-126">Minimum supported server</span></span><br/> | <span data-ttu-id="407ba-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="407ba-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="407ba-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="407ba-128">Namespace</span></span><br/>                | <span data-ttu-id="407ba-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="407ba-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="407ba-130">MOF</span><span class="sxs-lookup"><span data-stu-id="407ba-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="407ba-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="407ba-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="407ba-132">DLL</span><span class="sxs-lookup"><span data-stu-id="407ba-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="407ba-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="407ba-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="407ba-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="407ba-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="407ba-135">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="407ba-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

