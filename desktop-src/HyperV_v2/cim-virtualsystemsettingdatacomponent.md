---
description: Rappresenta una parte di una relazione tra un' \_ istanza CIM VirtualSystemSettingData e un set di \_ istanze ResourceAllocationSettingData CIM.
ms.assetid: 4f167517-079e-4b5f-885a-741ac1d1dc71
title: Classe CIM_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingDataComponent
- CIM_VirtualSystemSettingDataComponent.GroupComponent
- CIM_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afbd7ab192c65e99f4479e5380e57dc78c8a0a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131999"
---
# <a name="cim_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="f1fb5-103">CIM \_ VirtualSystemSettingDataComponent (classe)</span><span class="sxs-lookup"><span data-stu-id="f1fb5-103">CIM\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="f1fb5-104">Rappresenta una parte di una relazione tra un'istanza [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) e un set di [**istanze \_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f1fb5-104">Represents a portion of a relationship between a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) instance and a set of [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1fb5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1fb5-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingDataComponent : CIM_Component
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="f1fb5-106">Members</span><span class="sxs-lookup"><span data-stu-id="f1fb5-106">Members</span></span>

<span data-ttu-id="f1fb5-107">La classe **CIM \_ VirtualSystemSettingDataComponent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f1fb5-107">The **CIM\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="f1fb5-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1fb5-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1fb5-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1fb5-109">Properties</span></span>

<span data-ttu-id="f1fb5-110">La classe **CIM \_ VirtualSystemSettingDataComponent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f1fb5-110">The **CIM\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1fb5-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f1fb5-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fb5-112">Tipo di dati: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="f1fb5-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="f1fb5-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1fb5-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fb5-114">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="f1fb5-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f1fb5-115">Riferimento all'oggetto [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) di primo livello della configurazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="f1fb5-115">A reference to the top-level [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) object of the virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="f1fb5-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f1fb5-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1fb5-117">Tipo di dati: **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="f1fb5-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="f1fb5-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1fb5-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1fb5-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="f1fb5-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f1fb5-120">Un riferimento all' [**oggetto \_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) che rappresenta una parte della configurazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="f1fb5-120">A reference the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) object that represents a part of the virtual system configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1fb5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1fb5-121">Requirements</span></span>



| <span data-ttu-id="f1fb5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1fb5-122">Requirement</span></span> | <span data-ttu-id="f1fb5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f1fb5-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1fb5-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1fb5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f1fb5-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f1fb5-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f1fb5-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1fb5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f1fb5-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1fb5-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f1fb5-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f1fb5-128">Namespace</span></span><br/>                | <span data-ttu-id="f1fb5-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f1fb5-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f1fb5-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f1fb5-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1fb5-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1fb5-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1fb5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f1fb5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1fb5-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1fb5-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1fb5-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1fb5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1fb5-135">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="f1fb5-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

