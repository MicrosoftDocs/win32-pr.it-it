---
description: Rappresenta un'associazione tra un sistema e un pool di risorse che è un componente del sistema.
ms.assetid: 0ac60dbd-0498-4978-b2d6-f4c9926a83a8
title: Classe CIM_HostedResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedResourcePool
- CIM_HostedResourcePool.GroupComponent
- CIM_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dbb6d523b533d6e8b2f5bc1e21de93962cfd860f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305666"
---
# <a name="cim_hostedresourcepool-class"></a><span data-ttu-id="f99bf-103">CIM \_ HostedResourcePool (classe)</span><span class="sxs-lookup"><span data-stu-id="f99bf-103">CIM\_HostedResourcePool class</span></span>

<span data-ttu-id="f99bf-104">Rappresenta un'associazione tra un sistema e un pool di risorse che è un componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="f99bf-104">Represents an association between a system and a resource pool that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f99bf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f99bf-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_HostedResourcePool : CIM_SystemComponent
{
  CIM_System       REF GroupComponent;
  CIM_ResourcePool REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="f99bf-106">Members</span><span class="sxs-lookup"><span data-stu-id="f99bf-106">Members</span></span>

<span data-ttu-id="f99bf-107">La classe **CIM \_ HostedResourcePool** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f99bf-107">The **CIM\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="f99bf-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f99bf-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f99bf-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f99bf-109">Properties</span></span>

<span data-ttu-id="f99bf-110">La classe **CIM \_ HostedResourcePool** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f99bf-110">The **CIM\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f99bf-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f99bf-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99bf-112">Tipo di dati **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="f99bf-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="f99bf-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f99bf-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f99bf-114">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f99bf-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f99bf-115">Sistema padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="f99bf-115">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="f99bf-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f99bf-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f99bf-117">Tipo di dati: **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="f99bf-117">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="f99bf-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f99bf-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f99bf-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="f99bf-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f99bf-120">Pool di risorse che è un componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="f99bf-120">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f99bf-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f99bf-121">Requirements</span></span>



| <span data-ttu-id="f99bf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f99bf-122">Requirement</span></span> | <span data-ttu-id="f99bf-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f99bf-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f99bf-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f99bf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f99bf-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f99bf-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f99bf-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f99bf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f99bf-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f99bf-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f99bf-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f99bf-128">Namespace</span></span><br/>                | <span data-ttu-id="f99bf-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f99bf-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f99bf-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f99bf-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f99bf-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f99bf-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f99bf-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f99bf-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f99bf-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f99bf-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f99bf-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f99bf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f99bf-135">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="f99bf-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

