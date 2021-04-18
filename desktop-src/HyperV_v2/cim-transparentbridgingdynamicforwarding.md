---
description: Associa un servizio di bridging trasparente a una voce del database di inoltri.
ms.assetid: 6db93e71-c9b7-4710-a9ee-99a1055cfd82
title: Classe CIM_TransparentBridgingDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingDynamicForwarding
- CIM_TransparentBridgingDynamicForwarding.Antecedent
- CIM_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d089ca662880ad269cb9d9c63cb0935ff6de0b5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310570"
---
# <a name="cim_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="07e55-103">CIM \_ TransparentBridgingDynamicForwarding (classe)</span><span class="sxs-lookup"><span data-stu-id="07e55-103">CIM\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="07e55-104">Associa un servizio di bridging trasparente a una voce del database di inoltri.</span><span class="sxs-lookup"><span data-stu-id="07e55-104">Associates a transparent bridging service with an entry of its forwarding database.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e55-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07e55-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingDynamicForwarding : CIM_Dependency
{
  CIM_TransparentBridgingService REF Antecedent;
  CIM_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="07e55-106">Members</span><span class="sxs-lookup"><span data-stu-id="07e55-106">Members</span></span>

<span data-ttu-id="07e55-107">La classe **CIM \_ TransparentBridgingDynamicForwarding** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="07e55-107">The **CIM\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="07e55-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07e55-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07e55-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07e55-109">Properties</span></span>

<span data-ttu-id="07e55-110">La classe **CIM \_ TransparentBridgingDynamicForwarding** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="07e55-110">The **CIM\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07e55-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="07e55-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07e55-112">Tipo di dati: **CIM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="07e55-112">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="07e55-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07e55-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07e55-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="07e55-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="07e55-115">Riferimento [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) al servizio bridging trasparente.</span><span class="sxs-lookup"><span data-stu-id="07e55-115">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="07e55-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="07e55-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07e55-117">Tipo di dati: **CIM \_ DynamicForwardingEntry**</span><span class="sxs-lookup"><span data-stu-id="07e55-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="07e55-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07e55-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07e55-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="07e55-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="07e55-120">Riferimento [**CIM \_ DynamicForwardingEntry**](cim-dynamicforwardingentry.md) alla voce del database di inoltri.</span><span class="sxs-lookup"><span data-stu-id="07e55-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the forwarding database entry.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07e55-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07e55-121">Requirements</span></span>



| <span data-ttu-id="07e55-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="07e55-122">Requirement</span></span> | <span data-ttu-id="07e55-123">Valore</span><span class="sxs-lookup"><span data-stu-id="07e55-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07e55-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07e55-124">Minimum supported client</span></span><br/> | <span data-ttu-id="07e55-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="07e55-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="07e55-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07e55-126">Minimum supported server</span></span><br/> | <span data-ttu-id="07e55-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="07e55-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="07e55-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07e55-128">Namespace</span></span><br/>                | <span data-ttu-id="07e55-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="07e55-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="07e55-130">MOF</span><span class="sxs-lookup"><span data-stu-id="07e55-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07e55-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07e55-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="07e55-132">DLL</span><span class="sxs-lookup"><span data-stu-id="07e55-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07e55-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="07e55-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="07e55-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07e55-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07e55-135">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="07e55-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

