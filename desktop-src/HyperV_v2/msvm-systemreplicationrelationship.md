---
description: Rappresenta un'associazione tra un'istanza di MSVM \_ ComputerSystem che rappresenta la macchina virtuale e un'istanza di MSVM \_ ReplicationRelationship che rappresenta una relazione di replica della macchina virtuale.
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Classe Msvm_SystemReplicationRelationship
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dd5ada4eef811a7d542c01c0a3be66d53cca0916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966496"
---
# <a name="msvm_systemreplicationrelationship-class"></a><span data-ttu-id="b7d26-103">\_Classe MSVM SystemReplicationRelationship</span><span class="sxs-lookup"><span data-stu-id="b7d26-103">Msvm\_SystemReplicationRelationship class</span></span>

<span data-ttu-id="b7d26-104">Rappresenta un'associazione tra un'istanza di [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale e un'istanza di [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) che rappresenta una relazione di replica della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b7d26-104">Represents an association between an instance of [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the virtual machine and an instance of [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) that represents a replication relationship of the virtual machine.</span></span> <span data-ttu-id="b7d26-105">Questa classe deriva dalla classe di [**\_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .</span><span class="sxs-lookup"><span data-stu-id="b7d26-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="b7d26-106">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b7d26-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d26-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7d26-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b7d26-108">Members</span><span class="sxs-lookup"><span data-stu-id="b7d26-108">Members</span></span>

<span data-ttu-id="b7d26-109">La **classe \_ SystemReplicationRelationship di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b7d26-109">The **Msvm\_SystemReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="b7d26-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b7d26-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7d26-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b7d26-111">Properties</span></span>

<span data-ttu-id="b7d26-112">La **classe \_ SystemReplicationRelationship di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b7d26-112">The **Msvm\_SystemReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7d26-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b7d26-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d26-114">Tipo di dati: **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="b7d26-114">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b7d26-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7d26-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7d26-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="b7d26-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b7d26-117">Riferimento all'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b7d26-117">Reference to the instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="b7d26-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="b7d26-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d26-119">Tipo di dati: **MSVM \_ ReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="b7d26-119">Data type: **Msvm\_ReplicationRelationship**</span></span>
</dt> <dt>

<span data-ttu-id="b7d26-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b7d26-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7d26-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. dependent")</span><span class="sxs-lookup"><span data-stu-id="b7d26-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b7d26-122">Riferimento all'istanza della classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) che rappresenta la relazione di replica di un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="b7d26-122">Reference to the instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that represents the replication relationship of a virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7d26-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7d26-123">Requirements</span></span>



| <span data-ttu-id="b7d26-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7d26-124">Requirement</span></span> | <span data-ttu-id="b7d26-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b7d26-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d26-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7d26-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d26-127">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7d26-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b7d26-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7d26-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d26-129">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7d26-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b7d26-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b7d26-130">Namespace</span></span><br/>                | <span data-ttu-id="b7d26-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b7d26-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b7d26-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b7d26-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7d26-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7d26-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7d26-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b7d26-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7d26-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b7d26-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b7d26-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7d26-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d26-137">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="b7d26-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="b7d26-138">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="b7d26-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

