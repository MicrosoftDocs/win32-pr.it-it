---
description: Rappresenta un'associazione in cui un servizio è un componente di un servizio padre, che insieme, costituisce un servizio di livello superiore.
ms.assetid: c629d59d-d9d3-4019-a378-cd1d4d31a5d9
title: Classe CIM_ServiceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceComponent
- CIM_ServiceComponent.GroupComponent
- CIM_ServiceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2bfb9943685f8568674e696a76df94fda502fcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226242"
---
# <a name="cim_servicecomponent-class"></a><span data-ttu-id="297dd-103">CIM \_ servicecomponent (classe)</span><span class="sxs-lookup"><span data-stu-id="297dd-103">CIM\_ServiceComponent class</span></span>

<span data-ttu-id="297dd-104">Rappresenta un'associazione in cui un servizio è un componente di un servizio padre, che insieme, costituisce un servizio di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="297dd-104">Represents an association in which a service is a component of a parent service, which together, form a higher-level service.</span></span>

## <a name="syntax"></a><span data-ttu-id="297dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="297dd-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceComponent : CIM_Component
{
  CIM_Service REF GroupComponent;
  CIM_Service REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="297dd-106">Members</span><span class="sxs-lookup"><span data-stu-id="297dd-106">Members</span></span>

<span data-ttu-id="297dd-107">La classe **CIM \_ servicecomponent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="297dd-107">The **CIM\_ServiceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="297dd-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="297dd-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="297dd-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="297dd-109">Properties</span></span>

<span data-ttu-id="297dd-110">La classe **CIM \_ servicecomponent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="297dd-110">The **CIM\_ServiceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="297dd-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="297dd-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="297dd-112">Tipo di dati **: \_ servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="297dd-112">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="297dd-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="297dd-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="297dd-114">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="297dd-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="297dd-115">Il servizio padre.</span><span class="sxs-lookup"><span data-stu-id="297dd-115">The parent service.</span></span>

</dd> <dt>

<span data-ttu-id="297dd-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="297dd-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="297dd-117">Tipo di dati **: \_ servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="297dd-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="297dd-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="297dd-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="297dd-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="297dd-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="297dd-120">Il servizio componenti.</span><span class="sxs-lookup"><span data-stu-id="297dd-120">The component service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="297dd-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="297dd-121">Requirements</span></span>



| <span data-ttu-id="297dd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="297dd-122">Requirement</span></span> | <span data-ttu-id="297dd-123">Valore</span><span class="sxs-lookup"><span data-stu-id="297dd-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="297dd-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="297dd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="297dd-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="297dd-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="297dd-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="297dd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="297dd-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="297dd-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="297dd-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="297dd-128">Namespace</span></span><br/>                | <span data-ttu-id="297dd-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="297dd-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="297dd-130">MOF</span><span class="sxs-lookup"><span data-stu-id="297dd-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="297dd-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="297dd-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="297dd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="297dd-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="297dd-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="297dd-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="297dd-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="297dd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297dd-135">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="297dd-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

