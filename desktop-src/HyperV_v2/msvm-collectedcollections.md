---
description: 'Msvm_CollectedCollections classe: associa Msvm \_ VirtualSystemCollection agli oggetti Msvm \_ ComputerSystem contenuti.'
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Msvm_CollectedCollections classe
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
ms.openlocfilehash: 83719d364fac22923d68206c8cfe7d37adad5edb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112129"
---
# <a name="msvm_collectedcollections-class"></a><span data-ttu-id="56f81-103">Classe Msvm \_ CollectedCollections</span><span class="sxs-lookup"><span data-stu-id="56f81-103">Msvm\_CollectedCollections class</span></span>

<span data-ttu-id="56f81-104">Associa [**Msvm \_ VirtualSystemCollection agli**](msvm-virtualsystemcollection.md) oggetti [**Msvm \_ ComputerSystem**](msvm-computersystem.md) contenuti.</span><span class="sxs-lookup"><span data-stu-id="56f81-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="56f81-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="56f81-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="56f81-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56f81-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a><span data-ttu-id="56f81-107">Members</span><span class="sxs-lookup"><span data-stu-id="56f81-107">Members</span></span>

<span data-ttu-id="56f81-108">La **classe Msvm \_ CollectedCollections** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="56f81-108">The **Msvm\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="56f81-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56f81-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="56f81-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56f81-110">Properties</span></span>

<span data-ttu-id="56f81-111">La **classe Msvm \_ CollectedCollections** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="56f81-111">The **Msvm\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56f81-112">**Raccolta**</span><span class="sxs-lookup"><span data-stu-id="56f81-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f81-113">Tipo di dati: **Msvm \_ ManagementCollection**</span><span class="sxs-lookup"><span data-stu-id="56f81-113">Data type: **Msvm\_ManagementCollection**</span></span>
</dt> <dt>

<span data-ttu-id="56f81-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56f81-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f81-115">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="56f81-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="56f81-116">Oggetto [**di \_ raggruppamento Msvm ManagementCollection**](msvm-managementcollection.md) o "bag" che rappresenta la raccolta.</span><span class="sxs-lookup"><span data-stu-id="56f81-116">An [**Msvm\_ManagementCollection**](msvm-managementcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="56f81-117">**Membro**</span><span class="sxs-lookup"><span data-stu-id="56f81-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f81-118">Tipo di dati: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="56f81-118">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="56f81-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="56f81-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f81-120">Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="56f81-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="56f81-121">Oggetto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) contenente i membri della raccolta.</span><span class="sxs-lookup"><span data-stu-id="56f81-121">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56f81-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56f81-122">Requirements</span></span>



| <span data-ttu-id="56f81-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="56f81-123">Requirement</span></span> | <span data-ttu-id="56f81-124">Valore</span><span class="sxs-lookup"><span data-stu-id="56f81-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56f81-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56f81-125">Minimum supported client</span></span><br/> | <span data-ttu-id="56f81-126">Windows 10 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="56f81-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="56f81-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56f81-127">Minimum supported server</span></span><br/> | <span data-ttu-id="56f81-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="56f81-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="56f81-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="56f81-129">Namespace</span></span><br/>                | <span data-ttu-id="56f81-130">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="56f81-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="56f81-131">MOF</span><span class="sxs-lookup"><span data-stu-id="56f81-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56f81-132"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="56f81-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="56f81-133">DLL</span><span class="sxs-lookup"><span data-stu-id="56f81-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56f81-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="56f81-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="56f81-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56f81-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56f81-136">**CIM \_ CollectedMSEs**</span><span class="sxs-lookup"><span data-stu-id="56f81-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

