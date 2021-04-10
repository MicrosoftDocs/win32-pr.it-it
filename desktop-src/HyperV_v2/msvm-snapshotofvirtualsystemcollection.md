---
description: Associa MSVM \_ snapshotcollection agli oggetti MSVM VirtualSystemCollection corrispondenti \_ .
ms.assetid: 4dbfe21f-e700-4266-aedb-236c57c424f6
title: Classe Msvm_SnapshotOfVirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystemCollection
- Msvm_SnapshotOfVirtualSystemCollection.Antecedent
- Msvm_SnapshotOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae3c9c146cea8a8af98f4d3071ee7339d53eb6b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880205"
---
# <a name="msvm_snapshotofvirtualsystemcollection-class"></a><span data-ttu-id="5958b-103">\_Classe MSVM SnapshotOfVirtualSystemCollection</span><span class="sxs-lookup"><span data-stu-id="5958b-103">Msvm\_SnapshotOfVirtualSystemCollection class</span></span>

<span data-ttu-id="5958b-104">Associa [**MSVM \_ snapshotcollection**](msvm-snapshotcollection.md) agli oggetti [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="5958b-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="5958b-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5958b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5958b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5958b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5958b-107">Members</span><span class="sxs-lookup"><span data-stu-id="5958b-107">Members</span></span>

<span data-ttu-id="5958b-108">La **classe \_ SnapshotOfVirtualSystemCollection di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5958b-108">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="5958b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5958b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5958b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5958b-110">Properties</span></span>

<span data-ttu-id="5958b-111">La **classe \_ SnapshotOfVirtualSystemCollection di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5958b-111">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5958b-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5958b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5958b-113">Tipo di dati: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="5958b-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="5958b-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5958b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5958b-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="5958b-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5958b-116">[**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) che rappresenta l'oggetto indipendente in questa associazione.</span><span class="sxs-lookup"><span data-stu-id="5958b-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="5958b-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="5958b-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5958b-118">Tipo di dati **: \_ raccolta CIM**</span><span class="sxs-lookup"><span data-stu-id="5958b-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="5958b-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5958b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5958b-120">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="5958b-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5958b-121">[**\_ Raccolta CIM**](cim-collection.md) che rappresenta l'oggetto dipendente dall'attività **precedente.**</span><span class="sxs-lookup"><span data-stu-id="5958b-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent.**</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5958b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5958b-122">Requirements</span></span>



| <span data-ttu-id="5958b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5958b-123">Requirement</span></span> | <span data-ttu-id="5958b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5958b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5958b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5958b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5958b-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5958b-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5958b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5958b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5958b-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5958b-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5958b-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5958b-129">Namespace</span></span><br/>                | <span data-ttu-id="5958b-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5958b-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5958b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5958b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5958b-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5958b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5958b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5958b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5958b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5958b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5958b-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5958b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5958b-136">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="5958b-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

