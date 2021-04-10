---
description: Associa un'istanza di una risorsa allocata al nodo NUMA fisico dal quale è stata allocata.
ms.assetid: 811ed19f-9084-4e30-8604-860d2bf722c7
title: Classe Msvm_ElementAllocatedFromNumaNode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromNumaNode
- Msvm_ElementAllocatedFromNumaNode.Antecedent
- Msvm_ElementAllocatedFromNumaNode.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98940306f25d46c6af1be31133ee336765f8f1a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883050"
---
# <a name="msvm_elementallocatedfromnumanode-class"></a><span data-ttu-id="ba5ef-103">\_Classe MSVM ElementAllocatedFromNumaNode</span><span class="sxs-lookup"><span data-stu-id="ba5ef-103">Msvm\_ElementAllocatedFromNumaNode class</span></span>

<span data-ttu-id="ba5ef-104">Associa un'istanza di una risorsa allocata al nodo NUMA fisico dal quale è stata allocata.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-104">Associates an instance of an allocated resource with the physical NUMA node from which it was allocated.</span></span>

<span data-ttu-id="ba5ef-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba5ef-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba5ef-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromNumaNode : CIM_Dependency
{
  Msvm_NumaNode      REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ba5ef-107">Members</span><span class="sxs-lookup"><span data-stu-id="ba5ef-107">Members</span></span>

<span data-ttu-id="ba5ef-108">La **classe \_ ElementAllocatedFromNumaNode di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ba5ef-108">The **Msvm\_ElementAllocatedFromNumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="ba5ef-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba5ef-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba5ef-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba5ef-110">Properties</span></span>

<span data-ttu-id="ba5ef-111">La **classe \_ ElementAllocatedFromNumaNode di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-111">The **Msvm\_ElementAllocatedFromNumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba5ef-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ba5ef-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba5ef-113">Tipo di dati: **[ **MSVM \_ NumaNode**](msvm-numanode.md)**</span><span class="sxs-lookup"><span data-stu-id="ba5ef-113">Data type: **[**Msvm\_NumaNode**](msvm-numanode.md)**</span></span>
</dt> <dt>

<span data-ttu-id="ba5ef-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba5ef-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba5ef-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="ba5ef-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ba5ef-116">Nodo NUMA fisico.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-116">The physical NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="ba5ef-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="ba5ef-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba5ef-118">Tipo di dati: **[ **\_ LogicalElement CIM**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="ba5ef-118">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="ba5ef-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba5ef-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba5ef-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="ba5ef-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ba5ef-121">Risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-121">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba5ef-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba5ef-122">Requirements</span></span>



| <span data-ttu-id="ba5ef-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba5ef-123">Requirement</span></span> | <span data-ttu-id="ba5ef-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ba5ef-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba5ef-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba5ef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ba5ef-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ba5ef-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ba5ef-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba5ef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ba5ef-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ba5ef-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba5ef-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ba5ef-129">Namespace</span></span><br/>                | <span data-ttu-id="ba5ef-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ba5ef-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ba5ef-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ba5ef-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba5ef-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba5ef-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba5ef-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ba5ef-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba5ef-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba5ef-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

