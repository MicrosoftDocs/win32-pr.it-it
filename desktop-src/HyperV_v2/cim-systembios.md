---
description: Associa un BIOS a un sistema di computer.
ms.assetid: a06af789-75c8-4d58-8a25-572dcf1091e2
title: Classe CIM_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemBIOS
- CIM_SystemBIOS.GroupComponent
- CIM_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: faa3130544fdb97bdf216fa266bc9e8cfe1815bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049831"
---
# <a name="cim_systembios-class"></a><span data-ttu-id="1afca-103">CIM \_ SystemBIOS (classe)</span><span class="sxs-lookup"><span data-stu-id="1afca-103">CIM\_SystemBIOS class</span></span>

<span data-ttu-id="1afca-104">Associa un BIOS a un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="1afca-104">Associates a BIOS with a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1afca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1afca-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_SystemBIOS : CIM_SystemComponent
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_BIOSElement    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="1afca-106">Members</span><span class="sxs-lookup"><span data-stu-id="1afca-106">Members</span></span>

<span data-ttu-id="1afca-107">La classe **CIM \_ SystemBIOS** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1afca-107">The **CIM\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="1afca-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1afca-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1afca-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1afca-109">Properties</span></span>

<span data-ttu-id="1afca-110">La classe **CIM \_ SystemBIOS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1afca-110">The **CIM\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1afca-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="1afca-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1afca-112">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="1afca-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="1afca-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1afca-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1afca-114">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="1afca-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1afca-115">Il computer che si avvia dal BIOS.</span><span class="sxs-lookup"><span data-stu-id="1afca-115">The computer system that boots from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="1afca-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1afca-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1afca-117">Tipo di dati: **CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="1afca-117">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="1afca-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1afca-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1afca-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="1afca-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="1afca-120">Il BIOS.</span><span class="sxs-lookup"><span data-stu-id="1afca-120">The BIOS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1afca-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1afca-121">Requirements</span></span>



| <span data-ttu-id="1afca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1afca-122">Requirement</span></span> | <span data-ttu-id="1afca-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1afca-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1afca-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1afca-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1afca-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1afca-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1afca-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1afca-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1afca-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1afca-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1afca-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1afca-128">Namespace</span></span><br/>                | <span data-ttu-id="1afca-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1afca-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1afca-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1afca-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1afca-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1afca-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1afca-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1afca-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1afca-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1afca-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1afca-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1afca-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1afca-135">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="1afca-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

