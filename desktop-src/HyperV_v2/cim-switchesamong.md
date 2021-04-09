---
description: Rappresenta un servizio di commutazione, che passa i frame tra le porte di commutazione.
ms.assetid: ee2d4831-df00-408c-b350-26d2d1d3e8aa
title: Classe CIM_SwitchesAmong
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchesAmong
- CIM_SwitchesAmong.Antecedent
- CIM_SwitchesAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16a87797b4a138ef79be3d5ea8c6304d2ce4a942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129690"
---
# <a name="cim_switchesamong-class"></a><span data-ttu-id="b3ac4-103">CIM \_ SwitchesAmong (classe)</span><span class="sxs-lookup"><span data-stu-id="b3ac4-103">CIM\_SwitchesAmong class</span></span>

<span data-ttu-id="b3ac4-104">Rappresenta un servizio di commutazione, che passa i frame tra le porte di commutazione.</span><span class="sxs-lookup"><span data-stu-id="b3ac4-104">Represents a switch service, which switches frames between switch ports.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ac4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3ac4-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchesAmong : CIM_ForwardsAmong
{
  CIM_SwitchPort    REF Antecedent;
  CIM_SwitchService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b3ac4-106">Members</span><span class="sxs-lookup"><span data-stu-id="b3ac4-106">Members</span></span>

<span data-ttu-id="b3ac4-107">La classe **CIM \_ SwitchesAmong** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b3ac4-107">The **CIM\_SwitchesAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="b3ac4-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3ac4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3ac4-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3ac4-109">Properties</span></span>

<span data-ttu-id="b3ac4-110">La classe **CIM \_ SwitchesAmong** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3ac4-110">The **CIM\_SwitchesAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3ac4-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b3ac4-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3ac4-112">Tipo di dati: **CIM \_ SwitchPort**</span><span class="sxs-lookup"><span data-stu-id="b3ac4-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="b3ac4-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3ac4-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3ac4-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="b3ac4-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b3ac4-115">Riferimento [**CIM \_ SwitchPort**](cim-switchport.md) alla porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="b3ac4-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="b3ac4-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="b3ac4-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3ac4-117">Tipo di dati: **CIM \_ SwitchService**</span><span class="sxs-lookup"><span data-stu-id="b3ac4-117">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="b3ac4-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3ac4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3ac4-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="b3ac4-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b3ac4-120">Riferimento [**CIM \_ SwitchService**](cim-switchservice.md) al servizio di cambio.</span><span class="sxs-lookup"><span data-stu-id="b3ac4-120">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3ac4-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3ac4-121">Requirements</span></span>



| <span data-ttu-id="b3ac4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3ac4-122">Requirement</span></span> | <span data-ttu-id="b3ac4-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b3ac4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ac4-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3ac4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b3ac4-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b3ac4-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b3ac4-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3ac4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b3ac4-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b3ac4-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b3ac4-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b3ac4-128">Namespace</span></span><br/>                | <span data-ttu-id="b3ac4-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b3ac4-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b3ac4-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b3ac4-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3ac4-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3ac4-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3ac4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b3ac4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3ac4-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b3ac4-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b3ac4-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3ac4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ac4-135">**\_FORWARDSAMONG CIM**</span><span class="sxs-lookup"><span data-stu-id="b3ac4-135">**CIM\_ForwardsAmong**</span></span>](cim-forwardsamong.md)
</dt> </dl>

 

