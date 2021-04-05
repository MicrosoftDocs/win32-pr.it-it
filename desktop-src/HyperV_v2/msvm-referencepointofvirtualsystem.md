---
description: Associa il \_ VirtualSystemReferencePoint MSVM ai corrispondenti \_ oggetti VirtualSystem di MSVM.
ms.assetid: 5a9cb099-c0ae-4088-a64c-f2720a6cb9c8
title: Classe Msvm_ReferencePointOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystem
- Msvm_ReferencePointOfVirtualSystem.Antecedent
- Msvm_ReferencePointOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debe1931154c5c7a7868e8ee301daf977076b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756896"
---
# <a name="msvm_referencepointofvirtualsystem-class"></a><span data-ttu-id="f7c95-103">\_Classe MSVM ReferencePointOfVirtualSystem</span><span class="sxs-lookup"><span data-stu-id="f7c95-103">Msvm\_ReferencePointOfVirtualSystem class</span></span>

<span data-ttu-id="f7c95-104">Associa il [**\_ VirtualSystemReferencePoint MSVM**](msvm-virtualsystemreferencepoint.md) ai corrispondenti oggetti [**\_ VirtualSystem di MSVM**](msvm-virtualsystemresourcecomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="f7c95-104">Associates the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) to the corresponding [**Msvm\_VirtualSystem**](msvm-virtualsystemresourcecomponent.md) objects.</span></span>

<span data-ttu-id="f7c95-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f7c95-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c95-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7c95-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystem : CIM_Dependency
{
  Msvm_ComputerSystem              REF Antecedent;
  Msvm_VirtualSystemReferencePoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f7c95-107">Members</span><span class="sxs-lookup"><span data-stu-id="f7c95-107">Members</span></span>

<span data-ttu-id="f7c95-108">La **classe \_ ReferencePointOfVirtualSystem di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f7c95-108">The **Msvm\_ReferencePointOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="f7c95-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7c95-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7c95-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7c95-110">Properties</span></span>

<span data-ttu-id="f7c95-111">La **classe \_ ReferencePointOfVirtualSystem di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f7c95-111">The **Msvm\_ReferencePointOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7c95-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f7c95-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c95-113">Tipo di dati: **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="f7c95-113">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="f7c95-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7c95-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c95-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="f7c95-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f7c95-116">[**\_ ComputerSystem MSVM**](msvm-computersystem.md) che rappresenta l'oggetto indipendente in questa associazione.</span><span class="sxs-lookup"><span data-stu-id="f7c95-116">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="f7c95-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="f7c95-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c95-118">Tipo di dati: **MSVM \_ VirtualSystemReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="f7c95-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="f7c95-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7c95-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c95-120">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="f7c95-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f7c95-121">[**\_ VirtualSystemReferencePoint MSVM**](msvm-virtualsystemreferencepoint.md) che rappresenta l'oggetto dipendente dall'attività **precedente**.</span><span class="sxs-lookup"><span data-stu-id="f7c95-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7c95-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7c95-122">Requirements</span></span>



| <span data-ttu-id="f7c95-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7c95-123">Requirement</span></span> | <span data-ttu-id="f7c95-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f7c95-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c95-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7c95-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f7c95-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f7c95-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f7c95-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7c95-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f7c95-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f7c95-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f7c95-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f7c95-129">Namespace</span></span><br/>                | <span data-ttu-id="f7c95-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f7c95-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f7c95-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f7c95-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7c95-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7c95-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7c95-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f7c95-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7c95-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f7c95-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f7c95-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7c95-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c95-136">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="f7c95-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

