---
description: Rappresenta l'opzione impostazioni gruppo NIC.
ms.assetid: 7a48bdae-1953-4011-aaa8-1e3ca73494ff
title: Classe Msvm_VirtualEthernetSwitchNicTeamingSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingSettingData
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.TeamingMode
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.LoadBalancingAlgorithm
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 45f306f9ddb388ef4e8124d7ab2c8dd125a62e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760850"
---
# <a name="msvm_virtualethernetswitchnicteamingsettingdata-class"></a><span data-ttu-id="8231b-103">\_Classe MSVM VirtualEthernetSwitchNicTeamingSettingData</span><span class="sxs-lookup"><span data-stu-id="8231b-103">Msvm\_VirtualEthernetSwitchNicTeamingSettingData class</span></span>

<span data-ttu-id="8231b-104">Rappresenta l'opzione impostazioni gruppo NIC.</span><span class="sxs-lookup"><span data-stu-id="8231b-104">Represents the switch nic teaming settings.</span></span>

<span data-ttu-id="8231b-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8231b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8231b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8231b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("17AD26F1-DD6F-4ED9-BD2F-3750ADE6B68B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Nic Teaming Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  UINT32 TeamingMode = 0;
  UINT32 LoadBalancingAlgorithm = 5;
};
```

## <a name="members"></a><span data-ttu-id="8231b-107">Members</span><span class="sxs-lookup"><span data-stu-id="8231b-107">Members</span></span>

<span data-ttu-id="8231b-108">La **classe \_ VirtualEthernetSwitchNicTeamingSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8231b-108">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8231b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8231b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8231b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8231b-110">Properties</span></span>

<span data-ttu-id="8231b-111">La **classe \_ VirtualEthernetSwitchNicTeamingSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8231b-111">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8231b-112">**LoadBalancingAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="8231b-112">**LoadBalancingAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8231b-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8231b-113">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="8231b-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8231b-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8231b-115">Qualificatori: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8231b-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8231b-116">Algoritmo di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="8231b-116">The load balancing algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="8231b-117">**TeamingMode**</span><span class="sxs-lookup"><span data-stu-id="8231b-117">**TeamingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8231b-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8231b-118">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="8231b-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8231b-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8231b-120">Qualificatori: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="8231b-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8231b-121">Modalità gruppo.</span><span class="sxs-lookup"><span data-stu-id="8231b-121">The teaming mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8231b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8231b-122">Requirements</span></span>



| <span data-ttu-id="8231b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8231b-123">Requirement</span></span> | <span data-ttu-id="8231b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8231b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8231b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8231b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8231b-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8231b-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8231b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8231b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8231b-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8231b-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8231b-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8231b-129">Namespace</span></span><br/>                | <span data-ttu-id="8231b-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8231b-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8231b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8231b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8231b-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8231b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8231b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8231b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8231b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8231b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8231b-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8231b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8231b-136">**\_EthernetSwitchFeatureSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="8231b-136">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




