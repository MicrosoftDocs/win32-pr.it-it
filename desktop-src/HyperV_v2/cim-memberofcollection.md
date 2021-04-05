---
description: Rappresenta una relazione in cui un elemento gestito è un membro di e viene aggregato da una raccolta.
ms.assetid: 324284fa-ece6-41df-9891-040a7561dce4
title: Classe CIM_MemberOfCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemberOfCollection
- CIM_MemberOfCollection.Collection
- CIM_MemberOfCollection.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9bcebfb08cbbc0cb18e00f1b0e5e2646ca086faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057823"
---
# <a name="cim_memberofcollection-class"></a><span data-ttu-id="4728f-103">CIM \_ MemberOfCollection (classe)</span><span class="sxs-lookup"><span data-stu-id="4728f-103">CIM\_MemberOfCollection class</span></span>

<span data-ttu-id="4728f-104">Rappresenta una relazione in cui un elemento gestito è un membro di e viene aggregato da una raccolta.</span><span class="sxs-lookup"><span data-stu-id="4728f-104">Represents a relationship in which a managed element is a member of and is aggregated by a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4728f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4728f-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_MemberOfCollection
{
  CIM_Collection     REF Collection;
  CIM_ManagedElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="4728f-106">Members</span><span class="sxs-lookup"><span data-stu-id="4728f-106">Members</span></span>

<span data-ttu-id="4728f-107">La classe **CIM \_ MemberOfCollection** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4728f-107">The **CIM\_MemberOfCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="4728f-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4728f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4728f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4728f-109">Properties</span></span>

<span data-ttu-id="4728f-110">La classe **CIM \_ MemberOfCollection** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4728f-110">The **CIM\_MemberOfCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4728f-111">**Raccolta**</span><span class="sxs-lookup"><span data-stu-id="4728f-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4728f-112">Tipo di dati **: \_ raccolta CIM**</span><span class="sxs-lookup"><span data-stu-id="4728f-112">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="4728f-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4728f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4728f-114">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**aggregazione**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4728f-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4728f-115">Raccolta che aggrega i membri.</span><span class="sxs-lookup"><span data-stu-id="4728f-115">The collection that aggregates members.</span></span>

</dd> <dt>

<span data-ttu-id="4728f-116">**Membro**</span><span class="sxs-lookup"><span data-stu-id="4728f-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4728f-117">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="4728f-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4728f-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4728f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4728f-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4728f-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4728f-120">Membro della raccolta.</span><span class="sxs-lookup"><span data-stu-id="4728f-120">The member of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4728f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4728f-121">Requirements</span></span>



| <span data-ttu-id="4728f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4728f-122">Requirement</span></span> | <span data-ttu-id="4728f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4728f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4728f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4728f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4728f-125">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4728f-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4728f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4728f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4728f-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4728f-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4728f-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4728f-128">Namespace</span></span><br/>                | <span data-ttu-id="4728f-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4728f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4728f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4728f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4728f-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4728f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4728f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4728f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4728f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4728f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

