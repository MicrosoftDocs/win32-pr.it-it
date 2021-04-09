---
description: Rappresenta un'associazione tra un sistema e uno degli elementi che lo compongono.
ms.assetid: 728f25bf-3d52-4b1c-bf72-51e8ed0a4e72
title: Classe CIM_SystemComponent (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.GroupComponent
- CIM_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 79bb7d3807a93b2d29157a3377d6e6a9079bfe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880762"
---
# <a name="cim_systemcomponent-class-hyper-v-management"></a><span data-ttu-id="fe7b0-103">Classe CIM_SystemComponent (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="fe7b0-103">CIM_SystemComponent class (Hyper-V management)</span></span>

<span data-ttu-id="fe7b0-104">Rappresenta un'associazione tra un sistema e uno degli elementi che lo compongono.</span><span class="sxs-lookup"><span data-stu-id="fe7b0-104">Represents an association between a system and one of the elements that compose it.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe7b0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe7b0-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="fe7b0-106">Members</span><span class="sxs-lookup"><span data-stu-id="fe7b0-106">Members</span></span>

<span data-ttu-id="fe7b0-107">La classe **CIM \_ SystemComponent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fe7b0-107">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="fe7b0-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fe7b0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe7b0-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fe7b0-109">Properties</span></span>

<span data-ttu-id="fe7b0-110">La classe **CIM \_ SystemComponent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe7b0-110">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe7b0-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="fe7b0-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe7b0-112">Tipo di dati **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="fe7b0-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="fe7b0-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe7b0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe7b0-114">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="fe7b0-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="fe7b0-115">[**\_ Sistema CIM**](cim-system.md) che contiene **PartComponent**.</span><span class="sxs-lookup"><span data-stu-id="fe7b0-115">The [**CIM\_System**](cim-system.md) that contains the **PartComponent**.</span></span>

</dd> <dt>

<span data-ttu-id="fe7b0-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="fe7b0-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe7b0-117">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="fe7b0-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="fe7b0-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe7b0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe7b0-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="fe7b0-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="fe7b0-120">Il [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) figlio che è un componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="fe7b0-120">The child [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe7b0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe7b0-121">Requirements</span></span>



| <span data-ttu-id="fe7b0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe7b0-122">Requirement</span></span> | <span data-ttu-id="fe7b0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fe7b0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe7b0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe7b0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fe7b0-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fe7b0-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="fe7b0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe7b0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fe7b0-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fe7b0-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="fe7b0-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fe7b0-128">Namespace</span></span><br/>                | <span data-ttu-id="fe7b0-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fe7b0-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fe7b0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="fe7b0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe7b0-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe7b0-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe7b0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fe7b0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe7b0-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe7b0-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fe7b0-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe7b0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe7b0-135">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="fe7b0-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

