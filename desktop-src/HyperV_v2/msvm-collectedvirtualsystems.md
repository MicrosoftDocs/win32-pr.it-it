---
description: 'Msvm_CollectedVirtualSystems classe: associa Msvm \_ VirtualSystemCollection agli oggetti Msvm \_ ComputerSystem contenuti.'
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Msvm_CollectedVirtualSystems classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedVirtualSystems
- Msvm_CollectedVirtualSystems.Collection
- Msvm_CollectedVirtualSystems.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6775f41a6e2ae7e45bac642fcd32b8deaec3fda
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119279"
---
# <a name="msvm_collectedvirtualsystems-class"></a><span data-ttu-id="e028f-103">Classe Msvm \_ CollectedVirtualSystems</span><span class="sxs-lookup"><span data-stu-id="e028f-103">Msvm\_CollectedVirtualSystems class</span></span>

<span data-ttu-id="e028f-104">Associa [**Msvm \_ VirtualSystemCollection agli**](msvm-virtualsystemcollection.md) oggetti [**Msvm \_ ComputerSystem**](msvm-computersystem.md) contenuti.</span><span class="sxs-lookup"><span data-stu-id="e028f-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="e028f-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e028f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e028f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e028f-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a><span data-ttu-id="e028f-107">Members</span><span class="sxs-lookup"><span data-stu-id="e028f-107">Members</span></span>

<span data-ttu-id="e028f-108">La **classe Msvm \_ CollectedVirtualSystems** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e028f-108">The **Msvm\_CollectedVirtualSystems** class has these types of members:</span></span>

-   [<span data-ttu-id="e028f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e028f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e028f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e028f-110">Properties</span></span>

<span data-ttu-id="e028f-111">La **classe Msvm \_ CollectedVirtualSystems** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e028f-111">The **Msvm\_CollectedVirtualSystems** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e028f-112">**Raccolta**</span><span class="sxs-lookup"><span data-stu-id="e028f-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e028f-113">Tipo di dati: **Msvm \_ VirtualSystemCollection**</span><span class="sxs-lookup"><span data-stu-id="e028f-113">Data type: **Msvm\_VirtualSystemCollection**</span></span>
</dt> <dt>

<span data-ttu-id="e028f-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e028f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e028f-115">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="e028f-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="e028f-116">Oggetto di raggruppamento o "bag" [**di Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) che rappresenta la raccolta.</span><span class="sxs-lookup"><span data-stu-id="e028f-116">An [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="e028f-117">**Membro**</span><span class="sxs-lookup"><span data-stu-id="e028f-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e028f-118">Tipo di dati: **Msvm \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="e028f-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e028f-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e028f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e028f-120">Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="e028f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="e028f-121">Oggetto [**Msvm \_ ComputerSystem**](msvm-computersystem.md) contenente i membri della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e028f-121">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) object containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e028f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e028f-122">Requirements</span></span>



| <span data-ttu-id="e028f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e028f-123">Requirement</span></span> | <span data-ttu-id="e028f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e028f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e028f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e028f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e028f-126">Windows 10 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e028f-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e028f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e028f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e028f-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e028f-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e028f-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e028f-129">Namespace</span></span><br/>                | <span data-ttu-id="e028f-130">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e028f-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e028f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e028f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e028f-132"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="e028f-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e028f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e028f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e028f-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e028f-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e028f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e028f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e028f-136">**CIM \_ CollectedMSEs**</span><span class="sxs-lookup"><span data-stu-id="e028f-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

