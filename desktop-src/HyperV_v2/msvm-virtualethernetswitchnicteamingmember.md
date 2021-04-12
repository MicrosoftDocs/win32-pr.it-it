---
description: Rappresenta l'associazione tra un ExternalEthernetPort del team e un ExternalEthernetPort del membro.
ms.assetid: e21bea94-d6a8-4788-958e-78ce255837aa
title: Classe Msvm_VirtualEthernetSwitchNicTeamingMember
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingMember
- Msvm_VirtualEthernetSwitchNicTeamingMember.Antecedent
- Msvm_VirtualEthernetSwitchNicTeamingMember.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbf83f4605d6ab1b7bc9740b14c493393eb93163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234360"
---
# <a name="msvm_virtualethernetswitchnicteamingmember-class"></a><span data-ttu-id="1673e-103">\_Classe MSVM VirtualEthernetSwitchNicTeamingMember</span><span class="sxs-lookup"><span data-stu-id="1673e-103">Msvm\_VirtualEthernetSwitchNicTeamingMember class</span></span>

<span data-ttu-id="1673e-104">Rappresenta l'associazione tra un ExternalEthernetPort del team e un ExternalEthernetPort del membro.</span><span class="sxs-lookup"><span data-stu-id="1673e-104">Represents the association between a team ExternalEthernetPort and a member ExternalEthernetPort.</span></span>

<span data-ttu-id="1673e-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1673e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1673e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1673e-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingMember : CIM_Dependency
{
  Msvm_ExternalEthernetPort REF Antecedent;
  Msvm_ExternalEthernetPort REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1673e-107">Members</span><span class="sxs-lookup"><span data-stu-id="1673e-107">Members</span></span>

<span data-ttu-id="1673e-108">La **classe \_ VirtualEthernetSwitchNicTeamingMember di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1673e-108">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these types of members:</span></span>

-   [<span data-ttu-id="1673e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1673e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1673e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1673e-110">Properties</span></span>

<span data-ttu-id="1673e-111">La **classe \_ VirtualEthernetSwitchNicTeamingMember di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1673e-111">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1673e-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="1673e-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1673e-113">Tipo di dati: **MSVM \_ ExternalEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="1673e-113">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="1673e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1673e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1673e-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="1673e-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="1673e-116">Un [**\_ ExternalEthernetPort MSVM**](msvm-externalethernetport.md) che fa riferimento all'istanza della porta Ethernet esterna del team.</span><span class="sxs-lookup"><span data-stu-id="1673e-116">An [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) that references the team external ethernet port instance.</span></span>

</dd> <dt>

<span data-ttu-id="1673e-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="1673e-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1673e-118">Tipo di dati: **MSVM \_ ExternalEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="1673e-118">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="1673e-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1673e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1673e-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="1673e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1673e-121">Riferimento all'istanza [**\_ ExternalEthernetPort**](msvm-externalethernetport.md) del membro MSVM.</span><span class="sxs-lookup"><span data-stu-id="1673e-121">Reference to the member [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1673e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1673e-122">Requirements</span></span>



| <span data-ttu-id="1673e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1673e-123">Requirement</span></span> | <span data-ttu-id="1673e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1673e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1673e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1673e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1673e-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1673e-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="1673e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1673e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1673e-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1673e-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1673e-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1673e-129">Namespace</span></span><br/>                | <span data-ttu-id="1673e-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1673e-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1673e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1673e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1673e-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1673e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1673e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1673e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1673e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1673e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1673e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1673e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1673e-136">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="1673e-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

