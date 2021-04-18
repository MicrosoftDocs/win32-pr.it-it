---
description: Associa un sistema a un dispositivo logico che è un componente del sistema.
ms.assetid: d5a36f71-5ebe-46e2-aaa9-5d99fa075d31
title: Classe CIM_SystemDevice (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.GroupComponent
- CIM_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b02921e4be0f8aa0cddc194a2ed430e10e115eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310575"
---
# <a name="cim_systemdevice-class-hyper-v-management"></a><span data-ttu-id="4f9e0-103">Classe CIM_SystemDevice (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="4f9e0-103">CIM_SystemDevice class (Hyper-V management)</span></span>

<span data-ttu-id="4f9e0-104">Associa un sistema a un dispositivo logico che è un componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-104">Associates a system with a logical device that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f9e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f9e0-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="4f9e0-106">Members</span><span class="sxs-lookup"><span data-stu-id="4f9e0-106">Members</span></span>

<span data-ttu-id="4f9e0-107">La classe **CIM \_ SystemDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4f9e0-107">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="4f9e0-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f9e0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f9e0-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f9e0-109">Properties</span></span>

<span data-ttu-id="4f9e0-110">La classe **CIM \_ SystemDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-110">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f9e0-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4f9e0-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f9e0-112">Tipo di dati **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="4f9e0-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="4f9e0-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f9e0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f9e0-114">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4f9e0-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4f9e0-115">Riferimento [**di \_ sistema CIM**](cim-system.md) al sistema padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-115">A [**CIM\_System**](cim-system.md) reference to the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="4f9e0-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4f9e0-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f9e0-117">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="4f9e0-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4f9e0-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f9e0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f9e0-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4f9e0-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4f9e0-120">Un riferimento [**CIM \_ LogicalDevice**](cim-logicaldevice.md) al dispositivo logico che è un componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="4f9e0-120">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) reference to the logical device that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f9e0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f9e0-121">Requirements</span></span>



| <span data-ttu-id="4f9e0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f9e0-122">Requirement</span></span> | <span data-ttu-id="4f9e0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4f9e0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f9e0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f9e0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4f9e0-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4f9e0-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4f9e0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f9e0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4f9e0-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4f9e0-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4f9e0-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f9e0-128">Namespace</span></span><br/>                | <span data-ttu-id="4f9e0-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4f9e0-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4f9e0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4f9e0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f9e0-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f9e0-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f9e0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4f9e0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f9e0-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f9e0-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4f9e0-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f9e0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f9e0-135">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="4f9e0-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

