---
description: Associa il \_ ReferencePointCollection MSVM agli oggetti contenuti MSVM \_ VirtualSystemReferencePoint.
ms.assetid: 826125c3-0a89-4573-ac28-88588eac248d
title: Classe Msvm_CollectedReferencePoints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedReferencePoints
- Msvm_CollectedReferencePoints.Collection
- Msvm_CollectedReferencePoints.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4891d4ec4c613c92c3b5d5a090f2683bfc77dc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753023"
---
# <a name="msvm_collectedreferencepoints-class"></a><span data-ttu-id="afe1e-103">\_Classe MSVM CollectedReferencePoints</span><span class="sxs-lookup"><span data-stu-id="afe1e-103">Msvm\_CollectedReferencePoints class</span></span>

<span data-ttu-id="afe1e-104">Associa il [**\_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) agli oggetti contenuti [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) .</span><span class="sxs-lookup"><span data-stu-id="afe1e-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the contained [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) objects.</span></span>

<span data-ttu-id="afe1e-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="afe1e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="afe1e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afe1e-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedReferencePoints : CIM_CollectedMSEs
{
  Msvm_ReferencePointCollection    REF Collection;
  Msvm_VirtualSystemReferencePoint REF Member;
};
```

## <a name="members"></a><span data-ttu-id="afe1e-107">Members</span><span class="sxs-lookup"><span data-stu-id="afe1e-107">Members</span></span>

<span data-ttu-id="afe1e-108">La **classe \_ CollectedReferencePoints di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="afe1e-108">The **Msvm\_CollectedReferencePoints** class has these types of members:</span></span>

-   [<span data-ttu-id="afe1e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="afe1e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="afe1e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="afe1e-110">Properties</span></span>

<span data-ttu-id="afe1e-111">La **classe \_ CollectedReferencePoints di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="afe1e-111">The **Msvm\_CollectedReferencePoints** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afe1e-112">**Raccolta**</span><span class="sxs-lookup"><span data-stu-id="afe1e-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afe1e-113">Tipo di dati: **MSVM \_ ReferencePointCollection**</span><span class="sxs-lookup"><span data-stu-id="afe1e-113">Data type: **Msvm\_ReferencePointCollection**</span></span>
</dt> <dt>

<span data-ttu-id="afe1e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="afe1e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afe1e-115">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="afe1e-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="afe1e-116">Oggetto di raggruppamento o ' contenitore ' di [**MSVM \_ ReferencePointCollection**](msvm-referencepointcollection.md) che rappresenta la raccolta.</span><span class="sxs-lookup"><span data-stu-id="afe1e-116">An [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="afe1e-117">**Membro**</span><span class="sxs-lookup"><span data-stu-id="afe1e-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afe1e-118">Tipo di dati: **MSVM \_ VirtualSystemReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="afe1e-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="afe1e-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="afe1e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afe1e-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="afe1e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="afe1e-121">[**\_ VirtualSystemReferencePoint MSVM**](msvm-virtualsystemreferencepoint.md) contenente i membri della raccolta.</span><span class="sxs-lookup"><span data-stu-id="afe1e-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="afe1e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afe1e-122">Requirements</span></span>



| <span data-ttu-id="afe1e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="afe1e-123">Requirement</span></span> | <span data-ttu-id="afe1e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="afe1e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afe1e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afe1e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="afe1e-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="afe1e-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="afe1e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afe1e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="afe1e-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="afe1e-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="afe1e-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="afe1e-129">Namespace</span></span><br/>                | <span data-ttu-id="afe1e-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="afe1e-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="afe1e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="afe1e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afe1e-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afe1e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="afe1e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="afe1e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afe1e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="afe1e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="afe1e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afe1e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe1e-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="afe1e-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

