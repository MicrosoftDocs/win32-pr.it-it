---
description: Rappresenta i dati dell'impostazione del dominio di routing.
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Classe Msvm_EthernetSwitchPortRoutingDomainSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 40e16a3c952e63ab89c345201742dafe24cdde7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885863"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a><span data-ttu-id="88c46-103">\_Classe MSVM EthernetSwitchPortRoutingDomainSettingData</span><span class="sxs-lookup"><span data-stu-id="88c46-103">Msvm\_EthernetSwitchPortRoutingDomainSettingData class</span></span>

<span data-ttu-id="88c46-104">Rappresenta i dati dell'impostazione del dominio di routing.</span><span class="sxs-lookup"><span data-stu-id="88c46-104">Represents the routing domain setting data.</span></span>

<span data-ttu-id="88c46-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="88c46-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="88c46-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88c46-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a><span data-ttu-id="88c46-107">Members</span><span class="sxs-lookup"><span data-stu-id="88c46-107">Members</span></span>

<span data-ttu-id="88c46-108">La **classe \_ EthernetSwitchPortRoutingDomainSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="88c46-108">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="88c46-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="88c46-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88c46-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="88c46-110">Properties</span></span>

<span data-ttu-id="88c46-111">La **classe \_ EthernetSwitchPortRoutingDomainSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="88c46-111">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88c46-112">**IsolationIdList**</span><span class="sxs-lookup"><span data-stu-id="88c46-112">**IsolationIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c46-113">Tipo di dati: matrice **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88c46-113">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="88c46-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="88c46-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="88c46-115">Qualificatori: **WmiDataId** (3), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="88c46-115">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="88c46-116">ID VirtualSubnetId o VLAN per i domini di routing.</span><span class="sxs-lookup"><span data-stu-id="88c46-116">The VirtualSubnetId or VLAN IDs for the routing domains.</span></span>

</dd> <dt>

<span data-ttu-id="88c46-117">**IsolationIdNameList**</span><span class="sxs-lookup"><span data-stu-id="88c46-117">**IsolationIdNameList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c46-118">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="88c46-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="88c46-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="88c46-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="88c46-120">Qualificatori: **WmiDataId** (4), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="88c46-120">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="88c46-121">Matrice di nomi descrittivi VirtualSubnetId o VLAN.</span><span class="sxs-lookup"><span data-stu-id="88c46-121">The VirtualSubnetId or VLAN friendly name array.</span></span>

</dd> <dt>

<span data-ttu-id="88c46-122">**RoutingDomainGuid**</span><span class="sxs-lookup"><span data-stu-id="88c46-122">**RoutingDomainGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c46-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="88c46-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c46-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="88c46-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="88c46-125">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="88c46-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="88c46-126">GUID del dominio di routing.</span><span class="sxs-lookup"><span data-stu-id="88c46-126">The routing domain GUID.</span></span>

</dd> <dt>

<span data-ttu-id="88c46-127">**RoutingDomainName**</span><span class="sxs-lookup"><span data-stu-id="88c46-127">**RoutingDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c46-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="88c46-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88c46-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="88c46-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="88c46-130">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**versione**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisione**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="88c46-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="88c46-131">Nome descrittivo del dominio di routing.</span><span class="sxs-lookup"><span data-stu-id="88c46-131">The routing domain friendly name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88c46-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88c46-132">Requirements</span></span>



| <span data-ttu-id="88c46-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="88c46-133">Requirement</span></span> | <span data-ttu-id="88c46-134">Valore</span><span class="sxs-lookup"><span data-stu-id="88c46-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c46-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88c46-135">Minimum supported client</span></span><br/> | <span data-ttu-id="88c46-136">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="88c46-136">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="88c46-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88c46-137">Minimum supported server</span></span><br/> | <span data-ttu-id="88c46-138">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="88c46-138">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="88c46-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88c46-139">Namespace</span></span><br/>                | <span data-ttu-id="88c46-140">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="88c46-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="88c46-141">MOF</span><span class="sxs-lookup"><span data-stu-id="88c46-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88c46-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88c46-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="88c46-143">DLL</span><span class="sxs-lookup"><span data-stu-id="88c46-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88c46-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="88c46-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="88c46-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88c46-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88c46-146">**\_EthernetSwitchPortFeatureSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="88c46-146">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

