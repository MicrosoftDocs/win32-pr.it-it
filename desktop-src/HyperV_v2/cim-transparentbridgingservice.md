---
description: Rappresenta l'aspetto di bridging trasparente di un \_ oggetto SWITCHSERVICE CIM.
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: Classe CIM_TransparentBridgingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed2c21c0f00bd89b0054667274a559ef25ce9326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880757"
---
# <a name="cim_transparentbridgingservice-class"></a><span data-ttu-id="fb650-103">CIM \_ TransparentBridgingService (classe)</span><span class="sxs-lookup"><span data-stu-id="fb650-103">CIM\_TransparentBridgingService class</span></span>

<span data-ttu-id="fb650-104">Rappresenta l'aspetto di bridging trasparente di un [**oggetto \_ SwitchService CIM**](cim-switchservice.md) .</span><span class="sxs-lookup"><span data-stu-id="fb650-104">Represents the transparent bridging aspect of a [**CIM\_SwitchService**](cim-switchservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb650-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb650-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a><span data-ttu-id="fb650-106">Members</span><span class="sxs-lookup"><span data-stu-id="fb650-106">Members</span></span>

<span data-ttu-id="fb650-107">La classe **CIM \_ TransparentBridgingService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fb650-107">The **CIM\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="fb650-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fb650-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb650-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fb650-109">Properties</span></span>

<span data-ttu-id="fb650-110">La classe **CIM \_ TransparentBridgingService** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fb650-110">The **CIM\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb650-111">**AgingTime**</span><span class="sxs-lookup"><span data-stu-id="fb650-111">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb650-112">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fb650-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb650-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fb650-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb650-114">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("secondi"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpAgingTime ")</span><span class="sxs-lookup"><span data-stu-id="fb650-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpAgingTime")</span></span>
</dt> </dl>

<span data-ttu-id="fb650-115">Periodo di timeout, espresso in secondi, per l'invecchiamento delle informazioni di invio apprese dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="fb650-115">The timeout period, in seconds, for aging out dynamically learned forwarding information.</span></span> <span data-ttu-id="fb650-116">Lo standard 802.1 D-1990 consiglia un valore predefinito di 300 secondi.</span><span class="sxs-lookup"><span data-stu-id="fb650-116">The 802.1D-1990 standard recommends a default of 300 seconds.</span></span>

</dd> <dt>

<span data-ttu-id="fb650-117">**FID**</span><span class="sxs-lookup"><span data-stu-id="fb650-117">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb650-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fb650-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb650-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fb650-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb650-120">Filtro dell'identificatore di database utilizzato dai commutatori compatibili con VLAN con più di un database di filtraggio.</span><span class="sxs-lookup"><span data-stu-id="fb650-120">Filtering Database Identifier used by VLAN-aware switches that have more than one filtering database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb650-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb650-121">Requirements</span></span>



| <span data-ttu-id="fb650-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb650-122">Requirement</span></span> | <span data-ttu-id="fb650-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fb650-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb650-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb650-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fb650-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fb650-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="fb650-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb650-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fb650-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fb650-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="fb650-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fb650-128">Namespace</span></span><br/>                | <span data-ttu-id="fb650-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fb650-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fb650-130">MOF</span><span class="sxs-lookup"><span data-stu-id="fb650-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb650-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb650-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb650-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fb650-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb650-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fb650-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fb650-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb650-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb650-135">**\_FORWARDINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fb650-135">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 

