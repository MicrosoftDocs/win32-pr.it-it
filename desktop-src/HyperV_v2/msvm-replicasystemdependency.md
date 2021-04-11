---
description: Rappresenta un'associazione tra un'istanza della classe CIM \_ ComputerSystem che rappresenta la replica della macchina virtuale e un'istanza della classe CIM \_ ComputerSystem che rappresenta la replica della macchina virtuale di test.
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Classe Msvm_ReplicaSystemDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8c0db6e476cb883ee1179fcfcc9ac4b212f0b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231746"
---
# <a name="msvm_replicasystemdependency-class"></a><span data-ttu-id="b013f-103">\_Classe MSVM ReplicaSystemDependency</span><span class="sxs-lookup"><span data-stu-id="b013f-103">Msvm\_ReplicaSystemDependency class</span></span>

<span data-ttu-id="b013f-104">Rappresenta un'associazione tra un'istanza della classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la replica della macchina virtuale e un'istanza della classe **CIM \_ ComputerSystem** che rappresenta la replica della macchina virtuale di test.</span><span class="sxs-lookup"><span data-stu-id="b013f-104">Represents an association between an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica and an instance of the **CIM\_ComputerSystem** class that represents the test virtual machine replica.</span></span>

<span data-ttu-id="b013f-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b013f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b013f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b013f-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b013f-107">Members</span><span class="sxs-lookup"><span data-stu-id="b013f-107">Members</span></span>

<span data-ttu-id="b013f-108">La **classe \_ ReplicaSystemDependency di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b013f-108">The **Msvm\_ReplicaSystemDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="b013f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b013f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b013f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b013f-110">Properties</span></span>

<span data-ttu-id="b013f-111">La **classe \_ ReplicaSystemDependency di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b013f-111">The **Msvm\_ReplicaSystemDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b013f-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b013f-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b013f-113">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="b013f-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b013f-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b013f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b013f-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="b013f-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b013f-116">Riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la replica della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b013f-116">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica.</span></span> <span data-ttu-id="b013f-117">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="b013f-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="b013f-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="b013f-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b013f-119">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="b013f-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b013f-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b013f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b013f-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. dependent")</span><span class="sxs-lookup"><span data-stu-id="b013f-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b013f-122">Riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la replica della macchina virtuale di test creata dal metodo [**MSVM \_ ReplicationService. TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b013f-122">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the test virtual machine replica created by the [**Msvm\_ReplicationService.TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) method.</span></span> <span data-ttu-id="b013f-123">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="b013f-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b013f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b013f-124">Requirements</span></span>



| <span data-ttu-id="b013f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b013f-125">Requirement</span></span> | <span data-ttu-id="b013f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b013f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b013f-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b013f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b013f-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b013f-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b013f-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b013f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b013f-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b013f-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b013f-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b013f-131">Namespace</span></span><br/>                | <span data-ttu-id="b013f-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b013f-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b013f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b013f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b013f-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b013f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b013f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b013f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b013f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b013f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

