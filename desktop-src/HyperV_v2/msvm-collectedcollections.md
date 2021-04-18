---
description: Associa il \_ VirtualSystemCollection MSVM agli oggetti contenuti MSVM \_ ComputerSystem.
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Classe Msvm_CollectedCollections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedCollections
- Msvm_CollectedCollections.Collection
- Msvm_CollectedCollections.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16ec6ad77c44e0a4e9001a0cb77d227573635ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319519"
---
# <a name="msvm_collectedcollections-class"></a><span data-ttu-id="38501-103">\_Classe MSVM CollectedCollections</span><span class="sxs-lookup"><span data-stu-id="38501-103">Msvm\_CollectedCollections class</span></span>

<span data-ttu-id="38501-104">Associa il [**\_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) agli oggetti contenuti [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="38501-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="38501-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="38501-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="38501-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38501-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a><span data-ttu-id="38501-107">Members</span><span class="sxs-lookup"><span data-stu-id="38501-107">Members</span></span>

<span data-ttu-id="38501-108">La **classe \_ CollectedCollections di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="38501-108">The **Msvm\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="38501-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="38501-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38501-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="38501-110">Properties</span></span>

<span data-ttu-id="38501-111">La **classe \_ CollectedCollections di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="38501-111">The **Msvm\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38501-112">**Raccolta**</span><span class="sxs-lookup"><span data-stu-id="38501-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38501-113">Tipo di dati: **MSVM \_ managementcollection**</span><span class="sxs-lookup"><span data-stu-id="38501-113">Data type: **Msvm\_ManagementCollection**</span></span>
</dt> <dt>

<span data-ttu-id="38501-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38501-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38501-115">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="38501-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="38501-116">Oggetto di raggruppamento o ' contenitore ' di [**MSVM \_ managementcollection**](msvm-managementcollection.md) che rappresenta la raccolta.</span><span class="sxs-lookup"><span data-stu-id="38501-116">An [**Msvm\_ManagementCollection**](msvm-managementcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="38501-117">**Membro**</span><span class="sxs-lookup"><span data-stu-id="38501-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38501-118">Tipo di dati: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="38501-118">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="38501-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38501-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38501-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="38501-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="38501-121">[**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) contenente i membri della raccolta.</span><span class="sxs-lookup"><span data-stu-id="38501-121">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38501-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38501-122">Requirements</span></span>



| <span data-ttu-id="38501-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="38501-123">Requirement</span></span> | <span data-ttu-id="38501-124">Valore</span><span class="sxs-lookup"><span data-stu-id="38501-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38501-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38501-125">Minimum supported client</span></span><br/> | <span data-ttu-id="38501-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="38501-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="38501-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38501-127">Minimum supported server</span></span><br/> | <span data-ttu-id="38501-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="38501-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="38501-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="38501-129">Namespace</span></span><br/>                | <span data-ttu-id="38501-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="38501-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="38501-131">MOF</span><span class="sxs-lookup"><span data-stu-id="38501-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38501-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38501-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38501-133">DLL</span><span class="sxs-lookup"><span data-stu-id="38501-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38501-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38501-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="38501-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38501-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38501-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="38501-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

