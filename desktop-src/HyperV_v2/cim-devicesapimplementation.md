---
description: Rappresenta un'associazione tra un punto di accesso al servizio (SAP) e un dispositivo logico che lo implementa.
ms.assetid: 40c8111a-d439-4c0f-805e-9c10d7182eb4
title: Classe CIM_DeviceSAPImplementation (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Antecedent
- CIM_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e32676077cccd5c7e17fa551e904079f457b8d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308356"
---
# <a name="cim_devicesapimplementation-class-hyper-v-management"></a><span data-ttu-id="2d253-103">Classe CIM_DeviceSAPImplementation (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="2d253-103">CIM_DeviceSAPImplementation class (Hyper-V management)</span></span>

<span data-ttu-id="2d253-104">Rappresenta un'associazione tra un punto di accesso al servizio (SAP) e un dispositivo logico che lo implementa.</span><span class="sxs-lookup"><span data-stu-id="2d253-104">Represents an association between a service access point (SAP) and a logical device that implements it.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d253-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d253-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2d253-106">Members</span><span class="sxs-lookup"><span data-stu-id="2d253-106">Members</span></span>

<span data-ttu-id="2d253-107">La classe **CIM \_ DeviceSAPImplementation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2d253-107">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="2d253-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d253-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d253-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d253-109">Properties</span></span>

<span data-ttu-id="2d253-110">La classe **CIM \_ DeviceSAPImplementation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2d253-110">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d253-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="2d253-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d253-112">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="2d253-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="2d253-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d253-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d253-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="2d253-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2d253-115">Il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2d253-115">The logical device.</span></span>

</dd> <dt>

<span data-ttu-id="2d253-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="2d253-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d253-117">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="2d253-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="2d253-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d253-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d253-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="2d253-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2d253-120">SAP implementato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2d253-120">The SAP implemented by the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d253-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d253-121">Requirements</span></span>



| <span data-ttu-id="2d253-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d253-122">Requirement</span></span> | <span data-ttu-id="2d253-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2d253-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d253-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d253-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2d253-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2d253-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2d253-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d253-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2d253-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d253-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2d253-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2d253-128">Namespace</span></span><br/>                | <span data-ttu-id="2d253-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2d253-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2d253-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2d253-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d253-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d253-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d253-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2d253-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d253-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d253-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d253-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d253-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d253-135">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="2d253-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

