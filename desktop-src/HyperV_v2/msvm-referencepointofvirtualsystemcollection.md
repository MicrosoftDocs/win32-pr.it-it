---
description: Associa il \_ ReferencePointCollection MSVM ai corrispondenti \_ oggetti VirtualSystemCollection di MSVM.
ms.assetid: 847f1f46-364f-4c91-b9e8-4740d3da1947
title: Classe Msvm_ReferencePointOfVirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystemCollection
- Msvm_ReferencePointOfVirtualSystemCollection.Antecedent
- Msvm_ReferencePointOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0919b8666915817d8475908b0305e90ea39e60f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312896"
---
# <a name="msvm_referencepointofvirtualsystemcollection-class"></a><span data-ttu-id="633cd-103">\_Classe MSVM ReferencePointOfVirtualSystemCollection</span><span class="sxs-lookup"><span data-stu-id="633cd-103">Msvm\_ReferencePointOfVirtualSystemCollection class</span></span>

<span data-ttu-id="633cd-104">Associa il [**\_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) ai corrispondenti oggetti [**\_ VirtualSystemCollection di MSVM**](msvm-virtualsystemcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="633cd-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="633cd-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="633cd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="633cd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="633cd-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="633cd-107">Members</span><span class="sxs-lookup"><span data-stu-id="633cd-107">Members</span></span>

<span data-ttu-id="633cd-108">La **classe \_ ReferencePointOfVirtualSystemCollection di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="633cd-108">The **Msvm\_ReferencePointOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="633cd-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="633cd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="633cd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="633cd-110">Properties</span></span>

<span data-ttu-id="633cd-111">La **classe \_ ReferencePointOfVirtualSystemCollection di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="633cd-111">The **Msvm\_ReferencePointOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="633cd-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="633cd-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633cd-113">Tipo di dati: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="633cd-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="633cd-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="633cd-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="633cd-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="633cd-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="633cd-116">[**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) che rappresenta l'oggetto indipendente in questa associazione.</span><span class="sxs-lookup"><span data-stu-id="633cd-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="633cd-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="633cd-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="633cd-118">Tipo di dati **: \_ raccolta CIM**</span><span class="sxs-lookup"><span data-stu-id="633cd-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="633cd-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="633cd-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="633cd-120">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="633cd-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="633cd-121">[**\_ Raccolta CIM**](cim-collection.md) che rappresenta l'oggetto dipendente dall'attività **precedente**.</span><span class="sxs-lookup"><span data-stu-id="633cd-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="633cd-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="633cd-122">Requirements</span></span>



| <span data-ttu-id="633cd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="633cd-123">Requirement</span></span> | <span data-ttu-id="633cd-124">Valore</span><span class="sxs-lookup"><span data-stu-id="633cd-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="633cd-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="633cd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="633cd-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="633cd-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="633cd-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="633cd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="633cd-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="633cd-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="633cd-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="633cd-129">Namespace</span></span><br/>                | <span data-ttu-id="633cd-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="633cd-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="633cd-131">MOF</span><span class="sxs-lookup"><span data-stu-id="633cd-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="633cd-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="633cd-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="633cd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="633cd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="633cd-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="633cd-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="633cd-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="633cd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633cd-136">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="633cd-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

