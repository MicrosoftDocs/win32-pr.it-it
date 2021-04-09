---
description: Definisce l'associazione tra un comswitch Ethernet e una risorsa switch.
ms.assetid: fb29f4cb-50c4-4865-b267-21ff99bb4a8b
title: Classe Msvm_EthernetSwitchInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchInfo
- Msvm_EthernetSwitchInfo.Antecedent
- Msvm_EthernetSwitchInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1106e0930716572b10a95846865d8f90aa991cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968765"
---
# <a name="msvm_ethernetswitchinfo-class"></a><span data-ttu-id="2f58d-103">\_Classe MSVM EthernetSwitchInfo</span><span class="sxs-lookup"><span data-stu-id="2f58d-103">Msvm\_EthernetSwitchInfo class</span></span>

<span data-ttu-id="2f58d-104">Definisce l'associazione tra un comswitch Ethernet e una risorsa switch.</span><span class="sxs-lookup"><span data-stu-id="2f58d-104">Defines the association between an Ethernet switch and a switch resource.</span></span>

<span data-ttu-id="2f58d-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2f58d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f58d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f58d-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchInfo : CIM_Dependency
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  Msvm_EthernetSwitchData    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2f58d-107">Members</span><span class="sxs-lookup"><span data-stu-id="2f58d-107">Members</span></span>

<span data-ttu-id="2f58d-108">La **classe \_ EthernetSwitchInfo di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2f58d-108">The **Msvm\_EthernetSwitchInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="2f58d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2f58d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f58d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2f58d-110">Properties</span></span>

<span data-ttu-id="2f58d-111">La **classe \_ EthernetSwitchInfo di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2f58d-111">The **Msvm\_EthernetSwitchInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f58d-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="2f58d-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f58d-113">Tipo di dati: **MSVM \_ VirtualEthernetSwitch**</span><span class="sxs-lookup"><span data-stu-id="2f58d-113">Data type: **Msvm\_VirtualEthernetSwitch**</span></span>
</dt> <dt>

<span data-ttu-id="2f58d-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f58d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f58d-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="2f58d-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2f58d-116">Riferimento alla classe [**\_ VirtualEthernetSwitch di MSVM**](msvm-virtualethernetswitch.md) che rappresenta il sistema host.</span><span class="sxs-lookup"><span data-stu-id="2f58d-116">A reference to the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the hosting system.</span></span> <span data-ttu-id="2f58d-117">Questa proprietà è derivata dalla [**\_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="2f58d-117">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="2f58d-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="2f58d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f58d-119">Tipo di dati: **MSVM \_ EthernetSwitchData**</span><span class="sxs-lookup"><span data-stu-id="2f58d-119">Data type: **Msvm\_EthernetSwitchData**</span></span>
</dt> <dt>

<span data-ttu-id="2f58d-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f58d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f58d-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="2f58d-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2f58d-122">Riferimento alla classe [**\_ EthernetSwitchData MSVM**](msvm-ethernetswitchdata.md) che rappresenta la risorsa switch.</span><span class="sxs-lookup"><span data-stu-id="2f58d-122">A reference to the [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md) class that represents the switch resource.</span></span> <span data-ttu-id="2f58d-123">Questa proprietà è derivata dalla [**\_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="2f58d-123">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f58d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f58d-124">Requirements</span></span>



| <span data-ttu-id="2f58d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f58d-125">Requirement</span></span> | <span data-ttu-id="2f58d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2f58d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f58d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f58d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2f58d-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2f58d-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2f58d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f58d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2f58d-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2f58d-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f58d-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2f58d-131">Namespace</span></span><br/>                | <span data-ttu-id="2f58d-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2f58d-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2f58d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2f58d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f58d-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f58d-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f58d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2f58d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f58d-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f58d-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

