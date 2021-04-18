---
description: Rappresenta un'associazione in cui un servizio Bridge è un componente di un servizio di commutazione.
ms.assetid: 737d5ba1-0759-40cf-bc46-a059d19902c8
title: Classe CIM_SwitchServiceTransparentBridging
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchServiceTransparentBridging
- CIM_SwitchServiceTransparentBridging.GroupComponent
- CIM_SwitchServiceTransparentBridging.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04bce4bf673dc029b7b3a2d2b837670b01300c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310581"
---
# <a name="cim_switchservicetransparentbridging-class"></a><span data-ttu-id="df537-103">CIM \_ SwitchServiceTransparentBridging (classe)</span><span class="sxs-lookup"><span data-stu-id="df537-103">CIM\_SwitchServiceTransparentBridging class</span></span>

<span data-ttu-id="df537-104">Rappresenta un'associazione in cui un servizio Bridge è un componente di un servizio di commutazione.</span><span class="sxs-lookup"><span data-stu-id="df537-104">Represents an association in which a bridge service is a component of a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="df537-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df537-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchServiceTransparentBridging : CIM_ServiceComponent
{
  CIM_SwitchService              REF GroupComponent;
  CIM_TransparentBridgingService REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="df537-106">Members</span><span class="sxs-lookup"><span data-stu-id="df537-106">Members</span></span>

<span data-ttu-id="df537-107">La classe **CIM \_ SwitchServiceTransparentBridging** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="df537-107">The **CIM\_SwitchServiceTransparentBridging** class has these types of members:</span></span>

-   [<span data-ttu-id="df537-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="df537-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df537-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="df537-109">Properties</span></span>

<span data-ttu-id="df537-110">La classe **CIM \_ SwitchServiceTransparentBridging** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="df537-110">The **CIM\_SwitchServiceTransparentBridging** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df537-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="df537-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df537-112">Tipo di dati: **CIM \_ SwitchService**</span><span class="sxs-lookup"><span data-stu-id="df537-112">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="df537-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df537-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df537-114">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="df537-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="df537-115">Riferimento [**CIM \_ SwitchService**](cim-switchservice.md) al servizio Switch.</span><span class="sxs-lookup"><span data-stu-id="df537-115">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switch service.</span></span>

</dd> <dt>

<span data-ttu-id="df537-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="df537-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df537-117">Tipo di dati: **CIM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="df537-117">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="df537-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df537-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df537-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="df537-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="df537-120">Riferimento [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) al servizio di bridging dei componenti.</span><span class="sxs-lookup"><span data-stu-id="df537-120">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the component bridging service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df537-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df537-121">Requirements</span></span>



| <span data-ttu-id="df537-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="df537-122">Requirement</span></span> | <span data-ttu-id="df537-123">Valore</span><span class="sxs-lookup"><span data-stu-id="df537-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df537-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df537-124">Minimum supported client</span></span><br/> | <span data-ttu-id="df537-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="df537-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="df537-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df537-126">Minimum supported server</span></span><br/> | <span data-ttu-id="df537-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="df537-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="df537-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="df537-128">Namespace</span></span><br/>                | <span data-ttu-id="df537-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="df537-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="df537-130">MOF</span><span class="sxs-lookup"><span data-stu-id="df537-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df537-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df537-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="df537-132">DLL</span><span class="sxs-lookup"><span data-stu-id="df537-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df537-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="df537-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="df537-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df537-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df537-135">**\_SERVICECOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="df537-135">**CIM\_ServiceComponent**</span></span>](cim-servicecomponent.md)
</dt> </dl>

 

