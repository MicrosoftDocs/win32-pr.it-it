---
description: Rappresenta un'associazione generica tra una raccolta di elementi di sistema gestiti e i membri della raccolta.
ms.assetid: c9e2bbca-67be-41f2-a94c-cf4eaf5f4694
title: Classe CIM_CollectedMSEs (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdf5c5d682f1b6e1b47b64100b3e00f5f79cebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315524"
---
# <a name="cim_collectedmses-class-hyper-v-management"></a><span data-ttu-id="72317-103">Classe CIM_CollectedMSEs (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="72317-103">CIM_CollectedMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="72317-104">Rappresenta un'associazione generica tra una raccolta di elementi di sistema gestiti e i membri della raccolta.</span><span class="sxs-lookup"><span data-stu-id="72317-104">Represents a generic association between a collection of managed system elements and the members of the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="72317-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72317-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectedMSEs : CIM_MemberOfCollection
{
  CIM_CollectionOfMSEs     REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="72317-106">Members</span><span class="sxs-lookup"><span data-stu-id="72317-106">Members</span></span>

<span data-ttu-id="72317-107">La classe **CIM \_ CollectedMSEs** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="72317-107">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="72317-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72317-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72317-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72317-109">Properties</span></span>

<span data-ttu-id="72317-110">La classe **CIM \_ CollectedMSEs** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="72317-110">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72317-111">**Raccolta**</span><span class="sxs-lookup"><span data-stu-id="72317-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72317-112">Tipo di dati: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="72317-112">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="72317-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72317-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72317-114">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="72317-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="72317-115">Raccolta.</span><span class="sxs-lookup"><span data-stu-id="72317-115">The collection.</span></span>

</dd> <dt>

<span data-ttu-id="72317-116">**Membro**</span><span class="sxs-lookup"><span data-stu-id="72317-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72317-117">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="72317-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="72317-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72317-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72317-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="72317-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="72317-120">Membri della raccolta.</span><span class="sxs-lookup"><span data-stu-id="72317-120">The members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72317-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72317-121">Requirements</span></span>



| <span data-ttu-id="72317-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="72317-122">Requirement</span></span> | <span data-ttu-id="72317-123">Valore</span><span class="sxs-lookup"><span data-stu-id="72317-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72317-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72317-124">Minimum supported client</span></span><br/> | <span data-ttu-id="72317-125">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="72317-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="72317-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72317-126">Minimum supported server</span></span><br/> | <span data-ttu-id="72317-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="72317-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="72317-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="72317-128">Namespace</span></span><br/>                | <span data-ttu-id="72317-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="72317-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="72317-130">MOF</span><span class="sxs-lookup"><span data-stu-id="72317-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72317-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72317-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72317-132">DLL</span><span class="sxs-lookup"><span data-stu-id="72317-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72317-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72317-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72317-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72317-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72317-135">**\_MEMBEROFCOLLECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="72317-135">**CIM\_MemberOfCollection**</span></span>](cim-memberofcollection.md)
</dt> </dl>

 

