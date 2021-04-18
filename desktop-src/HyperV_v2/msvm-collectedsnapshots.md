---
description: Associa MSVM \_ snapshotcollection agli oggetti VirtualSystemSettingData MSVM contenuti \_ .
ms.assetid: 21005e8a-0bc6-4ea7-8f6f-d79803b43bc0
title: Classe Msvm_CollectedSnapshots
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedSnapshots
- Msvm_CollectedSnapshots.Collection
- Msvm_CollectedSnapshots.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9c89e7c7390cc1f2cc0c3217fca93e3f2d2d01ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308911"
---
# <a name="msvm_collectedsnapshots-class"></a><span data-ttu-id="e8521-103">\_Classe MSVM CollectedSnapshots</span><span class="sxs-lookup"><span data-stu-id="e8521-103">Msvm\_CollectedSnapshots class</span></span>

<span data-ttu-id="e8521-104">Associa [**MSVM \_ snapshotcollection**](msvm-snapshotcollection.md) agli oggetti [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) contenuti.</span><span class="sxs-lookup"><span data-stu-id="e8521-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the contained [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) objects.</span></span>

<span data-ttu-id="e8521-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e8521-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8521-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8521-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedSnapshots : CIM_CollectedMSEs
{
  Msvm_SnapshotCollection       REF Collection;
  Msvm_VirtualSystemSettingData REF Member;
};
```

## <a name="members"></a><span data-ttu-id="e8521-107">Members</span><span class="sxs-lookup"><span data-stu-id="e8521-107">Members</span></span>

<span data-ttu-id="e8521-108">La **classe \_ CollectedSnapshots di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e8521-108">The **Msvm\_CollectedSnapshots** class has these types of members:</span></span>

-   [<span data-ttu-id="e8521-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e8521-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8521-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e8521-110">Properties</span></span>

<span data-ttu-id="e8521-111">La **classe \_ CollectedSnapshots di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e8521-111">The **Msvm\_CollectedSnapshots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8521-112">**Raccolta**</span><span class="sxs-lookup"><span data-stu-id="e8521-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8521-113">Tipo di dati: **MSVM \_ snapshotcollection**</span><span class="sxs-lookup"><span data-stu-id="e8521-113">Data type: **Msvm\_SnapshotCollection**</span></span>
</dt> <dt>

<span data-ttu-id="e8521-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8521-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8521-115">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="e8521-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="e8521-116">Un oggetto Grouping o ' Bag ' di [**MSVM \_ snapshotcollection**](msvm-snapshotcollection.md) che rappresenta la raccolta.</span><span class="sxs-lookup"><span data-stu-id="e8521-116">An [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="e8521-117">**Membro**</span><span class="sxs-lookup"><span data-stu-id="e8521-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8521-118">Tipo di dati: **MSVM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="e8521-118">Data type: **Msvm\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="e8521-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e8521-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8521-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="e8521-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="e8521-121">[**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) contenente i membri della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e8521-121">An [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8521-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8521-122">Requirements</span></span>



| <span data-ttu-id="e8521-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8521-123">Requirement</span></span> | <span data-ttu-id="e8521-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e8521-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8521-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8521-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e8521-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e8521-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e8521-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8521-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e8521-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e8521-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e8521-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e8521-129">Namespace</span></span><br/>                | <span data-ttu-id="e8521-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e8521-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e8521-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e8521-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8521-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8521-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8521-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e8521-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8521-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e8521-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e8521-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8521-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8521-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="e8521-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

