---
description: Rappresenta un'associazione generica utilizzata per stabilire le parti di una relazione tra elementi gestiti.
ms.assetid: 9785ea8b-fb76-4ffe-8649-aa2fe1b01d5f
title: Classe CIM_ConcreteComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteComponent
- CIM_ConcreteComponent.GroupComponent
- CIM_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77ee0f33f540bfd215ec10a24c3c574976189d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882426"
---
# <a name="cim_concretecomponent-class"></a><span data-ttu-id="d199a-103">CIM \_ ConcreteComponent (classe)</span><span class="sxs-lookup"><span data-stu-id="d199a-103">CIM\_ConcreteComponent class</span></span>

<span data-ttu-id="d199a-104">Rappresenta un'associazione generica utilizzata per stabilire le parti di una relazione tra elementi gestiti.</span><span class="sxs-lookup"><span data-stu-id="d199a-104">Represents a generic association used to establish the parts of a relationship between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="d199a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d199a-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteComponent : CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="d199a-106">Members</span><span class="sxs-lookup"><span data-stu-id="d199a-106">Members</span></span>

<span data-ttu-id="d199a-107">La classe **CIM \_ ConcreteComponent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d199a-107">The **CIM\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="d199a-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d199a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d199a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d199a-109">Properties</span></span>

<span data-ttu-id="d199a-110">La classe **CIM \_ ConcreteComponent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d199a-110">The **CIM\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d199a-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d199a-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d199a-112">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="d199a-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d199a-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d199a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d199a-114">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="d199a-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d199a-115">Elemento padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="d199a-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="d199a-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d199a-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d199a-117">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="d199a-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d199a-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d199a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d199a-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="d199a-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d199a-120">Elemento figlio nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="d199a-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d199a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d199a-121">Requirements</span></span>



| <span data-ttu-id="d199a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d199a-122">Requirement</span></span> | <span data-ttu-id="d199a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d199a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d199a-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d199a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d199a-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d199a-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d199a-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d199a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d199a-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d199a-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d199a-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d199a-128">Namespace</span></span><br/>                | <span data-ttu-id="d199a-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d199a-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d199a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d199a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d199a-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d199a-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d199a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d199a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d199a-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d199a-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d199a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d199a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d199a-135">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="d199a-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

