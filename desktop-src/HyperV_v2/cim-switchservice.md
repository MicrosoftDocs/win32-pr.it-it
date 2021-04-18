---
description: Rappresenta un servizio di commutazione.
ms.assetid: cf6319fa-7d69-4820-b0e0-775aad8b190c
title: Classe CIM_SwitchService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchService
- CIM_SwitchService.BridgeAddress
- CIM_SwitchService.NumPorts
- CIM_SwitchService.BridgeType
- CIM_SwitchService.BridgeAddressType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9abe6869c5b8ac61630091315e476ae232630717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310583"
---
# <a name="cim_switchservice-class"></a><span data-ttu-id="0486c-103">CIM \_ SwitchService (classe)</span><span class="sxs-lookup"><span data-stu-id="0486c-103">CIM\_SwitchService class</span></span>

<span data-ttu-id="0486c-104">Rappresenta un servizio di commutazione.</span><span class="sxs-lookup"><span data-stu-id="0486c-104">Represents a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0486c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0486c-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchService : CIM_ForwardingService
{
  string BridgeAddress;
  uint16 NumPorts;
  uint8  BridgeType;
  uint16 BridgeAddressType;
};
```

## <a name="members"></a><span data-ttu-id="0486c-106">Members</span><span class="sxs-lookup"><span data-stu-id="0486c-106">Members</span></span>

<span data-ttu-id="0486c-107">La classe **CIM \_ SwitchService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0486c-107">The **CIM\_SwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="0486c-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0486c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0486c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0486c-109">Properties</span></span>

<span data-ttu-id="0486c-110">La classe **CIM \_ SwitchService** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0486c-110">The **CIM\_SwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0486c-111">**BridgeAddress**</span><span class="sxs-lookup"><span data-stu-id="0486c-111">**BridgeAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0486c-112">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0486c-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0486c-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0486c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0486c-114">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseBridgeAddress "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**.**BridgeAddressType**")</span><span class="sxs-lookup"><span data-stu-id="0486c-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseBridgeAddress"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddressType**")</span></span>
</dt> </dl>

<span data-ttu-id="0486c-115">Indirizzo del servizio Switch, che è una parte dell'identificatore univoco del servizio.</span><span class="sxs-lookup"><span data-stu-id="0486c-115">The address of the switch service, which is a portion of the unique identifier of the service.</span></span>

</dd> <dt>

<span data-ttu-id="0486c-116">**BridgeAddressType**</span><span class="sxs-lookup"><span data-stu-id="0486c-116">**BridgeAddressType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0486c-117">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0486c-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0486c-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0486c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0486c-119">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**.**BridgeAddress**")</span><span class="sxs-lookup"><span data-stu-id="0486c-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="0486c-120">Formato di indirizzamento utilizzato per il Bridge e la proprietà **BridgeAddress** .</span><span class="sxs-lookup"><span data-stu-id="0486c-120">The addressing format used for the bridge and the **BridgeAddress** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0486c-121">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0486c-121">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="0486c-122">**IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="0486c-122">**IPv4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="0486c-123">**IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="0486c-123">**IPv6** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC"></span><span id="mac"></span>

<span data-ttu-id="0486c-124">**Mac** (4)</span><span class="sxs-lookup"><span data-stu-id="0486c-124">**MAC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC___Spanning_Tree_Priority"></span><span id="mac___spanning_tree_priority"></span><span id="MAC___SPANNING_TREE_PRIORITY"></span>

<span data-ttu-id="0486c-125">**Priorità albero per Mac + spanning** (5)</span><span class="sxs-lookup"><span data-stu-id="0486c-125">**MAC + Spanning Tree Priority** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0486c-126">**BridgeType**</span><span class="sxs-lookup"><span data-stu-id="0486c-126">**BridgeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0486c-127">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0486c-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0486c-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0486c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0486c-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseType ")</span><span class="sxs-lookup"><span data-stu-id="0486c-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseType")</span></span>
</dt> </dl>

<span data-ttu-id="0486c-130">Tipo di servizio di trasferimento da eseguire.</span><span class="sxs-lookup"><span data-stu-id="0486c-130">The type of switching service to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0486c-131">**Sconosciuto** (1)</span><span class="sxs-lookup"><span data-stu-id="0486c-131">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparent-only"></span><span id="transparent-only"></span><span id="TRANSPARENT-ONLY"></span>

<span data-ttu-id="0486c-132">**Solo trasparente** (2)</span><span class="sxs-lookup"><span data-stu-id="0486c-132">**Transparent-only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SourceRoute-only"></span><span id="sourceroute-only"></span><span id="SOURCEROUTE-ONLY"></span>

<span data-ttu-id="0486c-133">**Solo la proprietà SourceRoute** (3)</span><span class="sxs-lookup"><span data-stu-id="0486c-133">**SourceRoute-only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRT"></span><span id="srt"></span>

<span data-ttu-id="0486c-134">**SRT** (4)</span><span class="sxs-lookup"><span data-stu-id="0486c-134">**SRT** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0486c-135">**NumPorts**</span><span class="sxs-lookup"><span data-stu-id="0486c-135">**NumPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0486c-136">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0486c-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0486c-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0486c-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0486c-138">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseNumPorts ")</span><span class="sxs-lookup"><span data-stu-id="0486c-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseNumPorts")</span></span>
</dt> </dl>

<span data-ttu-id="0486c-139">Numero di porte di commutazione controllate da questo servizio di commutazione.</span><span class="sxs-lookup"><span data-stu-id="0486c-139">The number of switch ports controlled by this switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0486c-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0486c-140">Requirements</span></span>



| <span data-ttu-id="0486c-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0486c-141">Requirement</span></span> | <span data-ttu-id="0486c-142">Valore</span><span class="sxs-lookup"><span data-stu-id="0486c-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0486c-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0486c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0486c-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0486c-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0486c-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0486c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0486c-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0486c-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0486c-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0486c-147">Namespace</span></span><br/>                | <span data-ttu-id="0486c-148">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0486c-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0486c-149">MOF</span><span class="sxs-lookup"><span data-stu-id="0486c-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0486c-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0486c-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0486c-151">DLL</span><span class="sxs-lookup"><span data-stu-id="0486c-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0486c-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0486c-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0486c-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0486c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0486c-154">**\_FORWARDINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0486c-154">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 

