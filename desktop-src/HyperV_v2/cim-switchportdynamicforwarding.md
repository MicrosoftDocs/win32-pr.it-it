---
description: Rappresenta un'associazione in cui una voce di un database di inoltri viene applicata a una porta di commutazione.
ms.assetid: e63ac61d-ed0c-49e9-b056-4fcb6d1d5455
title: Classe CIM_SwitchPortDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPortDynamicForwarding
- CIM_SwitchPortDynamicForwarding.Antecedent
- CIM_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e0d87e2ee5df6a7564d92fd1f8421dfa09abe20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310582"
---
# <a name="cim_switchportdynamicforwarding-class"></a><span data-ttu-id="60a2f-103">CIM \_ SwitchPortDynamicForwarding (classe)</span><span class="sxs-lookup"><span data-stu-id="60a2f-103">CIM\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="60a2f-104">Rappresenta un'associazione in cui una voce di un database di inoltri viene applicata a una porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="60a2f-104">Represents an association in which an entry of a forwarding database applies to a switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="60a2f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60a2f-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_SwitchPortDynamicForwarding : CIM_Dependency
{
  CIM_SwitchPort             REF Antecedent;
  CIM_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="60a2f-106">Members</span><span class="sxs-lookup"><span data-stu-id="60a2f-106">Members</span></span>

<span data-ttu-id="60a2f-107">La classe **CIM \_ SwitchPortDynamicForwarding** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="60a2f-107">The **CIM\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="60a2f-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="60a2f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60a2f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="60a2f-109">Properties</span></span>

<span data-ttu-id="60a2f-110">La classe **CIM \_ SwitchPortDynamicForwarding** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="60a2f-110">The **CIM\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60a2f-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="60a2f-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60a2f-112">Tipo di dati: **CIM \_ SwitchPort**</span><span class="sxs-lookup"><span data-stu-id="60a2f-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="60a2f-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="60a2f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60a2f-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="60a2f-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="60a2f-115">Riferimento [**CIM \_ SwitchPort**](cim-switchport.md) alla porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="60a2f-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="60a2f-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="60a2f-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60a2f-117">Tipo di dati: **CIM \_ DynamicForwardingEntry**</span><span class="sxs-lookup"><span data-stu-id="60a2f-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="60a2f-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="60a2f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60a2f-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="60a2f-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="60a2f-120">Riferimento [**CIM \_ DynamicForwardingEntry**](cim-dynamicforwardingentry.md) alla voce del database di invio.</span><span class="sxs-lookup"><span data-stu-id="60a2f-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60a2f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60a2f-121">Requirements</span></span>



| <span data-ttu-id="60a2f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="60a2f-122">Requirement</span></span> | <span data-ttu-id="60a2f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="60a2f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60a2f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60a2f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="60a2f-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="60a2f-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="60a2f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60a2f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="60a2f-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60a2f-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="60a2f-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="60a2f-128">Namespace</span></span><br/>                | <span data-ttu-id="60a2f-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="60a2f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="60a2f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="60a2f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60a2f-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60a2f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60a2f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="60a2f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60a2f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60a2f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60a2f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60a2f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60a2f-135">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="60a2f-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

