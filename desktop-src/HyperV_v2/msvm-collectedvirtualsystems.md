---
description: Associa il \_ VirtualSystemCollection MSVM agli oggetti contenuti MSVM \_ ComputerSystem.
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Classe Msvm_CollectedVirtualSystems
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
ms.openlocfilehash: 0803eda14ffbaf21ee2bf4491bd835123b7191e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317205"
---
# <a name="msvm_collectedvirtualsystems-class"></a><span data-ttu-id="d7c7d-103">\_Classe MSVM CollectedVirtualSystems</span><span class="sxs-lookup"><span data-stu-id="d7c7d-103">Msvm\_CollectedVirtualSystems class</span></span>

<span data-ttu-id="d7c7d-104">Associa il [**\_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) agli oggetti contenuti [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="d7c7d-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="d7c7d-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d7c7d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c7d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7c7d-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a><span data-ttu-id="d7c7d-107">Members</span><span class="sxs-lookup"><span data-stu-id="d7c7d-107">Members</span></span>

<span data-ttu-id="d7c7d-108">La **classe \_ CollectedVirtualSystems di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d7c7d-108">The **Msvm\_CollectedVirtualSystems** class has these types of members:</span></span>

-   [<span data-ttu-id="d7c7d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d7c7d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7c7d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d7c7d-110">Properties</span></span>

<span data-ttu-id="d7c7d-111">La **classe \_ CollectedVirtualSystems di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d7c7d-111">The **Msvm\_CollectedVirtualSystems** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7c7d-112">**Raccolta**</span><span class="sxs-lookup"><span data-stu-id="d7c7d-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7c7d-113">Tipo di dati: **MSVM \_ VirtualSystemCollection**</span><span class="sxs-lookup"><span data-stu-id="d7c7d-113">Data type: **Msvm\_VirtualSystemCollection**</span></span>
</dt> <dt>

<span data-ttu-id="d7c7d-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d7c7d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7c7d-115">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="d7c7d-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="d7c7d-116">Oggetto di raggruppamento o ' contenitore ' di [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) che rappresenta la raccolta.</span><span class="sxs-lookup"><span data-stu-id="d7c7d-116">An [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="d7c7d-117">**Membro**</span><span class="sxs-lookup"><span data-stu-id="d7c7d-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7c7d-118">Tipo di dati: **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="d7c7d-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d7c7d-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d7c7d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7c7d-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="d7c7d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="d7c7d-121">Oggetto [**MSVM \_ ComputerSystem**](msvm-computersystem.md) contenente i membri della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d7c7d-121">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) object containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7c7d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7c7d-122">Requirements</span></span>



| <span data-ttu-id="d7c7d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7c7d-123">Requirement</span></span> | <span data-ttu-id="d7c7d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d7c7d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c7d-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7c7d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d7c7d-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d7c7d-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d7c7d-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7c7d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d7c7d-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d7c7d-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d7c7d-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d7c7d-129">Namespace</span></span><br/>                | <span data-ttu-id="d7c7d-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d7c7d-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d7c7d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d7c7d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7c7d-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7c7d-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7c7d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d7c7d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7c7d-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d7c7d-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d7c7d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7c7d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c7d-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="d7c7d-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

